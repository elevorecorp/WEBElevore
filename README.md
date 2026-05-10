<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Elevore Premium Services — Elite cleaning and handyman services in Orlando, FL. Precision. Speed. Results.">
<title>ELEVORE — Premium Property Services</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Barlow:ital,wght@0,400;0,600;0,700;1,900&family=Barlow+Condensed:wght@300;700;900&display=swap" rel="stylesheet">
<style>
:root {
  --gold: #fbbf24;
  --gold-dark: #d97706;
  --green: #22c55e;
  --black: #000000;
  --off-black: #080808;
  --gray-900: #0f0f0f;
  --gray-800: #1a1a1a;
  --gray-700: #2a2a2a;
  --gray-400: #9ca3af;
  --white: #ffffff;
  --off-white: #f5f5f0;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  font-family: 'Barlow', sans-serif;
  background: var(--black);
  color: var(--off-white);
  overflow-x: hidden;
  cursor: default;
}

/* ── NOISE TEXTURE OVERLAY ── */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.03'/%3E%3C/svg%3E");
  pointer-events: none;
  z-index: 999;
  opacity: 0.4;
}

/* ── TYPOGRAPHY ── */
.font-display { font-family: 'Bebas Neue', sans-serif; letter-spacing: 0.04em; }
.font-condensed { font-family: 'Barlow Condensed', sans-serif; }

/* ── SCROLLBAR ── */
::-webkit-scrollbar { width: 3px; }
::-webkit-scrollbar-track { background: var(--black); }
::-webkit-scrollbar-thumb { background: var(--gold); }

/* ── NAV ── */
nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  padding: 1.5rem 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: rgba(0,0,0,0.85);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid rgba(251,191,36,0.1);
  transition: all 0.4s;
}

.nav-logo {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  text-decoration: none;
}

.nav-logo-mark {
  width: 44px;
  height: 44px;
  background: var(--gold);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.5rem;
  color: var(--black);
  clip-path: polygon(0 0, 85% 0, 100% 15%, 100% 100%, 15% 100%, 0 85%);
}

.nav-logo-text {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.6rem;
  color: var(--white);
  letter-spacing: 0.08em;
}

.nav-logo-text span { color: var(--gold); }

.nav-links {
  display: flex;
  align-items: center;
  gap: 2rem;
  list-style: none;
}

.nav-links a {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700;
  font-size: 0.75rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--gray-400);
  text-decoration: none;
  transition: color 0.2s;
}

.nav-links a:hover { color: var(--gold); }

.nav-cta {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 900;
  font-size: 0.75rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  background: var(--gold);
  color: var(--black);
  padding: 0.7rem 1.5rem;
  text-decoration: none;
  clip-path: polygon(0 0, 90% 0, 100% 25%, 100% 100%, 10% 100%, 0 75%);
  transition: all 0.2s;
}

.nav-cta:hover {
  background: var(--white);
  transform: translateY(-1px);
}

.nav-mobile-toggle {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  flex-direction: column;
  gap: 5px;
  padding: 4px;
}

.nav-mobile-toggle span {
  display: block;
  width: 24px;
  height: 2px;
  background: var(--gold);
  transition: 0.3s;
}

/* ── HERO ── */
#hero {
  min-height: 100vh;
  display: grid;
  grid-template-rows: 1fr auto;
  padding: 0;
  position: relative;
  overflow: hidden;
}

.hero-bg {
  position: absolute;
  inset: 0;
  background:
    radial-gradient(ellipse 80% 60% at 60% 40%, rgba(251,191,36,0.06) 0%, transparent 70%),
    radial-gradient(ellipse 40% 50% at 10% 80%, rgba(34,197,94,0.04) 0%, transparent 60%),
    var(--black);
}

.hero-grid {
  position: absolute;
  inset: 0;
  background-image:
    linear-gradient(rgba(251,191,36,0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(251,191,36,0.03) 1px, transparent 1px);
  background-size: 60px 60px;
  mask-image: radial-gradient(ellipse 80% 80% at 50% 50%, black 20%, transparent 100%);
}

.hero-content {
  position: relative;
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 8rem 2rem 4rem;
  max-width: 1200px;
  margin: 0 auto;
  width: 100%;
}

.hero-eyebrow {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
  opacity: 0;
  animation: fadeUp 0.8s 0.2s forwards;
}

.hero-eyebrow-line {
  width: 40px;
  height: 1px;
  background: var(--gold);
}

.hero-eyebrow-text {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700;
  font-size: 0.7rem;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--gold);
}

.hero-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(5rem, 14vw, 13rem);
  line-height: 0.9;
  letter-spacing: 0.02em;
  color: var(--white);
  opacity: 0;
  animation: fadeUp 0.8s 0.35s forwards;
}

.hero-title .accent { color: var(--gold); }
.hero-title .outline {
  -webkit-text-stroke: 2px rgba(255,255,255,0.15);
  color: transparent;
}

.hero-subtitle {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 300;
  font-size: clamp(1.1rem, 2.5vw, 1.6rem);
  letter-spacing: 0.05em;
  color: var(--gray-400);
  margin-top: 1.5rem;
  max-width: 560px;
  line-height: 1.4;
  opacity: 0;
  animation: fadeUp 0.8s 0.5s forwards;
}

.hero-subtitle strong {
  color: var(--off-white);
  font-weight: 700;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  margin-top: 3rem;
  flex-wrap: wrap;
  opacity: 0;
  animation: fadeUp 0.8s 0.65s forwards;
}

.btn-primary {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.1rem;
  letter-spacing: 0.1em;
  background: var(--gold);
  color: var(--black);
  padding: 1rem 2.5rem;
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  clip-path: polygon(0 0, 92% 0, 100% 20%, 100% 100%, 8% 100%, 0 80%);
  transition: all 0.25s;
  position: relative;
  overflow: hidden;
}

.btn-primary::before {
  content: '';
  position: absolute;
  inset: 0;
  background: var(--white);
  transform: translateX(-110%);
  transition: transform 0.3s;
}

.btn-primary:hover::before { transform: translateX(0); }
.btn-primary span { position: relative; z-index: 1; }

.btn-secondary {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700;
  font-size: 0.8rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--off-white);
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  border-bottom: 1px solid rgba(255,255,255,0.2);
  padding-bottom: 0.25rem;
  transition: all 0.2s;
}

.btn-secondary:hover {
  color: var(--gold);
  border-color: var(--gold);
  gap: 0.75rem;
}

.hero-stats {
  display: grid;
  grid-template-columns: repeat(3, auto);
  gap: 0 3rem;
  padding: 2rem;
  border-top: 1px solid rgba(255,255,255,0.06);
  border-bottom: 1px solid rgba(255,255,255,0.06);
  margin-top: 4rem;
  opacity: 0;
  animation: fadeUp 0.8s 0.8s forwards;
  position: relative;
  z-index: 2;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
  width: 100%;
}

.stat-item {}
.stat-number {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 3rem;
  color: var(--gold);
  line-height: 1;
}
.stat-label {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 300;
  font-size: 0.7rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gray-400);
  margin-top: 0.25rem;
}

/* ── TICKER ── */
.ticker-wrap {
  background: var(--gold);
  padding: 0.75rem 0;
  overflow: hidden;
  white-space: nowrap;
}

.ticker {
  display: inline-block;
  animation: ticker 30s linear infinite;
}

.ticker-item {
  display: inline-flex;
  align-items: center;
  gap: 1.5rem;
  padding: 0 3rem;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 0.9rem;
  letter-spacing: 0.1em;
  color: var(--black);
}

.ticker-dot {
  width: 4px;
  height: 4px;
  background: var(--black);
  border-radius: 50%;
  opacity: 0.4;
}

@keyframes ticker {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}

/* ── SECTIONS ── */
section {
  padding: 7rem 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.section-full {
  max-width: 100%;
  padding-left: 0;
  padding-right: 0;
}

.section-eyebrow {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 1rem;
}

.section-eyebrow-line {
  width: 30px;
  height: 1px;
  background: var(--gold);
}

.section-eyebrow-text {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700;
  font-size: 0.65rem;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--gold);
}

.section-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(3rem, 6vw, 5rem);
  line-height: 0.95;
  color: var(--white);
  letter-spacing: 0.03em;
}

.section-title .accent { color: var(--gold); }

/* ── SERVICES ── */
#services {
  background: var(--off-black);
  max-width: 100%;
  padding: 7rem 2rem;
}

#services-inner {
  max-width: 1200px;
  margin: 0 auto;
}

.services-header {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: end;
  margin-bottom: 5rem;
}

.services-desc {
  font-size: 1.05rem;
  color: var(--gray-400);
  line-height: 1.7;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1px;
  background: rgba(255,255,255,0.05);
}

.service-card {
  background: var(--off-black);
  padding: 3rem 2.5rem;
  position: relative;
  overflow: hidden;
  transition: all 0.4s;
  cursor: default;
}

.service-card::before {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: var(--gold);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.4s cubic-bezier(0.19, 1, 0.22, 1);
}

.service-card:hover::before { transform: scaleX(1); }

.service-card:hover { background: #0d0d0d; }

.service-number {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 5rem;
  line-height: 1;
  color: rgba(251,191,36,0.06);
  position: absolute;
  top: 1.5rem;
  right: 2rem;
  letter-spacing: 0;
  transition: color 0.4s;
}

.service-card:hover .service-number { color: rgba(251,191,36,0.12); }

.service-icon {
  width: 48px;
  height: 48px;
  background: rgba(251,191,36,0.1);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.3rem;
  margin-bottom: 1.5rem;
  clip-path: polygon(0 0, 80% 0, 100% 20%, 100% 100%, 20% 100%, 0 80%);
}

.service-name {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.8rem;
  letter-spacing: 0.05em;
  color: var(--white);
  margin-bottom: 0.75rem;
}

.service-desc {
  font-size: 0.875rem;
  color: var(--gray-400);
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.service-price {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 900;
  font-size: 1.1rem;
  color: var(--gold);
  letter-spacing: 0.05em;
}

.service-features {
  margin-top: 1.5rem;
  space: 0.5rem;
  list-style: none;
}

.service-features li {
  font-size: 0.8rem;
  color: var(--gray-400);
  padding: 0.4rem 0;
  border-bottom: 1px solid rgba(255,255,255,0.04);
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.service-features li::before {
  content: '→';
  color: var(--gold);
  font-size: 0.7rem;
}

/* ── QUOTE SECTION ── */
#quote {
  background: var(--gold);
  max-width: 100%;
  padding: 0;
}

.quote-inner {
  max-width: 1200px;
  margin: 0 auto;
  padding: 5rem 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 6rem;
  align-items: center;
}

.quote-left .section-title { color: var(--black); }
.quote-left .section-eyebrow-text { color: rgba(0,0,0,0.5); }
.quote-left .section-eyebrow-line { background: rgba(0,0,0,0.3); }

.quote-left p {
  font-size: 1rem;
  color: rgba(0,0,0,0.6);
  line-height: 1.7;
  margin-top: 1.5rem;
  font-weight: 600;
}

.quote-form {
  background: var(--black);
  padding: 2.5rem;
  clip-path: polygon(0 0, 95% 0, 100% 5%, 100% 100%, 5% 100%, 0 95%);
}

.form-group {
  margin-bottom: 1.25rem;
}

.form-label {
  display: block;
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700;
  font-size: 0.65rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gray-400);
  margin-bottom: 0.5rem;
}

.form-input {
  width: 100%;
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.08);
  padding: 0.875rem 1rem;
  color: var(--white);
  font-family: 'Barlow', sans-serif;
  font-size: 0.9rem;
  outline: none;
  transition: border-color 0.2s;
}

.form-input:focus { border-color: var(--gold); }
.form-input::placeholder { color: rgba(255,255,255,0.2); }

.form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }

.form-select {
  width: 100%;
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.08);
  padding: 0.875rem 1rem;
  color: var(--white);
  font-family: 'Barlow', sans-serif;
  font-size: 0.9rem;
  outline: none;
  cursor: pointer;
  appearance: none;
  transition: border-color 0.2s;
}

.form-select:focus { border-color: var(--gold); }
.form-select option { background: var(--gray-900); }

.form-submit {
  width: 100%;
  background: var(--gold);
  color: var(--black);
  border: none;
  padding: 1.1rem;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.2rem;
  letter-spacing: 0.1em;
  cursor: pointer;
  transition: all 0.25s;
  clip-path: polygon(0 0, 92% 0, 100% 25%, 100% 100%, 8% 100%, 0 75%);
  margin-top: 0.5rem;
}

.form-submit:hover { background: var(--white); transform: translateY(-1px); }

.form-note {
  font-size: 0.7rem;
  color: var(--gray-400);
  text-align: center;
  margin-top: 0.75rem;
  font-family: 'Barlow Condensed', sans-serif;
  letter-spacing: 0.05em;
}

/* ── WHY US ── */
#why {
  padding: 7rem 2rem;
}

.why-inner {
  max-width: 1200px;
  margin: 0 auto;
}

.why-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1px;
  background: rgba(255,255,255,0.05);
  margin-top: 4rem;
  border: 1px solid rgba(255,255,255,0.05);
}

.why-card {
  background: var(--black);
  padding: 2.5rem 2rem;
  transition: background 0.3s;
}

.why-card:hover { background: var(--gray-900); }

.why-icon {
  font-size: 2rem;
  margin-bottom: 1.5rem;
  display: block;
}

.why-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.4rem;
  letter-spacing: 0.05em;
  color: var(--white);
  margin-bottom: 0.75rem;
}

.why-desc {
  font-size: 0.85rem;
  color: var(--gray-400);
  line-height: 1.6;
}

/* ── PROCESS ── */
#process {
  background: var(--off-black);
  max-width: 100%;
  padding: 7rem 2rem;
}

.process-inner {
  max-width: 1200px;
  margin: 0 auto;
}

.process-steps {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 0;
  margin-top: 5rem;
  position: relative;
}

.process-steps::before {
  content: '';
  position: absolute;
  top: 2rem;
  left: 12%;
  right: 12%;
  height: 1px;
  background: linear-gradient(90deg, var(--gold), rgba(251,191,36,0.1));
}

.step {
  padding: 0 1.5rem;
  position: relative;
}

.step-number {
  width: 4rem;
  height: 4rem;
  background: var(--gold);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.3rem;
  color: var(--black);
  margin-bottom: 2rem;
  clip-path: polygon(0 0, 80% 0, 100% 20%, 100% 100%, 20% 100%, 0 80%);
  position: relative;
  z-index: 1;
}

.step-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.3rem;
  letter-spacing: 0.05em;
  color: var(--white);
  margin-bottom: 0.5rem;
}

.step-desc {
  font-size: 0.82rem;
  color: var(--gray-400);
  line-height: 1.6;
}

/* ── TESTIMONIALS ── */
#testimonials {
  padding: 7rem 2rem;
}

.testimonials-inner {
  max-width: 1200px;
  margin: 0 auto;
}

.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1px;
  background: rgba(255,255,255,0.05);
  margin-top: 4rem;
  border: 1px solid rgba(255,255,255,0.05);
}

.testimonial-card {
  background: var(--black);
  padding: 2.5rem;
  position: relative;
  transition: background 0.3s;
}

.testimonial-card:hover { background: var(--gray-900); }

.testimonial-stars {
  display: flex;
  gap: 0.25rem;
  margin-bottom: 1.5rem;
}

.star { color: var(--gold); font-size: 0.9rem; }

.testimonial-text {
  font-size: 0.95rem;
  line-height: 1.7;
  color: var(--off-white);
  margin-bottom: 2rem;
  font-style: italic;
}

.testimonial-text::before {
  content: '"';
  font-family: 'Bebas Neue', sans-serif;
  font-size: 3rem;
  color: rgba(251,191,36,0.15);
  display: block;
  line-height: 1;
  margin-bottom: 0.5rem;
}

.testimonial-author {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.author-avatar {
  width: 40px;
  height: 40px;
  background: rgba(251,191,36,0.15);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1rem;
  color: var(--gold);
  clip-path: polygon(0 0, 80% 0, 100% 20%, 100% 100%, 20% 100%, 0 80%);
}

.author-name {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700;
  font-size: 0.9rem;
  letter-spacing: 0.05em;
  color: var(--white);
}

.author-location {
  font-size: 0.75rem;
  color: var(--gray-400);
  font-family: 'Barlow Condensed', sans-serif;
  letter-spacing: 0.05em;
}

/* ── CTA BAND ── */
.cta-band {
  background: var(--gray-900);
  border-top: 1px solid rgba(251,191,36,0.15);
  border-bottom: 1px solid rgba(251,191,36,0.15);
  padding: 4rem 2rem;
  text-align: center;
}

.cta-band-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(2.5rem, 5vw, 4.5rem);
  color: var(--white);
  letter-spacing: 0.05em;
  margin-bottom: 0.5rem;
}

.cta-band-title .gold { color: var(--gold); }

.cta-band-sub {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 300;
  font-size: 1.1rem;
  color: var(--gray-400);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  margin-bottom: 2.5rem;
}

.cta-band-actions {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.btn-wa {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: #25D366;
  color: var(--white);
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.1rem;
  letter-spacing: 0.1em;
  padding: 1rem 2.5rem;
  text-decoration: none;
  clip-path: polygon(0 0, 92% 0, 100% 20%, 100% 100%, 8% 100%, 0 80%);
  transition: all 0.25s;
}

.btn-wa:hover { background: #1db954; transform: translateY(-2px); }

/* ── FOOTER ── */
footer {
  background: var(--off-black);
  padding: 4rem 2rem 2rem;
  border-top: 1px solid rgba(255,255,255,0.05);
}

.footer-inner {
  max-width: 1200px;
  margin: 0 auto;
}

.footer-top {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  gap: 4rem;
  margin-bottom: 3rem;
}

.footer-brand-logo {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 2.5rem;
  color: var(--white);
  letter-spacing: 0.05em;
  margin-bottom: 1rem;
}

.footer-brand-logo span { color: var(--gold); }

.footer-brand-desc {
  font-size: 0.875rem;
  color: var(--gray-400);
  line-height: 1.7;
  max-width: 280px;
}

.footer-contact {
  margin-top: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.footer-contact a {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 0.9rem;
  color: var(--gray-400);
  text-decoration: none;
  transition: color 0.2s;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.footer-contact a:hover { color: var(--gold); }

.footer-col-title {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700;
  font-size: 0.65rem;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 1.5rem;
}

.footer-links {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.footer-links a {
  font-size: 0.875rem;
  color: var(--gray-400);
  text-decoration: none;
  transition: color 0.2s;
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 600;
  letter-spacing: 0.05em;
}

.footer-links a:hover { color: var(--off-white); }

.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 2rem;
  border-top: 1px solid rgba(255,255,255,0.05);
  flex-wrap: wrap;
  gap: 1rem;
}

.footer-copy {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 0.75rem;
  letter-spacing: 0.1em;
  color: var(--gray-400);
}

.footer-copy span { color: var(--gold); }

.footer-badge {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700;
  font-size: 0.65rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gray-400);
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.footer-badge::before {
  content: '';
  width: 6px;
  height: 6px;
  background: var(--green);
  border-radius: 50%;
  box-shadow: 0 0 8px var(--green);
  animation: pulse-green 2s infinite;
}

@keyframes pulse-green {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.4; }
}

/* ── ANIMATIONS ── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

.reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s cubic-bezier(0.19, 1, 0.22, 1), transform 0.8s cubic-bezier(0.19, 1, 0.22, 1);
}

.reveal.visible { opacity: 1; transform: translateY(0); }
.reveal-delay-1 { transition-delay: 0.1s; }
.reveal-delay-2 { transition-delay: 0.2s; }
.reveal-delay-3 { transition-delay: 0.3s; }
.reveal-delay-4 { transition-delay: 0.4s; }

/* ── MOBILE ── */
@media (max-width: 768px) {
  .nav-links { display: none; }
  .nav-cta { display: none; }
  .nav-mobile-toggle { display: flex; }

  .hero-title { font-size: clamp(4rem, 16vw, 6rem); }

  .hero-stats {
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }

  .services-header { grid-template-columns: 1fr; gap: 2rem; }
  .services-grid { grid-template-columns: 1fr; }

  .quote-inner { grid-template-columns: 1fr; gap: 3rem; }

  .why-grid { grid-template-columns: 1fr 1fr; }

  .process-steps {
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
  }

  .process-steps::before { display: none; }

  .testimonials-grid { grid-template-columns: 1fr; }

  .footer-top { grid-template-columns: 1fr; gap: 2.5rem; }

  .form-grid { grid-template-columns: 1fr; }
}

@media (max-width: 480px) {
  .hero-stats { grid-template-columns: 1fr; gap: 1.5rem; }
  .why-grid { grid-template-columns: 1fr; }
  .process-steps { grid-template-columns: 1fr; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav id="navbar">
  <a href="#" class="nav-logo">
    <div class="nav-logo-mark">E</div>
    <div class="nav-logo-text">ELEVORE <span>PRO</span></div>
  </a>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#why">Why Us</a></li>
    <li><a href="#process">Process</a></li>
    <li><a href="#testimonials">Reviews</a></li>
  </ul>
  <a href="#quote" class="nav-cta">Get Free Quote</a>
  <button class="nav-mobile-toggle" onclick="toggleMenu()" aria-label="Menu">
    <span></span><span></span><span></span>
  </button>
</nav>

<!-- MOBILE MENU -->
<div id="mobile-menu" style="display:none;position:fixed;inset:0;background:rgba(0,0,0,0.97);z-index:99;flex-direction:column;align-items:center;justify-content:center;gap:2rem;">
  <a href="#services" onclick="toggleMenu()" style="font-family:'Bebas Neue',sans-serif;font-size:3rem;color:var(--white);text-decoration:none;letter-spacing:0.05em;">Services</a>
  <a href="#why" onclick="toggleMenu()" style="font-family:'Bebas Neue',sans-serif;font-size:3rem;color:var(--white);text-decoration:none;letter-spacing:0.05em;">Why Us</a>
  <a href="#process" onclick="toggleMenu()" style="font-family:'Bebas Neue',sans-serif;font-size:3rem;color:var(--white);text-decoration:none;letter-spacing:0.05em;">Process</a>
  <a href="#testimonials" onclick="toggleMenu()" style="font-family:'Bebas Neue',sans-serif;font-size:3rem;color:var(--white);text-decoration:none;letter-spacing:0.05em;">Reviews</a>
  <a href="#quote" onclick="toggleMenu()" class="btn-primary" style="margin-top:1rem;"><span>Get Free Quote →</span></a>
</div>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-content">
    <div class="hero-eyebrow">
      <div class="hero-eyebrow-line"></div>
      <span class="hero-eyebrow-text">Orlando, Florida — Licensed & Insured</span>
    </div>
    <h1 class="hero-title">
      YOUR HOME.<br>
      <span class="accent">OUR</span><br>
      <span class="outline">MISSION.</span>
    </h1>
    <p class="hero-subtitle">
      <strong>Elevore Premium Services</strong> delivers elite cleaning and handyman work with military precision. We don't clean houses — we transform them.
    </p>
    <div class="hero-actions">
      <a href="#quote" class="btn-primary"><span>Get Instant Quote →</span></a>
      <a href="tel:4079524228" class="btn-secondary">📞 (407) 952-4228</a>
    </div>
  </div>
  <div class="hero-stats">
    <div class="stat-item">
      <div class="stat-number">500+</div>
      <div class="stat-label">Missions Completed</div>
    </div>
    <div class="stat-item">
      <div class="stat-number">4.9★</div>
      <div class="stat-label">Average Rating</div>
    </div>
    <div class="stat-item">
      <div class="stat-number">48h</div>
      <div class="stat-label">Max Response Time</div>
    </div>
  </div>
</section>

<!-- TICKER -->
<div class="ticker-wrap">
  <div class="ticker">
    <span class="ticker-item">Regular Cleaning <span class="ticker-dot"></span></span>
    <span class="ticker-item">Deep Clean <span class="ticker-dot"></span></span>
    <span class="ticker-item">Move-Out Clean <span class="ticker-dot"></span></span>
    <span class="ticker-item">Post-Construction <span class="ticker-dot"></span></span>
    <span class="ticker-item">Handyman Services <span class="ticker-dot"></span></span>
    <span class="ticker-item">Orlando & Surroundings <span class="ticker-dot"></span></span>
    <span class="ticker-item">Licensed & Insured <span class="ticker-dot"></span></span>
    <span class="ticker-item">Same-Week Booking <span class="ticker-dot"></span></span>
    <span class="ticker-item">Regular Cleaning <span class="ticker-dot"></span></span>
    <span class="ticker-item">Deep Clean <span class="ticker-dot"></span></span>
    <span class="ticker-item">Move-Out Clean <span class="ticker-dot"></span></span>
    <span class="ticker-item">Post-Construction <span class="ticker-dot"></span></span>
    <span class="ticker-item">Handyman Services <span class="ticker-dot"></span></span>
    <span class="ticker-item">Orlando & Surroundings <span class="ticker-dot"></span></span>
    <span class="ticker-item">Licensed & Insured <span class="ticker-dot"></span></span>
    <span class="ticker-item">Same-Week Booking <span class="ticker-dot"></span></span>
  </div>
</div>

<!-- SERVICES -->
<div id="services">
  <div id="services-inner">
    <div class="services-header reveal">
      <div>
        <div class="section-eyebrow">
          <div class="section-eyebrow-line"></div>
          <span class="section-eyebrow-text">Our Services</span>
        </div>
        <h2 class="section-title">FIVE WAYS WE<br><span class="accent">DOMINATE.</span></h2>
      </div>
      <p class="services-desc">Every service comes with digital documentation, before & after photos, and a real-time client portal. No guessing — you see everything.</p>
    </div>
    <div class="services-grid">
      <div class="service-card reveal reveal-delay-1">
        <div class="service-number">01</div>
        <div class="service-icon">🏠</div>
        <div class="service-name">Regular Clean</div>
        <p class="service-desc">Weekly, bi-weekly or monthly maintenance to keep your home flawless all year.</p>
        <div class="service-price">From $95</div>
        <ul class="service-features">
          <li>All rooms & common areas</li>
          <li>Kitchen & bathroom deep</li>
          <li>Floors mopped & vacuumed</li>
          <li>Recurring discount up to 15%</li>
        </ul>
      </div>
      <div class="service-card reveal reveal-delay-2">
        <div class="service-number">02</div>
        <div class="service-icon">✨</div>
        <div class="service-name">Deep Clean</div>
        <p class="service-desc">Top-to-bottom intensive clean that reaches what regular maintenance misses.</p>
        <div class="service-price">From $165</div>
        <ul class="service-features">
          <li>Inside appliances</li>
          <li>Baseboards & vents</li>
          <li>Cabinet interiors</li>
          <li>Window sills & tracks</li>
        </ul>
      </div>
      <div class="service-card reveal reveal-delay-3">
        <div class="service-number">03</div>
        <div class="service-icon">📦</div>
        <div class="service-name">Move-Out Clean</div>
        <p class="service-desc">Deposit-saving precision clean guaranteed to impress landlords and new owners.</p>
        <div class="service-price">From $195</div>
        <ul class="service-features">
          <li>Full property documentation</li>
          <li>Before & after photos</li>
          <li>Digital signature proof</li>
          <li>Landlord-ready report</li>
        </ul>
      </div>
      <div class="service-card reveal reveal-delay-1">
        <div class="service-number">04</div>
        <div class="service-icon">🏗️</div>
        <div class="service-name">Post-Construction</div>
        <p class="service-desc">Heavy-duty debris and dust removal after renovation or new construction.</p>
        <div class="service-price">$0.35 per sqft</div>
        <ul class="service-features">
          <li>Dust & debris removal</li>
          <li>Window & surface clean</li>
          <li>Floor finishing</li>
          <li>Move-in ready result</li>
        </ul>
      </div>
      <div class="service-card reveal reveal-delay-2">
        <div class="service-number">05</div>
        <div class="service-icon">🛠️</div>
        <div class="service-name">Handyman</div>
        <p class="service-desc">From mounting TVs to installing doors — skilled labor with transparent pricing.</p>
        <div class="service-price">$85/hr + materials</div>
        <ul class="service-features">
          <li>TV mounting from $150</li>
          <li>Door installation from $200</li>
          <li>Drywall patch from $180</li>
          <li>Tiered material markup</li>
        </ul>
      </div>
      <div class="service-card reveal reveal-delay-3" style="background: linear-gradient(135deg, rgba(251,191,36,0.05) 0%, transparent 100%); border-left: 3px solid var(--gold);">
        <div class="service-number" style="color: rgba(251,191,36,0.15);">+</div>
        <div class="service-icon" style="background: rgba(251,191,36,0.15);">💎</div>
        <div class="service-name">Membership Plans</div>
        <p class="service-desc">Lock in priority scheduling and permanent discounts with a recurring plan.</p>
        <div class="service-price">From $199/mo</div>
        <ul class="service-features">
          <li>Basic — 2 cleans/month</li>
          <li>Premium — 4 cleans/month</li>
          <li>VIP — 6 cleans + all add-ons</li>
          <li>Dedicated team assigned</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<!-- QUOTE FORM -->
<div id="quote">
  <div class="quote-inner">
    <div class="quote-left reveal">
      <div class="section-eyebrow">
        <div class="section-eyebrow-line"></div>
        <span class="section-eyebrow-text">Free Estimate</span>
      </div>
      <h2 class="section-title">GET YOUR<br>QUOTE IN<br>60 SECONDS.</h2>
      <p>Fill the form and we'll send your personalized quote via WhatsApp immediately. No waiting. No guessing.</p>
    </div>
    <div class="quote-form reveal reveal-delay-2">
      <form onsubmit="submitQuote(event)">
        <div class="form-grid">
          <div class="form-group">
            <label class="form-label">First Name</label>
            <input type="text" class="form-input" placeholder="Jose" required id="q-name">
          </div>
          <div class="form-group">
            <label class="form-label">Phone (WhatsApp)</label>
            <input type="tel" class="form-input" placeholder="(407) 000-0000" required id="q-phone">
          </div>
        </div>
        <div class="form-group">
          <label class="form-label">Property Address</label>
          <input type="text" class="form-input" placeholder="123 Main St, Orlando, FL" required id="q-address">
        </div>
        <div class="form-grid">
          <div class="form-group">
            <label class="form-label">Service Type</label>
            <select class="form-select" required id="q-service">
              <option value="">Select...</option>
              <option value="Regular Cleaning">Regular Cleaning</option>
              <option value="Deep Clean">Deep Clean</option>
              <option value="Move-Out Clean">Move-Out Clean</option>
              <option value="Post-Construction">Post-Construction</option>
              <option value="Handyman">Handyman</option>
            </select>
          </div>
          <div class="form-group">
            <label class="form-label">Bedrooms</label>
            <select class="form-select" id="q-beds">
              <option value="1">1 Bedroom</option>
              <option value="2" selected>2 Bedrooms</option>
              <option value="3">3 Bedrooms</option>
              <option value="4">4 Bedrooms</option>
              <option value="5">5+ Bedrooms</option>
            </select>
          </div>
        </div>
        <div class="form-group">
          <label class="form-label">Bathrooms</label>
          <select class="form-select" id="q-baths">
            <option value="1">1 Bathroom</option>
            <option value="2" selected>2 Bathrooms</option>
            <option value="3">3 Bathrooms</option>
            <option value="4">4+ Bathrooms</option>
          </select>
        </div>
        <button type="submit" class="form-submit">⚡ SEND MY FREE QUOTE</button>
        <p class="form-note">✓ Instant WhatsApp reply &nbsp;•&nbsp; No commitment &nbsp;•&nbsp; (407) 952-4228</p>
      </form>
    </div>
  </div>
</div>

<!-- WHY US -->
<div id="why" style="padding: 7rem 2rem; background: var(--black);">
  <div class="why-inner">
    <div class="reveal" style="margin-bottom: 4rem;">
      <div class="section-eyebrow">
        <div class="section-eyebrow-line"></div>
        <span class="section-eyebrow-text">Why Elevore</span>
      </div>
      <h2 class="section-title">THE ELEVORE<br><span class="accent">DIFFERENCE.</span></h2>
    </div>
    <div class="why-grid">
      <div class="why-card reveal reveal-delay-1">
        <span class="why-icon">⚡</span>
        <div class="why-title">Real-Time Tracking</div>
        <p class="why-desc">You get a live mission portal with check-in times, team arrival updates, and before & after photos — all in real time.</p>
      </div>
      <div class="why-card reveal reveal-delay-2">
        <span class="why-icon">✍️</span>
        <div class="why-title">Digital Signatures</div>
        <p class="why-desc">Every job is legally documented. You approve the quote digitally and sign off on completion — zero paperwork.</p>
      </div>
      <div class="why-card reveal reveal-delay-3">
        <span class="why-icon">🛡️</span>
        <div class="why-title">Licensed & Insured</div>
        <p class="why-desc">Full insurance coverage on every job. Your property is protected and our team is accountable at all times.</p>
      </div>
      <div class="why-card reveal reveal-delay-4">
        <span class="why-icon">📱</span>
        <div class="why-title">WhatsApp First</div>
        <p class="why-desc">Book, track, and communicate entirely through WhatsApp. No apps to download, no portals to remember.</p>
      </div>
    </div>
  </div>
</div>

<!-- PROCESS -->
<div id="process" style="background: var(--off-black); padding: 7rem 2rem;">
  <div class="process-inner">
    <div class="reveal" style="margin-bottom: 1rem;">
      <div class="section-eyebrow">
        <div class="section-eyebrow-line"></div>
        <span class="section-eyebrow-text">How It Works</span>
      </div>
      <h2 class="section-title">SIMPLE AS<br><span class="accent">4 STEPS.</span></h2>
    </div>
    <div class="process-steps">
      <div class="step reveal reveal-delay-1">
        <div class="step-number">01</div>
        <div class="step-title">Request Quote</div>
        <p class="step-desc">Fill our 60-second form or send us a WhatsApp. We respond with a full price breakdown instantly.</p>
      </div>
      <div class="step reveal reveal-delay-2">
        <div class="step-number">02</div>
        <div class="step-title">Digital Approval</div>
        <p class="step-desc">Review your quote online and sign digitally. Your spot is locked in the moment you sign.</p>
      </div>
      <div class="step reveal reveal-delay-3">
        <div class="step-number">03</div>
        <div class="step-title">Mission Day</div>
        <p class="step-desc">Our team checks in on arrival. You track everything live and see before & after photos in real time.</p>
      </div>
      <div class="step reveal reveal-delay-4">
        <div class="step-number">04</div>
        <div class="step-title">Final Sign-Off</div>
        <p class="step-desc">You inspect the work, sign completion digitally, and pay via Zelle. Simple, transparent, done.</p>
      </div>
    </div>
  </div>
</div>

<!-- TESTIMONIALS -->
<div id="testimonials" style="padding: 7rem 2rem; background: var(--black);">
  <div class="testimonials-inner">
    <div class="reveal" style="margin-bottom: 1rem;">
      <div class="section-eyebrow">
        <div class="section-eyebrow-line"></div>
        <span class="section-eyebrow-text">Client Reviews</span>
      </div>
      <h2 class="section-title">WHAT ORLANDO<br><span class="accent">SAYS.</span></h2>
    </div>
    <div class="testimonials-grid" style="margin-top: 4rem;">
      <div class="testimonial-card reveal reveal-delay-1">
        <div class="testimonial-stars">
          <span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span>
        </div>
        <p class="testimonial-text">Elevore transformed my house before I sold it. The move-out clean was so thorough that my realtor asked who did it. The before & after photos were an incredible touch.</p>
        <div class="testimonial-author">
          <div class="author-avatar">MR</div>
          <div>
            <div class="author-name">Maria Rodriguez</div>
            <div class="author-location">Windermere, FL</div>
          </div>
        </div>
      </div>
      <div class="testimonial-card reveal reveal-delay-2">
        <div class="testimonial-stars">
          <span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span>
        </div>
        <p class="testimonial-text">I've had cleaners before but nothing like this. The real-time portal showing the team's arrival time and progress? That's next level. I booked them for monthly service immediately.</p>
        <div class="testimonial-author">
          <div class="author-avatar">DT</div>
          <div>
            <div class="author-name">David Thompson</div>
            <div class="author-location">Lake Nona, FL</div>
          </div>
        </div>
      </div>
      <div class="testimonial-card reveal reveal-delay-3">
        <div class="testimonial-stars">
          <span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span>
        </div>
        <p class="testimonial-text">The handyman fixed my TV mount, patched drywall, and installed a new lock all in one visit. The itemized invoice with digital sign-off made me feel like I was dealing with a real company.</p>
        <div class="testimonial-author">
          <div class="author-avatar">JL</div>
          <div>
            <div class="author-name">Jennifer Lee</div>
            <div class="author-location">Doctor Phillips, FL</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- CTA BAND -->
<div class="cta-band">
  <h2 class="cta-band-title">READY TO BOOK YOUR <span class="gold">MISSION?</span></h2>
  <p class="cta-band-sub">Same-week availability · Orlando & Surrounding Areas</p>
  <div class="cta-band-actions">
    <a href="https://wa.me/14079524228?text=Hi%20Elevore!%20I%27d%20like%20to%20get%20a%20quote." class="btn-wa" target="_blank">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
      WhatsApp Us Now
    </a>
    <a href="tel:4079524228" class="btn-primary" style="background: var(--white);"><span style="color: var(--black);">📞 (407) 952-4228</span></a>
    <a href="#quote" class="btn-primary"><span>Get Free Quote →</span></a>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-top">
      <div>
        <div class="footer-brand-logo">ELEVORE <span>PRO</span></div>
        <p class="footer-brand-desc">Elite cleaning and handyman services in Orlando and surrounding areas. Precision, transparency, and results — every single time.</p>
        <div class="footer-contact">
          <a href="tel:4079524228">📞 (407) 952-4228</a>
          <a href="https://wa.me/14079524228" target="_blank">💬 WhatsApp</a>
          <a href="mailto:info@elevore.pro">✉️ info@elevore.pro</a>
        </div>
      </div>
      <div>
        <div class="footer-col-title">Services</div>
        <ul class="footer-links">
          <li><a href="#services">Regular Cleaning</a></li>
          <li><a href="#services">Deep Clean</a></li>
          <li><a href="#services">Move-Out Clean</a></li>
          <li><a href="#services">Post-Construction</a></li>
          <li><a href="#services">Handyman</a></li>
          <li><a href="#services">Memberships</a></li>
        </ul>
      </div>
      <div>
        <div class="footer-col-title">Service Areas</div>
        <ul class="footer-links">
          <li><a href="#quote">Orlando</a></li>
          <li><a href="#quote">Windermere</a></li>
          <li><a href="#quote">Lake Nona</a></li>
          <li><a href="#quote">Kissimmee</a></li>
          <li><a href="#quote">Doctor Phillips</a></li>
          <li><a href="#quote">Winter Garden</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="footer-copy">© 2025 <span>Elevore Premium Services</span> — All rights reserved. Orlando, FL</div>
      <div class="footer-badge">Serving Orlando Since 2024</div>
    </div>
  </div>
</footer>

<script>
// ── MOBILE MENU ──
function toggleMenu() {
  const m = document.getElementById('mobile-menu');
  m.style.display = m.style.display === 'flex' ? 'none' : 'flex';
}

// ── SCROLL REVEAL ──
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

// ── NAV SCROLL ──
window.addEventListener('scroll', () => {
  const nav = document.getElementById('navbar');
  nav.style.borderBottomColor = window.scrollY > 50 ? 'rgba(251,191,36,0.2)' : 'rgba(251,191,36,0.1)';
});

// ── QUOTE FORM — sends to WhatsApp ──
function submitQuote(e) {
  e.preventDefault();
  const name    = document.getElementById('q-name').value;
  const phone   = document.getElementById('q-phone').value;
  const address = document.getElementById('q-address').value;
  const service = document.getElementById('q-service').value;
  const beds    = document.getElementById('q-beds').value;
  const baths   = document.getElementById('q-baths').value;

  // Basic price estimate
  const prices  = {'Regular Cleaning': 95, 'Deep Clean': 165, 'Move-Out Clean': 195, 'Post-Construction': 200, 'Handyman': 170};
  const base    = (prices[service] || 95) + (parseInt(beds) * 40) + (parseInt(baths) * 35);

  const msg = `Hi Elevore! I'd like a quote:\n\n👤 Name: ${name}\n📞 Phone: ${phone}\n📍 Address: ${address}\n🏠 Service: ${service}\n🛏️ Bedrooms: ${beds}\n🚿 Bathrooms: ${baths}\n\n💰 Estimated range: $${base}+\n\nPlease confirm availability!`;

  window.open(`https://wa.me/14079524228?text=${encodeURIComponent(msg)}`, '_blank');
}

// ── SMOOTH ANCHOR ──
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', e => {
    const id = a.getAttribute('href');
    if(id === '#') return;
    const el = document.querySelector(id);
    if(el) { e.preventDefault(); el.scrollIntoView({ behavior: 'smooth' }); }
  });
});
</script>
</body>
</html>
