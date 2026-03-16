[index.html](https://github.com/user-attachments/files/26032947/aman_resume.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Aman Kapoor | Pharmaceutical Scientist</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Playfair+Display:wght@700;800&display=swap" rel="stylesheet"/>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"/>
  <style>
    :root {
      --primary: #0f4c81;
      --primary-light: #1a6bba;
      --accent: #00b4d8;
      --accent2: #48cae4;
      --gold: #f4a261;
      --bg: #f0f4f8;
      --card: #ffffff;
      --text: #1a202c;
      --muted: #64748b;
      --border: #e2e8f0;
      --gradient: linear-gradient(135deg, #0f4c81 0%, #1a6bba 50%, #00b4d8 100%);
      --gradient-hero: linear-gradient(135deg, #0f4c81 0%, #1565c0 40%, #00b4d8 100%);
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.7;
    }

    /* ───── NAV ───── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
      background: rgba(15, 76, 129, 0.95);
      backdrop-filter: blur(12px);
      display: flex; align-items: center; justify-content: space-between;
      padding: 0 40px; height: 64px;
      box-shadow: 0 2px 20px rgba(0,0,0,0.2);
    }
    .nav-brand {
      font-family: 'Playfair Display', serif;
      font-size: 1.3rem; color: #fff; letter-spacing: 1px;
    }
    .nav-links { display: flex; gap: 28px; list-style: none; }
    .nav-links a {
      color: rgba(255,255,255,0.85); text-decoration: none;
      font-size: 0.85rem; font-weight: 500; letter-spacing: 0.5px;
      text-transform: uppercase; transition: color 0.3s;
    }
    .nav-links a:hover { color: var(--accent2); }

    /* ───── HERO ───── */
    .hero {
      min-height: 100vh;
      background: var(--gradient-hero);
      display: flex; align-items: center; justify-content: center;
      text-align: center; padding: 100px 20px 60px;
      position: relative; overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute; inset: 0;
      background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.04'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    }
    .hero-particles {
      position: absolute; inset: 0; overflow: hidden; pointer-events: none;
    }
    .particle {
      position: absolute; border-radius: 50%;
      background: rgba(255,255,255,0.1);
      animation: float 8s infinite ease-in-out;
    }
    @keyframes float {
      0%,100% { transform: translateY(0) scale(1); opacity:0.6; }
      50% { transform: translateY(-40px) scale(1.1); opacity:1; }
    }
    .hero-avatar {
      width: 140px; height: 140px;
      background: rgba(255,255,255,0.15);
      border: 4px solid rgba(255,255,255,0.4);
      border-radius: 50%; display: flex; align-items: center;
      justify-content: center; margin: 0 auto 28px;
      font-size: 3.5rem; color: #fff;
      box-shadow: 0 0 60px rgba(0,180,216,0.4);
      animation: pulse-glow 3s ease-in-out infinite;
    }
    @keyframes pulse-glow {
      0%,100% { box-shadow: 0 0 40px rgba(0,180,216,0.4); }
      50% { box-shadow: 0 0 80px rgba(0,180,216,0.7); }
    }
    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.5rem, 6vw, 4.2rem);
      color: #fff; font-weight: 800; letter-spacing: 1px;
      text-shadow: 0 2px 20px rgba(0,0,0,0.2);
      margin-bottom: 8px;
    }
    .hero-degree {
      font-size: 1rem; color: rgba(255,255,255,0.8);
      letter-spacing: 2px; text-transform: uppercase;
      margin-bottom: 20px; font-weight: 400;
    }
    .hero-tagline {
      font-size: 1.15rem; color: rgba(255,255,255,0.9);
      max-width: 600px; margin: 0 auto 32px;
      font-weight: 300;
    }
    .hero-badges {
      display: flex; flex-wrap: wrap; gap: 10px;
      justify-content: center; margin-bottom: 36px;
    }
    .badge {
      background: rgba(255,255,255,0.15);
      border: 1px solid rgba(255,255,255,0.3);
      color: #fff; padding: 6px 18px; border-radius: 50px;
      font-size: 0.82rem; font-weight: 500; letter-spacing: 0.5px;
      backdrop-filter: blur(4px);
    }
    .hero-contacts {
      display: flex; flex-wrap: wrap; gap: 16px; justify-content: center;
    }
    .contact-btn {
      display: flex; align-items: center; gap: 8px;
      padding: 10px 22px; border-radius: 50px;
      text-decoration: none; font-size: 0.9rem; font-weight: 600;
      transition: all 0.3s; letter-spacing: 0.5px;
    }
    .contact-btn.primary {
      background: #fff; color: var(--primary);
    }
    .contact-btn.primary:hover { background: var(--accent2); color: #fff; transform: translateY(-2px); }
    .contact-btn.outline {
      border: 2px solid rgba(255,255,255,0.6); color: #fff;
    }
    .contact-btn.outline:hover { background: rgba(255,255,255,0.15); transform: translateY(-2px); }

    .scroll-indicator {
      position: absolute; bottom: 28px; left: 50%;
      transform: translateX(-50%);
      color: rgba(255,255,255,0.7); font-size: 1.5rem;
      animation: bounce 2s infinite;
    }
    @keyframes bounce {
      0%,100% { transform: translateX(-50%) translateY(0); }
      50% { transform: translateX(-50%) translateY(10px); }
    }

    /* ───── STATS BAR ───── */
    .stats-bar {
      background: var(--card);
      box-shadow: 0 4px 30px rgba(0,0,0,0.08);
      padding: 32px 20px;
    }
    .stats-inner {
      max-width: 1000px; margin: 0 auto;
      display: grid; grid-template-columns: repeat(auto-fit, minmax(150px,1fr));
      gap: 20px; text-align: center;
    }
    .stat-item {
      padding: 16px;
      border-right: 1px solid var(--border);
    }
    .stat-item:last-child { border-right: none; }
    .stat-num {
      font-size: 2.4rem; font-weight: 800;
      background: var(--gradient); -webkit-background-clip: text;
      -webkit-text-fill-color: transparent; background-clip: text;
      display: block; line-height: 1.1;
    }
    .stat-label {
      font-size: 0.78rem; color: var(--muted);
      text-transform: uppercase; letter-spacing: 1px;
      margin-top: 4px; font-weight: 600;
    }

    /* ───── MAIN LAYOUT ───── */
    main { max-width: 1100px; margin: 0 auto; padding: 60px 20px; }

    section { margin-bottom: 70px; }

    .section-header {
      display: flex; align-items: center; gap: 14px;
      margin-bottom: 36px;
    }
    .section-icon {
      width: 48px; height: 48px; border-radius: 14px;
      background: var(--gradient); display: flex;
      align-items: center; justify-content: center;
      color: #fff; font-size: 1.2rem;
      flex-shrink: 0;
      box-shadow: 0 4px 15px rgba(15,76,129,0.3);
    }
    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: 1.9rem; color: var(--primary); font-weight: 700;
    }
    .section-line {
      flex: 1; height: 2px;
      background: linear-gradient(90deg, var(--primary-light), transparent);
      border-radius: 2px;
    }

    /* ───── OBJECTIVE ───── */
    .objective-card {
      background: var(--gradient);
      border-radius: 20px; padding: 36px 40px;
      color: #fff; position: relative; overflow: hidden;
    }
    .objective-card::before {
      content: '\f10d';
      font-family: 'Font Awesome 6 Free'; font-weight: 900;
      position: absolute; top: 20px; left: 28px;
      font-size: 4rem; opacity: 0.12; color: #fff;
    }
    .objective-card p {
      font-size: 1.05rem; line-height: 1.9;
      font-weight: 300; position: relative; z-index: 1;
    }

    /* ───── EXPERIENCE ───── */
    .timeline { position: relative; padding-left: 30px; }
    .timeline::before {
      content: ''; position: absolute; left: 10px; top: 0; bottom: 0;
      width: 2px;
      background: linear-gradient(180deg, var(--primary), var(--accent), transparent);
      border-radius: 2px;
    }
    .timeline-item {
      position: relative; margin-bottom: 40px;
    }
    .timeline-dot {
      position: absolute; left: -26px; top: 20px;
      width: 16px; height: 16px; border-radius: 50%;
      background: var(--gradient); border: 3px solid #fff;
      box-shadow: 0 0 0 3px var(--primary);
    }
    .exp-card {
      background: var(--card); border-radius: 18px;
      padding: 28px 32px; border: 1px solid var(--border);
      box-shadow: 0 4px 20px rgba(0,0,0,0.06);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .exp-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 12px 40px rgba(15,76,129,0.15);
    }
    .exp-top {
      display: flex; flex-wrap: wrap;
      justify-content: space-between; align-items: flex-start;
      gap: 10px; margin-bottom: 8px;
    }
    .exp-role {
      font-size: 1.15rem; font-weight: 700; color: var(--primary);
    }
    .exp-duration {
      background: #e8f4fd; color: var(--primary-light);
      padding: 4px 14px; border-radius: 50px;
      font-size: 0.78rem; font-weight: 600;
    }
    .exp-org {
      font-size: 0.95rem; color: var(--muted); font-weight: 500;
      margin-bottom: 12px;
    }
    .exp-org i { margin-right: 6px; color: var(--accent); }
    .exp-tags { display: flex; flex-wrap: wrap; gap: 8px; }
    .exp-tag {
      background: #f0f7ff; color: var(--primary);
      padding: 3px 12px; border-radius: 20px;
      font-size: 0.78rem; font-weight: 500;
      border: 1px solid #c3ddf7;
    }

    /* ───── EDUCATION ───── */
    .edu-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(260px,1fr));
      gap: 22px;
    }
    .edu-card {
      background: var(--card); border-radius: 18px;
      padding: 26px 24px; border: 1px solid var(--border);
      box-shadow: 0 4px 20px rgba(0,0,0,0.05);
      transition: all 0.3s; position: relative; overflow: hidden;
    }
    .edu-card::before {
      content: ''; position: absolute; top: 0; left: 0; right: 0; height: 4px;
      background: var(--gradient);
    }
    .edu-card:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(15,76,129,0.15); }
    .edu-icon {
      width: 44px; height: 44px; background: var(--gradient);
      border-radius: 12px; display: flex; align-items: center;
      justify-content: center; color: #fff; font-size: 1.1rem;
      margin-bottom: 14px;
    }
    .edu-degree { font-size: 0.95rem; font-weight: 700; color: var(--primary); margin-bottom: 4px; }
    .edu-uni { font-size: 0.82rem; color: var(--muted); margin-bottom: 10px; }
    .edu-meta {
      display: flex; justify-content: space-between;
      font-size: 0.8rem;
    }
    .edu-year { color: var(--muted); font-weight: 500; }
    .edu-grade {
      background: var(--gradient); -webkit-background-clip: text;
      -webkit-text-fill-color: transparent; background-clip: text;
      font-weight: 700;
    }
    .edu-badge {
      display: inline-block;
      background: #fff3cd; color: #856404;
      padding: 2px 10px; border-radius: 20px;
      font-size: 0.72rem; font-weight: 700;
      margin-top: 8px; border: 1px solid #ffd700;
    }

    /* ───── SKILLS ───── */
    .skills-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(280px,1fr));
      gap: 22px;
    }
    .skill-category {
      background: var(--card); border-radius: 18px;
      padding: 26px 24px; border: 1px solid var(--border);
      box-shadow: 0 4px 20px rgba(0,0,0,0.05);
    }
    .skill-cat-title {
      font-size: 0.85rem; font-weight: 700; text-transform: uppercase;
      letter-spacing: 1px; color: var(--primary); margin-bottom: 18px;
      display: flex; align-items: center; gap: 8px;
    }
    .skill-cat-title i { color: var(--accent); }
    .skill-item {
      margin-bottom: 14px;
    }
    .skill-meta {
      display: flex; justify-content: space-between;
      font-size: 0.82rem; margin-bottom: 6px;
    }
    .skill-name { font-weight: 600; color: var(--text); }
    .skill-pct { color: var(--muted); font-weight: 500; }
    .skill-bar {
      height: 7px; background: #e2e8f0; border-radius: 10px; overflow: hidden;
    }
    .skill-fill {
      height: 100%; border-radius: 10px;
      background: var(--gradient);
      transition: width 1.5s ease;
      width: 0;
    }

    /* ───── PUBLICATIONS ───── */
    .pub-list { display: flex; flex-direction: column; gap: 16px; }
    .pub-card {
      background: var(--card); border-radius: 14px;
      padding: 20px 24px; border: 1px solid var(--border);
      border-left: 4px solid var(--primary);
      box-shadow: 0 2px 15px rgba(0,0,0,0.05);
      display: flex; align-items: flex-start; gap: 16px;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .pub-card:hover { transform: translateX(4px); box-shadow: 0 6px 25px rgba(15,76,129,0.12); }
    .pub-num {
      width: 34px; height: 34px; border-radius: 10px;
      background: var(--gradient); color: #fff;
      display: flex; align-items: center; justify-content: center;
      font-size: 0.85rem; font-weight: 700; flex-shrink: 0; margin-top: 2px;
    }
    .pub-text { font-size: 0.9rem; color: var(--text); line-height: 1.6; }
    .pub-text strong { color: var(--primary); }

    /* ───── PATENTS ───── */
    .patents-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(300px,1fr));
      gap: 22px;
    }
    .patent-card {
      background: var(--card); border-radius: 18px;
      padding: 26px 24px; border: 1px solid var(--border);
      box-shadow: 0 4px 20px rgba(0,0,0,0.05);
      transition: all 0.3s; position: relative; overflow: hidden;
    }
    .patent-card::after {
      content: '';
      position: absolute; top: -30px; right: -30px;
      width: 90px; height: 90px; border-radius: 50%;
      background: rgba(15,76,129,0.06);
    }
    .patent-card:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(15,76,129,0.15); }
    .patent-type {
      display: inline-flex; align-items: center; gap: 6px;
      background: #e8f4fd; color: var(--primary);
      padding: 4px 12px; border-radius: 20px;
      font-size: 0.75rem; font-weight: 700; margin-bottom: 12px;
      text-transform: uppercase; letter-spacing: 0.5px;
    }
    .patent-title {
      font-size: 0.95rem; font-weight: 700; color: var(--text);
      margin-bottom: 8px; line-height: 1.5;
    }
    .patent-id {
      font-size: 0.8rem; color: var(--muted); font-family: monospace;
    }
    .patent-status {
      display: inline-block; margin-top: 10px;
      padding: 3px 10px; border-radius: 20px;
      font-size: 0.75rem; font-weight: 600;
    }
    .status-granted { background: #d4edda; color: #155724; }
    .status-process { background: #fff3cd; color: #856404; }

    /* ───── ACHIEVEMENTS ───── */
    .achieve-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(180px,1fr));
      gap: 20px;
    }
    .achieve-card {
      background: var(--card); border-radius: 18px;
      padding: 28px 20px; text-align: center;
      border: 1px solid var(--border);
      box-shadow: 0 4px 20px rgba(0,0,0,0.05);
      transition: all 0.3s; position: relative; overflow: hidden;
    }
    .achieve-card::before {
      content: ''; position: absolute; inset: 0;
      background: var(--gradient); opacity: 0; transition: opacity 0.3s;
    }
    .achieve-card:hover::before { opacity: 1; }
    .achieve-card:hover .achieve-num,
    .achieve-card:hover .achieve-label,
    .achieve-card:hover .achieve-icon { color: #fff !important; -webkit-text-fill-color: #fff !important; }
    .achieve-icon {
      font-size: 1.8rem; color: var(--accent);
      margin-bottom: 10px; display: block;
      position: relative; z-index: 1; transition: color 0.3s;
    }
    .achieve-num {
      font-size: 2.6rem; font-weight: 900;
      background: var(--gradient); -webkit-background-clip: text;
      -webkit-text-fill-color: transparent; background-clip: text;
      display: block; line-height: 1;
      position: relative; z-index: 1; transition: all 0.3s;
    }
    .achieve-label {
      font-size: 0.78rem; color: var(--muted);
      text-transform: uppercase; letter-spacing: 1px;
      margin-top: 6px; font-weight: 600;
      position: relative; z-index: 1; transition: color 0.3s;
    }

    /* ───── FDP TABLE ───── */
    .fdp-table-wrap {
      background: var(--card); border-radius: 18px;
      overflow: hidden; border: 1px solid var(--border);
      box-shadow: 0 4px 20px rgba(0,0,0,0.05);
    }
    table { width: 100%; border-collapse: collapse; }
    thead { background: var(--gradient); }
    thead th {
      padding: 14px 20px; color: #fff;
      font-size: 0.82rem; font-weight: 700;
      text-transform: uppercase; letter-spacing: 1px; text-align: left;
    }
    tbody tr { border-bottom: 1px solid var(--border); transition: background 0.2s; }
    tbody tr:last-child { border-bottom: none; }
    tbody tr:hover { background: #f8fbff; }
    tbody td {
      padding: 12px 20px; font-size: 0.85rem; color: var(--text);
    }
    .fdp-badge {
      display: inline-block; padding: 2px 10px;
      border-radius: 20px; font-size: 0.75rem; font-weight: 600;
    }
    .fdp-online { background: #d4edda; color: #155724; }
    .fdp-offline { background: #cce5ff; color: #004085; }

    /* ───── PERSONAL INFO ───── */
    .personal-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(240px,1fr));
      gap: 16px;
    }
    .personal-item {
      background: var(--card); border-radius: 14px;
      padding: 18px 22px; border: 1px solid var(--border);
      display: flex; align-items: center; gap: 14px;
      box-shadow: 0 2px 12px rgba(0,0,0,0.05);
    }
    .personal-icon {
      width: 40px; height: 40px; border-radius: 12px;
      background: var(--gradient); display: flex;
      align-items: center; justify-content: center;
      color: #fff; font-size: 1rem; flex-shrink: 0;
    }
    .personal-label {
      font-size: 0.72rem; color: var(--muted);
      text-transform: uppercase; letter-spacing: 1px; font-weight: 600;
    }
    .personal-value { font-size: 0.9rem; font-weight: 600; color: var(--text); }

    /* ───── FOOTER ───── */
    footer {
      background: var(--primary); color: rgba(255,255,255,0.85);
      text-align: center; padding: 32px 20px;
      font-size: 0.88rem;
    }
    footer strong { color: #fff; }
    footer a { color: var(--accent2); text-decoration: none; }

    /* ───── RESPONSIVE ───── */
    @media (max-width: 768px) {
      nav { padding: 0 20px; }
      .nav-links { display: none; }
      .hero h1 { font-size: 2.2rem; }
      main { padding: 40px 16px; }
      .stats-inner { grid-template-columns: repeat(2,1fr); }
      .stat-item { border-right: none; border-bottom: 1px solid var(--border); }
    }

    /* ───── ANIMATIONS ───── */
    .fade-in {
      opacity: 0; transform: translateY(30px);
      transition: opacity 0.7s ease, transform 0.7s ease;
    }
    .fade-in.visible { opacity: 1; transform: translateY(0); }

    .count-up { display: inline-block; }
  </style>
</head>
<body>

<!-- ── NAVIGATION ── -->
<nav>
  <div class="nav-brand">Aman Kapoor</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#publications">Publications</a></li>
    <li><a href="#patents">Patents</a></li>
    <li><a href="#achievements">Achievements</a></li>
  </ul>
</nav>

<!-- ── HERO ── -->
<section class="hero">
  <div class="hero-particles" id="particles"></div>
  <div style="position:relative;z-index:2;">
    <div class="hero-avatar"><i class="fas fa-microscope"></i></div>
    <h1>Aman Kapoor</h1>
    <p class="hero-degree">M.Pharmacy · Pharmaceutical Analysis &amp; Quality Assurance</p>
    <p class="hero-tagline">
      Pharmaceutical Scientist &amp; Assistant Professor | Analytical Method Development |
      AI-Powered Drug Discovery | 3 Patents · 7 Publications
    </p>
    <div class="hero-badges">
      <span class="badge"><i class="fas fa-flask"></i> RP-HPLC Expert</span>
      <span class="badge"><i class="fas fa-graduation-cap"></i> Ph.D. Candidate</span>
      <span class="badge"><i class="fas fa-lightbulb"></i> Innovator &amp; Inventor</span>
      <span class="badge"><i class="fas fa-chalkboard-teacher"></i> Academic Professional</span>
    </div>
    <div class="hero-contacts">
      <a class="contact-btn primary" href="/cdn-cgi/l/email-protection#50313d313e3b31203f3f222031213110373d31393c7e333f3d">
        <i class="fas fa-envelope"></i> <span class="__cf_email__" data-cfemail="ef8e828e81848e9f80809d9f8e9e8eaf88828e8683c18c8082">[email&#160;protected]</span>
      </a>
      <a class="contact-btn outline" href="tel:+916005132478">
        <i class="fas fa-phone"></i> +91 6005132478
      </a>
      <a class="contact-btn outline" href="#about">
        <i class="fas fa-user"></i> View Profile
      </a>
    </div>
  </div>
  <div class="scroll-indicator"><i class="fas fa-chevron-down"></i></div>
</section>

<!-- ── STATS BAR ── -->
<div class="stats-bar" id="stats">
  <div class="stats-inner">
    <div class="stat-item">
      <span class="stat-num count-up" data-target="5">0</span>
      <div class="stat-label">Years Experience</div>
    </div>
    <div class="stat-item">
      <span class="stat-num count-up" data-target="7">0</span>
      <div class="stat-label">Papers Published</div>
    </div>
    <div class="stat-item">
      <span class="stat-num count-up" data-target="3">0</span>
      <div class="stat-label">Patents</div>
    </div>
    <div class="stat-item">
      <span class="stat-num count-up" data-target="2">0</span>
      <div class="stat-label">Copyrights</div>
    </div>
    <div class="stat-item">
      <span class="stat-num count-up" data-target="46">0</span>
      <div class="stat-label">Intl. Conferences</div>
    </div>
    <div class="stat-item">
      <span class="stat-num count-up" data-target="17">0</span>
      <div class="stat-label">Natl. Conferences</div>
    </div>
  </div>
</div>

<main>

  <!-- ── OBJECTIVE ── -->
  <section id="about" class="fade-in">
    <div class="section-header">
      <div class="section-icon"><i class="fas fa-bullseye"></i></div>
      <h2 class="section-title">Career Objective</h2>
      <div class="section-line"></div>
    </div>
    <div class="objective-card">
      <p>
        Pharmaceutical Analysis &amp; Quality Assurance post-graduate with <strong>5+ years</strong> of
        academic and research experience — with proven expertise in <strong>analytical method
        development</strong>, instrumental analysis, and pharmaceutical teaching. Known for managing
        regulatory documentation, PCI compliance, and lab infrastructure. Holding <strong>3 patents</strong>
        in AI-powered drug discovery technologies, I am seeking a challenging role in pharma education or
        industry to contribute meaningfully while growing within an innovative, research-driven organization.
      </p>
    </div>
  </section>

  <!-- ── EXPERIENCE ── -->
  <section id="experience" class="fade-in">
    <div class="section-header">
      <div class="section-icon"><i class="fas fa-briefcase"></i></div>
      <h2 class="section-title">Work Experience</h2>
      <div class="section-line"></div>
    </div>
    <div class="timeline">

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="exp-card">
          <div class="exp-top">
            <div class="exp-role">Assistant Professor</div>
            <span class="exp-duration">Aug 2025 – Present</span>
          </div>
          <div class="exp-org">
            <i class="fas fa-university"></i>
            Prabha Harjilal College of Pharmacy &amp; Paraclinical Sciences, Jammu
          </div>
          <div class="exp-tags">
            <span class="exp-tag">Pharmaceutical Analysis</span>
            <span class="exp-tag">Quality Assurance</span>
            <span class="exp-tag">Academic Research</span>
            <span class="exp-tag">Lab Management</span>
          </div>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="exp-card">
          <div class="exp-top">
            <div class="exp-role">Assistant Professor</div>
            <span class="exp-duration">Feb 2022 – Aug 2025 · 3.5 Years</span>
          </div>
          <div class="exp-org">
            <i class="fas fa-university"></i>
            SVS Pharmacy College, Rajouri
          </div>
          <div class="exp-tags">
            <span class="exp-tag">Method Development</span>
            <span class="exp-tag">RP-HPLC</span>
            <span class="exp-tag">PCI Compliance</span>
            <span class="exp-tag">Regulatory Documentation</span>
            <span class="exp-tag">UV Spectroscopy</span>
          </div>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="exp-card">
          <div class="exp-top">
            <div class="exp-role">Lecturer</div>
            <span class="exp-duration">Jun 2020 – Jan 2022 · 1.7 Years</span>
          </div>
          <div class="exp-org">
            <i class="fas fa-school"></i>
            SVS Paramedical College, Rajouri
          </div>
          <div class="exp-tags">
            <span class="exp-tag">Pharmaceutical Teaching</span>
            <span class="exp-tag">Instrumentation</span>
            <span class="exp-tag">Lab Instruction</span>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- ── EDUCATION ── -->
  <section id="education" class="fade-in">
    <div class="section-header">
      <div class="section-icon"><i class="fas fa-graduation-cap"></i></div>
      <h2 class="section-title">Education</h2>
      <div class="section-line"></div>
    </div>
    <div class="edu-grid">
      <div class="edu-card">
        <div class="edu-icon"><i class="fas fa-atom"></i></div>
        <div class="edu-degree">Ph.D. – Pharmaceutical Sciences</div>
        <div class="edu-uni">Desh Bhagat University, Punjab</div>
        <div class="edu-meta">
          <span class="edu-year">Pursuing</span>
          <span class="edu-grade">In Progress</span>
        </div>
        <span class="edu-badge">🔬 Ongoing Research</span>
      </div>
      <div class="edu-card">
        <div class="edu-icon"><i class="fas fa-flask"></i></div>
        <div class="edu-degree">M.Pharmacy – PA &amp; QA</div>
        <div class="edu-uni">Himachal Pradesh Technical University (HPTU)</div>
        <div class="edu-meta">
          <span class="edu-year">2020</span>
          <span class="edu-grade">8.55 CGPA</span>
        </div>
        <span class="edu-badge">🥉 3rd University Rank</span>
      </div>
      <div class="edu-card">
        <div class="edu-icon"><i class="fas fa-mortar-pestle"></i></div>
        <div class="edu-degree">B.Pharmacy</div>
        <div class="edu-uni">Himachal Pradesh Technical University (HPTU)</div>
        <div class="edu-meta">
          <span class="edu-year">2018</span>
          <span class="edu-grade">69.2%</span>
        </div>
      </div>
      <div class="edu-card">
        <div class="edu-icon"><i class="fas fa-school"></i></div>
        <div class="edu-degree">12th – CBSE</div>
        <div class="edu-uni">J.N.V Doda</div>
        <div class="edu-meta">
          <span class="edu-year">2013</span>
          <span class="edu-grade">65.8%</span>
        </div>
      </div>
      <div class="edu-card">
        <div class="edu-icon"><i class="fas fa-book"></i></div>
        <div class="edu-degree">10th – CBSE</div>
        <div class="edu-uni">J.N.V Doda</div>
        <div class="edu-meta">
          <span class="edu-year">2011</span>
          <span class="edu-grade">8.4 CGPA</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ── SKILLS ── -->
  <section id="skills" class="fade-in">
    <div class="section-header">
      <div class="section-icon"><i class="fas fa-cogs"></i></div>
      <h2 class="section-title">Skills &amp; Expertise</h2>
      <div class="section-line"></div>
    </div>
    <div class="skills-grid">
      <div class="skill-category">
        <div class="skill-cat-title"><i class="fas fa-vial"></i> Analytical Instrumentation</div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">RP-HPLC</span><span class="skill-pct">95%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="95"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">UV-Visible Spectrophotometer</span><span class="skill-pct">90%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="90"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">FT-IR Spectroscopy</span><span class="skill-pct">85%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="85"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">Dissolution Apparatus</span><span class="skill-pct">88%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="88"></div></div>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-cat-title"><i class="fas fa-brain"></i> Research &amp; Documentation</div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">Method Development &amp; Validation</span><span class="skill-pct">92%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="92"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">Regulatory Documentation</span><span class="skill-pct">85%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="85"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">PCI Compliance</span><span class="skill-pct">80%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="80"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">Scientific Writing</span><span class="skill-pct">88%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="88"></div></div>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-cat-title"><i class="fas fa-robot"></i> Emerging Tech &amp; AI</div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">AI Drug Discovery</span><span class="skill-pct">78%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="78"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">Molecular Screening</span><span class="skill-pct">75%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="75"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">Drug Interaction Analysis</span><span class="skill-pct">82%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="82"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-meta"><span class="skill-name">GC-MS / LC-MS Techniques</span><span class="skill-pct">80%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="80"></div></div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── PUBLICATIONS ── -->
  <section id="publications" class="fade-in">
    <div class="section-header">
      <div class="section-icon"><i class="fas fa-file-alt"></i></div>
      <h2 class="section-title">Research Publications</h2>
      <div class="section-line"></div>
    </div>
    <div class="pub-list">
      <div class="pub-card">
        <div class="pub-num">01</div>
        <div class="pub-text">Method Development and Validation for <strong>Multicomponent Analysis of Emtricitabine and Ritonavir</strong> in Bulk Drug by RP-HPLC</div>
      </div>
      <div class="pub-card">
        <div class="pub-num">02</div>
        <div class="pub-text">An Overview of <strong>Investigational Drugs for the Treatment of COVID-19</strong></div>
      </div>
      <div class="pub-card">
        <div class="pub-num">03</div>
        <div class="pub-text">A Review on <strong>GC-MS Hyphenated Technique</strong></div>
      </div>
      <div class="pub-card">
        <div class="pub-num">04</div>
        <div class="pub-text"><strong>LC–TOF-MS:</strong> An Influential Hyphenated Technique and Its Application</div>
      </div>
      <div class="pub-card">
        <div class="pub-num">05</div>
        <div class="pub-text"><strong>Quantitative Determination of Sulphur in Manikaran's Water</strong> (April 2024)</div>
      </div>
      <div class="pub-card">
        <div class="pub-num">06</div>
        <div class="pub-text">Qualitative Analysis of <strong>Water of Govind Sagar Lake, Bilaspur</strong></div>
      </div>
      <div class="pub-card">
        <div class="pub-num">07</div>
        <div class="pub-text">Analytical Method Development and Validation for the Simultaneous Estimation of <strong>Emtricitabine and Ritonavir</strong> in Bulk Drug by UV-Spectrophotometer and RP-HPLC</div>
      </div>
    </div>
  </section>

  <!-- ── PATENTS & COPYRIGHTS ── -->
  <section id="patents" class="fade-in">
    <div class="section-header">
      <div class="section-icon"><i class="fas fa-certificate"></i></div>
      <h2 class="section-title">Patents &amp; Copyrights</h2>
      <div class="section-line"></div>
    </div>
    <div class="patents-grid">
      <div class="patent-card">
        <div class="patent-type"><i class="fas fa-award"></i> Patent</div>
        <div class="patent-title">Drug Interaction Analysis Device</div>
        <div class="patent-id">ID: 165481-001 · Filed: 12/07/2025</div>
        <span class="patent-status status-granted">✓ Granted</span>
      </div>
      <div class="patent-card">
        <div class="patent-type"><i class="fas fa-award"></i> Patent</div>
        <div class="patent-title">AI-Powered Molecular Screening and Drug Discovery Device</div>
        <div class="patent-id">ID: 464823-001 · Filed: 07/07/2025</div>
        <span class="patent-status status-granted">✓ Granted</span>
      </div>
      <div class="patent-card">
        <div class="patent-type"><i class="fas fa-award"></i> Patent</div>
        <div class="patent-title">Portable Drug Interaction Analysis Device</div>
        <div class="patent-id">ID: 483600-001 · Filed: 12/12/2025</div>
        <span class="patent-status status-process">⏳ In Process</span>
      </div>
      <div class="patent-card">
        <div class="patent-type"><i class="fas fa-copyright"></i> Copyright</div>
        <div class="patent-title">Intelligent Drug Target Interaction Analysis Device</div>
        <div class="patent-id">ID: LD-28689/2025-CO</div>
        <span class="patent-status status-granted">✓ Registered</span>
      </div>
      <div class="patent-card">
        <div class="patent-type"><i class="fas fa-copyright"></i> Copyright</div>
        <div class="patent-title">AI-Powered Molecular Screening and Drug Discovery Platform</div>
        <div class="patent-id">ID: LD-27644/2025-CO</div>
        <span class="patent-status status-granted">✓ Registered</span>
      </div>
    </div>
  </section>

  <!-- ── ACHIEVEMENTS ── -->
  <section id="achievements" class="fade-in">
    <div class="section-header">
      <div class="section-icon"><i class="fas fa-trophy"></i></div>
      <h2 class="section-title">Achievements &amp; Conferences</h2>
      <div class="section-line"></div>
    </div>
    <div class="achieve-grid">
      <div class="achieve-card">
        <i class="achieve-icon fas fa-globe"></i>
        <span class="achieve-num count-up" data-target="46">0</span>
        <div class="achieve-label">International Conferences</div>
      </div>
      <div class="achieve-card">
        <i class="achieve-icon fas fa-flag"></i>
        <span class="achieve-num count-up" data-target="17">0</span>
        <div class="achieve-label">National Conferences</div>
      </div>
      <div class="achieve-card">
        <i class="achieve-icon fas fa-image"></i>
        <span class="achieve-num count-up" data-target="2">0</span>
        <div class="achieve-label">Poster Presentations</div>
      </div>
      <div class="achieve-card">
        <i class="achieve-icon fas fa-file-alt"></i>
        <span class="achieve-num count-up" data-target="7">0</span>
        <div class="achieve-label">Papers Published</div>
      </div>
      <div class="achieve-card">
        <i class="achieve-icon fas fa-lightbulb"></i>
        <span class="achieve-num count-up" data-target="3">0</span>
        <div class="achieve-label">Patents Filed</div>
      </div>
      <div class="achieve-card">
        <i class="achieve-icon fas fa-copyright"></i>
        <span class="achieve-num count-up" data-target="2">0</span>
        <div class="achieve-label">Copyrights</div>
      </div>
    </div>
  </section>

  <!-- ── FDP & WORKSHOPS ── -->
  <section id="fdp" class="fade-in">
    <div class="section-header">
      <div class="section-icon"><i class="fas fa-chalkboard-teacher"></i></div>
      <h2 class="section-title">FDPs &amp; Workshops</h2>
      <div class="section-line"></div>
    </div>
    <div class="fdp-table-wrap">
      <table>
        <thead>
          <tr>
            <th>#</th><th>Program</th><th>Organizer / Details</th><th>Date</th><th>Mode</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>1</td><td>AI Technology for Nanobiotechnology</td><td>RIPS, Bareilly (AKTU)</td><td>Jan 2026</td><td><span class="fdp-badge fdp-online">Online</span></td></tr>
          <tr><td>2</td><td>Bio-Entrepreneurship Workshop</td><td>NABI, Mohali</td><td>Feb 2026</td><td><span class="fdp-badge fdp-offline">Offline</span></td></tr>
          <tr><td>3</td><td>Current Advancements in Drug Discovery</td><td>Pharma Conference</td><td>May 2024</td><td><span class="fdp-badge fdp-online">Online</span></td></tr>
          <tr><td>4</td><td>Faculty Development Programs</td><td>Various Universities</td><td>Multiple</td><td><span class="fdp-badge fdp-online">Online</span></td></tr>
        </tbody>
      </table>
    </div>
  </section>

  <!-- ── PERSONAL DETAILS ── -->
  <section id="personal" class="fade-in">
    <div class="section-header">
      <div class="section-icon"><i class="fas fa-id-card"></i></div>
      <h2 class="section-title">Personal Details</h2>
      <div class="section-line"></div>
    </div>
    <div class="personal-grid">
      <div class="personal-item">
        <div class="personal-icon"><i class="fas fa-birthday-cake"></i></div>
        <div><div class="personal-label">Date of Birth</div><div class="personal-value">21st January, 1995</div></div>
      </div>
      <div class="personal-item">
        <div class="personal-icon"><i class="fas fa-flag"></i></div>
        <div><div class="personal-label">Nationality</div><div class="personal-value">Indian</div></div>
      </div>
      <div class="personal-item">
        <div class="personal-icon"><i class="fas fa-venus-mars"></i></div>
        <div><div class="personal-label">Gender</div><div class="personal-value">Male</div></div>
      </div>
      <div class="personal-item">
        <div class="personal-icon"><i class="fas fa-heart"></i></div>
        <div><div class="personal-label">Marital Status</div><div class="personal-value">Unmarried</div></div>
      </div>
      <div class="personal-item">
        <div class="personal-icon"><i class="fas fa-language"></i></div>
        <div><div class="personal-label">Languages</div><div class="personal-value">English, Hindi, Punjabi</div></div>
      </div>
      <div class="personal-item">
        <div class="personal-icon"><i class="fas fa-map-marker-alt"></i></div>
        <div><div class="personal-label">Location</div><div class="personal-value">Jammu – 181201, J&amp;K, India</div></div>
      </div>
      <div class="personal-item">
        <div class="personal-icon"><i class="fas fa-user-tie"></i></div>
        <div><div class="personal-label">Father's Name</div><div class="personal-value">Mr. Manmohan Kapoor</div></div>
      </div>
      <div class="personal-item">
        <div class="personal-icon"><i class="fas fa-user"></i></div>
        <div><div class="personal-label">Mother's Name</div><div class="personal-value">Mrs. Bharti Kapoor</div></div>
      </div>
    </div>
  </section>

</main>

<!-- ── FOOTER ── -->
<footer>
  <p>
    <strong>Aman Kapoor</strong> — Assistant Professor &amp; Pharmaceutical Researcher<br/>
    <i class="fas fa-envelope"></i>
    <a href="/cdn-cgi/l/email-protection#046569656a6f65746b6b7674657565446369656d682a676b69"><span class="__cf_email__" data-cfemail="31505c505f5a50415e5e434150405071565c50585d1f525e5c">[email&#160;protected]</span></a> &nbsp;|&nbsp;
    <i class="fas fa-phone"></i> +91 6005132478 &nbsp;|&nbsp;
    <i class="fas fa-map-marker-alt"></i> Jammu, J&amp;K, India
  </p>
  <p style="margin-top:12px;font-size:0.78rem;opacity:0.6;">
    © 2026 Aman Kapoor · Built with passion for science &amp; innovation
  </p>
</footer>

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
  // ── Particle generator ──
  const pc = document.getElementById('particles');
  for (let i = 0; i < 18; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    const s = Math.random() * 70 + 20;
    p.style.cssText = `
      width:${s}px; height:${s}px;
      left:${Math.random()*100}%; top:${Math.random()*100}%;
      animation-delay:${Math.random()*6}s;
      animation-duration:${Math.random()*6+6}s;
    `;
    pc.appendChild(p);
  }

  // ── Intersection Observer for fade-in ──
  const observer = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        // Trigger skill bars
        e.target.querySelectorAll('.skill-fill').forEach(bar => {
          bar.style.width = bar.dataset.width + '%';
        });
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

  // ── Count-up animation ──
  function countUp(el) {
    const target = +el.dataset.target;
    const duration = 1800;
    const step = target / (duration / 16);
    let current = 0;
    const timer = setInterval(() => {
      current += step;
      if (current >= target) { current = target; clearInterval(timer); }
      el.textContent = Math.floor(current) + (target > 10 ? '' : '');
    }, 16);
  }

  const statsObserver = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('.count-up').forEach(countUp);
        statsObserver.unobserve(e.target);
      }
    });
  }, { threshold: 0.3 });

  document.querySelectorAll('#stats, #achievements').forEach(el => statsObserver.observe(el));

  // ── Smooth active nav highlight ──
  const sections = document.querySelectorAll('section[id], div[id]');
  const navLinks = document.querySelectorAll('.nav-links a');
  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(s => {
      if (window.scrollY >= s.offsetTop - 100) current = s.id;
    });
    navLinks.forEach(a => {
      a.style.color = a.getAttribute('href') === '#' + current
        ? '#48cae4' : 'rgba(255,255,255,0.85)';
    });
  });
</script>
</body>
</html>
