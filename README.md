<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Shannyth Solsol Olanos - GitHub Profile</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      background: #0d0d0d;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      min-height: 100vh;
      padding: 20px;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    }
    .wrap {
      width: 100%;
      max-width: 900px;
      background: #0d0d0d;
      color: #e6edf3;
      border-radius: 14px;
      overflow: hidden;
      border: 0.5px solid #1a1a1a;
    }

    /* HERO */
    .hero {
      background: linear-gradient(180deg, #1a0000 0%, #2a0000 50%, #0d0d0d 100%);
      padding: 0 0 28px;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    .hero-dots {
      position: absolute; top: 0; left: 0; width: 100%; height: 100%;
      background-image: radial-gradient(circle, #EE2C2C44 1px, transparent 1px);
      background-size: 28px 28px;
      opacity: 0.18;
      pointer-events: none;
    }
    .hero-glow-left {
      position: absolute; top: 0; left: 0;
      width: 40%; height: 100%;
      background: radial-gradient(ellipse at 20% 50%, #EE2C2C33 0%, transparent 70%);
      pointer-events: none;
    }
    .hero-glow-right {
      position: absolute; top: 0; right: 0;
      width: 40%; height: 100%;
      background: radial-gradient(ellipse at 80% 30%, #EE2C2C22 0%, transparent 60%);
      pointer-events: none;
    }

    /* AVATAR */
    .avatar-wrap {
      position: relative;
      display: inline-block;
      margin-top: 30px;
      z-index: 2;
    }
    .avatar-ring {
      width: 160px;
      height: 160px;
      border-radius: 50%;
      border: 3px solid #EE2C2C;
      overflow: hidden;
      display: inline-block;
      box-shadow: 0 0 24px #EE2C2C55, 0 0 48px #EE2C2C22;
    }
    .avatar-ring img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center top;
    }

    /* NAME & ROLES */
    .hero-name {
      font-size: 32px;
      font-weight: 800;
      color: #fff;
      margin-top: 14px;
      text-shadow: 0 0 30px #EE2C2C88;
      position: relative;
      z-index: 2;
    }
    .hero-roles {
      font-size: 15px;
      color: #ccc;
      font-weight: 500;
      line-height: 2;
      margin-top: 6px;
      position: relative;
      z-index: 2;
    }
    .hero-quote {
      font-size: 13px;
      color: #EE2C2C;
      font-style: italic;
      margin-top: 6px;
      position: relative;
      z-index: 2;
    }
    .typing-bar {
      display: inline-block;
      background: #1a0000;
      border: 0.5px solid #EE2C2C55;
      border-radius: 8px;
      padding: 7px 20px;
      margin-top: 12px;
      font-size: 13px;
      color: #EE2C2C;
      font-family: monospace;
      position: relative;
      z-index: 2;
    }

    .divider { height: 0.5px; background: #1a1a1a; margin: 0 20px; }

    /* MAIN GRID */
    .main-grid {
      display: grid;
      grid-template-columns: 1fr 230px;
      gap: 0;
    }
    .left  { padding: 18px 20px; }
    .right { padding: 18px 18px 18px 0; }

    .sec-title {
      font-size: 11px;
      font-weight: 700;
      color: #EE2C2C;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      margin-bottom: 12px;
    }

    /* OVERVIEW */
    .ov-item {
      font-size: 13px;
      color: #bbb;
      margin-bottom: 9px;
      display: flex;
      align-items: flex-start;
      gap: 8px;
      line-height: 1.5;
    }
    .ov-item strong { color: #fff; }
    .ov-item a { color: #EE2C2C; text-decoration: none; font-weight: 600; }
    .tag {
      background: #EE2C2C22;
      color: #EE2C2C;
      border-radius: 4px;
      padding: 1px 7px;
      font-size: 11px;
      font-weight: 600;
    }

    /* TECH BADGES */
    .tech-row { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 16px; }
    .tb {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 6px 14px;
      border-radius: 8px;
      font-size: 13px;
      font-weight: 600;
    }
    .tb-red  { background: #EE2C2C; color: #fff; }
    .tb-dark { background: #1a1a2e; color: #5ed8a0; border: 0.5px solid #3ECF8E55; }

    /* SPOTIFY */
    .spotify-label {
      font-size: 11px;
      font-weight: 700;
      color: #fff;
      background: #EE2C2C;
      border-radius: 20px;
      padding: 5px 14px;
      display: inline-flex;
      align-items: center;
      gap: 5px;
      margin-bottom: 10px;
    }
    .spotify-card {
      background: #1a1a2e;
      border: 0.5px solid #333;
      border-radius: 10px;
      padding: 12px;
    }
    .sp-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      font-size: 11px;
      color: #ccc;
      margin-bottom: 10px;
      font-weight: 600;
    }
    .sp-row {
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .sp-thumb {
      width: 40px;
      height: 40px;
      background: #2d2d2d;
      border-radius: 6px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      flex-shrink: 0;
    }
    .sp-track  { font-size: 13px; font-weight: 600; color: #fff; }
    .sp-artist { font-size: 11px; color: #aaa; margin-top: 2px; }
    .sp-bar    { height: 3px; background: #333; border-radius: 2px; margin-top: 10px; overflow: hidden; }
    .sp-fill   { height: 100%; width: 45%; background: #1DB954; border-radius: 2px; }

    /* METRICS */
    .metrics-section { padding: 0 20px 18px; }
    .metrics-title {
      font-size: 16px;
      font-weight: 700;
      color: #fff;
      margin-bottom: 14px;
    }
    .metrics-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
    }
    .metric-card {
      background: #1a1a1a;
      border: 0.5px solid #2a2a2a;
      border-radius: 10px;
      padding: 14px;
    }
    .mc-title { font-size: 12px; font-weight: 700; color: #EE2C2C; margin-bottom: 10px; }
    .mc-row {
      display: flex;
      justify-content: space-between;
      font-size: 12px;
      color: #bbb;
      margin-bottom: 6px;
    }
    .mc-row span:last-child { color: #fff; font-weight: 600; }

    /* LANG BARS */
    .lb-row { display: flex; justify-content: space-between; font-size: 11px; color: #bbb; margin-bottom: 3px; }
    .lb-row span:last-child { color: #fff; }
    .lb-bg  { background: #2a2a2a; border-radius: 3px; height: 6px; margin-bottom: 8px; overflow: hidden; }
    .lb-fill { height: 100%; border-radius: 3px; }

    /* CONTRIBUTION GRAPH */
    .contrib-section { padding: 0 20px 18px; }
    .contrib-months {
      display: flex;
      justify-content: space-between;
      font-size: 10px;
      color: #555;
      margin-bottom: 6px;
      padding-left: 32px;
    }
    .contrib-grid { display: flex; flex-direction: column; gap: 3px; }
    .contrib-row  { display: flex; align-items: center; gap: 3px; }
    .c-label { font-size: 9px; color: #555; width: 28px; flex-shrink: 0; }
    .c-cells { display: flex; gap: 3px; flex: 1; }
    .cc { flex: 1; aspect-ratio: 1; border-radius: 2px; min-width: 6px; }
    .cc0 { background: #1a1a1a; }
    .cc1 { background: #4a0a0a; }
    .cc2 { background: #8a1515; }
    .cc3 { background: #cc2020; }
    .cc4 { background: #EE2C2C; }
    .legend {
      display: flex;
      align-items: center;
      justify-content: flex-end;
      gap: 5px;
      margin-top: 8px;
      font-size: 10px;
      color: #555;
    }
    .lc { width: 10px; height: 10px; border-radius: 2px; }

    /* FOOTER */
    .footer {
      text-align: center;
      padding: 14px;
      background: #0a0a0a;
      border-top: 0.5px solid #1a1a1a;
      font-size: 11px;
      color: #444;
    }
  </style>
</head>
<body>
<div class="wrap">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-dots"></div>
    <div class="hero-glow-left"></div>
    <div class="hero-glow-right"></div>

    <!-- AVATAR con tu foto -->
    <div class="avatar-wrap">
      <div class="avatar-ring">
        <img src="5033120304598813727.jpg" alt="Shannyth Solsol Olanos"/>
      </div>
    </div>

    <div class="hero-name">Shannyth Solsol Olanos</div>
    <div class="hero-roles">
      Backend &amp; SQL Architect<br>
      Python Enthusiast<br>
      Curious as a Cat 🐈‍⬛<br>
      Connecting Code &amp; Music
    </div>
    <div class="hero-quote">"Bridging the Gap Between Code &amp; Coolness" 😎</div>
    <div class="typing-bar">▍ Software Engineering Student...</div>
  </div>

  <!-- MAIN GRID -->
  <div class="main-grid">

    <!-- LEFT -->
    <div class="left">
      <div class="sec-title">🚀 Overview</div>
      <div class="ov-item">🌱 <span><strong>Currently learning:</strong>
        <span class="tag">Advanced SQL</span>
        <span class="tag">Python</span>
        <span class="tag">Supabase</span>
        <span class="tag">ML</span>
      </span></div>
      <div class="ov-item">💬 <span><strong>Discuss:</strong> Backend Design, OOP, Deep Learning</span></div>
      <div class="ov-item">❤️ <span><strong>Reach me:</strong>
        <a href="https://www.instagram.com/shth_lll">Shannyth Solsol Olanos (Instagram)</a>
      </span></div>

      <!-- TECH BADGES -->
      <div class="tech-row">
        <span class="tb tb-red">🐍 Python</span>
        <span class="tb tb-red">🗄️ SQL</span>
        <span class="tb tb-red">🐘 PostgreSQL</span>
        <span class="tb tb-dark">⚡ Supabase</span>
        <span class="tb tb-red">🔀 Git</span>
        <span class="tb tb-red">🌐 HTML</span>
      </div>
    </div>

    <!-- RIGHT: SPOTIFY -->
    <div class="right">
      <div class="spotify-label">🎧 Shannyth's Backend Beats</div>
      <div class="spotify-card">
        <div class="sp-header">
          <span>Solsol Spotify Playing</span>
          <svg width="16" height="16" viewBox="0 0 24 24" fill="#1DB954">
            <path d="M12 0C5.4 0 0 5.4 0 12s5.4 12 12 12 12-5.4 12-12S18.66 0 12 0zm5.521 17.34c-.24.359-.66.48-1.021.24-2.82-1.74-6.36-2.101-10.561-1.141-.418.122-.779-.179-.899-.539-.12-.421.18-.78.54-.9 4.56-1.021 8.52-.6 11.64 1.32.42.18.479.659.301 1.02zm1.44-3.3c-.301.42-.841.6-1.262.3-3.239-1.98-8.159-2.58-11.939-1.38-.479.12-1.02-.12-1.14-.6-.12-.48.12-1.021.6-1.141C9.6 9.9 15 10.561 18.72 12.84c.361.181.54.78.241 1.2zm.12-3.36C15.24 8.4 8.82 8.16 5.16 9.301c-.6.179-1.2-.181-1.38-.721-.18-.601.18-1.2.72-1.381 4.26-1.26 11.28-1.02 15.721 1.621.539.3.719 1.02.419 1.56-.299.421-1.02.599-1.559.3z"/>
          </svg>
        </div>
        <div class="sp-row">
          <div class="sp-thumb">🎵</div>
          <div>
            <div class="sp-track">The Flight Imo Ban S...</div>
            <div class="sp-artist">Solsol</div>
          </div>
        </div>
        <div class="sp-bar"><div class="sp-fill"></div></div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- METRICS -->
  <div class="metrics-section" style="margin-top:18px">
    <div class="metrics-title">📊 Cat-tastic GitHub Metrics</div>
    <div class="metrics-grid">

      <div class="metric-card">
        <div class="mc-title">GitHub Stats</div>
        <div class="mc-row"><span>GitHub stats</span><span>92</span></div>
        <div class="mc-row"><span>Backend architectures</span><span>161</span></div>
        <div class="mc-row"><span>Reference theme</span><span>78</span></div>
        <div class="mc-row"><span>Contribution graph</span><span>1</span></div>
      </div>

      <div class="metric-card">
        <div class="mc-title">Top Langs</div>
        <div class="lb-row"><span>🐍 Python</span><span>53%</span></div>
        <div class="lb-bg"><div class="lb-fill" style="width:53%;background:#EE2C2C"></div></div>
        <div class="lb-row"><span>🗄️ SQL</span><span>11%</span></div>
        <div class="lb-bg"><div class="lb-fill" style="width:11%;background:#cc2020"></div></div>
        <div class="lb-row"><span>🐘 PostgreSQL</span><span>8%</span></div>
        <div class="lb-bg"><div class="lb-fill" style="width:8%;background:#aa1515"></div></div>
        <div class="lb-row"><span>⚡ Supabase</span><span>4%</span></div>
        <div class="lb-bg"><div class="lb-fill" style="width:4%;background:#881010"></div></div>
        <div class="lb-row"><span>🌐 HTML</span><span>3%</span></div>
        <div class="lb-bg"><div class="lb-fill" style="width:3%;background:#660a0a"></div></div>
      </div>

    </div>
  </div>

  <div class="divider"></div>

  <!-- CONTRIBUTION GRAPH -->
  <div class="contrib-section" style="margin-top:18px">
    <div class="sec-title">Activity Graph</div>
    <div class="contrib-months">
      <span>Jan</span><span>Feb</span><span>Mar</span><span>Apr</span>
      <span>May</span><span>Jun</span><span>Jul</span><span>Aug</span>
      <span>Sep</span><span>Oct</span><span>Nov</span><span>Dec</span>
    </div>
    <div class="contrib-grid">

      <div class="contrib-row">
        <div class="c-label">Nov</div>
        <div class="c-cells">
          <div class="cc cc0"></div><div class="cc cc1"></div><div class="cc cc2"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div>
        </div>
      </div>

      <div class="contrib-row">
        <div class="c-label">Dec</div>
        <div class="c-cells">
          <div class="cc cc1"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div>
        </div>
      </div>

      <div class="contrib-row">
        <div class="c-label">Jan</div>
        <div class="c-cells">
          <div class="cc cc0"></div><div class="cc cc1"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc2"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc3"></div><div class="cc cc4"></div><div class="cc cc4"></div><div class="cc cc4"></div>
        </div>
      </div>

    </div>
    <div class="legend">
      <span>Bord</span>
      <div class="lc" style="background:#1a1a1a;border:0.5px solid #333"></div>
      <div class="lc" style="background:#4a0a0a"></div>
      <div class="lc" style="background:#8a1515"></div>
      <div class="lc" style="background:#cc2020"></div>
      <div class="lc" style="background:#EE2C2C"></div>
      <span>High</span>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    Special contribution graph &nbsp;|&nbsp; Made with 🐈‍⬛ &amp; ❤️ by Shannyth Solsol Olanos
  </div>

</div>
</body>
</html>
