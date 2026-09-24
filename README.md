# <!DOCTYPE html>

<html lang="da">
<head>
 <meta charset="UTF-8" />
 <meta name="viewport" content="width=device-width, initial-scale=1.0" />

<title>Isak Barber | Barber i Solbjerg</title>

<meta name="theme-color" content="#090909" />

<meta property="og:title" content="Isak Barber | Solbjerg" />
 <meta
   property="og:description"
   content="Din lokale barber i Solbjerg. Se billeder, vælg en ledig tid og book hos Isak Barber."
 />
 <meta property="og:type" content="website" />

<link rel="preconnect" href="https://fonts.googleapis.com" />
 <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
 <link
   href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700;800&display=swap"
   rel="stylesheet"
 />

<style>
   :root {
     --bg: #080808;
     --bg-soft: #111111;
     --card: #151515;
     --text: #f5f2eb;
     --muted: #aaa59b;
     --gold: #d7ad62;
     --gold-light: #efd08e;
     --border: rgba(255,255,255,.09);
     --radius: 22px;
     --max: 1180px;
     --success: #8fd6a4;
   }

   * {
     box-sizing: border-box;
     margin: 0;
     padding: 0;
   }

   html {
     scroll-behavior: smooth;
   }

   body {
     font-family: "DM Sans", sans-serif;
     background: var(--bg);
     color: var(--text);
     line-height: 1.6;
     overflow-x: hidden;
   }

   a {
     color: inherit;
     text-decoration: none;
   }

   img {
     display: block;
     width: 100%;
   }

   button,
   input,
   select,
   textarea {
     font: inherit;
   }

   .container {
     width: min(92%, var(--max));
     margin: auto;
   }

   header {
     position: fixed;
     top: 0;
     width: 100%;
     z-index: 1000;
     background: rgba(8,8,8,.78);
     backdrop-filter: blur(18px);
     border-bottom: 1px solid transparent;
     transition: .3s ease;
   }

   header.scrolled {
     border-bottom-color: var(--border);
   }

   .nav {
     min-height: 78px;
     display: flex;
     align-items: center;
     justify-content: space-between;
     gap: 30px;
   }

   .logo {
     font-family: "Playfair Display", serif;
     font-size: 25px;
     font-weight: 800;
     letter-spacing: -.5px;
   }

   .logo span {
     color: var(--gold);
   }

   .nav-links {
     display: flex;
     gap: 28px;
     align-items: center;
     list-style: none;
   }

   .nav-links a {
     color: #d8d4cc;
     font-size: 14px;
     transition: .2s;
   }

   .nav-links a:hover {
     color: var(--gold-light);
   }

   .nav-book {
     padding: 12px 20px;
     border-radius: 100px;
     background: var(--gold);
     color: #080808 !important;
     font-weight: 700;
   }

   .menu-btn {
     display: none;
     background: none;
     border: 0;
     color: white;
     font-size: 27px;
     cursor: pointer;
   }

   .hero {
     min-height: 100vh;
     display: grid;
     place-items: center;
     position: relative;
     overflow: hidden;
     padding: 140px 0 80px;
     background:
       linear-gradient(90deg, rgba(0,0,0,.82), rgba(0,0,0,.42)),
       url("https://images.unsplash.com/photo-1621605815971-fbc98d665033?auto=format&fit=crop&w=2200&q=85")
       center/cover no-repeat;
   }

   .hero::before {
     content: "";
     position: absolute;
     inset: 0;
     background:
       radial-gradient(circle at 75% 25%, rgba(215,173,98,.2), transparent 30%),
       linear-gradient(rgba(255,255,255,.018) 1px, transparent 1px),
       linear-gradient(90deg, rgba(255,255,255,.018) 1px, transparent 1px);
     background-size: auto, 60px 60px, 60px 60px;
     pointer-events: none;
   }

   .hero-content {
     position: relative;
     max-width: 850px;
     text-align: center;
     z-index: 2;
   }

   .eyebrow {
     display: inline-flex;
     align-items: center;
     gap: 10px;
     color: var(--gold-light);
     text-transform: uppercase;
     letter-spacing: 3px;
     font-size: 12px;
     font-weight: 700;
     margin-bottom: 25px;
   }

   .eyebrow::before,
   .eyebrow::after {
     content: "";
     width: 30px;
     height: 1px;
     background: var(--gold);
   }

   h1 {
     font-family: "Playfair Display", serif;
     font-size: clamp(58px, 9vw, 110px);
     line-height: .92;
     letter-spacing: -4px;
     margin-bottom: 30px;
   }

   h1 span {
     color: var(--gold);
     display: block;
   }

   .hero p {
     max-width: 650px;
     margin: auto;
     color: #d4d0c8;
     font-size: 18px;
   }

   .hero-buttons {
     margin-top: 38px;
     display: flex;
     justify-content: center;
     gap: 14px;
     flex-wrap: wrap;
   }

   .btn {
     display: inline-flex;
     align-items: center;
     justify-content: center;
     gap: 9px;
     min-height: 54px;
     padding: 0 27px;
     border-radius: 100px;
     border: 1px solid var(--border);
     font-weight: 700;
     transition: transform .2s, background .2s, border .2s;
     cursor: pointer;
   }

   .btn:hover {
     transform: translateY(-3px);
   }

   .btn-primary {
     background: var(--gold);
     color: #080808;
     border-color: var(--gold);
   }

   .btn-primary:hover {
     background: var(--gold-light);
   }

   .btn-secondary {
     background: rgba(255,255,255,.08);
   }

   .btn-secondary:hover {
     border-color: rgba(215,173,98,.5);
   }

   section {
     padding: 110px 0;
   }

   .section-head {
     text-align: center;
     max-width: 700px;
     margin: 0 auto 60px;
   }

   .section-label {
     color: var(--gold);
     text-transform: uppercase;
     letter-spacing: 3px;
     font-size: 12px;
     font-weight: 700;
     margin-bottom: 13px;
   }

   h2 {
     font-family: "Playfair Display", serif;
     font-size: clamp(38px, 6vw, 62px);
     line-height: 1;
     margin-bottom: 18px;
   }

   .section-head p {
     color: var(--muted);
   }

   .trust {
     background: var(--bg-soft);
     border-top: 1px solid var(--border);
     border-bottom: 1px solid var(--border);
   }

   .trust-grid {
     display: grid;
     grid-template-columns: repeat(3, 1fr);
     text-align: center;
   }

   .trust-item {
     padding: 28px;
     border-right: 1px solid var(--border);
   }

   .trust-item:last-child {
     border: 0;
   }

   .trust-number {
     font-family: "Playfair Display", serif;
     font-size: 37px;
     color: var(--gold);
   }

   .trust-label {
     color: var(--muted);
     font-size: 14px;
   }

   .services {
     background: #0a0a0a;
   }

   .service-grid {
     display: grid;
     grid-template-columns: repeat(3, 1fr);
     gap: 18px;
   }

   .service {
     padding: 32px;
     border: 1px solid var(--border);
     border-radius: var(--radius);
     background: linear-gradient(145deg, #151515, #0e0e0e);
     transition: .25s;
   }

   .service:hover {
     transform: translateY(-6px);
     border-color: rgba(215,173,98,.35);
   }

   .service-icon {
     font-size: 31px;
     margin-bottom: 20px;
   }

   .service h3 {
     font-family: "Playfair Display", serif;
     font-size: 25px;
     margin-bottom: 10px;
   }

   .service p {
     color: var(--muted);
     font-size: 14px;
   }

   .gallery {
     background: #0a0a0a;
   }

   .gallery-grid {
     display: grid;
     grid-template-columns: 1.35fr .8fr .8fr;
     grid-template-rows: 250px 250px;
     gap: 16px;
   }

   .gallery-item {
     position: relative;
     overflow: hidden;
     border-radius: var(--radius);
     border: 1px solid var(--border);
     background: #151515;
   }

   .gallery-item:first-child {
     grid-row: span 2;
   }

   .gallery-item img {
     height: 100%;
     object-fit: cover;
     transition: transform .5s ease;
   }

   .gallery-item:hover img {
     transform: scale(1.06);
   }

   .gallery-caption {
     position: absolute;
     left: 18px;
     right: 18px;
     bottom: 16px;
     padding: 12px 15px;
     border-radius: 13px;
     background: rgba(0,0,0,.62);
     backdrop-filter: blur(10px);
     font-size: 13px;
   }

   .about-grid {
     display: grid;
     grid-template-columns: 1fr 1fr;
     gap: 70px;
     align-items: center;
   }

   .about-box {
     position: relative;
     min-height: 500px;
     border-radius: 30px;
     overflow: hidden;
     border: 1px solid var(--border);
     background: #151515;
   }

   .about-box img {
     height: 100%;
     object-fit: cover;
   }

   .about-box::after {
     content: "";
     position: absolute;
     inset: 0;
     background: linear-gradient(transparent 45%, rgba(0,0,0,.72));
   }

   .about-badge {
     position: absolute;
     z-index: 2;
     left: 25px;
     bottom: 25px;
     padding: 14px 18px;
     border-radius: 14px;
     background: rgba(0,0,0,.68);
     backdrop-filter: blur(10px);
     color: var(--gold-light);
     font-weight: 700;
   }

   .about-content .section-label {
     margin-bottom: 15px;
   }

   .about-content p {
     color: var(--muted);
     margin-bottom: 20px;
   }

   .check-list {
     list-style: none;
     margin: 30px 0;
     display: grid;
     gap: 12px;
   }

   .check-list li {
     display: flex;
     align-items: center;
     gap: 12px;
   }

   .check {
     width: 25px;
     height: 25px;
     display: grid;
     place-items: center;
     border-radius: 50%;
     background: rgba(215,173,98,.12);
     color: var(--gold);
     font-size: 13px;
   }

   .booking {
     background:
       radial-gradient(circle at 50% 0%, rgba(215,173,98,.12), transparent 35%),
       var(--bg-soft);
   }

   .booking-card {
     max-width: 900px;
     margin: auto;
     padding: 45px;
     background: #111;
     border: 1px solid var(--border);
     border-radius: 30px;
     box-shadow: 0 30px 100px rgba(0,0,0,.3);
   }

   .booking-form {
     display: grid;
     gap: 17px;
   }

   .form-grid {
     display: grid;
     grid-template-columns: 1fr 1fr;
     gap: 17px;
   }

   label {
     display: block;
     font-size: 13px;
     color: #c4c0b8;
     margin-bottom: 7px;
   }

   input,
   select,
   textarea {
     width: 100%;
     padding: 15px 16px;
     background: #080808;
     color: white;
     border: 1px solid var(--border);
     border-radius: 13px;
     outline: none;
   }

   input:focus,
   select:focus,
   textarea:focus {
     border-color: rgba(215,173,98,.65);
   }

   textarea {
     min-height: 110px;
     resize: vertical;
   }

   .booking-note {
     color: var(--muted);
     font-size: 13px;
     margin-top: 3px;
   }

   .booking-steps {
     display: grid;
     grid-template-columns: repeat(3, 1fr);
     gap: 12px;
     margin-bottom: 28px;
   }

   .booking-step {
     padding: 14px;
     border: 1px solid var(--border);
     border-radius: 14px;
     color: var(--muted);
     font-size: 13px;
     text-align: center;
   }

   .booking-step.active {
     color: var(--gold-light);
     border-color: rgba(215,173,98,.55);
     background: rgba(215,173,98,.08);
   }

   .date-picker,
   .time-picker {
     display: grid;
     grid-template-columns: repeat(4, 1fr);
     gap: 10px;
   }

   .choice-button {
     min-height: 62px;
     padding: 10px;
     border: 1px solid var(--border);
     border-radius: 14px;
     background: #080808;
     color: var(--text);
     cursor: pointer;
     transition: .2s;
   }

   .choice-button:hover,
   .choice-button.selected {
     border-color: var(--gold);
     background: rgba(215,173,98,.13);
     color: var(--gold-light);
   }

   .choice-button:disabled {
     opacity: .35;
     cursor: not-allowed;
     text-decoration: line-through;
   }

   .choice-day {
     display: block;
     color: var(--muted);
     font-size: 11px;
     text-transform: uppercase;
     letter-spacing: 1px;
   }

   .choice-date {
     display: block;
     font-size: 18px;
     font-weight: 700;
   }

   .time-button {
     min-height: 48px;
   }

   .selection-summary {
     display: none;
     padding: 18px;
     border: 1px solid rgba(215,173,98,.35);
     border-radius: 15px;
     background: rgba(215,173,98,.08);
     color: #e9dfc9;
   }

   .selection-summary.visible {
     display: block;
   }

   .selection-summary strong {
     color: var(--gold-light);
   }

   .booking-success {
     display: none;
     padding: 18px;
     border: 1px solid rgba(143,214,164,.35);
     border-radius: 15px;
     background: rgba(143,214,164,.08);
     color: var(--success);
   }

   .booking-success.visible {
     display: block;
   }

   .hours-grid {
     display: grid;
     grid-template-columns: 1fr 1fr;
     gap: 20px;
   }

   .hours-card,
   .contact-card {
     background: #111;
     border: 1px solid var(--border);
     border-radius: var(--radius);
     padding: 35px;
   }

   .hours-row {
     display: flex;
     justify-content: space-between;
     gap: 20px;
     padding: 14px 0;
     border-bottom: 1px solid var(--border);
   }

   .hours-row:last-child {
     border-bottom: 0;
   }

   .hours-row span:last-child {
     color: var(--gold-light);
     font-weight: 600;
   }

   .closed {
     color: #777 !important;
   }

   .contact-list {
     display: grid;
     gap: 18px;
     margin-top: 25px;
   }

   .contact-link {
     display: flex;
     gap: 14px;
     align-items: center;
     padding: 16px;
     background: rgba(255,255,255,.035);
     border-radius: 14px;
     transition: .2s;
   }

   .contact-link:hover {
     background: rgba(215,173,98,.09);
   }

   .contact-icon {
     width: 42px;
     height: 42px;
     display: grid;
     place-items: center;
     border-radius: 12px;
     background: rgba(215,173,98,.12);
   }

   .contact-link small {
     display: block;
     color: var(--muted);
     font-size: 11px;
   }

   .map {
     width: 100%;
     height: 400px;
     border: 0;
     filter: grayscale(1) contrast(1.1);
   }

   .faq {
     max-width: 850px;
     margin: auto;
   }

   details {
     border-bottom: 1px solid var(--border);
     padding: 22px 0;
   }

   summary {
     cursor: pointer;
     list-style: none;
     font-weight: 700;
     font-size: 17px;
   }

   summary::-webkit-details-marker {
     display: none;
   }

   details p {
     color: var(--muted);
     padding-top: 14px;
     max-width: 700px;
   }

   footer {
     padding: 55px 0 25px;
     border-top: 1px solid var(--border);
     background: #050505;
   }

   .footer-grid {
     display: grid;
     grid-template-columns: 2fr 1fr 1fr;
     gap: 50px;
     margin-bottom: 45px;
   }

   .footer-brand p {
     color: var(--muted);
     max-width: 380px;
     margin-top: 15px;
   }

   .footer-title {
     font-weight: 700;
     margin-bottom: 15px;
   }

   .footer-links {
     display: grid;
     gap: 10px;
     color: var(--muted);
     font-size: 14px;
   }

   .footer-links a:hover {
     color: var(--gold);
   }

   .copyright {
     border-top: 1px solid var(--border);
     padding-top: 22px;
     color: #68645d;
     font-size: 12px;
     display: flex;
     justify-content: space-between;
     gap: 20px;
   }

   @media (max-width: 800px) {
     .nav-links {
       display: none;
       position: absolute;
       left: 4%;
       right: 4%;
       top: 70px;
       padding: 20px;
       background: #111;
       border: 1px solid var(--border);
       border-radius: 18px;
       flex-direction: column;
       align-items: stretch;
     }

     .nav-links.active {
       display: flex;
     }

     .nav-book {
       text-align: center;
     }

     .menu-btn {
       display: block;
     }

     .trust-grid,
     .service-grid,
     .about-grid,
     .hours-grid,
     .footer-grid {
       grid-template-columns: 1fr;
     }

     .trust-item {
       border-right: 0;
       border-bottom: 1px solid var(--border);
     }

     .trust-item:last-child {
       border-bottom: 0;
     }

     .gallery-grid {
       grid-template-columns: 1fr 1fr;
       grid-template-rows: 220px 180px 180px;
     }

     .gallery-item:first-child {
       grid-column: span 2;
       grid-row: auto;
     }

     .about-box {
       min-height: 330px;
     }

     .form-grid {
       grid-template-columns: 1fr;
     }

     .booking-card {
       padding: 25px;
     }

     .booking-steps {
       grid-template-columns: 1fr;
     }

     .date-picker,
     .time-picker {
       grid-template-columns: repeat(2, 1fr);
     }

     .footer-grid {
       gap: 35px;
     }

     .copyright {
       flex-direction: column;
     }

     h1 {
       letter-spacing: -2px;
     }
   }
 </style>

</head>

<body>

<header id="header">
   <div class="container nav">
     <a href="#top" class="logo">
       ISAK <span>BARBER</span>
     </a>

<button class="menu-btn" id="menuBtn" aria-label="Åbn menu">
   ☰
 </button>

 <ul class="nav-links" id="navLinks">
   <li><a href="#services">Services</a></li>
   <li><a href="#gallery">Billeder</a></li>
   <li><a href="#about">Om os</a></li>
   <li><a href="#booking">Book</a></li>
   <li><a href="#hours">Åbningstider</a></li>
   <li><a href="#contact">Kontakt</a></li>
   <li><a href="#booking" class="nav-book">Book tid</a></li>
 </ul>
</div>
</header>

<main id="top">

<section class="hero">
 <div class="container hero-content">
   <div class="eyebrow">Barber i Solbjerg</div>

   <h1>
     ISAK
     <span>BARBER</span>
     SOLBJERG
   </h1>

   <p>
     Velkommen hos Isak Barber i Solbjerg.
      Vælg en ledig dato og tid,
     og send din booking direkte via SMS.
   </p>

   <div class="hero-buttons">
     <a href="#booking" class="btn btn-primary">
       ✂ Book din tid
     </a>

     <a href="#gallery" class="btn btn-secondary">
       📸 Se billeder
     </a>
   </div>
 </div>
</section>

<section class="trust">
 <div class="container trust-grid">
   <div class="trust-item">
     <div class="trust-number">4.7★</div>
     <div class="trust-label">Google-rating</div>
   </div>

   <div class="trust-item">
     <div class="trust-number">2018</div>
     <div class="trust-label">Etableret i Solbjerg</div>
   </div>

   <div class="trust-item">
     <div class="trust-number">8355</div>
     <div class="trust-label">Solbjerg</div>
   </div>
 </div>
</section>

<section class="services" id="services">
 <div class="container">
   <div class="section-head">
     <div class="section-label">Det vi laver</div>
     <h2>Din stil. Din tid.</h2>
     <p>
       En god barberoplevelse handler ikke kun om håret.
       Det handler om detaljerne, finishen og den gode følelse bagefter.
     </p>
   </div>

   <div class="service-grid">
     <article class="service">
       <div class="service-icon">✂️</div>
       <h3>Herreklip</h3>
       <p>
         En skarp og personlig klipning tilpasset dit ønskede look.
       </p>
     </article>

     <article class="service">
       <div class="service-icon">🪒</div>
       <h3>Skæg & barbering</h3>
       <p>
         Få styr på skægget og detaljerne omkring ansigtet.
       </p>
     </article>

     <article class="service">
       <div class="service-icon">💈</div>
       <h3>Styling</h3>
       <p>
         Finish og styling, så din frisure sidder rigtigt,
         når du forlader stolen.
       </p>
     </article>
   </div>
 </div>
</section>

<section class="gallery" id="gallery">
 <div class="container">
   <div class="section-head">
     <div class="section-label">Stemningen hos barbereren</div>
     <h2>Se stilen.</h2>
     <p>

     </p>
   </div>

   <div class="gallery-grid">
     <figure class="gallery-item">
       <img
         src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?auto=format&fit=crop&w=1200&q=85"
         alt="Barber arbejder med en klipning"
         loading="lazy"
       />
       <figcaption class="gallery-caption">
         Detaljer, finish og personlig stil
       </figcaption>
     </figure>

     <figure class="gallery-item">
       <img
         src="https://images.unsplash.com/photo-1503951914875-452162b0f3f1?auto=format&fit=crop&w=900&q=85"
         alt="Barberstol og barberudstyr"
         loading="lazy"
       />
       <figcaption class="gallery-caption">
         Klassisk barberstemning
       </figcaption>
     </figure>

     <figure class="gallery-item">
       <img
         src="https://images.unsplash.com/photo-1599351431202-1e0f0137899a?auto=format&fit=crop&w=900&q=85"
         alt="Professionelt barberudstyr"
         loading="lazy"
       />
       <figcaption class="gallery-caption">
         Skarpe værktøjer
       </figcaption>
     </figure>

     <figure class="gallery-item">
       <img
         src="https://images.unsplash.com/photo-1622286342621-4bd786c2447c?auto=format&fit=crop&w=900&q=85"
         alt="Mand med moderne frisure"
         loading="lazy"
       />
       <figcaption class="gallery-caption">
         Et look der passer til dig
       </figcaption>
     </figure>

     <figure class="gallery-item">
       <img
         src="https://images.unsplash.com/photo-1512690459411-b9245aed614b?auto=format&fit=crop&w=900&q=85"
         alt="Barber klipper hår"
         loading="lazy"
       />
       <figcaption class="gallery-caption">
         Fokus på detaljerne
       </figcaption>
     </figure>
   </div>
 </div>
</section>

<section id="about">
 <div class="container about-grid">
   <div class="about-box">
     <img
       src="https://images.unsplash.com/photo-1585747860715-2ba37e788b70?auto=format&fit=crop&w=1200&q=85"
       alt="Barber i en moderne barbershop"
       loading="lazy"
     />
     <div class="about-badge">
       Isak Barber · Solbjerg
     </div>
   </div>

   <div class="about-content">
     <div class="section-label">Isak Barber</div>

     <h2>
       Mere end bare en klipning.
     </h2>

     <p>
       Isak Barber er en lokal barbershop i Solbjerg,
       hvor fokus er på kunderne, den gode service og et
       resultat, du kan være tilfreds med.
     </p>

     <p>
       Virksomheden blev etableret i 2018 og drives af
       Abdul Hamid Mohammad Jammu.
     </p>

     <ul class="check-list">
       <li>
         <span class="check">✓</span>
         Lokal barber i Solbjerg
       </li>

       <li>
         <span class="check">✓</span>
         Personlig service
       </li>

       <li>
         <span class="check">✓</span>
         Valg af ledig dato og tidspunkt
       </li>

       <li>
         <span class="check">✓</span>
         Nem booking via SMS
       </li>
     </ul>

     <a href="#booking" class="btn btn-primary">
       Vælg en tid
     </a>
   </div>
 </div>
</section>

<section class="booking" id="booking">
 <div class="container">
   <div class="section-head">
     <div class="section-label">Booking</div>

     <h2>
       Book din tid 
     </h2>

     <p>
      
     </p>
   </div>

   <div class="booking-card">
     <div class="booking-steps">
       <div class="booking-step active" id="stepService">
         1. Behandling
       </div>

       <div class="booking-step" id="stepDate">
         2. Dato
       </div>

       <div class="booking-step" id="stepTime">
         3. Tidspunkt
       </div>
     </div>

     <form class="booking-form" id="bookingForm">
       <div class="form-grid">
         <div>
           <label for="name">Navn</label>
           <input
             id="name"
             type="text"
             placeholder="Dit navn"
             required
           />
         </div>

         <div>
           <label for="phone">Telefonnummer</label>
           <input
             id="phone"
             type="tel"
             placeholder="Dit telefonnummer"
             required
           />
         </div>
       </div>

       <div>
         <label for="service">
           1. Vælg behandling
         </label>

         <select id="service" required>
           <option value="">Vælg behandling</option>
           <option value="Herreklip">Herreklip</option>
           <option value="Skæg / barbering">Skæg / barbering</option>
           <option value="Herreklip + skæg">Herreklip + skæg</option>
           <option value="Andet">Andet</option>
         </select>
       </div>

       <div>
         <label>
           2. Vælg en ledig dato
         </label>

         <div
           class="date-picker"
           id="datePicker"
           aria-label="Ledige datoer"
         ></div>

         <input
           id="selectedDate"
           type="hidden"
           required
         />
       </div>

       <div>
         <label>
           3. Vælg et ledigt tidspunkt
         </label>

         <div
           class="time-picker"
           id="timePicker"
           aria-label="Ledige tidspunkter"
         >
           <button
             class="choice-button time-button"
             type="button"
             disabled
           >
             Vælg først en dato
           </button>
         </div>

         <input
           id="selectedTime"
           type="hidden"
           required
         />
       </div>

       <div class="selection-summary" id="selectionSummary">
         Din valgte tid:
         <strong id="summaryText"></strong>
       </div>

       <div>
         <label for="message">
           Ekstra besked
         </label>

         <textarea
           id="message"
           placeholder="Fx: Jeg vil gerne have en fade..."
         ></textarea>
       </div>

       <button class="btn btn-primary" type="submit">
         📱 Send booking via SMS
       </button>

       <div class="booking-success" id="bookingSuccess">
         Din SMS åbnes nu. Tryk på send i din SMS-app for at sende
         bookingforespørgslen til Isak Barber.
       </div>

       <p class="booking-note">
         Bemærk: Dette er en bookingforespørgsel via SMS.
         Tiden er først endeligt bekræftet, når Isak Barber svarer.
       </p>
     </form>
   </div>
 </div>
</section>

<section id="hours">
 <div class="container">
   <div class="section-head">
     <div class="section-label">Find os</div>
     <h2>Åbent for dig.</h2>
   </div>

   <div class="hours-grid">
     <div class="hours-card">
       <h3 style="font-family:'Playfair Display',serif;font-size:28px;margin-bottom:20px;">
         Åbningstider
       </h3>

       <div class="hours-row">
         <span>Mandag</span>
         <span>10:00 – 18:00</span>
       </div>

       <div class="hours-row">
         <span>Tirsdag</span>
         <span>10:00 – 18:00</span>
       </div>

       <div class="hours-row">
         <span>Onsdag</span>
         <span>12:00 – 18:00</span>
       </div>

       <div class="hours-row">
         <span>Torsdag</span>
         <span>10:00 – 18:00</span>
       </div>

       <div class="hours-row">
         <span>Fredag</span>
         <span>10:00 – 18:00</span>
       </div>

       <div class="hours-row">
         <span>Lørdag</span>
         <span>10:00 – 15:00</span>
       </div>

       <div class="hours-row">
         <span>Søndag</span>
         <span class="closed">Lukket</span>
       </div>
     </div>

     <div class="contact-card" id="contact">
       <h3 style="font-family:'Playfair Display',serif;font-size:28px;">
         Kontakt
       </h3>

       <div class="contact-list">
         <a class="contact-link" href="tel:+4520756530">
           <span class="contact-icon">☎</span>
           <span>
             <small>Telefon</small>
             20 75 65 30
           </span>
         </a>

         <a class="contact-link" href="sms:+4520756530">
           <span class="contact-icon">💬</span>
           <span>
             <small>SMS</small>
             Send en besked
           </span>
         </a>

         <a
           class="contact-link"
           href="https://www.facebook.com/"
           target="_blank"
           rel="noopener"
         >
           <span class="contact-icon">f</span>
           <span>
             <small>Facebook</small>
             Find Isak Barber på Facebook
           </span>
         </a>

         <div class="contact-link">
           <span class="contact-icon">📍</span>
           <span>
             <small>Adresse</small>
             Solbjerg Hedevej 4C<br />
             8355 Solbjerg
           </span>
         </div>
       </div>
     </div>
   </div>
 </div>
</section>

<section style="padding-top:0;">
 <div class="container">
   <iframe
     class="map"
     src="https://www.google.com/maps?q=Solbjerg%20Hedevej%204C,%208355%20Solbjerg&output=embed"
     loading="lazy"
     referrerpolicy="no-referrer-when-downgrade"
     title="Isak Barber på kort"
   ></iframe>
 </div>
</section>

<section>
 <div class="container">
   <div class="section-head">
     <div class="section-label">FAQ</div>
     <h2>Ofte stillede spørgsmål.</h2>
   </div>

   <div class="faq">
     <details>
       <summary>
         Hvordan vælger jeg en tid?
       </summary>

       <p>
         Vælg først en behandling. Derefter vises klikbare datoer
         og ledige tidspunkter. Når du har valgt begge dele,
         udfylder du navn og telefonnummer og sender bookingforespørgslen
         via SMS.
       </p>
     </details>

     <details>
       <summary>
         Er tiden automatisk reserveret?
       </summary>

       <p>
         Nej. Hjemmesiden åbner en SMS med dine oplysninger.
         Isak Barber skal svare og bekræfte tiden, før bookingen
         er endelig.
       </p>
     </details>

     <details>
       <summary>
         Hvor ligger Isak Barber?
       </summary>

       <p>
         Isak Barber ligger på Solbjerg Hedevej 4C,
         8355 Solbjerg.
       </p>
     </details>

     <details>
       <summary>
         Kan åbningstiderne ændre sig?
       </summary>

       <p>
         Ja. Åbningstider kan ændre sig ved ferie, helligdage
         eller særlige lukkedage. Tjek derfor altid den seneste
         besked fra barberen.
       </p>
     </details>
   </div>
 </div>
</section>
</main>

<footer>
   <div class="container">
     <div class="footer-grid">
       <div class="footer-brand">
         <div class="logo">
           ISAK <span>BARBER</span>
         </div>

    <p>
       Barber i Solbjerg.
       Skarpe klipninger, god service og personlig stil.
     </p>
   </div>

   <div>
     <div class="footer-title">Genveje</div>

     <div class="footer-links">
       <a href="#services">Services</a>
       <a href="#gallery">Billeder</a>
       <a href="#about">Om os</a>
       <a href="#booking">Book tid</a>
       <a href="#hours">Åbningstider</a>
     </div>
   </div>

   <div>
     <div class="footer-title">Kontakt</div>

     <div class="footer-links">
       <a href="tel:+4520756530">
         20 75 65 30
       </a>

       <a href="sms:+4520756530">
         Send SMS
       </a>

       <a
         href="https://www.google.com/maps/search/?api=1&query=Solbjerg%20Hedevej%204C%208355%20Solbjerg"
         target="_blank"
         rel="noopener"
       >
         Find vej
       </a>
     </div>
   </div>
 </div>

 <div class="copyright">
   <span>
     © <span id="year"></span> Isak Barber
   </span>

   <span>
     Solbjerg Hedevej 4C · 8355 Solbjerg
   </span>
 </div>
</div>
</footer>

<script>
   const menuBtn = document.getElementById("menuBtn");
   const navLinks = document.getElementById("navLinks");

   menuBtn.addEventListener("click", () => {
     navLinks.classList.toggle("active");
   });

   document.querySelectorAll(".nav-links a").forEach(link => {
     link.addEventListener("click", () => {
       navLinks.classList.remove("active");
     });
   });

   const header = document.getElementById("header");

   window.addEventListener("scroll", () => {
     header.classList.toggle("scrolled", window.scrollY > 20);
   });

   document.getElementById("year").textContent =
     new Date().getFullYear();

   const bookingForm = document.getElementById("bookingForm");
   const serviceInput = document.getElementById("service");
   const datePicker = document.getElementById("datePicker");
   const timePicker = document.getElementById("timePicker");
   const selectedDateInput = document.getElementById("selectedDate");
   const selectedTimeInput = document.getElementById("selectedTime");
   const selectionSummary = document.getElementById("selectionSummary");
   const summaryText = document.getElementById("summaryText");
   const bookingSuccess = document.getElementById("bookingSuccess");

   const stepService = document.getElementById("stepService");
   const stepDate = document.getElementById("stepDate");
   const stepTime = document.getElementById("stepTime");

   const openingHours = {
     0: null,
     1: ["10:00", "18:00"],
     2: ["10:00", "18:00"],
     3: ["12:00", "18:00"],
     4: ["10:00", "18:00"],
     5: ["10:00", "18:00"],
     6: ["10:00", "15:00"]
   };

   const unavailableSlots = {
     /*
       Eksempel på tider, der kan fjernes fra listen:

       "2025-12-24": ["10:00", "10:30", "11:00"]

       Dette er kun en frontend-demo.
       En rigtig bookingløsning skal hente optagede tider
       fra en database eller et bookingsystem.
     */
   };

   let selectedDateLabel = "";
   let selectedTimeLabel = "";

   function pad(number) {
     return String(number).padStart(2, "0");
   }

   function formatDateKey(date) {
     return [
       date.getFullYear(),
       pad(date.getMonth() + 1),
       pad(date.getDate())
     ].join("-");
   }

   function formatDateLabel(date) {
     return date.toLocaleDateString("da-DK", {
       weekday: "short",
       day: "numeric",
       month: "short"
     });
   }

   function createDateOptions() {
     datePicker.innerHTML = "";

     const today = new Date();
     today.setHours(12, 0, 0, 0);

     let createdDates = 0;
     let daysChecked = 0;

     while (createdDates < 14 && daysChecked < 45) {
       const date = new Date(today);
       date.setDate(today.getDate() + daysChecked);

       const dayOfWeek = date.getDay();
       const hours = openingHours[dayOfWeek];
       const dateKey = formatDateKey(date);

       if (hours && !unavailableSlots[dateKey]?.allDay) {
         const button = document.createElement("button");
         button.type = "button";
         button.className = "choice-button";
         button.dataset.date = dateKey;
         button.dataset.label = formatDateLabel(date);

         button.innerHTML = `
           <span class="choice-day">${date.toLocaleDateString("da-DK", {
             weekday: "short"
           })}</span>
           <span class="choice-date">${date.getDate()}/${date.getMonth() + 1}</span>
         `;

         button.addEventListener("click", () => {
           document
             .querySelectorAll("#datePicker .choice-button")
             .forEach(item => item.classList.remove("selected"));

           button.classList.add("selected");
           selectedDateInput.value = dateKey;
           selectedDateLabel = button.dataset.label;

           stepDate.classList.add("active");
           stepTime.classList.add("active");

           createTimeOptions(dateKey, hours);
           updateSummary();
         });

         datePicker.appendChild(button);
         createdDates++;
       }

       daysChecked++;
     }
   }

   function createTimeOptions(dateKey, hours) {
     timePicker.innerHTML = "";

     const [openingHour, closingHour] = hours;
     const startMinutes = convertTimeToMinutes(openingHour);
     const endMinutes = convertTimeToMinutes(closingHour);
     const unavailable = unavailableSlots[dateKey] || {};
     let availableCount = 0;

     for (
       let minutes = startMinutes;
       minutes < endMinutes;
       minutes += 30
     ) {
       const time = convertMinutesToTime(minutes);

       if (Array.isArray(unavailable) && unavailable.includes(time)) {
         continue;
       }

       const button = document.createElement("button");
       button.type = "button";
       button.className = "choice-button time-button";
       button.textContent = time;
       button.dataset.time = time;

       button.addEventListener("click", () => {
         document
           .querySelectorAll("#timePicker .choice-button")
           .forEach(item => item.classList.remove("selected"));

         button.classList.add("selected");
         selectedTimeInput.value = time;
         selectedTimeLabel = time;
         updateSummary();
       });

       timePicker.appendChild(button);
       availableCount++;
     }

     if (!availableCount) {
       const emptyMessage = document.createElement("p");
       emptyMessage.className = "booking-note";
       emptyMessage.textContent =
         "Der er ingen ledige tider denne dag. Vælg venligst en anden dato.";
       timePicker.appendChild(emptyMessage);
     }
   }

   function convertTimeToMinutes(time) {
     const [hours, minutes] = time.split(":").map(Number);
     return hours * 60 + minutes;
   }

   function convertMinutesToTime(minutes) {
     const hours = Math.floor(minutes / 60);
     const remainingMinutes = minutes % 60;
     return `${pad(hours)}:${pad(remainingMinutes)}`;
   }

   function updateSummary() {
     if (selectedDateInput.value && selectedTimeInput.value) {
       selectionSummary.classList.add("visible");
       summaryText.textContent =
         `${selectedDateLabel} kl. ${selectedTimeLabel}`;
     } else {
       selectionSummary.classList.remove("visible");
     }
   }

   serviceInput.addEventListener("change", () => {
     if (serviceInput.value) {
       stepService.classList.add("active");
     } else {
       stepService.classList.remove("active");
     }
   });

   bookingForm.addEventListener("submit", event => {
     event.preventDefault();

     if (
       !serviceInput.value ||
       !selectedDateInput.value ||
       !selectedTimeInput.value
     ) {
       alert("Vælg behandling, dato og tidspunkt først.");
       return;
     }

     const name = document.getElementById("name").value.trim();
     const phone = document.getElementById("phone").value.trim();
     const message = document.getElementById("message").value.trim();

     const formattedDate = new Date(
       `${selectedDateInput.value}T12:00:00`
     ).toLocaleDateString("da-DK");

     const smsText =
`Hej Isak Barber 👋

Jeg vil gerne booke en tid.

Navn: ${name}
Telefon: ${phone}
Dato: ${formattedDate}
Tid: ${selectedTimeInput.value}
Behandling: ${serviceInput.value}

${message ? "Besked: " + message : ""}

Mvh ${name}`;

     const smsUrl =
       "sms:+4520756530?body=" +
       encodeURIComponent(smsText);

     bookingSuccess.classList.add("visible");
     window.location.href = smsUrl;
   });

   createDateOptions();
 </script>

</body>
</html>






