# PEM-WEB-Projek-bersama
####
Nama :
1. Fadhlulloh Yusron Almanshurin
2. Andi Hani Tuzlimatul Izzati
3. Clara Ganesia
4. Melda Dali
#

    <!DOCTYPE html> 
### Menentukan dokumen HTML5
Fungsi utama <!DOCTYPE html> adalah agar browser dapat membaca dan menampilkan halaman web sesuai standar HTML modern. Jika deklarasi ini tidak ditambahkan, browser bisa menampilkan halaman dalam mode kompatibilitas lama sehingga tampilan atau fungsi website mungkin tidak berjalan dengan baik.

#
    <html lang="id"> 
    
Tag `<html>` adalah elemen utama (root) dalam dokumen HTML yang membungkus seluruh isi halaman web.

Atribut `lang="id"` digunakan untuk menentukan bahasa yang digunakan pada halaman tersebut, yaitu Bahasa Indonesia.
#

    <head>
    <meta charset="UTF-8"> 

Encoding karakter agar teks tampil benar

Penjelasan Tag `head` dan <meta `charset="UTF-8">` dalam HTML

Tag <head> adalah bagian dari dokumen HTML yang berisi informasi tentang halaman web. Informasi ini tidak ditampilkan langsung kepada pengguna, tetapi digunakan oleh browser untuk mengatur dan memahami halaman.

Salah satu elemen penting di dalam <head> adalah:

<meta `charset="UTF-8">`

Tag `<meta charset="UTF-8">` digunakan untuk menentukan jenis encoding karakter yang digunakan pada halaman web. Encoding UTF-8 memungkinkan halaman menampilkan berbagai jenis karakter, seperti:

Huruf (A-Z, a-z)
Angka
Simbol
Emoji
Berbagai bahasa (Indonesia, Arab, Jepang, dll)

Dengan menggunakan UTF-8, teks pada halaman web akan tampil dengan benar dan tidak mengalami error atau karakter aneh.
#
      <title>Form Data Mahasiswa</title> 
### Judul halaman
Tag `<title>` digunakan untuk menentukan judul halaman web yang akan ditampilkan pada tab browser.

#### Penjelasan
- `<title>` berisi nama atau judul halaman.
- Teks "Form Data Mahasiswa" akan muncul di bagian atas tab browser.
- Judul ini juga digunakan oleh mesin pencari (SEO) sebagai nama halaman di hasil pencarian.
#### Fungsi <title>
- Menampilkan nama halaman di tab browser.
- Membantu pengguna mengenali isi halaman.
- Mendukung optimasi mesin pencari (SEO).

#

    <style>
        body {
            font-family: Arial; 
            margin: 20px; 
            background: #f5f5f5; 
        }
Tag `<style>` digunakan untuk menuliskan CSS (Cascading Style Sheets) langsung di dalam file HTML. CSS berfungsi untuk mengatur tampilan atau desain halaman web.
Penjelasan
- `body`
Selector yang digunakan untuk mengatur seluruh isi halaman web.
- `font-family: Arial;`
Mengatur jenis huruf (font) yang digunakan menjadi Arial.
- `margin: 20px;`
Memberikan jarak antara isi halaman dengan tepi browser sebesar 20 pixel.
- `background: #f5f5f5;`
Mengatur warna latar belakang halaman menjadi abu-abu muda.
#
        form {
            background: #fff; 
            padding: 20px; 
            border-radius: 10px; 
            margin-bottom: 20px;
        }

### Styling Form
Digunakan untuk mempercantik tampilan form agar lebih rapi dan nyaman digunakan.

- `background: #fff;` → Warna putih agar terlihat bersih
- `padding: 20px;` → Jarak isi ke dalam agar tidak menempel
- `border-radius: 10px;` → Sudut melengkung (modern)
- `margin-bottom: 20px;` → Jarak dengan elemen bawah

#
        input, textarea, select {
            width: 100%; 
            padding: 8px;
            margin: 5px 0 15px;
        }

### Styling Input
- `width: 100%;`  
  Mengatur lebar elemen menjadi **100% dari container (wadahnya)**.  
  Tujuannya agar semua input memiliki ukuran yang sama dan terlihat sejajar.

- `padding: 8px;`  
  Memberikan **jarak di dalam elemen (inner spacing)** antara teks dengan border.  
  Ini membuat input lebih nyaman saat digunakan (tidak terlalu sempit).

- `margin: 5px 0 15px;`  
  Memberikan **jarak antar elemen (outer spacing)**:
  - `5px` → jarak atas
  - `0` → kiri dan kanan
  - `15px` → jarak bawah  
  Tujuannya agar tampilan tidak terlalu rapat dan lebih mudah dibaca.

#
        button {
            padding: 10px;
            margin-right: 5px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

### Styling Button
Digunakan untuk mengatur tampilan tombol agar lebih menarik, mudah digunakan, dan terlihat modern.

- `padding: 10px;`  
  Memberikan **ruang di dalam tombol** sehingga ukuran tombol menjadi lebih besar dan nyaman diklik.

- `margin-right: 5px;`  
  Memberikan **jarak antar tombol**, agar tombol tidak saling menempel.

- `border: none;`  
  Menghilangkan garis tepi default pada tombol sehingga tampilannya lebih bersih.

- `border-radius: 5px;`  
  Membuat **sudut tombol menjadi melengkung (rounded)** agar terlihat lebih modern.

- `cursor: pointer;`  
  Mengubah kursor menjadi **ikon tangan** saat diarahkan ke tombol, menandakan bahwa tombol bisa diklik.


#
        .submit { background: green; color: white; }
        .reset { background: orange; color: white; }

### Warna Tombol
Digunakan untuk membedakan fungsi tombol berdasarkan warna.

#### Penjelasan:

- `.submit`  
  - `background: green;` → Warna hijau melambangkan aksi **simpan / kirim data**  
  - `color: white;` → Teks putih agar kontras dan mudah dibaca  

- `.reset`  
  - `background: orange;` → Warna oranye sebagai tanda aksi **menghapus / mengulang input**  
  - `color: white;` → Teks tetap jelas terlihat  

#
        table {
            width: 100%;
            border-collapse: collapse;
            background: #fff;
        }

### Styling Tabel
- `width: 100%;`  
  Membuat tabel memenuhi lebar halaman.

- `border-collapse: collapse;`  
  Menggabungkan garis tabel agar tidak terlihat double (lebih rapi).

- `background: #fff;`  
  Memberikan warna latar putih agar kontras dengan halaman.

#
        th, td {
            border: 1px solid #ccc;
            padding: 10px;
            text-align: center;
        }

### Styling Isi Tabel (th & td)
Digunakan untuk mengatur tampilan isi tabel.

#### Penjelasan Properti:

- `border: 1px solid #ccc;`  
  Memberikan garis tipis berwarna abu-abu pada setiap sel tabel.

- `padding: 10px;`  
  Memberikan jarak di dalam sel agar teks tidak terlalu rapat.

- `text-align: center;`  
  Membuat teks berada di tengah (horizontal).

#
        img {
            cursor: pointer;
        }

### Styling Gambar (Icon)
Digunakan untuk ikon seperti tombol **edit** dan **delete** pada tabel.
- `cursor: pointer;`  
  Mengubah kursor menjadi **ikon tangan** saat diarahkan ke gambar.  
  Ini menandakan bahwa gambar tersebut **bisa diklik (interaktif)**.
#
        </style>
        </head>
        <body>
### Penutup Bagian Head & Awal Body
- `</style>`  
  Menandakan **akhir dari penulisan CSS** di dalam tag `<style>`.  
  Semua aturan styling sudah selesai ditulis sebelum tag ini ditutup.

- `</head>`  
  Menandakan **akhir dari bagian head** dalam dokumen HTML.  
  Bagian `<head>` berisi informasi seperti:
  - Judul halaman (`<title>`)
  - Metadata (`<meta>`)
  - Styling (`<style>`)

- `<body>`  
  Menandakan **awal dari isi halaman web yang akan ditampilkan ke pengguna**.
  
#
    <h2>Form Data Mahasiswa</h2>

### Judul Form
Digunakan sebagai **judul utama halaman**.

- Tag `<h2>` → heading ukuran sedang
- Menjelaskan isi form kepada pengguna

#
    <form id="formMahasiswa">

### Form Input Data
Digunakan sebagai wadah untuk semua input data mahasiswa.
- `id="formMahasiswa"` → digunakan untuk diakses oleh JavaScript

#
    <label>NIM</label>
    <input type="text" id="nim" required>

### Input NIM
Digunakan untuk memasukkan Nomor Induk Mahasiswa.

- `<label>NIM</label>`  
  Digunakan sebagai **teks penjelas** untuk input.  
  Membantu pengguna mengetahui data apa yang harus diisi.

- `<input type="text">`  
  Digunakan untuk menerima **input berupa teks** dari pengguna.

- `id="nim"`  
  Digunakan sebagai **identitas unik** untuk elemen input.  
  Biasanya dipakai oleh JavaScript untuk mengambil nilai input.

- `required`  
  Menandakan bahwa input ini **wajib diisi** sebelum form bisa dikirim.

#
    <label>Nama</label>
    <input type="text" id="nama" required>

### Input Nama
Digunakan untuk memasukkan **nama mahasiswa**.

- `type="text"`  
  Menentukan bahwa input menerima **data berupa teks** (huruf, angka, simbol).

- `id="nama"`  
  Digunakan sebagai **identitas unik** dari input.  
  Biasanya dipakai oleh JavaScript untuk mengambil nilai yang dimasukkan user.

- `required`  
  Menandakan bahwa field ini **wajib diisi** sebelum form dapat disubmit.

#
    <label>Alamat</label>
    <textarea id="alamat"></textarea>

### Input Alamat
Digunakan untuk memasukkan **alamat mahasiswa**.
- `<textarea>` digunakan untuk input teks panjang (lebih fleksibel dibanding input biasa)
- `id="alamat"` digunakan untuk mengambil data melalui JavaScript

#
    <label>Jenis Kelamin</label><br>

    <input type="radio" name="jk" value="Pria"> Pria
    <input type="radio" name="jk" value="Wanita"> Wanita
    <input type="radio" name="jk" value="Lainnya"> Lainnya

### Input Jenis Kelamin
- `type="radio"` → hanya bisa memilih satu opsi
- `name="jk"` → mengelompokkan pilihan
- `value` → nilai yang akan dikirim ke JavaScript

❌ BUG 1: Tidak ada validasi  
User bisa tidak memilih

✅ Solusi:
```javascript
const jkSelected = document.querySelector('input[name="jk"]:checked');
if (!jkSelected) {
    alert("Pilih jenis kelamin!");
    return;
}
```

#
    <label>Tanggal Lahir</label>
    <select id="tanggal"></select>

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

### Input Tanggal Lahir
Digunakan untuk memasukkan **tanggal lahir mahasiswa** menggunakan dropdown.

#### Struktur Input:
Terdiri dari 3 bagian:
1. **Tanggal (`select id="tanggal"`)**
2. **Bulan (`select id="bulan"`)**
3. **Tahun (`select id="tahun"`)**

#### Penjelasan Tiap Bagian:

- `<label>Tanggal Lahir</label>`  
  Berfungsi sebagai **penjelas input** agar user tahu data apa yang harus diisi.
- `<select id="tanggal"></select>`  
  Dropdown untuk memilih **tanggal (1–31)**.  
  Nilainya akan diisi otomatis menggunakan JavaScript.
- `<select id="bulan">...</select>`  
  Dropdown untuk memilih **bulan**.
  - `<option>` → pilihan yang tersedia
  - `value="01"` → nilai yang dikirim (format angka)
  - "Januari" → teks yang ditampilkan ke user
- `<select id="tahun"></select>`  
  Dropdown untuk memilih **tahun lahir**.  
  Diisi otomatis oleh JavaScript (misalnya 1990–2025).
#### Kelebihan:
- Menghindari kesalahan format tanggal
- Lebih mudah digunakan dibanding input manual
- Konsisten (format selalu sama)
❌ **Potensi BUG: User tidak memilih tanggal**
Jika tidak diberi validasi, user bisa submit tanpa memilih tanggal.
✅ **Solusi Validasi:**
```javascript
        if (!tanggal || !bulan || !tahun) {
            alert("Lengkapi tanggal lahir!");
            return;
        }
```
#
    <label>Password</label>
    <input type="password" id="password">

### Input Password
- `type="password"` → menyembunyikan karakter saat diketik
- Digunakan untuk data sensitif
  
❌ BUG 2: Tidak wajib diisi

✅ Solusi:
```html
<input type="password" id="password" required>
```

#
    <button type="submit" class="submit">Submit</button>
    <button type="reset" class="reset">Reset</button>

### Tombol
- `submit` → mengirim data ke tabel
- `reset` → mengosongkan form

#
    </form>
    <h2>Data Mahasiswa</h2>
    
### Penutup Form & Judul Tabel

- `</form>`  
  Menandakan **akhir dari form input data mahasiswa**.  
  Semua elemen seperti input, textarea, radio button, dan tombol berada di dalam tag `<form>` ini.

- `<h2>Data Mahasiswa</h2>`  
  Digunakan sebagai **judul untuk bagian tabel data** yang akan ditampilkan di bawah form.

### Tabel Data Mahasiswa

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

### Struktur Tabel (Header)

- `<table>`  
  Digunakan untuk membuat **tabel** sebagai tempat menampilkan data mahasiswa.

- `<thead>`  
  Menandakan bagian **kepala tabel (header)**.  
  Biasanya berisi judul kolom.

- `<tr>` (*table row*)  
  Digunakan untuk membuat **baris** pada tabel.

- `<th>` (*table header*)  
  Digunakan untuk membuat **judul kolom** pada tabel.

#### Penjelasan Kolom:

- `NIM` → Nomor Induk Mahasiswa  
- `Nama` → Nama mahasiswa  
- `Alamat` → Alamat mahasiswa  
- `JK` → Jenis Kelamin  
- `TTL` → Tanggal Lahir  
- `Password` → Password (⚠ data sensitif)  
- `Aksi` → Tombol untuk edit & hapus data  

---

❌ **BUG / Kekurangan: Password ditampilkan di tabel**

Menampilkan password secara langsung sangat berbahaya karena termasuk **data sensitif**.

✅ **Solusi:**
Ganti tampilan password menjadi simbol tersembunyi:

```javascript
<td>******</td>
```
#
    <tbody id="tableBody"></tbody>
    </table>

### Body Tabel & Penutup Tabel
- `<tbody>`  
  Digunakan untuk menampung **isi/data tabel** yang akan ditampilkan.

- `id="tableBody"`  
  Berfungsi sebagai **identitas unik** agar bisa diakses oleh JavaScript.  
  Data dari form akan dimasukkan ke dalam bagian ini secara dinamis.

- `</tbody>`  
  Menandakan akhir dari isi tabel.

- `</table>`  
  Menandakan akhir dari keseluruhan tabel.

---

#### Cara Kerja:
- Saat user mengisi form dan menekan tombol **Submit**
- JavaScript akan membuat baris baru (`<tr>`)
- Lalu data akan dimasukkan ke dalam `<tbody id="tableBody">`

#
    /<script>
    const form = document.getElementById("formMahasiswa");
    const tableBody = document.getElementById("tableBody");
### Inisialisasi JavaScript
- `<script>`  
  Digunakan untuk memulai penulisan **kode JavaScript** di dalam HTML.

---

- `const form = document.getElementById("formMahasiswa");`  
  Digunakan untuk mengambil elemen `<form>` berdasarkan `id`.

  Fungsi:
  - Menghubungkan HTML dengan JavaScript
  - Digunakan untuk menangani event seperti submit

---

- `const tableBody = document.getElementById("tableBody");`  
  Digunakan untuk mengambil bagian `<tbody>` pada tabel.

  Fungsi:
  - Menjadi tempat untuk menampilkan data mahasiswa
  - Digunakan saat menambahkan baris baru ke tabel
    
#
Mengisi dropdown tanggal 1–31

    for (let i = 1; i <= 31; i++) {
        document.getElementById("tanggal").innerHTML += 
        `<option value="${i}">${i}</option>`;
    }
### Generate Dropdown Tanggal

- `for (let i = 1; i <= 31; i++)`  
  Perulangan untuk membuat angka dari **1 sampai 31** (jumlah hari dalam sebulan).

- `document.getElementById("tanggal")`  
  Mengambil elemen `<select id="tanggal">` dari HTML.

- `innerHTML +=`  
  Menambahkan isi baru ke dalam elemen tanpa menghapus isi sebelumnya.

- `` `<option value="${i}">${i}</option>` ``  
  Membuat elemen `<option>` secara dinamis:
  - `value="${i}"` → nilai yang dikirim
  - `${i}` → teks yang ditampilkan

---

#### Hasil:
Dropdown tanggal akan berisi:
1, 2, 3, ..., sampai 31

#
Mengisi dropdown tahun 1990–2025

    for (let i = 1990; i <= 2025; i++) {
        document.getElementById("tahun").innerHTML += 
        `<option value="${i}">${i}</option>`;
    }

#
    form.addEventListener("submit", function(e) {
        e.preventDefault();
## Generate Dropdown Tahun

- `for (let i = 1990; i <= 2025; i++)`  
  Perulangan untuk membuat daftar tahun dari **1990 sampai 2025**.

- `document.getElementById("tahun")`  
  Mengambil elemen `<select id="tahun">` dari HTML.

- `innerHTML +=`  
  Digunakan untuk menambahkan isi ke dalam dropdown tanpa menghapus data sebelumnya.

- `` `<option value="${i}">${i}</option>` ``  
  Membuat pilihan tahun:
  - `value="${i}"` → nilai yang dikirim
  - `${i}` → teks yang ditampilkan

#### Hasil:
Dropdown akan berisi:
1990, 1991, 1992, ..., sampai 2025

❌ **BUG / Kekurangan: Tahun statis (tidak update otomatis)**

Jika tahun sudah melewati 2025, maka:
- Dropdown akan menjadi **tidak relevan**
- Harus diubah manual di kode

✅ **Solusi (lebih fleksibel):**
Gunakan tahun saat ini secara otomatis:

```javascript
const currentYear = new Date().getFullYear();

for (let i = 1990; i <= currentYear; i++) {
    document.getElementById("tahun").innerHTML += 
    `<option value="${i}">${i}</option>`;
}
```

#### Kelebihan Solusi:
- Selalu update otomatis
- Tidak perlu ubah kode setiap tahun
- Lebih profesional
### Event Submit
Mencegah reload halaman

#
        const nim = document.getElementById("nim").value;
        const nama = document.getElementById("nama").value;
        const alamat = document.getElementById("alamat").value;
        const jk = document.querySelector('input[name="jk"]:checked')?.value || "-";
### Mengambil Data Input + Jenis Kelamin

- `document.getElementById("nim").value`  
  Mengambil nilai NIM dari input.

- `document.getElementById("nama").value`  
  Mengambil nilai nama.

- `document.getElementById("alamat").value`  
  Mengambil nilai alamat.

- `document.querySelector('input[name="jk"]:checked')`  
  Digunakan untuk mengambil **radio button yang dipilih** (checked).

- `?.value` *(optional chaining)*  
  Jika ada yang dipilih → ambil nilainya  
  Jika tidak ada → tidak error (undefined)

- `|| "-"`  
  Jika tidak ada pilihan, maka nilai default menjadi `"-"`

#### Fungsi:
Digunakan untuk mengambil semua data input termasuk **jenis kelamin**.

❌ **BUG: Jenis kelamin bisa kosong**

Jika user tidak memilih:
- Tidak ada error
- Program tetap jalan
- Nilai otomatis menjadi `"-"`

➡ Ini berbahaya karena:
- Data menjadi tidak valid
- User tidak dipaksa mengisi
  
✅ **Solusi (validasi wajib pilih):**
```javascript
const jkSelected = document.querySelector('input[name="jk"]:checked');

if (!jkSelected) {
    alert("Pilih jenis kelamin!");
    return;
}

const jk = jkSelected.value;
```

❌ **BUG Tambahan: Validasi input lain masih kurang**

Data seperti:
- NIM
- Nama

Masih bisa berisi spasi kosong.

✅ **Solusi tambahan:**
```javascript
if (!nim.trim() || !nama.trim()) {
    alert("NIM dan Nama wajib diisi!");
    return;
}
```

# 

        const tanggal = document.getElementById("tanggal").value;
        const bulan = document.getElementById("bulan").value;
        const tahun = document.getElementById("tahun").value;
### Mengambil Data Tanggal Lahir

#### Penjelasan:

- `document.getElementById("tanggal").value`  
  Mengambil nilai **tanggal (1–31)** dari dropdown.

- `document.getElementById("bulan").value`  
  Mengambil nilai **bulan (01–12)** dari dropdown.

- `document.getElementById("tahun").value`  
  Mengambil nilai **tahun** dari dropdown.

---

#### Fungsi:
Digunakan untuk mengambil data tanggal lahir yang dipilih user, yang nantinya akan digabung menjadi satu format (TTL).

---

#### Contoh Hasil:
Jika user memilih:
- Tanggal: 10  
- Bulan: 05  
- Tahun: 2003  

Maka akan menjadi:
```
10-05-2003
```

---

❌ **BUG / Kekurangan: Tidak ada validasi**

User bisa saja:
- Tidak memilih tanggal
- Tidak memilih tahun

➡ Data tetap diproses meskipun tidak lengkap

---

✅ **Solusi (validasi input):**
```javascript
if (!tanggal || !bulan || !tahun) {
    alert("Lengkapi tanggal lahir!");
    return;
}
```

---

❌ **BUG tambahan: Tidak validasi jumlah hari**

Contoh:
- User bisa pilih **31 Februari** (padahal tidak valid)

---

✅ **Solusi lanjutan (opsional):**
Gunakan validasi jumlah hari berdasarkan bulan:

```javascript
const isValidDate = new Date(`${tahun}-${bulan}-${tanggal}`).getDate() == tanggal;

if (!isValidDate) {
    alert("Tanggal tidak valid!");
    return;
}
```
#
        const ttl = `${tanggal}-${bulan}-${tahun}`;
        
### Menggabungkan Tanggal Lahir (TTL)

- Template string digunakan untuk menggabungkan:
  - tanggal
  - bulan
  - tahun
    
#### Hasil:
Format menjadi:
```
DD-MM-YYYY
```
Contoh:
```
10-05-2003
```

#
        const password = document.getElementById("password").value;
        
### Mengambil Password

#### Penjelasan:
- Mengambil nilai dari input password

❌ **BUG: Data sensitif**
Password tidak boleh ditampilkan secara langsung.

#
        const row = document.createElement("tr");
        
### Membuat Baris Tabel

- Membuat elemen `<tr>` baru
- Digunakan untuk menampung data mahasiswa

#
        row.innerHTML = `
            <td>${nim}</td>
            <td>${nama}</td>
            <td>${alamat}</td>
            <td>${jk}</td>
            <td>${ttl}</td>
            <td>${password}</td>
            <td>
### Mengisi Data ke Tabel

- Menggunakan template literal untuk memasukkan data ke tabel

❌ **BUG 1: Password ditampilkan**
```html
<td>${password}</td>
```

⚠ Ini berbahaya (data sensitif)

✅ **Solusi:**
```javascript
<td>******</td>
```

#
                <a href="#" onclick="editRow(this)">
                    <img src="edit.png" width="20">
                </a>
                <a href="#" onclick="deleteRow(this)">
                    <img src="trash.png" width="20">
                </a>
            </td>
        `;
### Tombol Aksi (Edit & Delete)

#### Penjelasan:
- `editRow(this)` → mengedit data
- `deleteRow(this)` → menghapus data

❌ **BUG 2: href="#"**
- Halaman bisa loncat ke atas

✅ **Solusi:**
```html
<a href="javascript:void(0)">
```

❌ **BUG 3: Icon tidak muncul**
Jika file `edit.png` atau `trash.png` tidak ada

✅ **Solusi:**
```html
✏️ 🗑️
```
#
        tableBody.appendChild(row);
        form.reset();
    });
### Menambahkan Data ke Tabel

#### Penjelasan:
- Menambahkan baris baru ke dalam `<tbody>`

### Reset Form

#### Penjelasan:
- Mengosongkan input setelah submit


#
    function deleteRow(el) {
        el.parentElement.parentElement.remove();
    }

### Fungsi Hapus Data (deleteRow)

- `function deleteRow(el)`  
  Fungsi ini digunakan untuk **menghapus data (baris) pada tabel**.

- `el`  
  Merupakan elemen yang diklik (biasanya tombol/icon delete).

---

- `el.parentElement`  
  Mengambil elemen **parent** dari tombol, yaitu `<td>`.

- `el.parentElement.parentElement`  
  Mengambil **baris tabel (`<tr>`)** yang berisi data.

- `.remove()`  
  Digunakan untuk **menghapus elemen tersebut dari halaman**.
  
#### Cara Kerja:
1. User klik tombol delete
2. Fungsi dipanggil dengan parameter `this`
3. Sistem mencari baris `<tr>`
4. Baris langsung dihapus dari tabel

❌ **BUG: Tidak ada konfirmasi**

Masalah:
- Data langsung terhapus
- User bisa salah klik
- Tidak ada peringatan

✅ **Solusi (tambahkan konfirmasi):**
```javascript
function deleteRow(el) {
    if (confirm("Yakin ingin menghapus data ini?")) {
        el.parentElement.parentElement.remove();
    }
}
```

❌ **BUG Tambahan: Data tidak tersimpan**

Jika halaman di-refresh:
- Data akan hilang
- Tidak ada penyimpanan


✅ **Solusi (gunakan localStorage):**
```javascript
function deleteRow(el) {
    if (confirm("Yakin ingin menghapus data ini?")) {
        el.parentElement.parentElement.remove();
        localStorage.setItem("dataMahasiswa", tableBody.innerHTML);
    }
}
```

#
    function editRow(el) {
        const row = el.parentElement.parentElement;
        const cells = row.children;

        document.getElementById("nim").value = cells[0].innerText;
        document.getElementById("nama").value = cells[1].innerText;
        document.getElementById("alamat").value = cells[2].innerText;
        document.getElementById("password").value = cells[5].innerText;
        row.remove();
    }
### Fungsi Edit Data (editRow)

- `function editRow(el)`  
  Fungsi ini digunakan untuk **mengedit data mahasiswa** yang sudah ada di tabel.

- `el`  
  Merupakan elemen yang diklik (ikon edit).

---

- `const row = el.parentElement.parentElement;`  
  Mengambil baris tabel (`<tr>`) dari tombol yang diklik.

- `const cells = row.children;`  
  Mengambil semua kolom (`<td>`) dalam baris tersebut.

---

#### Mengisi Kembali Form:

- `cells[0].innerText` → NIM  
- `cells[1].innerText` → Nama  
- `cells[2].innerText` → Alamat  
- `cells[5].innerText` → Password  

Data dari tabel dimasukkan kembali ke form agar bisa diedit.

---

- `row.remove();`  
  Menghapus data lama dari tabel sebelum diperbarui.

---

#### Cara Kerja:
1. User klik tombol edit  
2. Data dari tabel diambil  
3. Form diisi ulang dengan data tersebut  
4. Data lama dihapus  
5. User bisa submit ulang data yang sudah diperbaiki  

---

❌ **BUG 1: Edit tidak lengkap**

Data yang tidak ikut terisi:
- Jenis Kelamin (JK)
- Tanggal Lahir (TTL)

➡ Akibatnya:
- User harus mengisi ulang manual
- Bisa menyebabkan data tidak konsisten

---

✅ **Solusi: Tambahkan pengisian ulang semua field**

Contoh perbaikan:
```javascript
// Set jenis kelamin
const jk = cells[3].innerText;
document.querySelectorAll('input[name="jk"]').forEach(radio => {
    radio.checked = (radio.value === jk);
});

// Set tanggal lahir
const [tgl, bln, thn] = cells[4].innerText.split("-");
document.getElementById("tanggal").value = tgl;
document.getElementById("bulan").value = bln;
document.getElementById("tahun").value = thn;
```

---

❌ **BUG 2: Password diambil dari tabel**

Masalah:
- Password sebelumnya ditampilkan di tabel (tidak aman)
- Saat edit, password diambil kembali dari tabel

---

✅ **Solusi:**
- Jangan tampilkan password asli di tabel
- Gunakan placeholder atau minta user input ulang password

Contoh:
```javascript
document.getElementById("password").value = "";
```

---

❌ **BUG 3: Data langsung dihapus**

Masalah:
- Jika user batal edit, data hilang

---

✅ **Solusi (opsional):**
Tambahkan konfirmasi sebelum edit:
```javascript
if (confirm("Edit data ini?")) {
    // proses edit
}
```

---

#### Kesimpulan:
Fungsi ini sudah bisa melakukan edit data, namun perlu perbaikan agar:
- Semua field ikut terisi  
- Data lebih aman  
- Tidak terjadi kehilangan data 
#
    </script>
    
    </body>
    </html>
### Penutup Dokumen HTML

- `</script>`  
  Menandakan **akhir dari kode JavaScript** yang ditulis di dalam file HTML.

  Setelah tag ini, tidak ada lagi kode JavaScript yang dijalankan.

---

- `</body>`  
  Menandakan **akhir dari isi halaman web**.

  Semua elemen yang ditampilkan ke pengguna seperti:
  - Form
  - Tabel
  - Teks
  harus berada di dalam tag `<body>` ini.

---

- `</html>`  
  Menandakan **akhir dari seluruh dokumen HTML**.

  Ini adalah penutup dari struktur utama HTML.

---

#### Struktur Dasar HTML:
```html
<html>
    <head>
        <!-- Informasi halaman -->
    </head>
    <body>
        <!-- Isi halaman -->
    </body>
</html>
```

---

#### Kesimpulan:
Bagian ini berfungsi sebagai **penutup dari seluruh program**, memastikan struktur HTML lengkap dan dapat dibaca dengan baik oleh browser.

Jika salah atau tidak lengkap, maka:
- Halaman bisa error
- Tampilan tidak sempurna
