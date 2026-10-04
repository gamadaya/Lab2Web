# Dokumentasi Praktikum Web: HTML Lanjutan

**Identitas Mahasiswa:**
- **Nama:** Gama Daya Laksana
- **NIM:** 312510051
- **Kelas:** I253A
- **Program Studi:** Teknik Informatika
- **Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom.
- **Kampus:** Universitas Pelita Bangsa

---

## Panduan Screenshot Tugas

Simpan semua file tangkapan layar (screenshot) di dalam folder `screenshots/` dengan format nama angka (`1.png` sampai `8.png`) sesuai tabel berikut:

| No File | Aplikasi / Lokasi | Yang Harus Di-Screenshot |
|---|---|---|
| **`1.png`** | Browser | 1. Tampilan tabel data mahasiswa. |
| **`2.png`** | Browser | 2. Tampilan Tabel dengan `<thead>`, `<tbody,>` dan `<tfoot.>` |
| **`3.png`** | Browser | 3. Tampilan Membuat Form Registrasi Mahasiswa. |
| **`4.png`** | Browser | 4. Tampilan elemen Radio Button dan Checkbox. |
| **`5.png`** | Browser | 5. Tampilan Select dan Textarea. |
| **`6.png`** | Browser | 6. Tampilan Validasi Form Dasar. |
| **`7.png`** | Browser | 7. Tampilan Halaman Semantic HTML. |
| **`8.png`** | Browser | 8. Tampilan Menambahkan Multimedia. |
| **`9.png`** | Browser | 9. Tampilan Proyek Mini — Form Biodata Mahasiswa |
---

## Struktur Folder

```text
Lab2Web/
├── index.html
├── index1.html
├── biodata.html
├── media/
│   ├── audio.mp3
│   └── video.mp4
├── screenshots/
│   ├── 1.png
│   ├── 2.png
│   ├── 3.png
│   ├── 4.png
│   ├── 5.png
│   ├── 6.png
│   ├── 7.png
│   └── 8.png
└── README.md
```

---

## Pendahuluan

**HTML Lanjutan** memperdalam kemampuan pengembangan web dengan menghadirkan interaktivitas pengumpulan data pengguna, penyajikan struktur data kompleks, serta integrasi media. Praktikum ini berfokus pada lima pilar utama:

1. **Tabel HTML:** Menyajikan data terstruktur dalam bentuk baris dan kolom beserta hierarki header, body, dan footer.
2. **Form & Input:** Elemen interaktif untuk menerima data pengguna mulai dari teks, kata sandi, tanggal, hingga pilihan.
3. **Validasi Form Dasar:** Memastikan integritas data yang dimasukkan sebelum dikirimkan menggunakan atribut bawaan HTML5.
4. **Semantic HTML:** Menggunakan tag bermakna khusus untuk membangun tata letak web yang akurat bagi browser, *screen reader*, dan SEO.
5. **Multimedia:** Mengintegrasikan pemutar audio dan video native tanpa perlu dependensi library eksternal.

---

## Implementasi Kode & Dokumentasi

### 1. Tabel Data Mahasiswa

Menjelaskan struktur dasar tabel HTML menggunakan tag `<table>`, `<tr>` (baris), `<th>` (header kolom), dan `<td>` (sel data). Elemen ini digunakan untuk menyajikan informasi berupa data mahasiswa secara rapi dalam format kolom dan baris.

**Input Code:**

```html
 <!-- Tabel Data Mahasiswa -->

    <h1>Data Mahasiswa</h1>
    <table border="1">
        <tr>
            <th>Nama</th>
            <th>NIM</th>
            <th>Program Studi</th>
            <th>Alamat</th>
        </tr>
        <tr>
            <td>Gama</td>
            <td>3123456</td>
            <td>Teknik Informatika</td>
            <td>Jakarta</td>
        </tr>
        <tr>
            <td>Salsa</td>
            <td>3123457</td>
            <td>Teknik Informatika</td>
            <td>Bandung</td>
        </tr>
        <tr>
            <td>Rizky</td>
            <td>3123458</td>
            <td>Teknik Informatika</td>
            <td>Surabaya</td>
        </tr>

    </table>
```

**Capture Output:**

> ![Output Tabel Data Mahasiswa](./screenshots/1.png)

---

### 2. Mengembangkan Tabel dengan Caption, Thead, Tbody, dan Tfoot

Menjelaskan pengelompokan elemen tabel secara lebih terstruktur:

`<caption>`: Memberikan judul atau deskripsi tabel.

`<thead>`: Membungkus bagian baris header tabel.

`<tbody>`: Membungkus konten utama dari data tabel.

`<tfoot>`: Membungkus baris ringkasan atau total di bagian bawah tabel.

**Input Code:**

```html
<!-- 2. Mengembangkan Tabel dengan Caption, Thead, Tbody, dan Tfoot -->

    <table border="1">
        <br>
        <caption>Nilai Praktikum</caption>
        <thead>
            <tr>
                <th>No</th>
                <th>Nama</th>
                <th>Nilai</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>Gama Daya Laksana</td>
                <td>85</td>
            </tr>
            <tr>
                <td>2</td>
                <td>Budi Santoso</td>
                <td>90</td>
            </tr>
            <tr>
                <td>3</td>
                <td>Siti Aminah</td>
                <td>88</td>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="2">Rata-rata</td>
                <td>87.5</td>
            </tr>
        </tfoot>
    </table>
```

**Capture Output:**

> ![Output Form Registrasi](./screenshots/2.png)

---

### 3. 3. Membuat Form Registrasi Mahasiswa

Menjelaskan penggunaan tag `<form>` sebagai wadah untuk mengumpulkan input dari pengguna. Poin ini mengenalkan elemen `<label>` sebagai petunjuk input, tag `<input>` dengan berbagai tipe (text, email, password, date), serta tombol `<button>` untuk mengirim (submit) atau mengosongkan (reset) isi formulir.
**Input Code:**

```html
 <!-- 3. Membuat Form Registrasi Mahasiswa -->
    <h1>Form Registrasi Mahasiswa</h1>
    <form>
        <label for="nama">Nama Lengkap</label><br>
        <input type="text" id="nama" name="nama"><br><br>
        <label for="email">Email</label><br>
        <input type="email" id="email" name="email"><br><br>
        <label for="password">Password</label><br>
        <input type="password" id="password" name="password"><br><br>
        <label for="tanggal">Tanggal Lahir</label><br>
        <input type="date" id="tanggal" name="tanggal"><br><br>
        <button type="submit">Daftar</button>
        <button type="reset">Reset</button>
    </form>
```

**Capture Output:**

> ![Output Radio dan Checkbox](./screenshots/3.png)

---

### 4. Radio Button dan Checkbox

Menjelaskan pembuatan pilihan opsi pada form:

Radio Button `(type="radio")`: Digunakan untuk memilih satu opsi dari beberapa pilihan yang saling eksklusif (misalnya jenis kelamin L/P).

Checkbox `(type="checkbox")`: Digunakan untuk memilih satu atau lebih opsi secara bebas (misalnya pilihan keahlian/skill).
**Input Code:**

```html
 <!-- 4. Radio Button dan Checkbox -->
    <h2>Jenis Kelamin</h2>
    <input type="radio" id="laki" name="jk" value="L">
    <label for="laki">Laki-laki</label>
    <input type="radio" id="perempuan" name="jk" value="P">
    <label for="perempuan">Perempuan</label>
    <h2>Keahlian</h2>
    <input type="checkbox" id="html" name="skill" value="HTML">
    <label for="html">HTML</label>
    <input type="checkbox" id="css" name="skill" value="CSS">
    <label for="css">CSS</label>
    <input type="checkbox" id="js" name="skill" value="JavaScript">
    <label for="js">JavaScript</label>
```

**Capture Output:**

> ![Output Select dan Textarea](./screenshots/4.png)

---

### 5. Select dan Text Area

Menjelaskan jenis input pilihan tingkat lanjut dan teks panjang:

`<select>` & `<option>`: Membuat menu drop-down untuk memilih opsi dalam daftar terbatas (misalnya program studi).

`<textarea>`: Menyediakan kolom input teks multibaris untuk menampung teks yang panjang (misalnya input alamat).
**Input Code:**

```html
 <!-- 5. Select Dan Text Area-->
    <br><br>
    <label for="prodi">Program Studi</label>
    <select id="prodi" name="prodi">
        <option value="">-- Pilih Prodi --</option>
        <option value="ti">Teknik Informatika</option>
        <option value="si">Sistem Informasi</option>
    </select>
    <br><br>
    <label for="alamat">Alamat</label><br>
    <textarea id="alamat" name="alamat" rows="5" cols="40"></textarea>
```

**Capture Output:**

> ![Output Validasi Form](./screenshots/5.png)

---

### 6. Validasi Form Dasar

Menjelaskan penggunaan atribut bawaan HTML5 untuk memvalidasi isian pengguna sebelum dikirim ke server tanpa menggunakan JavaScript. Contohnya atribut required (wajib diisi), minlength (panjang karakter minimum), serta min dan max untuk batasan nilai angka.

**Input Code:**

```html
 <!-- 6. Validasi Form Dasar-->
    <form>
        <br>
        <label for="nama">Nama</label>
        <input type="text" id="nama" name="nama" required minlength="3">
        <br>
        <label for="email">Email</label>
        <input type="email" id="email" name="email" required>
        <br>
        <label for="umur">Umur</label>
        <input type="number" id="umur" name="umur" min="17" max="60" required>
        <br>
        <button type="submit">Kirim</button>
    </form>
```

**Capture Output:**

> ![Output Semantic HTML](./screenshots/6.png)

---

### 7. Membuat Halaman Semantic HTML

Berikut adalah penjelasan fungsi dari setiap tag Semantic HTML yang digunakan

`<header>` : Menandai bagian kepala atau koping (header) dari halaman web. Biasanya berisi judul utama web, logo, atau deskripsi singkat halaman.

`<nav>` (Navigation) : Membungkus kumpulan link navigasi utama (seperti Beranda, Profil, Kontak) untuk membantu pengguna dan mesin pencari mengenali struktur menu situs.

`<main>` : Menandai area konten utama yang unik dan paling penting dari dokumen HTML. Dalam satu halaman hanya boleh ada satu elemen `<main>`.

`<section>` : Mengelompokkan konten yang memiliki tema atau topik pembahasan yang sama (dalam contoh ini: grup "Informasi Akademik").

`<article>` : Membungkus konten mandiri yang memiliki arti utuh, seperti artikel berita, postingan blog, atau pengumuman (dalam contoh ini: pengumuman "Praktikum HTML Lanjutan").

`<aside>` : Menampung konten sampingan atau informasi tambahan yang sifatnya melengkapi konten utama (seperti sidebar, iklan, atau tautan terkait).

`<footer>` : Menandai bagian kaki halaman web. Biasanya berisi informasi hak cipta (&copy;), kontak pengembang, atau tautan kebijakan privasi.
**Input Code:**

```html
<!--7. Membuat Halaman Semantic HTML -->

<!DOCTYPE html>
<html>

<head>
    <title>Portal Mahasiswa</title>
</head>

<body>
    <header>
        <h1>Portal Mahasiswa</h1>
    </header>
    <nav> <a href="#">Beranda</a> <a href="#">Profil</a> <a href="#">Kontak</a> </nav>
    <main>
        <section>
            <h2>Informasi Akademik</h2>
            <article>
                <h3>Praktikum HTML Lanjutan</h3>
                <p>Mahasiswa mempelajari tabel, form, semantic HTML, multimedia, dan validasi.</p>
            </article>
        </section>
        <aside>Informasi tambahan mahasiswa.</aside>
    </main>
    <footer>
        <p>&copy; 2026 Teknik Informatika</p>
    </footer>
</body>

</html>
```

**Capture Output:**

> ![Output Multimedia Audio & Video](./screenshots/7.png)

---

### 8. Menambahkan Multimedia

Menjelaskan cara menampilkan media suara dan video pada halaman web menggunakan tag `<audio>` dan `<video>`. Atribut controls digunakan untuk memunculkan tombol pemutar (play, pause, volume), sedangkan tag <source> menentukan lokasi serta format file media tersebut.
**Input Code:**

```html
 <!-- 8. Menambahkan Multimedia-->
    <h2>Audio</h2>
    <audio controls>
        <source src="media/audio.mp3" type="audio/mpeg">
        Browser tidak mendukung audio.
    </audio>
    <h2>Video</h2>
    <video controls width="480">
        <source src="media/video.mp4" type="video/mp4">
        Browser tidak mendukung video.
    </video>
```

**Capture Output:**

> ![Output Proyek Mini Biodata](./screenshots/8.png)

---

## 9. Projek Mini Biodata Mahasiswa
```html
<!DOCTYPE html>
<html>


<!--Projek Mini Form Biodata Mahasiswa -->
<head>
    <title>Biodata Mahasiswa</title>
</head>

<body>
    <header>
        <h1>Biodata Mahasiswa</h1>
    </header>
    <nav> <a href="index.html">Beranda</a> <a href="#biodata">Biodata</a> <a href="#form">Form</a> </nav>
    <main>
        <section id="biodata">
            <h2>Data Mahasiswa</h2>
            <table border="1">
                <tr>
                    <th>Data</th>
                    <th>Keterangan</th>
                </tr>
                <tr>
                    <td>NIM</td>
                    <td>312510051</td>
                </tr>
                <tr>
                    <td>Nama</td>
                    <td>Gama Daya Laksana</td>
                </tr>
                <tr>
                    <td>Program Studi</td>
                    <td>Teknik Informatika</td>
                </tr>
            </table>
        </section>
        <section id="form">
            <h2>Form Biodata</h2>
            <form> <label for="nama">Nama</label>
                <input type="text" id="nama" name="nama" required> <br><br> <label for="email">Email</label> <input
                    type="email" id="email" name="email" required> <br><br> <label for="prodi">Program Studi</label>
                <select id="prodi" name="prodi" required>
                    <option value="">-- Pilih --</option>
                    <option value="ti">Teknik Informatika</option>
                    <option value="si">Sistem Informasi</option>
                </select> <br><br> <label for="alamat">Alamat</label><br> <textarea id="alamat" name="alamat"
                    required></textarea> <br><br> <button type="submit">Simpan</button> <button
                    type="reset">Reset</button>
            </form>
        </section>
    </main>
    <footer>
        <p>&copy; 2026 Teknik Informatika</p>
    </footer>
</body>

</html>

```

## Jawaban Pertanyaan

1. Fungsi `<table>`, `<tr>`, `<th>`, dan `<td>`

`<table>`: Membungkus dan membentuk seluruh elemen tabel.

`<tr>` (Table Row): Membuat satu baris baru di dalam tabel.

`<th>` (Table Header): Menandai sel sebagai header/judul kolom.

`<td>` (Table Data): Menandai sel biasa yang berisi data atau isi tabel.

2. Perbedaan `<th>` dan `<td>`

`<th>`: Teks otomatis dicetak tebal (bold) dan berada di tengah sel (center). Digunakan untuk nama kolom/kategori.

`<td>`: Teks berukuran normal dan berada di posisi rata kiri secara default. Digunakan untuk isi data.

3. Fungsi colspan pada Tabel

Digunakan untuk menggabungkan beberapa kolom secara horizontal menjadi satu sel besar (seperti fitur Merge Cells di spreadsheet).

4. Fungsi <form> dalam HTML

Berfungsi sebagai wadah untuk menampung elemen-elemen input (teks, pilihan, tombol) yang digunakan untuk mengumpulkan data dari pengguna lalu mengirimkannya ke server.

5. Perbedaan Radio Button dan Checkbox

Radio Button `(type="radio")`: Pengguna hanya bisa memilih satu dari beberapa opsi yang tersedia (misal: jenis kelamin).

Checkbox `(type="checkbox")`: Pengguna bisa memilih satu, lebih dari satu, atau tidak memilih sama sekali dari daftar pilihan (misal: hobi atau keahlian).

6. Alasan `<label>` Dihubungkan ke id Input via Atribut for

Aksesibilitas & Pengalaman Pengguna: Membuat label dapat diklik. Ketika pengguna mengeklik teks label, kursor akan otomatis fokus ke dalam kolom input terkait (sangat berguna untuk pengguna HP atau screen reader).

7. Perbedaan `<textarea>` dan Input type="text"

Input type="text": Hanya menerima satu baris teks pendek (misal: nama lengkap).

`<textarea>`: Menerima banyak baris teks panjang yang bisa di-scroll dan diubah ukurannya (misal: alamat lengkap atau pesan).

8. Fungsi Elemen Semantic HTML

`<header>`: Area kepala halaman web (berisi judul, logo, atau deskripsi).

`<nav>`: Membungkus menu navigasi utama.

`<main>`: Menampung konten utama yang unik dalam satu halaman.

`<section>`: Mengelompokkan konten berdasarkan satu tema/topik tertentu.

`<article>`: Membungkus konten mandiri yang utuh (seperti pengumuman, berita, atau postingan blog).

`<aside>`: Membungkus konten sampingan/pelengkap yang tidak terkait langsung dengan konten utama (seperti sidebar).

`<footer>`: Area kaki halaman web (berisi hak cipta, kontak, atau tautan tambahan).

9. Fungsi required, min, max, dan minlength

required: Memaksa kolom input wajib diisi sebelum form dikirim.

min: Menentukan batas nilai angka atau tanggal minimum yang boleh diinput.

max: Menentukan batas nilai angka atau tanggal maksimum yang boleh diinput.

minlength: Menentukan jumlah karakter teks minimum yang harus diketik pengguna.

10. Perbedaan Elemen `<audio>` dan `<video>`

`<audio>`: Hanya memutar berkas suara (sound/music) tanpa area visual.

`<video>`: Memutar berkas video lengkap dengan visual gambar bergerak dan suara, serta mendukung atribut tambahan seperti width, height, dan poster.

---

## Checklist Sebelum Dikumpulkan

Checklist Sebelum Dikumpulkan
- [x] Tabel berhasil ditampilkan dan memiliki header yang sesuai.
- [x] Form memiliki label dan beberapa jenis input.
- [x] Radio button dan checkbox sudah digunakan.
- [x] Select dan textarea sudah digunakan.
- [x] Validasi required dan validasi dasar lainnya sudah dicoba.
- [x] Semantic HTML sudah digunakan.
- [x] Audio dan/atau video berhasil ditampilkan.
- [x] Proyek mini biodata menggabungkan materi utama.
- [x] Screenshot dan README.md sudah tersedia.
- [x] Repository sudah di-commit dan URL siap dikirim.
- [x] Screenshot dan README.md sudah tersedia.
- [x] Repository sudah di-commit dan URL siap dikirim.
