
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>OLIVE — Cafe & Restaurant | Ordu</title>
<meta name="description" content="Olive Cafe & Restaurant — Ordu Rıhtım'da deniz manzarası eşliğinde seçkin Türk ve Dünya mutfağı.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@500;600;700&display=swap" rel="stylesheet">

<style>
:root{
  --bg:#07100d;
  --bg2:#0d1915;
  --card:#10211b;
  --gold:#c9a86a;
  --gold2:#e5ca91;
  --cream:#f5f0e5;
  --muted:#aeb8b2;
  --line:rgba(255,255,255,.10);
  --green:#19352a;
  --danger:#c65c5c;
  --success:#5fb879;
}

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

html{
  scroll-behavior:smooth;
}

body{
  background:var(--bg);
  color:var(--cream);
  font-family:"DM Sans",sans-serif;
  overflow-x:hidden;
}

a{
  color:inherit;
  text-decoration:none;
}

button,input,select,textarea{
  font:inherit;
}

.container{
  width:min(1180px,92%);
  margin:auto;
}

/* LOADER */

.loader{
  position:fixed;
  inset:0;
  z-index:9999;
  background:#06100c;
  display:flex;
  align-items:center;
  justify-content:center;
  flex-direction:column;
  transition:.8s ease;
}

.loader.hide{
  opacity:0;
  visibility:hidden;
}

.loader-logo{
  font-family:"Playfair Display",serif;
  font-size:48px;
  letter-spacing:8px;
  color:var(--gold2);
}

.loader-line{
  width:160px;
  height:1px;
  background:rgba(255,255,255,.2);
  margin-top:22px;
  overflow:hidden;
}

.loader-line span{
  display:block;
  height:100%;
  width:40%;
  background:var(--gold);
  animation:load 1.2s infinite;
}

@keyframes load{
  from{transform:translateX(-100%)}
  to{transform:translateX(300%)}
}

/* HEADER */

header{
  position:fixed;
  top:0;
  left:0;
  width:100%;
  z-index:1000;
  padding:20px 0;
  transition:.4s;
}

header.scrolled{
  background:rgba(5,12,9,.82);
  backdrop-filter:blur(18px);
  border-bottom:1px solid var(--line);
  padding:13px 0;
}

.nav{
  display:flex;
  justify-content:space-between;
  align-items:center;
}

.logo{
  font-family:"Playfair Display",serif;
  font-size:29px;
  letter-spacing:5px;
  color:white;
}

.logo span{
  color:var(--gold2);
}

.navlinks{
  display:flex;
  gap:32px;
  align-items:center;
}

.navlinks a{
  color:#e7e5df;
  font-size:14px;
  transition:.3s;
}

.navlinks a:hover{
  color:var(--gold2);
}

.nav-btn{
  border:1px solid rgba(229,202,145,.6);
  padding:11px 19px;
  border-radius:30px;
  color:var(--gold2)!important;
}

.menu-btn{
  display:none;
  border:0;
  background:none;
  color:white;
  font-size:27px;
}

/* HERO */

.hero{
  min-height:100vh;
  position:relative;
  display:flex;
  align-items:center;
  overflow:hidden;
}

.hero-bg{
  position:absolute;
  inset:0;
  background:
  linear-gradient(90deg,rgba(4,12,8,.92),rgba(4,12,8,.52),rgba(4,12,8,.25)),
  url("https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=2200&q=90")
  center/cover;
  transform:scale(1.04);
  animation:heroZoom 12s ease-out forwards;
}

@keyframes heroZoom{
  to{transform:scale(1)}
}

.hero-content{
  position:relative;
  z-index:2;
  max-width:750px;
  padding-top:80px;
}

.eyebrow{
  color:var(--gold2);
  letter-spacing:5px;
  font-size:12px;
  text-transform:uppercase;
  margin-bottom:24px;
}

.hero h1{
  font-family:"Playfair Display",serif;
  font-size:clamp(55px,8vw,105px);
  line-height:.94;
  font-weight:500;
}

.hero h1 span{
  color:var(--gold2);
}

.hero p{
  color:#d0d5d1;
  max-width:600px;
  font-size:17px;
  line-height:1.8;
  margin:30px 0;
}

.hero-buttons{
  display:flex;
  gap:14px;
  flex-wrap:wrap;
}

.btn{
  border:0;
  cursor:pointer;
  padding:15px 24px;
  border-radius:4px;
  font-weight:700;
  transition:.3s;
}

.btn-gold{
  background:var(--gold);
  color:#10130f;
}

.btn-gold:hover{
  background:var(--gold2);
  transform:translateY(-2px);
}

.btn-outline{
  background:transparent;
  color:white;
  border:1px solid rgba(255,255,255,.35);
}

.btn-outline:hover{
  border-color:var(--gold2);
  color:var(--gold2);
}

.scroll{
  position:absolute;
  bottom:28px;
  left:50%;
  transform:translateX(-50%);
  font-size:10px;
  letter-spacing:4px;
  color:#9ba39e;
}

/* SECTION */

section{
  padding:105px 0;
}

.section-head{
  margin-bottom:48px;
}

.section-label{
  color:var(--gold2);
  letter-spacing:4px;
  font-size:11px;
  text-transform:uppercase;
  margin-bottom:14px;
}

.section-title{
  font-family:"Playfair Display",serif;
  font-size:clamp(38px,5vw,65px);
  font-weight:500;
}

.section-text{
  color:var(--muted);
  line-height:1.8;
  max-width:650px;
  margin-top:18px;
}

/* STATS */

.stats{
  border-top:1px solid var(--line);
  border-bottom:1px solid var(--line);
  padding:28px 0;
  background:#09130f;
}

.stats-grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
}

.stat{
  text-align:center;
  border-right:1px solid var(--line);
}

.stat:last-child{
  border:0;
}

.stat strong{
  display:block;
  font-family:"Playfair Display",serif;
  font-size:34px;
  color:var(--gold2);
}

.stat span{
  color:#8e9993;
  font-size:12px;
}

/* MENU */

.menu-tabs{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
  margin-bottom:30px;
}

.tab{
  border:1px solid var(--line);
  background:transparent;
  color:#b9c1bc;
  padding:10px 17px;
  border-radius:30px;
  cursor:pointer;
}

.tab.active,
.tab:hover{
  background:var(--gold);
  color:#111;
  border-color:var(--gold);
}

.menu-grid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:18px;
}

.menu-card{
  background:linear-gradient(145deg,#10221b,#0b1713);
  border:1px solid var(--line);
  padding:25px;
  min-height:180px;
  transition:.35s;
}

.menu-card:hover{
  transform:translateY(-6px);
  border-color:rgba(201,168,106,.5);
}

.menu-card .category{
  color:var(--gold2);
  font-size:11px;
  letter-spacing:2px;
  text-transform:uppercase;
}

.menu-card h3{
  margin:14px 0 10px;
  font-family:"Playfair Display",serif;
  font-size:23px;
}

.menu-card p{
  color:#8f9b94;
  font-size:13px;
  line-height:1.6;
}

.price{
  display:block;
  color:var(--gold2);
  margin-top:17px;
  font-weight:700;
}

/* ABOUT */

.about{
  background:#0a1511;
}

.about-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:70px;
  align-items:center;
}

.about-img{
  height:600px;
  background:url("https://images.unsplash.com/photo-1515003197210-e0cd71810b5f?auto=format&fit=crop&w=1200&q=85")
  center/cover;
}

.about-copy p{
  color:var(--muted);
  line-height:1.9;
  margin:25px 0;
}

.features{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:18px;
}

.feature{
  border-top:1px solid var(--line);
  padding-top:18px;
}

.feature strong{
  color:var(--gold2);
  display:block;
  margin-bottom:6px;
}

.feature span{
  color:#89938e;
  font-size:13px;
}

/* GALLERY */

.gallery{
  display:grid;
  grid-template-columns:2fr 1fr 1fr;
  grid-template-rows:250px 250px;
  gap:10px;
}

.gallery div{
  overflow:hidden;
}

.gallery div:first-child{
  grid-row:span 2;
}

.gallery img{
  width:100%;
  height:100%;
  object-fit:cover;
  transition:.6s;
}

.gallery div:hover img{
  transform:scale(1.07);
}

/* RESERVATION */

.reserve{
  background:
  linear-gradient(90deg,rgba(7,16,13,.96),rgba(7,16,13,.80)),
  url("https://images.unsplash.com/photo-1414235077428-338989a2e8c0?auto=format&fit=crop&w=2000&q=85")
  center/cover fixed;
}

.reserve-box{
  background:rgba(10,24,18,.88);
  border:1px solid rgba(255,255,255,.12);
  backdrop-filter:blur(20px);
  padding:45px;
}

.step{
  display:none;
}

.step.active{
  display:block;
}

.step-title{
  font-family:"Playfair Display",serif;
  font-size:34px;
  margin-bottom:30px;
}

.form-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:18px;
}

.field{
  display:flex;
  flex-direction:column;
  gap:8px;
}

.field.full{
  grid-column:1/-1;
}

.field label{
  font-size:12px;
  color:#aab4ae;
}

.field input,
.field select,
.field textarea{
  width:100%;
  padding:15px;
  border:1px solid var(--line);
  background:#08130f;
  color:white;
  outline:none;
  border-radius:4px;
}

.field input:focus,
.field select:focus,
.field textarea:focus{
  border-color:var(--gold);
}

.people-box{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:10px;
  margin-bottom:25px;
}

.people{
  border:1px solid var(--line);
  background:#09150f;
  color:#ddd;
  padding:16px 10px;
  cursor:pointer;
  border-radius:4px;
}

.people.active{
  background:var(--gold);
  color:#111;
  border-color:var(--gold);
}

.time-grid{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:10px;
}

.time{
  padding:14px 8px;
  border:1px solid rgba(95,184,121,.4);
  background:rgba(95,184,121,.08);
  color:#bce5c6;
  cursor:pointer;
  border-radius:4px;
  text-align:center;
}

.time.full{
  border-color:rgba(198,92,92,.4);
  background:rgba(198,92,92,.09);
  color:#e89b9b;
  cursor:not-allowed;
}

.time.selected{
  background:var(--gold);
  color:#111;
  border-color:var(--gold);
}

.status{
  display:flex;
  gap:20px;
  color:#909a95;
  font-size:12px;
  margin:18px 0 25px;
}

.dot{
  display:inline-block;
  width:8px;
  height:8px;
  border-radius:50%;
  background:var(--success);
  margin-right:5px;
}

.dot.red{
  background:var(--danger);
}

.people-list{
  display:grid;
  gap:15px;
}

.person-card{
  padding:20px;
  border:1px solid var(--line);
  background:#09150f;
}

.person-card h4{
  color:var(--gold2);
  margin-bottom:12px;
}

.food-select{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
}

.summary{
  background:#08130f;
  border:1px solid var(--line);
  padding:24px;
  margin-top:25px;
}

.summary-row{
  display:flex;
  justify-content:space-between;
  padding:9px 0;
  border-bottom:1px solid rgba(255,255,255,.06);
  color:#aab3ae;
}

.summary-total{
  display:flex;
  justify-content:space-between;
  margin-top:15px;
  color:var(--gold2);
  font-size:22px;
  font-family:"Playfair Display",serif;
}

.next{
  margin-top:25px;
  width:100%;
}

/* CONTACT */

.contact-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:20px;
}

.contact-card{
  padding:30px;
  background:#0c1914;
  border:1px solid var(--line);
}

.contact-card small{
  color:var(--gold2);
  letter-spacing:2px;
}

.contact-card h3{
  margin:12px 0;
  font-size:20px;
}

.contact-card p{
  color:#929d97;
  line-height:1.7;
}

.map{
  width:100%;
  height:380px;
  border:0;
  margin-top:20px;
  filter:grayscale(.8);
}

/* FOOTER */

footer{
  border-top:1px solid var(--line);
  padding:40px 0;
  background:#050c09;
}

.footer{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:20px;
}

.footer p{
  color:#69736e;
  font-size:12px;
}

/* WHATSAPP */

.whatsapp{
  position:fixed;
  right:20px;
  bottom:20px;
  width:58px;
  height:58px;
  background:#25d366;
  color:white;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  font-weight:800;
  z-index:900;
  box-shadow:0 10px 30px rgba(0,0,0,.35);
}

/* MOBILE */

.mobile-bar{
  display:none;
}

@media(max-width:800px){

  .navlinks{
    display:none;
  }

  .menu-btn{
    display:block;
  }

  .hero{
    min-height:92vh;
  }

  .hero h1{
    font-size:58px;
  }

  .hero p{
    font-size:15px;
  }

  .stats-grid{
    grid-template-columns:1fr 1fr;
    gap:25px 0;
  }

  .stat:nth-child(2){
    border:0;
  }

  .menu-grid{
    grid-template-columns:1fr;
  }

  .about-grid,
  .contact-grid{
    grid-template-columns:1fr;
  }

  .about-img{
    height:420px;
  }

  .gallery{
    grid-template-columns:1fr 1fr;
    grid-template-rows:220px 180px 180px;
  }

  .gallery div:first-child{
    grid-column:span 2;
    grid-row:auto;
  }

  .reserve-box{
    padding:25px 18px;
  }

  .form-grid{
    grid-template-columns:1fr;
  }

  .field.full{
    grid-column:auto;
  }

  .people-box{
    grid-template-columns:repeat(3,1fr);
  }

  .time-grid{
    grid-template-columns:repeat(3,1fr);
  }

  .food-select{
    grid-template-columns:1fr;
  }

  .footer{
    flex-direction:column;
    text-align:center;
  }

  .mobile-bar{
    position:fixed;
    display:grid;
    grid-template-columns:1fr 1fr;
    left:0;
    right:0;
    bottom:0;
    z-index:800;
    background:rgba(5,12,9,.94);
    backdrop-filter:blur(15px);
    border-top:1px solid var(--line);
  }

  .mobile-bar a{
    padding:15px;
    text-align:center;
    color:white;
    font-size:13px;
  }

  .mobile-bar a:first-child{
    border-right:1px solid var(--line);
    color:var(--gold2);
  }

  .whatsapp{
    bottom:75px;
  }
}
</style>
</head>

<body>

<div class="loader" id="loader">
  <div class="loader-logo">OLIVE</div>
  <div class="loader-line"><span></span></div>
</div>

<header id="header">
  <div class="container nav">

    <a href="#" class="logo">OLI<span>V</span>E</a>

    <nav class="navlinks">
      <a href="#menu">Menü</a>
      <a href="#about">Hakkımızda</a>
      <a href="#gallery">Galeri</a>
      <a href="#reservation">Rezervasyon</a>
      <a href="#contact">İletişim</a>
      <a href="#reservation" class="nav-btn">Masa Ayırt</a>
    </nav>

    <button class="menu-btn" onclick="mobileMenu()">☰</button>
  </div>
</header>

<main>

<section class="hero">

  <div class="hero-bg"></div>

  <div class="container hero-content">

    <div class="eyebrow">ORDU • RIHITIM • 2017'DEN BERİ</div>

    <h1>
      Şehrin<br>
      <span>Lezzet</span> Noktası.
    </h1>

    <p>
      Deniz manzarası, modern atmosfer ve Türk & Dünya mutfağının
      seçkin lezzetleriyle Olive deneyimine hoş geldiniz.
    </p>

    <div class="hero-buttons">
      <a href="#reservation" class="btn btn-gold">
        Masa Ayırt →
      </a>

      <a href="#menu" class="btn btn-outline">
        Menüyü Keşfet
      </a>
    </div>

  </div>

  <div class="scroll">AŞAĞI KAYDIR ↓</div>

</section>

<section class="stats">
  <div class="container stats-grid">

    <div class="stat">
      <strong>2017</strong>
      <span>Kuruluş</span>
    </div>

    <div class="stat">
      <strong>∞</strong>
      <span>Lezzet</span>
    </div>

    <div class="stat">
      <strong>360°</strong>
      <span>Manzara</span>
    </div>

    <div class="stat">
      <strong>01</strong>
      <span>Olive Deneyimi</span>
    </div>

  </div>
</section>

<section id="menu">

<div class="container">

  <div class="section-head">
    <div class="section-label">OLIVE MENU</div>
    <h2 class="section-title">Lezzetleri keşfet.</h2>
    <p class="section-text">
      Kahvaltıdan steak'e, pizzadan tatlıya kadar Olive menüsünden
      seçilmiş lezzetler.
    </p>
  </div>

  <div class="menu-tabs">
    <button class="tab active" onclick="filterMenu('all',this)">Tümü</button>
    <button class="tab" onclick="filterMenu('et',this)">Kırmızı Et</button>
    <button class="tab" onclick="filterMenu('tavuk',this)">Beyaz Et</button>
    <button class="tab" onclick="filterMenu('burger',this)">Burger</button>
    <button class="tab" onclick="filterMenu('tatli',this)">Tatlı</button>
  </div>

  <div class="menu-grid" id="menuGrid"></div>

</div>
</section>

<section id="about" class="about">

<div class="container about-grid">

  <div class="about-img"></div>

  <div class="about-copy">

    <div class="section-label">OUR STORY</div>

    <h2 class="section-title">Denizin kıyısında<br>bir tutku.</h2>

    <p>
      Ordu Rıhtım'da konumlanan Olive, 2017'den bu yana
      modern ve zarif atmosferinde Türk ve Dünya mutfağından
      seçkin lezzetler sunuyor.
    </p>

    <p>
      Açık mutfağı, terası, kahve kültürü ve deniz manzarasıyla
      sadece yemek yemek için değil, iyi vakit geçirmek için
      tasarlanmış bir deneyim noktası.
    </p>

    <div class="features">

      <div class="feature">
        <strong>01 — Rıhtım</strong>
        <span>Deniz kenarında özel konum</span>
      </div>

      <div class="feature">
        <strong>02 — Coffee</strong>
        <span>Özenle seçilmiş kahveler</span>
      </div>

      <div class="feature">
        <strong>03 — Kitchen</strong>
        <span>Açık mutfak deneyimi</span>
      </div>

      <div class="feature">
        <strong>04 — Events</strong>
        <span>Özel organizasyon alanları</span>
      </div>

    </div>

  </div>

</div>
</section>

<section id="gallery">

<div class="container">

  <div class="section-head">
    <div class="section-label">VISUAL EXPERIENCE</div>
    <h2 class="section-title">Olive'den kareler.</h2>
  </div>

  <div class="gallery">

    <div>
      <img src="https://images.unsplash.com/photo-1515003197210-e0cd71810b5f?auto=format&fit=crop&w=1200&q=85">
    </div>

    <div>
      <img src="https://images.unsplash.com/photo-1544148103-0773bf10d330?auto=format&fit=crop&w=900&q=85">
    </div>

    <div>
      <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?auto=format&fit=crop&w=900&q=85">
    </div>

    <div>
      <img src="https://images.unsplash.com/photo-1414235077428-338989a2e8c0?auto=format&fit=crop&w=900&q=85">
    </div>

    <div>
      <img src="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=900&q=85">
    </div>

  </div>

</div>
</section>

<section id="reservation" class="reserve">

<div class="container">

  <div class="section-head">
    <div class="section-label">TABLE RESERVATION</div>
    <h2 class="section-title">Masanı ayır.</h2>
    <p class="section-text">
      Tarihini, saatini ve kişi sayısını seç.
      Ardından herkes için yemek tercihini oluştur.
    </p>
  </div>

  <div class="reserve-box">

    <!-- STEP 1 -->

    <div class="step active" id="step1">

      <div class="step-title">Rezervasyon bilgileri</div>

      <div class="form-grid">

        <div class="field">
          <label>TARİH</label>
          <input type="date" id="date">
        </div>

        <div class="field">
          <label>KİŞİ SAYISI</label>

          <div class="people-box">

            <button class="people active" onclick="selectPeople(1,this)">1</button>
            <button class="people" onclick="selectPeople(2,this)">2</button>
            <button class="people" onclick="selectPeople(3,this)">3</button>
            <button class="people" onclick="selectPeople(4,this)">4</button>
            <button class="people" onclick="selectPeople(5,this)">5</button>
            <button class="people" onclick="selectPeople(6,this)">6</button>
            <button class="people" onclick="selectPeople(7,this)">7</button>
            <button class="people" onclick="selectPeople(8,this)">8</button>
            <button class="people" onclick="selectPeople(9,this)">9</button>
            <button class="people" onclick="selectPeople(10,this)">10+</button>

          </div>

        </div>

        <div class="field full">

          <label>SAAT SEÇ</label>

          <div class="time-grid" id="times"></div>

          <div class="status">
            <span><i class="dot"></i>Müsait</span>
            <span><i class="dot red"></i>Dolu</span>
          </div>

        </div>

      </div>

      <button class="btn btn-gold next" onclick="goStep2()">
        Devam Et →
      </button>

    </div>


    <!-- STEP 2 -->

    <div class="step" id="step2">

      <div class="step-title">Misafirlerin yemekleri</div>

      <p style="color:#8f9994;margin-bottom:25px">
        Her misafir için tercih edilen ana yemeği seç.
      </p>

      <div id="peopleList" class="people-list"></div>

      <button class="btn btn-gold next" onclick="goStep3()">
        Rezervasyonu Oluştur →
      </button>

    </div>


    <!-- STEP 3 -->

    <div class="step" id="step3">

      <div class="step-title">Son bilgiler</div>

      <div class="form-grid">

        <div class="field">
          <label>AD SOYAD</label>
          <input id="customerName" placeholder="Adınız Soyadınız">
        </div>

        <div class="field">
          <label>TELEFON</label>
          <input id="customerPhone" placeholder="05xx xxx xx xx">
        </div>

        <div class="field full">
          <label>ÖZEL NOT</label>
          <textarea id="note" rows="4" placeholder="Doğum günü, özel masa, alerji vb."></textarea>
        </div>

      </div>

      <div class="summary" id="summary"></div>

      <button class="btn btn-gold next" onclick="sendReservation()">
        WhatsApp ile Rezervasyonu Gönder →
      </button>

    </div>

  </div>

</div>
</section>

<section id="contact">

<div class="container">

  <div class="section-head">
    <div class="section-label">COME VISIT US</div>
    <h2 class="section-title">Bizi bul.</h2>
  </div>

  <div class="contact-grid">

    <div class="contact-card">
      <small>ADRES</small>
      <h3>Olive Cafe & Restaurant</h3>
      <p>
        Atatürk Bulvarı No: 65<br>
        Taşbaşı Mahallesi<br>
        Ordu
      </p>
    </div>

    <div class="contact-card">
      <small>REZERVASYON</small>
      <h3>0535 962 10 10</h3>
      <p>
        Masa rezervasyonu ve özel organizasyonlar
        için bizimle iletişime geçebilirsiniz.
      </p>
    </div>

  </div>

  <iframe
    class="map"
    src="https://www.google.com/maps?q=Olive+Cafe+Restaurant+Ordu&output=embed"
    loading="lazy">
  </iframe>

</div>
</section>

</main>

<footer>

<div class="container footer">

  <div class="logo">OLI<span>V</span>E</div>

  <p>
    © 2026 Olive Cafe & Restaurant — Ordu
  </p>

  <p>
    Türk & Dünya Mutfağı
  </p>

</div>

</footer>

<a
  class="whatsapp"
  href="https://wa.me/905359621010"
  target="_blank">
  WA
</a>

<div class="mobile-bar">
  <a href="#reservation">Masa Ayırt</a>
  <a href="tel:+905359621010">Ara</a>
</div>


<script>

/* LOADER */

window.addEventListener("load",()=>{
  setTimeout(()=>{
    document.getElementById("loader").classList.add("hide");
  },900);
});


/* HEADER */

window.addEventListener("scroll",()=>{
  document.getElementById("header")
    .classList.toggle("scrolled",window.scrollY>60);
});


/* MENU DATA */

const menuData = [

 {
  name:"Lokum Bonfile",
  category:"et",
  label:"KIRMIZI ET",
  desc:"180–200 gr dana bonfile, kremalı mantarlı ıspanak ve kumpir patates.",
  price:1399
 },

 {
  name:"Dana Antrikot",
  category:"et",
  label:"KIRMIZI ET",
  desc:"Izgara dana antrikot, kremalı mantarlı ıspanak ve kumpir patates.",
  price:1099
 },

 {
  name:"Hünkar Beğendi",
  category:"et",
  label:"KIRMIZI ET",
  desc:"Dana antrikot, köz patlıcan, yoğurt ve özel garnitür.",
  price:999
 },

 {
  name:"Izgara Tavuk Bonfile",
  category:"tavuk",
  label:"BEYAZ ET",
  desc:"Piliç fileto, pirinç pilavı, köz domates, biber ve patates.",
  price:599
 },

 {
  name:"Köri Soslu Tavuk",
  category:"tavuk",
  label:"BEYAZ ET",
  desc:"Piliç fileto, sebzeler, köri sos ve kremalı makarna.",
  price:599
 },

 {
  name:"Klasik Burger",
  category:"burger",
  label:"BURGER",
  desc:"Özel burger köftesi ve Olive dokunuşları.",
  price:599
 },

 {
  name:"San Sebastian",
  category:"tatli",
  label:"TATLI",
  desc:"Belçika çikolatası ile servis edilen cheesecake.",
  price:399
 },

 {
  name:"Dubai Cup",
  category:"tatli",
  label:"TATLI",
  desc:"Pastacı kreması, çikolata sosu ve fıstık kreması.",
  price:389
 }

];


function renderMenu(filter="all"){

 const grid=document.getElementById("menuGrid");

 grid.innerHTML="";

 menuData
 .filter(x=>filter==="all"||x.category===filter)
 .forEach(x=>{

   grid.innerHTML+=`

   <div class="menu-card">

     <span class="category">${x.label}</span>

     <h3>${x.name}</h3>

     <p>${x.desc}</p>

     <span class="price">${x.price.toLocaleString("tr-TR")} ₺</span>

   </div>

   `;

 });

}

renderMenu();


function filterMenu(category,button){

 document
 .querySelectorAll(".tab")
 .forEach(x=>x.classList.remove("active"));

 button.classList.add("active");

 renderMenu(category);
}


/* RESERVATION */

let selectedPeople=1;
let selectedTime="";
let guestFoods=[];


/*
 DEMO DOLU SAATLER

 Gerçek sistemde bu bilgiler
 veritabanından gelecek.
*/

const fullTimes = [
 "14:00",
 "18:30",
 "20:00"
];

const times=[
 "12:00",
 "12:30",
 "13:00",
 "13:30",
 "14:00",
 "14:30",
 "15:00",
 "15:30",
 "16:00",
 "16:30",
 "17:00",
 "17:30",
 "18:00",
 "18:30",
 "19:00",
 "19:30",
 "20:00",
 "20:30",
 "21:00",
 "21:30",
 "22:00"
];


function renderTimes(){

 const box=document.getElementById("times");

 box.innerHTML="";

 times.forEach(time=>{

   const isFull=fullTimes.includes(time);

   const button=document.createElement("button");

   button.className="time"+(isFull?" full":"");

   button.textContent=isFull
     ? time+" • DOLU"
     : time;

   if(!isFull){

     button.onclick=()=>{

       document
       .querySelectorAll(".time")
       .forEach(x=>x.classList.remove("selected"));

       button.classList.add("selected");

       selectedTime=time;
     };

   }

   box.appendChild(button);

 });

}

renderTimes();


function selectPeople(number,button){

 selectedPeople=number;

 document
 .querySelectorAll(".people")
 .forEach(x=>x.classList.remove("active"));

 button.classList.add("active");
}


function goStep2(){

 if(!document.getElementById("date").value){
   alert("Lütfen tarih seçin.");
   return;
 }

 if(!selectedTime){
   alert("Lütfen müsait bir saat seçin.");
   return;
 }

 createPeople();

 document.getElementById("step1").classList.remove("active");
 document.getElementById("step2").classList.add("active");

 window.scrollTo({
   top:document.getElementById("reservation").offsetTop-80,
   behavior:"smooth"
 });

}


function createPeople(){

 const list=document.getElementById("peopleList");

 list.innerHTML="";

 guestFoods=[];

 for(let i=1;i<=selectedPeople;i++){

   guestFoods.push({
     name:"Misafir "+i,
     food:"",
     price:0
   });

   list.innerHTML+=`

   <div class="person-card">

     <h4>Misafir ${i}</h4>

     <div class="field">

       <label>YEMEK TERCİHİ</label>

       <select onchange="setFood(${i-1},this.value)">

         <option value="">Yemek seçiniz</option>

         ${menuData.map((x,index)=>`

           <option value="${index}">
             ${x.name} — ${x.price.toLocaleString("tr-TR")} ₺
           </option>

         `).join("")}

       </select>

     </div>

   </div>

   `;

 }

}


function setFood(index,value){

 if(value===""){
   guestFoods[index].food="";
   guestFoods[index].price=0;
   return;
 }

 const item=menuData[Number(value)];

 guestFoods[index].food=item.name;
 guestFoods[index].price=item.price;
}


function goStep3(){

 const missing=guestFoods.some(x=>!x.food);

 if(missing){
   alert("Lütfen tüm misafirler için yemek seçin.");
   return;
 }

 document.getElementById("step2").classList.remove("active");
 document.getElementById("step3").classList.add("active");

 createSummary();

 window.scrollTo({
   top:document.getElementById("reservation").offsetTop-80,
   behavior:"smooth"
 });

}


function createSummary(){

 const total=guestFoods.reduce(
   (sum,item)=>sum+item.price,
   0
 );

 let html=`

 <div class="summary-row">
   <span>Tarih</span>
   <strong>${document.getElementById("date").value}</strong>
 </div>

 <div class="summary-row">
   <span>Saat</span>
   <strong>${selectedTime}</strong>
 </div>

 <div class="summary-row">
   <span>Kişi</span>
   <strong>${selectedPeople}</strong>
 </div>

 `;

 guestFoods.forEach((guest,index)=>{

   html+=`

   <div class="summary-row">
     <span>${guest.name}</span>
     <strong>${guest.food}</strong>
   </div>

   `;

 });

 html+=`

 <div class="summary-total">
   <span>Tahmini Toplam</span>
   <strong>${total.toLocaleString("tr-TR")} ₺</strong>
 </div>

 `;

 document.getElementById("summary").innerHTML=html;
}


function sendReservation(){

 const name=document.getElementById("customerName").value.trim();
 const phone=document.getElementById("customerPhone").value.trim();
 const note=document.getElementById("note").value.trim();

 if(!name||!phone){

   alert("Lütfen adınızı ve telefon numaranızı girin.");

   return;
 }

 const total=guestFoods.reduce(
   (sum,item)=>sum+item.price,
   0
 );

 let message=
 `OLIVE CAFE & RESTAURANT REZERVASYON%0A%0A`+

 `👤 Ad Soyad: ${encodeURIComponent(name)}%0A`+
 `📱 Telefon: ${encodeURIComponent(phone)}%0A`+
 `📅 Tarih: ${encodeURIComponent(document.getElementById("date").value)}%0A`+
 `🕐 Saat: ${encodeURIComponent(selectedTime)}%0A`+
 `👥 Kişi: ${selectedPeople}%0A%0A`+

 `🍽️ YEMEK TERCİHLERİ%0A`;

 guestFoods.forEach((guest,index)=>{

   message+=
   `${index+1}. ${encodeURIComponent(guest.food)}%0A`;

 });

 message+=
 `%0A💰 Tahmini toplam: ${total.toLocaleString("tr-TR")} TL%0A`;

 if(note){
   message+=
   `%0A📝 Not: ${encodeURIComponent(note)}`;
 }

 window.open(
   "https://wa.me/905359621010?text="+message,
   "_blank"
 );

}


/* DATE */

const dateInput=document.getElementById("date");

const today=new Date();

const yyyy=today.getFullYear();

const mm=String(today.getMonth()+1).padStart(2,"0");

const dd=String(today.getDate()).padStart(2,"0");

dateInput.min=`${yyyy}-${mm}-${dd}`;


/* MOBILE MENU */

function mobileMenu(){

 const nav=document.querySelector(".navlinks");

 if(nav.style.display==="flex"){
   nav.style.display="";
 }else{
   nav.style.display="flex";
   nav.style.position="absolute";
   nav.style.top="70px";
   nav.style.left="4%";
   nav.style.right="4%";
   nav.style.background="rgba(5,12,9,.97)";
   nav.style.padding="25px";
   nav.style.flexDirection="column";
   nav.style.border="1px solid rgba(255,255,255,.1)";
 }

}

</script>

</body>
</html>
