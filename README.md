<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Say Fontina — Premium Italian & Mediterranean Dining, Noida</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;0,900;1,400;1,700&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400;1,500&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet" />
<style>
  :root {
    --black: #0F0F0F;
    --charcoal: #1A1A1A;
    --gold: #C9A84C;
    --gold-light: #E2C270;
    --gold-dark: #9E7A2C;
    --cream: #F5F1E8;
    --cream-dim: #D8D2C4;
    --white: #FFFFFF;
    --glass-bg: rgba(255,255,255,0.04);
    --glass-border: rgba(201,168,76,0.18);
    --glass-hover: rgba(201,168,76,0.08);
    --shadow-gold: 0 8px 40px rgba(201,168,76,0.12);
    --shadow-deep: 0 20px 80px rgba(0,0,0,0.6);
    --radius: 2px;
    --transition: 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; font-size: 16px; }

  body {
    background: var(--black);
    color: var(--cream);
    font-family: 'Poppins', sans-serif;
    font-weight: 300;
    line-height: 1.7;
    overflow-x: hidden;
    cursor: default;
  }

  /* ─── Custom Scrollbar ─── */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: var(--black); }
  ::-webkit-scrollbar-thumb { background: var(--gold-dark); border-radius: 2px; }

  /* ─── Selection ─── */
  ::selection { background: var(--gold); color: var(--black); }

  /* ─── NAVBAR ─── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
    padding: 0 6vw;
    display: flex; align-items: center; justify-content: space-between;
    height: 80px;
    transition: all var(--transition);
  }
  nav.scrolled {
    background: rgba(10,10,10,0.92);
    backdrop-filter: blur(24px);
    -webkit-backdrop-filter: blur(24px);
    border-bottom: 1px solid var(--glass-border);
    height: 64px;
    box-shadow: 0 4px 40px rgba(0,0,0,0.4);
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem;
    font-weight: 700;
    color: var(--gold);
    letter-spacing: 0.08em;
    text-decoration: none;
    display: flex; align-items: center; gap: 10px;
  }
  .nav-logo span {
    display: inline-block;
    width: 36px; height: 36px;
    border: 1.5px solid var(--gold);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 0.7rem; letter-spacing: 0.05em;
    color: var(--gold); font-family: 'Poppins', sans-serif;
    font-weight: 400;
    flex-shrink: 0;
  }
  .nav-links {
    display: flex; align-items: center; gap: 2.4rem;
    list-style: none;
  }
  .nav-links a {
    text-decoration: none;
    font-family: 'Poppins', sans-serif;
    font-size: 0.72rem;
    font-weight: 400;
    color: var(--cream-dim);
    letter-spacing: 0.18em;
    text-transform: uppercase;
    transition: color var(--transition);
    position: relative;
  }
  .nav-links a::after {
    content: ''; position: absolute; bottom: -4px; left: 0;
    width: 0; height: 1px; background: var(--gold);
    transition: width var(--transition);
  }
  .nav-links a:hover { color: var(--gold); }
  .nav-links a:hover::after { width: 100%; }
  .nav-reserve-btn {
    background: transparent;
    border: 1px solid var(--gold);
    color: var(--gold) !important;
    padding: 8px 20px !important;
    letter-spacing: 0.16em !important;
    transition: all var(--transition) !important;
  }
  .nav-reserve-btn::after { display: none !important; }
  .nav-reserve-btn:hover {
    background: var(--gold) !important;
    color: var(--black) !important;
  }
  .hamburger {
    display: none;
    flex-direction: column; gap: 5px; cursor: pointer;
    background: none; border: none; padding: 4px;
  }
  .hamburger span {
    display: block; width: 24px; height: 1.5px;
    background: var(--gold); transition: all var(--transition);
  }
  .mobile-menu {
    display: none; position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    background: rgba(10,10,10,0.98);
    backdrop-filter: blur(30px);
    z-index: 999;
    flex-direction: column; align-items: center; justify-content: center;
    gap: 2.4rem;
  }
  .mobile-menu.open { display: flex; }
  .mobile-menu a {
    font-family: 'Playfair Display', serif;
    font-size: 2rem; color: var(--cream);
    text-decoration: none; letter-spacing: 0.04em;
    transition: color var(--transition);
  }
  .mobile-menu a:hover { color: var(--gold); }
  .mobile-close {
    position: absolute; top: 24px; right: 6vw;
    background: none; border: none; color: var(--gold);
    font-size: 1.8rem; cursor: pointer;
  }

  /* ─── HERO ─── */
  #hero {
    position: relative; min-height: 100vh;
    display: flex; align-items: center; justify-content: center;
    overflow: hidden;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background-image:
      linear-gradient(to bottom, rgba(10,10,10,0.35) 0%, rgba(10,10,10,0.55) 50%, rgba(10,10,10,0.88) 100%),
      url('https://images.unsplash.com/photo-1555396273-367ea4eb4db5?w=1800&q=80&auto=format&fit=crop');
    background-size: cover;
    background-position: center;
    transform: scale(1.06);
    transition: transform 12s ease-out;
  }
  #hero.loaded .hero-bg { transform: scale(1); }
  .hero-grain {
    position: absolute; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none; opacity: 0.5;
  }
  .hero-content {
    position: relative; z-index: 2;
    text-align: center; padding: 0 6vw;
    max-width: 880px;
    opacity: 0; transform: translateY(30px);
    animation: heroReveal 1.4s cubic-bezier(0.16, 1, 0.3, 1) 0.4s forwards;
  }
  @keyframes heroReveal {
    to { opacity: 1; transform: translateY(0); }
  }
  .hero-eyebrow {
    font-family: 'Poppins', sans-serif;
    font-size: 0.68rem; font-weight: 400;
    letter-spacing: 0.35em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 1.4rem;
    display: flex; align-items: center; justify-content: center; gap: 16px;
  }
  .hero-eyebrow::before, .hero-eyebrow::after {
    content: ''; flex: 1; max-width: 60px;
    height: 1px; background: var(--gold-dark);
  }
  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3.8rem, 9vw, 8rem);
    font-weight: 700; line-height: 0.92;
    color: var(--cream); letter-spacing: -0.01em;
    margin-bottom: 0.2em;
  }
  .hero-title em {
    font-style: italic; color: var(--gold);
    font-weight: 400;
  }
  .hero-subtitle {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.1rem, 2.5vw, 1.5rem);
    font-style: italic; font-weight: 300;
    color: var(--cream-dim); margin: 1.4rem 0 2.4rem;
    letter-spacing: 0.04em;
  }
  .hero-divider {
    width: 60px; height: 1px;
    background: linear-gradient(to right, transparent, var(--gold), transparent);
    margin: 0 auto 2.4rem;
  }
  .hero-cta {
    display: flex; align-items: center; justify-content: center;
    gap: 1.2rem; flex-wrap: wrap;
  }
  .btn-primary {
    background: var(--gold);
    color: var(--black);
    border: none; padding: 14px 36px;
    font-family: 'Poppins', sans-serif;
    font-size: 0.72rem; font-weight: 600;
    letter-spacing: 0.2em; text-transform: uppercase;
    cursor: pointer; text-decoration: none;
    display: inline-flex; align-items: center; gap: 10px;
    transition: all var(--transition);
    position: relative; overflow: hidden;
  }
  .btn-primary::before {
    content: ''; position: absolute; inset: 0;
    background: var(--gold-light);
    transform: scaleX(0); transform-origin: left;
    transition: transform var(--transition);
  }
  .btn-primary:hover::before { transform: scaleX(1); }
  .btn-primary span { position: relative; z-index: 1; }
  .btn-primary:hover { box-shadow: 0 8px 32px rgba(201,168,76,0.35); transform: translateY(-2px); }
  .btn-outline {
    background: transparent;
    color: var(--cream);
    border: 1px solid rgba(245,241,232,0.4);
    padding: 14px 36px;
    font-family: 'Poppins', sans-serif;
    font-size: 0.72rem; font-weight: 400;
    letter-spacing: 0.2em; text-transform: uppercase;
    cursor: pointer; text-decoration: none;
    display: inline-flex; align-items: center; gap: 10px;
    transition: all var(--transition);
  }
  .btn-outline:hover {
    border-color: var(--gold); color: var(--gold);
    background: rgba(201,168,76,0.06);
    transform: translateY(-2px);
  }
  .hero-scroll {
    position: absolute; bottom: 40px; left: 50%;
    transform: translateX(-50%);
    display: flex; flex-direction: column; align-items: center; gap: 8px;
    z-index: 2;
    opacity: 0; animation: fadeIn 1s 1.8s forwards;
  }
  @keyframes fadeIn { to { opacity: 1; } }
  .hero-scroll span {
    font-size: 0.6rem; letter-spacing: 0.3em; text-transform: uppercase;
    color: var(--gold); font-family: 'Poppins', sans-serif; font-weight: 400;
  }
  .scroll-line {
    width: 1px; height: 48px;
    background: linear-gradient(to bottom, var(--gold), transparent);
    animation: scrollPulse 2s ease-in-out infinite;
  }
  @keyframes scrollPulse {
    0%, 100% { opacity: 0.4; } 50% { opacity: 1; }
  }

  /* ─── SECTION COMMONS ─── */
  section { padding: 120px 6vw; }
  .section-label {
    font-family: 'Poppins', sans-serif;
    font-size: 0.65rem; font-weight: 400;
    letter-spacing: 0.4em; text-transform: uppercase;
    color: var(--gold); display: flex; align-items: center; gap: 14px;
    margin-bottom: 1rem;
  }
  .section-label::before {
    content: ''; width: 32px; height: 1px; background: var(--gold);
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.2rem, 5vw, 3.8rem);
    font-weight: 700; line-height: 1.1;
    color: var(--cream); margin-bottom: 1.2rem;
  }
  .section-title em { font-style: italic; color: var(--gold); }
  .section-body {
    font-family: 'Poppins', sans-serif;
    font-size: 0.9rem; font-weight: 300;
    color: var(--cream-dim); line-height: 1.9;
    max-width: 600px;
  }
  .gold-rule {
    width: 50px; height: 1px;
    background: var(--gold); margin: 1.4rem 0;
  }

  /* ─── REVEAL ANIMATION ─── */
  .reveal {
    opacity: 0; transform: translateY(40px);
    transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1),
                transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }
  .reveal-delay-1 { transition-delay: 0.1s; }
  .reveal-delay-2 { transition-delay: 0.2s; }
  .reveal-delay-3 { transition-delay: 0.3s; }
  .reveal-delay-4 { transition-delay: 0.4s; }

  /* ─── ABOUT ─── */
  #about { background: var(--charcoal); }
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 6rem; align-items: center;
    max-width: 1200px; margin: 0 auto;
  }
  .about-image-wrap {
    position: relative;
  }
  .about-image {
    width: 100%; aspect-ratio: 4/5;
    object-fit: cover;
    display: block;
  }
  .about-image-frame {
    position: absolute; inset: -16px;
    border: 1px solid var(--glass-border);
    pointer-events: none; z-index: 0;
  }
  .about-image-wrap > img { position: relative; z-index: 1; }
  .about-badge {
    position: absolute; bottom: -20px; right: -20px; z-index: 2;
    background: var(--gold);
    color: var(--black);
    padding: 20px 24px;
    text-align: center;
  }
  .about-badge .num {
    font-family: 'Playfair Display', serif;
    font-size: 2.2rem; font-weight: 700;
    display: block; line-height: 1;
  }
  .about-badge .label {
    font-family: 'Poppins', sans-serif;
    font-size: 0.6rem; font-weight: 500;
    letter-spacing: 0.15em; text-transform: uppercase;
    display: block; margin-top: 4px;
  }
  .about-stats {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 1px; margin-top: 3rem;
    background: var(--glass-border);
  }
  .stat-item {
    background: var(--charcoal);
    padding: 1.6rem;
  }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem; font-weight: 700;
    color: var(--gold); line-height: 1;
  }
  .stat-text {
    font-family: 'Poppins', sans-serif;
    font-size: 0.72rem; font-weight: 300;
    color: var(--cream-dim); margin-top: 6px;
    letter-spacing: 0.06em;
  }

  /* ─── DISHES ─── */
  #dishes { background: var(--black); }
  .dishes-header {
    max-width: 1200px; margin: 0 auto 4rem;
    display: flex; justify-content: space-between; align-items: flex-end;
    flex-wrap: wrap; gap: 2rem;
  }
  .dishes-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    max-width: 1200px; margin: 0 auto;
  }
  .dish-card {
    position: relative; overflow: hidden;
    background: var(--charcoal);
    border: 1px solid var(--glass-border);
    cursor: pointer;
    transition: all var(--transition);
    group: true;
  }
  .dish-card:hover {
    border-color: var(--gold);
    box-shadow: var(--shadow-gold);
    transform: translateY(-6px);
  }
  .dish-card:first-child {
    grid-column: span 2;
  }
  .dish-img {
    width: 100%; height: 260px;
    object-fit: cover;
    transition: transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
    display: block;
  }
  .dish-card:first-child .dish-img { height: 340px; }
  .dish-card:hover .dish-img { transform: scale(1.06); }
  .dish-overlay {
    position: absolute; inset: 0;
    background: linear-gradient(to top, rgba(10,10,10,0.92) 0%, rgba(10,10,10,0.1) 60%, transparent 100%);
    opacity: 0; transition: opacity var(--transition);
  }
  .dish-card:hover .dish-overlay { opacity: 1; }
  .dish-info {
    padding: 1.4rem 1.6rem 1.6rem;
  }
  .dish-category {
    font-family: 'Poppins', sans-serif;
    font-size: 0.6rem; letter-spacing: 0.3em;
    text-transform: uppercase; color: var(--gold);
    margin-bottom: 0.5rem;
  }
  .dish-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem; font-weight: 600;
    color: var(--cream); margin-bottom: 0.5rem;
    line-height: 1.3;
  }
  .dish-desc {
    font-family: 'Poppins', sans-serif;
    font-size: 0.78rem; font-weight: 300;
    color: var(--cream-dim); line-height: 1.7;
  }
  .dish-arrow {
    display: inline-flex; align-items: center; gap: 8px;
    margin-top: 1rem;
    font-family: 'Poppins', sans-serif;
    font-size: 0.65rem; font-weight: 400;
    letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--gold); text-decoration: none;
    transition: gap var(--transition);
  }
  .dish-card:hover .dish-arrow { gap: 14px; }

  /* ─── CUISINE ─── */
  #cuisine {
    background: linear-gradient(to bottom, var(--charcoal), var(--black));
    text-align: center;
  }
  .cuisine-header { max-width: 600px; margin: 0 auto 4rem; }
  .cuisine-header .section-label { justify-content: center; }
  .cuisine-header .section-label::before { display: none; }
  .cuisine-grid {
    display: flex; flex-wrap: wrap;
    gap: 1rem; justify-content: center;
    max-width: 1000px; margin: 0 auto;
  }
  .cuisine-card {
    flex: 0 0 auto;
    padding: 2rem 2.4rem;
    border: 1px solid var(--glass-border);
    background: var(--glass-bg);
    backdrop-filter: blur(12px);
    display: flex; flex-direction: column; align-items: center; gap: 1rem;
    transition: all var(--transition);
    cursor: default; min-width: 160px;
  }
  .cuisine-card:hover {
    border-color: var(--gold);
    background: var(--glass-hover);
    transform: translateY(-4px);
    box-shadow: var(--shadow-gold);
  }
  .cuisine-icon {
    font-size: 2.2rem; line-height: 1;
    filter: saturate(0.8);
  }
  .cuisine-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1rem; font-weight: 500;
    color: var(--cream); letter-spacing: 0.04em;
    text-align: center;
  }

  /* ─── REVIEWS ─── */
  #reviews { background: var(--black); }
  .reviews-layout {
    max-width: 1200px; margin: 0 auto;
    display: grid; grid-template-columns: 1fr 1.6fr; gap: 6rem;
    align-items: start;
  }
  .rating-platforms {
    display: flex; flex-direction: column; gap: 1rem;
  }
  .platform-card {
    display: flex; align-items: center;
    gap: 1.4rem; padding: 1.4rem 1.8rem;
    border: 1px solid var(--glass-border);
    background: var(--glass-bg);
    transition: all var(--transition);
  }
  .platform-card:hover {
    border-color: var(--gold);
    background: var(--glass-hover);
    transform: translateX(4px);
  }
  .platform-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1rem; font-weight: 700;
    color: var(--gold); min-width: 80px;
  }
  .platform-stars {
    display: flex; gap: 3px;
  }
  .star {
    color: var(--gold); font-size: 0.85rem;
    line-height: 1;
  }
  .star.half { opacity: 0.5; }
  .platform-score {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem; font-weight: 700;
    color: var(--cream); margin-left: auto;
  }
  .platform-reviews {
    font-family: 'Poppins', sans-serif;
    font-size: 0.65rem; color: var(--cream-dim);
    letter-spacing: 0.06em;
  }
  .testimonials { display: flex; flex-direction: column; gap: 1.5rem; }
  .testimonial-card {
    padding: 2rem 2.2rem;
    border: 1px solid var(--glass-border);
    background: var(--glass-bg);
    position: relative;
    transition: all var(--transition);
  }
  .testimonial-card:hover {
    border-color: var(--glass-border);
    background: rgba(255,255,255,0.06);
  }
  .testimonial-card::before {
    content: '"';
    position: absolute; top: 1rem; right: 1.6rem;
    font-family: 'Playfair Display', serif;
    font-size: 5rem; color: var(--gold);
    opacity: 0.15; line-height: 1;
    pointer-events: none;
  }
  .testimonial-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.08rem; font-style: italic;
    color: var(--cream); line-height: 1.8;
    margin-bottom: 1.2rem;
  }
  .testimonial-meta {
    display: flex; align-items: center; gap: 1rem;
  }
  .reviewer-name {
    font-family: 'Poppins', sans-serif;
    font-size: 0.75rem; font-weight: 500;
    color: var(--gold); letter-spacing: 0.08em;
  }
  .reviewer-platform {
    font-family: 'Poppins', sans-serif;
    font-size: 0.65rem; color: var(--cream-dim);
    letter-spacing: 0.06em;
  }
  .meta-divider { color: var(--gold-dark); font-size: 0.5rem; }

  /* ─── LOCATION ─── */
  #location {
    background: var(--charcoal);
  }
  .location-grid {
    display: grid; grid-template-columns: 1fr 1.2fr;
    gap: 4rem; align-items: start;
    max-width: 1200px; margin: 0 auto;
  }
  .location-info { }
  .location-detail {
    display: flex; gap: 1.2rem;
    align-items: flex-start;
    padding: 1.4rem 0;
    border-bottom: 1px solid var(--glass-border);
  }
  .location-detail:last-of-type { border-bottom: none; }
  .loc-icon {
    width: 40px; height: 40px; flex-shrink: 0;
    border: 1px solid var(--gold-dark);
    display: flex; align-items: center; justify-content: center;
    color: var(--gold); font-size: 1rem;
  }
  .loc-label {
    font-family: 'Poppins', sans-serif;
    font-size: 0.62rem; letter-spacing: 0.25em;
    text-transform: uppercase; color: var(--gold);
    margin-bottom: 0.3rem; display: block;
  }
  .loc-value {
    font-family: 'Poppins', sans-serif;
    font-size: 0.85rem; font-weight: 300;
    color: var(--cream); line-height: 1.6;
  }
  .map-embed {
    width: 100%; aspect-ratio: 4/3;
    border: 1px solid var(--glass-border);
    overflow: hidden; position: relative;
  }
  .map-embed iframe {
    width: 100%; height: 100%;
    filter: grayscale(0.7) invert(0.85) hue-rotate(200deg) brightness(0.8);
    border: none;
  
