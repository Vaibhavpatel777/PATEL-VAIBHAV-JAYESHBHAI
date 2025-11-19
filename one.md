<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Patel Vaibhav — Profile</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">

  <style>
    /* ---------- Root / Variables ---------- */
    :root{
      --bg: #0f1724;
      --card: #0b1220;
      --muted: #94a3b8;
      --glass: rgba(255,255,255,0.04);
      --accent: linear-gradient(90deg,#06b6d4,#7c3aed);
      --accent-solid: #06b6d4;
      --glass-2: rgba(255,255,255,0.03);
      --radius: 14px;
      --glass-border: rgba(255,255,255,0.05);
      --shadow: 0 8px 30px rgba(2,6,23,0.6);
    }

    /* Light theme overrides (js toggles body.light) */
    body.light {
      --bg: #f6f8fa;
      --card: #ffffff;
      --muted: #6b7280;
      --glass: rgba(15,23,36,0.02);
      --glass-2: rgba(2,6,23,0.02);
      --glass-border: rgba(2,6,23,0.06);
      --shadow: 0 8px 30px rgba(16,24,40,0.06);
    }

    /* ---------- Base ---------- */
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial;
      background: radial-gradient(1200px 500px at 10% 10%, rgba(124,58,237,0.12), transparent),
                  radial-gradient(900px 400px at 90% 90%, rgba(6,182,212,0.06), transparent),
                  var(--bg);
      color: #e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:48px 24px;
    }

    /* ---------- Container ---------- */
    .container{
      max-width:1100px;
      margin:0 auto;
      display:grid;
      grid-template-columns: 1fr 360px;
      gap:28px;
      align-items:start;
    }

    /* stacked on small screens */
    @media (max-width:880px){
      .container{grid-template-columns:1fr; padding:0 12px}
    }

    /* ---------- Card ---------- */
    .card{
      background: linear-gradient(180deg, rgba(255,255,255,0.02), transparent);
      border-radius:var(--radius);
      border:1px solid var(--glass-border);
      padding:22px;
      box-shadow:var(--shadow);
      backdrop-filter: blur(6px) saturate(120%);
    }

    /* ---------- Header / Intro ---------- */
    .profile-head{
      display:flex;
      gap:18px;
      align-items:center;
    }
    .avatar{
      width:96px;
      height:96px;
      border-radius:18px;
      background:linear-gradient(180deg, rgba(255,255,255,0.06), rgba(255,255,255,0.02));
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:700;
      font-size:30px;
      color: white;
      letter-spacing:0.6px;
      flex-shrink:0;
      border:1px solid var(--glass-border);
    }
    .title{
      display:flex;
      flex-direction:column;
      gap:6px;
    }
    .title h1{
      margin:0;
      font-size:20px;
      letter-spacing:-0.2px;
    }
    .title p{margin:0;color:var(--muted);font-size:13px}

    .meta-list{
      margin-top:14px;
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:10px;
    }
    .meta-item{
      display:flex;
      gap:10px;
      align-items:center;
      padding:10px;
      background:var(--glass);
      border-radius:10px;
      font-size:13px;
      color:var(--muted);
      border:1px solid var(--glass-2);
    }

    /* ---------- Tech badges ---------- */
    .tech{
      display:flex;
      flex-wrap:wrap;
      gap:10px;
      margin-top:16px;
    }
    .badge{
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding:8px 12px;
      background:linear-gradient(90deg, rgba(255,255,255,0.02), transparent);
      border-radius:10px;
      font-size:13px;
      color:var(--muted);
      border:1px solid var(--glass-2);
      transition:transform .18s ease, color .18s ease;
    }
    .badge img{height:20px;width:20px;object-fit:contain;border-radius:4px}
    .badge:hover{transform:translateY(-6px); color: #fff}

    /* ---------- Stats section ---------- */
    .stats-grid{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:12px;
      margin-top:16px;
    }
    .stat{
      padding:12px;
      text-align:center;
      border-radius:10px;
      background:linear-gradient(90deg, rgba(255,255,255,0.014), transparent);
      border:1px solid var(--glass-2);
    }
    .stat strong{display:block;font-size:16px}
    .stat span{display:block;color:var(--muted);font-size:12px}

    /* ---------- Roadmap / Content ---------- */
    .content h2{
      margin:0 0 6px 0;
      font-size:18px;
      display:flex;
      align-items:center;
      gap:10px;
    }
    .section{
      margin-top:14px;
    }
    .list{
      list-style:none;
      padding:0;
      margin:8px 0 0 0;
      display:grid;
      gap:8px;
    }
    .list li{
      background:linear-gradient(180deg, rgba(255,255,255,0.01), transparent);
      padding:10px 12px;
      border-radius:10px;
      border:1px solid var(--glass-2);
      display:flex;
      align-items:center;
      gap:12px;
      color:var(--muted);
      font-size:14px;
    }
    .pill{
      font-size:12px;
      padding:6px 8px;
      border-radius:999px;
      background:transparent;
      border:1px solid rgba(255,255,255,0.06);
      color:var(--muted);
    }

    /* ---------- Right column ---------- */
    .right{
      position:sticky;
      top:28px;
      height:fit-content;
    }
    .card h3{margin-top:0}

    /* ---------- CTA and small footer ---------- */
    .cta{
      display:flex;
      gap:10px;
      margin-top:12px;
      flex-wrap:wrap;
    }
    .btn{
      padding:10px 14px;
      border-radius:10px;
      border:0;
      cursor:pointer;
      font-weight:600;
      background:var(--accent);
      color:white;
      box-shadow:0 6px 18px rgba(124,58,237,0.16);
      transition:transform .16s ease;
    }
    .btn.secondary{
      background:transparent;
      border:1px solid var(--glass-2);
      color:var(--muted);
      box-shadow:none;
      font-weight:600;
    }
    .btn:active{transform:translateY(1px)}

    /* subtle animated gradient underline on headings */
    .underline{
      display:inline-block;
      background:linear-gradient(90deg,#06b6d4,#7c3aed);
      height:4px;
      width:40px;
      border-radius:4px;
      margin-left:8px;
      vertical-align:middle;
    }

    /* ---------- small responsive tweaks ---------- */
    @media (max-width:540px){
      .meta-list{grid-template-columns:1fr}
      .stats-grid{grid-template-columns:repeat(2,1fr)}
      .avatar{width:76px;height:76px;font-size:26px}
    }

    /* tiny focus styles */
    a:focus, button:focus {outline:3px solid rgba(124,58,237,0.14); outline-offset:3px}

    /* ---------- Nice fade-in ---------- */
    .fade-in{opacity:0;transform:translateY(6px);animation:fade .6s ease forwards}
    .fade-in:nth-child(1){animation-delay:.05s}
    .fade-in:nth-child(2){animation-delay:.08s}
    .fade-in:nth-child(3){animation-delay:.11s}
    @keyframes fade{to{opacity:1;transform:none}}
  </style>
</head>
<body>
  <main class="container">

    <!-- LEFT: Main info + roadmap -->
    <section class="card fade-in" aria-labelledby="profile-title">
      <div class="profile-head">
        <div class="avatar" aria-hidden="true">PV</div>
        <div class="title">
          <h1 id="profile-title">💫 Hi 👋, I'm <strong>Patel Vaibhav</strong></h1>
          <p>Student • MCA • Full-Stack Learner • Front-end enthusiast</p>
          <div style="margin-top:8px;display:flex;gap:8px;align-items:center">
            <button class="btn" onclick="window.location='mailto:pvv1515@gmail.com'">Email</button>
            <a class="btn secondary" href="https://linkedin.com/in/patel-vaibhav-0223a7172" target="_blank" rel="noopener">LinkedIn</a>
            <button class="btn secondary" id="themeToggle" title="Toggle light / dark">Toggle theme</button>
          </div>
        </div>
      </div>

      <div class="meta-list" role="list" aria-label="Profile quick facts">
        <div class="meta-item"><strong>🌱</strong><div><div style="font-weight:600">Learning</div><div style="font-size:13px;color:var(--muted)">MCA • Full-Stack</div></div></div>
        <div class="meta-item"><strong>👯</strong><div><div style="font-weight:600">Collaborate</div><div style="font-size:13px;color:var(--muted)">Front-End Projects</div></div></div>
        <div class="meta-item"><strong>🤔</strong><div><div style="font-weight:600">Help</div><div style="font-size:13px;color:var(--muted)">HTML & CSS</div></div></div>
        <div class="meta-item"><strong>📫</strong><div><div style="font-weight:600">Mail</div><div style="font-size:13px;color:var(--muted)"><a href="mailto:pvv1515@gmail.com" style="color:inherit;text-decoration:underline">pvv1515@gmail.com</a></div></div></div>
      </div>

      <div style="margin-top:18px">
        <div style="display:flex;justify-content:space-between;align-items:end">
          <h3 style="margin:0">💻 Tech Stack <span class="underline" aria-hidden="true"></span></h3>
          <small style="color:var(--muted)">selected</small>
        </div>

        <div class="tech" aria-hidden="false">
          <!-- a few representative badges (you can add/remove) -->
          <span class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="" /> HTML5</span>
          <span class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="" /> CSS3</span>
          <span class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="" /> JavaScript</span>
          <span class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="" /> React</span>
          <span class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" alt="" /> NodeJS</span>
          <span class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="" /> Python</span>
          <span class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="" /> MySQL</span>
          <span class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" alt="" /> MongoDB</span>
        </div>

        <div class="stats-grid" role="list" aria-label="Quick stats">
          <div class="stat"><strong>Front-end</strong><span>HTML • CSS • JS</span></div>
          <div class="stat"><strong>Back-end</strong><span>Node • Django • APIs</span></div>
          <div class="stat"><strong>DBs</strong><span>MySQL • MongoDB</span></div>
        </div>
      </div>

      <div class="content" style="margin-top:18px">
        <h2>🚀 Full-Stack Roadmap <span class="underline" aria-hidden="true"></span></h2>

        <div class="section">
          <h3 style="margin-bottom:6px">1. Front-End</h3>
          <ul class="list" aria-label="Front end list">
            <li><span class="pill">Core</span> HTML5 • CSS3 • JavaScript (ES6+)</li>
            <li><span class="pill">Frameworks</span> React / Vue / Angular</li>
            <li><span class="pill">Styling</span> Tailwind • Bootstrap • Sass</li>
            <li><span class="pill">Skills</span> Responsive design • A11Y • DevTools</li>
          </ul>
        </div>

        <div class="section">
          <h3 style="margin-bottom:6px">2. Back-End</h3>
          <ul class="list" aria-label="Back end list">
            <li><span class="pill">Pick one</span> Node.js • Python (Django) • Java • PHP • C#</li>
            <li><span class="pill">API</span> REST • Authentication (JWT/OAuth)</li>
            <li><span class="pill">Deploy</span> Servers • Docker • CI/CD</li>
          </ul>
        </div>

        <div class="section">
          <h3 style="margin-bottom:6px">3. Databases & Tools</h3>
          <ul class="list" aria-label="Databases list">
            <li><span class="pill">SQL</span> MySQL • PostgreSQL • SQLite</li>
            <li><span class="pill">NoSQL</span> MongoDB • Redis</li>
            <li><span class="pill">Tools</span> Git • VS Code • Postman • Docker</li>
          </ul>
        </div>

        <div class="section">
          <h3 style="margin-bottom:6px">4. Extra Skills</h3>
          <ul class="list" aria-label="Extra skills">
            <li><span class="pill">DSA</span> Data Structures & Algorithms</li>
            <li><span class="pill">Cloud</span> AWS / GCP / Azure basics</li>
            <li><span class="pill">Testing</span> Unit tests • Jest • PyTest</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- RIGHT: Summary / Stats / Projects -->
    <aside class="right">
      <div class="card fade-in">
        <h3>About</h3>
        <p style="color:var(--muted);margin:10px 0 0 0">MCA student focused on front-end and full-stack development. Open to collaboration and learning new technologies. Reach me at <a href="mailto:pvv1515@gmail.com">pvv1515@gmail.com</a>.</p>

        <div style="margin-top:12px;display:flex;gap:8px;flex-wrap:wrap">
          <button class="btn" onclick="window.open('https://github.com/Vaibhavpatel777','_blank')">GitHub</button>
          <a class="btn secondary" href="#roadmap">Roadmap</a>
        </div>
      </div>

      <div class="card fade-in" style="margin-top:16px">
        <h3>Top Skills</h3>
        <div style="display:flex;flex-direction:column;gap:8px;margin-top:8px">
          <div class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="">HTML</div>
          <div class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="">CSS</div>
          <div class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="">JavaScript</div>
          <div class="badge"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="">React</div>
        </div>
      </div>

      <div class="card fade-in" style="margin-top:16px">
        <h3>Contact</h3>
        <p style="color:var(--muted);margin:8px 0">Email: <a href="mailto:pvv1515@gmail.com">pvv1515@gmail.com</a></p>
        <p style="color:var(--muted);margin:8px 0">LinkedIn: <a href="https://linkedin.com/in/patel-vaibhav-0223a7172" target="_blank">patel-vaibhav</a></p>
      </div>
    </aside>
  </main>

  <script>
    /* Theme toggle: preserves choice in localStorage */
    const btn = document.getElementById('themeToggle');
    const root = document.body;
    function setTheme(theme){
      if(theme === 'light'){ root.classList.add('light'); localStorage.setItem('theme','light'); }
      else { root.classList.remove('light'); localStorage.setItem('theme','dark'); }
    }
    // init
    const saved = localStorage.getItem('theme') || (window.matchMedia && window.matchMedia('(prefers-color-scheme:light)').matches ? 'light' : 'dark');
    setTheme(saved);
    btn.addEventListener('click', ()=> setTheme(root.classList.contains('light') ? 'dark' : 'light'));
  </script>
</body>
</html>
