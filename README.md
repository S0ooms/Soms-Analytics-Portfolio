<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Analytics Portfolio</title>

  <style>
    :root {
      --bg: #ffffff;
      --text: #111827;
      --muted: #6b7280;
      --card: #f9fafb;
      --border: #e5e7eb;
      --accent: #2563eb;
    }

    body.dark {
      --bg: #0f172a;
      --text: #f1f5f9;
      --muted: #94a3b8;
      --card: #111827;
      --border: #1f2937;
      --accent: #60a5fa;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      transition: 0.3s;
    }

    header {
      padding: 80px 20px 40px;
      text-align: center;
    }

    h1 {
      font-size: 42px;
      margin-bottom: 10px;
    }

    p {
      color: var(--muted);
    }

    .buttons a {
      display: inline-block;
      margin: 8px;
      padding: 10px 16px;
      border: 1px solid var(--border);
      border-radius: 6px;
      text-decoration: none;
      color: var(--text);
      transition: 0.2s;
    }

    .buttons a:hover {
      background: var(--text);
      color: var(--bg);
    }

    .toggle {
      margin-top: 15px;
      cursor: pointer;
      font-size: 14px;
      color: var(--accent);
    }

    section {
      max-width: 950px;
      margin: auto;
      padding: 40px 20px;
      opacity: 0;
      transform: translateY(20px);
      transition: all 0.6s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      border-bottom: 1px solid var(--border);
      padding-bottom: 6px;
      margin-bottom: 20px;
    }

    .filters {
      margin-bottom: 20px;
    }

    .filters button {
      margin-right: 8px;
      padding: 6px 12px;
      border: 1px solid var(--border);
      background: none;
      color: var(--text);
      cursor: pointer;
      border-radius: 5px;
    }

    .card {
      background: var(--card);
      border: 1px solid var(--border);
      padding: 18px;
      border-radius: 10px;
      margin-bottom: 15px;
      transition: transform 0.2s;
    }

    .card:hover {
      transform: translateY(-3px);
    }

    .tag {
      font-size: 12px;
      border: 1px solid var(--border);
      padding: 2px 6px;
      border-radius: 5px;
      margin-right: 5px;
    }

    .project-img {
      width: 100%;
      height: 180px;
      background: #d1d5db;
      border-radius: 8px;
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #374151;
      font-size: 14px;
    }

    .star {
      font-size: 13px;
      color: var(--muted);
      margin-top: 8px;
    }

    a.link {
      color: var(--accent);
      text-decoration: none;
    }

    footer {
      text-align: center;
      padding: 40px;
      color: var(--muted);
      font-size: 13px;
    }
  </style>
</head>
<body>

<header>
  <h1>Your Name Here</h1>
  <p>Business Intelligence Analyst | Power BI • SQL • Excel</p>
  <p>Turning data into business insights and operational impact</p>

  <div class="buttons">
    <a href="INSERT_RESUME">Resume</a>
    <a href="INSERT_LINKEDIN">LinkedIn</a>
    <a href="INSERT_GITHUB">GitHub</a>
  </div>

  <div class="toggle" onclick="toggleTheme()">Toggle Dark Mode</div>
</header>

<section>
  <h2>About Me</h2>
  <p>
    Business Intelligence and Data Analyst focused on transforming operational data into insights through dashboards,
    reporting systems, and process improvement initiatives.
  </p>
</section>

<section>
  <h2>Featured Projects</h2>

  <div class="filters">
    <button onclick="filterProjects('all')">All</button>
    <button onclick="filterProjects('powerbi')">Power BI</button>
    <button onclick="filterProjects('sql')">SQL</button>
    <button onclick="filterProjects('excel')">Excel</button>
  </div>

  <div class="card project powerbi">
    <div class="project-img">Insert Dashboard Screenshot</div>
    <h3>Project Title</h3>
    <p>Problem → Solution summary goes here.</p>
    <span class="tag">Power BI</span>
    <span class="tag">SQL</span>

    <div class="star">
      <b>S:</b> Situation description here<br>
      <b>T:</b> Task description here<br>
      <b>A:</b> Action taken here<br>
      <b>R:</b> Result/impact here
    </div>

    <p><a class="link" href="INSERT_LINK">View Project</a></p>
  </div>

</section>

<section>
  <h2>Business Experience</h2>

  <div class="card">
    <div class="project-img">Insert Workflow / Report Screenshot</div>
    <h3>Business Impact Case</h3>
    <p>Describe automation, reporting system, or process improvement work.</p>
  </div>

</section>

<section>
  <h2>Learning Lab</h2>

  <div class="card">
    <div class="project-img">Insert Learning Project Screenshot</div>
    <h3>Guided Project</h3>
    <p>Learning-based analytics output or training project.</p>
    <a class="link" href="INSERT_LINK">View Work</a>
  </div>

</section>

<section>
  <h2>Skills</h2>
  <p>Power BI • SQL • Excel • Data Modeling • Process Improvement • Lean Six Sigma</p>
</section>

<section>
  <h2>Certifications</h2>
  <ul>
    <li>INSERT CERTIFICATION</li>
  </ul>
</section>

<section>
  <h2>Contact</h2>
  <p>Email: INSERT_EMAIL</p>
</section>

<footer>
  © 2026 Your Name. Built with GitHub Pages.
</footer>

<script>
  function toggleTheme() {
    document.body.classList.toggle('dark');
  }

  function filterProjects(type) {
    let projects = document.querySelectorAll('.project');
    projects.forEach(p => {
      if (type === 'all') {
        p.style.display = 'block';
      } else {
        p.style.display = p.classList.contains(type) ? 'block' : 'none';
      }
    });
  }

  // Scroll animation
  const sections = document.querySelectorAll('section');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, { threshold: 0.1 });

  sections.forEach(sec => observer.observe(sec));
</script>

</body>
</html>
