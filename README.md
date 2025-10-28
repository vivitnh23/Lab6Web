# Lab6Web
# Nama  : Vivit Nurul Hidayah
# NIM  : 312410110 
# kelas : TI.24.A.1 
# Mata Kuliah : Pemrograman Mobile 

# CSS Framework 
## Penjelasan Program 
Project ini merupakan hasil Praktikum 6 CSS Framework dengan tujuan membuat layout web responsif menggunakan Bootstrap 5.
Desain dibuat modern dan estetik dengan tema warna Lavender, Dusty, Overcast, dan Paper.

## Fitur& Desain
- Navbar responsif dengan ikon.
- Hero section dengan tombol dan gambar.
- 3 Card informatif dengan efek hover.
- Artikel (featurette) bergambar.
- Sidebar dengan widget link & text.
- Footer sederhana.
- Warna lembut & bayangan halus untuk tampilan modern.

# Input Program 
```
<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Layout Sederhana - Lab6 CSS Framework</title>

  <!-- Bootstrap 5 CSS CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <!-- Font Awesome for icons -->
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
  <style>
    /* Dusty, Lavender, Overcast, and Paper color aesthetic styles */
    body {
      font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
      background: linear-gradient(135deg, #faf0e6 0%, #f5f5dc 100%); /* Paper tones */
      color: #4b4b4b;
    }
    .navbar {
      background-color: #e6e6fa; /* Lavender */
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      border-bottom: 1px solid #d8bfd8;
    }
    .navbar-brand {
      color: #778899 !important; /* Overcast */
      font-weight: bold;
    }
    .nav-link {
      color: #b0a695 !important; /* Dusty */
      transition: color 0.2s;
    }
    .nav-link:hover {
      color: #778899 !important; /* Overcast */
    }
    #hero {
      background: linear-gradient(135deg, #778899 0%, #b0a695 100%); /* Overcast to Dusty */
      color: #faf0e6; /* Paper */
      padding: 4rem 0;
      border-radius: 0.5rem;
      margin-bottom: 2rem;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    #hero .btn-primary {
      background-color: #e6e6fa; /* Lavender */
      border-color: #e6e6fa;
      color: #778899; /* Overcast */
      font-weight: bold;
      transition: all 0.3s;
    }
    #hero .btn-primary:hover {
      background-color: #d8bfd8;
      border-color: #d8bfd8;
    }
    .card {
      border: 1px solid #f5f5dc; /* Paper */
      border-radius: 0.75rem;
      box-shadow: 0 2px 4px rgba(0,0,0,0.05);
      transition: box-shadow 0.3s, transform 0.3s;
      overflow: hidden;
      background-color: #ffffff;
    }
    .card:hover {
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      transform: translateY(-2px);
      border-color: #e6e6fa; /* Lavender */
    }
    .image-circle {
      width: 120px;
      height: 120px;
      object-fit: cover;
      border: 3px solid #b0a695; /* Dusty */
    }
    .card-body {
      min-height: 170px;
      padding: 1.5rem;
    }
    .btn-outline-secondary {
      border-color: #778899; /* Overcast */
      color: #778899;
      transition: all 0.3s;
    }
    .btn-outline-secondary:hover {
      background-color: #778899;
      border-color: #778899;
      color: #faf0e6; /* Paper */
    }
    .divider {
      border-top: 1px solid #f5f5dc; /* Paper */
      margin: 2rem 0;
      position: relative;
    }
    .divider::after {
      content: '';
      position: absolute;
      top: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 60px;
      height: 1px;
      background-color: #b0a695; /* Dusty */
    }
    .entry {
      background-color: #ffffff;
      border: 1px solid #f5f5dc; /* Paper */
      border-radius: 0.75rem;
      padding: 1.5rem;
      margin-bottom: 2rem;
      box-shadow: 0 2px 4px rgba(0,0,0,0.05);
      transition: box-shadow 0.3s;
    }
    .entry:hover {
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      border-color: #e6e6fa; /* Lavender */
    }
    .entry img {
      max-width: 150px;
      border-radius: 0.5rem;
      margin-right: 1rem;
      transition: filter 0.3s;
    }
    .entry img:hover {
      filter: sepia(20%);
    }
    .entry .right-img {
      float: right;
      margin-left: 1rem;
      margin-right: 0;
      transition: filter 0.3s;
    }
    .entry .right-img:hover {
      filter: sepia(20%);
    }
    #sidebar .card {
      border: 1px solid #f5f5dc; /* Paper */
      border-radius: 0.75rem;
      box-shadow: 0 2px 4px rgba(0,0,0,0.05);
      background-color: #ffffff;
    }
    #sidebar .card-header {
      background-color: #faf0e6; /* Paper */
      border-bottom: 1px solid #f5f5dc;
      font-weight: bold;
      color: #b0a695; /* Dusty */
    }
    footer {
      background-color: #e6e6fa; /* Lavender */
      color: #778899; /* Overcast */
      padding: 1rem 0;
      margin-top: 2rem;
    }
    @media (max-width: 767px) {
      .entry img, .entry .right-img {
        float: none;
        display: block;
        margin: 0 auto 1rem;
      }
    }
  </style>
</head>
<body>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container">
      <a class="navbar-brand" href="#"><i class="fas fa-palette me-2"></i>Layout Sederhana</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#mainNav"
              aria-controls="mainNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="mainNav">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li class="nav-item"><a class="nav-link active" aria-current="page" href="home.html"><i class="fas fa-home me-1"></i>Home</a></li>
          <li class="nav-item"><a class="nav-link" href="artikel.html"><i class="fas fa-newspaper me-1"></i>Artikel</a></li>
          <li class="nav-item"><a class="nav-link" href="about.html"><i class="fas fa-info-circle me-1"></i>About</a></li>
          <li class="nav-item"><a class="nav-link" href="kontak.html"><i class="fas fa-envelope me-1"></i>Kontak</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Page content -->
  <main class="container my-4">
    <!-- Hero / Jumbotron -->
    <section id="hero" class="p-4">
      <div class="row align-items-center">
        <div class="col-lg-8">
          <h1 class="display-5"><i class="fas fa-globe me-2"></i>Hello World!</h1>
          <p class="lead">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.</p>
          <a class="btn btn-primary btn-lg" href="home.html"><i class="fas fa-arrow-right me-2"></i>Learn more »</a>
        </div>
        <div class="col-lg-4 text-center">
          <img src="https://dummyimage.com/220x140/778899/fff.png" alt="hero" class="img-fluid rounded">
        </div>
      </div>
    </section>

    <!-- Main & Sidebar -->
    <div class="row">
      <!-- Main content (8 col) -->
      <section id="main" class="col-md-8">
        <!-- Three boxes (cards) -->
        <div class="row g-3 mb-4">
          <div class="col-sm-6 col-lg-4">
            <div class="card h-100 text-center">
              <img src="https://dummyimage.com/120/b0a695/fff.png" class="rounded-circle mx-auto mt-3 image-circle" alt="">
              <div class="card-body">
                <h5 class="card-title">Heading</h5>
                <p class="card-text">Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                <a href="#" class="btn btn-outline-secondary btn-sm"><i class="fas fa-eye me-1"></i>View detail</a>
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-lg-4">
            <div class="card h-100 text-center">
              <img src="https://dummyimage.com/120/e6e6fa/fff.png" class="rounded-circle mx-auto mt-3 image-circle" alt="">
              <div class="card-body">
                <h5 class="card-title">Heading</h5>
                <p class="card-text">Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                <a href="#" class="btn btn-outline-secondary btn-sm"><i class="fas fa-eye me-1"></i>View detail</a>
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-lg-4">
            <div class="card h-100 text-center">
              <img src="https://dummyimage.com/120/778899/fff.png" class="rounded-circle mx-auto mt-3 image-circle" alt="">
              <div class="card-body">
                <h5 class="card-title">Heading</h5>
                <p class="card-text">Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                <a href="#" class="btn btn-outline-secondary btn-sm"><i class="fas fa-eye me-1"></i>View detail</a>
              </div>
            </div>
          </div>
        </div>

        <hr class="divider">

        <!-- Featurette 1 -->
        <article class="entry d-flex align-items-start mb-4">
          <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="me-3">
          <div>
            <h2 class="h5">First featurette heading.</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis.</p>
          </div>
        </article>

        <hr class="divider">

        <!-- Featurette 2 (image right) -->
        <article class="entry mb-4">
          <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
          <h2 class="h5">Second featurette heading.</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
          <div class="clearfix"></div>
        </article>
      </section>

      <!-- Sidebar (4 col) -->
      <aside id="sidebar" class="col-md-4">
        <div class="card mb-3">
          <div class="card-header">
            <h5 class="mb-0"><i class="fas fa-list me-2"></i>Widget Header</h5>
          </div>
          <div class="card-body">
            <ul class="list-unstyled mb-0">
              <li><a href="#"><i class="fas fa-link me-2"></i>Widget Link</a></li>
              <li><a href="#"><i class="fas fa-link me-2"></i>Widget Link</a></li>
              <li><a href="#"><i class="fas fa-link me-2"></i>Widget Link</a></li>
              <li><a href="#"><i class="fas fa-link me-2"></i>Widget Link</a></li>
              <li><a href="#"><i class="fas fa-link me-2"></i>Widget Link</a></li>
            </ul>
          </div>
        </div>

        <div class="card">
          <div class="card-header">
            <h5 class="mb-0"><i class="fas fa-file-alt me-2"></i>Widget Text</h5>
          </div>
          <div class="card-body">
            <p class="mb-0">Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis.</p>
          </div>
        </div>
      </aside>
    </div>
  </main>

  <!-- Footer -->
  <footer class="text-center">
    <div class="container">
      <p class="mb-0"><i class="fas fa-copyright me-1"></i>&copy; 2021 - Universitas Pelita Bangsa</p>
    </div>
  </footer>

  <!-- Bootstrap 5 JS (with Popper) -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

# Output Program 
<img width="1352" height="634" alt="image" src="https://github.com/user-attachments/assets/6ee1d34e-a7e7-4b15-8964-7e8169d95e28" />
