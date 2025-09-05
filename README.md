<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>My Digital Portfolio</title>
  <style>
    :root{
      --bg:#0f172a;          /* slate-900 */
      --panel:#111827;       /* gray-900 */
      --muted:#94a3b8;       /* slate-400 */
      --text:#e5e7eb;        /* gray-200 */
      --accent:#22c55e;      /* green-500 */
      --accent-2:#38bdf8;    /* sky-400 */
      --ring:#334155;        /* slate-700 */
    }*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,Cantarell,"Helvetica Neue",Arial,"Noto Sans","Apple Color Emoji","Segoe UI Emoji";
  color:var(--text);
  background:radial-gradient(1200px 800px at 10% -10%, #1e293b 0%, rgba(15,23,42,0) 60%),
             radial-gradient(1200px 800px at 110% 10%, #0b3b46 0%, rgba(15,23,42,0) 50%),
             var(--bg);
  line-height:1.6;
}

/* Layout */
header{
  position:sticky; top:0; z-index:50;
  backdrop-filter: blur(6px);
  background:rgba(15,23,42,0.6);
  border-bottom:1px solid var(--ring);
}
.container{max-width:980px; margin:0 auto; padding:0 1rem}
nav{
  display:flex; align-items:center; justify-content:space-between;
  height:64px;
}
nav a.brand{
  font-weight:700; letter-spacing:0.4px; text-decoration:none; color:var(--text);
}
nav .links{display:flex; gap:1rem; flex-wrap:wrap}
nav .links a{color:var(--muted); text-decoration:none; padding:6px 10px; border-radius:10px}
nav .links a:hover, nav .links a:focus{outline:none; color:var(--text); background:#0b1220}

main{padding:3rem 0}
section{padding:3rem 0; border-bottom:1px dashed var(--ring)}
section:last-of-type{border-bottom:none}

/* Hero */
.hero{display:grid; grid-template-columns:1.1fr; gap:1.5rem; text-align:center}
.badge{display:inline-flex; align-items:center; gap:8px; padding:6px 10px; border:1px solid var(--ring); border-radius:999px; color:var(--muted)}
.badge .dot{width:8px; height:8px; border-radius:999px; background:var(--accent)}
h1{font-size:clamp(1.8rem, 2.4vw + 1rem, 3rem); line-height:1.2; margin:0.6rem 0}
.subtitle{color:var(--muted); max-width:60ch; margin:0 auto}

.cta{margin-top:1.25rem; display:flex; gap:.75rem; justify-content:center; flex-wrap:wrap}
.btn{appearance:none; border:none; padding:.9rem 1.1rem; border-radius:14px; cursor:pointer; font-weight:600}
.btn.primary{background:linear-gradient(90deg, var(--accent), var(--accent-2)); color:#061222}
.btn.ghost{background:transparent; color:var(--text); border:1px solid var(--ring)}
.btn:focus-visible{outline:3px solid var(--accent-2)}

/* Grid cards */
.grid{display:grid; gap:1rem}
@media (min-width:700px){ .grid{grid-template-columns:repeat(3, 1fr)} }

.card{background:rgba(17,24,39,0.7); border:1px solid var(--ring); border-radius:18px; padding:1rem}
.card h3{margin:.2rem 0 .5rem}
.muted{color:var(--muted)}

/* Lists */
ul.clean{list-style:none; padding:0; margin:.25rem 0}
ul.clean li{padding:.35rem 0; display:flex; align-items:flex-start; gap:.6rem}
ul.clean li .tick{margin-top:.35rem; width:.9rem; height:.9rem; border-radius:3px; background:linear-gradient(90deg, var(--accent), var(--accent-2))}

/* Project list */
.projects{display:grid; gap:1rem}
@media (min-width:800px){ .projects{grid-template-columns:repeat(2,1fr)} }
.project{background:rgba(17,24,39,0.7); border:1px solid var(--ring); border-radius:18px; padding:1rem}
.project h4{margin:.2rem 0 .25rem}
.project a{color:var(--accent-2); text-decoration:none}
.project a:hover{text-decoration:underline}

/* Contact */
form{display:grid; gap:.75rem; max-width:520px}
label{font-weight:600}
input, textarea{
  width:100%; padding:.8rem .9rem; border-radius:12px; border:1px solid var(--ring);
  background:#0b1220; color:var(--text)
}
textarea{min-height:120px}
.note{font-size:.95rem; color:var(--muted)}

footer{padding:2rem 0; color:var(--muted)}

  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav>
        <a class="brand" href="#">S.Parvathavarthini</a>
        <div class="links" aria-label="Primary">
          <a href="#about">About</a>
          <a href="#skills">Skills</a>
          <a href="#projects">Projects</a>
          <a href="#contact">Contact</a>
        </div>
      </nav>
    </div>
  </header>  <main class="container">
    <!-- Hero -->
    <section class="hero" id="home">
      <span class="badge" aria-label="Availability">
        <span class="dot" aria-hidden="true"></span>
        Open to opportunities
      </span>
      <h1>Front‑End Developer & UI Enthusiast</h1>
      <p class="subtitle">I build clean, accessible web experiences with HTML, CSS, and JavaScript. I care about performance, semantics, and simple design.</p>
      <div class="cta">
        <a class="btn primary" href="#projects">View Projects</a>
        <a class="btn ghost" href="#contact">Contact Me</a>
      </div>
    </section><!-- About -->
<section id="about" aria-labelledby="about-title">
  <h2 id="about-title">About</h2>
  <p class="muted">Short intro about yourself. Example:</p>
  <p>I’m a self‑taught developer from Chennai, focusing on responsive, accessible interfaces. I enjoy turning ideas into products and collaborating with friendly teams.</p>

  <div class="grid" style="margin-top:1rem">
    <div class="card">
      <h3>Highlights</h3>
      <ul class="clean">
        <li><span class="tick"></span><span>2+ years building web UIs</span></li>
        <li><span class="tick"></span><span>Strong in semantic HTML & modern CSS</span></li>
        <li><span class="tick"></span><span>Basics of React & APIs</span></li>
      </ul>
    </div>
    <div class="card">
      <h3>Education</h3>
      <ul class="clean">
        <li><span class="tick"></span><span>B.Sc. Computer Science — 2023</span></li>
        <li><span class="tick"></span><span>Frontend Mentor challenges</span></li>
        <li><span class="tick"></span><span>100 Days of Code</span></li>
      </ul>
    </div>
    <div class="card">
      <h3>Contact</h3>
      <ul class="clean">
        <li><span class="tick"></span><span>Email: parvatha5454@gmail.com</span></li>
        <li><span class="tick"></span><span>Phone: +91 90000 00000</span></li>
        <li><span class="tick"></span><span>Location: Tamil Nadu, India</span></li>
      </ul>
    </div>
  </div>
</section>

<!-- Skills -->
<section id="skills" aria-labelledby="skills-title">
  <h2 id="skills-title">Skills</h2>
  <div class="grid" style="margin-top:.5rem">
    <div class="card">
      <h3>Core</h3>
      <ul class="clean">
        <li><span class="tick"></span><span>HTML5 (semantic, accessible)</span></li>
        <li><span class="tick"></span><span>CSS3 (Flexbox, Grid, animations)</span></li>
        <li><span class="tick"></span><span>JavaScript (ES6+ basics)</span></li>
      </ul>
    </div>
    <div class="card">
      <h3>Tools</h3>
      <ul class="clean">
        <li><span class="tick"></span><span>Git & GitHub</span></li>
        <li><span class="tick"></span><span>VS Code</span></li>
        <li><span class="tick"></span><span>Chrome DevTools</span></li>
      </ul>
    </div>
    <div class="card">
      <h3>Soft</h3>
      <ul class="clean">
        <li><span class="tick"></span><span>Communication</span></li>
        <li><span class="tick"></span><span>Time management</span></li>
        <li><span class="tick"></span><span>Problem solving</span></li>
      </ul>
    </div>
  </div>
</section>

<!-- Projects -->
<section id="projects" aria-labelledby="projects-title">
  <h2 id="projects-title">Projects</h2>
  <div class="projects" style="margin-top:.5rem">
    <article class="project">
      <h4>Task Tracker</h4>
      <p class="muted">A simple to‑do app with localStorage. Add, complete, and filter tasks.</p>
      <p><a href="#" aria-label="Open Task Tracker project">Live Demo</a> · <a href="#" aria-label="View Task Tracker code on GitHub">Source</a></p>
    </article>
    <article class="project">
      <h4>Portfolio Template</h4>
      <p class="muted">This page itself — clean, responsive, and fast. Copy & customise.</p>
      <p><a href="#">Live Demo</a> · <a href="#">Source</a></p>
    </article>
    <article class="project">
      <h4>Weather Widget</h4>
      <p class="muted">Fetches and displays current weather for any city using a public API.</p>
      <p><a href="#">Live Demo</a> · <a href="#">Source</a></p>
    </article>
    <article class="project">
      <h4>Landing Page</h4>
      <p class="muted">A responsive marketing page using CSS Grid and accessible components.</p>
      <p><a href="#">Live Demo</a> · <a href="#">Source</a></p>
    </article>
  </div>
</section>

<!-- Contact -->
<section id="contact" aria-labelledby="contact-title">
  <h2 id="contact-title">Contact</h2>
  <p class="note">Prefer email? Send to <strong>parvatha5454@gmail.com</strong>. Or use the form below:</p>
  <form onsubmit="event.preventDefault(); alert('Thanks! I\'ll get back to you soon.');" aria-label="Contact form">
    <div>
      <label for="name">Name</label>
      <input id="name" name="name" type="text" placeholder="Your name" required />
    </div>
    <div>
      <label for="email">Email</label>
      <input id="email" name="email" type="email" placeholder="parvatha5454@gmail.com" required />
    </div>
    <div>
      <label for="message">Message</label>
      <textarea id="message" name="message" placeholder="Say hello..." required></textarea>
    </div>
    <button class="btn primary" type="submit">Send Message</button>
  </form>
</section>

  </main>  <footer>
    <div class="container">
      <small>© <span id="year"></span> S.Parvathavarthini • Built with pure HTML & CSS</small>
    </div>
  </footer>  <script>
    // keep the year current
    document.getElementById('year').textContent = new Date().getFullYear();
  </script></body>
</html>
