<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Rithin Ragunathan — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #060610;
    --surface: #0d0d1f;
    --card: #111128;
    --border: rgba(100,120,255,0.18);
    --accent: #5b6ef5;
    --accent2: #a259ff;
    --accent3: #00f0c8;
    --text: #e8e8ff;
    --muted: #7878aa;
    --glow: rgba(91,110,245,0.35);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Animated starfield */
  .starfield {
    position: fixed; inset: 0; z-index: 0; pointer-events: none;
    overflow: hidden;
  }
  .star {
    position: absolute;
    border-radius: 50%;
    background: white;
    animation: twinkle var(--dur, 3s) ease-in-out infinite var(--delay, 0s);
  }
  @keyframes twinkle {
    0%, 100% { opacity: 0.1; transform: scale(1); }
    50% { opacity: 0.9; transform: scale(1.4); }
  }

  /* Floating orbs */
  .orb {
    position: fixed; border-radius: 50%; filter: blur(80px);
    pointer-events: none; z-index: 0; animation: drift var(--d,12s) ease-in-out infinite alternate;
  }
  @keyframes drift { from { transform: translate(0,0); } to { transform: translate(var(--tx,30px), var(--ty,20px)); } }

  .orb1 { width:380px; height:380px; background: rgba(91,110,245,0.18); top:-80px; left:-100px; --d:14s; --tx:40px; --ty:50px; }
  .orb2 { width:300px; height:300px; background: rgba(162,89,255,0.15); bottom:0; right:-80px; --d:11s; --tx:-30px; --ty:-40px; }
  .orb3 { width:200px; height:200px; background: rgba(0,240,200,0.1); top:50%; left:50%; --d:9s; --tx:60px; --ty:-30px; }

  .container {
    position: relative; z-index: 1;
    max-width: 860px;
    margin: 0 auto;
    padding: 48px 24px 80px;
  }

  /* Hero */
  .hero {
    text-align: center;
    padding: 56px 0 48px;
    position: relative;
  }
  .hero-ring {
    display: inline-block;
    position: relative;
    margin-bottom: 28px;
  }
  .avatar-placeholder {
    width: 110px; height: 110px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    display: flex; align-items: center; justify-content: center;
    font-size: 48px;
    position: relative;
    z-index: 1;
    animation: pulse-avatar 3s ease-in-out infinite;
  }
  @keyframes pulse-avatar {
    0%,100% { box-shadow: 0 0 0 0 rgba(91,110,245,0.4), 0 0 32px rgba(91,110,245,0.3); }
    50% { box-shadow: 0 0 0 16px rgba(91,110,245,0), 0 0 48px rgba(162,89,255,0.5); }
  }
  .ring-svg {
    position: absolute; inset: -14px;
    animation: spin-ring 8s linear infinite;
  }
  @keyframes spin-ring { to { transform: rotate(360deg); } }

  .hero h1 {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: clamp(2rem, 5vw, 3.2rem);
    letter-spacing: -1px;
    background: linear-gradient(90deg, var(--accent), var(--accent2), var(--accent3));
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    animation: fadeUp 0.8s ease both;
  }
  .hero .tagline {
    font-size: 0.88rem;
    color: var(--muted);
    margin-top: 10px;
    letter-spacing: 0.08em;
    animation: fadeUp 0.8s 0.15s ease both;
  }

  /* Typing text */
  .typing-wrap {
    margin-top: 20px;
    animation: fadeUp 0.8s 0.3s ease both;
    height: 28px;
  }
  .typing {
    font-family: 'Space Mono', monospace;
    font-size: 0.95rem;
    color: var(--accent3);
    border-right: 2px solid var(--accent3);
    white-space: nowrap;
    overflow: hidden;
    display: inline-block;
    animation: blink-cursor 0.7s step-end infinite;
  }
  @keyframes blink-cursor { 50% { border-color: transparent; } }

  /* Status badge */
  .status {
    display: inline-flex; align-items: center; gap: 8px;
    margin-top: 22px;
    padding: 7px 16px;
    border-radius: 100px;
    border: 1px solid var(--border);
    background: rgba(91,110,245,0.08);
    font-size: 0.78rem;
    color: var(--muted);
    animation: fadeUp 0.8s 0.45s ease both;
  }
  .status-dot {
    width: 8px; height: 8px; border-radius: 50%;
    background: var(--accent3);
    animation: pulse-dot 1.5s ease infinite;
  }
  @keyframes pulse-dot {
    0%,100% { box-shadow: 0 0 0 0 rgba(0,240,200,0.5); }
    50% { box-shadow: 0 0 0 6px rgba(0,240,200,0); }
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(22px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Section */
  .section {
    margin-top: 48px;
    animation: fadeUp 0.8s ease both;
  }
  .section-label {
    font-family: 'Syne', sans-serif;
    font-size: 0.72rem;
    letter-spacing: 0.22em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 18px;
    display: flex; align-items: center; gap: 10px;
  }
  .section-label::after {
    content:''; flex: 1; height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* Grid cards */
  .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  @media(max-width:600px) { .grid-2 { grid-template-columns: 1fr; } }

  .card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 22px;
    transition: border-color 0.3s, transform 0.3s, box-shadow 0.3s;
    position: relative; overflow: hidden;
  }
  .card::before {
    content:''; position: absolute;
    inset: 0; border-radius: inherit;
    background: linear-gradient(135deg, rgba(91,110,245,0.06), transparent 60%);
    pointer-events: none;
  }
  .card:hover {
    border-color: var(--accent);
    transform: translateY(-4px);
    box-shadow: 0 12px 40px rgba(91,110,245,0.2);
  }
  .card-icon { font-size: 1.6rem; margin-bottom: 12px; }
  .card-title {
    font-family: 'Syne', sans-serif;
    font-size: 0.95rem; font-weight: 700;
    color: var(--text);
    margin-bottom: 6px;
  }
  .card-desc { font-size: 0.78rem; color: var(--muted); line-height: 1.65; }

  /* Tech stack pills */
  .pills { display: flex; flex-wrap: wrap; gap: 10px; }
  .pill {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 6px 14px;
    border-radius: 100px;
    border: 1px solid var(--border);
    background: var(--card);
    font-size: 0.78rem;
    color: var(--text);
    transition: all 0.25s;
    cursor: default;
    position: relative; overflow: hidden;
  }
  .pill::after {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    opacity: 0; transition: opacity 0.25s;
    border-radius: inherit;
  }
  .pill:hover::after { opacity: 0.12; }
  .pill:hover { border-color: var(--accent); transform: scale(1.05); }
  .pill-dot { width: 7px; height: 7px; border-radius: 50%; }

  /* Learning path */
  .path-list { display: flex; flex-direction: column; gap: 0; }
  .path-item {
    display: flex; align-items: flex-start; gap: 16px;
    padding: 14px 0;
    border-bottom: 1px solid rgba(100,120,255,0.07);
    transition: background 0.2s;
  }
  .path-item:last-child { border-bottom: none; }
  .path-num {
    font-family: 'Syne', sans-serif;
    font-size: 0.7rem; font-weight: 700;
    color: var(--accent);
    min-width: 28px;
    padding-top: 2px;
    letter-spacing: 0.05em;
  }
  .path-text { font-size: 0.85rem; color: var(--text); }
  .path-sub { font-size: 0.75rem; color: var(--muted); margin-top: 3px; }

  /* Progress bars */
  .progress-row { margin-bottom: 18px; }
  .progress-label {
    display: flex; justify-content: space-between;
    font-size: 0.78rem; color: var(--muted);
    margin-bottom: 6px;
  }
  .progress-label span:first-child { color: var(--text); }
  .bar-bg {
    height: 6px; border-radius: 99px;
    background: rgba(255,255,255,0.05);
    overflow: hidden;
  }
  .bar-fill {
    height: 100%; border-radius: 99px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    width: 0%;
    transition: width 1.4s cubic-bezier(0.4,0,0.2,1);
  }
  .bar-fill.green { background: linear-gradient(90deg, var(--accent3), #00b894); }
  .bar-fill.purple { background: linear-gradient(90deg, var(--accent2), #e056fd); }

  /* Stats card */
  .stats-row { display: flex; gap: 16px; flex-wrap: wrap; }
  .stat-box {
    flex: 1; min-width: 120px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 18px;
    text-align: center;
    transition: all 0.3s;
    position: relative; overflow: hidden;
  }
  .stat-box:hover { border-color: var(--accent2); transform: translateY(-3px); box-shadow: 0 8px 30px rgba(162,89,255,0.2); }
  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 1.8rem; font-weight: 800;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  }
  .stat-lbl { font-size: 0.7rem; color: var(--muted); margin-top: 4px; letter-spacing: 0.05em; }

  /* Currently building */
  .build-card {
    background: linear-gradient(135deg, rgba(91,110,245,0.1), rgba(162,89,255,0.08));
    border: 1px solid rgba(91,110,245,0.3);
    border-radius: 18px;
    padding: 28px;
    position: relative; overflow: hidden;
  }
  .build-card::before {
    content: '';
    position: absolute; top: -40px; right: -40px;
    width: 180px; height: 180px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(162,89,255,0.15), transparent 70%);
  }
  .build-title {
    font-family: 'Syne', sans-serif;
    font-size: 1.1rem; font-weight: 700;
    margin-bottom: 8px;
  }
  .build-desc { font-size: 0.82rem; color: var(--muted); line-height: 1.7; }
  .build-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 16px; }
  .build-tag {
    padding: 4px 12px; border-radius: 100px;
    background: rgba(91,110,245,0.15);
    border: 1px solid rgba(91,110,245,0.25);
    font-size: 0.72rem; color: var(--accent);
  }

  /* Connect */
  .connect-row { display: flex; gap: 14px; flex-wrap: wrap; }
  .connect-btn {
    display: inline-flex; align-items: center; gap: 10px;
    padding: 12px 22px;
    border-radius: 12px;
    border: 1px solid var(--border);
    background: var(--card);
    color: var(--text);
    text-decoration: none;
    font-family: 'Space Mono', monospace;
    font-size: 0.82rem;
    transition: all 0.25s;
  }
  .connect-btn:hover {
    border-color: var(--accent);
    box-shadow: 0 0 20px rgba(91,110,245,0.25);
    transform: translateY(-2px);
  }
  .connect-btn svg { width: 18px; height: 18px; }

  /* Footer */
  .footer {
    text-align: center;
    margin-top: 64px;
    font-size: 0.75rem;
    color: var(--muted);
    letter-spacing: 0.1em;
  }
  .footer span { color: var(--accent3); }

  /* Scroll animation observer */
  .reveal { opacity: 0; transform: translateY(30px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .reveal.visible { opacity: 1; transform: none; }
</style>
</head>
<body>

<!-- Starfield -->
<div class="starfield" id="starfield"></div>
<div class="orb orb1"></div>
<div class="orb orb2"></div>
<div class="orb orb3"></div>

<div class="container">

  <!-- Hero -->
  <div class="hero">
    <div class="hero-ring">
      <div class="avatar-placeholder">👨‍💻</div>
      <svg class="ring-svg" viewBox="0 0 138 138" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="69" cy="69" r="64" stroke="url(#rg)" stroke-width="2" stroke-dasharray="8 6" stroke-linecap="round"/>
        <defs>
          <linearGradient id="rg" x1="0" y1="0" x2="138" y2="138" gradientUnits="userSpaceOnUse">
            <stop stop-color="#5b6ef5"/>
            <stop offset="0.5" stop-color="#a259ff"/>
            <stop offset="1" stop-color="#00f0c8"/>
          </linearGradient>
        </defs>
      </svg>
    </div>

    <h1>Rithin Ragunathan</h1>
    <p class="tagline">ECE @ Bannari Amman Institute of Technology · Sathyamangalam</p>

    <div class="typing-wrap">
      <span class="typing" id="typer"></span>
    </div>

    <div class="status">
      <div class="status-dot"></div>
      Building AI/ML + Full Stack Systems · Open to Collaborate
    </div>
  </div>

  <!-- About cards -->
  <div class="section reveal">
    <div class="section-label">About</div>
    <div class="grid-2">
      <div class="card">
        <div class="card-icon">🧠</div>
        <div class="card-title">AI/ML Systems</div>
        <div class="card-desc">Deep interest in building ML pipelines from scratch — RAG, transformers, DeepStream, OpenCV. No shortcuts, always from first principles.</div>
      </div>
      <div class="card">
        <div class="card-icon">⚙️</div>
        <div class="card-title">Full Stack Dev</div>
        <div class="card-desc">Building real products with React, FastAPI, Node.js, PostgreSQL. Currently exploring Spring Boot vs Express architecture side by side.</div>
      </div>
      <div class="card">
        <div class="card-icon">🔬</div>
        <div class="card-title">Computer Vision</div>
        <div class="card-desc">YOLOv8/v11 with DeepStream pipelines, polygonal ROI tracking, people counting, and real-world measurement with OpenCV calibration.</div>
      </div>
      <div class="card">
        <div class="card-icon">📐</div>
        <div class="card-title">DSA & Problem Solving</div>
        <div class="card-desc">Structured Socratic approach to recursion, complexity reduction, and algorithm design. Depth and correctness over shortcuts.</div>
      </div>
    </div>
  </div>

  <!-- Tech Stack -->
  <div class="section reveal">
    <div class="section-label">Tech Stack</div>
    <div class="pills">
      <span class="pill"><span class="pill-dot" style="background:#f89820"></span>Java</span>
      <span class="pill"><span class="pill-dot" style="background:#555"></span>C</span>
      <span class="pill"><span class="pill-dot" style="background:#3572A5"></span>Python</span>
      <span class="pill"><span class="pill-dot" style="background:#e34c26"></span>HTML5</span>
      <span class="pill"><span class="pill-dot" style="background:#264de4"></span>CSS3</span>
      <span class="pill"><span class="pill-dot" style="background:#f7df1e"></span>JavaScript</span>
      <span class="pill"><span class="pill-dot" style="background:#00b894"></span>Node.js</span>
      <span class="pill"><span class="pill-dot" style="background:#61dafb"></span>React</span>
      <span class="pill"><span class="pill-dot" style="background:#009688"></span>FastAPI</span>
      <span class="pill"><span class="pill-dot" style="background:#336791"></span>PostgreSQL</span>
      <span class="pill"><span class="pill-dot" style="background:#4DB33D"></span>MongoDB</span>
      <span class="pill"><span class="pill-dot" style="background:#ff6b35"></span>OpenCV</span>
      <span class="pill"><span class="pill-dot" style="background:#ee4c2c"></span>PyTorch</span>
      <span class="pill"><span class="pill-dot" style="background:#f05032"></span>Git</span>
      <span class="pill"><span class="pill-dot" style="background:#e95420"></span>Linux</span>
      <span class="pill"><span class="pill-dot" style="background:#007acc"></span>VS Code</span>
    </div>
  </div>

  <!-- Skills progress -->
  <div class="section reveal">
    <div class="section-label">Skill Progress</div>
    <div class="card">
      <div class="progress-row">
        <div class="progress-label"><span>Java & DSA</span><span>75%</span></div>
        <div class="bar-bg"><div class="bar-fill" data-width="75"></div></div>
      </div>
      <div class="progress-row">
        <div class="progress-label"><span>Python / AI/ML</span><span>68%</span></div>
        <div class="bar-bg"><div class="bar-fill purple" data-width="68"></div></div>
      </div>
      <div class="progress-row">
        <div class="progress-label"><span>Full Stack (React + FastAPI)</span><span>60%</span></div>
        <div class="bar-bg"><div class="bar-fill" data-width="60"></div></div>
      </div>
      <div class="progress-row">
        <div class="progress-label"><span>Computer Vision / DeepStream</span><span>55%</span></div>
        <div class="bar-bg"><div class="bar-fill green" data-width="55"></div></div>
      </div>
      <div class="progress-row" style="margin-bottom:0">
        <div class="progress-label"><span>Linux & DevOps Basics</span><span>40%</span></div>
        <div class="bar-bg"><div class="bar-fill purple" data-width="40"></div></div>
      </div>
    </div>
  </div>

  <!-- Learning Path -->
  <div class="section reveal">
    <div class="section-label">Learning Path</div>
    <div class="card">
      <div class="path-list">
        <div class="path-item">
          <div class="path-num">01</div>
          <div><div class="path-text">🌐 Web Foundations</div><div class="path-sub">HTML · CSS · JavaScript — scratch to production</div></div>
        </div>
        <div class="path-item">
          <div class="path-num">02</div>
          <div><div class="path-text">⚙️ Backend Systems</div><div class="path-sub">Node.js / Express vs Spring Boot · REST APIs · Auth</div></div>
        </div>
        <div class="path-item">
          <div class="path-num">03</div>
          <div><div class="path-text">🗄️ Databases</div><div class="path-sub">PostgreSQL · MongoDB · SQL deep dives · Supabase</div></div>
        </div>
        <div class="path-item">
          <div class="path-num">04</div>
          <div><div class="path-text">🧠 AI/ML & GenAI</div><div class="path-sub">NumPy · Pandas · RAG from scratch · Transformers · LLM agents</div></div>
        </div>
        <div class="path-item">
          <div class="path-num">05</div>
          <div><div class="path-text">👁️ Computer Vision</div><div class="path-sub">OpenCV · DeepStream · YOLO pipelines · Real-world measurement</div></div>
        </div>
        <div class="path-item">
          <div class="path-num">06</div>
          <div><div class="path-text">🐧 Linux, Git & Deployment</div><div class="path-sub">Git/GitHub · Linux internals · CI/CD · Docker · Cloud basics</div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- Stats -->
  <div class="section reveal">
    <div class="section-label">GitHub Stats</div>
    <div class="stats-row">
      <div class="stat-box">
        <div class="stat-num" data-count="6">0</div>
        <div class="stat-lbl">Languages</div>
      </div>
      <div class="stat-box">
        <div class="stat-num" data-count="12">0</div>
        <div class="stat-lbl">Repositories</div>
      </div>
      <div class="stat-box">
        <div class="stat-num" data-count="5">0</div>
        <div class="stat-lbl">Projects</div>
      </div>
      <div class="stat-box">
        <div class="stat-num" data-count="365">0</div>
        <div class="stat-lbl">Days Learning</div>
      </div>
    </div>
  </div>

  <!-- Currently Building -->
  <div class="section reveal">
    <div class="section-label">Currently Building</div>
    <div class="build-card">
      <div class="build-title">🤖 AI-Powered Personalized Study Mentor</div>
      <div class="build-desc">
        A full-stack, ML-integrated web app designed as both a college submission and a real deployable product.
        Adaptive learning paths, YouTube integration, voice-enabled sessions, and Claude AI at its core.
      </div>
      <div class="build-tags">
        <span class="build-tag">FastAPI</span>
        <span class="build-tag">React + Tailwind</span>
        <span class="build-tag">Claude API</span>
        <span class="build-tag">PostgreSQL / Supabase</span>
        <span class="build-tag">YouTube Data API</span>
        <span class="build-tag">Cloudinary</span>
        <span class="build-tag">WebSpeech API</span>
      </div>
    </div>
  </div>

  <!-- Connect -->
  <div class="section reveal">
    <div class="section-label">Connect</div>
    <div class="connect-row">
      <a class="connect-btn" href="https://www.linkedin.com/in/rithinragunathan" target="_blank">
        <svg viewBox="0 0 24 24" fill="#0a66c2"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a class="connect-btn" href="https://github.com/rithinragunathan" target="_blank">
        <svg viewBox="0 0 24 24" fill="white"><path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/></svg>
        GitHub
      </a>
    </div>
  </div>

  <div class="footer">
    <span>✨</span> Work in progress — learning every single day <span>✨</span>
  </div>

</div>

<script>
// Stars
const sf = document.getElementById('starfield');
for(let i=0;i<120;i++){
  const s=document.createElement('div');
  s.className='star';
  const sz=Math.random()*2.5+0.5;
  s.style.cssText=`width:${sz}px;height:${sz}px;top:${Math.random()*100}%;left:${Math.random()*100}%;--dur:${2+Math.random()*4}s;--delay:${Math.random()*4}s`;
  sf.appendChild(s);
}

// Typing effect
const phrases = [
  'Building AI systems from scratch...',
  'Exploring Full Stack Development...',
  'Deep diving into Computer Vision...',
  'Learning every single day...',
  'ECE student × AI/ML enthusiast...',
];
let pi=0, ci=0, deleting=false;
const typer=document.getElementById('typer');
function typeStep(){
  const phrase=phrases[pi];
  if(!deleting){
    typer.textContent=phrase.slice(0,ci+1);
    ci++;
    if(ci===phrase.length){ deleting=true; setTimeout(typeStep,1800); return; }
  } else {
    typer.textContent=phrase.slice(0,ci-1);
    ci--;
    if(ci===0){ deleting=false; pi=(pi+1)%phrases.length; }
  }
  setTimeout(typeStep, deleting?40:60);
}
typeStep();

// Scroll reveal
const obs = new IntersectionObserver(entries=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      e.target.classList.add('visible');
      // Animate bars
      e.target.querySelectorAll('.bar-fill').forEach(b=>{
        b.style.width = (b.dataset.width||0)+'%';
      });
      // Animate counters
      e.target.querySelectorAll('.stat-num[data-count]').forEach(el=>{
        const target=+el.dataset.count;
        let cur=0;
        const step=Math.ceil(target/40);
        const t=setInterval(()=>{
          cur=Math.min(cur+step, target);
          el.textContent=cur+(target===365?'':'+');
          if(cur>=target) clearInterval(t);
        },30);
      });
    }
  });
},{threshold:0.15});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));
</script>
</body>
</html>
