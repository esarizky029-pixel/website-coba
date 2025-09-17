<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UPTD Dinas PUTR Bidang SDA Wilayah Talaga</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        /* Header Styles */
        .header {
            background: linear-gradient(135deg, #2c5aa0 0%, #1e3a8a 100%);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-top {
            background-color: rgba(255,255,255,0.1);
            padding: 0.5rem 0;
            font-size: 0.9rem;
        }

        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            align-items: center;
            justify-content: between;
            gap: 2rem;
        }

        .logo-section {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo {
            width: 80px;
            height: 80px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .logo img {
            width: 60px;
            height: 60px;
            object-fit: contain;
        }

        .org-info h1 {
            font-size: 1.8rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .org-info p {
            font-size: 1rem;
            opacity: 0.9;
        }

        /* Navigation */
        .navbar {
            background-color: rgba(255,255,255,0.1);
            padding: 1rem 0;
            margin-top: 1rem;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
            justify-content: center;
        }

        .nav-menu li a {
            color: white;
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .nav-menu li a:hover, .nav-menu li a.active {
            background-color: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(44, 90, 160, 0.8), rgba(30, 58, 138, 0.8));
            padding: 4rem 0;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/2827294c-8809-4521-a405-a43055bed88e.png');
            background-size: cover;
            background-position: center;
            z-index: -1;
        }

        .hero-bg-img {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -1;
            opacity: 0.3;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 0 2rem;
            position: relative;
            z-index: 2;
        }

        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.95;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #f59e0b, #d97706);
            color: white;
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(245, 158, 11, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(245, 158, 11, 0.4);
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Section Styles */
        .section {
            padding: 4rem 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #2c5aa0;
            position: relative;
        }

        .section-title::after {
            content: '';
            width: 80px;
            height: 4px;
            background: linear-gradient(45deg, #2c5aa0, #1e3a8a);
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        /* About Section */
        .about {
            background: white;
            border-radius: 15px;
            padding: 3rem;
            margin: 2rem 0;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-image {
            position: relative;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .about-image img {
            width: 100%;
            height: 300px;
            object-fit: cover;
        }

        .about-content h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: #2c5aa0;
        }

        .about-content p {
            margin-bottom: 1rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        /* Services Grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .service-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            border-top: 4px solid #2c5aa0;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.15);
        }

        .service-icon {
            font-size: 3rem;
            color: #2c5aa0;
            margin-bottom: 1rem;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .service-card p {
            color: #666;
            line-height: 1.6;
        }

        /* Stats Section */
        .stats {
            background: linear-gradient(135deg, #2c5aa0, #1e3a8a);
            color: white;
            padding: 4rem 0;
            position: relative;
        }

        .stats-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            opacity: 0.1;
            z-index: 1;
        }

        .stats-content {
            position: relative;
            z-index: 2;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            text-align: center;
        }

        .stat-item {
            padding: 2rem;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: #f59e0b;
        }

        .stat-label {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-top: 2rem;
        }

        .contact-info {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
            padding: 1rem;
            background: #f8f9fa;
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            background: #e9ecef;
            transform: translateX(5px);
        }

        .contact-icon {
            font-size: 1.5rem;
            color: #2c5aa0;
            width: 40px;
            text-align: center;
        }

        .map-container {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            height: 400px;
            position: relative;
        }

        .map-placeholder {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* News Section */
        .news-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .news-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .news-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.15);
        }

        .news-image {
            height: 200px;
            overflow: hidden;
        }

        .news-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .news-card:hover .news-image img {
            transform: scale(1.05);
        }

        .news-content {
            padding: 1.5rem;
        }

        .news-date {
            color: #2c5aa0;
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }

        .news-title {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .news-excerpt {
            color: #666;
            line-height: 1.6;
        }

        /* Footer */
        .footer {
            background: #1a202c;
            color: white;
            padding: 3rem 0 1rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1rem;
            color: #f59e0b;
        }

        .footer-section p, .footer-section li {
            margin-bottom: 0.5rem;
            opacity: 0.8;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section a {
            color: white;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: #f59e0b;
        }

        .footer-bottom {
            border-top: 1px solid #374151;
            padding-top: 2rem;
            text-align: center;
            opacity: 0.7;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }

            .nav-menu {
                flex-direction: column;
                gap: 0.5rem;
            }

            .hero h2 {
                font-size: 2rem;
            }

            .about-grid, .contact-grid {
                grid-template-columns: 1fr;
            }

            .container {
                padding: 0 1rem;
            }

            .section {
                padding: 2rem 0;
            }
        }

        /* Animation */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .animate-fade-in {
            animation: fadeInUp 0.8s ease-out;
        }

        /* Scroll behavior */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="header-top">
            <div class="container">
                <div style="text-align: center;">
                    <i class="fas fa-phone"></i> (021) 123-4567 | 
                    <i class="fas fa-envelope"></i> info@uptdtalaga.go.id
                </div>
            </div>
        </div>
        
        <div class="header-content">
            <div class="logo-section">
                <div class="logo">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a75c3be4-0d22-4c79-8e22-369b0e7e8bd4.png" alt="Logo resmi Pemerintah Indonesia dengan Garuda Pancasila berwarna emas pada latar belakang putih" />
                </div>
                <div class="org-info">
                    <h1>UPTD DINAS PUTR</h1>
                    <p>Bidang Sumber Daya Air Wilayah Talaga</p>
                </div>
            </div>
        </div>

        <nav class="navbar">
            <div class="nav-container">
                <ul class="nav-menu">
                    <li><a href="#home" class="active">Beranda</a></li>
                    <li><a href="#about">Tentang Kami</a></li>
                    <li><a href="#services">Layanan</a></li>
                    <li><a href="#news">Berita</a></li>
                    <li><a href="#contact">Kontak</a></li>
                </ul>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/838dab0c-801b-4a56-9804-7bba74bfbe6f.png" alt="Panorama infrastruktur sumber daya air dengan bendungan besar, saluran irigasi hijau, dan pegunungan di latar belakang pada siang hari cerah" class="hero-bg-img" />
        <div class="hero-content">
            <h2>Mengelola Sumber Daya Air untuk Kesejahteraan Masyarakat</h2>
            <p>Unit Pelaksana Teknis Daerah Dinas Pekerjaan Umum dan Tata Ruang Bidang Sumber Daya Air Wilayah Talaga berkomitmen untuk pengelolaan dan pelestarian sumber daya air yang berkelanjutan</p>
            <a href="#services" class="cta-button">Lihat Layanan Kami</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">Tentang Kami</h2>
            <div class="about">
                <div class="about-grid">
                    <div class="about-content">
                        <h3>Visi & Misi UPTD</h3>
                        <p><strong>Visi:</strong> Menjadi institusi terdepan dalam pengelolaan sumber daya air yang berkelanjutan dan bermanfaat bagi kesejahteraan masyarakat Talaga.</p>
                        <p><strong>Misi:</strong></p>
                        <ul style="margin-left: 1.5rem; margin-bottom: 1rem;">
                            <li>Mengelola dan melestarikan sumber daya air secara optimal</li>
                            <li>Memberikan pelayanan prima kepada masyarakat</li>
                            <li>Mengembangkan infrastruktur air yang berkelanjutan</li>
                            <li>Meningkatkan kapasitas SDM dalam bidang sumber daya air</li>
                        </ul>
                    </div>
                    <div class="about-image">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/d55650b5-fd68-4aec-afd4-2fc29e86a37e.png" alt="Tim profesional UPTD sedang melakukan inspeksi lapangan di area bendungan dengan mengenakan helm safety berwarna kuning dan rompi reflektif" />
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="section" style="background: #f8f9fa;">
        <div class="container">
            <h2 class="section-title">Layanan Kami</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-water"></i>
                    </div>
                    <h3>Pengelolaan Irigasi</h3>
                    <p>Pemeliharaan dan pengembangan jaringan irigasi untuk mendukung sektor pertanian dan ketahanan pangan masyarakat</p>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tint"></i>
                    </div>
                    <h3>Pengendalian Banjir</h3>
                    <p>Sistem pengendalian banjir dan drainase untuk melindungi pemukiman dan infrastruktur dari ancaman banjir</p>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Monitoring Kualitas Air</h3>
                    <p>Pemantauan dan pengawasan kualitas air sungai, waduk, dan sumber air lainnya secara berkala</p>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-file-alt"></i>
                    </div>
                    <h3>Perizinan SDA</h3>
                    <p>Pelayanan perizinan penggunaan sumber daya air untuk berbagai keperluan industri dan domestik</p>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <h3>Pemeliharaan Infrastruktur</h3>
                    <p>Pemeliharaan rutin dan perbaikan infrastruktur sumber daya air seperti bendungan, tanggul, dan pintu air</p>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <h3>Edukasi Masyarakat</h3>
                    <p>Program sosialisasi dan edukasi kepada masyarakat tentang pentingnya konservasi sumber daya air</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/40cc8fb4-0ba0-4bff-a3ce-91642e45c53f.png" alt="Aerial view kompleks infrastruktur air modern dengan bendungan besar dan sistem irigasi yang tersebar di landscape hijau" class="stats-bg" />
        <div class="stats-content">
            <div class="container">
                <div class="stats-grid">
                    <div class="stat-item">
                        <div class="stat-number" data-target="15">0</div>
                        <div class="stat-label">Desa Terlayani</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number" data-target="2500">0</div>
                        <div class="stat-label">Hektar Irigasi</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number" data-target="8">0</div>
                        <div class="stat-label">Bendungan Dikelola</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number" data-target="50000">0</div>
                        <div class="stat-label">Masyarakat Terlayani</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- News Section -->
    <section id="news" class="section">
        <div class="container">
            <h2 class="section-title">Berita & Pengumuman</h2>
            <div class="news-grid">
                <div class="news-card">
                    <div class="news-image">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/780c6e75-a521-4d6f-94fd-4fee3df6311d.png" alt="Upacara peresmian proyek bendungan baru dengan pejabat pemerintah dan masyarakat setempat berkumpul di area konstruksi" />
                    </div>
                    <div class="news-content">
                        <div class="news-date">15 Desember 2024</div>
                        <h3 class="news-title">Peresmian Bendungan Talaga Baru</h3>
                        <p class="news-excerpt">Bendungan Talaga Baru resmi diresmikan oleh Bupati dengan kapasitas tampung 5 juta m³ air untuk mendukung irigasi pertanian...</p>
                    </div>
                </div>

                <div class="news-card">
                    <div class="news-image">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/dbb13e68-ef49-4631-a5ef-9eeb52ffb6e0.png" alt="Workshop pelatihan dengan peserta duduk di ruangan modern menghadap layar presentasi tentang teknologi pengelolaan air" />
                    </div>
                    <div class="news-content">
                        <div class="news-date">10 Desember 2024</div>
                        <h3 class="news-title">Pelatihan Pengelolaan Air Berkelanjutan</h3>
                        <p class="news-excerpt">UPTD mengadakan pelatihan untuk meningkatkan kapasitas petugas dalam pengelolaan sumber daya air yang ramah lingkungan...</p>
                    </div>
                </div>

                <div class="news-card">
                    <div class="news-image">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/aa326006-e72d-4cb2-ad68-8ee340b61788.png" alt="Kegiatan sosialisasi di balai desa dengan petugas UPTD memberikan presentasi kepada warga desa yang duduk mendengarkan" />
                    </div>
                    <div class="news-content">
                        <div class="news-date">5 Desember 2024</div>
                        <h3 class="news-title">Sosialisasi Konservasi Air di Desa</h3>
                        <p class="news-excerpt">Program sosialisasi konservasi air dilaksanakan di 5 desa untuk meningkatkan kesadaran masyarakat tentang pentingnya menjaga sumber air...</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section" style="background: #f8f9fa;">
        <div class="container">
            <h2 class="section-title">Hubungi Kami</h2>
            <div class="contact-grid">
                <div class="contact-info">
                    <h3 style="margin-bottom: 1.5rem; color: #2c5aa0;">Informasi Kontak</h3>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <strong>Alamat:</strong><br>
                            2879+V6P, Jl. Desa, Ganeas, Kec. Talaga<br>
                            Kabupaten Majalengka, Jawa Barat 45463
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <strong>Telepon:</strong><br>
                            (0233) 123-4567
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <strong>Email:</strong><br>
                            info@uptdtalaga.go.id
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div>
                            <strong>Jam Operasional:</strong><br>
                            Senin - Jumat: 08:00 - 16:00 WIB<br>
                            Sabtu: 08:00 - 12:00 WIB
                        </div>
                    </div>
                </div>

                <div class="map-container">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/265580e6-b043-42c3-af61-aba2a9b36be2.png" alt="Peta lokasi UPTD Dinas PUTR Bidang SDA Wilayah Talaga dengan marker merah menunjukkan posisi kantor di Jalan Raya Talaga" class="map-placeholder" />
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>UPTD Dinas PUTR Bidang SDA</h3>
                    <p>Unit Pelaksana Teknis Daerah yang berkomitmen dalam pengelolaan sumber daya air untuk kesejahteraan masyarakat Talaga.</p>
                    <div style="margin-top: 1rem;">
                        <a href="#" style="margin-right: 1rem; font-size: 1.5rem;"><i class="fab fa-facebook"></i></a>
                        <a href="#" style="margin-right: 1rem; font-size: 1.5rem;"><i class="fab fa-twitter"></i></a>
                        <a href="#" style="margin-right: 1rem; font-size: 1.5rem;"><i class="fab fa-instagram"></i></a>
                        <a href="#" style="font-size: 1.5rem;"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>

                <div class="footer-section">
                    <h3>Layanan</h3>
                    <ul>
                        <li><a href="#">Pengelolaan Irigasi</a></li>
                        <li><a href="#">Pengendalian Banjir</a></li>
                        <li><a href="#">Monitoring Kualitas Air</a></li>
                        <li><a href="#">Perizinan SDA</a></li>
                        <li><a href="#">Pemeliharaan Infrastruktur</a></li>
                    </ul>
                </div>

                <div class="footer-section">
                    <h3>Informasi</h3>
                    <ul>
                        <li><a href="#">Profil UPTD</a></li>
                        <li><a href="#">Struktur Organisasi</a></li>
                        <li><a href="#">Visi & Misi</a></li>
                        <li><a href="#">Tugas & Fungsi</a></li>
                        <li><a href="#">Laporan Kinerja</a></li>
                    </ul>
                </div>

                <div class="footer-section">
                    <h3>Kontak</h3>
                    <p><i class="fas fa-map-marker-alt"></i> Jl. Raya Talaga No. 123, Majalengka</p>
                    <p><i class="fas fa-phone"></i> (0233) 123-4567</p>
                    <p><i class="fas fa-envelope"></i> info@uptdtalaga.go.id</p>
                    <p><i class="fas fa-globe"></i> www.uptdtalaga.go.id</p>
                </div>
            </div>

            <div class="footer-bottom">
                <p>© 2024 UPTD Dinas PUTR Bidang SDA Wilayah Talaga. Hak Cipta Dilindungi.</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Active navigation highlighting
        window.addEventListener('scroll', () => {
            const sections = document.querySelectorAll('section[id]');
            const navLinks = document.querySelectorAll('.nav-menu a');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (window.pageYOffset >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });

        // Counter animation for stats
        function animateCounters() {
            const counters = document.querySelectorAll('.stat-number');
            
            counters.forEach(counter => {
                const target = parseInt(counter.getAttribute('data-target'));
                const count = parseInt(counter.innerText);
                const increment = target / 100;
                
                if (count < target) {
                    counter.innerText = Math.ceil(count + increment);
                    setTimeout(() => animateCounters(), 10);
                } else {
                    counter.innerText = target.toLocaleString();
                }
            });
        }

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate-fade-in');
                    
                    // Trigger counter animation when stats section is visible
                    if (entry.target.classList.contains('stats')) {
                        animateCounters();
                    }
                }
            });
        }, observerOptions);

        // Observe sections for animation
        document.querySelectorAll('section, .service-card, .news-card').forEach(el => {
            observer.observe(el);
        });

        // Mobile menu toggle (if needed in future)
        function toggleMobileMenu() {
            const navMenu = document.querySelector('.nav-menu');
            navMenu.classList.toggle('active');
        }

        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('.header');
            if (window.scrollY > 100) {
                header.style.boxShadow = '0 4px 20px rgba(0,0,0,0.2)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0,0,0,0.1)';
            }
        });

        // Loading animation
        window.addEventListener('load', () => {
            document.body.style.opacity = '0';
            setTimeout(() => {
                document.body.style.transition = 'opacity 0.5s ease-in-out';
                document.body.style.opacity = '1';
            }, 100);
        });

        // Form validation (if forms are added later)
        function validateForm(form) {
            const inputs = form.querySelectorAll('input[required], textarea[required]');
            let isValid = true;
            
            inputs.forEach(input => {
                if (!input.value.trim()) {
                    input.style.borderColor = '#dc3545';
                    isValid = false;
                } else {
                    input.style.borderColor = '#28a745';
                }
            });
            
            return isValid;
        }

        // Back to top button functionality
        const backToTop = document.createElement('button');
        backToTop.innerHTML = '<i class="fas fa-chevron-up"></i>';
        backToTop.className = 'back-to-top';
        backToTop.style.cssText = `
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #2c5aa0;
            color: white;
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            cursor: pointer;
            display: none;
            z-index: 1000;
            box-shadow: 0 4px 15px rgba(44, 90, 160, 0.3);
            transition: all 0.3s ease;
        `;

        document.body.appendChild(backToTop);

        window.addEventListener('scroll', () => {
            if (window.scrollY > 300) {
                backToTop.style.display = 'block';
            } else {
                backToTop.style.display = 'none';
            }
        });

        backToTop.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });

        backToTop.addEventListener('mouseenter', () => {
            backToTop.style.transform = 'translateY(-3px)';
            backToTop.style.boxShadow = '0 6px 20px rgba(44, 90, 160, 0.4)';
        });

        backToTop.addEventListener('mouseleave', () => {
            backToTop.style.transform = 'translateY(0)';
            backToTop.style.boxShadow = '0 4px 15px rgba(44, 90, 160, 0.3)';
        });
    </script>
</body>
</html>

