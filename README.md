<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mohit Tumati | Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0b0f19;
      --card-bg: rgba(22, 27, 46, 0.7);
      --card-border: rgba(255, 255, 255, 0.08);
      --text-main: #f8fafc;
      --text-muted: #94a3b8;
      --accent-management: #38bdf8;
      --accent-dance: #f43f5e;
      --accent-tech: #10b981;
      --primary: #6366f1;
      --font-body: 'Plus Jakarta Sans', sans-serif;
      --font-heading: 'Space Grotesk', sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background-color: var(--bg);
      color: var(--text-main);
      font-family: var(--font-body);
      min-height: 100vh;
      overflow-x: hidden;
      line-height: 1.6;
    }

    /* Ambient background glow */
    .glow-bg {
      position: fixed;
      top: -20%;
      left: 50%;
      transform: translateX(-50%);
      width: 800px;
      height: 600px;
      background: radial-gradient(circle, rgba(99, 102, 241, 0.15) 0%, rgba(11, 15, 25, 0) 70%);
      z-index: -1;
      pointer-events: none;
    }

    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 3rem 1.5rem;
    }

    /* Hero Section */
    .hero {
      text-align: center;
      padding: 3rem 1rem 4rem;
      position: relative;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: rgba(99, 102, 241, 0.12);
      border: 1px solid rgba(99, 102, 241, 0.3);
      padding: 0.4rem 1rem;
      border-radius: 9999px;
      font-size: 0.85rem;
      color: #a5b4fc;
      font-weight: 600;
      letter-spacing: 0.05em;
      margin-bottom: 1.5rem;
      text-transform: uppercase;
    }

    .badge::before {
      content: "";
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: #818cf8;
      box-shadow: 0 0 8px #818cf8;
    }

    h1 {
      font-family: var(--font-heading);
      font-size: clamp(2.5rem, 6vw, 4rem);
      font-weight: 700;
      letter-spacing: -0.02em;
      line-height: 1.1;
      margin-bottom: 1rem;
    }

    .subtitle {
      font-size: 1.125rem;
      color: var(--text-muted);
      max-width: 600px;
      margin: 0 auto 2rem;
    }

    .cta-row {
      display: flex;
      justify-content: center;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.75rem 1.5rem;
      border-radius: 8px;
      font-weight: 600;
      font-size: 0.95rem;
      text-decoration: none;
      transition: all 0.2s ease;
    }

    .btn-primary {
      background: var(--primary);
      color: #ffffff;
      box-shadow: 0 4px 14px rgba(99, 102, 241, 0.35);
    }

    .btn-primary:hover {
      background: #4f46e5;
      transform: translateY(-2px);
    }

    .btn-secondary {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid var(--card-border);
      color: var(--text-main);
    }

    .btn-secondary:hover {
      background: rgba(255, 255, 255, 0.1);
      transform: translateY(-2px);
    }

    /* Pillars / Focus Areas */
    .section-title {
      font-family: var(--font-heading);
      font-size: 1.75rem;
      margin-bottom: 1.5rem;
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.5rem;
      margin-bottom: 4rem;
    }

    .card {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      backdrop-filter: blur(12px);
      border-radius: 12px;
      padding: 1.75rem;
      transition: border-color 0.2s ease, transform 0.2s ease;
    }

    .card:hover {
      transform: translateY(-3px);
    }

    .card-tech:hover { border-color: var(--accent-tech); }
    .card-management:hover { border-color: var(--accent-management); }
    .card-dance:hover { border-color: var(--accent-dance); }

    .tag {
      display: inline-block;
      font-size: 0.75rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.05em;
      margin-bottom: 0.75rem;
    }

    .tag-tech { color: var(--accent-tech); }
    .tag-management { color: var(--accent-management); }
    .tag-dance { color: var(--accent-dance); }

    .card h3 {
      font-family: var(--font-heading);
      font-size: 1.25rem;
      margin-bottom: 0.5rem;
    }

    .card p {
      color: var(--text-muted);
      font-size: 0.95rem;
    }

    footer {
      text-align: center;
      color: var(--text-muted);
      font-size: 0.85rem;
      padding-top: 2rem;
      border-top: 1px solid var(--card-border);
    }
  </style>
</head>
<body>
  <div class="glow-bg"></div>

  <main class="container">
    <!-- Hero Section -->
    <header class="hero">
      <div class="badge">Available for Projects & Roles</div>
      <h1>Mohit Tumati</h1>
      <p class="subtitle">
        Bridging technical execution, strategic product management, and creative performance arts.
      </p>
      <div class="cta-row">
        <a href="#work" class="btn btn-primary">View Highlights</a>
        <a href="mailto:contact@mohittumati.com" class="btn btn-secondary">Get in Touch</a>
      </div>
    </header>

    <!-- Core Domains -->
    <section id="work">
      <h2 class="section-title">What I Do</h2>
      <div class="grid">
        <div class="card card-tech">
          <span class="tag tag-tech">Engineering</span>
          <h3>Technical Architecture</h3>
          <p>Building clean, scalable full-stack applications with modern web tooling, strong system design, and performant code.</p>
        </div>

        <div class="card card-management">
          <span class="tag tag-management">Strategy</span>
          <h3>Product & Operations</h3>
          <p>Aligning cross-functional teams, driving roadmaps from 0 to 1, and optimizing resource delivery with agile execution.</p>
        </div>

        <div class="card card-dance">
          <span class="tag tag-dance">Creative</span>
          <h3>Choreography & Movement</h3>
          <p>Exploring stage performance, spatial dynamics, rhythm, and storytelling through collaborative choreography.</p>
        </div>
      </div>
    </section>

    <footer>
      <p>&copy; 2026 Mohit Tumati. Crafted with clean semantics and dark mode aesthetics.</p>
    </footer>
  </main>
</body>
</html>
 
  