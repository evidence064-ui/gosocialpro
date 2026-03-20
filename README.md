# gosocialpro
YOUR GO TO SOCIAL MEDIA MANAGER AND MARKETER

Copy

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Evidence | Social Media Manager & Strategist</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Outfit:wght@300;400;500;600;700&family=Space+Mono:ital@0;1&display=swap" rel="stylesheet">
<style>
  :root {
    --orange: #FF5C00;
    --orange-light: #FF8040;
    --black: #0A0A0A;
    --dark: #111111;
    --card: #161616;
    --border: #232323;
    --white: #F5F0E8;
    --grey: #888;
  }
 
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
 
  html { scroll-behavior: smooth; }
 
  body {
    font-family: 'Outfit', sans-serif;
    background: var(--black);
    color: var(--white);
    overflow-x: hidden;
  }
 
  /* NOISE OVERLAY */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9999;
    opacity: 0.4;
  }
 
  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 48px;
    background: rgba(10,10,10,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.5rem;
    letter-spacing: 3px;
    color: var(--white);
  }
  .nav-logo span { color: var(--orange); }
  .nav-links {
    display: flex; gap: 36px; list-style: none;
  }
  .nav-links a {
    font-size: 0.78rem;
    font-weight: 500;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;
    color: var(--grey);
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--orange); }
 
  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: 120px 48px 80px;
    position: relative;
    overflow: hidden;
  }
  .hero-bg {
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 80% 60% at 70% 50%, rgba(255,92,0,0.12) 0%, transparent 70%);
  }
  .hero-grid {
    position: absolute;
    inset: 0;
    background-image: linear-gradient(var(--border) 1px, transparent 1px),
                      linear-gradient(90deg, var(--border) 1px, transparent 1px);
    background-size: 60px 60px;
    opacity: 0.3;
    mask-image: radial-gradient(ellipse at center, black 30%, transparent 80%);
  }
  .hero-content { position: relative; z-index: 2; max-width: 900px; }
  .hero-eyebrow {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 4px;
    color: var(--orange);
    text-transform: uppercase;
    margin-bottom: 24px;
    display: flex; align-items: center; gap: 12px;
  }
  .hero-eyebrow::before {
    content: '';
    display: inline-block;
    width: 40px; height: 1px;
    background: var(--orange);
  }
  h1 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(4rem, 10vw, 8.5rem);
    line-height: 0.92;
    letter-spacing: -1px;
    margin-bottom: 32px;
  }
  h1 .accent { color: var(--orange); }
  h1 .outline {
    -webkit-text-stroke: 2px var(--white);
    color: transparent;
  }
  .hero-sub {
    font-size: 1.1rem;
    color: var(--grey);
    max-width: 560px;
    line-height: 1.7;
    margin-bottom: 48px;
  }
  .hero-cta {
    display: flex; gap: 16px; flex-wrap: wrap;
  }
  .btn-primary {
    display: inline-flex; align-items: center; gap: 10px;
    padding: 16px 36px;
    background: var(--orange);
    color: var(--black);
    font-weight: 700;
    font-size: 0.85rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;
    border: none; cursor: pointer;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-primary:hover { background: var(--orange-light); transform: translateY(-2px); }
  .btn-outline {
    display: inline-flex; align-items: center; gap: 10px;
    padding: 16px 36px;
    background: transparent;
    color: var(--white);
    font-weight: 600;
    font-size: 0.85rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;
    border: 1px solid var(--border);
    cursor: pointer;
    transition: border-color 0.2s, transform 0.15s;
  }
  .btn-outline:hover { border-color: var(--orange); color: var(--orange); transform: translateY(-2px); }
 
  /* TICKER */
  .ticker {
    background: var(--orange);
    padding: 14px 0;
    overflow: hidden;
    white-space: nowrap;
  }
  .ticker-inner {
    display: inline-block;
    animation: ticker 28s linear infinite;
  }
  .ticker-inner span {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1rem;
    letter-spacing: 3px;
    color: var(--black);
    margin: 0 32px;
  }
  @keyframes ticker {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); }
  }
 
  /* SECTION COMMON */
  section { padding: 100px 48px; }
  .section-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 4px;
    color: var(--orange);
    text-transform: uppercase;
    margin-bottom: 16px;
    display: flex; align-items: center; gap: 12px;
  }
  .section-label::before {
    content: '';
    display: inline-block;
    width: 24px; height: 1px;
    background: var(--orange);
  }
  .section-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(2.5rem, 5vw, 4rem);
    line-height: 1;
    margin-bottom: 60px;
  }
  .section-title .dim { color: var(--grey); }
 
  /* STATS */
  .stats {
    background: var(--dark);
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    padding: 70px 48px;
  }
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 40px;
  }
  .stat-item { text-align: center; }
  .stat-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 3.5rem;
    color: var(--orange);
    line-height: 1;
    margin-bottom: 8px;
  }
  .stat-label {
    font-size: 0.78rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--grey);
  }
 
  /* SERVICES */
  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 2px;
  }
  .service-card {
    background: var(--card);
    padding: 40px 32px;
    border: 1px solid var(--border);
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s;
  }
  .service-card::before {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: var(--orange);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.35s;
  }
  .service-card:hover { border-color: var(--orange); }
  .service-card:hover::before { transform: scaleX(1); }
  .service-icon {
    font-size: 1.8rem;
    margin-bottom: 20px;
  }
  .service-card h3 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.4rem;
    letter-spacing: 1px;
    margin-bottom: 12px;
  }
  .service-card p {
    font-size: 0.88rem;
    color: var(--grey);
    line-height: 1.65;
  }
 
  /* PLATFORMS */
  .platforms { background: var(--dark); }
  .platforms-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-bottom: 24px;
  }
  .platform-badge {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 10px 22px;
    border: 1px solid var(--border);
    font-size: 0.82rem;
    font-weight: 600;
    letter-spacing: 1px;
    color: var(--white);
    background: var(--card);
    transition: all 0.2s;
  }
  .platform-badge:hover {
    border-color: var(--orange);
    color: var(--orange);
  }
 
  /* PORTFOLIO / CLIENTS */
  .clients-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
  }
  .client-card {
    background: var(--card);
    border: 1px solid var(--border);
    overflow: hidden;
    transition: border-color 0.3s, transform 0.3s;
    position: relative;
  }
  .client-card:hover {
    border-color: var(--orange);
    transform: translateY(-4px);
  }
  .client-header {
    padding: 28px 28px 20px;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 16px;
  }
  .client-avatar {
    width: 48px; height: 48px;
    border-radius: 50%;
    background: var(--orange);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.2rem;
    color: var(--black);
    flex-shrink: 0;
  }
  .client-name {
    font-weight: 700;
    font-size: 1rem;
    margin-bottom: 2px;
  }
  .client-handle {
    font-family: 'Space Mono', monospace;
    font-size: 0.68rem;
    color: var(--orange);
  }
  .client-niche-badge {
    margin-left: auto;
    padding: 4px 12px;
    border: 1px solid var(--border);
    font-size: 0.68rem;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: var(--grey);
    white-space: nowrap;
  }
  .client-body { padding: 22px 28px; }
  .client-stats {
    display: flex; gap: 24px;
    margin-bottom: 18px;
  }
  .cstat { text-align: center; }
  .cstat-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.4rem;
    color: var(--white);
  }
  .cstat-lbl {
    font-size: 0.62rem;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: var(--grey);
  }
  .client-services {
    display: flex; flex-wrap: wrap; gap: 6px;
  }
  .tag {
    padding: 4px 10px;
    background: rgba(255,92,0,0.1);
    border: 1px solid rgba(255,92,0,0.25);
    font-size: 0.68rem;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: var(--orange);
  }
  .client-location {
    font-size: 0.75rem;
    color: var(--grey);
    margin-top: 14px;
    display: flex; align-items: center; gap: 6px;
  }
 
  /* NICHES */
  .niche-section { background: var(--dark); }
  .niche-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 16px;
  }
  .niche-item {
    padding: 28px 24px;
    border: 1px solid var(--border);
    background: var(--card);
    display: flex; align-items: center; gap: 16px;
    font-weight: 600;
    font-size: 0.9rem;
    transition: border-color 0.2s;
  }
  .niche-item:hover { border-color: var(--orange); }
  .niche-item .icon { font-size: 1.5rem; }
 
  /* CTA BANNER */
  .cta-banner {
    background: var(--orange);
    padding: 80px 48px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .cta-banner::before {
    content: 'HIRE ME';
    position: absolute;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 18vw;
    color: rgba(0,0,0,0.06);
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    white-space: nowrap;
    pointer-events: none;
  }
  .cta-banner h2 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(2.5rem, 6vw, 5rem);
    color: var(--black);
    margin-bottom: 16px;
    position: relative;
  }
  .cta-banner p {
    font-size: 1rem;
    color: rgba(0,0,0,0.65);
    max-width: 480px;
    margin: 0 auto 36px;
    position: relative;
  }
  .btn-dark {
    display: inline-flex; align-items: center; gap: 10px;
    padding: 16px 40px;
    background: var(--black);
    color: var(--white);
    font-weight: 700;
    font-size: 0.85rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;
    border: none; cursor: pointer;
    transition: transform 0.2s;
    position: relative;
  }
  .btn-dark:hover { transform: scale(1.04); }
 
  /* FOOTER */
  footer {
    background: var(--dark);
    border-top: 1px solid var(--border);
    padding: 40px 48px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 16px;
  }
  .footer-logo {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.3rem;
    letter-spacing: 3px;
  }
  .footer-logo span { color: var(--orange); }
  footer p {
    font-size: 0.78rem;
    color: var(--grey);
    font-family: 'Space Mono', monospace;
  }
 
  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .hero-content > * {
    animation: fadeUp 0.7s ease both;
  }
  .hero-content > *:nth-child(1) { animation-delay: 0.1s; }
  .hero-content > *:nth-child(2) { animation-delay: 0.25s; }
  .hero-content > *:nth-child(3) { animation-delay: 0.4s; }
  .hero-content > *:nth-child(4) { animation-delay: 0.55s; }
 
  /* RESPONSIVE */
  @media (max-width: 768px) {
    nav { padding: 16px 20px; }
    .nav-links { display: none; }
    section, .stats, .cta-banner { padding: 60px 20px; }
    .hero { padding: 100px 20px 60px; }
    footer { padding: 32px 20px; flex-direction: column; text-align: center; }
  }
</style>
</head>
<body>
 
<!-- NAV -->
<nav>
  <div class="nav-logo">Go<span>Social</span>Pro</div>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#portfolio">Clients</a></li>
    <li><a href="#niches">Niches</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>
 
<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-content">
    <div class="hero-eyebrow">Social Media Manager & Strategist</div>
    <h1>
      GROW YOUR<br>
      <span class="accent">BRAND</span><br>
      <span class="outline">ONLINE.</span>
    </h1>
    <p class="hero-sub">Full-service social media management — from strategy and content creation to ads and analytics. I build and grow brands across every major platform.</p>
    <div class="hero-cta">
      <a href="#portfolio" class="btn-primary">View My Work ↓</a>
      <a href="#contact" class="btn-outline">Let's Work Together</a>
    </div>
  </div>
</section>
 
<!-- TICKER -->
<div class="ticker">
  <div class="ticker-inner">
    <span>CONTENT STRATEGY</span><span>★</span>
    <span>REELS EDITING</span><span>★</span>
    <span>ADS MANAGEMENT</span><span>★</span>
    <span>ACCOUNT GROWTH</span><span>★</span>
    <span>BRAND IDENTITY</span><span>★</span>
    <span>CAPTION WRITING</span><span>★</span>
    <span>CONTENT CALENDAR</span><span>★</span>
    <span>ACCOUNT AUDIT</span><span>★</span>
    <span>CONTENT STRATEGY</span><span>★</span>
    <span>REELS EDITING</span><span>★</span>
    <span>ADS MANAGEMENT</span><span>★</span>
    <span>ACCOUNT GROWTH</span><span>★</span>
    <span>BRAND IDENTITY</span><span>★</span>
    <span>CAPTION WRITING</span><span>★</span>
    <span>CONTENT CALENDAR</span><span>★</span>
    <span>ACCOUNT AUDIT</span><span>★</span>
  </div>
</div>
 
<!-- STATS -->
<div class="stats">
  <div class="stats-grid">
    <div class="stat-item">
      <div class="stat-num">14+</div>
      <div class="stat-label">Brands Managed</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">6</div>
      <div class="stat-label">Platforms</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">5+</div>
      <div class="stat-label">Industries</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">100%</div>
      <div class="stat-label">Full-Service</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">∞</div>
      <div class="stat-label">Creative Energy</div>
    </div>
  </div>
</div>
 
<!-- SERVICES -->
<section id="services">
  <div class="section-label">What I Do</div>
  <div class="section-title">MY <span class="dim">SERVICES</span></div>
  <div class="services-grid">
    <div class="service-card">
      <div class="service-icon">🔍</div>
      <h3>Account Audit & Analysis</h3>
      <p>Deep-dive audits that uncover what's working, what's not, and exactly what needs to change to unlock growth.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🎯</div>
      <h3>Strategy Development</h3>
      <p>Custom-built social media strategies tailored to your niche, goals, and audience. No copy-paste templates.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🎨</div>
      <h3>Branding & Optimization</h3>
      <p>Full account branding — bio, highlights, grid aesthetic, profile picture, and tone of voice alignment.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🎬</div>
      <h3>Reels & Video Editing</h3>
      <p>Scroll-stopping Reels edited with hooks, text overlays, transitions, and trending audio for maximum reach.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">✍️</div>
      <h3>Caption & Hook Writing</h3>
      <p>Captions that convert, hooks that stop the scroll. Strategic copywriting built for engagement and action.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">📅</div>
      <h3>Content Calendar</h3>
      <p>Monthly content calendars with post ideas, captions, formats, and posting schedules — all planned ahead.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">📱</div>
      <h3>Full Account Management</h3>
      <p>End-to-end management: posting, community engagement, DM responses, reporting, and continuous optimization.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">📊</div>
      <h3>Ads Campaign Management</h3>
      <p>Paid social campaigns on Instagram, Facebook, and TikTok — from creative to targeting to ROAS tracking.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🖼️</div>
      <h3>Content Creation</h3>
      <p>Graphics, carousels, static posts, and short-form videos using provided or sourced footage with branded design.</p>
    </div>
  </div>
</section>
 
<!-- PLATFORMS -->
<section class="platforms" id="platforms">
  <div class="section-label">Where I Work</div>
  <div class="section-title">PLATFORMS <span class="dim">I MANAGE</span></div>
  <div class="platforms-row">
    <div class="platform-badge">📸 Instagram</div>
    <div class="platform-badge">🎵 TikTok</div>
    <div class="platform-badge">▶️ YouTube</div>
    <div class="platform-badge">🐦 Twitter / X</div>
    <div class="platform-badge">💼 LinkedIn</div>
    <div class="platform-badge">✈️ Telegram</div>
  </div>
</section>
 
<!-- PORTFOLIO -->
<section id="portfolio">
  <div class="section-label">Client Work</div>
  <div class="section-title">BRANDS I'VE <span class="dim">WORKED WITH</span></div>
  <div class="clients-grid">
 
    <!-- Ryan's Cafe -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">RC</div>
        <div>
          <div class="client-name">Ryan's Cafe</div>
          <div class="client-handle">@_ryanscafe_</div>
        </div>
        <div class="client-niche-badge">☕ Food & Bev</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">460</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">31</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Account Mgmt</span>
          <span class="tag">Reels</span>
          <span class="tag">Content Creation</span>
          <span class="tag">Captions</span>
        </div>
        <div class="client-location">📍 Fairfield, California, USA</div>
      </div>
    </div>
 
    <!-- Lite N' Eze -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">LN</div>
        <div>
          <div class="client-name">Lite N' Eze Bar & Restaurant</div>
          <div class="client-handle">@liteneze</div>
        </div>
        <div class="client-niche-badge">🍽️ Restaurant</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">3.2K</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">101</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Strategy</span>
          <span class="tag">Content Design</span>
          <span class="tag">Account Mgmt</span>
        </div>
        <div class="client-location">📍 English Harbour, Antigua & Barbuda</div>
      </div>
    </div>
 
    <!-- Cafe Cino -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">CC</div>
        <div>
          <div class="client-name">Cafe Cino</div>
          <div class="client-handle">@cafecinopulheim</div>
        </div>
        <div class="client-niche-badge">☕ Café</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">762</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">14</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Reels</span>
          <span class="tag">Branding</span>
          <span class="tag">Content Calendar</span>
        </div>
        <div class="client-location">📍 Pulheim, Germany</div>
      </div>
    </div>
 
    <!-- Revival Beauty + Wellness -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">RB</div>
        <div>
          <div class="client-name">Revival Beauty + Wellness</div>
          <div class="client-handle">@revival.beauty.wellness</div>
        </div>
        <div class="client-niche-badge">💅 Beauty</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">683</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">149</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Account Optimization</span>
          <span class="tag">Strategy</span>
          <span class="tag">Branding</span>
        </div>
        <div class="client-location">📍 Fairfield, California, USA</div>
      </div>
    </div>
 
    <!-- HeadSpace Beauty -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">HS</div>
        <div>
          <div class="client-name">HeadSpace Beauty Lounge</div>
          <div class="client-handle">@headspace_beauty</div>
        </div>
        <div class="client-niche-badge">💅 Beauty</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">2.1K</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">544</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Content Strategy</span>
          <span class="tag">Reels</span>
          <span class="tag">Community</span>
        </div>
        <div class="client-location">📍 Beauty Lounge</div>
      </div>
    </div>
 
    <!-- Danielle's Body & Skin Care -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">DB</div>
        <div>
          <div class="client-name">Danielle's Body & Skin Care</div>
          <div class="client-handle">@danielle.phiacademy.master</div>
        </div>
        <div class="client-niche-badge">✨ PMU / Beauty</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">3.4K</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">1,282</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Account Audit</span>
          <span class="tag">Strategy</span>
          <span class="tag">Caption Writing</span>
        </div>
        <div class="client-location">📍 New York, USA</div>
      </div>
    </div>
 
    <!-- BrowLush -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">BL</div>
        <div>
          <div class="client-name">BrowLush</div>
          <div class="client-handle">@browlushla</div>
        </div>
        <div class="client-niche-badge">✨ Beauty Salon</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">4K</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">298</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Branding</span>
          <span class="tag">Content Creation</span>
          <span class="tag">Highlights</span>
        </div>
        <div class="client-location">📍 Beverly Hills & LA, USA</div>
      </div>
    </div>
 
    <!-- OSA18 -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">OS</div>
        <div>
          <div class="client-name">OSA18</div>
          <div class="client-handle">@osa18_official</div>
        </div>
        <div class="client-niche-badge">🎵 Music</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">3.7K</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">139</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Artist Branding</span>
          <span class="tag">Reels</span>
          <span class="tag">Music Promo</span>
        </div>
        <div class="client-location">📍 Music Artist — Nigeria/Italy</div>
      </div>
    </div>
 
    <!-- JoJo165 -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">JJ</div>
        <div>
          <div class="client-name">JoJo165</div>
          <div class="client-handle">@jojo165.music</div>
        </div>
        <div class="client-niche-badge">🎤 Music</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">476</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">46</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Reels Editing</span>
          <span class="tag">Hook Writing</span>
          <span class="tag">Strategy</span>
        </div>
        <div class="client-location">📍 Deutschrap Artist — Germany</div>
      </div>
    </div>
 
    <!-- Sacred Presents -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">SP</div>
        <div>
          <div class="client-name">Sacred Presents</div>
          <div class="client-handle">@sacredpresents</div>
        </div>
        <div class="client-niche-badge">🎧 Music / Art</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">20</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">13</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Account Setup</span>
          <span class="tag">Branding</span>
          <span class="tag">Content Strategy</span>
        </div>
        <div class="client-location">📍 Laser / Electronic Artist</div>
      </div>
    </div>
 
    <!-- Ritualmanufaktur -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">RM</div>
        <div>
          <div class="client-name">Ritualmanufaktur</div>
          <div class="client-handle">@ritualmanufaktur</div>
        </div>
        <div class="client-niche-badge">🌿 Wellness</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">1K</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">374</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Content Calendar</span>
          <span class="tag">Strategy</span>
          <span class="tag">Reels</span>
        </div>
        <div class="client-location">📍 Germany</div>
      </div>
    </div>
 
    <!-- Jonas Digital Monetizer -->
    <div class="client-card">
      <div class="client-header">
        <div class="client-avatar">JD</div>
        <div>
          <div class="client-name">Jonas Digital Monetizer</div>
          <div class="client-handle">@jonas.digitalmonetizer</div>
        </div>
        <div class="client-niche-badge">💻 Digital Services</div>
      </div>
      <div class="client-body">
        <div class="client-stats">
          <div class="cstat"><div class="cstat-num">75</div><div class="cstat-lbl">Followers</div></div>
          <div class="cstat"><div class="cstat-num">19</div><div class="cstat-lbl">Posts</div></div>
        </div>
        <div class="client-services">
          <span class="tag">Account Setup</span>
          <span class="tag">Branding</span>
          <span class="tag">Content Strategy</span>
          <span class="tag">Captions</span>
        </div>
        <div class="client-location">📍 Germany</div>
      </div>
    </div>
 
  </div>
</section>
 
<!-- NICHES -->
<section class="niche-section" id="niches">
  <div class="section-label">Industry Expertise</div>
  <div class="section-title">NICHES I <span class="dim">SPECIALISE IN</span></div>
  <div class="niche-list">
    <div class="niche-item"><span class="icon">🎵</span> Music & Artists</div>
    <div class="niche-item"><span class="icon">💅</span> Beauty & Salons</div>
    <div class="niche-item"><span class="icon">🍽️</span> Restaurants & Cafés</div>
    <div class="niche-item"><span class="icon">🌿</span> Wellness & Health</div>
    <div class="niche-item"><span class="icon">💻</span> Digital Services</div>
    <div class="niche-item"><span class="icon">🛍️</span> E-Commerce</div>
    <div class="niche-item"><span class="icon">🏠</span> Local Businesses</div>
    <div class="niche-item"><span class="icon">📱</span> Personal Brands</div>
    <div class="niche-item"><span class="icon">🏡</span> Real Estate</div>
  </div>
  <p style="margin-top: 32px; color: var(--grey); font-size: 0.9rem; max-width: 600px; line-height: 1.7;">
    Not limited to the above — I work with brands across <strong style="color: var(--white);">all industries and niches</strong>. Whether you're a startup, an established business, or a personal brand, I bring the same full-service expertise to every client.
  </p>
</section>
 
<!-- CTA -->
<div class="cta-banner" id="contact">
  <h2>READY TO GROW YOUR BRAND?</h2>
  <p>Let's build a social media presence that actually converts. Reach out and let's talk strategy.</p>
  <div style="display:flex; gap:14px; justify-content:center; flex-wrap:wrap; position:relative;">
    <a href="mailto:evidence064@gmail.com" class="btn-dark">✉️ Email Me</a>
    <a href="https://wa.me/15852812526" target="_blank" class="btn-dark" style="background:#1a1a1a; color:#fff;">💬 WhatsApp</a>
    <a href="https://www.instagram.com/gosocialpro1?igsh=aDBtbGppeGRvcHdv" target="_blank" class="btn-dark">📸 Instagram</a>
    <a href="https://www.tiktok.com/@gosocialpro1?_r=1&_t=ZS-94rH5sNhAO0" target="_blank" class="btn-dark">🎵 TikTok</a>
  </div>
  <p style="margin-top:24px; font-size:0.8rem; color:rgba(0,0,0,0.5); position:relative;">evidence064@gmail.com &nbsp;·&nbsp; +1 (585) 281-2526</p>
</div>
 
<!-- FOOTER -->
<footer>
  <div class="footer-logo">Go<span>Social</span>Pro</div>
  <p>© 2025 GoSocialPro1 · Social Media Manager · Nigeria, Africa & Germany</p>
  <p>Instagram · TikTok · YouTube
