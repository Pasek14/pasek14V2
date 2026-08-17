<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SMK Negeri 1 Manggis</title>

<style>

/* =========================
   DASAR
========================= */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    color: #17202a;
    background: #f5f8f7;
    line-height: 1.6;
}

/* =========================
   HEADER / HERO
========================= */

.hero {
    min-height: 100vh;
    padding: 30px 8%;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;

    background:
        radial-gradient(circle at 20% 20%, rgba(0,255,170,.35), transparent 30%),
        radial-gradient(circle at 80% 30%, rgba(0,120,255,.35), transparent 30%),
        linear-gradient(135deg, #063b2c, #087f5b, #0759a5);

    color: white;
    position: relative;
    overflow: hidden;
}

/* lingkaran dekorasi */

.hero::before,
.hero::after {
    content: "";
    position: absolute;
    border-radius: 50%;
    filter: blur(3px);
}

.hero::before {
    width: 300px;
    height: 300px;
    background: rgba(255,255,255,.08);
    top: -100px;
    left: -100px;
}

.hero::after {
    width: 400px;
    height: 400px;
    background: rgba(255,255,255,.06);
    bottom: -180px;
    right: -100px;
}

.hero-content {
    max-width: 900px;
    position: relative;
    z-index: 2;
}

.logo {
    width: 110px;
    height: 110px;
    margin: auto;
    margin-bottom: 25px;

    border-radius: 30px;

    background: rgba(255,255,255,.16);
    border: 1px solid rgba(255,255,255,.3);

    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);

    display: flex;
    align-items: center;
    justify-content: center;

    font-size: 45px;
    font-weight: bold;

    box-shadow: 0 20px 50px rgba(0,0,0,.2);
}

.hero h1 {
    font-size: clamp(35px, 7vw, 75px);
    line-height: 1.05;
    margin-bottom: 20px;
}

.hero p {
    font-size: 19px;
    max-width: 700px;
    margin: auto;
    opacity: .9;
}

.hero-buttons {
    margin-top: 35px;
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
}

/* =========================
   LIQUID GLASS BUTTON
========================= */

.glass-button {
    display: inline-block;
    padding: 14px 25px;

    color: white;
    text-decoration: none;

    border-radius: 50px;

    background: rgba(255,255,255,.15);
    border: 1px solid rgba(255,255,255,.3);

    backdrop-filter: blur(15px);
    -webkit-backdrop-filter: blur(15px);

    transition: .3s;
}

.glass-button:hover {
    transform: translateY(-4px);
    background: rgba(255,255,255,.28);
    box-shadow: 0 15px 35px rgba(0,0,0,.2);
}

/* =========================
   NAVBAR
========================= */

nav {
    position: sticky;
    top: 0;
    z-index: 100;

    padding: 15px 7%;

    background: rgba(255,255,255,.75);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);

    border-bottom: 1px solid rgba(0,0,0,.08);
}

.nav-container {
    max-width: 1200px;
    margin: auto;

    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}

.nav-logo {
    font-weight: bold;
    color: #087f5b;
}

.nav-links {
    display: flex;
    gap: 20px;
    list-style: none;
}

.nav-links a {
    color: #17202a;
    text-decoration: none;
    font-size: 14px;
    font-weight: bold;
}

.nav-links a:hover {
    color: #087f5b;
}

/* =========================
   SECTION
========================= */

section {
    padding: 90px 8%;
}

.section-title {
    text-align: center;
    margin-bottom: 50px;
}

.section-title h2 {
    font-size: 40px;
    margin-bottom: 10px;
}

.section-title p {
    color: #667085;
}

/* =========================
   ABOUT
========================= */

.about {
    background: white;
}

.about-box {
    max-width: 950px;
    margin: auto;

    padding: 40px;

    border-radius: 30px;

    background: linear-gradient(135deg, #f1fff9, #eef7ff);

    border: 1px solid #dcece7;

    box-shadow: 0 20px 50px rgba(0,0,0,.06);
}

.about-box h3 {
    color: #087f5b;
    margin-bottom: 15px;
}

/* =========================
   JURUSAN
========================= */

.major-section {
    background: #eef3f2;
}

.major-grid {
    max-width: 1200px;
    margin: auto;

    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));

    gap: 25px;
}

.major-card {
    padding: 30px;

    border-radius: 28px;

    color: white;

    min-height: 340px;

    position: relative;
    overflow: hidden;

    transition: .35s;

    box-shadow: 0 20px 40px rgba(0,0,0,.12);
}

.major-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 30px 60px rgba(0,0,0,.2);
}

.major-card::after {
    content: "";
    position: absolute;

    width: 180px;
    height: 180px;

    border-radius: 50%;

    background: rgba(255,255,255,.12);

    right: -70px;
    top: -70px;
}

.major-number {
    font-size: 14px;
    opacity: .8;
}

.major-card h3 {
    font-size: 28px;
    margin: 15px 0;
}

.major-card p {
    opacity: .9;
}

.major-card h4 {
    margin-top: 20px;
    margin-bottom: 8px;
}

.major-card ul {
    padding-left: 20px;
}

/* WARNA JURUSAN */

/* Perhotelan - pink */

.hotel {
    background: linear-gradient(135deg, #ff4f9a, #d41469);
}

/* Tata Boga - ungu hitam putih */

.boga {
    background: linear-gradient(135deg, #6a11cb, #24102f);
}

/* TJKT - biru gradient */

.tjkt {
    background: linear-gradient(135deg, #006eff, #00c6ff);
}

/* TKR - biru tua */

.tkr {
    background: linear-gradient(135deg, #071a52, #123b8c);
}

/* TBSM - putih merah */

.tbsm {
    background: linear-gradient(135deg, #ffffff, #eeeeee);
    color: #9d1111;
    border: 3px solid #d71920;
}

.tbsm p {
    color: #444;
}

.tbsm .major-number {
    color: #777;
}

/* =========================
   KEUNGGULAN SEKOLAH
========================= */

.features {
    background: white;
}

.feature-grid {
    max-width: 1100px;
    margin: auto;

    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));

    gap: 20px;
}

.feature {
    padding: 30px;

    border-radius: 25px;

    background: #f7faf9;

    border: 1px solid #e5e9e7;

    transition: .3s;
}

.feature:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 35px rgba(0,0,0,.08);
}

.feature-icon {
    width: 55px;
    height: 55px;

    border-radius: 18px;

    background: linear-gradient(135deg, #087f5b, #0b72c9);

    color: white;

    display: flex;
    align-items: center;
    justify-content: center;

    font-size: 25px;

    margin-bottom: 20px;
}

.feature h3 {
    margin-bottom: 10px;
}

/* =========================
   AJAKAN
========================= */

.cta {
    background:
        radial-gradient(circle at 20% 50%, rgba(0,255,170,.2), transparent 30%),
        linear-gradient(135deg, #063b2c, #0759a5);

    color: white;
    text-align: center;
}

.cta h2 {
    font-size: 42px;
    margin-bottom: 15px;
}

.cta p {
    max-width: 700px;
    margin: auto;
    opacity: .9;
}

/* =========================
   FOOTER
========================= */

footer {
    background: #07130f;
    color: white;

    padding: 45px 8%;

    text-align: center;
}

footer h3 {
    color: #50e3a4;
    margin-bottom: 10px;
}

footer p {
    color: #9ca8a3;
}

.footer-line {
    margin-top: 25px;
    padding-top: 20px;

    border-top: 1px solid rgba(255,255,255,.1);

    font-size: 14px;
}

/* =========================
   RESPONSIVE
========================= */

@media (max-width: 700px) {

    .nav-container {
        flex-direction: column;
    }

    .nav-links {
        gap: 12px;
        flex-wrap: wrap;
        justify-content: center;
    }

    section {
        padding: 65px 5%;
    }

    .about-box {
        padding: 25px;
    }

    .cta h2 {
        font-size: 32px;
    }

}

</style>
</head>

<body>

<!-- =========================
     HERO
========================= -->

<header class="hero" id="home">

    <div class="hero-content">

        <div class="logo">
            SMK
        </div>

        <h1>
            SMK Negeri 1 Manggis
        </h1>

        <p>
            Membangun generasi terampil, kreatif,
            berkarakter, dan siap menghadapi dunia kerja
            serta masa depan digital.
        </p>

        <div class="hero-buttons">

            <a href="#tentang" class="glass-button">
                Tentang Sekolah
            </a>

            <a href="#jurusan" class="glass-button">
                Lihat Jurusan
            </a>

        </div>

    </div>

</header>


<!-- =========================
     NAVBAR
========================= -->

<nav>

    <div class="nav-container">

        <div class="nav-logo">
            SMK NEGERI 1 MANGGIS
        </div>

        <ul class="nav-links">

            <li>
                <a href="#home">Home</a>
            </li>

            <li>
                <a href="#tentang">Tentang</a>
            </li>

            <li>
                <a href="#jurusan">Jurusan</a>
            </li>

            <li>
                <a href="#keunggulan">Keunggulan</a>
            </li>

        </ul>

    </div>

</nav>


<!-- =========================
     TENTANG SEKOLAH
========================= -->

<section class="about" id="tentang">

    <div class="section-title">

        <h2>Tentang Sekolah</h2>

        <p>
            Tempat belajar, berkembang, dan mempersiapkan masa depan.
        </p>

    </div>

    <div class="about-box">

        <h3>SMK Negeri 1 Manggis</h3>

        <p>
            SMK Negeri 1 Manggis merupakan lembaga pendidikan
            kejuruan yang memberikan kesempatan kepada peserta
            didik untuk mengembangkan pengetahuan, keterampilan,
            kreativitas, dan karakter.
        </p>

        <br>

        <p>
            Melalui berbagai program keahlian, siswa tidak hanya
            belajar teori tetapi juga mendapatkan pengalaman
            praktik yang relevan dengan kebutuhan dunia kerja.
        </p>

        <br>

        <p>
            Dengan semangat belajar dan berkembang, setiap siswa
            memiliki kesempatan untuk menjadi pribadi yang
            kompeten, mandiri, kreatif, dan siap menghadapi
            tantangan masa depan.
        </p>

    </div>

</section>


<!-- =========================
     JURUSAN
========================= -->

<section class="major-section" id="jurusan">

    <div class="section-title">

        <h2>Program Keahlian</h2>

        <p>
            Pilih bidang yang sesuai dengan minat,
            bakat, dan cita-citamu.
        </p>

    </div>


    <div class="major-grid">


        <!-- PERHOTELAN -->

        <div class="major-card hotel">

            <span class="major-number">
                PROGRAM KEAHLIAN 01
            </span>

            <h3>Perhotelan</h3>

            <p>
                Jurusan Perhotelan mempersiapkan siswa
                untuk memahami dunia hospitality dan
                pelayanan profesional.
            </p>

            <h4>Keunggulan</h4>

            <ul>
                <li>Hospitality dan pelayanan</li>
                <li>Housekeeping</li>
                <li>Komunikasi dengan tamu</li>
                <li>Pengenalan industri pariwisata</li>
            </ul>

        </div>


        <!-- TATA BOGA -->

        <div class="major-card boga">

            <span class="major-number">
                PROGRAM KEAHLIAN 02
            </span>

            <h3>Tata Boga</h3>

            <p>
                Mengembangkan kreativitas melalui dunia
                kuliner, pengolahan makanan, dan penyajian.
            </p>

            <h4>Keunggulan</h4>

            <ul>
                <li>Teknik dasar memasak</li>
                <li>Pengolahan makanan</li>
                <li>Penyajian makanan</li>
                <li>Dasar usaha kuliner</li>
            </ul>

        </div>


        <!-- TJKT -->

        <div class="major-card tjkt">

            <span class="major-number">
                PROGRAM KEAHLIAN 03
            </span>

            <h3>TJKT</h3>

            <p>
                Teknik Komputer, Jaringan dan Telekomunikasi
                mempelajari teknologi komputer, jaringan,
                server, dan telekomunikasi.
            </p>

            <h4>Keunggulan</h4>

            <ul>
                <li>Konfigurasi jaringan</li>
                <li>Server dan sistem operasi</li>
                <li>Troubleshooting</li>
                <li>Teknologi telekomunikasi</li>
            </ul>

        </div>


        <!-- TKR -->

        <div class="major-card tkr">

            <span class="major-number">
                PROGRAM KEAHLIAN 04
            </span>

            <h3>TKR</h3>

            <p>
                Teknik Kendaraan Ringan mempelajari
                perawatan dan perbaikan kendaraan serta
                sistem mesin dan kelistrikan.
            </p>

            <h4>Keunggulan</h4>

            <ul>
                <li>Perawatan kendaraan</li>
                <li>Sistem mesin</li>
                <li>Kelistrikan kendaraan</li>
                <li>Troubleshooting kendaraan</li>
            </ul>

        </div>


        <!-- TBSM -->

        <div class="major-card tbsm">

            <span class="major-number">
                PROGRAM KEAHLIAN 05
            </span>

            <h3>TBSM</h3>

            <p>
                Teknik Bisnis Sepeda Motor mempersiapkan
                siswa dalam perawatan, perbaikan, dan
                pelayanan kendaraan sepeda motor.
            </p>

            <h4>Keunggulan</h4>

            <ul>
                <li>Servis sepeda motor</li>
                <li>Perawatan kendaraan</li>
                <li>Sistem mesin dan kelistrikan</li>
                <li>Dasar bisnis dan pelayanan</li>
            </ul>

        </div>

    </div>

</section>


<!-- =========================
     KEUNGGULAN
========================= -->

<section class="features" id="keunggulan">

    <div class="section-title">

        <h2>Mengapa Memilih SMK?</h2>

        <p>
            Pendidikan kejuruan memberikan pengalaman
            belajar yang dekat dengan dunia nyata.
        </p>

    </div>


    <div class="feature-grid">


        <div class="feature">

            <div class="feature-icon">
                01
            </div>

            <h3>Belajar Keterampilan</h3>

            <p>
                Siswa mendapatkan pengetahuan dan
                keterampilan sesuai bidang keahlian.
            </p>

        </div>


        <div class="feature">

            <div class="feature-icon">
                02
            </div>

            <h3>Pengalaman Praktik</h3>

            <p>
                Pembelajaran praktik membantu siswa
                memahami penerapan ilmu secara langsung.
            </p>

        </div>


        <div class="feature">

            <div class="feature-icon">
                03
            </div>

            <h3>Siap Menghadapi Dunia Kerja</h3>

            <p>
                Kompetensi yang dipelajari menjadi
                bekal untuk menghadapi kebutuhan industri.
            </p>

        </div>


        <div class="feature">

            <div class="feature-icon">
                04
            </div>

            <h3>Kreatif dan Mandiri</h3>

            <p>
                Siswa didorong untuk berpikir kreatif,
                berani mencoba, dan mengembangkan potensi.
            </p>

        </div>

    </div>

</section>


<!-- =========================
     CTA
========================= -->

<section class="cta">

    <h2>
        Temukan Potensimu.
    </h2>

    <p>
        Setiap keahlian adalah langkah menuju masa depan.
        Pilih bidang yang kamu sukai, pelajari dengan serius,
        dan jadikan keterampilanmu sebagai kekuatan.
    </p>

    <br>

    <a href="#jurusan" class="glass-button">
        Jelajahi Jurusan
    </a>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <h3>
        SMK Negeri 1 Manggis
    </h3>

    <p>
        Sekolah Kejuruan • Keterampilan • Kreativitas • Masa Depan
    </p>

    <div class="footer-line">

        Created by <strong>Pasek Web</strong>

        <br>

        © 2026 SMK Negeri 1 Manggis

    </div>

</footer>

</body>
</html>
