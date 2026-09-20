<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover"/>
<title>Kawin M.S — GitHub Profile README</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600;700&family=Inter:wght@400;500;600;700&display=swap');
  :root {
    --bg:#0d1117; --card:#0f1a12; --border:#1a3a25;
    --green:#10b981; --green2:#065f46; --white:#e6edf3;
    --muted:#8b949e; --active:#3fb950;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  body{background:var(--bg);color:var(--white);font-family:'Inter',sans-serif;font-size:15px;line-height:1.6;max-width:880px;margin:0 auto;padding:0 0 60px;}

  /* BANNER */
  .banner{width:100%;position:relative;background:linear-gradient(160deg,#0d1117 0%,#0a2a1a 55%,#10b98111 100%);padding:52px 32px 40px;text-align:center;overflow:hidden;}
  .grid-lines{position:absolute;inset:0;pointer-events:none;background-image:linear-gradient(to right,#10b98109 1px,transparent 1px),linear-gradient(to bottom,#10b98109 1px,transparent 1px);background-size:48px 48px;animation:gridMove 14s linear infinite;}
  @keyframes gridMove{from{background-position:0 0}to{background-position:48px 48px}}
  .banner h1{font-family:'Fira Code',monospace;font-size:44px;font-weight:700;color:#fff;letter-spacing:4px;position:relative;animation:glowPulse 3s ease-in-out infinite alternate;}
  @keyframes glowPulse{from{text-shadow:0 0 20px #10b98155}to{text-shadow:0 0 60px #10b981cc,0 0 100px #10b98144}}
  .banner .subtitle{font-family:'Fira Code',monospace;color:var(--green);font-size:13px;letter-spacing:2px;margin-top:5px;}
  .profile-photo{width:112px;height:112px;border-radius:50%;border:3px solid var(--green);box-shadow:0 0 0 6px #10b98122,0 0 40px #10b98144;margin:18px auto 0;display:block;animation:photoFloat 4s ease-in-out infinite;}
  @keyframes photoFloat{0%,100%{transform:translateY(0);box-shadow:0 0 0 6px #10b98122,0 0 30px #10b98144}50%{transform:translateY(-7px);box-shadow:0 0 0 9px #10b98133,0 0 55px #10b98166}}
  .typing-line{font-family:'Fira Code',monospace;font-size:14px;color:var(--green);margin-top:14px;min-height:22px;}
  .typing-line::after{content:'|';animation:blink .7s step-end infinite;color:var(--green);}
  @keyframes blink{50%{opacity:0}}
  .badges{display:flex;flex-wrap:wrap;justify-content:center;gap:7px;margin-top:16px;}
  .badge{display:inline-flex;align-items:center;gap:5px;padding:6px 13px;border-radius:6px;font-size:12px;font-weight:600;text-decoration:none;transition:transform .2s,box-shadow .2s;}
  .badge:hover{transform:translateY(-2px);box-shadow:0 4px 18px #10b98144;}
  .badge-green{background:#10b98120;color:var(--green);border:1px solid var(--green);}
  .badge-blue{background:#0A66C220;color:#4fa3e8;border:1px solid #0A66C2;}
  .badge-dark{background:#21262d;color:var(--white);border:1px solid #30363d;}
  .badge-red{background:#EA433520;color:#f87171;border:1px solid #EA4335;}

  /* SECTIONS */
  section{padding:28px 28px 0;}
  h2{font-family:'Fira Code',monospace;font-size:16px;color:var(--green);margin-bottom:16px;display:flex;align-items:center;gap:10px;}
  h2::after{content:'';flex:1;height:1px;background:linear-gradient(to right,var(--border),transparent);}
  hr{border:none;border-top:1px solid var(--border);margin:24px 28px 0;}

  /* CODE BLOCK */
  .code-block{background:#080e0b;border:1px solid var(--border);border-radius:10px;padding:18px 22px;font-family:'Fira Code',monospace;font-size:13px;line-height:1.85;position:relative;overflow:hidden;}
  .code-block::before{content:'● ● ●';position:absolute;top:10px;left:14px;font-size:11px;color:#2d4a38;letter-spacing:6px;}
  .code-block::after{content:'';position:absolute;left:0;right:0;height:2px;background:linear-gradient(to right,transparent,#10b98133,transparent);animation:scanLine 5s ease-in-out infinite;top:0;}
  @keyframes scanLine{0%{top:0;opacity:0}10%{opacity:1}90%{opacity:1}100%{top:100%;opacity:0}}
  .code-inner{margin-top:16px;}
  .kw{color:#ff79c6}.cls{color:#50fa7b}.str{color:#a8ff78}.key{color:#8be9fd}.cmt{color:#3d6b50}.arr{color:#bd93f9}

  /* TECH STACK */
  .stack-group{margin-bottom:14px;}
  .stack-label{font-family:'Fira Code',monospace;font-size:10px;color:var(--muted);letter-spacing:2px;text-transform:uppercase;margin-bottom:7px;}
  .pill-row{display:flex;flex-wrap:wrap;gap:6px;}
  .pill{display:inline-flex;align-items:center;gap:5px;padding:5px 11px;border-radius:6px;font-size:12px;font-weight:600;border:1px solid var(--border);background:var(--card);color:var(--white);transition:transform .15s,box-shadow .15s,border-color .15s;cursor:default;}
  .pill:hover{transform:translateY(-2px);box-shadow:0 3px 12px #10b98133;border-color:var(--green);}
  .pill img{width:14px;height:14px;object-fit:contain;}

  /* SKILL BARS */
  .skill-bars{display:flex;flex-direction:column;gap:11px;}
  .skill-row{display:flex;align-items:center;gap:12px;}
  .skill-name{font-family:'Fira Code',monospace;font-size:12px;color:var(--white);width:130px;flex-shrink:0;}
  .bar-track{flex:1;height:9px;background:#1a3a2522;border-radius:999px;border:1px solid var(--border);overflow:hidden;}
  .bar-fill{height:100%;border-radius:999px;background:linear-gradient(90deg,var(--green2),var(--green));box-shadow:0 0 8px #10b98188;transform:scaleX(0);transform-origin:left;animation:barGrow 1.4s cubic-bezier(.22,1,.36,1) forwards;}
  @keyframes barGrow{to{transform:scaleX(1)}}
  .skill-pct{font-family:'Fira Code',monospace;font-size:11px;color:var(--green);width:36px;text-align:right;}

  /* PROJECT CARDS */
  .projects-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px;}
  @media(max-width:580px){.projects-grid{grid-template-columns:1fr}}
  .project-card{background:var(--card);border:1px solid var(--border);border-radius:12px;padding:20px 18px 16px;position:relative;overflow:hidden;transition:transform .2s,box-shadow .2s,border-color .2s;}
  .project-card:hover{transform:translateY(-4px);box-shadow:0 10px 32px #10b98122;border-color:var(--green);}
  .project-card::before{content:'';position:absolute;top:0;left:0;width:40px;height:40px;background:linear-gradient(135deg,#10b98122,transparent);border-radius:0 0 40px 0;}
  .project-card::after{content:'';position:absolute;top:10px;right:10px;width:8px;height:8px;border-radius:50%;background:var(--green);box-shadow:0 0 6px var(--green);animation:pulse 2s ease-in-out infinite;}
  @keyframes pulse{0%,100%{box-shadow:0 0 4px var(--green)}50%{box-shadow:0 0 14px var(--green)}}
  .project-card h3{font-family:'Fira Code',monospace;font-size:14px;font-weight:700;color:var(--white);margin-bottom:8px;}
  .tag-row{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:10px;}
  .tag{font-size:10px;font-weight:600;padding:2px 8px;border-radius:4px;background:#10b98112;color:var(--green);border:1px solid #10b98133;font-family:'Fira Code',monospace;}
  .project-card p{font-size:12.5px;color:var(--muted);line-height:1.6;}

  /* STAT COUNTERS */
  .stat-counters{display:flex;gap:1px;background:var(--border);border:1px solid var(--border);border-radius:10px;overflow:hidden;margin-bottom:14px;}
  .stat-box{flex:1;background:var(--card);padding:16px 8px;text-align:center;}
  .stat-val{font-family:'Fira Code',monospace;font-size:24px;font-weight:700;color:var(--green);display:block;animation:countUp .6s ease-out;}
  @keyframes countUp{from{opacity:0;transform:translateY(8px)}to{opacity:1}}
  .stat-lbl{font-size:10px;color:var(--muted);margin-top:3px;}

  /* LANG BAR */
  .lang-bar-track{display:flex;height:8px;border-radius:999px;overflow:hidden;margin-bottom:10px;}
  .lang-segment{height:100%;}
  .lang-legend{display:flex;flex-wrap:wrap;gap:10px;}
  .lang-dot{display:flex;align-items:center;gap:5px;font-size:11px;font-family:'Fira Code',monospace;color:var(--muted);}
  .dot{width:9px;height:9px;border-radius:50%;flex-shrink:0;}

  /* CONTRIB GRID */
  .contrib-graph{margin-top:12px;background:#080e0b;border:1px solid var(--border);border-radius:10px;padding:16px;text-align:center;font-family:'Fira Code',monospace;font-size:10px;color:var(--muted);overflow:hidden;}
  .contrib-grid{display:grid;grid-template-columns:repeat(52,1fr);gap:2px;margin:8px 0 0;}
  .contrib-cell{aspect-ratio:1;border-radius:2px;background:#161b22;}

  /* EXPERIENCE */
  .exp-table{width:100%;border-collapse:collapse;}
  .exp-table th{font-family:'Fira Code',monospace;font-size:10px;color:var(--green);text-align:left;padding:8px 12px;border-bottom:1px solid var(--border);text-transform:uppercase;letter-spacing:1px;}
  .exp-table td{padding:11px 12px;font-size:13px;color:var(--white);border-bottom:1px solid #1a3a2533;}
  .exp-table tr:last-child td{border-bottom:none;}
  .exp-table tr:hover td{background:#10b98108;}
  .period-badge{font-family:'Fira Code',monospace;font-size:10px;color:var(--green);background:#10b98112;border:1px solid #10b98133;padding:2px 8px;border-radius:4px;}
  .active-dot{display:inline-block;width:7px;height:7px;border-radius:50%;background:var(--active);margin-right:5px;box-shadow:0 0 6px var(--active);animation:activePulse 1.5s ease-in-out infinite;}
  @keyframes activePulse{0%,100%{box-shadow:0 0 4px var(--active)}50%{box-shadow:0 0 12px var(--active)}}

  /* CERTS */
  .cert-list{list-style:none;display:flex;flex-direction:column;gap:8px;}
  .cert-list li{display:flex;align-items:flex-start;gap:10px;background:var(--card);border:1px solid var(--border);border-radius:8px;padding:11px 13px;font-size:13px;transition:border-color .2s;}
  .cert-list li:hover{border-color:var(--green);}
  .cert-icon{font-size:16px;flex-shrink:0;}
  .cert-title{font-weight:600;color:var(--white);font-size:13px;}
  .cert-org{font-size:11px;color:var(--muted);margin-top:2px;font-family:'Fira Code',monospace;}

  /* INTEGER.IO */
  .company-card{background:linear-gradient(135deg,#080e0b,#0a1f14);border:1px solid var(--green);border-radius:12px;padding:22px;position:relative;overflow:hidden;}
  .company-card::before{content:'';position:absolute;top:-40px;right:-40px;width:120px;height:120px;border-radius:50%;background:radial-gradient(circle,#10b98122,transparent);pointer-events:none;}
  .company-header{display:flex;align-items:center;gap:16px;margin-bottom:12px;}
  .company-logo{width:60px;height:60px;border-radius:50%;object-fit:cover;border:2px solid var(--green);background:#0a150f;flex-shrink:0;box-shadow:0 0 16px #10b98133;}
  .company-name{font-family:'Fira Code',monospace;font-size:20px;font-weight:700;color:var(--green);margin-bottom:3px;}
  .company-role{font-size:11px;color:var(--muted);font-family:'Fira Code',monospace;}
  .company-card p{font-size:13px;color:var(--white);line-height:1.65;}
  .company-services{display:flex;flex-wrap:wrap;gap:6px;margin-top:11px;}
  .service-tag{font-size:11px;font-family:'Fira Code',monospace;padding:3px 9px;border-radius:4px;background:#10b98112;color:var(--green);border:1px solid #10b98133;}
  .company-link{display:inline-block;margin-top:13px;font-size:12px;font-family:'Fira Code',monospace;color:var(--green);text-decoration:none;border:1px solid var(--green);padding:5px 14px;border-radius:6px;background:#10b98110;transition:background .2s;}
  .company-link:hover{background:#10b98122;}

  /* FOOTER */
  .footer{margin-top:44px;padding:28px 28px 20px;text-align:center;background:linear-gradient(180deg,transparent,#0a2a1a33);border-top:1px solid var(--border);}
  .footer p{font-size:13px;color:var(--muted);}

  /* ROBOT */
  .robot-anim{position:fixed;right:16px;bottom:16px;width:52px;height:52px;pointer-events:none;animation:robotFloat 3s ease-in-out infinite;z-index:99;}
  @keyframes robotFloat{0%,100%{transform:translateY(0) rotate(-3deg)}50%{transform:translateY(-10px) rotate(3deg)}}
  body::after{content:'';position:fixed;inset:0;background:repeating-linear-gradient(0deg,transparent,transparent 2px,#00000010 2px,#00000010 4px);pointer-events:none;z-index:200;}
</style>
</head>
<body>

<!-- Robot -->
<svg class="robot-anim" viewBox="0 0 54 54" xmlns="http://www.w3.org/2000/svg">
  <rect x="15" y="18" width="24" height="20" rx="4" fill="#10b98118" stroke="#10b981" stroke-width="1.5"/>
  <rect x="21" y="24" width="5" height="5" rx="1" fill="#10b981"/><rect x="28" y="24" width="5" height="5" rx="1" fill="#10b981"/>
  <rect x="23" y="32" width="8" height="2" rx="1" fill="#10b98188"/>
  <rect x="20" y="14" width="14" height="5" rx="2" fill="#0a150f" stroke="#10b981" stroke-width="1.2"/>
  <line x1="27" y1="10" x2="27" y2="14" stroke="#10b981" stroke-width="1.5" stroke-linecap="round"/>
  <rect x="11" y="20" width="4" height="10" rx="2" fill="#0a150f" stroke="#10b981" stroke-width="1"/>
  <rect x="39" y="20" width="4" height="10" rx="2" fill="#0a150f" stroke="#10b981" stroke-width="1"/>
  <rect x="19" y="38" width="5" height="8" rx="2" fill="#0a150f" stroke="#10b981" stroke-width="1"/>
  <rect x="30" y="38" width="5" height="8" rx="2" fill="#0a150f" stroke="#10b981" stroke-width="1"/>
  <circle cx="27" cy="10" r="2" fill="#10b981"><animate attributeName="opacity" values="1;0.2;1" dur="1.2s" repeatCount="indefinite"/></circle>
</svg>

<!-- BANNER -->
<div class="banner">
  <div class="grid-lines"></div>
  <h1>KAWIN M.S</h1>
  <div class="subtitle">🤖 AI Engineer &nbsp;·&nbsp; 💻 Frontend Developer</div>
  <img src="https://avatars.githubusercontent.com/u/172995384?v=4" class="profile-photo" alt="Kawin M.S"/>
  <div class="typing-line" id="typingLine"></div>
  <div class="badges">
    <a href="https://kawin-portfolio.netlify.app/" class="badge badge-green">Portfolio</a>
    <a href="https://www.integerio.com/" class="badge badge-green">Integer.IO Tech</a>
    <a href="https://www.linkedin.com/in/kawin-m-s-570961285/" class="badge badge-blue">LinkedIn</a>
    <a href="https://github.com/kawin789" class="badge badge-dark">GitHub</a>
    <a href="mailto:mskawin2004@gmail.com" class="badge badge-red">Email</a>
  </div>
</div>

<!-- ABOUT -->
<section>
  <h2>🧬 About Me</h2>
  <div class="code-block"><div class="code-inner"><pre><span class="cmt"># ┌──────────────────────────────────────────────────────────┐
# │          system.boot()  ·  kawin.exe  [OK]              │
# └──────────────────────────────────────────────────────────┘</span>

<span class="kw">class</span> <span class="cls">KawinMS</span>:
    <span class="key">name</span>       = <span class="str">"Kawin M.S"</span>
    <span class="key">role</span>       = <span class="arr">[</span><span class="str">"AI Engineer"</span>, <span class="str">"Frontend Developer"</span><span class="arr">]</span>
    <span class="key">company</span>    = <span class="str">"Integer.IO Tech  ·  integerio.com"</span>
    <span class="key">location</span>   = <span class="str">"Madurai, Tamil Nadu, India"</span>
    <span class="key">education</span>  = <span class="str">"BSc Computer Science · KG College of Arts &amp; Science (2022–2025)"</span>
    <span class="key">current</span>    = <span class="str">"AI Engineer @ Integer.IO Tech"</span>
    <span class="key">shipped</span>    = <span class="str">"50+ AI/ML &amp; Web Projects  ·  30+ Clients across India"</span>
    <span class="key">available</span>  = <span class="arr">[</span><span class="str">"Freelance"</span>, <span class="str">"Collaboration"</span>, <span class="str">"Full-time"</span><span class="arr">]</span>
    <span class="key">quote</span>      = <span class="str">"Combine logic + creativity → build intelligent solutions"</span></pre></div></div>
</section>

<hr/>

<!-- TECH STACK -->
<section>
  <h2>🛠️ Tech Stack</h2>

  <div class="stack-group">
    <div class="stack-label">Frontend</div>
    <div class="pill-row">
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg"/>HTML5</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"/>CSS3</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"/>JavaScript</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg"/>TypeScript</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg"/>React</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg"/>Bootstrap</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg"/>Tailwind</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vitejs/vitejs-original.svg"/>Vite</span>
    </div>
  </div>

  <div class="stack-group">
    <div class="stack-label">Backend &amp; Database</div>
    <div class="pill-row">
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"/>Python</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg"/>Django</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/fastapi/fastapi-original.svg"/>FastAPI</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg"/>Node.js</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg"/>MySQL</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg"/>PostgreSQL</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg"/>MongoDB</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg"/>Firebase</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg"/>Linux</span>
    </div>
  </div>

  <div class="stack-group">
    <div class="stack-label">AI / GenAI</div>
    <div class="pill-row">
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg"/>TensorFlow</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/opencv/opencv-original.svg"/>OpenCV</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg"/>Pandas</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg"/>NumPy</span>
      <span class="pill">🤗 HuggingFace</span>
      <span class="pill">✦ OpenAI</span>
      <span class="pill">♊ Gemini</span>
      <span class="pill">⛓ LangChain</span>
      <span class="pill">🔍 FAISS</span>
      <span class="pill">📡 RAG</span>
      <span class="pill">🎯 YOLO</span>
      <span class="pill">🔄 n8n</span>
      <span class="pill">🧩 MCP</span>
      <span class="pill">🎨 Stable Diffusion</span>
    </div>
  </div>

  <div class="stack-group">
    <div class="stack-label">Tools &amp; DevOps</div>
    <div class="pill-row">
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg"/>Git</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg"/>GitHub</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg"/>Docker</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/azure/azure-original.svg"/>Azure</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg"/>VS Code</span>
      <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vercel/vercel-original.svg"/>Vercel</span>
      <span class="pill">⚡ Supabase</span>
      <span class="pill">📮 Postman</span>
      <span class="pill">📊 Power BI</span>
    </div>
  </div>
</section>

<hr/>

<!-- SKILL BARS -->
<section>
  <h2>⚡ Skill Levels</h2>
  <div class="skill-bars">
    <div class="skill-row"><div class="skill-name">Python</div><div class="bar-track"><div class="bar-fill" style="width:90%;animation-delay:.1s"></div></div><div class="skill-pct">90%</div></div>
    <div class="skill-row"><div class="skill-name">React / JS</div><div class="bar-track"><div class="bar-fill" style="width:85%;animation-delay:.2s"></div></div><div class="skill-pct">85%</div></div>
    <div class="skill-row"><div class="skill-name">Django REST</div><div class="bar-track"><div class="bar-fill" style="width:80%;animation-delay:.3s"></div></div><div class="skill-pct">80%</div></div>
    <div class="skill-row"><div class="skill-name">GenAI / RAG</div><div class="bar-track"><div class="bar-fill" style="width:75%;animation-delay:.4s"></div></div><div class="skill-pct">75%</div></div>
    <div class="skill-row"><div class="skill-name">Data Science</div><div class="bar-track"><div class="bar-fill" style="width:65%;animation-delay:.5s"></div></div><div class="skill-pct">65%</div></div>
    <div class="skill-row"><div class="skill-name">Docker / Azure</div><div class="bar-track"><div class="bar-fill" style="width:55%;animation-delay:.6s"></div></div><div class="skill-pct">55%</div></div>
  </div>
</section>

<hr/>

<!-- PROJECTS -->
<section>
  <h2>🚀 Featured Projects</h2>
  <div class="projects-grid">

    <div class="project-card">
      <h3>Prospient GRC</h3>
      <div class="tag-row">
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/fastapi/fastapi-original.svg"/>FastAPI</span>
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"/>Python</span>
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vitejs/vitejs-original.svg"/>Vite</span>
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg"/>PostgreSQL</span>
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/azure/azure-original.svg"/>Azure</span>
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg"/>Docker</span>
      </div>
      <p>Multi-tenant Governance, Risk &amp; Compliance platform built on a 37-model SQLAlchemy schema with tenant isolation, RBAC, and audit trails. FastAPI backend, Vite frontend, deployed to a Windows Azure VM behind an IIS reverse proxy.</p>
    </div>

    <div class="project-card">
      <h3>CRM Portal</h3>
      <div class="tag-row">
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg"/>React</span>
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg"/>TypeScript</span>
        <span class="pill">⚡ Supabase</span>
      </div>
      <p>CRM portal in active development on React, TypeScript, and Supabase — architected to extend into a companion Android app via the Supabase Kotlin SDK for real-time sync across web and mobile.</p>
    </div>

    <div class="project-card">
      <h3>Bhoosparsh</h3>
      <div class="tag-row">
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg"/>Django</span>
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"/>Python</span>
        <span class="tag">cPanel</span>
        <span class="tag">SMS OTP</span>
      </div>
      <p>Django-powered real estate platform live at bhoosparsh.com, hosted on cPanel. Resolved production deployment issues — static file config, Passenger restarts, Python-version constraints — and integrated MSG91 SMS OTP verification.</p>
    </div>

    <div class="project-card">
      <h3>Integer.IO Tech — Web</h3>
      <div class="tag-row">
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg"/>React</span>
        <span class="pill"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vercel/vercel-original.svg"/>Vercel</span>
        <span class="tag">SEO</span>
        <span class="tag">Branding</span>
      </div>
      <p>Company website and brand presence for Integer.IO Tech — built the About Us and "Why Choose Us" pages in React, connected the domain through Vercel, and drove SEO-optimized positioning across social platforms.</p>
    </div>

  </div>
</section>

<hr/>

<!-- EXPERIENCE -->
<section>
  <h2>💼 Experience</h2>
  <table class="exp-table">
    <thead><tr><th>🗓️ Period</th><th>🧑‍💻 Role</th><th>🏢 Organization</th></tr></thead>
    <tbody>
      <tr><td><span class="active-dot"></span><span class="period-badge">Present</span></td><td>AI Engineer</td><td>Integer.IO Tech</td></tr>
      <tr><td><span class="active-dot"></span><span class="period-badge">Present</span></td><td>AI Engineer</td><td>Prospient GRC</td></tr>
      <tr><td><span class="period-badge">Present</span></td><td>Python Developer</td><td>M7 Corporation · Thaagam Foundation</td></tr>
      <tr><td><span class="period-badge">2025</span></td><td>Front-End Developer Intern</td><td>SMIE Industries Pvt. Ltd.</td></tr>
      <tr><td><span class="period-badge">2023–Now</span></td><td>Freelance Developer</td><td>Self-employed · 50+ Projects</td></tr>
    </tbody>
  </table>
</section>

<hr/>

<!-- GITHUB STATS -->
<section>
  <h2>📊 GitHub Stats</h2>
  <div class="stat-counters">
    <div class="stat-box"><span class="stat-val">196</span><div class="stat-lbl">Contributions</div></div>
    <div class="stat-box"><span class="stat-val">43</span><div class="stat-lbl">Public Repos</div></div>
    <div class="stat-box"><span class="stat-val">5</span><div class="stat-lbl">Stars Earned</div></div>
    <div class="stat-box"><span class="stat-val">7</span><div class="stat-lbl">Followers</div></div>
  </div>
  <div class="lang-bar-track">
    <div class="lang-segment" style="width:35%;background:#10b981"></div>
    <div class="lang-segment" style="width:28%;background:#f1e05a"></div>
    <div class="lang-segment" style="width:20%;background:#e34c26"></div>
    <div class="lang-segment" style="width:11%;background:#563d7c"></div>
    <div class="lang-segment" style="width:6%;background:#3572A5"></div>
  </div>
  <div class="lang-legend" style="margin-bottom:12px;">
    <div class="lang-dot"><div class="dot" style="background:#10b981"></div>Python 35%</div>
    <div class="lang-dot"><div class="dot" style="background:#f1e05a"></div>JavaScript 28%</div>
    <div class="lang-dot"><div class="dot" style="background:#e34c26"></div>HTML 20%</div>
    <div class="lang-dot"><div class="dot" style="background:#563d7c"></div>CSS 11%</div>
    <div class="lang-dot"><div class="dot" style="background:#3572A5"></div>Other 6%</div>
  </div>
  <div class="contrib-graph">
    <div style="color:var(--green);font-size:10px;letter-spacing:1px;margin-bottom:6px;">CONTRIBUTION ACTIVITY</div>
    <div class="contrib-grid" id="contribGrid"></div>
  </div>
  <div style="display:flex;flex-wrap:wrap;gap:12px;margin-top:14px;justify-content:center;">
    <img src="https://github-readme-stats.vercel.app/api?username=kawin789&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&bg_color=0d1117&title_color=10b981&icon_color=10b981&text_color=ffffff&border_radius=8" style="flex:1;min-width:240px;max-width:400px;border-radius:10px;" alt="Stats"/>
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kawin789&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=10b981&text_color=ffffff&border_radius=8&langs_count=8" style="flex:1;min-width:200px;max-width:340px;border-radius:10px;" alt="Langs"/>
  </div>
  <div style="text-align:center;margin-top:12px;">
    <img src="https://streak-stats.demolab.com?user=kawin789&theme=tokyonight&hide_border=true&background=0d1117&ring=10b981&fire=10b981&currStreakLabel=10b981&sideLabels=10b981&dates=8b949e&stroke=0d1117" style="max-width:100%;border-radius:10px;" alt="Streak"/>
  </div>
</section>

<hr/>

<!-- CERTS -->
<section>
  <h2>🏆 Certifications</h2>
  <ul class="cert-list">
    <li><span class="cert-icon">🥉</span><div><div class="cert-title">3rd Place — Dev Day's 24 Hackathon</div><div class="cert-org">Metazord · Certificate · Medal · Cash Prize</div></div></li>
    <li><span class="cert-icon">📊</span><div><div class="cert-title">Data Science with Python</div><div class="cert-org">Brainery Spot Technologies Institute</div></div></li>
    <li><span class="cert-icon">🎨</span><div><div class="cert-title">Frontend Web Development</div><div class="cert-org">Innovate Technologies</div></div></li>
    <li><span class="cert-icon">🤖</span><div><div class="cert-title">Artificial Intelligence Master Class</div><div class="cert-org">30-Day Program</div></div></li>
    <li><span class="cert-icon">⚙️</span><div><div class="cert-title">UI Path Studio — Automation Development</div><div class="cert-org">UiPath</div></div></li>
  </ul>
</section>

<hr/>

<!-- INTEGER.IO -->
<section>
  <h2>🏢 Integer.IO Tech</h2>
  <div class="company-card">
    <div class="company-header">
      <img class="company-logo" src="https://www.integerio.com/assets/half_logo-RemiG_br.webp" alt="Integer.IO Tech logo"/>
      <div>
        <div class="company-name">Integer.IO Tech</div>
        <div class="company-role">AI Engineer — integerio.com · Madurai, Tamil Nadu, India</div>
      </div>
    </div>
    <p>An IT company delivering professional web development, AI automation, SaaS products, billing software, digital marketing, and branding services — trusted by <strong>30+ clients across India</strong>. We also support students and institutions with final-year and academic project development.</p>
    <div class="company-services">
      <span class="service-tag">Web Development</span>
      <span class="service-tag">AI Automation</span>
      <span class="service-tag">SaaS Products</span>
      <span class="service-tag">Billing Software</span>
      <span class="service-tag">Digital Marketing</span>
      <span class="service-tag">Branding</span>
      <span class="service-tag">Student Projects</span>
      <span class="service-tag">Cloud Deployment</span>
    </div>
    <a href="https://www.integerio.com/" class="company-link">Visit integerio.com →</a>
  </div>
</section>

<!-- FOOTER -->
<div class="footer">
  <p>Open to freelance projects, collaborations, and full-time opportunities</p>
  <p style="margin-top:8px;"><strong>mskawin2004@gmail.com</strong> &nbsp;·&nbsp; Madurai, Tamil Nadu, India</p>
</div>

<script>
  const lines=["AI Engineer | GenAI Systems | REST APIs","AI Engineer @ Integer.IO Tech","50+ Projects · 30+ Clients Across India","Building Intelligent, User-Focused Solutions"];
  let li=0,ci=0,del=false;
  const el=document.getElementById('typingLine');
  function type(){
    const cur=lines[li];
    if(!del){el.textContent=cur.slice(0,++ci);if(ci===cur.length){del=true;setTimeout(type,1800);return;}}
    else{el.textContent=cur.slice(0,--ci);if(ci===0){del=false;li=(li+1)%lines.length;}}
    setTimeout(type,del?38:62);
  }
  type();
  const grid=document.getElementById('contribGrid');
  const cols=['#161b22','#0d3320','#166534','#16a34a','#22c55e'];
  for(let i=0;i<364;i++){
    const c=document.createElement('div');c.className='contrib-cell';
    const w=Math.random();
    c.style.background=w<.55?cols[0]:w<.70?cols[1]:w<.82?cols[2]:w<.92?cols[3]:cols[4];
    grid.appendChild(c);
  }
</script>
</body>
</html>
