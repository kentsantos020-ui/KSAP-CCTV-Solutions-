<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KSAP CCTV Solutions</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Serif+Display&display=swap" rel="stylesheet">
<style>
:root {
  --red: #e8281e;
  --red-light: #fdf1f0;
  --white: #ffffff;
  --off: #f7f7f5;
  --gray-100: #f0efed;
  --gray-200: #e0dedb;
  --gray-400: #a09d98;
  --gray-600: #6b6864;
  --gray-800: #2a2825;
  --black: #111110;
  --font-display: 'DM Serif Display', serif;
  --font-body: 'DM Sans', sans-serif;
}
*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior:smooth; }
body {
  font-family: var(--font-body);
  background: var(--white);
  color: var(--gray-800);
  -webkit-font-smoothing: antialiased;
}

/* ===== NAV ===== */
nav {
  position: sticky; top:0; z-index:200;
  background: rgba(255,255,255,0.95);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid var(--gray-200);
  padding: 0 4rem;
  display: flex; align-items:center; justify-content:space-between;
  height: 68px;
}
.nav-logo img {
  height: 42px; width: auto; object-fit:contain;
}
.nav-links { display:flex; gap:2.5rem; align-items:center; }
.nav-links a {
  text-decoration:none; color: var(--gray-600);
  font-size:0.82rem; font-weight:500; letter-spacing:0.04em;
  transition:color 0.2s;
}
.nav-links a:hover { color: var(--red); }
.nav-divider { width:1px; height:20px; background:var(--gray-200); }
.btn-nav {
  background: var(--red); color:#fff; border:none;
  padding: 9px 22px; font-family: var(--font-body);
  font-size:0.82rem; font-weight:600; cursor:pointer;
  transition:opacity 0.2s; letter-spacing:0.02em;
  border-radius:2px;
}
.btn-nav:hover { opacity:0.88; }

/* ===== HERO ===== */
.hero {
  min-height: calc(100vh - 68px);
  background: var(--off);
  display:grid; grid-template-columns:1fr 1fr;
  align-items:stretch; overflow:hidden;
}
.hero-left {
  padding: 6rem 4rem 6rem 6rem;
  display:flex; flex-direction:column; justify-content:center;
  border-right: 1px solid var(--gray-200);
}
.hero-eyebrow {
  display:flex; align-items:center; gap:0.75rem; margin-bottom:2rem;
}
.eyebrow-line { width:32px; height:1px; background:var(--red); }
.eyebrow-text { font-size:0.72rem; font-weight:600; letter-spacing:0.12em; color:var(--red); text-transform:uppercase; }
.hero-left h1 {
  font-family: var(--font-display);
  font-size: clamp(2.8rem, 4vw, 4.2rem);
  line-height: 1.05; color: var(--black);
  font-weight:400;
}
.hero-left h1 em { font-style:italic; color:var(--red); }
.hero-left p {
  margin-top: 1.75rem; color:var(--gray-600);
  font-size:1rem; line-height:1.75; max-width:420px;
  font-weight:300;
}
.hero-actions { margin-top:3rem; display:flex; gap:1rem; align-items:center; }
.btn-primary {
  background:var(--red); color:#fff; border:none; padding:13px 28px;
  font-family:var(--font-body); font-size:0.85rem; font-weight:600;
  cursor:pointer; border-radius:2px; transition:opacity 0.2s;
  text-decoration:none; display:inline-block; letter-spacing:0.02em;
}
.btn-primary:hover { opacity:0.88; }
.btn-ghost {
  background:transparent; color:var(--gray-800); border:1px solid var(--gray-200);
  padding:13px 28px; font-family:var(--font-body); font-size:0.85rem; font-weight:500;
  cursor:pointer; border-radius:2px; transition:border-color 0.2s, color 0.2s;
  text-decoration:none; display:inline-block;
}
.btn-ghost:hover { border-color:var(--red); color:var(--red); }
.hero-stats {
  margin-top:4rem; padding-top:2.5rem; border-top:1px solid var(--gray-200);
  display:flex; gap:2.5rem;
}
.stat-item .num {
  font-family:var(--font-display); font-size:2.2rem; color:var(--black); line-height:1;
}
.stat-item .lbl {
  font-size:0.72rem; color:var(--gray-400); margin-top:4px;
  letter-spacing:0.06em; text-transform:uppercase; font-weight:500;
}
.hero-right {
  position:relative; overflow:hidden;
  background: var(--white);
  display:flex; align-items:center; justify-content:center;
}
.hero-right-bg {
  position:absolute; inset:0;
  background: linear-gradient(135deg, #f9f9f7 0%, #f0efed 100%);
}
.hero-right-img {
  position:relative; z-index:1;
  width:80%; height:80%; object-fit:cover;
  box-shadow: 0 32px 80px rgba(0,0,0,0.1);
}
.hero-accent {
  position:absolute; bottom:2rem; left:2rem; z-index:2;
  background:var(--white); border:1px solid var(--gray-200); padding:1rem 1.25rem;
  display:flex; align-items:center; gap:0.75rem;
  box-shadow: 0 4px 20px rgba(0,0,0,0.06);
}
.accent-dot { width:8px; height:8px; border-radius:50%; background:var(--red); flex-shrink:0; }
.accent-text { font-size:0.75rem; font-weight:500; color:var(--gray-600); }
.accent-text strong { color:var(--black); display:block; font-size:0.82rem; }

/* ===== BRAND BAR ===== */
.brand-bar {
  padding:1.5rem 4rem;
  border-bottom:1px solid var(--gray-200);
  display:flex; align-items:center; gap:0; overflow:hidden;
}
.brand-bar-label {
  font-size:0.68rem; letter-spacing:0.1em; color:var(--gray-400);
  text-transform:uppercase; font-weight:500; white-space:nowrap;
  padding-right:2.5rem; border-right:1px solid var(--gray-200);
  flex-shrink:0;
}
.brand-scroll {
  display:flex; gap:3rem; align-items:center; padding-left:2.5rem; flex-wrap:wrap;
}
.brand-item {
  font-size:0.78rem; font-weight:600; letter-spacing:0.08em;
  text-transform:uppercase; color:var(--gray-400); transition:color 0.2s; cursor:default;
}
.brand-item:hover { color:var(--gray-800); }

/* ===== SECTION WRAPPER ===== */
.section-wrap { max-width:1200px; margin:0 auto; padding:6rem 2rem; }
.section-wrap.flush { padding-left:0; padding-right:0; max-width:none; }

.tag { font-size:0.7rem; font-weight:600; letter-spacing:0.12em; text-transform:uppercase; color:var(--red); }
.section-title {
  font-family:var(--font-display); font-size:clamp(2rem,3vw,2.8rem);
  color:var(--black); margin-top:0.5rem; font-weight:400; line-height:1.1;
}
.section-sub { color:var(--gray-600); font-size:0.95rem; margin-top:0.75rem; line-height:1.7; max-width:480px; }

/* ===== PRODUCTS ===== */
.products-section { background:var(--off); padding:6rem 0; }
.products-inner { max-width:1200px; margin:0 auto; padding:0 2rem; }
.products-head {
  display:flex; align-items:flex-end; justify-content:space-between;
  margin-bottom:3rem; flex-wrap:wrap; gap:1.5rem;
}

.filter-tabs { display:flex; gap:0; border:1px solid var(--gray-200); background:var(--white); border-radius:3px; overflow:hidden; }
.filter-btn {
  background:transparent; border:none; border-right:1px solid var(--gray-200);
  color:var(--gray-600); padding:8px 18px; font-family:var(--font-body);
  font-size:0.78rem; font-weight:500; letter-spacing:0.04em; cursor:pointer;
  transition:all 0.2s; text-transform:uppercase;
}
.filter-btn:last-child { border-right:none; }
.filter-btn.active, .filter-btn:hover { background:var(--red); color:#fff; }

.product-grid {
  display:grid; grid-template-columns:repeat(auto-fill, minmax(280px,1fr)); gap:1px;
  background:var(--gray-200);
  border:1px solid var(--gray-200);
}
.product-card {
  background:var(--white); display:flex; flex-direction:column;
  cursor:pointer; transition:background 0.2s;
}
.product-card:hover { background:var(--off); }
.product-img-wrap {
  aspect-ratio:3/4; overflow:hidden; position:relative; background:var(--off);
}
.product-img-wrap img { width:100%; height:100%; object-fit:cover; transition:transform 0.5s ease; }
.product-card:hover .product-img-wrap img { transform:scale(1.04); }
.product-tag-badge {
  position:absolute; top:0; left:0;
  background:var(--red); color:#fff;
  font-size:0.62rem; font-weight:600; letter-spacing:0.08em;
  text-transform:uppercase; padding:5px 10px;
}
.product-body { padding:1.5rem; flex:1; display:flex; flex-direction:column; border-top:1px solid var(--gray-200); }
.product-cat { font-size:0.68rem; color:var(--red); font-weight:600; letter-spacing:0.08em; text-transform:uppercase; }
.product-name { font-family:var(--font-display); font-size:1.15rem; color:var(--black); margin-top:4px; line-height:1.2; }
.product-desc { font-size:0.8rem; color:var(--gray-600); margin-top:0.5rem; line-height:1.6; flex:1; }
.product-feats { margin-top:0.75rem; display:flex; flex-wrap:wrap; gap:4px; }
.feat { font-size:0.62rem; padding:3px 8px; background:var(--gray-100); color:var(--gray-600); letter-spacing:0.04em; text-transform:uppercase; font-weight:500; }
.product-foot { margin-top:1.25rem; padding-top:1rem; border-top:1px solid var(--gray-100); display:flex; align-items:center; justify-content:space-between; }
.product-price { font-size:0.75rem; color:var(--gray-400); font-weight:500; }
.btn-inq {
  background:var(--black); color:#fff; border:none; padding:7px 16px;
  font-family:var(--font-body); font-size:0.75rem; font-weight:600;
  cursor:pointer; border-radius:2px; transition:background 0.2s; letter-spacing:0.02em;
}
.btn-inq:hover { background:var(--red); }

/* ===== SERVICES ===== */
.services-grid { display:grid; grid-template-columns:repeat(3,1fr); gap:1px; background:var(--gray-200); border:1px solid var(--gray-200); margin-top:3rem; }
.service-card { background:var(--white); padding:2.5rem 2rem; transition:background 0.2s; }
.service-card:hover { background:var(--off); }
.svc-num { font-family:var(--font-display); font-size:2.5rem; color:var(--gray-200); line-height:1; }
.service-card h3 { font-family:var(--font-display); font-size:1.15rem; color:var(--black); margin-top:0.75rem; font-weight:400; }
.service-card p { font-size:0.82rem; color:var(--gray-600); margin-top:0.5rem; line-height:1.65; }
.svc-tag { display:inline-block; margin-top:1rem; font-size:0.65rem; color:var(--red); font-weight:600; letter-spacing:0.08em; text-transform:uppercase; }

/* ===== WHY KSAP ===== */
.why-section { background:var(--black); padding:6rem 0; }
.why-inner { max-width:1200px; margin:0 auto; padding:0 2rem; display:grid; grid-template-columns:1fr 1fr; gap:5rem; align-items:start; }
.why-left .tag { color:#e8281e; }
.why-left h2 { font-family:var(--font-display); font-size:clamp(2rem,3vw,3rem); color:var(--white); margin-top:0.5rem; font-weight:400; line-height:1.1; }
.why-left p { color: rgba(255,255,255,0.5); font-size:0.92rem; margin-top:1rem; line-height:1.75; }
.why-points { margin-top:3rem; display:flex; flex-direction:column; gap:0; border-top:1px solid rgba(255,255,255,0.08); }
.why-pt {
  padding:1.5rem 0; border-bottom:1px solid rgba(255,255,255,0.08);
  display:grid; grid-template-columns:36px 1fr; gap:1rem; align-items:start;
}
.why-pt-num { font-size:0.7rem; color:var(--red); font-weight:600; padding-top:4px; }
.why-pt h4 { font-size:0.9rem; color:var(--white); font-weight:600; }
.why-pt p { font-size:0.8rem; color:rgba(255,255,255,0.45); margin-top:4px; line-height:1.6; }
.why-right { }
.brand-mosaic { display:grid; grid-template-columns:1fr 1fr; gap:1px; background:rgba(255,255,255,0.08); border:1px solid rgba(255,255,255,0.08); }
.bm-card { background:var(--black); padding:2rem 1.5rem; transition:background 0.2s; }
.bm-card:hover { background:#1a1a18; }
.bm-name { font-size:0.85rem; font-weight:700; letter-spacing:0.08em; text-transform:uppercase; color:var(--white); }
.bm-desc { font-size:0.7rem; color:rgba(255,255,255,0.35); margin-top:4px; letter-spacing:0.04em; }
.why-cta { margin-top:2rem; }
.btn-white {
  background:var(--white); color:var(--black); border:none; padding:13px 28px;
  font-family:var(--font-body); font-size:0.85rem; font-weight:600;
  cursor:pointer; border-radius:2px; transition:opacity 0.2s;
  text-decoration:none; display:inline-block;
}
.btn-white:hover { opacity:0.88; }

/* ===== INQUIRE ===== */
.inquire-section { padding:6rem 0; background:var(--off); }
.inquire-inner { max-width:1200px; margin:0 auto; padding:0 2rem; display:grid; grid-template-columns:1fr 1fr; gap:5rem; align-items:center; }
.inq-left h2 { font-family:var(--font-display); font-size:clamp(2rem,3vw,2.8rem); color:var(--black); font-weight:400; line-height:1.1; }
.inq-left p { color:var(--gray-600); font-size:0.92rem; margin-top:1rem; line-height:1.75; }
.inq-qr {
  background:var(--white); border:1px solid var(--gray-200); padding:2rem;
  display:inline-flex; flex-direction:column; align-items:center; gap:1rem; margin-top:2rem;
}
.inq-qr img { width:160px; height:160px; object-fit:contain; }
.inq-qr-label { font-size:0.7rem; color:var(--gray-400); letter-spacing:0.08em; text-transform:uppercase; font-weight:500; }
.inq-right { background:var(--white); border:1px solid var(--gray-200); padding:2.5rem; }
.inq-right h3 { font-family:var(--font-display); font-size:1.4rem; color:var(--black); font-weight:400; margin-bottom:1.5rem; }
.form-group { margin-bottom:1.25rem; }
.form-group label { display:block; font-size:0.7rem; font-weight:600; letter-spacing:0.08em; text-transform:uppercase; color:var(--gray-400); margin-bottom:6px; }
.form-group input, .form-group select, .form-group textarea {
  width:100%; padding:11px 14px; border:1px solid var(--gray-200); background:var(--off);
  font-family:var(--font-body); font-size:0.88rem; color:var(--black); outline:none;
  transition:border-color 0.2s; border-radius:2px;
}
.form-group input:focus, .form-group select:focus, .form-group textarea:focus { border-color:var(--red); background:var(--white); }
.form-group textarea { height:90px; resize:vertical; }
.form-row { display:grid; grid-template-columns:1fr 1fr; gap:1rem; }
.btn-submit {
  width:100%; background:var(--red); color:#fff; border:none; padding:14px;
  font-family:var(--font-body); font-size:0.88rem; font-weight:600; cursor:pointer;
  border-radius:2px; transition:opacity 0.2s; margin-top:0.5rem; letter-spacing:0.02em;
}
.btn-submit:hover { opacity:0.88; }

/* ===== CONTACT STRIP ===== */
.contact-strip { background:var(--white); border-top:1px solid var(--gray-200); border-bottom:1px solid var(--gray-200); padding:2rem 0; }
.contact-strip-inner { max-width:1200px; margin:0 auto; padding:0 2rem; display:flex; gap:3rem; flex-wrap:wrap; align-items:center; justify-content:space-between; }
.c-item { display:flex; align-items:center; gap:0.75rem; }
.c-icon { font-size:1.1rem; }
.c-label { font-size:0.68rem; color:var(--gray-400); text-transform:uppercase; letter-spacing:0.06em; font-weight:500; }
.c-val { font-size:0.85rem; color:var(--black); font-weight:500; margin-top:1px; }

/* ===== MODAL ===== */
.modal-overlay {
  position:fixed; inset:0; background:rgba(17,17,16,0.7); z-index:500;
  display:none; align-items:center; justify-content:center; padding:1rem;
  backdrop-filter:blur(4px);
}
.modal-overlay.open { display:flex; }
.modal {
  background:var(--white); max-width:480px; width:100%; padding:2.5rem;
  border:1px solid var(--gray-200); position:relative; animation:mIn 0.25s ease;
}
@keyframes mIn { from{opacity:0;transform:translateY(12px)} to{opacity:1;transform:translateY(0)} }
.modal-close {
  position:absolute; top:1.25rem; right:1.25rem; background:none; border:none;
  font-size:1.2rem; color:var(--gray-400); cursor:pointer; line-height:1;
}
.modal-close:hover { color:var(--black); }
.modal-prod { font-size:0.68rem; color:var(--red); font-weight:600; letter-spacing:0.1em; text-transform:uppercase; margin-bottom:0.5rem; }
.modal h3 { font-family:var(--font-display); font-size:1.6rem; color:var(--black); font-weight:400; margin-bottom:1.5rem; }

/* ===== FOOTER ===== */
footer { background:var(--black); padding:3rem 2rem; }
.footer-inner { max-width:1200px; margin:0 auto; display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; gap:1.5rem; }
.footer-logo img { height:36px; filter:brightness(0) invert(1); }
.footer-links { display:flex; gap:2rem; }
.footer-links a { color:rgba(255,255,255,0.35); text-decoration:none; font-size:0.78rem; transition:color 0.2s; }
.footer-links a:hover { color:rgba(255,255,255,0.8); }
.footer-copy { color:rgba(255,255,255,0.2); font-size:0.72rem; width:100%; text-align:center; padding-top:2rem; border-top:1px solid rgba(255,255,255,0.06); margin-top:2rem; }

@media(max-width:900px){
  .hero { grid-template-columns:1fr; }
  .hero-right { display:none; }
  nav { padding:0 1.5rem; }
  .hero-left { padding:4rem 1.5rem; }
  .why-inner, .inquire-inner { grid-template-columns:1fr; gap:3rem; }
  .services-grid { grid-template-columns:1fr 1fr; }
  .brand-bar { padding:1.5rem 1.5rem; }
  .nav-links { display:none; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">
    <img src="/mnt/user-data/uploads/493187094_1176512570938315_1926001927982410807_n.jpg" alt="KSAP CCTV Solutions">
  </div>
  <div class="nav-links">
    <a href="#products">Products</a>
    <a href="#services">Services</a>
    <a href="#whyus">About</a>
    <a href="#inquire">Contact</a>
    <div class="nav-divider"></div>
    <button class="btn-nav" onclick="openModal('General Inquiry')">Get a Quote</button>
  </div>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-left">
    <div class="hero-eyebrow">
      <div class="eyebrow-line"></div>
      <div class="eyebrow-text">Authorized Dahua Distributor — Philippines</div>
    </div>
    <h1>Smart Security,<br><em>Simplified.</em></h1>
    <p>Professional CCTV systems installed by certified technicians. From home cameras to enterprise perimeter protection — we deliver complete security solutions.</p>
    <div class="hero-actions">
      <a href="#products" class="btn-primary">Shop Cameras</a>
      <a href="#inquire" class="btn-ghost">Free Site Survey</a>
    </div>
    <div class="hero-stats">
      <div class="stat-item"><div class="num">500+</div><div class="lbl">Installations</div></div>
      <div class="stat-item"><div class="num">24/7</div><div class="lbl">Support</div></div>
      <div class="stat-item"><div class="num">8+</div><div class="lbl">Brands</div></div>
    </div>
  </div>
  <div class="hero-right">
    <div class="hero-right-bg"></div>
    <img class="hero-right-img" src="/mnt/user-data/uploads/12.png" alt="Hero Series H31">
    <div class="hero-accent">
      <div class="accent-dot"></div>
      <div class="accent-text">
        <strong>WiFi 6 · AI Detection · 360° PTZ</strong>
        Dahua Hero Series H31
      </div>
    </div>
  </div>
</div>

<!-- BRAND BAR -->
<div class="brand-bar">
  <div class="brand-bar-label">Our Brands</div>
  <div class="brand-scroll">
    <div class="brand-item">Dahua</div>
    <div class="brand-item">Hikvision</div>
    <div class="brand-item">Imou</div>
    <div class="brand-item">Seagate</div>
    <div class="brand-item">ZKTeco</div>
    <div class="brand-item">Ruijie Reyee</div>
    <div class="brand-item">VR-CHT</div>
  </div>
</div>

<!-- PRODUCTS -->
<div class="products-section" id="products">
  <div class="products-inner">
    <div class="products-head">
      <div>
        <div class="tag">// Products</div>
        <div class="section-title" style="margin-top:0.4rem;">Security Camera Lineup</div>
        <div class="section-sub">Indoor, outdoor, and enterprise-grade cameras for every need.</div>
      </div>
      <div class="filter-tabs">
        <button class="filter-btn active" onclick="filterProducts('all',this)">All</button>
        <button class="filter-btn" onclick="filterProducts('indoor',this)">Indoor</button>
        <button class="filter-btn" onclick="filterProducts('outdoor',this)">Outdoor</button>
        <button class="filter-btn" onclick="filterProducts('wifi',this)">WiFi</button>
        <button class="filter-btn" onclick="filterProducts('ptz',this)">PTZ</button>
      </div>
    </div>

    <div class="product-grid" id="productGrid">

      <div class="product-card" data-tags="indoor wifi">
        <div class="product-img-wrap">
          <img src="/mnt/user-data/uploads/12.png" alt="Hero Series H31">
          <div class="product-tag-badge">WiFi 6</div>
        </div>
        <div class="product-body">
          <div class="product-cat">Indoor · Wireless</div>
          <div class="product-name">Hero Series H31</div>
          <div class="product-desc">360° pan-tilt WiFi 6 camera with AI human & pet detection, cloud storage, and auto smart tracking.</div>
          <div class="product-feats">
            <span class="feat">360° PT</span><span class="feat">AI Detection</span><span class="feat">Cloud</span><span class="feat">Two-Way Talk</span>
          </div>
          <div class="product-foot">
            <div class="product-price">Inquire for price</div>
            <button class="btn-inq" onclick="openModal('Hero Series H31')">Inquire</button>
          </div>
        </div>
      </div>

      <div class="product-card" data-tags="indoor wifi">
        <div class="product-img-wrap">
          <img src="/mnt/user-data/uploads/6.png" alt="DH-H3A/H5A">
          <div class="product-tag-badge">Smart Home</div>
        </div>
        <div class="product-body">
          <div class="product-cat">Indoor · Wireless</div>
          <div class="product-name">DH-H3A / H5A</div>
          <div class="product-desc">Smart home security with AI human detection, night vision, and real-time mobile app control.</div>
          <div class="product-feats">
            <span class="feat">AI Human</span><span class="feat">Night Vision</span><span class="feat">App Control</span>
          </div>
          <div class="product-foot">
            <div class="product-price">Inquire for price</div>
            <button class="btn-inq" onclick="openModal('DH-H3A/H5A Smart Home Security')">Inquire</button>
          </div>
        </div>
      </div>

      <div class="product-card" data-tags="outdoor wifi ptz">
        <div class="product-img-wrap">
          <img src="/mnt/user-data/uploads/7.png" alt="PICOO Outdoor">
          <div class="product-tag-badge">Outdoor PTZ</div>
        </div>
        <div class="product-body">
          <div class="product-cat">Outdoor · PTZ</div>
          <div class="product-name">PICOO Outdoor</div>
          <div class="product-desc">Smart dual-light PTZ with AI detection, active deterrence using blue/red flashing lights, and smart linkage.</div>
          <div class="product-feats">
            <span class="feat">Dual Light</span><span class="feat">PTZ</span><span class="feat">Deterrence</span>
          </div>
          <div class="product-foot">
            <div class="product-price">Inquire for price</div>
            <button class="btn-inq" onclick="openModal('PICOO Outdoor Smart Dual Light PTZ')">Inquire</button>
          </div>
        </div>
      </div>

      <div class="product-card" data-tags="outdoor wifi ptz">
        <div class="product-img-wrap">
          <img src="/mnt/user-data/uploads/8.png" alt="Outdoor Standard PTZ">
          <div class="product-tag-badge">IP66</div>
        </div>
        <div class="product-body">
          <div class="product-cat">Outdoor · PTZ</div>
          <div class="product-name">Outdoor Standard PTZ</div>
          <div class="product-desc">Advanced perimeter security with dual-antenna WiFi, starlight night vision up to 100ft, IP66 weatherproofing.</div>
          <div class="product-feats">
            <span class="feat">IP66</span><span class="feat">Starlight</span><span class="feat">Dual Antenna</span>
          </div>
          <div class="product-foot">
            <div class="product-price">Inquire for price</div>
            <button class="btn-inq" onclick="openModal('Outdoor Standard PTZ Series')">Inquire</button>
          </div>
        </div>
      </div>

      <div class="product-card" data-tags="outdoor ptz">
        <div class="product-img-wrap">
          <img src="/mnt/user-data/uploads/9.png" alt="Outdoor Pro Wall-Mount PTZ">
          <div class="product-tag-badge">Pro Series</div>
        </div>
        <div class="product-body">
          <div class="product-cat">Outdoor · Pro PTZ</div>
          <div class="product-name">Pro Wall-Mount PTZ</div>
          <div class="product-desc">High-capacity exterior camera with AI human & vehicle detection, auto tracking, and ultra HD encryption.</div>
          <div class="product-feats">
            <span class="feat">Auto Track</span><span class="feat">Ultra HD</span><span class="feat">Encrypted</span>
          </div>
          <div class="product-foot">
            <div class="product-price">Inquire for price</div>
            <button class="btn-inq" onclick="openModal('Outdoor Pro Wall-Mount PTZ Series')">Inquire</button>
          </div>
        </div>
      </div>

      <div class="product-card" data-tags="indoor wifi ptz">
        <div class="product-img-wrap">
          <img src="/mnt/user-data/uploads/10.png" alt="Indoor HD Turret PT">
          <div class="product-tag-badge">Turret PT</div>
        </div>
        <div class="product-body">
          <div class="product-cat">Indoor · PTZ Turret</div>
          <div class="product-name">Indoor HD Turret PT</div>
          <div class="product-desc">Ceiling-mount turret with dual-band WiFi, AI detection, auto tracking, and encrypted UHD streaming.</div>
          <div class="product-feats">
            <span class="feat">Dual-Band</span><span class="feat">Auto Track</span><span class="feat">Encrypted</span>
          </div>
          <div class="product-foot">
            <div class="product-price">Inquire for price</div>
            <button class="btn-inq" onclick="openModal('Indoor HD Turret PT Series')">Inquire</button>
          </div>
        </div>
      </div>

      <div class="product-card" data-tags="outdoor wifi ptz">
        <div class="product-img-wrap">
          <img src="/mnt/user-data/uploads/11.png" alt="Outdoor Integrated Bracket PT">
          <div class="product-tag-badge">Dual Lens</div>
        </div>
        <div class="product-body">
          <div class="product-cat">Outdoor · PTZ</div>
          <div class="product-name">Integrated Bracket PT</div>
          <div class="product-desc">Dual-sensor exterior PTZ with auto smart tracking, active deterrence siren & light, full 360° outdoor coverage.</div>
          <div class="product-feats">
            <span class="feat">Dual Sensor</span><span class="feat">360° PTZ</span><span class="feat">Siren+Light</span>
          </div>
          <div class="product-foot">
            <div class="product-price">Inquire for price</div>
            <button class="btn-inq" onclick="openModal('Outdoor Integrated Bracket PT Series')">Inquire</button>
          </div>
        </div>
      </div>

      <div class="product-card" data-tags="indoor outdoor wifi">
        <div class="product-img-wrap">
          <img src="/mnt/user-data/uploads/13.png" alt="WiFi Camera Complete Line">
          <div class="product-tag-badge">Full Line</div>
        </div>
        <div class="product-body">
          <div class="product-cat">WiFi · Indoor & Outdoor</div>
          <div class="product-name">WiFi Camera Complete Line</div>
          <div class="product-desc">Full lineup: Hero H31, H3A/H5A, Hero A1, Hero D1, PICOO, and Pro Wall-Mount for total coverage.</div>
          <div class="product-feats">
            <span class="feat">6 Models</span><span class="feat">H.265+</span><span class="feat">App Access</span>
          </div>
          <div class="product-foot">
            <div class="product-price">Package Deals Available</div>
            <button class="btn-inq" onclick="openModal('WiFi Camera Package (Full Line)')">Inquire</button>
          </div>
        </div>
      </div>

    </div>
  </div>
</div>

<!-- SERVICES -->
<div class="section-wrap" id="services">
  <div class="tag">// Services</div>
  <div class="section-title">Installation & Support</div>
  <div class="section-sub">End-to-end security solutions — from site survey to post-installation maintenance.</div>
  <div class="services-grid">
    <div class="service-card">
      <div class="svc-num">01</div>
      <h3>Residential Installation</h3>
      <p>Complete home security setup with expert camera placement, cable management, and full mobile app configuration.</p>
      <div class="svc-tag">Homes · Condos · Lots</div>
    </div>
    <div class="service-card">
      <div class="svc-num">02</div>
      <h3>Commercial & Business</h3>
      <p>Enterprise-grade CCTV with NVR setup, perimeter protection, access control, and multi-site remote management.</p>
      <div class="svc-tag">Offices · Retail · Warehouses</div>
    </div>
    <div class="service-card">
      <div class="svc-num">03</div>
      <h3>Network & WiFi Setup</h3>
      <p>Ruijie Reyee networking solutions for high-speed, stable connectivity across all cameras and security devices.</p>
      <div class="svc-tag">LAN · WiFi · Structured Cabling</div>
    </div>
    <div class="service-card">
      <div class="svc-num">04</div>
      <h3>Maintenance & Repair</h3>
      <p>Preventive maintenance schedules, firmware updates, lens cleaning, and on-site repair to keep systems reliable.</p>
      <div class="svc-tag">Annual Contracts Available</div>
    </div>
    <div class="service-card">
      <div class="svc-num">05</div>
      <h3>Cloud Storage Setup</h3>
      <p>Configure secure cloud recording with easy remote playback — footage stays safe even if hardware is tampered with.</p>
      <div class="svc-tag">Remote Access · Easy Playback</div>
    </div>
    <div class="service-card">
      <div class="svc-num">06</div>
      <h3>Free Site Survey</h3>
      <p>Book a no-obligation on-site security assessment and get a customized camera placement plan and accurate quotation.</p>
      <div class="svc-tag">No Commitment · 100% Free</div>
    </div>
  </div>
</div>

<!-- WHY KSAP -->
<div class="why-section" id="whyus">
  <div class="why-inner">
    <div class="why-left">
      <div class="tag">// Why KSAP</div>
      <h2>Your Trusted Security Partner</h2>
      <p>We don't just sell cameras — we design complete security ecosystems tailored to your space, budget, and goals.</p>
      <div class="why-points">
        <div class="why-pt">
          <div class="why-pt-num">01</div>
          <div>
            <h4>Authorized Dealer</h4>
            <p>Official distributor of Dahua, Hikvision, Imou, Seagate, ZKTeco, and Ruijie Reyee — genuine products with full warranty.</p>
          </div>
        </div>
        <div class="why-pt">
          <div class="why-pt-num">02</div>
          <div>
            <h4>Certified Technicians</h4>
            <p>Years of hands-on experience in residential, commercial, and enterprise security deployments across the Philippines.</p>
          </div>
        </div>
        <div class="why-pt">
          <div class="why-pt-num">03</div>
          <div>
            <h4>After-Sales Support</h4>
            <p>We stay with you long after installation — remote assistance, on-site visits, and long-term maintenance contracts.</p>
          </div>
        </div>
        <div class="why-pt">
          <div class="why-pt-num">04</div>
          <div>
            <h4>Competitive Pricing</h4>
            <p>Best-value packages for every budget. Free site survey and transparent quote — no hidden charges.</p>
          </div>
        </div>
      </div>
      <div class="why-cta" style="margin-top:2.5rem;">
        <a href="#inquire" class="btn-white">Get a Free Quote</a>
      </div>
    </div>
    <div class="why-right">
      <div class="brand-mosaic">
        <div class="bm-card"><div class="bm-name">Dahua</div><div class="bm-desc">Technology</div></div>
        <div class="bm-card"><div class="bm-name">Hikvision</div><div class="bm-desc">Security Systems</div></div>
        <div class="bm-card"><div class="bm-name">Imou</div><div class="bm-desc">Smart Home</div></div>
        <div class="bm-card"><div class="bm-name">Seagate</div><div class="bm-desc">Storage Solutions</div></div>
        <div class="bm-card"><div class="bm-name">ZKTeco</div><div class="bm-desc">Access Control</div></div>
        <div class="bm-card"><div class="bm-name">Reyee</div><div class="bm-desc">Networking</div></div>
      </div>
    </div>
  </div>
</div>

<!-- CONTACT STRIP -->
<div class="contact-strip">
  <div class="contact-strip-inner">
    <div class="c-item">
      <div class="c-icon">📍</div>
      <div><div class="c-label">Location</div><div class="c-val">Metro Manila, Philippines</div></div>
    </div>
    <div class="c-item">
      <div class="c-icon">⏰</div>
      <div><div class="c-label">Business Hours</div><div class="c-val">Mon – Sat · 8AM to 6PM</div></div>
    </div>
    <div class="c-item">
      <div class="c-icon">🛡️</div>
      <div><div class="c-label">Warranty</div><div class="c-val">Official Manufacturer Warranty</div></div>
    </div>
    <div class="c-item">
      <div class="c-icon">🔍</div>
      <div><div class="c-label">Site Survey</div><div class="c-val">Free · No Commitment</div></div>
    </div>
  </div>
</div>

<!-- INQUIRE -->
<div class="inquire-section" id="inquire">
  <div class="inquire-inner">
    <div class="inq-left">
      <div class="tag">// Contact</div>
      <h2>Ready to Secure<br>Your Space?</h2>
      <p>Scan the QR code to reach us instantly via our preferred channel, or fill in the inquiry form and our team will get back to you within the day.</p>
      <div class="inq-qr">
        <img src="/mnt/user-data/uploads/699186744_1482693103653592_6541242170653532552_n.jpg" alt="KSAP QR Code">
        <div class="inq-qr-label">Scan to inquire now</div>
      </div>
    </div>
    <div class="inq-right">
      <h3>Send Us a Message</h3>
      <div class="form-row">
        <div class="form-group">
          <label>Full Name</label>
          <input type="text" placeholder="Juan dela Cruz">
        </div>
        <div class="form-group">
          <label>Contact Number</label>
          <input type="text" placeholder="+63 9XX XXX XXXX">
        </div>
      </div>
      <div class="form-group">
        <label>Location / Area</label>
        <input type="text" placeholder="e.g. Quezon City, Metro Manila">
      </div>
      <div class="form-group">
        <label>Inquiry Type</label>
        <select>
          <option>Product Purchase</option>
          <option>Installation Service</option>
          <option>Free Site Survey</option>
          <option>After-Sales / Repair</option>
          <option>General Inquiry</option>
        </select>
      </div>
      <div class="form-group">
        <label>Message</label>
        <textarea placeholder="Tell us about your security needs..."></textarea>
      </div>
      <button class="btn-submit" onclick="submitForm()">Send Inquiry →</button>
    </div>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-logo">
      <img src="/mnt/user-data/uploads/493187094_1176512570938315_1926001927982410807_n.jpg" alt="KSAP CCTV Solutions">
    </div>
    <div class="footer-links">
      <a href="#products">Products</a>
      <a href="#services">Services</a>
      <a href="#whyus">About</a>
      <a href="#inquire">Contact</a>
    </div>
  </div>
  <div class="footer-copy">© 2025 KSAP CCTV Solutions · Authorized Dahua Distributor · All rights reserved.</div>
</footer>

<!-- MODAL -->
<div class="modal-overlay" id="modalOverlay" onclick="closeOutside(event)">
  <div class="modal">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div class="modal-prod" id="modalProd">Product Inquiry</div>
    <h3>Get a Free Quote</h3>
    <div class="form-group" style="margin-top:1rem;">
      <label>Full Name</label>
      <input type="text" placeholder="Juan dela Cruz">
    </div>
    <div class="form-group">
      <label>Contact Number</label>
      <input type="text" placeholder="+63 9XX XXX XXXX">
    </div>
    <div class="form-group">
      <label>Location</label>
      <input type="text" placeholder="Quezon City, Metro Manila">
    </div>
    <div class="form-group">
      <label>Message</label>
      <textarea placeholder="Tell us more about your security needs..."></textarea>
    </div>
    <button class="btn-submit" onclick="submitModal()">Send Inquiry →</button>
  </div>
</div>

<script>
function openModal(product) {
  document.getElementById('modalProd').textContent = product || 'General Inquiry';
  document.getElementById('modalOverlay').classList.add('open');
  document.body.style.overflow = 'hidden';
}
function closeModal() {
  document.getElementById('modalOverlay').classList.remove('open');
  document.body.style.overflow = '';
}
function closeOutside(e) {
  if (e.target === document.getElementById('modalOverlay')) closeModal();
}
function submitModal() {
  alert('Thank you! Our KSAP team will contact you shortly. You may also scan our QR code for a faster response.');
  closeModal();
}
function submitForm() {
  alert('Thank you for reaching out! Our team will get back to you within the day.');
}
function filterProducts(tag, btn) {
  document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  document.querySelectorAll('.product-card').forEach(card => {
    card.style.display = (tag === 'all' || card.dataset.tags.includes(tag)) ? 'flex' : 'none';
  });
}
</script>
</body>
</html>
