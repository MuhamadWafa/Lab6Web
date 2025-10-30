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
