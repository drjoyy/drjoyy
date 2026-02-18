[drjoy-personal-brand-site.html](https://github.com/user-attachments/files/25397681/drjoy-personal-brand-site.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dr. Joy — Your Smile Transformation Artist</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=DM+Sans:ital,wght@0,300;0,400;0,500;0,600;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #F5F0EB;
    --ivory: #FAF7F4;
    --warm-white: #FDFCFA;
    --sand: #E8DFD5;
    --rose-gold: #C4A68A;
    --deep-rose: #A67C5B;
    --charcoal: #2C2825;
    --warm-gray: #6B6462;
    --light-gray: #9B9490;
    --accent: #B8917A;
    --serif: 'Cormorant Garamond', Georgia, serif;
    --sans: 'DM Sans', -apple-system, sans-serif;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html {
    scroll-behavior: smooth;
    font-size: 16px;
  }

  body {
    font-family: var(--sans);
    background: var(--warm-white);
    color: var(--charcoal);
    overflow-x: hidden;
    -webkit-font-smoothing: antialiased;
  }

  /* ═══════════════════════════════════════════
     NAVIGATION
  ═══════════════════════════════════════════ */
  nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 100;
    padding: 1.5rem 3rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    background: rgba(253, 252, 250, 0.85);
  }

  nav.scrolled {
    padding: 1rem 3rem;
    box-shadow: 0 1px 0 rgba(44, 40, 37, 0.06);
  }

  .nav-brand {
    font-family: var(--serif);
    font-size: 1.4rem;
    font-weight: 400;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--charcoal);
    text-decoration: none;
  }

  .nav-brand span {
    font-weight: 300;
    font-style: italic;
    color: var(--deep-rose);
  }

  .nav-links {
    display: flex;
    gap: 2.5rem;
    align-items: center;
    list-style: none;
  }

  .nav-links a {
    font-family: var(--sans);
    font-size: 0.75rem;
    font-weight: 500;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--warm-gray);
    text-decoration: none;
    transition: color 0.3s ease;
  }

  .nav-links a:hover {
    color: var(--charcoal);
  }

  .nav-cta {
    font-family: var(--sans) !important;
    font-size: 0.7rem !important;
    font-weight: 500 !important;
    letter-spacing: 0.15em !important;
    text-transform: uppercase !important;
    color: var(--warm-white) !important;
    background: var(--charcoal);
    padding: 0.75rem 1.8rem;
    border-radius: 0;
    transition: all 0.3s ease;
  }

  .nav-cta:hover {
    background: var(--deep-rose) !important;
    color: var(--warm-white) !important;
  }

  /* ═══════════════════════════════════════════
     HERO
  ═══════════════════════════════════════════ */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 8rem 2rem 4rem;
    position: relative;
    background: var(--cream);
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: radial-gradient(ellipse at 30% 20%, rgba(196, 166, 138, 0.12) 0%, transparent 60%),
                radial-gradient(ellipse at 70% 80%, rgba(184, 145, 122, 0.08) 0%, transparent 50%);
    pointer-events: none;
  }

  .hero-eyebrow {
    font-family: var(--sans);
    font-size: 0.7rem;
    font-weight: 500;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 2rem;
    opacity: 0;
    animation: fadeUp 1s 0.3s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  }

  .hero h1 {
    font-family: var(--serif);
    font-size: clamp(3.5rem, 9vw, 7rem);
    font-weight: 300;
    line-height: 1.05;
    color: var(--charcoal);
    max-width: 900px;
    margin-bottom: 2rem;
    opacity: 0;
    animation: fadeUp 1s 0.5s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  }

  .hero h1 em {
    font-style: italic;
    font-weight: 400;
    color: var(--deep-rose);
  }

  .hero-sub {
    font-family: var(--sans);
    font-size: 1.1rem;
    font-weight: 300;
    color: var(--warm-gray);
    max-width: 520px;
    line-height: 1.7;
    margin-bottom: 3rem;
    opacity: 0;
    animation: fadeUp 1s 0.7s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  }

  .hero-cta-group {
    display: flex;
    gap: 1.5rem;
    align-items: center;
    opacity: 0;
    animation: fadeUp 1s 0.9s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  }

  .btn-primary {
    display: inline-block;
    font-family: var(--sans);
    font-size: 0.7rem;
    font-weight: 500;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--warm-white);
    background: var(--charcoal);
    padding: 1.1rem 2.8rem;
    text-decoration: none;
    transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
    position: relative;
    overflow: hidden;
  }

  .btn-primary:hover {
    background: var(--deep-rose);
    transform: translateY(-1px);
  }

  .btn-secondary {
    display: inline-block;
    font-family: var(--sans);
    font-size: 0.7rem;
    font-weight: 500;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--charcoal);
    text-decoration: none;
    padding: 1.1rem 0;
    border-bottom: 1px solid var(--charcoal);
    transition: all 0.3s ease;
  }

  .btn-secondary:hover {
    color: var(--deep-rose);
    border-color: var(--deep-rose);
  }

  .hero-scroll {
    position: absolute;
    bottom: 2.5rem;
    left: 50%;
    transform: translateX(-50%);
    opacity: 0;
    animation: fadeUp 1s 1.2s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  }

  .hero-scroll span {
    font-family: var(--sans);
    font-size: 0.6rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--light-gray);
    display: block;
    text-align: center;
  }

  .hero-scroll .line {
    width: 1px;
    height: 40px;
    background: var(--sand);
    margin: 0.8rem auto 0;
    position: relative;
    overflow: hidden;
  }

  .hero-scroll .line::after {
    content: '';
    position: absolute;
    top: -100%;
    left: 0;
    width: 100%;
    height: 100%;
    background: var(--accent);
    animation: scrollLine 2s infinite;
  }

  /* ═══════════════════════════════════════════
     TRANSFORMATION STORY
  ═══════════════════════════════════════════ */
  .transformation {
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: 100vh;
    overflow: hidden;
  }

  .transformation-image {
    background: var(--sand);
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .transformation-image-placeholder {
    width: 100%;
    height: 100%;
    min-height: 600px;
    background: linear-gradient(145deg, var(--sand) 0%, var(--rose-gold) 50%, var(--cream) 100%);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    position: relative;
  }

  .transformation-image-placeholder::after {
    content: '';
    position: absolute;
    inset: 2rem;
    border: 1px solid rgba(255,255,255,0.3);
  }

  .placeholder-text {
    font-family: var(--serif);
    font-size: 1.2rem;
    font-weight: 400;
    color: rgba(44, 40, 37, 0.4);
    letter-spacing: 0.1em;
    text-align: center;
  }

  .placeholder-sub {
    font-family: var(--sans);
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: rgba(44, 40, 37, 0.3);
  }

  .transformation-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 6rem 5rem;
    background: var(--warm-white);
  }

  .transformation-eyebrow {
    font-family: var(--sans);
    font-size: 0.65rem;
    font-weight: 500;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 2rem;
  }

  .transformation-content h2 {
    font-family: var(--serif);
    font-size: clamp(2.2rem, 4vw, 3.5rem);
    font-weight: 300;
    line-height: 1.15;
    color: var(--charcoal);
    margin-bottom: 2rem;
  }

  .transformation-content h2 em {
    font-style: italic;
    font-weight: 400;
    color: var(--deep-rose);
  }

  .transformation-content p {
    font-family: var(--sans);
    font-size: 0.95rem;
    font-weight: 300;
    line-height: 1.85;
    color: var(--warm-gray);
    margin-bottom: 1.5rem;
    max-width: 440px;
  }

  .transformation-signature {
    font-family: var(--serif);
    font-size: 1.6rem;
    font-weight: 400;
    font-style: italic;
    color: var(--deep-rose);
    margin-top: 1.5rem;
    margin-bottom: 2rem;
  }

  /* ═══════════════════════════════════════════
     PHILOSOPHY / APPROACH
  ═══════════════════════════════════════════ */
  .philosophy {
    padding: 8rem 3rem;
    background: var(--ivory);
    text-align: center;
  }

  .philosophy-eyebrow {
    font-family: var(--sans);
    font-size: 0.65rem;
    font-weight: 500;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 1.5rem;
  }

  .philosophy h2 {
    font-family: var(--serif);
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 300;
    color: var(--charcoal);
    margin-bottom: 1rem;
  }

  .philosophy-sub {
    font-family: var(--sans);
    font-size: 0.9rem;
    font-weight: 300;
    color: var(--warm-gray);
    max-width: 500px;
    margin: 0 auto 4rem;
    line-height: 1.7;
  }

  .philosophy-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    max-width: 1100px;
    margin: 0 auto;
    background: var(--sand);
  }

  .philosophy-card {
    background: var(--warm-white);
    padding: 4rem 3rem;
    text-align: center;
    transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
    position: relative;
  }

  .philosophy-card:hover {
    background: var(--cream);
  }

  .philosophy-number {
    font-family: var(--serif);
    font-size: 3rem;
    font-weight: 300;
    color: var(--sand);
    margin-bottom: 1.5rem;
    line-height: 1;
  }

  .philosophy-card h3 {
    font-family: var(--serif);
    font-size: 1.5rem;
    font-weight: 400;
    color: var(--charcoal);
    margin-bottom: 1rem;
    letter-spacing: 0.02em;
  }

  .philosophy-card p {
    font-family: var(--sans);
    font-size: 0.85rem;
    font-weight: 300;
    color: var(--warm-gray);
    line-height: 1.75;
    max-width: 280px;
    margin: 0 auto;
  }

  /* ═══════════════════════════════════════════
     SIGNATURE TRANSFORMATION
  ═══════════════════════════════════════════ */
  .signature {
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: 90vh;
    overflow: hidden;
  }

  .signature-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 6rem 5rem;
    background: var(--charcoal);
    color: var(--cream);
  }

  .signature-eyebrow {
    font-family: var(--sans);
    font-size: 0.65rem;
    font-weight: 500;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--rose-gold);
    margin-bottom: 2rem;
  }

  .signature-content h2 {
    font-family: var(--serif);
    font-size: clamp(2.2rem, 4vw, 3.5rem);
    font-weight: 300;
    line-height: 1.15;
    color: var(--cream);
    margin-bottom: 2rem;
  }

  .signature-content h2 em {
    font-style: italic;
    font-weight: 400;
    color: var(--rose-gold);
  }

  .signature-content p {
    font-family: var(--sans);
    font-size: 0.95rem;
    font-weight: 300;
    line-height: 1.85;
    color: var(--light-gray);
    margin-bottom: 1.5rem;
    max-width: 440px;
  }

  .signature-features {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    margin: 2rem 0 3rem;
  }

  .sig-feature {
    display: flex;
    align-items: flex-start;
    gap: 1rem;
  }

  .sig-feature-line {
    width: 24px;
    height: 1px;
    background: var(--rose-gold);
    margin-top: 0.7rem;
    flex-shrink: 0;
  }

  .sig-feature span {
    font-family: var(--sans);
    font-size: 0.85rem;
    font-weight: 300;
    color: var(--light-gray);
    line-height: 1.6;
  }

  .btn-light {
    display: inline-block;
    font-family: var(--sans);
    font-size: 0.7rem;
    font-weight: 500;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--charcoal);
    background: var(--cream);
    padding: 1.1rem 2.8rem;
    text-decoration: none;
    transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
    align-self: flex-start;
  }

  .btn-light:hover {
    background: var(--rose-gold);
    color: var(--warm-white);
  }

  .signature-image {
    background: var(--sand);
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .signature-image .transformation-image-placeholder {
    background: linear-gradient(160deg, var(--charcoal) 0%, var(--deep-rose) 50%, var(--rose-gold) 100%);
  }

  .signature-image .placeholder-text,
  .signature-image .placeholder-sub {
    color: rgba(245, 240, 235, 0.5);
  }

  .signature-image .transformation-image-placeholder::after {
    border-color: rgba(245, 240, 235, 0.15);
  }

  /* ═══════════════════════════════════════════
     PATIENT TRANSFORMATIONS
  ═══════════════════════════════════════════ */
  .results {
    padding: 8rem 3rem;
    background: var(--warm-white);
    text-align: center;
  }

  .results-eyebrow {
    font-family: var(--sans);
    font-size: 0.65rem;
    font-weight: 500;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 1.5rem;
  }

  .results h2 {
    font-family: var(--serif);
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 300;
    color: var(--charcoal);
    margin-bottom: 1rem;
  }

  .results-sub {
    font-family: var(--sans);
    font-size: 0.9rem;
    font-weight: 300;
    color: var(--warm-gray);
    max-width: 460px;
    margin: 0 auto 4rem;
    line-height: 1.7;
  }

  .results-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    max-width: 1000px;
    margin: 0 auto 4rem;
  }

  .result-card {
    aspect-ratio: 3/4;
    background: linear-gradient(145deg, var(--cream) 0%, var(--sand) 100%);
    position: relative;
    overflow: hidden;
    cursor: pointer;
    transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
  }

  .result-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 20px 60px rgba(44, 40, 37, 0.1);
  }

  .result-card-inner {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    padding: 2rem;
  }

  .result-card .placeholder-text {
    font-size: 0.9rem;
  }

  .result-label {
    position: absolute;
    bottom: 1.5rem;
    left: 1.5rem;
    font-family: var(--sans);
    font-size: 0.65rem;
    font-weight: 500;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--warm-gray);
  }

  /* Testimonial */
  .testimonial {
    max-width: 700px;
    margin: 0 auto;
    padding: 3rem 0;
    border-top: 1px solid var(--sand);
  }

  .testimonial blockquote {
    font-family: var(--serif);
    font-size: 1.4rem;
    font-weight: 300;
    font-style: italic;
    line-height: 1.6;
    color: var(--charcoal);
    margin-bottom: 1.5rem;
  }

  .testimonial cite {
    font-family: var(--sans);
    font-size: 0.75rem;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--light-gray);
    font-style: normal;
  }

  /* ═══════════════════════════════════════════
     WAYS TO WORK TOGETHER
  ═══════════════════════════════════════════ */
  .services {
    padding: 8rem 3rem;
    background: var(--cream);
  }

  .services-header {
    text-align: center;
    margin-bottom: 5rem;
  }

  .services-header h2 {
    font-family: var(--serif);
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 300;
    color: var(--charcoal);
  }

  .services-list {
    max-width: 900px;
    margin: 0 auto;
  }

  .service-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 2rem 0;
    border-bottom: 1px solid var(--sand);
    cursor: pointer;
    transition: all 0.3s ease;
  }

  .service-item:first-child {
    border-top: 1px solid var(--sand);
  }

  .service-item:hover {
    padding-left: 1rem;
  }

  .service-item:hover .service-name {
    color: var(--deep-rose);
  }

  .service-name {
    font-family: var(--serif);
    font-size: 1.4rem;
    font-weight: 400;
    color: var(--charcoal);
    transition: color 0.3s ease;
  }

  .service-desc {
    font-family: var(--sans);
    font-size: 0.8rem;
    font-weight: 300;
    color: var(--light-gray);
    letter-spacing: 0.05em;
    text-align: right;
    max-width: 300px;
  }

  .service-arrow {
    font-size: 1.2rem;
    color: var(--sand);
    transition: all 0.3s ease;
    margin-left: 1.5rem;
  }

  .service-item:hover .service-arrow {
    color: var(--deep-rose);
    transform: translateX(4px);
  }

  /* ═══════════════════════════════════════════
     WORK WITH ME CTA
  ═══════════════════════════════════════════ */
  .work-cta {
    padding: 8rem 3rem;
    background: var(--warm-white);
    text-align: center;
  }

  .work-card {
    max-width: 700px;
    margin: 0 auto;
    padding: 5rem 4rem;
    background: var(--cream);
    position: relative;
  }

  .work-card::before {
    content: '';
    position: absolute;
    inset: 1rem;
    border: 1px solid var(--sand);
    pointer-events: none;
  }

  .work-card h2 {
    font-family: var(--serif);
    font-size: clamp(1.8rem, 3.5vw, 2.8rem);
    font-weight: 300;
    color: var(--charcoal);
    margin-bottom: 1rem;
    line-height: 1.2;
  }

  .work-card h2 em {
    font-style: italic;
    font-weight: 400;
    color: var(--deep-rose);
  }

  .work-card p {
    font-family: var(--sans);
    font-size: 0.9rem;
    font-weight: 300;
    color: var(--warm-gray);
    margin-bottom: 2.5rem;
    line-height: 1.7;
  }

  /* ═══════════════════════════════════════════
     INVESTMENT & APPROACH FAQ
  ═══════════════════════════════════════════ */
  .faq {
    padding: 6rem 3rem;
    background: var(--ivory);
    max-width: 800px;
    margin: 0 auto;
  }

  .faq-container {
    background: var(--ivory);
    padding: 6rem 3rem;
  }

  .faq-header {
    text-align: center;
    margin-bottom: 3rem;
  }

  .faq-header h2 {
    font-family: var(--serif);
    font-size: 2rem;
    font-weight: 300;
    color: var(--charcoal);
  }

  .faq-item {
    border-bottom: 1px solid var(--sand);
    padding: 1.8rem 0;
  }

  .faq-item:first-child {
    border-top: 1px solid var(--sand);
  }

  .faq-question {
    font-family: var(--sans);
    font-size: 0.95rem;
    font-weight: 500;
    color: var(--charcoal);
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: color 0.3s ease;
  }

  .faq-question:hover {
    color: var(--deep-rose);
  }

  .faq-toggle {
    font-size: 1.2rem;
    color: var(--light-gray);
    transition: transform 0.3s ease;
  }

  .faq-item.active .faq-toggle {
    transform: rotate(45deg);
  }

  .faq-answer {
    font-family: var(--sans);
    font-size: 0.85rem;
    font-weight: 300;
    line-height: 1.8;
    color: var(--warm-gray);
    max-height: 0;
    overflow: hidden;
    transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
  }

  .faq-item.active .faq-answer {
    max-height: 200px;
    padding-top: 1rem;
  }

  /* ═══════════════════════════════════════════
     LOCATION & CONTACT
  ═══════════════════════════════════════════ */
  .location {
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: 50vh;
  }

  .location-map {
    background: var(--sand);
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 400px;
  }

  .location-map .placeholder-text {
    font-size: 0.9rem;
  }

  .location-info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 4rem 5rem;
    background: var(--warm-white);
  }

  .location-info h3 {
    font-family: var(--serif);
    font-size: 2rem;
    font-weight: 300;
    color: var(--charcoal);
    margin-bottom: 1.5rem;
  }

  .location-detail {
    font-family: var(--sans);
    font-size: 0.9rem;
    font-weight: 300;
    color: var(--warm-gray);
    line-height: 1.8;
    margin-bottom: 0.5rem;
  }

  .location-detail a {
    color: var(--deep-rose);
    text-decoration: none;
    transition: opacity 0.3s ease;
  }

  .location-detail a:hover {
    opacity: 0.7;
  }

  /* ═══════════════════════════════════════════
     FOOTER
  ═══════════════════════════════════════════ */
  footer {
    padding: 4rem 3rem;
    background: var(--charcoal);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-brand {
    font-family: var(--serif);
    font-size: 1rem;
    font-weight: 400;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--cream);
  }

  .footer-tagline {
    font-family: var(--serif);
    font-size: 0.9rem;
    font-weight: 300;
    font-style: italic;
    color: var(--rose-gold);
  }

  .footer-links {
    display: flex;
    gap: 2rem;
  }

  .footer-links a {
    font-family: var(--sans);
    font-size: 0.7rem;
    font-weight: 400;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--light-gray);
    text-decoration: none;
    transition: color 0.3s ease;
  }

  .footer-links a:hover {
    color: var(--cream);
  }

  /* ═══════════════════════════════════════════
     ANIMATIONS
  ═══════════════════════════════════════════ */
  @keyframes fadeUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @keyframes scrollLine {
    0% { top: -100%; }
    50% { top: 100%; }
    100% { top: 100%; }
  }

  .reveal {
    opacity: 0;
    transform: translateY(40px);
    transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
  }

  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* ═══════════════════════════════════════════
     RESPONSIVE
  ═══════════════════════════════════════════ */
  @media (max-width: 900px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    .transformation { grid-template-columns: 1fr; }
    .transformation-content { padding: 4rem 2rem; }
    .transformation-image-placeholder { min-height: 400px; }
    .signature { grid-template-columns: 1fr; }
    .signature-content { padding: 4rem 2rem; order: 1; }
    .signature-image { order: 2; min-height: 400px; }
    .philosophy-grid { grid-template-columns: 1fr; }
    .results-grid { grid-template-columns: 1fr; }
    .result-card { aspect-ratio: 4/3; }
    .location { grid-template-columns: 1fr; }
    .location-info { padding: 3rem 2rem; }
    .work-card { padding: 3rem 2rem; }
    footer { flex-direction: column; gap: 2rem; text-align: center; }
    .hero-cta-group { flex-direction: column; }
  }
</style>
</head>
<body>

<!-- ═══ NAVIGATION ═══ -->
<nav id="navbar">
  <a href="#" class="nav-brand">Dr <span>Joy</span></a>
  <ul class="nav-links">
    <li><a href="#story">My Story</a></li>
    <li><a href="#work">How I Work</a></li>
    <li><a href="#transformations">Transformations</a></li>
    <li><a href="#contact">Work With Me</a></li>
    <li><a href="https://calendly.com/mikenah-vega/30min" class="nav-cta" target="_blank">Book Consultation</a></li>
  </ul>
</nav>

<!-- ═══ HERO ═══ -->
<section class="hero">
  <div class="hero-eyebrow">Dr. Mikenah Joy Vega, DMD — Houston</div>
  <h1>I transform <em>lives</em><br>through smiles.</h1>
  <p class="hero-sub">I've rebuilt my own life from the inside out. Transformed my health, talked on stages, built practices from nothing. When you're ready for transformation that goes beyond just your teeth — this is where we begin.</p>
  <div class="hero-cta-group">
    <a href="https://calendly.com/mikenah-vega/30min" class="btn-primary" target="_blank">Start Your Transformation</a>
    <a href="#story" class="btn-secondary">My Story</a>
  </div>
  <div class="hero-scroll">
    <span>Scroll</span>
    <div class="line"></div>
  </div>
</section>

<!-- ═══ TRANSFORMATION STORY ═══ -->
<section class="transformation" id="story">
  <div class="transformation-image">
    <div class="transformation-image-placeholder">
      <span class="placeholder-text">Dr. Joy Transformation</span>
      <span class="placeholder-sub">Before/during/after photos</span>
    </div>
  </div>
  <div class="transformation-content">
    <div class="transformation-eyebrow reveal">The Journey</div>
    <h2 class="reveal">Transformation isn't just what I do. <em>It's who I am.</em></h2>
    <p class="reveal">I know what it feels like to hide. To avoid mirrors, photos, moments that should bring joy. To carry the weight of believing you're not worth the effort it would take to change.</p>
    <p class="reveal">But transformation taught me something: the person willing to rebuild themselves completely is the same person you want working on the parts of you that matter most.</p>
    <p class="reveal">Every smile I craft carries this understanding. Every patient who sits in my chair gets the version of care I wish I'd had when I was ready to risk everything for joy.</p>
    <div class="transformation-signature reveal">— Dr. Joy</div>
    <a href="https://calendly.com/mikenah-vega/30min" class="btn-primary reveal" target="_blank">Let's Talk</a>
  </div>
</section>

<!-- ═══ PHILOSOPHY ═══ -->
<section class="philosophy">
  <div class="philosophy-eyebrow reveal">My Approach</div>
  <h2 class="reveal">How I work with you</h2>
  <p class="philosophy-sub reveal">Transformation requires trust. Trust requires understanding exactly what we're building together.</p>
  <div class="philosophy-grid">
    <div class="philosophy-card reveal">
      <div class="philosophy-number">01</div>
      <h3>We Start with Why</h3>
      <p>What do you want to feel when you see yourself? How do you want to move through the world? The technical work follows the emotional vision.</p>
    </div>
    <div class="philosophy-card reveal">
      <div class="philosophy-number">02</div>
      <h3>Precision in Everything</h3>
      <p>From the first consultation to the final result — every detail is considered, every material chosen with intention, every outcome planned in advance.</p>
    </div>
    <div class="philosophy-card reveal">
      <div class="philosophy-number">03</div>
      <h3>You're Never Alone</h3>
      <p>This is your transformation journey, but you don't walk it alone. I'm here for every question, every concern, every moment you need reassurance.</p>
    </div>
  </div>
</section>

<!-- ═══ SIGNATURE TRANSFORMATION ═══ -->
<section class="signature">
  <div class="signature-content">
    <div class="signature-eyebrow reveal">Signature Work</div>
    <h2 class="reveal">The Complete<br><em>Life</em> Transformation</h2>
    <p class="reveal">This isn't just cosmetic dentistry. It's the intersection of Invisalign precision, porcelain artistry, and the deep work of helping someone fall in love with their reflection for the first time.</p>
    <div class="signature-features">
      <div class="sig-feature reveal">
        <div class="sig-feature-line"></div>
        <span>3D smile preview — see your new life before we begin</span>
      </div>
      <div class="sig-feature reveal">
        <div class="sig-feature-line"></div>
        <span>Structural + aesthetic transformation in one comprehensive journey</span>
      </div>
      <div class="sig-feature reveal">
        <div class="sig-feature-line"></div>
        <span>Ongoing support through every phase of your transformation</span>
      </div>
    </div>
    <a href="https://calendly.com/mikenah-vega/30min" class="btn-light reveal" target="_blank">Begin Your Journey</a>
  </div>
  <div class="signature-image">
    <div class="transformation-image-placeholder">
      <span class="placeholder-text">Complete Transformation</span>
      <span class="placeholder-sub">Patient smile journey</span>
    </div>
  </div>
</section>

<!-- ═══ PATIENT TRANSFORMATIONS ═══ -->
<section class="results" id="transformations">
  <div class="results-eyebrow reveal">The Work</div>
  <h2 class="reveal">Patient transformations</h2>
  <p class="results-sub reveal">These are the moments that make everything worth it — when someone sees themselves the way I've seen them all along.</p>
  <div class="results-grid">
    <div class="result-card reveal">
      <div class="result-card-inner">
        <span class="placeholder-text">Sarah's Journey</span>
        <span class="placeholder-sub">Complete transformation</span>
      </div>
      <div class="result-label">Full Life Makeover</div>
    </div>
    <div class="result-card reveal">
      <div class="result-card-inner">
        <span class="placeholder-text">Maria's Story</span>
        <span class="placeholder-sub">Confidence rebuilt</span>
      </div>
      <div class="result-label">Porcelain Artistry</div>
    </div>
    <div class="result-card reveal">
      <div class="result-card-inner">
        <span class="placeholder-text">James' Path</span>
        <span class="placeholder-sub">Professional confidence</span>
      </div>
      <div class="result-label">Invisalign + Veneers</div>
    </div>
  </div>
  <div class="testimonial reveal">
    <blockquote>"Dr. Joy didn't just transform my smile — she gave me permission to take up space in rooms where I used to hide."</blockquote>
    <cite>— Sarah M., Complete Transformation Patient</cite>
  </div>
</section>

<!-- ═══ WAYS TO WORK TOGETHER ═══ -->
<section class="services" id="work">
  <div class="services-header">
    <div class="philosophy-eyebrow reveal">Ways We Can Work</div>
    <h2 class="reveal">How I can help you</h2>
  </div>
  <div class="services-list">
    <div class="service-item reveal">
      <div>
        <div class="service-name">Complete Smile Transformation</div>
      </div>
      <div style="display:flex;align-items:center;">
        <div class="service-desc">The full journey — Invisalign, veneers, confidence coaching</div>
        <span class="service-arrow">→</span>
      </div>
    </div>
    <div class="service-item reveal">
      <div>
        <div class="service-name">Invisalign with Intention</div>
      </div>
      <div style="display:flex;align-items:center;">
        <div class="service-desc">Straightening that aligns with who you're becoming</div>
        <span class="service-arrow">→</span>
      </div>
    </div>
    <div class="service-item reveal">
      <div>
        <div class="service-name">Porcelain Artistry</div>
      </div>
      <div style="display:flex;align-items:center;">
        <div class="service-desc">Custom veneers designed for your unique story</div>
        <span class="service-arrow">→</span>
      </div>
    </div>
    <div class="service-item reveal">
      <div>
        <div class="service-name">Confidence Restoration</div>
      </div>
      <div style="display:flex;align-items:center;">
        <div class="service-desc">Rebuilding what time or life has worn away</div>
        <span class="service-arrow">→</span>
      </div>
    </div>
    <div class="service-item reveal">
      <div>
        <div class="service-name">Smile Preview Session</div>
      </div>
      <div style="display:flex;align-items:center;">
        <div class="service-desc">See your transformation before you commit</div>
        <span class="service-arrow">→</span>
      </div>
    </div>
  </div>
</section>

<!-- ═══ WORK WITH ME CTA ═══ -->
<section class="work-cta">
  <div class="work-card reveal">
    <div class="philosophy-eyebrow">Ready?</div>
    <h2>Your transformation <em>starts</em> now.</h2>
    <p>The version of yourself you've been imagining doesn't have to stay imaginary. Let's talk about what's possible when you decide your smile — and your confidence — are worth the investment.</p>
    <a href="https://calendly.com/mikenah-vega/30min" class="btn-primary" target="_blank">Book Your Consultation</a>
  </div>
</section>

<!-- ═══ INVESTMENT & APPROACH FAQ ═══ -->
<div class="faq-container">
  <div class="faq" style="background:transparent;">
    <div class="faq-header">
      <div class="philosophy-eyebrow reveal">Investment & Approach</div>
      <h2 class="reveal">Working together</h2>
    </div>
    <div class="faq-item reveal">
      <div class="faq-question" onclick="toggleFaq(this)">
        <span>How do you approach investment and insurance?</span>
        <span class="faq-toggle">+</span>
      </div>
      <div class="faq-answer">I work outside insurance networks — which means your transformation isn't limited by what an insurance company thinks your smile is worth. We focus on the result you want, then find a way to make it happen.</div>
    </div>
    <div class="faq-item reveal">
      <div class="faq-question" onclick="toggleFaq(this)">
        <span>Can I use my insurance benefits?</span>
        <span class="faq-toggle">+</span>
      </div>
      <div class="faq-answer">Absolutely. Think of insurance as a contribution toward your investment. I handle all the paperwork, and any reimbursement comes directly to you — seamless and stress-free.</div>
    </div>
    <div class="faq-item reveal">
      <div class="faq-question" onclick="toggleFaq(this)">
        <span>How do I know what this will cost?</span>
        <span class="faq-toggle">+</span>
      </div>
      <div class="faq-answer">Complete transparency, always. After we design your transformation together, you'll know exactly what the investment is before making any commitments. No surprises, no pressure.</div>
    </div>
    <div class="faq-item reveal">
      <div class="faq-question" onclick="toggleFaq(this)">
        <span>What makes working with you different?</span>
        <span class="faq-toggle">+</span>
      </div>
      <div class="faq-answer">I'm not just your dentist — I'm someone who understands transformation from the inside out. You get clinical excellence combined with genuine understanding of what it takes to become who you're meant to be.</div>
    </div>
  </div>
</div>

<!-- ═══ LOCATION & CONTACT ═══ -->
<section class="location" id="contact">
  <div class="location-map">
    <div style="display:flex;flex-direction:column;align-items:center;gap:0.5rem;">
      <span class="placeholder-text">Map Embed</span>
      <span class="placeholder-sub">Houston Location</span>
    </div>
  </div>
  <div class="location-info">
    <div class="transformation-eyebrow reveal" style="margin-bottom:1.5rem;">Work With Me</div>
    <h3 class="reveal">Houston, Texas</h3>
    <p class="location-detail reveal">2202 Waugh Dr, Houston, TX 77006</p>
    <p class="location-detail reveal">In the heart of Montrose — where transformation happens.</p>
    <p class="location-detail reveal" style="margin-top:1rem;"><a href="tel:+17135213131">(713) 521-3131</a>&nbsp;&nbsp;·&nbsp;&nbsp;Call or Text</p>
    <a href="https://calendly.com/mikenah-vega/30min" class="btn-primary reveal" style="margin-top:2rem;" target="_blank">Start Your Transformation</a>
  </div>
</section>

<!-- ═══ FOOTER ═══ -->
<footer>
  <div>
    <div class="footer-brand">Dr Joy</div>
    <div class="footer-tagline" style="margin-top:0.5rem;">Risk everything for joy.</div>
  </div>
  <div class="footer-links">
    <a href="https://www.instagram.com/drjoyy" target="_blank">Instagram</a>
    <a href="tel:+17135213131">Call</a>
    <a href="https://calendly.com/mikenah-vega/30min" target="_blank">Work Together</a>
  </div>
</footer>

<script>
  // Nav scroll effect
  const navbar = document.getElementById('navbar');
  window.addEventListener('scroll', () => {
    navbar.classList.toggle('scrolled', window.scrollY > 50);
  });

  // Reveal on scroll
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, index) => {
      if (entry.isIntersecting) {
        setTimeout(() => {
          entry.target.classList.add('visible');
        }, index * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1, rootMargin: '0px 0px -50px 0px' });

  reveals.forEach(el => observer.observe(el));

  // FAQ toggle
  function toggleFaq(el) {
    const item = el.parentElement;
    const isActive = item.classList.contains('active');
    document.querySelectorAll('.faq-item').forEach(i => i.classList.remove('active'));
    if (!isActive) item.classList.add('active');
  }

  // Smooth scroll for anchor links
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if (target) {
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });
</script>

</body>
</html>
