<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Microfun Apps</title>
  <meta name="description" content="Microfun Apps — tiny apps, big smiles." />
  <meta property="og:title" content="Microfun Apps" />
  <meta property="og:description" content="Tiny apps, big smiles." />
  <meta property="og:type" content="website" />
  <meta name="theme-color" content="#0ea5e9" />
  <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Ccircle cx='32' cy='32' r='30' fill='%230ea5e9'/%3E%3Cpath d='M20 24h24v6H20zm0 10h24v6H20z' fill='white'/%3E%3C/svg%3E" />
  <style>
    :root{
      --bg: #0b1020;
      --bg-soft: #0f152a;
      --txt: #e6e7ee;
      --muted: #94a3b8;
      --brand: #0ea5e9; /* sky-500 */
      --brand-2: #22d3ee; /* cyan-400 */
      --card: rgba(255,255,255,0.06);
      --border: rgba(255,255,255,0.12);
      --shadow: 0 10px 30px rgba(2,6,23,0.5);
      --radius: 16px;
      --grid-gap: clamp(16px, 2vw, 28px);
    }
    @media (prefers-color-scheme: light){
      :root{
        --bg: #f8fafc;
        --bg-soft: #f1f5f9;
        --txt: #0b1020;
        --muted: #475569;
        --card: rgba(255,255,255,0.9);
        --border: rgba(2,6,23,0.08);
        --shadow: 0 10px 24px rgba(2,6,23,0.08);
      }
    }
    *, *::before, *::after{ box-sizing:border-box; }
    html, body{ height:100%; }
    body{
      margin:0; font-family: ui-rounded, system-ui, -apple-system, Segoe UI, Roboto, Inter, "Helvetica Neue", Arial, "Apple Color Emoji", "Segoe UI Emoji";
      color: var(--txt); background: radial-gradient(1200px 800px at 80% -10%, rgba(34,211,238,0.12), transparent 60%), radial-gradient(800px 600px at -10% 20%, rgba(14,165,233,0.18), transparent 60%), var(--bg);
      line-height:1.5;
    }
    a{ color:inherit; text-decoration: none; }
    .container{ width:min(1100px, 90%); margin-inline:auto; }

    /* Header */
    header{
      position:sticky; top:0; z-index:10;
      background: linear-gradient(to bottom, rgba(0,0,0,0.25), rgba(0,0,0,0));
      backdrop-filter: saturate(130%) blur(6px);
      border-bottom: 1px solid var(--border);
    }
    .nav{ display:flex; align-items:center; justify-content:space-between; padding:14px 0; }
    .brand{ display:flex; gap:10px; align-items:center; font-weight:800; letter-spacing:0.2px; }
    .logo{ width:34px; height:34px; display:grid; place-items:center; border-radius:10px; background: linear-gradient(135deg, var(--brand), var(--brand-2)); box-shadow: var(--shadow); }
    .logo svg{ width:20px; height:20px; }
    .nav a.btn{ padding:10px 14px; border:1px solid var(--border); border-radius:12px; background: var(--card); transition: transform .1s ease, background .2s ease; }
    .nav a.btn:hover{ transform: translateY(-2px); }

    /* Hero */
    .hero{ padding: clamp(48px, 8vw, 96px) 0 40px; text-align:center; }
    .hero h1{ font-size: clamp(28px, 6vw, 56px); line-height:1.05; margin:0 0 14px; }
    .hero p{ margin:0 auto 22px; max-width:700px; color: var(--muted); font-size: clamp(16px, 2.5vw, 18px); }
    .cta{ display:flex; gap:12px; justify-content:center; flex-wrap:wrap; margin-top:16px; }
    .button{ padding:12px 18px; border-radius:14px; font-weight:600; border:1px solid var(--border); background: var(--card); box-shadow: var(--shadow); cursor:pointer; }
    .button.primary{ background: linear-gradient(135deg, var(--brand), var(--brand-2)); color:white; border-color: transparent; }

    /* Cards */
    .grid{ display:grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: var(--grid-gap); padding: 28px 0 64px; }
    .card{ background: var(--card); border:1px solid var(--border); border-radius: var(--radius); padding: 18px; box-shadow: var(--shadow); transition: transform .12s ease; }
    .card:hover{ transform: translateY(-3px); }
    .chip{ display:inline-flex; gap:8px; align-items:center; background: rgba(14,165,233,0.14); color:#c8f3ff; padding:6px 10px; border-radius:999px; border:1px solid rgba(14,165,233,0.25); font-size:12px; }
    .card h3{ margin:12px 0 6px; font-size:18px; }
    .card p{ margin:0; color: var(--muted); }

    /* Footer */
    footer{ border-top:1px solid var(--border); padding:22px 0 40px; color: var(--muted); text-align:center; }
    .small{ font-size: 12px; }

    /* Theme toggle */
    .theme-toggle{ position: fixed; right: 16px; bottom: 16px; }

    /* Utilities */
    .sr-only{ position:absolute; width:1px; height:1px; padding:0; margin:-1px; overflow:hidden; clip:rect(0,0,0,0); white-space:nowrap; border:0; }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="logo" aria-hidden="true">
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M6 7h12v3H6zM6 12h12v3H6z" fill="#fff"/>
          </svg>
        </div>
        <a href="#" aria-label="Microfun Apps Home"><span>Microfun Apps</span></a>
      </div>
      <nav>
        <a class="btn" href="#apps">Apps</a>
        <a class="btn" href="#about">About</a>
        <a class="btn" href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero" id="home">
      <span class="chip" aria-hidden="true">🚀 Tiny apps • Big smiles</span>
      <h1>Microfun Apps</h1>
      <p>We craft bite‑size, joyful tools you can open, use, and love in under a minute. Simple, fast, and a little bit magical.</p>
      <div class="cta">
        <a class="button primary" href="#apps">Explore Apps</a>
        <a class="button" href="#contact">Get in touch</a>
      </div>
    </section>

    <section id="apps" class="grid" aria-label="Featured apps">
      <article class="card">
        <span class="chip">New</span>
        <h3>Tap Timer</h3>
        <p>One‑tap interval timer for quick sprints. Zero setup, clean sound.</p>
      </article>
      <article class="card">
        <span class="chip">Fun</span>
        <h3>Mood Mixer</h3>
        <p>Blend emojis to match your vibe. Copy in one tap.</p>
      </article>
      <article class="card">
        <span class="chip">Tools</span>
        <h3>Snap Note</h3>
        <p>Sticky notes that auto‑save to your browser. Light and fast.</p>
      </article>
      <article class="card">
        <span class="chip">Beta</span>
        <h3>Decision Spinner</h3>
        <p>Give it options, spin once, move on. Analysis paralysis: solved.</p>
      </article>
    </section>

    <section id="about" class="grid" aria-label="About Microfun">
      <article class="card" style="grid-column: 1 / -1;">
        <h3>About</h3>
        <p>Microfun Apps builds tiny, delightful utilities for everyday life. No accounts. No ads. Just good vibes and quick wins.</p>
      </article>
    </section>

    <section id="contact" class="grid" aria-label="Contact">
      <article class="card" style="grid-column: 1 / -1;">
        <h3>Contact</h3>
        <p>Email us: <a href="mailto:hello@microfunapps.example">hello@microfunapps.example</a></p>
      </article>
    </section>
  </main>

  <footer>
    <div class="container">
      <div>© <span id="year"></span> Microfun Apps. All rights reserved.</div>
      <div class="small">Made with ❤️ and vanilla HTML/CSS.</div>
    </div>
  </footer>

  <button class="button theme-toggle" id="themeToggle" aria-live="polite" aria-label="Toggle theme">Toggle theme</button>

  <script>
    // Set current year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Simple theme toggle using data-theme attribute
    const btn = document.getElementById('themeToggle');
    const THEME_KEY = 'microfun-theme';
    const saved = localStorage.getItem(THEME_KEY);
    if(saved){
      document.documentElement.dataset.theme = saved;
      if(saved === 'light') applyLight(); else applyDark();
    }

    function applyLight(){
      // Force light by flipping to a CSS light palette via inline vars
      document.documentElement.style.setProperty('--bg', '#f8fafc');
      document.documentElement.style.setProperty('--bg-soft', '#f1f5f9');
      document.documentElement.style.setProperty('--txt', '#0b1020');
      document.documentElement.style.setProperty('--muted', '#475569');
      document.documentElement.style.setProperty('--card', 'rgba(255,255,255,0.9)');
      document.documentElement.style.setProperty('--border', 'rgba(2,6,23,0.08)');
      document.documentElement.style.setProperty('--shadow', '0 10px 24px rgba(2,6,23,0.08)');
      btn.setAttribute('aria-label','Switch to dark theme');
      btn.textContent = 'Dark mode';
    }
    function applyDark(){
      document.documentElement.style.setProperty('--bg', '#0b1020');
      document.documentElement.style.setProperty('--bg-soft', '#0f152a');
      document.documentElement.style.setProperty('--txt', '#e6e7ee');
      document.documentElement.style.setProperty('--muted', '#94a3b8');
      document.documentElement.style.setProperty('--card', 'rgba(255,255,255,0.06)');
      document.documentElement.style.setProperty('--border', 'rgba(255,255,255,0.12)');
      document.documentElement.style.setProperty('--shadow', '0 10px 30px rgba(2,6,23,0.5)');
      btn.setAttribute('aria-label','Switch to light theme');
      btn.textContent = 'Light mode';
    }

    btn.addEventListener('click', () => {
      const now = document.documentElement.dataset.theme === 'light' ? 'dark' : 'light';
      document.documentElement.dataset.theme = now;
      (now === 'light' ? applyLight : applyDark)();
      localStorage.setItem(THEME_KEY, now);
    });
  </script>
</body>
</html>
