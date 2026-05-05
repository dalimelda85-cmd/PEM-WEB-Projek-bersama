# PEM-WEB-Projek-bersama
<!DOCTYPE html> 
<!-- Menentukan dokumen HTML5 -->

<html lang="id"> 
<!-- Bahasa halaman Indonesia -->

<head>
    <meta charset="UTF-8"> 
    <!-- Encoding karakter agar teks tampil benar -->

    <title>Form Data Mahasiswa</title> 
    <!-- Judul halaman -->

    <style>
        body {
            font-family: Arial; 
            /* Mengatur font */

            margin: 20px; 
            /* Jarak luar halaman */

            background: #f5f5f5; 
            /* Warna background */
        }

        form {
            background: #fff; 
            /* Background form putih */

            padding: 20px; 
            /* Jarak dalam */

            border-radius: 10px; 
            /* Sudut melengkung */

            margin-bottom: 20px;
        }

        input, textarea, select {
            width: 100%; 
            /* Lebar penuh */

            padding: 8px;

            margin: 5px 0 15px;
        }

        button {
            padding: 10px;
            margin-right: 5px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .submit { background: green; color: white; }
        .reset { background: orange; color: white; }

        table {
            width: 100%;
            border-collapse: collapse;
            background: #fff;
        }

        th, td {
            border: 1px solid #ccc;
            padding: 10px;
            text-align: center;
        }

        img {
            cursor: pointer;
        }
    </style>
</head>

<body>

<h2>Form Data Mahasiswa</h2>
<!-- Judul form -->

<form id="formMahasiswa">
<!-- Form input data -->

    <label>NIM</label>
    <input type="text" id="nim" required>
    <!-- Input NIM (wajib diisi) -->

    <label>Nama</label>
    <input type="text" id="nama" required>
    <!-- Input nama (wajib diisi) -->

    <label>Alamat</label>
    <textarea id="alamat"></textarea>
    <!-- Input alamat -->

    <label>Jenis Kelamin</label><br>
    <!-- Pilihan jenis kelamin -->

    <input type="radio" name="jk" value="Pria"> Pria
    <input type="radio" name="jk" value="Wanita"> Wanita
    <input type="radio" name="jk" value="Lainnya"> Lainnya

    <!-- 🐞 BUG 4: Tidak ada validasi jenis kelamin
    Jika user tidak memilih JK, program tetap berjalan dan mengisi "-" -->

    <br><br>

    <label>Tanggal Lahir</label>

    <select id="tanggal"></select>
    <!-- Akan diisi otomatis oleh JavaScript -->

    <select id="bulan">
        <option value="01">Januari</option>
        <option value="02">Februari</option>
        <option value="03">Maret</option>
        <option value="04">April</option>
        <option value="05">Mei</option>
        <option value="06">Juni</option>
        <option value="07">Juli</option>
        <option value="08">Agustus</option>
        <option value="09">September</option>
        <option value="10">Oktober</option>
        <option value="11">November</option>
        <option value="12">Desember</option>
    </select>

    <select id="tahun"></select>
    <!-- Akan diisi otomatis oleh JavaScript -->

    <label>Password</label>
    <input type="password" id="password">
    <!-- 🐞 BUG: password tidak wajib diisi -->

    <button type="submit" class="submit">Submit</button>
    <button type="reset" class="reset">Reset</button>
</form>

<h2>Data Mahasiswa</h2>

<table>
    <thead>
        <tr>
            <th>NIM</th>
            <th>Nama</th>
            <th>Alamat</th>
            <th>JK</th>
            <th>TTL</th>
            <th>Password</th>
            <th>Aksi</th>
        </tr>
    </thead>

    <tbody id="tableBody"></tbody>
    <!-- Data ditampilkan di sini -->
</table>

<script>
    const form = document.getElementById("formMahasiswa");
    const tableBody = document.getElementById("tableBody");

    // Mengisi dropdown tanggal 1–31
    for (let i = 1; i <= 31; i++) {
        document.getElementById("tanggal").innerHTML += 
        `<option value="${i}">${i}</option>`;
    }

    // Mengisi dropdown tahun 1990–2025
    for (let i = 1990; i <= 2025; i++) {
        document.getElementById("tahun").innerHTML += 
        `<option value="${i}">${i}</option>`;
    }

    form.addEventListener("submit", function(e) {
        e.preventDefault();
        // Mencegah halaman reload

        const nim = document.getElementById("nim").value;
        const nama = document.getElementById("nama").value;
        const alamat = document.getElementById("alamat").value;

        /*
        🐞 BUG 4: Validasi jenis kelamin tidak ada
        Jika tidak dipilih, tetap lanjut dengan nilai "-"
        */
        const jk = document.querySelector('input[name="jk"]:checked')?.value || "-";

        const tanggal = document.getElementById("tanggal").value;
        const bulan = document.getElementById("bulan").value;
        const tahun = document.getElementById("tahun").value;

        const ttl = `${tanggal}-${bulan}-${tahun}`;
        const password = document.getElementById("password").value;

        const row = document.createElement("tr");

        row.innerHTML = `
            <td>${nim}</td>
            <td>${nama}</td>
            <td>${alamat}</td>
            <td>${jk}</td>
            <td>${ttl}</td>

            <!-- 🐞 BUG 3: Password ditampilkan langsung di tabel
            Ini tidak aman karena password adalah data sensitif -->

            <td>${password}</td>

            <td>
                <a href="#" onclick="editRow(this)">
                    <img src="edit.png" width="20">
                </a>

                <!-- 🐞 BUG 1: Ikon tidak muncul jika file tidak ada
                Solusi: gunakan emoji atau CDN -->

                <a href="#" onclick="deleteRow(this)">
                    <img src="trash.png" width="20">
                </a>

                <!-- 🐞 BUG 5: href="#" bisa menyebabkan halaman loncat ke atas -->
            </td>
        `;

        tableBody.appendChild(row);

        // 🐞 BUG 7: Data tidak disimpan (hilang saat refresh karena tidak pakai localStorage)

        form.reset();
    });

    function deleteRow(el) {
        // 🐞 BUG 8: Tidak ada konfirmasi sebelum hapus
        el.parentElement.parentElement.remove();
    }

    function editRow(el) {
        const row = el.parentElement.parentElement;
        const cells = row.children;

        document.getElementById("nim").value = cells[0].innerText;
        document.getElementById("nama").value = cells[1].innerText;
        document.getElementById("alamat").value = cells[2].innerText;

        /*
        🐞 BUG 2: Edit tidak lengkap
        Jenis kelamin dan TTL tidak dikembalikan ke form
        */

        document.getElementById("password").value = cells[5].innerText;

        row.remove();
    }
</script>

</body>
</html>
