<!DOCTYPE html>
<html lang="in">
<head>
    <meta charset="UTF-8">
    <title>Website Profil</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            overflow-x: hidden;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            transition: background-color 0.5s ease, color 0.5s ease;
        }
        .container {
            position: relative;
            width: 100vw;
            height: 100vh;
        }
        .container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .text {
            position: absolute;
            top: 200px;
            left: 10px;
            color: white;
            background-color: rgba(0, 0, 0, 0.5);
            padding: 10px;
            font-size: 24px;
        }
        .button-marquee {
            position: absolute;
            display: inline-block;
            top: 250px;
            left: 10px;
            width: 200px;
            overflow: hidden;
            background-color: white;
            border: 1px solid #ccc;
            padding: 5px;
            text-align: center;
            color: black; /* Pastikan warna teks tetap terlihat */
        }
        .div-h2 {
            font-family: 'Georgia', serif;
            text-align: center;
            margin: 20px 0;
            font-size: 2em;
            padding-bottom: 10px;
            transition: color 0.5s ease;
        }
        .div-h2.light {
            color: #2196F3; /* Warna teks terang */
            border-bottom: 3px solid #2196F3;
        }
        .div-h2.dark {
            color: #ffffff; /* Warna teks saat mode gelap */
            border-bottom: 3px solid #ffffff;
        }
        .div-p {
            max-width: 850px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            color: #555;
            font-size: 1.1em;
            transition: background-color 0.5s ease, color 0.5s ease;
        }
        .div-p.dark {
            background-color: #1e1e1e;
            color: #e0e0e0;
        }
        .img-container {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
        }
        .img-container img {
            width: 300px;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        /* Styles for the hamburger menu */
        .hamburger-menu {
            position: fixed;
            top: 10px;
            right: 20px;
            cursor: pointer;
            z-index: 100;
        }
        .hamburger-menu div {
            width: 30px;
            height: 3px;
            background-color: black;
            margin: 6px 0;
            transition: background-color 0.3s ease;
        }
        /* Navigation menu (hidden by default) */
        .nav-menu {
            position: fixed;
            top: 0;
            right: -250px;
            width: 250px;
            height: 100%;
            background-color: #333;
            color: white;
            transition: right 0.3s ease;
            z-index: 99;
            padding-top: 20px;
            box-shadow: -2px 0 5px rgba(0, 0, 0, 0.5);
        }
        .nav-menu ul {
            list-style: none;
            padding: 0;
            margin: 50px 0;
            text-align: center;
        }
        .nav-menu ul li {
            padding: 20px;
            border-bottom: 1px solid #555;
        }
        .nav-menu ul li a {
            color: white;
            text-decoration: none;
            font-size: 18px;
        }
        /* Tanda X besar di pojok kanan atas */
        .close-menu {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 40px;
            font-weight: bold;
            cursor: pointer;
            color: white;
        }
        /* Sticky navigation */
        .sticky {
            position: fixed;
            top: 0;
            right: 0;
            z-index: 101;
        }
        /* Show the nav menu */
        .nav-menu.active {
            right: 0;
        }
        /* Hide hamburger when menu is open */
        .hamburger-menu.hide {
            display: none;
        }
        /* Dark Mode & Light Mode Toggle */
        .mode-toggle {
            position: fixed;
            top: 10px;
            left: 20px;
            cursor: pointer;
            background-color: #fff;
            padding: 10px 20px;
            border: 1px solid #ccc;
            border-radius: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            z-index: 200;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        .mode-toggle:hover {
            background-color: #e0e0e0;
        }
        /* Dark Mode Styles */
        body.dark {
            background-color: #121212;
            color: #e0e0e0;
        }
        body.dark .div-p {
            background-color: #1e1e1e;
            color: #e0e0e0;
            box-shadow: 0 4px 8px rgba(255, 255, 255, 0.1);
        }
        body.dark .hamburger-menu div {
            background-color: white;
        }
        body.dark .nav-menu {
            background-color: #222;
            color: white;
        }
        body.dark .close-menu {
            color: #fff;
        }
    </style>
</head>
<body>
    <!-- Tombol Mode Terang/Gelap -->
    <div class="mode-toggle" id="modeToggle">Mode: Gelap</div>

    <!-- Hamburger menu -->
    <div class="hamburger-menu" id="hamburgerMenu" onclick="toggleMenu()">
        <div></div>
        <div></div>
        <div></div>
    </div>
    
    <!-- Navigation menu -->
    <div class="nav-menu" id="navMenu">
        <!-- Tanda X besar di kanan atas -->
        <span class="close-menu" onclick="toggleMenu()">×</span>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#jualan">Jualan</a></li>
            <li><a href="#bantuan">Bantuan</a></li>
        </ul>
    </div>
    
    <div class="container" id="home">
        <img src="https://i.ibb.co.com/bBpNnTS/IMG-20240821-175139.jpg" alt="">
        <div class="text">BANG DAFA</div>
    </div>
    
    <button class="button-marquee">
        <marquee bgcolor="white" behavior="scroll" direction="left">
            Saya Adalah Siswa SMKN 11 KABUPATEN TANGGERANG Kelas 10 TKJ 1
        </marquee>
    </button>    
    
    <div>
        <h2 class="div-h2 light" id="about">About</h2>
        <p class="div-p">Selamat datang di Website Profil Bisnis Dafa! Saya adalah seorang pelajar yang sedang berusaha memahami dan menguasai dunia coding. Dengan semangat belajar yang tinggi, saya berkomitmen untuk terus mengeksplorasi dan meningkatkan keterampilan pemrograman. Terima kasih telah mengunjungi dan mendukung perjalanan ini!</p>
    </div>
    <center class="img-container">
        <img src="4731897fb74d16a2848b62f5676adf74.jpg" alt="">
    </center>
    
    <div class="div-h2 light" id="jualan">
        <p>Cita-cita</p>
    </div>
    <div class="div-p">
        <p>
            Cita-cita saya adalah menjadi seorang programmer handal yangmengembangkan solusi teknologi untuk memecahkan masalah di masyarakat. Saya ingin terlibat dalam proyek-proyek yang inovatif dan memberikan dampak positif, baik dalam skala kecil maupun besar.
        </p>
    </div>

    <div class="div-h2 light" id="bantuan">
        <p>Bantuan</p>
    </div>
    <div class="div-p">
        <p>
            Jika Anda memiliki pertanyaan atau butuh bantuan lebih lanjut mengenai website ini, jangan ragu untuk menghubungi saya melalui email di: dafa@example.com. Saya akan dengan senang hati membantu Anda!
        </p>
    </div>

    <script>
        const modeToggle = document.getElementById('modeToggle');
        const body = document.body;

        modeToggle.addEventListener('click', () => {
            body.classList.toggle('dark');
            modeToggle.textContent = body.classList.contains('dark') ? 'Mode: Terang' : 'Mode: Gelap';
        });

        function toggleMenu() {
            const navMenu = document.getElementById('navMenu');
            const hamburgerMenu = document.getElementById('hamburgerMenu');
            navMenu.classList.toggle('active');
            hamburgerMenu.classList.toggle('hide');
        }
    </script>
</body>
</html>
