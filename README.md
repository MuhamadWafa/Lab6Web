# 🌐 Praktikum 6: Bootstrap
# Muhamad Wafa Mufida Zulfi
# 312410334
# TI.24.A4
# Agung Nugroho, S.Kom., M.Kom
# Pemograman Web 1

## Intruksi Praktikum
<img width="586" height="129" alt="image" src="https://github.com/user-attachments/assets/00a4e263-6e60-4684-91da-16d9575fbfdd" />

### 1. File: index.html
Setup Bootstrap (Menggunakan CDN)
Kita akan menggunakan Bootstrap melalui CDN (Content Delivery Network). Ini mirip dengan cara kita menyertakan file JavaScript eksternal. Kita perlu menyertakan file CSS di bagian <head> dan file JavaScript di akhir <body>.

html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Praktikum 6 Bootstrap</title>

  <!-- Link CSS Bootstrap -->
  <link 
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" 
    rel="stylesheet"
    integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" 
    crossorigin="anonymous"
  />

  <!-- Style tambahan -->
  <style>
    body {
      font-size: 0.9rem;
      background-color: #f8f9fa;
      margin: 0;
      height: 100vh;
      overflow-x: hidden;
    }

    .main-wrapper {
      display: flex;
      flex-direction: row;
      height: calc(100vh - 56px); /* mengurangi tinggi navbar */
    }

    .left-side, .right-side {
      overflow-y: auto;
      padding: 30px;
      background-color: #ffffff;
    }

    .left-side {
      flex: 2;
      border-right: 2px solid #dee2e6;
    }

    .right-side {
      flex: 1;
      background-color: #fdfdfd;
    }

    .btn {
      padding: 6px 14px;
      font-size: 0.9rem;
    }

    .card {
      margin-top: 20px;
    }

    h1, h2 {
      font-size: 1.25rem;
    }

    p {
      font-size: 0.95rem;
    }
  </style>
</head>

<body>

  <!-- Navbar Bootstrap -->
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Praktikum 6</a>
      <button 
        class="navbar-toggler" 
        type="button" 
        data-bs-toggle="collapse" 
        data-bs-target="#navbarNav"
        aria-controls="navbarNav" 
        aria-expanded="false" 
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Konten Utama (Full Layar) -->
  <div class="main-wrapper">

    <!-- Kolom Kiri -->
    <div class="left-side">
      <div class="text-center mb-3">
        <h1>Halo, Boskuuu!</h1>
        <button class="btn btn-primary">Perkenalkan</button>
      </div>
```
### hasil di browsernya
<img width="1902" height="362" alt="Cuplikan layar 2025-10-30 135107" src="https://github.com/user-attachments/assets/726753d6-a415-447b-a208-0b216a438072" />

## Materi Praktikum
### 1. Container
Bootstrap mengharuskan konten dibungkus di dalam container untuk mengatur lebar dan perataan.

.container: Memberikan lebar maksimum yang tetap (fixed-width) yang berubah pada ukuran layar tertentu.

.container-fluid: Memberikan lebar penuh (full-width) 100%.

```

      <div class="mb-3">
        <h2>Nama</h2>
        <p>Muhamad Wafa Mufida Zulfi</p>
      </div>

      <div class="mb-3">
        <h2>Tempat, Tanggal Lahir</h2>
        <p>Bekasi, 29 Desember 2006</p>
      </div>

      <div class="mb-3">
        <h2>Agama</h2>
        <p>Islam</p>
      </div>

      <div class="mb-3">
        <h2>Pendidikan</h2>
        <p>Universitas Pelita Bangsa</p>
      </div>
```

## Hasil Browssernya
<img width="1919" height="1097" alt="Cuplikan layar 2025-10-30 140138" src="https://github.com/user-attachments/assets/66209073-c79f-4535-8ec2-e7fb767676d8" />

### 2. Grid System (Sistem Grid)
Ini adalah fitur inti Bootstrap yang menggantikan float manual. Sistem grid Bootstrap menggunakan 12 kolom.

.row: Pembungkus untuk kolom. Ini menggantikan kebutuhan akan clearfix.
.col: Menandakan sebuah kolom. Jika hanya .col, lebarnya akan dibagi rata.
.col-{angka}: Menentukan lebar kolom dari 1 sampai 12. Contoh: .col-4 berarti lebar 4/12 (sepertiga).
.col-{breakpoint}-{angka}: Menentukan lebar kolom pada ukuran layar tertentu (misal: md untuk medium).
Contoh Grid: Membuat 3 kolom sama lebar yang di layout Praktikum 4 harus menggunakan float: left. Di Bootstrap, caranya:
```

 <div class="mt-4">
        <div class="row text-center">
          <div class="col bg-white p-3 m-2 rounded shadow-sm">Halo semuanya!!</div>
          <div class="col bg-white p-3 m-2 rounded shadow-sm">Saya biasa dipanggil Upit</div>
          <div class="col bg-white p-3 m-2 rounded shadow-sm">Hobi saya main musik</div>
        </div>
        <div class="row text-center mt-3">
          <div class="col bg-white p-3 m-2 rounded shadow-sm">Senang bertemu dengan kalian</div>
          <div class="col bg-white p-3 m-2 rounded shadow-sm">Sampai jumpa di lain hari</div>
        </div>
      </div>
```
## Hasil browsernya
<img width="1309" height="798" alt="Cuplikan layar 2025-10-30 213752" src="https://github.com/user-attachments/assets/0d3f8ea6-ffe4-4974-8929-d293603c3331" />

### 3. Komponen: Button (Tombol)
Bootstrap menyediakan berbagai style tombol.


      <div class="text-center mt-4">
        <button class="btn btn-primary m-2">Primary</button>
        <button class="btn btn-secondary m-2">Secondary</button>
        <button class="btn btn-success m-2">Success</button>
        <button class="btn btn-danger m-2">Danger</button>
      </div>

## Hasil browsernya
<img width="932" height="64" alt="Cuplikan layar 2025-10-30 214043" src="https://github.com/user-attachments/assets/eec631a6-d34b-466f-b775-473abd280683" />

4. Komponen: Navbar (Navigasi)
Membuat navigasi responsive yang bisa collapse (menjadi menu hamburger di mobile) sangat mudah.
```
  <!-- Navbar Bootstrap -->
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Praktikum 6</a>
      <button 
        class="navbar-toggler" 
        type="button" 
        data-bs-toggle="collapse" 
        data-bs-target="#navbarNav"
        aria-controls="navbarNav" 
        aria-expanded="false" 
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
        </ul>
      </div>
    </div>
  </nav>
```
## hasil browsernya
<img width="1910" height="170" alt="Cuplikan layar 2025-10-30 214301" src="https://github.com/user-attachments/assets/eaf8174c-d741-4317-9808-672c568c9d59" />




