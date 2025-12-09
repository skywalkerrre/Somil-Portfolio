<p align="center">
  <img src="./assets/banner.png" alt="Somil Portfolio Banner" style="max-width:100%;height:auto;border-radius:12px;box-shadow:0 12px 40px rgba(2,6,23,0.15)" />
</p>

# Somil Singh — Personal Portfolio

[![Vercel](https://img.shields.io/badge/deploy-vercel-000000?logo=vercel)](https://vercel.com) &nbsp; [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE) &nbsp; ❤️ Made with care

## What this repo contains
A polished, multi-page portfolio for **Somil Singh** — responsive, accessible, and deploy-ready. Upgrades from the single-page template:

- ✨ Animated section entrances (CSS + IntersectionObserver)
- 💼 A responsive sidebar resume layout (desktop) and stacked resume (mobile)
- 🧩 Multi-page version: `index.html`, `projects.html`, `resume.html`
- Dark / Light mode toggle (persisted to user preference)
- Clean, modern layout inspired by your OnePercent example
- Screenshot banner, badges, and an attractive README for Vercel deploy

---

## Live demo
Open `index.html` locally or deploy to Vercel for a live URL.

---

## Key files
- `index.html` — Landing + overview (animated entrances)
- `projects.html` — Dedicated projects gallery (expandable cards)
- `resume.html` — Sidebar resume layout with printable view
- `styles.css` — All styling (variables, animations, responsive grid)
- `script.js` — Theme + animations + simple routing helpers
- `assets/*` — Images, banner, icons

---

## Features
- Minimal & fast: vanilla HTML/CSS/JS — no frameworks
- Accessible: semantic HTML, keyboard friendly, ARIA labels
- Animated entrances: fade/slide animations trigger when sections scroll into view
- Sidebar resume: quick glance on desktop; printable resume page
- Multi-page: shareable links — great for LinkedIn profile link

---

## Quickstart (local)
1. Clone: `git clone https://github.com/<you>/somil-portfolio.git`
2. Serve: `cd somil-portfolio && npx http-server -p 8080` (or open files directly)
3. Visit: `http://localhost:8080`

---

## Deploy to Vercel (recommended)
1. Push repo to GitHub.
2. Sign into Vercel and click "Import Project" → choose your GitHub repo.
3. Use default settings (Framework: Other) and click "Deploy". Vercel provides a live production URL.

---

## Customization
- Replace `assets/banner.png` and project screenshots in `assets/`.
- Edit content inside `*.html` files to personalize text and links.
- Add more project cards in `projects.html`.

---

--- FILE: index.html ---

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Somil Singh — Portfolio</title>
  <link rel="stylesheet" href="styles.css">
  <meta name="description" content="Somil Singh — Software Engineer | AI Enthusiast | State-level footballer | Guitarist">
</head>
<body>
  <header class="hero">
    <div class="container hero-grid">
      <div class="hero-left">
        <h1>Somil Singh</h1>
        <p class="lead">Software Engineer · AI Enthusiast · State‑level Footballer · Guitarist</p>
        <p class="cta">I design fast, testable frontends and integration flows. I enjoy turning complex systems into simple, elegant user experiences.</p>
        <div class="actions">
          <a class="btn primary" href="resume.html">💼 View Resume</a>
          <a class="btn ghost" href="projects.html">🚀 Projects</a>
        </div>
      </div>
      <div class="hero-right">
        <img class="banner" src="assets/banner.png" alt="Somil Portfolio Banner">
      </div>
    </div>
    <div class="theme-toggle">
      <button id="themeBtn" aria-label="Toggle dark mode">☾</button>
    </div>
  </header>

  <nav class="site-nav">
    <a href="index.html">Home</a>
    <a href="projects.html">Projects</a>
    <a href="resume.html">Resume</a>
    <a href="#contact">Contact</a>
  </nav>

  <main>
    <section id="about" class="container section animate">
      <h2>💫 About Me</h2>
      <p>I’m a passionate software engineer with experience at Oracle, building frontend components and integration tests. I love working on AI-driven features and crafting production-grade user interfaces. Off the keyboard, I play guitar and compete in football at the state level.</p>
    </section>

    <section id="skills" class="container section animate">
      <h2>🛠️ Skills & Tech</h2>
      <ul class="chips">
        <li>Java</li>
        <li>JUnit / QUnit</li>
        <li>Preact</li>
        <li>Oracle JET</li>
        <li>Integration Testing</li>
        <li>OIC Integrations</li>
        <li>AI Foundations</li>
        <li>Cloud Concepts</li>
      </ul>
    </section>

    <section id="projects" class="container section animate">
      <h2>🚀 Work & Projects</h2>

      <div class="grid">
        <article class="card">
          <h3>Associate Software Developer — Oracle</h3>
          <p>Frontend components and cloud integrations for the Construction & Engineering GBU. Focused on testable components, accessibility and maintainability.</p>
        </article>

        <article class="card">
          <h3>Intern — Oracle (6 months)</h3>
          <p>Built component features, wrote integration tests and contributed to automation for developer workflows.</p>
        </article>
      </div>

    </section>

    <section id="extras" class="container section animate">
      <h2>🌟 More About Me</h2>
      <ul>
        <li>Published a research paper during my final semester project.</li>
        <li>State‑level footballer with tournament experience.</li>
        <li>Guitarist & badminton enthusiast.</li>
      </ul>
    </section>

    <section id="contact" class="container section animate">
      <h2>📬 Contact</h2>
      <p>Email: <a href="mailto:your-email@example.com">your-email@example.com</a></p>
      <p>LinkedIn: <a href="https://www.linkedin.com/in/your-profile" target="_blank">your-profile</a> · GitHub: <a href="https://github.com/your-github" target="_blank">your-github</a></p>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <p>© 2025 Somil Singh · Built with care.</p>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>

--- FILE: projects.html ---

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Projects — Somil Singh</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="mini-hero">
    <div class="container">
      <h1>🚀 Projects</h1>
      <p class="lead">A selection of what I’ve built — components, integrations, and research work.</p>
      <a class="btn ghost" href="index.html">← Back</a>
    </div>
  </header>

  <main class="container section">
    <div class="grid project-grid animate">
      <article class="card project-card">
        <img src="assets/project-1.png" alt="Project screenshot" />
        <h3>Integration Testing Suite</h3>
        <p>Comprehensive QUnit & JUnit driven tests for component reliability and CI pipelines.</p>
        <a class="btn" href="#">Details</a>
      </article>

      <article class="card project-card">
        <img src="assets/project-2.png" alt="Project screenshot" />
        <h3>Component Library — Oracle JET</h3>
        <p>Reusable Gbu components with hierarchical checklist logic and accessibility-first design.</p>
        <a class="btn" href="#">Details</a>
      </article>

      <!-- Add more project cards -->
    </div>
  </main>

  <footer class="site-footer">
    <div class="container">© 2025 Somil Singh</div>
  </footer>
  <script src="script.js"></script>
</body>
</html>

--- FILE: resume.html ---

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Resume — Somil Singh</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="resume-root container">
    <aside class="resume-side animate">
      <div class="profile">
        <img src="assets/avatar.png" alt="Somil avatar" />
        <h2>Somil Singh</h2>
        <p class="muted">Software Engineer</p>
      </div>

      <div class="side-block">
        <h4>Contact</h4>
        <p>your-email@example.com<br>LinkedIn / GitHub</p>
      </div>

      <div class="side-block">
        <h4>Skills</h4>
        <ul>
          <li>Java · JUnit</li>
          <li>Preact · Oracle JET</li>
          <li>Integration Testing</li>
        </ul>
      </div>
    </aside>

    <main class="resume-main animate">
      <section>
        <h3>Experience</h3>
        <div class="exp">
          <h4>Associate Software Developer — Oracle</h4>
          <p class="muted">2024 — Present</p>
          <p>Frontend components & cloud integrations for Construction & Engineering GBU.</p>
        </div>

        <div class="exp">
          <h4>Intern — Oracle</h4>
          <p class="muted">6 months</p>
          <p>Component features, test automation and developer tooling.</p>
        </div>
      </section>

      <section>
        <h3>Education & Research</h3>
        <p>Published a paper during final semester project; mentored work.</p>
      </section>
    </main>
  </div>

  <footer class="site-footer">
    <div class="container">Printable: Use browser print to export PDF</div>
  </footer>
  <script src="script.js"></script>
</body>
</html>

--- FILE: styles.css ---

:root{--bg:#ffffff;--text:#0b1220;--muted:#6b7280;--accent:#0f62fe;--card:#f8fafc}
[data-theme="dark"]{--bg:#071026;--text:#e6eef8;--muted:#9aa5b1;--accent:#58a6ff;--card:#0b1220}
*{box-sizing:border-box}
body{margin:0;font-family:Inter,ui-sans-serif,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;background:var(--bg);color:var(--text);-webkit-font-smoothing:antialiased}
.container{max-width:1100px;margin:0 auto;padding:24px}

/* HERO */
.hero{padding:56px 0;background:linear-gradient(135deg,var(--accent),#00c8ff);color:white;position:relative}
.hero-grid{display:flex;gap:24px;align-items:center}
.hero-left{flex:1}
.hero-right{flex:1;text-align:right}
.hero h1{font-size:44px;margin:0}
.lead{opacity:0.95;margin-top:8px}
.cta{margin-top:18px}
.actions{margin-top:18px}
.btn{display:inline-block;padding:10px 16px;border-radius:10px;text-decoration:none;background:transparent;border:1px solid rgba(0,0,0,0.08);color:inherit}
.btn.primary{background:#001f7a;color:white;border:0}
.btn.ghost{background:transparent;color:white;border:1px solid rgba(255,255,255,0.15)}
.banner{max-width:420px;border-radius:12px;box-shadow:0 12px 40px rgba(2,6,23,0.15)}
.theme-toggle{position:absolute;right:20px;top:16px}
.theme-toggle button{background:rgba(255,255,255,0.12);border:0;padding:8px;border-radius:8px;color:white;cursor:pointer}

.site-nav{display:flex;gap:18px;justify-content:center;padding:16px 0;background:var(--card)}
.site-nav a{text-decoration:none;color:var(--accent);font-weight:600}

.section{padding:36px 0}
.section h2{margin:0 0 12px 0}
.chips{display:flex;flex-wrap:wrap;gap:12px;padding:0;list-style:none}
.chips li{background:var(--card);padding:8px 12px;border-radius:999px;border:1px solid rgba(0,0,0,0.04)}
.grid{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}
.card{background:var(--card);padding:18px;border-radius:12px;box-shadow:0 6px 20px rgba(2,6,23,0.06)}
.project-grid img{width:100%;height:140px;object-fit:cover;border-radius:8px;margin-bottom:12px}
.project-card .btn{margin-top:8px}

/* Resume layout */
.resume-root{display:flex;gap:24px}
.resume-side{width:280px;background:var(--card);padding:18px;border-radius:12px}
.resume-main{flex:1;background:transparent;padding:8px}
.resume-side img{width:96px;height:96px;border-radius:12px;display:block;margin-bottom:12px}
.side-block{margin-top:18px}
.side-block h4{margin:0 0 6px 0}
.exp{margin-bottom:12px}
.muted{color:var(--muted)}

/* Animations */
.animate{opacity:0;transform:translateY(20px);transition:opacity 520ms cubic-bezier(.2,.9,.3,1),transform 520ms cubic-bezier(.2,.9,.3,1)}
.animate.in-view{opacity:1;transform:none}

/* Responsive */
@media(max-width:900px){
  .hero-grid{flex-direction:column;text-align:center}
  .hero-right{text-align:center}
  .grid{grid-template-columns:1fr}
  .resume-root{flex-direction:column}
  .resume-side{width:100%}
}

/* Print-friendly resume */
@media print{
  body{background:white;color:black}
  .site-nav,.theme-toggle,.actions{display:none}
}

--- FILE: script.js ---

// Theme toggle with persistence + Animated entrances
(function(){
  const themeKey = 'somil_theme';
  const btn = document.getElementById('themeBtn');

  function setTheme(theme){
    if(theme === 'dark') document.documentElement.setAttribute('data-theme','dark');
    else document.documentElement.removeAttribute('data-theme');
    try{ localStorage.setItem(themeKey, theme); }catch(e){}
  }

  function initTheme(){
    const saved = localStorage.getItem(themeKey);
    if(saved) setTheme(saved);
    else setTheme(window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light');

    if(btn) btn.addEventListener('click', ()=>{
      const now = document.documentElement.getAttribute('data-theme') === 'dark' ? 'dark' : 'light';
      setTheme(now === 'dark' ? 'light' : 'dark');
    });
  }

  // IntersectionObserver to add 'in-view' for animate elements
  function initAnimations(){
    const obs = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{ if(e.isIntersecting) e.target.classList.add('in-view'); });
    },{threshold:0.12});

    document.querySelectorAll('.animate').forEach(el=>obs.observe(el));
  }

  document.addEventListener('DOMContentLoaded', ()=>{ initTheme(); initAnimations(); });
})();

--- FILE: assets/README.txt ---
Place assets/banner.png (1200x600), avatar.png (400x400), project screenshots project-1.png, project-2.png etc.

--- FILE: LICENSE ---
MIT License

Copyright (c) 2025 Somil Singh

(Full MIT license text)

---

End of project files.
