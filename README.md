<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portofolio Saya</title>
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <!-- Google Fonts: Plus Jakarta Sans -->
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-main: #f8fafc;
      --bg-card: #ffffff;
      --primary: #9966cb;       /* Amethyst Purple */
      --primary-dark: #7b43b6;  /* Deep Purple */
      --primary-light: #f3ebfc; /* Soft Lilac */
      --text-main: #2d1548;
      --text-muted: #6b7280;
      --border-color: #ede9fe;
      --shadow: 0 10px 30px -10px rgba(153, 102, 203, 0.15);
      --shadow-hover: 0 20px 40px -15px rgba(153, 102, 203, 0.3);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Plus Jakarta Sans', sans-serif;
      scroll-behavior: smooth;
    }

    body {
      background-color: var(--bg-main);
      color: var(--text-main);
      line-height: 1.6;
    }

    /* Navigasi */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(12px);
      z-index: 1000;
      border-bottom: 1px solid var(--border-color);
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
      font-size: 1.4rem;
      font-weight: 800;
      color: var(--primary);
      text-decoration: none;
      letter-spacing: -0.5px;
    }

    .logo span {
      color: var(--text-main);
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
    }

    .nav-links a {
      color: var(--text-main);
      text-decoration: none;
      font-weight: 600;
      font-size: 0.95rem;
      transition: color 0.3s;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    /* Container */
    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 2rem;
    }

    section {
      padding: 6rem 0;
    }

    /* Hero Section */
    .hero {
      min-height: 90vh;
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
      flex: 1.2;
    }

    .badge {
      display: inline-block;
      background-color: var(--primary-light);
      color: var(--primary-dark);
      padding: 0.4rem 1rem;
      border-radius: 50px;
      font-size: 0.85rem;
      font-weight: 700;
      margin-bottom: 1rem;
      border: 1px solid rgba(153, 102, 203, 0.2);
    }

    .hero-text h1 {
      font-size: 3rem;
      font-weight: 800;
      line-height: 1.2;
      margin-bottom: 1rem;
      color: var(--text-main);
    }

    .hero-text h1 span {
      background: linear-gradient(135deg, var(--primary), var(--primary-dark));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero-text p {
      color: var(--text-muted);
      font-size: 1.05rem;
      margin-bottom: 2rem;
      max-width: 520px;
    }

    /* Foto Profil */
    .hero-image {
      flex: 0.8;
      display: flex;
      justify-content: center;
    }

    .img-wrapper {
      position: relative;
      width: 270px;
      height: 270px;
      border-radius: 30px;
      background: linear-gradient(135deg, #ffffff, var(--primary-light));
      padding: 8px;
      box-shadow: var(--shadow-hover);
      border: 2px solid var(--border-color);
      transform: rotate(-2deg);
      transition: transform 0.4s ease;
    }

    .img-wrapper:hover {
      transform: rotate(0deg) scale(1.02);
    }

    .img-wrapper img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 22px;
    }

    /* Social Links */
    .social-links {
      display: flex;
      gap: 1rem;
    }

    .social-icon {
      width: 44px;
      height: 44px;
      border-radius: 14px;
      background-color: var(--bg-card);
      color: var(--primary);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2rem;
      text-decoration: none;
      transition: all 0.3s ease;
      border: 1px solid var(--border-color);
      box-shadow: 0 4px 10px rgba(0,0,0,0.03);
    }

    .social-icon:hover {
      background-color: var(--primary);
      color: #ffffff;
      transform: translateY(-4px);
      box-shadow: 0 8px 18px rgba(153, 102, 203, 0.35);
    }

    /* Section Title */
    .section-title {
      font-size: 2rem;
      font-weight: 800;
      text-align: center;
      margin-bottom: 0.5rem;
    }

    .section-subtitle {
      text-align: center;
      color: var(--text-muted);
      margin-bottom: 3.5rem;
      font-size: 0.95rem;
    }

    /* Projects Grid */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 2rem;
    }

    .project-card {
      background-color: var(--bg-card);
      border-radius: 20px;
      overflow: hidden;
      border: 1px solid var(--border-color);
      box-shadow: var(--shadow);
      transition: all 0.3s ease;
    }

    .project-card:hover {
      transform: translateY(-8px);
      box-shadow: var(--shadow-hover);
    }

    .project-img-container {
      width: 100%;
      height: 210px;
      overflow: hidden;
      position: relative;
    }

    .project-img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
    }

    .project-card:hover .project-img {
      transform: scale(1.06);
    }

    .project-info {
      padding: 1.8rem;
    }

    .project-title {
      font-size: 1.2rem;
      font-weight: 700;
      margin-bottom: 0.6rem;
      color: var(--text-main);
    }

    .project-desc {
      color: var(--text-muted);
      font-size: 0.9rem;
      margin-bottom: 1.2rem;
      line-height: 1.5;
    }

    .project-tags {
      display: flex;
      gap: 0.5rem;
      flex-wrap: wrap;
      margin-bottom: 1.5rem;
    }

    .tag {
      background-color: var(--primary-light);
      color: var(--primary-dark);
      padding: 0.3rem 0.8rem;
      border-radius: 8px;
      font-size: 0.75rem;
      font-weight: 700;
    }

    .project-link {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      color: var(--primary);
      text-decoration: none;
      font-weight: 700;
      font-size: 0.9rem;
      transition: gap 0.3s ease;
    }

    .project-link:hover {
      gap: 0.8rem;
      color: var(--primary-dark);
    }

    /* Footer */
    footer {
      background-color: var(--bg-card);
      text-align: center;
      padding: 2.5rem 0;
      color: var(--text-muted);
      font-size: 0.9rem;
      border-top: 1px solid var(--border-color);
    }

    /* Mobile Responsive */
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
        width: 220px;
        height: 220px;
        transform: rotate(0deg);
      }

      .hero-text h1 {
        font-size: 2.2rem;
      }
    }
  </style>
</head>
<body>

  <!-- Navigasi Header -->
  <header>
    <nav>
      <a href="#" class="logo">Portofolio<span>.</span></a>
      <ul class="nav-links">
        <li><a href="#home">Beranda</a></li>
        <li><a href="#projects">Projek</a></li>
        <li><a href="#contact">Kontak</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section (Foto & Info Profil) -->
  <section id="home" class="hero">
    <div class="container">
      <div class="hero-content">
        <div class="hero-text">
          <span class="badge">Selamat Datang di Portofolio Saya ✨</span>
          <h1>Halo, Saya <span>Nama Anda</span></h1>
          <p>Seorang Software Developer & UI/UX Designer yang berfokus membangun aplikasi web modern, rapi, dan mudah digunakan.</p>
          
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
            <!-- Ganti foto-profil.jpg dengan lokasi foto Anda -->
            <img src="https://via.placeholder.com/300/f3ebfc/9966cb?text=Foto+Profil" alt="Foto Profil">
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects Section (Hasil Karya / Projek) -->
  <section id="projects">
    <div class="container">
      <h2 class="section-title">Hasil Karya & Projek</h2>
      <p class="section-subtitle">Beberapa hasil karya web dan rancangan antarmuka yang telah saya selesaikan.</p>
      
      <div class="projects-grid">
        
        <!-- Projek 1 -->
        <div class="project-card">
          <div class="project-img-container">
            <img src="https://via.placeholder.com/600x400/9966cb/ffffff?text=Aplikasi+Kasir" alt="Aplikasi Kasir" class="project-img">
          </div>
          <div class="project-info">
            <h3 class="project-title">Aplikasi Kasir Web</h3>
            <p class="project-desc">Sistem Kasir Point of Sale (POS) interaktif untuk mengelola stok barang, mencatat transaksi, dan mencetak nota pembelanjaan.</p>
            <div class="project-tags">
              <span class="tag">HTML/CSS</span>
              <span class="tag">PHP</span>
              <span class="tag">SQL</span>
            </div>
            <a href="#" class="project-link">Lihat Detail <i class="fas fa-arrow-right"></i></a>
          </div>
        </div>

        <!-- Projek 2 -->
        <div class="project-card">
          <div class="project-img-container">
            <img src="https://via.placeholder.com/600x400/7b43b6/ffffff?text=Laravel+CRUD" alt="Sistem Informasi CRUD" class="project-img">
          </div>
          <div class="project-info">
            <h3 class="project-title">Sistem Data Siswa & Guru</h3>
            <p class="project-desc">Aplikasi manajemen data internal sekolah berbasis framework Laravel dengan fitur CRUD lengkap dan navigasi multi-user.</p>
            <div class="project-tags">
              <span class="tag">Laravel</span>
              <span class="tag">Blade</span>
              <span class="tag">MySQL</span>
            </div>
            <a href="#" class="project-link">Lihat Detail <i class="fas fa-arrow-right"></i></a>
          </div>
        </div>

        <!-- Projek 3 -->
        <div class="project-card">
          <div class="project-img-container">
            <img src="https://via.placeholder.com/600x400/f3ebfc/7b43b6?text=UI/UX+Figma" alt="Desain UI/UX Web" class="project-img">
          </div>
          <div class="project-info">
            <h3 class="project-title">Redesain Portal Sekolah</h3>
            <p class="project-desc">Perancangan ulang antarmuka website profil sekolah untuk meningkatkan kenyamanan pengguna dan keterbacaan informasi.</p>
            <div class="project-tags">
              <span class="tag">Figma</span>
              <span class="tag">UI/UX</span>
              <span class="tag">Wireframe</span>
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
      <p>&copy; 2026 Portofolio. Dibuat dengan warna Purple & Soft White.</p>
    </div>
  </footer>

</body>
</html>
