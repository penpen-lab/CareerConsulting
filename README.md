
<html lang="zh-TW">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>職涯諮詢三二事</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+TC:wght@300;400;600;700;900&family=Playfair+Display:ital,wght@0,700;1,400&family=DM+Mono:wght@300;400&display=swap" rel="stylesheet" />
  <style>
    :root {
      --ink: #1a1208;
      --paper: #f5f0e8;
      --cream: #ede7d3;
      --gold: #c4922a;
      --gold-light: #e8c06a;
      --sage: #6b7c5e;
      --muted: #7a6f5e;
      --card-bg: #faf7f0;
      --fs-xs:   0.75rem;
      --fs-sm:   0.875rem;
      --fs-base: 1rem;
      --fs-md:   1.0625rem;
      --fs-lg:   1.25rem;
      --fs-xl:   1.5rem;
    }
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; -webkit-text-size-adjust: 100%; }
    body {
      font-family: 'Noto Serif TC', serif;
      background: var(--paper);
      color: var(--ink);
      overflow-x: hidden;
      font-size: var(--fs-base);
    }
    body::before {
      content: '';
      position: fixed; inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
      pointer-events: none; z-index: 999; opacity: .45;
    }
    /* ── NAV ── */
    nav { display: none; }

    /* ── HERO DECORATION ── */
    .hero-deco {
      position: absolute;
      inset: 0;
      pointer-events: none;
      overflow: hidden;
      z-index: 0;
    }
    .hero-deco svg {
      position: absolute;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      display: block;
    }
    /* push hero content above decoration */
    .hero-eyebrow,
    .hero-title,
    .hero-sub,
    .hero-cta {
      position: relative;
      z-index: 1;
    }
    /* ── HERO ── */
    .hero {
      display: flex; flex-direction: column; justify-content: flex-start; align-items: center;
      text-align: center; padding: 0 24px 5mm; position: relative;
      min-height: 100svh;
      background:
        radial-gradient(ellipse 70% 50% at 20% 80%, rgba(196,146,42,.12) 0%, transparent 60%),
        radial-gradient(ellipse 50% 60% at 80% 20%, rgba(107,124,94,.1) 0%, transparent 55%),
        var(--paper);
    }
    .hero-eyebrow {
      font-family: 'DM Mono', monospace; font-size: clamp(0.85rem, 2.8vw, 0.95rem);
      letter-spacing: .18em; color: var(--gold); text-transform: uppercase;
      margin-top: 10mm; margin-bottom: 5mm;
      opacity: 0; animation: fadeUp .8s .2s ease forwards;
    }
    .hero-title {
      font-weight: 900; font-size: clamp(4rem, 30vw, 3.75rem);
      line-height: 1.05; letter-spacing: -.02em;
      opacity: 0; animation: fadeUp .9s .4s ease forwards;
    }
    .hero-title span.accent { color: var(--gold); font-style: italic; }
    .hero-title .underline-deco { display: block; position: relative; }

    .hero-title .underline-deco::after {
      content: ''; position: absolute; left: 0; right: 0; bottom: -4px;
      height: 3px; background: linear-gradient(90deg, var(--gold), var(--gold-light), transparent);
      border-radius: 2px;
    }
    .hero-sub {
      margin-top: 28px; max-width: 480px;
      font-size: clamp(var(--fs-base), 2.2vw, 1.05rem);
      line-height: 1.9; color: var(--muted); font-weight: 300;
      opacity: 0; animation: fadeUp .8s .65s ease forwards;
    }
    .hero-cta {
      display: flex; gap: 12px; flex-wrap: wrap; justify-content: center;
      margin-top: 40px; opacity: 0; animation: fadeUp .8s .85s ease forwards;
    }
    .btn-primary {
      background: var(--ink); color: var(--paper); border: none;
      padding: 15px 36px;
      font-family: 'Noto Serif TC', serif; font-size: var(--fs-base); font-weight: 600;
      letter-spacing: .04em; cursor: pointer; transition: all .3s; position: relative; overflow: hidden;
    }
    .btn-primary::after {
      content: ''; position: absolute; inset: 0; background: var(--gold);
      transform: scaleX(0); transform-origin: left; transition: transform .35s ease; z-index: 0;
    }
    .btn-primary:hover::after { transform: scaleX(1); }
    .btn-primary span { position: relative; z-index: 1; }
    .btn-primary:hover { color: var(--ink); }
    .btn-outline {
      background: transparent; color: var(--ink); border: 1.5px solid var(--ink);
      padding: 15px 36px;
      font-family: 'Noto Serif TC', serif; font-size: var(--fs-base); font-weight: 400;
      letter-spacing: .04em; cursor: pointer; transition: all .3s;
    }
    .btn-outline:hover { background: var(--cream); }
    /* ── SECTIONS ── */
    section { padding: 48px clamp(20px, 7vw, 100px); }
    .section-label { font-family: 'DM Mono', monospace; font-size: var(--fs-xs); letter-spacing: .28em; text-transform: uppercase; color: var(--sage); margin-bottom: 14px; }
    .section-heading { font-size: clamp(var(--fs-xl), 4vw, 3rem); font-weight: 700; line-height: 1.2; margin-bottom: 18px; }
    .section-desc { font-size: var(--fs-base); line-height: 1.9; color: var(--muted); max-width: 540px; font-weight: 300; }
    /* ── ABOUT ── */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 48px;
      align-items: start;
    }
    .about-visual { position: relative; }
    /* ── NEW VISUAL BLOCK (replaces 諮 placeholder) ── */
    .about-photo-placeholder {
      width: 100%; aspect-ratio: 4/4;
      position: relative; overflow: hidden;
      background: var(--cream);
    }
    /* Bottom-left ink rectangle */
    .about-photo-placeholder::before {
      content: '';
      position: absolute;
      bottom: 0; left: 0;
      width: 60%; height: 55%;
      background: var(--ink);
      clip-path: polygon(0 18%, 100% 0, 100% 100%, 0 100%);
    }
    /* Top-right gold rectangle */
    .about-photo-placeholder::after {
      content: '';
      position: absolute;
      top: 0; right: 0;
      width: 62%; height: 58%;
      background: linear-gradient(135deg, var(--gold-light) 0%, var(--gold) 100%);
      clip-path: polygon(0 0, 100% 0, 100% 82%, 0 100%);
    }
    /* SVG overlay: decorative lines + dot grid */
    .visual-svg-overlay {
      position: absolute; inset: 0;
      width: 100%; height: 100%;
      z-index: 2; pointer-events: none;
    }
    /* Stat block: 9+ above YEARS EXP. near bottom-right of black geometry */
    .visual-stat {
      position: absolute;
      bottom: 3%;
      right: 40%;
      z-index: 3;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      gap: 0;
    }
    /* 9 and + in a row, bottom-aligned, then YEARS EXP below */
    .vs-num-wrap {
      display: inline-flex;
      flex-direction: row;
      align-items: flex-end;
      line-height: 1;
      gap: 0.04em;
      margin-bottom: 4mm;
    }
    /* 9 — big italic */
    .visual-stat .vs-num {
      font-family: 'Playfair Display', serif;
      font-style: italic;
      font-size: clamp(5rem, 14vw, 8.5rem);
      font-weight: 700;
      color: var(--paper);
      line-height: 1;
      text-shadow: 0 2px 24px rgba(26,18,8,.35);
    }
    /* + — bigger than YEARS EXP label, bold, sits beside 9 */
    .visual-stat .vs-suffix {
      font-family: 'Playfair Display', serif;
      font-style: normal;
      font-weight: 700;
      font-size: clamp(2rem, 5vw, 3rem);
      color: var(--paper);
      text-shadow: 0 2px 16px rgba(26,18,8,.35), 0 0 1px var(--paper), 0 0 2px var(--paper);
      -webkit-text-stroke: 0.06em var(--paper);
      line-height: 1;
      margin-bottom: 0;
    }
    /* YEARS EXP. — small mono label below 9+ */
    .visual-stat .vs-label {
      font-family: 'DM Mono', monospace;
      font-size: .62rem;
      letter-spacing: .22em;
      color: rgba(245,240,232,.7);
      text-transform: uppercase;
      display: block;
    }
    .about-content { padding-left: 0; padding-top: 4px; }
    .about-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 24px; }
    .tag { border: 1px solid var(--cream); padding: 6px 14px; font-size: var(--fs-sm); color: var(--muted); background: var(--card-bg); font-family: 'DM Mono', monospace; letter-spacing: .05em; transition: all .25s; }
    .tag:hover { border-color: var(--gold); color: var(--gold); }
    /* ── SERVICES ── */
    .services-header { display: flex; justify-content: space-between; align-items: flex-end; margin-bottom: 20px; flex-wrap: wrap; gap: 12px; }
    .services-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 2px; }
    .service-card {
      background: var(--card-bg); padding: 24px 24px 20px; position: relative; overflow: hidden;
      cursor: pointer; transition: background .3s; border: 1px solid var(--cream);
    }
    .service-card::before { content: ''; position: absolute; top: 0; left: 0; width: 3px; height: 0; background: var(--gold); transition: height .4s; }
    .service-card:hover::before { height: 100%; }
    .service-card:hover { background: #fff; }
    .card-number { font-family: 'Playfair Display', serif; font-style: italic; font-size: 2rem; color: var(--cream); line-height: 1; margin-bottom: 10px; transition: color .3s; }
    .service-card:hover .card-number { color: var(--gold-light); }
    .card-title { font-size: var(--fs-lg); font-weight: 700; margin-bottom: 12px; }
    .card-desc { font-size: var(--fs-sm); line-height: 1.85; color: var(--muted); font-weight: 300; }
    .card-arrow { display: inline-flex; align-items: center; gap: 8px; margin-top: 14px; font-family: 'DM Mono', monospace; font-size: var(--fs-xs); letter-spacing: .1em; color: var(--gold); opacity: 0; transform: translateX(-8px); transition: all .3s; }
    .service-card:hover .card-arrow { opacity: 1; transform: translateX(0); }
    /* ── FAQ ── */
    .faq-list { margin-top: 40px; max-width: 760px; }
    .faq-item { border-top: 1px solid var(--cream); }
    .faq-item:last-child { border-bottom: 1px solid var(--cream); }
    .faq-question {
      width: 100%; background: none; border: none; display: flex; justify-content: space-between; align-items: center;
      padding: 22px 0; font-family: 'Noto Serif TC', serif;
      font-size: var(--fs-base); font-weight: 600; color: var(--ink); cursor: pointer; text-align: left; gap: 16px;
    }
    .faq-icon { width: 28px; height: 28px; border: 1.5px solid var(--ink); display: flex; align-items: center; justify-content: center; flex-shrink: 0; font-size: 1.1rem; transition: all .3s; color: var(--ink); }
    .faq-item.open .faq-icon { background: var(--ink); color: var(--paper); transform: rotate(45deg); }
    .faq-answer { max-height: 0; overflow: hidden; transition: max-height .4s ease, padding .3s; }
    .faq-item.open .faq-answer { max-height: 300px; padding-bottom: 22px; }
    .faq-answer p { font-size: var(--fs-base); line-height: 1.9; color: var(--muted); font-weight: 300; }
    /* ── CTA BAND ── */
    .cta-band {
      background: linear-gradient(135deg, var(--ink) 0%, #2a1f0a 100%);
      color: var(--paper); text-align: center; padding: 64px clamp(20px, 7vw, 100px);
      position: relative; overflow: hidden;
    }
    .cta-band::before { content: '職'; position: absolute; font-size: 26rem; font-weight: 900; color: rgba(196,146,42,.04); top: 50%; left: 50%; transform: translate(-50%,-50%); line-height: 1; pointer-events: none; }
    .cta-band h2 { font-size: clamp(var(--fs-xl), 5vw, 4rem); font-weight: 700; margin-bottom: 16px; position: relative; }
    .cta-band p { color: rgba(245,240,232,.6); font-size: var(--fs-base); font-weight: 300; margin-bottom: 44px; max-width: 460px; margin-left: auto; margin-right: auto; line-height: 1.9; position: relative; }
    .btn-gold { background: var(--gold); color: var(--ink); border: none; padding: 17px 48px; font-family: 'Noto Serif TC', serif; font-size: var(--fs-base); font-weight: 700; letter-spacing: .05em; cursor: pointer; transition: all .3s; }
    .btn-gold:hover { background: var(--gold-light); transform: translateY(-2px); box-shadow: 0 12px 40px rgba(196,146,42,.3); }
    /* ── FOOTER ── */
    footer {
      padding: 32px clamp(20px, 7vw, 120px);
      display: flex; align-items: baseline; justify-content: space-between;
      flex-wrap: wrap; gap: 12px 24px;
      border-top: 1px solid var(--cream);
    }
    .footer-logo { font-size: var(--fs-sm); font-weight: 700; font-family: 'DM Mono', monospace; letter-spacing: .06em; color: var(--muted); }
    .footer-logo span { color: var(--gold); }
    .footer-links { display: flex; gap: 24px; list-style: none; align-items: baseline; }
    .footer-links a {
      text-decoration: none; font-family: 'DM Mono', monospace;
      font-size: var(--fs-xs); letter-spacing: .1em; color: var(--muted);
      text-transform: uppercase; transition: color .25s;
    }
    .footer-links a:hover { color: var(--gold); }
    .footer-copy { font-family: 'DM Mono', monospace; font-size: var(--fs-xs); color: var(--muted); letter-spacing: .06em; }
    /* ── ANIMATIONS ── */
    @keyframes fadeUp { from { opacity:0; transform:translateY(24px); } to { opacity:1; transform:translateY(0); } }
    .reveal { opacity:0; transform:translateY(28px); transition:opacity .7s ease,transform .7s ease; }
    .reveal.visible { opacity:1; transform:translateY(0); }
    .reveal-delay-1 { transition-delay:.1s; }
    .reveal-delay-2 { transition-delay:.2s; }
    .reveal-delay-3 { transition-delay:.3s; }
    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      .about-grid { grid-template-columns: 1fr; gap: 28px; }
      .services-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

<script>
  /* ═══════════════════════════════════════════════
     ★  修改這裡就能改圖內的數字文字  ★
     ═══════════════════════════════════════════════ */
  const VISUAL_CONFIG = {
    number: "9+",          // 圖中大數字（如 "9+"、"10+"、"15"）
    label:  "YEARS EXP.",  // 數字下方小標籤
  };
  /* ═══════════════════════════════════════════════ */
</script>

<!-- NAV -->
<nav id="nav">
  <ul class="nav-links">
    <li><a href="#about">關於我</a></li>
    <li><a href="#services">服務項目</a></li>
    <li><a href="#faq">常見問題</a></li>
  </ul>
</nav>
<!-- HERO -->
<section class="hero" id="home">

  <!-- Geometric background decoration -->
  <div class="hero-deco">
    <svg viewBox="0 0 1200 700" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice">
      <!-- Large ink triangle — top-left -->
      <polygon points="0,0 320,0 0,280" fill="rgba(26,18,8,0.06)"/>
      <polygon points="0,0 380,0 0,340" fill="none" stroke="rgba(26,18,8,0.08)" stroke-width="1"/>

      <!-- Gold diagonal band — upper right -->
      <polygon points="900,0 1200,0 1200,220 1060,0" fill="rgba(196,146,42,0.07)"/>
      <polygon points="840,0 1200,0 1200,280 980,0" fill="none" stroke="rgba(196,146,42,0.15)" stroke-width="1"/>

      <!-- Bottom-right ink block -->
      <polygon points="1200,700 900,700 1200,420" fill="rgba(26,18,8,0.05)"/>

      <!-- Dot grid — left side -->
      <g fill="rgba(196,146,42,0.22)">
        <circle cx="48"  cy="120" r="3.5"/><circle cx="80"  cy="120" r="3.5"/><circle cx="112" cy="120" r="3.5"/>
        <circle cx="48"  cy="152" r="3.5"/><circle cx="80"  cy="152" r="3.5"/><circle cx="112" cy="152" r="3.5"/>
        <circle cx="48"  cy="184" r="3.5"/><circle cx="80"  cy="184" r="3.5"/><circle cx="112" cy="184" r="3.5"/>
        <circle cx="48"  cy="216" r="3.5"/><circle cx="80"  cy="216" r="3.5"/><circle cx="112" cy="216" r="3.5"/>
      </g>

      <!-- Dot grid — right side -->
      <g fill="rgba(196,146,42,0.22)">
        <circle cx="1088" cy="400" r="3.5"/><circle cx="1120" cy="400" r="3.5"/><circle cx="1152" cy="400" r="3.5"/>
        <circle cx="1088" cy="432" r="3.5"/><circle cx="1120" cy="432" r="3.5"/><circle cx="1152" cy="432" r="3.5"/>
        <circle cx="1088" cy="464" r="3.5"/><circle cx="1120" cy="464" r="3.5"/><circle cx="1152" cy="464" r="3.5"/>
      </g>

      <!-- Vertical / horizontal rule lines -->
      <line x1="60"   y1="0"   x2="60"   y2="220"  stroke="rgba(196,146,42,0.12)" stroke-width="1"/>
      <line x1="1140" y1="0"   x2="1140" y2="200"  stroke="rgba(196,146,42,0.12)" stroke-width="1"/>
      <line x1="0"    y1="650" x2="500"  y2="650"  stroke="rgba(196,146,42,0.12)" stroke-width="1"/>

      <!-- Corner bracket marks — top left -->
      <line x1="30" y1="30" x2="80"  y2="30"  stroke="rgba(196,146,42,0.45)" stroke-width="2"/>
      <line x1="30" y1="30" x2="30"  y2="80"  stroke="rgba(196,146,42,0.45)" stroke-width="2"/>
      <!-- Corner bracket marks — top right -->
      <line x1="1170" y1="30" x2="1120" y2="30"  stroke="rgba(196,146,42,0.45)" stroke-width="2"/>
      <line x1="1170" y1="30" x2="1170" y2="80"  stroke="rgba(196,146,42,0.45)" stroke-width="2"/>
      <!-- Corner bracket marks — bottom left -->
      <line x1="30" y1="670" x2="80"  y2="670" stroke="rgba(196,146,42,0.45)" stroke-width="2"/>
      <line x1="30" y1="670" x2="30"  y2="620" stroke="rgba(196,146,42,0.45)" stroke-width="2"/>
      <!-- Corner bracket marks — bottom right -->
      <line x1="1170" y1="670" x2="1120" y2="670" stroke="rgba(196,146,42,0.45)" stroke-width="2"/>
      <line x1="1170" y1="670" x2="1170" y2="620" stroke="rgba(196,146,42,0.45)" stroke-width="2"/>

      <!-- Cross mark — left centre -->
      <line x1="28" y1="350" x2="52"  y2="350" stroke="rgba(196,146,42,0.4)" stroke-width="1.5"/>
      <line x1="40" y1="338" x2="40"  y2="362" stroke="rgba(196,146,42,0.4)" stroke-width="1.5"/>
      <!-- Cross mark — right centre -->
      <line x1="1148" y1="350" x2="1172" y2="350" stroke="rgba(196,146,42,0.4)" stroke-width="1.5"/>
      <line x1="1160" y1="338" x2="1160" y2="362" stroke="rgba(196,146,42,0.4)" stroke-width="1.5"/>

      <!-- Bottom centre rule -->
      <line x1="480" y1="690" x2="720" y2="690" stroke="rgba(196,146,42,0.2)" stroke-width="1"/>
    </svg>
  </div>

  <p class="hero-eyebrow">Career Consulting · 職涯諮詢</p>
  <h1 class="hero-title">
    <span class="underline-deco">職涯諮詢</span>
    <span class="accent">三二事</span>
  </h1>
  <p class="hero-sub">
    在每一個職涯的岔路口<br>
    你不必獨自面對<br>
    有時是迷惘 不知道下一步該往哪裡走<br>
    有時是卡關 明明很努力卻看不見出口<br>
    有時可能只是想停下來 好好思考方向<br>
    讓我們一起慢慢梳理<br>
    看見那些被忽略的能力與可能<br>
    職涯不只是找到一份工作<br>
    更是走向<br>更理解自己的旅程<br>
  </p>
  <div class="hero-cta">
    <button class="btn-primary" onclick="document.getElementById('services').scrollIntoView({behavior:'smooth'})">
      <span>探索內容</span>
    </button>
    <button class="btn-outline" onclick="document.getElementById('about').scrollIntoView({behavior:'smooth'})">
      認識我們
    </button>
  </div>
</section>
<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-visual reveal">
      <!-- New geometric visual replacing the 諮 character -->
      <div class="about-photo-placeholder">
        <!-- SVG decorative layer -->
        <svg class="visual-svg-overlay" viewBox="0 0 400 400" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
          <!-- Dot grid (top-left area) -->
          <g fill="rgba(196,146,42,0.25)">
            <circle cx="32" cy="32" r="2.5"/>
            <circle cx="56" cy="32" r="2.5"/>
            <circle cx="80" cy="32" r="2.5"/>
            <circle cx="104" cy="32" r="2.5"/>
            <circle cx="32" cy="56" r="2.5"/>
            <circle cx="56" cy="56" r="2.5"/>
            <circle cx="80" cy="56" r="2.5"/>
            <circle cx="104" cy="56" r="2.5"/>
            <circle cx="32" cy="80" r="2.5"/>
            <circle cx="56" cy="80" r="2.5"/>
            <circle cx="80" cy="80" r="2.5"/>
            <circle cx="104" cy="80" r="2.5"/>
            <circle cx="32" cy="104" r="2.5"/>
            <circle cx="56" cy="104" r="2.5"/>
            <circle cx="80" cy="104" r="2.5"/>
            <circle cx="104" cy="104" r="2.5"/>
          </g>
          <!-- Diagonal rule line across whole block -->
          <line x1="0" y1="400" x2="400" y2="0" stroke="rgba(245,240,232,0.12)" stroke-width="1.5"/>
          <!-- Thin border rect -->
          <rect x="18" y="18" width="364" height="364" fill="none" stroke="rgba(196,146,42,0.18)" stroke-width="1"/>
          <!-- Small corner marks -->
          <line x1="18" y1="18" x2="44" y2="18" stroke="rgba(196,146,42,0.5)" stroke-width="1.5"/>
          <line x1="18" y1="18" x2="18" y2="44" stroke="rgba(196,146,42,0.5)" stroke-width="1.5"/>
          <line x1="382" y1="18" x2="356" y2="18" stroke="rgba(196,146,42,0.5)" stroke-width="1.5"/>
          <line x1="382" y1="18" x2="382" y2="44" stroke="rgba(196,146,42,0.5)" stroke-width="1.5"/>
          <line x1="18" y1="382" x2="44" y2="382" stroke="rgba(196,146,42,0.5)" stroke-width="1.5"/>
          <line x1="18" y1="382" x2="18" y2="356" stroke="rgba(196,146,42,0.5)" stroke-width="1.5"/>
          <line x1="382" y1="382" x2="356" y2="382" stroke="rgba(196,146,42,0.5)" stroke-width="1.5"/>
          <line x1="382" y1="382" x2="382" y2="356" stroke="rgba(196,146,42,0.5)" stroke-width="1.5"/>
          <!-- Vertical rule (centre-right) -->
          <line x1="268" y1="60" x2="268" y2="180" stroke="rgba(245,240,232,0.2)" stroke-width="1"/>
          <!-- Horizontal rule (lower-left) -->
          <line x1="60" y1="295" x2="190" y2="295" stroke="rgba(196,146,42,0.3)" stroke-width="1"/>
        </svg>
        <!-- Centre stat label — rendered by JS from VISUAL_CONFIG -->
        <div class="visual-stat">
          <div class="vs-num-wrap">
            <span class="vs-num" id="vs-num"></span>
            <span class="vs-suffix" id="vs-suffix"></span>
          </div>
          <span class="vs-label" id="vs-label"></span>
        </div>
      </div>
    </div>
    <div class="about-content">
      <p class="section-label reveal">About · 關於我</p>
      <h2 class="section-heading reveal reveal-delay-1">陪你一起把想法<br>說得更清楚</h2>
      <p class="section-desc reveal reveal-delay-2">
        曾在科技業、新創與顧問業之間轉換，也在每一次的迷茫中，重新找到自己的答案。
        如今把這些歷程轉化為方法論，陪伴每一位正在思考「下一步怎麼走」的你。
      </p>
      <div class="about-tags reveal reveal-delay-3">
        <span class="tag">職涯轉職</span>
        <span class="tag">求職面試</span>
        <span class="tag">履歷健檢</span>
        <span class="tag">適性檢測</span>
        <span class="tag">自我探索</span>
        <span class="tag">個人品牌</span>
      </div>
    </div>
  </div>
</section>
<!-- SERVICES -->
<section id="services" style="background:var(--card-bg);">
  <div class="services-header">
    <div>
      <p class="section-label reveal">Services · 職涯服務</p>
      <h2 class="section-heading reveal reveal-delay-1">職涯陪你前行</h2>
    </div>
  </div>
  <div class="services-grid">
    <div class="service-card reveal" onclick="openForm()">
      <div class="card-number">01</div>
      <h3 class="card-title">職涯探索諮詢</h3>
      <p class="card-desc">不知道自己要什麼？透過結構化的對話，幫你梳理優勢、價值觀與興趣，找到最適合你的方向。適合初入職場或處於職涯瓶頸的你。</p>
      <span class="card-arrow">預約 →</span>
    </div>
    <div class="service-card reveal reveal-delay-1" onclick="openForm()">
      <div class="card-number">02</div>
      <h3 class="card-title">轉職策略規劃</h3>
      <p class="card-desc">有明確目標但不知如何下手？從履歷健診、求職策略到面試模擬，提供完整的轉職支援，讓每一步都走得更踏實。</p>
      <span class="card-arrow">預約 →</span>
    </div>
    <div class="service-card reveal reveal-delay-2" onclick="openForm()">
      <div class="card-number">03</div>
      <h3 class="card-title">講座 × 企業培訓</h3>
      <p class="card-desc">需要邀請演講或規劃職涯培訓課程？提供客製化的講座設計與團體工作坊，適合企業 HR、學校、社群組織。</p>
      <span class="card-arrow">預約 →</span>
    </div>
  </div>
</section>
<!-- FAQ -->
<section id="faq">
  <p class="section-label reveal">FAQ · 常見問題</p>
  <h2 class="section-heading reveal reveal-delay-1">你可能想知道的事</h2>
  <div class="faq-list">
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">我適合職涯諮詢嗎？<span class="faq-icon">+</span></button>
      <div class="faq-answer"><p>只要你對自己的職涯感到困惑、想改變現況，或是有明確目標卻不知如何達成，都非常適合。諮詢沒有「太早」或「太晚」，任何時間點都是開始的好時機。</p></div>
    </div>
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">諮詢的費用是多少？<span class="faq-icon">+</span></button>
      <div class="faq-answer"><p>讓彼此先確認是否合適。正式諮詢方案請在預約後透過信件確認。</p></div>
    </div>
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">諮詢以什麼形式進行？<span class="faq-icon">+</span></button>
      <div class="faq-answer"><p>目前主要以視訊方式進行，在台北的朋友也可以約在咖啡廳面對面。</p></div>
    </div>
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">可以協助指導履歷或準備面試嗎？<span class="faq-icon">+</span></button>
      <div class="faq-answer"><p>可以。如果你已經有明確的目標職位，我們可以從第一次對話就直接進入實戰準備。</p></div>
    </div>
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">諮詢後可以保密嗎？<span class="faq-icon">+</span></button>
      <div class="faq-answer"><p>絕對。所有的諮詢內容嚴格保密，不會以任何形式分享給第三方。這是諮詢關係最基本的信任基礎，請放心暢所欲言。</p></div>
    </div>
  </div>
</section>
<!-- CTA -->
<section class="cta-band" id="contact">
  <h2>準備好了嗎？</h2>
  <p>第一步往往是最難的<br>預約一次，讓我們一起開始</p>
  <button class="btn-gold" onclick="openForm()">預約諮詢</button>
</section>
<!-- FOOTER -->
<footer>
  <a href="#home" style="text-decoration:none;"><div class="footer-logo">職涯諮詢<span>三二事</span></div></a>
  <ul class="footer-links">
    <li><a href="#about">關於我</a></li>
    <li><a href="#services">服務</a></li>
    <li><a href="#faq">FAQ</a></li>
  </ul>
</footer>
<script>
  /* 將 VISUAL_CONFIG 的值注入 DOM，數字與符號分開渲染 */
  (function() {
    const raw = VISUAL_CONFIG.number;
    const match = raw.match(/^(\d+)(.*)/);
    const digit  = match ? match[1] : raw;
    const suffix = match ? match[2] : '';
    document.getElementById('vs-num').textContent    = digit;
    document.getElementById('vs-suffix').textContent = suffix;
    document.getElementById('vs-label').textContent  = VISUAL_CONFIG.label;
  })();

  const FORM_URL = 'https://docs.google.com/forms/d/e/1FAIpQLScFxA2Tkxi8Es59ld7SwPg7vDh1ZOd7fX_P2VyruDkkfCxPng/viewform';
  function openForm() { window.open(FORM_URL, '_blank'); }
  const nav = document.getElementById('nav');
  window.addEventListener('scroll', () => nav.classList.toggle('scrolled', window.scrollY > 60));
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); observer.unobserve(e.target); } });
  }, { threshold: 0.1 });
  reveals.forEach(el => observer.observe(el));
  function toggleFaq(btn) {
    const item = btn.closest('.faq-item');
    const isOpen = item.classList.contains('open');
    document.querySelectorAll('.faq-item.open').forEach(i => i.classList.remove('open'));
    if (!isOpen) item.classList.add('open');
  }
</script>
</body>
</html>




