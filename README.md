<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portofolio Saya</title>
  <!-- Font Awesome untuk Ikon Sosmed -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <!-- Google Font (Poppins) -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  
  <style>
    :root {
      --bg-color: #0f172a;
      --card-bg: #1e293b;
      --accent-color: #6366f1;
      --accent-hover: #4f46e5;
      --text-main: #f8fafc;
      --text-muted: #94a3b8;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-main);
      line-height: 1.6;
    }

    /* Header & Navigasi */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(15, 23, 42, 0.85);
      backdrop-filter: blur(10px);
      z-index: 1000;
      border-bottom: 1px solid rgba(255, 255, 255, 0.05);
    }

    nav {
      max-width: 1100px;
      margin: 0 auto;
      padding: 1.2rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 1.5rem;
      font-weight: 700;
      color: var(--accent-color);
      text-decoration: none;
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
    }

    .nav-links a {
      color: var(--text-main);
      text-decoration: none;
      font-weight: 500;
      transition: color 0.3s;
    }

    .nav-links a:hover {
      color: var(--accent-color);
    }

    /* Container utama */
    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 2rem;
    }

    section {
      padding: 6rem 0;
    }

    /* Hero / Profil */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding-top: 5rem;
    }

    .hero-content {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 3rem;
      width: 100%;
    }

    .hero-text {
      flex: 1;
    }

    .hero-text h1 {
      font-size: 3rem;
      font-weight: 700;
      margin-bottom: 0.5rem;
    }

    .hero-text h1 span {
      color: var(--accent-color);
    }

    .hero-text h3 {
      font-size: 1.4rem;
      color: var(--text-muted);
      font-weight: 400;
      margin-bottom: 1.5rem;
    }

    .hero-text p {
      color: var(--text-muted);
      margin-bottom: 2rem;
      max-width: 500px;
    }

    .hero-image {
      flex: 1;
      display: flex;
      justify-content: center;
    }

    .img-wrapper {
      position: relative;
      width: 280px;
      height: 280px;
      border-radius: 50%;
      padding: 8px;
      background: linear-gradient(135deg, var(--accent-color), #ec4899);
    }

    .img-wrapper img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%;
      background-color: var(--card-bg);
    }

    /* Sosial Media Link */
    .social-links {
      display: flex;
      gap: 1rem;
    }

    .social-icon {
      width: 45px;
      height: 45px;
      border-radius: 50%;
      background-color: var(--card-bg);
      color: var(--text-main);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2rem;
      text-decoration: none;
      transition: all 0.3s ease;
      border: 1px solid rgba(255, 255, 255, 0.1);
    }

    .social-icon:hover {
      background-color: var(--accent-color);
      transform: translateY(-5px);
    }

    /* Judul Section */
    .section-title {
      font-size: 2.2rem;
      text-align: center;
      margin-bottom: 3rem;
      position: relative;
    }

    .section-title::after {
      content: '';
      display: block;
      width: 60px;
      height: 4px;
      background-color: var(--accent-color);
      margin: 0.5rem auto 0;
      border-radius: 2px;
    }

    /* Grid Projek */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }

    .project-card {
      background-color: var(--card-bg);
      border-radius: 12px;
      overflow: hidden;
      border: 1px solid rgba(255, 255, 255, 0.05);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .project-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
    }

    .project-img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }

    .project-info {
      padding: 1.5rem;
    }

    .project-title {
      font-size: 1.25rem;
      margin-bottom: 0.5rem;
    }

    .project-desc {
      color: var(--text-muted);
      font-size: 0.9rem;
      margin-bottom: 1.2rem;
    }

    .project-tags {
      display: flex;
      gap: 0.5rem;
      flex-wrap: wrap;
      margin-bottom: 1.5rem;
    }

    .tag {
      background-color: rgba(99, 102, 241, 0.15);
      color: var(--accent-color);
      padding: 0.3rem 0.8rem;
      border-radius: 20px;
      font-size: 0.75rem;
      font-weight: 600;
    }

    .project-link {
      display: inline-block;
      color: var(--accent-color);
      text-decoration: none;
      font-weight: 600;
      font-size: 0.9rem;
      transition: color 0.3s;
    }

    .project-link:hover {
      color: var(--text-main);
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 2rem;
      color: var(--text-muted);
      font-size: 0.85rem;
      border-top: 1px solid rgba(255, 255, 255, 0.05);
    }

    /* Responsif Mobile */
    @media (max-width: 768px) {
      .hero-content {
        flex-direction: column-reverse;
        text-align: center;
      }

      .hero-text p {
        margin: 0 auto 2rem;
      }

      .social-links {
        justify-content: center;
      }

      .img-wrapper {
        width: 200px;
        height: 200px;
      }

      .nav-links {
        gap: 1rem;
      }
    }
  </style>
</head>
<body>

  <!-- Navigasi -->
  <header>
    <nav>
      <a href="#" class="logo">Portofolio.</a>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#projects">Projek</a></li>
        <li><a href="#contact">Kontak</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section (Foto & Bio Ringkas) -->
  <section id="home" class="hero">
    <div class="container">
      <div class="hero-content">
        <div class="hero-text">
          <h1>Halo, Saya <span>Nama Anda</span></h1>
          <h3>Web Developer & UI/UX Designer</h3>
          <p>Saya berfokus pada pembuatan aplikasi web yang responsif, fungsional, dan memiliki antarmuka pengguna yang menarik.</p>
          
          <!-- Social Media Links -->
          <div class="social-links">
            <a href="https://github.com" target="_blank" class="social-icon" title="GitHub"><i class="fab fa-github"></i></a>
            <a href="https://linkedin.com" target="_blank" class="social-icon" title="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
            <a href="https://instagram.com" target="_blank" class="social-icon" title="Instagram"><i class="fab fa-instagram"></i></a>
            <a href="mailto:emailanda@gmail.com" class="social-icon" title="Email"><i class="fas fa-envelope"></i></a>
          </div>
        </div>
        
        <div class="hero-image">
          <div class="img-wrapper">
            <!-- Ganti src dengan link foto Anda -->
            <img src="https://via.placeholder.com/300" alt="Foto Profil">
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects Section (Hasil Karya) -->
  <section id="projects">
    <div class="container">
      <h2 class="section-title">Hasil Karya & Projek</h2>
      
      <div class="projects-grid">
        <!-- Projek 1 -->
        <div class="project-card">
          <img src="https://via.placeholder.com/600x400" alt="Projek 1" class="project-img">
          <div class="project-info">
            <h3 class="project-title">Aplikasi Kasir Toko</h3>
            <p class="project-desc">Sistem Point of Sale (POS) berbasis web untuk pencatatan transaksi barang dan cetak struk otomatis.</p>
            <div class="project-tags">
              <span class="tag">PHP</span>
              <span class="tag">MySQL</span>
              <span class="tag">Bootstrap</span>
            </div>
            <a href="#" class="project-link">Lihat Detail <i class="fas fa-arrow-right"></i></a>
          </div>
        </div>

        <!-- Projek 2 -->
        <div class="project-card">
          <img src="https://via.placeholder.com/600x400" alt="Projek 2" class="project-img">
          <div class="project-info">
            <h3 class="project-title">Desain UI/UX Web Sekolah</h3>
            <p class="project-desc">Perancangan ulang antarmuka website profil sekolah agar lebih informatif dan modern.</p>
            <div class="project-tags">
              <span class="tag">Figma</span>
              <span class="tag">UI/UX</span>
              <span class="tag">Prototyping</span>
            </div>
            <a href="#" class="project-link">Lihat Detail <i class="fas fa-arrow-right"></i></a>
          </div>
        </div>

        <!-- Projek 3 -->
        <div class="project-card">
          <img src="https://via.placeholder.com/600x400" alt="Projek 3" class="project-img">
          <div class="project-info">
            <h3 class="project-title">Landing Page Produk</h3>
            <p class="project-desc">Halaman promosi produk interaktif dengan fitur penyesuaian warna tampilan secara dinamis.</p>
            <div class="project-tags">
              <span class="tag">HTML</span>
              <span class="tag">CSS</span>
              <span class="tag">JavaScript</span>
            </div>
            <a href="#" class="project-link">Lihat Detail <i class="fas fa-arrow-right"></i></a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer Section -->
  <footer id="contact">
    <div class="container">
      <p>&copy; 2026 Portofolio Saya. Dibuat dengan HTML & CSS.</p>
    </div>
  </footer>

</body>
</html>
