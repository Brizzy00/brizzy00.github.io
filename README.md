<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Samuel Ebisemiju · SQA Engineer</title>
  <meta name="description" content="SQA Engineer with 2+ years experience in manual, regression, and exploratory testing. Available for remote roles and freelance engagements.">
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://brizzy00.github.io/">
  <meta property="og:title" content="Samuel Ebisemiju · SQA Engineer">
  <meta property="og:description" content="SQA Engineer with 2+ years experience in manual, regression, and exploratory testing. Available for remote roles and freelance engagements.">
  <meta name="twitter:card" content="summary">
  <meta name="twitter:title" content="Samuel Ebisemiju · SQA Engineer">
  <meta name="twitter:description" content="SQA Engineer with 2+ years experience in manual, regression, and exploratory testing. Available for remote roles and freelance engagements.">
  <link rel="icon" type="image/svg+xml" href="favicon.svg">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Epilogue:ital,wght@0,300;0,400;0,500;0,600;1,300&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg:           #080C14;
      --bg-surface:   #0F1420;
      --bg-card:      #111827;
      --bg-card-hover:#151f30;
      --accent:       #00D4A1;
      --accent-dim:   rgba(0, 212, 161, 0.12);
      --accent-amber: #F59E0B;
      --accent-red:   #FF4D4D;
      --text:         #E2E8F0;
      --text-muted:   #64748B;
      --text-subtle:  #2A3545;
      --border:       rgba(255,255,255,0.06);
      --border-accent:rgba(0,212,161,0.28);
      --font-display: 'Bebas Neue', cursive;
      --font-mono:    'Space Mono', monospace;
      --font-body:    'Epilogue', sans-serif;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--font-body);
      font-weight: 300;
      line-height: 1.7;
      overflow-x: hidden;
    }

    /* Subtle grain overlay */
    body::after {
      content: '';
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 9999;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='300'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='300' height='300' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
      opacity: 0.35;
    }

    ::-webkit-scrollbar { width: 3px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: var(--accent); border-radius: 2px; }

    /* ── NAV ── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 200;
      display: flex; justify-content: space-between; align-items: center;
      padding: 1.25rem 3rem;
      background: rgba(8,12,20,0.88);
      backdrop-filter: blur(24px);
      border-bottom: 1px solid var(--border);
    }
    .nav-logo {
      font-family: var(--font-mono); font-size: 0.78rem;
      color: var(--accent); letter-spacing: 0.05em;
    }
    .nav-logo span { color: var(--text-muted); }
    .nav-links { display: flex; gap: 2.25rem; list-style: none; }
    .nav-links a {
      font-family: var(--font-mono); font-size: 0.68rem;
      letter-spacing: 0.14em; text-transform: uppercase;
      color: var(--text-muted); text-decoration: none;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--accent); }

    /* ── PROJECTS ── */
    .projects-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(320px,1fr));
      gap: 1.25rem;
    }
    .project-card {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 4px; padding: 1.6rem;
      display: flex; flex-direction: column; gap: 1rem;
      transition: border-color 0.25s, background 0.25s, transform 0.25s;
      text-decoration: none; color: inherit;
    }
    .project-card:hover {
      border-color: var(--border-accent);
      background: var(--bg-card-hover);
      transform: translateY(-2px);
    }
    .project-card-top {
      display: flex; justify-content: space-between; align-items: flex-start;
    }
    .project-type {
      font-family: var(--font-mono); font-size: 0.6rem;
      letter-spacing: 0.14em; text-transform: uppercase;
      padding: 0.15rem 0.5rem; border-radius: 2px; white-space: nowrap;
    }
    .project-type.py  { background: rgba(245,158,11,0.1); color: var(--accent-amber); border: 1px solid rgba(245,158,11,0.22); }
    .project-type.web { background: var(--accent-dim); color: var(--accent); border: 1px solid var(--border-accent); }
    .project-type.bot { background: rgba(168,85,247,0.1); color: #c084fc; border: 1px solid rgba(168,85,247,0.22); }
    .project-arrow {
      font-family: var(--font-mono); font-size: 0.85rem;
      color: var(--text-subtle); transition: color 0.2s, transform 0.2s;
    }
    .project-card:hover .project-arrow { color: var(--accent); transform: translate(2px,-2px); }
    .project-name { font-size: 1.05rem; font-weight: 500; color: var(--text); line-height: 1.3; }
    .project-desc { font-size: 0.88rem; color: var(--text-muted); line-height: 1.7; flex: 1; }
    .project-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-top: auto; }
    .project-tag {
      padding: 0.22rem 0.55rem;
      background: rgba(255,255,255,0.025); border: 1px solid var(--border);
      border-radius: 2px; font-family: var(--font-mono); font-size: 0.65rem;
      color: var(--text-muted);
    }

    /* ── HERO ── */
    .hero {
      min-height: 100vh;
      display: flex; flex-direction: column; justify-content: center;
      padding: 9rem 3rem 5rem;
      position: relative; overflow: hidden;
    }
    .hero-grid {
      position: absolute; inset: 0;
      background-image:
        linear-gradient(var(--border) 1px, transparent 1px),
        linear-gradient(90deg, var(--border) 1px, transparent 1px);
      background-size: 64px 64px;
      mask-image: radial-gradient(ellipse 80% 80% at 40% 50%, black 20%, transparent 80%);
    }
    .hero-glow {
      position: absolute; top: 15%; left: 10%;
      width: 700px; height: 700px;
      background: radial-gradient(circle, rgba(0,212,161,0.055) 0%, transparent 65%);
      pointer-events: none;
    }
    .hero-glow-2 {
      position: absolute; bottom: 5%; right: 5%;
      width: 400px; height: 400px;
      background: radial-gradient(circle, rgba(245,158,11,0.04) 0%, transparent 65%);
      pointer-events: none;
    }

    .hero-terminal {
      font-family: var(--font-mono); font-size: 0.78rem;
      color: var(--text-muted); margin-bottom: 2.25rem;
      position: relative; z-index: 1;
      display: flex; align-items: center; gap: 0.5rem;
    }
    .hero-terminal .prompt { color: var(--accent); }
    .cursor {
      display: inline-block; width: 9px; height: 1.1em;
      background: var(--accent);
      animation: blink 1s step-end infinite;
      vertical-align: middle;
    }
    @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

    .hero-name {
      font-family: var(--font-display);
      font-size: clamp(4.5rem, 11vw, 10rem);
      line-height: 0.88; letter-spacing: 0.01em;
      color: var(--text);
      position: relative; z-index: 1;
      animation: slideUp 0.9s cubic-bezier(0.16,1,0.3,1) both;
      animation-delay: 0.25s;
    }
    .hero-name .accent { color: var(--accent); }

    .hero-title {
      font-family: var(--font-mono); font-size: 0.82rem;
      letter-spacing: 0.22em; text-transform: uppercase;
      color: var(--text-muted); margin-top: 1.75rem;
      position: relative; z-index: 1;
      animation: slideUp 0.9s cubic-bezier(0.16,1,0.3,1) both;
      animation-delay: 0.42s;
    }

    .hero-badges {
      display: flex; flex-wrap: wrap; gap: 0.65rem;
      margin-top: 2rem; position: relative; z-index: 1;
      animation: slideUp 0.9s cubic-bezier(0.16,1,0.3,1) both;
      animation-delay: 0.58s;
    }
    .badge {
      display: inline-flex; align-items: center; gap: 0.45rem;
      padding: 0.3rem 0.8rem;
      border: 1px solid var(--border-accent);
      background: var(--accent-dim);
      border-radius: 2px;
      font-family: var(--font-mono); font-size: 0.68rem;
      letter-spacing: 0.1em; color: var(--accent);
    }
    .badge.amber {
      border-color: rgba(245,158,11,0.28);
      background: rgba(245,158,11,0.08);
      color: var(--accent-amber);
    }
    .badge.neutral {
      border-color: var(--border);
      background: rgba(255,255,255,0.02);
      color: var(--text-muted);
    }
    .badge .dot {
      width: 5px; height: 5px; border-radius: 50%;
      background: currentColor;
      animation: pls 2.2s ease-in-out infinite;
    }
    @keyframes pls { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.4;transform:scale(0.7)} }

    .hero-stats {
      display: flex; gap: 4rem; flex-wrap: wrap;
      margin-top: 4.5rem; padding-top: 2.5rem;
      border-top: 1px solid var(--border);
      position: relative; z-index: 1;
      animation: slideUp 0.9s cubic-bezier(0.16,1,0.3,1) both;
      animation-delay: 0.72s;
    }
    .stat-item { display: flex; flex-direction: column; }
    .stat-number {
      font-family: var(--font-display);
      font-size: clamp(2.8rem,5vw,4rem);
      line-height: 1; color: var(--accent);
    }
    .stat-suffix {
      font-family: var(--font-display);
      font-size: clamp(1.5rem,2.5vw,2rem);
      color: var(--accent); opacity: 0.7;
    }
    .stat-label {
      font-family: var(--font-mono); font-size: 0.62rem;
      letter-spacing: 0.14em; text-transform: uppercase;
      color: var(--text-muted); margin-top: 0.3rem;
      line-height: 1.5;
    }

    /* ── SECTION ── */
    section { padding: 7rem 3rem; max-width: 1100px; margin: 0 auto; }

    .section-label {
      font-family: var(--font-mono); font-size: 0.68rem;
      letter-spacing: 0.2em; text-transform: uppercase;
      color: var(--accent); margin-bottom: 1rem;
      display: flex; align-items: center; gap: 0.75rem;
    }
    .section-label::after {
      content: ''; flex: 0 0 50px; height: 1px;
      background: var(--accent); opacity: 0.35;
    }
    .section-title {
      font-family: var(--font-display);
      font-size: clamp(2.8rem, 6vw, 5rem);
      line-height: 0.92; color: var(--text);
      margin-bottom: 3.5rem;
    }

    /* ── ABOUT ── */
    .about-grid {
      display: grid; grid-template-columns: 1.1fr 0.9fr;
      gap: 4rem; align-items: start;
    }
    .about-text p {
      color: var(--text-muted); margin-bottom: 1.25rem;
      font-size: 1.05rem; line-height: 1.85;
    }
    .about-text p strong { color: var(--text); font-weight: 500; }

    .about-meta { display: flex; flex-direction: column; gap: 1px; }
    .meta-item {
      padding: 1.1rem 1.25rem;
      background: var(--bg-card); border: 1px solid var(--border);
      transition: border-color 0.25s, background 0.25s;
    }
    .meta-item:first-child { border-radius: 4px 4px 0 0; }
    .meta-item:last-child  { border-radius: 0 0 4px 4px; }
    .meta-item:hover { border-color: var(--border-accent); background: var(--bg-card-hover); }
    .meta-label {
      font-family: var(--font-mono); font-size: 0.62rem;
      letter-spacing: 0.15em; text-transform: uppercase;
      color: var(--text-muted); margin-bottom: 0.25rem;
    }
    .meta-value { color: var(--text); font-size: 0.92rem; }
    .meta-value a { color: var(--accent); text-decoration: none; }
    .meta-value a:hover { text-decoration: underline; }

    /* ── EXPERIENCE ── */
    .experience-list { display: flex; flex-direction: column; gap: 1.5rem; }

    .exp-suite {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 4px; overflow: hidden;
      transition: border-color 0.3s;
    }
    .exp-suite:hover { border-color: var(--border-accent); }

    .exp-suite-header {
      display: flex; justify-content: space-between; align-items: center;
      padding: 0.9rem 1.5rem;
      background: rgba(0,212,161,0.035);
      border-bottom: 1px solid var(--border);
    }
    .suite-label {
      font-family: var(--font-mono); font-size: 0.72rem;
      color: var(--accent); letter-spacing: 0.07em;
      display: flex; align-items: center; gap: 0.5rem;
    }
    .suite-label .pre { color: var(--text-muted); }
    .suite-count {
      font-family: var(--font-mono); font-size: 0.62rem;
      padding: 0.18rem 0.55rem;
      background: var(--accent-dim); color: var(--accent);
      border-radius: 2px; letter-spacing: 0.08em;
      white-space: nowrap;
    }

    .exp-test {
      padding: 1.5rem;
      border-bottom: 1px solid var(--border);
    }
    .exp-test:last-child { border-bottom: none; }

    .test-header {
      display: flex; justify-content: space-between;
      align-items: flex-start; margin-bottom: 0.85rem;
      flex-wrap: wrap; gap: 0.5rem;
    }
    .test-role {
      font-size: 1.05rem; font-weight: 500; color: var(--text);
      display: flex; align-items: center; gap: 0.6rem;
    }
    .pass-badge {
      font-family: var(--font-mono); font-size: 0.58rem;
      padding: 0.15rem 0.5rem;
      background: rgba(0,212,161,0.1); color: var(--accent);
      border: 1px solid rgba(0,212,161,0.22); border-radius: 2px;
      letter-spacing: 0.1em;
    }
    .test-date {
      font-family: var(--font-mono); font-size: 0.68rem;
      color: var(--text-muted); letter-spacing: 0.05em;
      white-space: nowrap;
    }

    .bullets { list-style: none; }
    .bullets li {
      font-size: 0.9rem; color: var(--text-muted);
      padding: 0.28rem 0 0.28rem 1.3rem;
      position: relative; line-height: 1.65;
    }
    .bullets li::before {
      content: '→'; position: absolute; left: 0;
      color: var(--text-subtle); font-family: var(--font-mono);
      font-size: 0.68rem; top: 0.38rem;
    }
    .bullets .hl { color: var(--accent); }

    /* ── SKILLS ── */
    .skills-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(290px,1fr));
      gap: 1.25rem;
    }
    .skill-cat {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 4px; padding: 1.4rem;
      transition: border-color 0.25s;
    }
    .skill-cat:hover { border-color: var(--border-accent); }
    .skill-cat-top {
      display: flex; justify-content: space-between;
      align-items: center; margin-bottom: 1.1rem;
    }
    .skill-cat-name {
      font-family: var(--font-mono); font-size: 0.67rem;
      letter-spacing: 0.14em; text-transform: uppercase;
      color: var(--text-muted);
    }
    .skill-cat-status {
      font-family: var(--font-mono); font-size: 0.6rem;
      padding: 0.12rem 0.45rem;
      background: rgba(0,212,161,0.08); color: var(--accent);
      border: 1px solid rgba(0,212,161,0.2);
      border-radius: 2px; letter-spacing: 0.08em;
    }
    .skill-tags { display: flex; flex-wrap: wrap; gap: 0.45rem; }
    .skill-tag {
      padding: 0.3rem 0.65rem;
      background: rgba(255,255,255,0.025);
      border: 1px solid var(--border);
      border-radius: 2px;
      font-family: var(--font-mono); font-size: 0.7rem;
      color: var(--text); transition: all 0.2s; cursor: default;
    }
    .skill-tag:hover {
      border-color: var(--border-accent);
      color: var(--accent); background: var(--accent-dim);
    }

    /* ── EDUCATION ── */
    .edu-grid {
      display: grid; grid-template-columns: 1fr 1fr;
      gap: 2.5rem; align-items: start;
    }
    .edu-cards { display: flex; flex-direction: column; gap: 1.25rem; }
    .edu-card {
      padding: 1.75rem; background: var(--bg-card);
      border: 1px solid var(--border); border-radius: 4px;
      border-left: 3px solid var(--accent);
      transition: border-color 0.25s;
    }
    .edu-card:hover { border-color: var(--border-accent); border-left-color: var(--accent); }
    .edu-degree { font-size: 1rem; font-weight: 500; color: var(--text); margin-bottom: 0.3rem; }
    .edu-school {
      font-family: var(--font-mono); font-size: 0.72rem;
      color: var(--accent); margin-bottom: 0.6rem; letter-spacing: 0.04em;
    }
    .edu-meta {
      font-family: var(--font-mono); font-size: 0.67rem;
      color: var(--text-muted); letter-spacing: 0.04em;
    }

    .cert-list { display: flex; flex-direction: column; gap: 1px; }
    .cert-item {
      display: flex; align-items: center; gap: 1rem;
      padding: 1.1rem 1.25rem;
      background: var(--bg-card); border: 1px solid var(--border);
      transition: border-color 0.25s, background 0.25s;
    }
    .cert-item:first-child { border-radius: 4px 4px 0 0; }
    .cert-item:last-child  { border-radius: 0 0 4px 4px; }
    .cert-item:hover { border-color: var(--border-accent); background: var(--bg-card-hover); }
    .cert-num {
      font-family: var(--font-mono); font-size: 0.65rem;
      color: var(--accent-amber); flex-shrink: 0; width: 28px;
    }
    .cert-name { font-size: 0.88rem; color: var(--text); }

    /* ── CONTACT ── */
    .contact-inner {
      text-align: center; padding: 8rem 3rem;
      max-width: 750px; margin: 0 auto;
    }
    .contact-inner .section-label {
      justify-content: center;
    }
    .contact-inner .section-label::before {
      content: ''; flex: 0 0 50px; height: 1px;
      background: var(--accent); opacity: 0.35;
    }
    .contact-tagline {
      font-size: 1.05rem; color: var(--text-muted);
      max-width: 480px; margin: 0 auto 3rem;
      line-height: 1.8;
    }
    .contact-links {
      display: flex; justify-content: center;
      flex-wrap: wrap; gap: 1rem;
    }
    .contact-link {
      display: inline-flex; align-items: center; gap: 0.6rem;
      padding: 0.8rem 1.6rem;
      border: 1px solid var(--border); border-radius: 2px;
      font-family: var(--font-mono); font-size: 0.72rem;
      letter-spacing: 0.09em; color: var(--text-muted);
      text-decoration: none; transition: all 0.22s;
    }
    .contact-link:hover {
      border-color: var(--border-accent);
      color: var(--accent); background: var(--accent-dim);
    }
    .contact-link.primary {
      border-color: var(--border-accent);
      background: var(--accent-dim); color: var(--accent);
    }
    .contact-link.primary:hover { background: rgba(0,212,161,0.2); }

    /* ── FOOTER ── */
    footer {
      padding: 2rem 3rem;
      border-top: 1px solid var(--border);
      display: flex; justify-content: space-between;
      align-items: center; flex-wrap: wrap; gap: 0.75rem;
    }
    footer p {
      font-family: var(--font-mono); font-size: 0.62rem;
      color: var(--text-subtle); letter-spacing: 0.12em;
    }
    footer a { color: var(--accent); text-decoration: none; }

    /* ── ANIMATIONS ── */
    @keyframes slideUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    .reveal {
      opacity: 0; transform: translateY(28px);
      transition: opacity 0.75s cubic-bezier(0.16,1,0.3,1),
                  transform 0.75s cubic-bezier(0.16,1,0.3,1);
    }
    .reveal.visible { opacity: 1; transform: translateY(0); }
    .reveal-delay-1 { transition-delay: 0.1s; }
    .reveal-delay-2 { transition-delay: 0.2s; }
    .reveal-delay-3 { transition-delay: 0.3s; }

    /* ── DIVIDER ── */
    .section-divider {
      width: 100%; height: 1px;
      background: linear-gradient(90deg, transparent, var(--border) 20%, var(--border) 80%, transparent);
      margin: 0;
    }

    /* ── HAMBURGER ── */
    .nav-toggle {
      display: none;
      flex-direction: column;
      justify-content: center;
      gap: 5px;
      background: none;
      border: none;
      cursor: pointer;
      padding: 0.4rem;
    }
    .nav-toggle span {
      display: block;
      width: 20px; height: 2px;
      background: var(--text-muted);
      border-radius: 1px;
      transition: all 0.25s cubic-bezier(0.16,1,0.3,1);
    }
    .nav-toggle.open span:nth-child(1) { transform: translateY(7px) rotate(45deg); background: var(--accent); }
    .nav-toggle.open span:nth-child(2) { opacity: 0; transform: scaleX(0); }
    .nav-toggle.open span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); background: var(--accent); }

    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      .about-grid { grid-template-columns: 1fr; gap: 2.5rem; }
      .edu-grid   { grid-template-columns: 1fr; }
    }
    @media (max-width: 768px) {
      nav { padding: 1rem 1.5rem; }
      .nav-links { gap: 1.25rem; }
      section { padding: 5rem 1.5rem; }
      .hero { padding: 7.5rem 1.5rem 4rem; }
      .hero-stats { gap: 2rem; }
      footer { padding: 1.5rem; flex-direction: column; text-align: center; }
    }
    @media (max-width: 520px) {
      .nav-toggle { display: flex; }
      .nav-links {
        display: none;
        position: fixed;
        top: 57px; left: 0; right: 0; bottom: 0;
        background: rgba(8,12,20,0.97);
        backdrop-filter: blur(24px);
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 2.5rem;
        z-index: 199;
        border-top: 1px solid var(--border);
      }
      .nav-links.open { display: flex; }
      .nav-links a { font-size: 0.88rem; letter-spacing: 0.2em; }
      .hero-stats { gap: 1.5rem; }
      .stat-number { font-size: 2.5rem; }
      .contact-inner { padding: 5rem 1.5rem; }
    }
  </style>
</head>
<body>

  <!-- ── NAV ── -->
  <nav>
    <div class="nav-logo"><span>~/</span>samuel.ebisemiju</div>
    <ul class="nav-links">
      <li><a href="#about">about</a></li>
      <li><a href="#experience">experience</a></li>
      <li><a href="#projects">projects</a></li>
      <li><a href="#skills">skills</a></li>
      <li><a href="#education">education</a></li>
      <li><a href="#contact">contact</a></li>
      <li><a href="Samuel_Ebisemiju_CV.pdf" target="_blank" rel="noopener" style="color:var(--accent);border:1px solid var(--border-accent);padding:0.2rem 0.65rem;border-radius:2px;">resume ↗</a></li>
    </ul>
    <button class="nav-toggle" aria-label="Toggle navigation" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
  </nav>

  <!-- ── HERO ── -->
  <div class="hero">
    <div class="hero-grid"></div>
    <div class="hero-glow"></div>
    <div class="hero-glow-2"></div>

    <div class="hero-terminal">
      <span class="prompt">$&nbsp;</span>
      <span id="typed-text"></span><span class="cursor"></span>
    </div>

    <h1 class="hero-name">
      Samuel<br><span class="accent">Ebisemiju</span>
    </h1>

    <p class="hero-title">Software Quality Assurance Engineer</p>

    <div class="hero-badges">
      <span class="badge"><span class="dot"></span>&nbsp;PASS: Available for Remote</span>
      <span class="badge neutral">Abuja, Nigeria</span>
      <span class="badge amber">Playwright &nbsp;·&nbsp; Python &nbsp;·&nbsp; Postman</span>
    </div>

    <div class="hero-stats">
      <div class="stat-item">
        <div>
          <span class="stat-number" data-count="30">30</span><span class="stat-suffix">%</span>
        </div>
        <span class="stat-label">Test Coverage<br>Improved</span>
      </div>
      <div class="stat-item">
        <div>
          <span class="stat-number" data-count="20">20</span><span class="stat-suffix">%</span>
        </div>
        <span class="stat-label">Production<br>Defects Reduced</span>
      </div>
      <div class="stat-item">
        <div>
          <span class="stat-number" data-count="40">40</span><span class="stat-suffix">+</span>
        </div>
        <span class="stat-label">Defects Found<br>Single Engagement</span>
      </div>
      <div class="stat-item">
        <div>
          <span class="stat-number" data-count="2">2</span><span class="stat-suffix">+</span>
        </div>
        <span class="stat-label">Years QA<br>Experience</span>
      </div>
    </div>
  </div>

  <div class="section-divider"></div>

  <!-- ── ABOUT ── -->
  <section id="about">
    <div class="section-label">01 &middot; About</div>
    <h2 class="section-title">Quality is<br>not optional.</h2>

    <div class="about-grid">
      <div class="about-text reveal">
        <p>
          I'm an SQA Engineer with hands-on experience in <strong>manual and regression testing</strong> for web applications. I've built a track record of measurably improving product stability — from owning full regression cycles to identifying 40+ defects (including XSS vulnerabilities) in a single freelance engagement.
        </p>
        <p>
          Building automation frameworks with <strong>Playwright and Python</strong>, with solid expertise in Qase, GitHub, and Postman across CI/CD-driven workflows. I collaborate directly with developers, participate in release validation, and treat quality as a shared responsibility.
        </p>
        <p>
          Passionate about delivering reliable, scalable software in remote, fast-paced environments. I don't just find bugs, I help prevent them.
        </p>
      </div>

      <div class="about-meta reveal reveal-delay-1">
        <div class="meta-item">
          <div class="meta-label">Location</div>
          <div class="meta-value">Abuja, Nigeria &nbsp;&middot;&nbsp; Open to Remote</div>
        </div>
        <div class="meta-item">
          <div class="meta-label">Email</div>
          <div class="meta-value">
            <a href="mailto:ebisemijusamuel1@gmail.com">ebisemijusamuel1@gmail.com</a>
          </div>
        </div>

        <div class="meta-item">
          <div class="meta-label">LinkedIn</div>
          <div class="meta-value"><a href="https://linkedin.com/in/samuel-ebisemiju" target="_blank" rel="noopener">linkedin.com/in/samuel-ebisemiju</a></div>
        </div>
        <div class="meta-item">
          <div class="meta-label">Status</div>
          <div class="meta-value" style="color:var(--accent)">&#9679; &nbsp;Available for Opportunities</div>
        </div>
      </div>
    </div>
  </section>

  <div class="section-divider"></div>

  <!-- ── EXPERIENCE ── -->
  <section id="experience">
    <div class="section-label">02 &middot; Experience</div>
    <h2 class="section-title">Test Suites<br>Shipped.</h2>

    <div class="experience-list">

      <!-- Field Tech -->
      <div class="exp-suite reveal">
        <div class="exp-suite-header">
          <span class="suite-label">
            <span class="pre">SUITE:</span>
            Field Technology Development Partners
          </span>
          <span class="suite-count">2 PASSED</span>
        </div>

        <div class="exp-test">
          <div class="test-header">
            <div class="test-role">
              Software Quality Assurance Engineer
              <span class="pass-badge">&#9679; PASS</span>
            </div>
            <span class="test-date">Mar 2026 &ndash; Present</span>
          </div>
          <ul class="bullets">
            <li>Design and execute structured test cases across staging and production environments, ensuring comprehensive coverage of functional and non-functional requirements.</li>
            <li>Own full regression testing cycles for releases and hotfixes, reducing post-release defect escapes.</li>
            <li>Identify, document, and track defects end-to-end using Qase and GitHub, collaborating directly with developers to accelerate resolution.</li>
            <li>Participate in CI/CD release validation workflows, supporting faster and more reliable deployment cycles.</li>
            <li>Improved test coverage by <span class="hl">30%</span>, reducing production defects by <span class="hl">20%</span>, contributing to measurable gains in product stability.</li>
          </ul>
        </div>

        <div class="exp-test">
          <div class="test-header">
            <div class="test-role">
              QA Intern
              <span class="pass-badge">&#9679; PASS</span>
            </div>
            <span class="test-date">Mar 2025 &ndash; Feb 2026</span>
          </div>
          <ul class="bullets">
            <li>Executed manual test cases for web applications, supporting the QA team across multiple active projects.</li>
            <li>Assisted with regression testing during staging releases and reported bugs with clear reproduction steps using Qase and GitHub.</li>
            <li>Collaborated with team members to clarify requirements and investigate edge cases.</li>
            <li>Contributed to QA documentation, test planning, and internal knowledge-sharing initiatives.</li>
          </ul>
        </div>
      </div>

      <!-- Freelance -->
      <div class="exp-suite reveal reveal-delay-1">
        <div class="exp-suite-header">
          <span class="suite-label">
            <span class="pre">SUITE:</span>
            Freelance QA Engineer &nbsp;&middot;&nbsp; Self-employed
          </span>
          <span class="suite-count">1 PASSED</span>
        </div>

        <div class="exp-test">
          <div class="test-header">
            <div class="test-role">
              End-to-End Security &amp; Functional Audit
              <span class="pass-badge">&#9679; PASS</span>
            </div>
            <span class="test-date">Feb 2026 &ndash; Mar 2026</span>
          </div>
          <ul class="bullets">
            <li>Performed end-to-end testing on a live web application covering functional, exploratory, and security-related scenarios.</li>
            <li>Identified <span class="hl">40+ defects</span> including XSS vulnerabilities, improving application security before production release with detailed reproduction steps and remediation recommendations.</li>
            <li>Collaborated with client stakeholders to validate all reported fixes and sign off on final quality.</li>
          </ul>
        </div>
      </div>

      <!-- NNPC -->
      <div class="exp-suite reveal reveal-delay-2">
        <div class="exp-suite-header">
          <span class="suite-label">
            <span class="pre">SUITE:</span>
            Nigerian National Petroleum Company (NNPC)
          </span>
          <span class="suite-count">1 PASSED</span>
        </div>

        <div class="exp-test">
          <div class="test-header">
            <div class="test-role">
              IT Intern
              <span class="pass-badge">&#9679; PASS</span>
            </div>
            <span class="test-date">Apr 2023 &ndash; Oct 2023</span>
          </div>
          <ul class="bullets">
            <li>Supported internal teams with system organization, documentation, and data management processes.</li>
            <li>Prepared reports and presentations for senior staff; participated in technical workshops and internal training sessions.</li>
            <li>Gained exposure to enterprise-level systems and professional IT workflows.</li>
          </ul>
        </div>
      </div>

    </div>
  </section>

  <div class="section-divider"></div>

  <!-- ── PROJECTS ── -->
  <section id="projects">
    <div class="section-label">03 &middot; Projects</div>
    <h2 class="section-title">Things I've<br>Built.</h2>

    <div class="projects-grid">

      <!-- Daily Timesheet Bot -->
      <a class="project-card reveal" href="https://github.com/Brizzy00/Timesheet-Bot" target="_blank" rel="noopener">
        <div class="project-card-top">
          <span class="project-type bot">Slack Bot</span>
          <span class="project-arrow">↗</span>
        </div>
        <div class="project-name">Daily Timesheet Bot</div>
        <div class="project-desc">
          A Slack bot that prompts you each day at 4:45 PM to log work tasks, then uses Gemini AI to match them to the correct Clockify projects and syncs automatically — including Google Calendar meetings to avoid overlap.
        </div>
        <div class="project-tags">
          <span class="project-tag">Python</span>
          <span class="project-tag">Slack Bolt</span>
          <span class="project-tag">Clockify API</span>
          <span class="project-tag">Google Calendar API</span>
          <span class="project-tag">Gemini AI</span>
          <span class="project-tag">Railway</span>
        </div>
      </a>

      <!-- Money Tracker -->
      <div class="project-card reveal reveal-delay-1">
        <div class="project-card-top">
          <span class="project-type web">Web App</span>
        </div>
        <div class="project-name">Money Tracker</div>
        <div class="project-desc">
          A personal finance dashboard for tracking transactions, setting budgets, and monitoring spending by category. Three-tab interface with month navigation, CRUD modals, and persistent local storage — no backend needed.
        </div>
        <div class="project-tags">
          <span class="project-tag">React</span>
          <span class="project-tag">Vite</span>
          <span class="project-tag">Tailwind CSS</span>
          <span class="project-tag">localStorage</span>
        </div>
      </div>

      <!-- EPUB Reader -->
      <div class="project-card reveal reveal-delay-2">
        <div class="project-card-top">
          <span class="project-type web">Web App</span>
        </div>
        <div class="project-name">EPUB Reader</div>
        <div class="project-desc">
          A single-file EPUB reader with a three-panel layout — library view, reader, and reading stats sidebar. Features reading progress tracking, continue-reading history, and a distraction-free reader mode. Zero dependencies.
        </div>
        <div class="project-tags">
          <span class="project-tag">HTML</span>
          <span class="project-tag">CSS</span>
          <span class="project-tag">JavaScript</span>
          <span class="project-tag">Single File</span>
        </div>
      </div>

      <!-- DiskMap -->
      <div class="project-card reveal">
        <div class="project-card-top">
          <span class="project-type py">Python CLI</span>
        </div>
        <div class="project-name">DiskMap</div>
        <div class="project-desc">
          A CLI tool that visualises disk space usage as a tree with Unicode box-drawing characters and proportional progress bars — instantly reveals which folders are eating your storage.
        </div>
        <div class="project-tags">
          <span class="project-tag">Python</span>
          <span class="project-tag">pathlib</span>
          <span class="project-tag">CLI</span>
        </div>
      </div>

      <!-- Dupes -->
      <div class="project-card reveal reveal-delay-1">
        <div class="project-card-top">
          <span class="project-type py">Python CLI</span>
        </div>
        <div class="project-name">Duplicate File Finder</div>
        <div class="project-desc">
          Scans directories for duplicate files using two-pass SHA-256 hashing (size first, then content) for efficiency. Calculates wasted space per group and offers interactive deletion with a safe dry-run mode.
        </div>
        <div class="project-tags">
          <span class="project-tag">Python</span>
          <span class="project-tag">hashlib</span>
          <span class="project-tag">CLI</span>
        </div>
      </div>

      <!-- Organise -->
      <div class="project-card reveal reveal-delay-2">
        <div class="project-card-top">
          <span class="project-type py">Python CLI</span>
        </div>
        <div class="project-name">File Organiser</div>
        <div class="project-desc">
          Automatically sorts a messy directory into category-based subfolders (Images, Documents, Code, etc.) across 8 categories and 50+ extensions. Dry-run preview, collision handling, and a tidy summary report.
        </div>
        <div class="project-tags">
          <span class="project-tag">Python</span>
          <span class="project-tag">pathlib</span>
          <span class="project-tag">shutil</span>
          <span class="project-tag">CLI</span>
        </div>
      </div>

    </div>
  </section>

  <div class="section-divider"></div>

  <!-- ── SKILLS ── -->
  <section id="skills">
    <div class="section-label">04 &middot; Skills</div>
    <h2 class="section-title">Core<br>Capabilities.</h2>

    <div class="skills-grid">
      <div class="skill-cat reveal">
        <div class="skill-cat-top">
          <span class="skill-cat-name">QA &amp; Testing</span>
          <span class="skill-cat-status">PASS</span>
        </div>
        <div class="skill-tags">
          <span class="skill-tag">Manual Testing</span>
          <span class="skill-tag">Functional Testing</span>
          <span class="skill-tag">Regression Testing</span>
          <span class="skill-tag">Exploratory Testing</span>
          <span class="skill-tag">Test Case Design</span>
          <span class="skill-tag">Defect Lifecycle</span>
          <span class="skill-tag">Verification &amp; Validation</span>
          <span class="skill-tag">Edge-Case Analysis</span>
          <span class="skill-tag">Requirements Analysis</span>
        </div>
      </div>

      <div class="skill-cat reveal reveal-delay-1">
        <div class="skill-cat-top">
          <span class="skill-cat-name">Automation</span>
          <span class="skill-cat-status">PASS</span>
        </div>
        <div class="skill-tags">
          <span class="skill-tag">Playwright</span>
          <span class="skill-tag">Python</span>
          <span class="skill-tag">Framework Design</span>
          <span class="skill-tag">Automation Strategy</span>
        </div>
      </div>

      <div class="skill-cat reveal reveal-delay-2">
        <div class="skill-cat-top">
          <span class="skill-cat-name">Tools &amp; Platforms</span>
          <span class="skill-cat-status">PASS</span>
        </div>
        <div class="skill-tags">
          <span class="skill-tag">Qase</span>
          <span class="skill-tag">GitHub</span>
          <span class="skill-tag">Postman</span>
          <span class="skill-tag">Notion</span>
          <span class="skill-tag">VS Code</span>
          <span class="skill-tag">PowerShell</span>
        </div>
      </div>

      <div class="skill-cat reveal reveal-delay-3">
        <div class="skill-cat-top">
          <span class="skill-cat-name">Infrastructure &amp; API</span>
          <span class="skill-cat-status">PASS</span>
        </div>
        <div class="skill-tags">
          <span class="skill-tag">CI/CD Pipelines</span>
          <span class="skill-tag">Release Validation</span>
          <span class="skill-tag">API Testing</span>
          <span class="skill-tag">Staging Environments</span>
          <span class="skill-tag">Response Validation</span>
        </div>
      </div>
    </div>
  </section>

  <div class="section-divider"></div>

  <!-- ── EDUCATION ── -->
  <section id="education">
    <div class="section-label">05 &middot; Education &amp; Certifications</div>
    <h2 class="section-title">Foundation<br>&amp; Growth.</h2>

    <div class="edu-grid">
      <div class="edu-cards reveal">
        <div class="edu-card">
          <div class="edu-degree">B.Sc. Computer Science &amp; Information Technology</div>
          <div class="edu-school">Veritas University, Abuja</div>
          <div class="edu-meta">Jan 2021 – Nov 2024 &nbsp;&middot;&nbsp; Second Class Upper Division</div>
        </div>
        <div class="edu-card">
          <div class="edu-degree">Senior Secondary Certificate (SSCE)</div>
          <div class="edu-school">Parliament International Secondary School, Abuja</div>
          <div class="edu-meta">Sep 2014 – Aug 2017 &nbsp;&middot;&nbsp; Senior Prefect</div>
        </div>
      </div>

      <div class="cert-list reveal reveal-delay-1">
        <div class="cert-item">
          <span class="cert-num">[01]</span>
          <span class="cert-name">EFSET English Certificate &mdash; 71/100 (C2 Proficient)</span>
        </div>
        <div class="cert-item">
          <span class="cert-num">[02]</span>
          <span class="cert-name">Introduction to Python &mdash; Automation</span>
        </div>
        <div class="cert-item">
          <span class="cert-num">[03]</span>
          <span class="cert-name">FlutterFlow &amp; Firebase Crash Course</span>
        </div>
      </div>
    </div>
  </section>

  <div class="section-divider"></div>

  <!-- ── CONTACT ── -->
  <section id="contact">
    <div class="contact-inner reveal">
      <div class="section-label">06 &middot; Contact</div>
      <h2 class="section-title" style="margin-bottom:1rem">Let's build<br>quality together.</h2>
      <p class="contact-tagline">
        Open to remote SQA roles and freelance testing engagements. Let's talk about how I can help your team ship more reliable software.
      </p>
      <div class="contact-links">
        <a href="mailto:ebisemijusamuel1@gmail.com" class="contact-link primary">
          ebisemijusamuel1@gmail.com
        </a>
        <a href="https://linkedin.com/in/samuel-ebisemiju" class="contact-link" target="_blank" rel="noopener">
          LinkedIn Profile
        </a>
        <a href="https://github.com/Brizzy00" class="contact-link" target="_blank" rel="noopener">
          GitHub &mdash; Brizzy00
        </a>
        <a href="Samuel_Ebisemiju_CV.pdf" target="_blank" rel="noopener" class="contact-link primary">
          View CV ↗
        </a>
      </div>
    </div>
  </section>

  <!-- ── FOOTER ── -->
  <footer>
    <p>&copy; 2026 SAMUEL EBISEMIJU</p>
    <p>SQA ENGINEER &nbsp;&middot;&nbsp; ABUJA, NIGERIA &nbsp;&middot;&nbsp; <a href="https://github.com/Brizzy00" target="_blank" rel="noopener">GITHUB</a></p>
  </footer>

  <script>
    // ── Typewriter
    const phrases = [
      'portfolio.load()',
      'running regression_suite --all',
      'status: all_tests_passed ✓',
      'git push origin main'
    ];
    let pIdx = 0, cIdx = 0, deleting = false;
    const el = document.getElementById('typed-text');

    function type() {
      const word = phrases[pIdx];
      if (deleting) {
        el.textContent = word.slice(0, --cIdx);
      } else {
        el.textContent = word.slice(0, ++cIdx);
      }
      let delay = deleting ? 35 : 75;
      if (!deleting && cIdx === word.length) { delay = 2200; deleting = true; }
      else if (deleting && cIdx === 0)       { deleting = false; pIdx = (pIdx + 1) % phrases.length; delay = 450; }
      setTimeout(type, delay);
    }
    type();

    // ── Count-up
    function countUp(el) {
      const target = +el.dataset.count;
      const dur = 1600;
      const start = performance.now();
      (function frame(now) {
        const t = Math.min((now - start) / dur, 1);
        const eased = 1 - Math.pow(1 - t, 3);
        el.textContent = Math.round(eased * target);
        if (t < 1) requestAnimationFrame(frame);
      })(performance.now());
    }

    let counted = false;
    const statEls = document.querySelectorAll('.stat-number[data-count]');

    // ── Scroll reveal
    const revealEls = document.querySelectorAll('.reveal');
    const io = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) e.target.classList.add('visible');
      });
    }, { threshold: 0.12 });
    revealEls.forEach(el => io.observe(el));

    // Count up on hero enter
    const heroIO = new IntersectionObserver((entries) => {
      if (entries[0].isIntersecting && !counted) {
        counted = true;
        setTimeout(() => statEls.forEach(countUp), 900);
      }
    }, { threshold: 0.4 });
    heroIO.observe(document.querySelector('.hero'));

    // ── Nav active state
    const sections = document.querySelectorAll('section[id]');
    const navLinks = document.querySelectorAll('.nav-links a');
    const NAV_OFFSET = 80;

    function updateActiveNav() {
      const scrollY = window.scrollY + NAV_OFFSET;
      let activeId = null;
      sections.forEach(s => {
        if (s.offsetTop <= scrollY) activeId = s.id;
      });
      navLinks.forEach(a => {
        const isActive = a.getAttribute('href') === '#' + activeId;
        a.style.color = isActive ? 'var(--accent)' : '';
      });
    }

    window.addEventListener('scroll', updateActiveNav, { passive: true });
    updateActiveNav();

    // ── Hamburger toggle
    const navToggle = document.querySelector('.nav-toggle');
    const navMenu = document.querySelector('.nav-links');
    navToggle.addEventListener('click', () => {
      const isOpen = navMenu.classList.toggle('open');
      navToggle.classList.toggle('open');
      navToggle.setAttribute('aria-expanded', isOpen);
      document.body.style.overflow = isOpen ? 'hidden' : '';
    });
    navMenu.querySelectorAll('a').forEach(link => {
      link.addEventListener('click', () => {
        navMenu.classList.remove('open');
        navToggle.classList.remove('open');
        navToggle.setAttribute('aria-expanded', 'false');
        document.body.style.overflow = '';
      });
    });
  </script>
</body>
</html>
