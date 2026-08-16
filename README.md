<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tasbir Kabir — AI Builder / Entrepreneur</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Archivo+Black&family=Space+Grotesk:wght@400;500;600;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root{
    --black:#0a0a0a;
    --paper:#f4f0e6;
    --card:#ffffff;
    --accent:#FFE500;
    --accent-2:#ff4d00;
    --muted:#6a6a6a;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html{scroll-behavior:smooth;}
  body{
    font-family:'Space Grotesk',sans-serif;
    background:var(--paper);
    color:var(--black);
    line-height:1.5;
    overflow-x:hidden;
    background-image:
      linear-gradient(rgba(10,10,10,.04) 1px,transparent 1px),
      linear-gradient(90deg,rgba(10,10,10,.04) 1px,transparent 1px);
    background-size:48px 48px;
  }
  ::selection{background:var(--accent);color:var(--black);}
  .mono{font-family:'Space Mono',monospace;}
  .container{max-width:1140px;margin:0 auto;padding:28px 28px 60px;}

  /* TOP BAR */
  .topbar{
    display:flex;justify-content:space-between;align-items:center;
    border:3px solid var(--black);background:var(--black);color:var(--paper);
    padding:10px 18px;font-family:'Space Mono',monospace;font-size:11px;
    text-transform:uppercase;letter-spacing:.1em;margin-bottom:36px;
    box-shadow:6px 6px 0 var(--accent);
  }
  .topbar .live{display:flex;align-items:center;gap:8px;}
  .topbar .live::before{
    content:'';display:inline-block;width:9px;height:9px;
    background:var(--accent-2);border:2px solid var(--paper);
    animation:pulse 1.6s infinite;
  }
  @keyframes pulse{0%,100%{opacity:1;}50%{opacity:.35;}}
  @media (prefers-reduced-motion:reduce){
    .topbar .live::before{animation:none;}
    *{transition:none!important;}
  }
  .topbar nav{display:flex;gap:18px;}
  .topbar nav a{color:var(--paper);text-decoration:none;}
  .topbar nav a:hover{color:var(--accent);}

  /* SECTION HEADER */
  .section-header{display:flex;align-items:center;gap:16px;margin-bottom:24px;margin-top:64px;}
  .section-header .num{
    font-family:'Space Mono',monospace;font-size:13px;
    background:var(--black);color:var(--accent);padding:5px 11px;
    border:2px solid var(--black);letter-spacing:.05em;font-weight:700;
  }
  .section-header .title{
    font-family:'Archivo Black',sans-serif;
    font-size:clamp(28px,5vw,46px);letter-spacing:-.02em;text-transform:uppercase;
  }
  .section-header .line{flex:1;height:4px;background:var(--black);}

  /* HERO */
  .hero{
    position:relative;border:4px solid var(--black);background:var(--card);
    padding:36px 36px 28px;box-shadow:14px 14px 0 var(--black);margin-bottom:12px;
  }
  .hero-meta{
    display:flex;justify-content:space-between;
    font-family:'Space Mono',monospace;font-size:11px;text-transform:uppercase;
    letter-spacing:.1em;border-bottom:2px dashed var(--black);
    padding-bottom:14px;margin-bottom:28px;
  }
  .hero-meta .right{color:var(--muted);}
  .hero-grid{display:grid;grid-template-columns:1.6fr 1fr;gap:36px;align-items:end;}
  .hero-title{
    font-family:'Archivo Black',sans-serif;
    font-size:clamp(56px,11vw,132px);line-height:.86;
    letter-spacing:-.045em;text-transform:uppercase;
  }
  .hero-title .block-2{display:block;margin-left:clamp(20px,8vw,96px);position:relative;}
  .hero-title .block-2::before{
    content:'●';color:var(--accent-2);position:absolute;
    left:-32px;top:50%;transform:translateY(-50%);font-size:.4em;
  }
  .hero-tagline{margin-top:28px;font-size:18px;max-width:540px;line-height:1.5;}
  .hero-tagline strong{background:var(--accent);padding:0 4px;font-weight:700;}
  .hero-links{margin-top:24px;display:flex;gap:14px;flex-wrap:wrap;}
  .hero-links a{
    font-family:'Space Mono',monospace;font-size:12px;text-transform:uppercase;
    letter-spacing:.08em;color:var(--black);text-decoration:none;
    border:2px solid var(--black);padding:8px 14px;background:var(--card);font-weight:700;
  }
  .hero-links a:hover{background:var(--black);color:var(--accent);}
  .hero-avatar{
    width:100%;aspect-ratio:1;background:var(--accent);
    border:4px solid var(--black);box-shadow:10px 10px 0 var(--black);
    position:relative;display:flex;align-items:center;justify-content:center;
    font-family:'Archivo Black',sans-serif;font-size:clamp(60px,14vw,120px);
    overflow:hidden;
  }
  .hero-avatar::after{
    content:'[ AVATAR — REPLACE ]';position:absolute;bottom:10px;right:12px;
    font-family:'Space Mono',monospace;font-size:10px;letter-spacing:.1em;
  }
  .hero-footer{
    display:flex;justify-content:space-between;gap:16px;flex-wrap:wrap;
    font-family:'Space Mono',monospace;font-size:11px;text-transform:uppercase;
    letter-spacing:.1em;border-top:2px dashed var(--black);
    padding-top:16px;margin-top:28px;
  }
  .hero-footer .atlas{background:var(--black);color:var(--accent);padding:2px 8px;}

  /* ABOUT */
  .about-grid{display:grid;grid-template-columns:1.4fr 1fr;gap:32px;align-items:start;}
  .about-text p{font-size:17px;line-height:1.65;margin-bottom:18px;}
  .about-text p strong{background:var(--accent);padding:0 4px;font-weight:700;}
  .about-meta{
    border:3px solid var(--black);background:var(--card);
    box-shadow:8px 8px 0 var(--black);padding:24px;
  }
  .about-meta h4{
    font-family:'Space Mono',monospace;font-size:11px;text-transform:uppercase;
    letter-spacing:.1em;border-bottom:2px solid var(--black);
    padding-bottom:8px;margin-bottom:16px;
  }
  .meta-block{margin-bottom:18px;}
  .meta-block:last-child{margin-bottom:0;}
  .meta-label{
    display:block;font-family:'Space Mono',monospace;font-size:10px;
    text-transform:uppercase;letter-spacing:.1em;color:var(--muted);margin-bottom:4px;
  }
  .meta-value{font-size:15px;font-weight:600;}

  /* PROJECTS */
  .project-card{
    border:4px solid var(--black);background:var(--card);padding:28px;
    margin-bottom:24px;box-shadow:10px 10px 0 var(--black);
    transition:transform .15s ease,box-shadow .15s ease;position:relative;
  }
  .project-card:hover{transform:translate(2px,2px);box-shadow:6px 6px 0 var(--black);}
  .project-card.featured{background:var(--accent);}
  .project-meta{
    display:flex;justify-content:space-between;align-items:center;
    border-bottom:2px solid var(--black);padding-bottom:12px;margin-bottom:20px;
    font-family:'Space Mono',monospace;font-size:11px;text-transform:uppercase;letter-spacing:.1em;
  }
  .project-meta .tag{background:var(--black);color:var(--accent);padding:4px 10px;font-weight:700;}
  .project-name{
    font-family:'Archivo Black',sans-serif;font-size:clamp(36px,6vw,64px);
    line-height:.95;letter-spacing:-.03em;text-transform:uppercase;
  }
  .project-tagline{
    font-family:'Space Mono',monospace;font-size:16px;margin-top:10px;font-style:italic;
  }
  .project-desc{font-size:16px;margin-top:16px;max-width:720px;line-height:1.6;}
  .project-grid{
    display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:24px;
    border-top:2px dashed var(--black);padding-top:20px;
  }
  .project-grid > div{font-size:14px;}
  .project-grid .meta-label{margin-bottom:2px;}
  .project-links{display:flex;gap:14px;margin-top:22px;flex-wrap:wrap;}
  .project-links a{
    font-family:'Space Mono',monospace;font-size:12px;text-transform:uppercase;
    letter-spacing:.08em;color:var(--black);text-decoration:none;
    border:2px solid var(--black);padding:6px 14px;background:var(--card);font-weight:700;
  }
  .project-links a:hover{background:var(--black);color:var(--accent);}
  .project-card.placeholder .project-name,
  .project-card.placeholder .project-tagline,
  .project-card.placeholder .project-desc,
  .project-card.placeholder .project-grid > div{color:var(--muted);}
  .project-card.placeholder .project-name{font-style:normal;}

  /* CURRENTLY */
  .now-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:24px;}
  .now-card{
    border:3px solid var(--black);background:var(--card);padding:24px;
    box-shadow:8px 8px 0 var(--black);position:relative;
    transition:transform .15s ease,box-shadow .15s ease;
  }
  .now-card:hover{transform:translate(2px,2px);box-shadow:4px 4px 0 var(--black);}
  .now-card:nth-child(1){background:var(--accent);}
  .now-card:nth-child(4){background:var(--black);color:var(--paper);}
  .now-card:nth-child(4) .now-label{color:var(--accent);border-color:var(--accent);}
  .now-label{
    display:inline-block;font-family:'Space Mono',monospace;font-size:11px;
    text-transform:uppercase;letter-spacing:.1em;border:2px solid currentColor;
    padding:3px 8px;margin-bottom:14px;font-weight:700;
  }
  .now-card h4{
    font-family:'Archivo Black',sans-serif;font-size:22px;
    letter-spacing:-.02em;margin-bottom:8px;
  }
  .now-card p{font-size:14px;line-height:1.5;}

  /* STACK */
  .stack-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;}
  .stack-col{
    border:3px solid var(--black);background:var(--card);padding:22px;
    box-shadow:8px 8px 0 var(--black);
  }
  .stack-col h4{
    font-family:'Archivo Black',sans-serif;font-size:18px;letter-spacing:-.01em;
    text-transform:uppercase;border-bottom:2px solid var(--black);
    padding-bottom:8px;margin-bottom:14px;
  }
  .stack-col ul{list-style:none;}
  .stack-col li{
    font-family:'Space Mono',monospace;font-size:13px;padding:5px 0;
    border-bottom:1px dashed rgba(0,0,0,.2);color:var(--muted);
  }
  .stack-col li:last-child{border-bottom:none;}
  .stack-col li::before{content:'→ ';color:var(--accent-2);font-weight:700;}

  /* PHILOSOPHY */
  .quote-box{
    border:4px solid var(--black);background:var(--black);color:var(--paper);
    padding:60px 50px;position:relative;box-shadow:14px 14px 0 var(--accent);
  }
  .quote-mark{
    position:absolute;top:0;left:30px;transform:translateY(-50%);
    background:var(--accent);color:var(--black);font-family:'Archivo Black',sans-serif;
    font-size:80px;padding:0 20px;line-height:1;
  }
  .quote-text{
    font-family:'Archivo Black',sans-serif;font-size:clamp(24px,4vw,42px);
    line-height:1.15;letter-spacing:-.02em;margin-top:20px;
  }
  .quote-text .hl{background:var(--accent);color:var(--black);padding:0 6px;}
  .quote-text .strike{text-decoration:line-through;text-decoration-thickness:4px;color:var(--muted);}
  .quote-attr{
    font-family:'Space Mono',monospace;font-size:12px;text-transform:uppercase;
    letter-spacing:.15em;margin-top:30px;color:var(--accent);
  }

  /* ACTIVITY */
  .activity-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;}
  .activity-card{
    border:3px solid var(--black);background:var(--card);padding:20px;
    box-shadow:8px 8px 0 var(--black);
  }
  .activity-card.full{grid-column:span 2;}
  .activity-card img{width:100%;height:auto;display:block;}
  .activity-label{
    font-family:'Space Mono',monospace;font-size:10px;text-transform:uppercase;
    letter-spacing:.1em;color:var(--muted);margin-bottom:10px;display:block;
  }

  /* CONNECT */
  .connect-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:20px;}
  .connect-card{
    border:3px solid var(--black);background:var(--card);padding:22px 24px;
    box-shadow:8px 8px 0 var(--black);text-decoration:none;color:var(--black);
    display:flex;justify-content:space-between;align-items:center;gap:16px;
    transition:transform .15s ease,box-shadow .15s ease;
  }
  .connect-card:hover{
    transform:translate(2px,2px);box-shadow:4px 4px 0 var(--black);background:var(--accent);
  }
  .connect-card .mono{font-size:12px;text-transform:uppercase;letter-spacing:.1em;font-weight:700;}
  .connect-card .link-value{font-family:'Space Mono',monospace;font-size:14px;}
  .connect-card.placeholder .link-value{color:var(--muted);font-style:italic;}

  /* FOOTER */
  .footer{
    margin-top:80px;border-top:4px solid var(--black);padding-top:16px;
    display:flex;justify-content:space-between;flex-wrap:wrap;gap:8px;
    font-family:'Space Mono',monospace;font-size:11px;text-transform:uppercase;letter-spacing:.1em;
  }

  /* RESPONSIVE */
  @media (max-width:800px){
    .hero-grid,.about-grid,.now-grid,.stack-grid,.connect-grid,.activity-grid{grid-template-columns:1fr;}
    .hero-title .block-2{margin-left:0;}
    .hero-title .block-2::before{display:none;}
    .project-grid{grid-template-columns:1fr;}
    .topbar nav{display:none;}
    .quote-box{padding:50px 28px;}
  }
  @media (max-width:480px){
    .container{padding:16px;}
    .hero{padding:24px 20px;box-shadow:8px 8px 0 var(--black);}
    .quote-mark{left:14px;font-size:54px;}
  }
</style>
</head>
<body>
<div class="container">

  <!-- TOP BAR -->
  <div class="topbar">
    <span class="live">LIVE / TASBIRKABIR</span>
    <nav>
      <a href="#about">about</a>
      <a href="#work">work</a>
      <a href="#now">now</a>
      <a href="#stack">stack</a>
      <a href="#connect">connect</a>
    </nav>
  </div>

  <!-- HERO -->
  <section class="hero" id="top">
    <div class="hero-meta">
      <span>[01] IDENTITY</span>
      <span class="right">FILE: tasbirkabir.profile / v1.0</span>
    </div>
    <div class="hero-grid">
      <div>
        <h1 class="hero-title">
          TASBIR
          <span class="block-2">KABIR</span>
        </h1>
        <p class="hero-tagline">AI builder / entrepreneur. Building <strong>Atlas One</strong> — an AI visibility &amp; discovery intelligence platform. <em>"See What AI Sees."</em></p>
        <div class="hero-links">
          <a href="https://github.com/tasbirkabir" target="_blank" rel="noopener">→ GitHub</a>
          <a href="mailto:tasbir777x@gmail.com">→ Email</a>
          <a href="#work">→ See Work</a>
        </div>
      </div>
      <div class="hero-avatar" aria-label="Avatar placeholder">TK</div>
    </div>
    <div class="hero-footer">
      <span>@tasbirkabir</span>
      <span>AI Consultant &amp; Entrepreneur</span>
      <span class="atlas">ATLAS ONE — "See What AI Sees."</span>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="about" id="about">
    <div class="section-header">
      <span class="num">02</span>
      <span class="title">About</span>
      <span class="line"></span>
    </div>
    <div class="about-grid">
      <div class="about-text">
        <p>I build AI products — not demos, but systems that observe, measure, and shape how information surfaces across generative AI. My main focus is <strong>Atlas One</strong>, an AI visibility &amp; discovery intelligence platform I'm building toward becoming a category-defining intelligence layer for how brands, entities, and information appear across generative systems.</p>
        <p>I care about <strong>proprietary datasets</strong>, defensible architecture, and shipping MVPs that earn the right to grow into enterprise-grade products. Long-term thinking over feature bloat. Substance over noise.</p>
        <p>Outside Atlas One, I experiment with developer tooling, automation, and data-driven product patterns. I treat software as a vehicle for leverage — not as an end in itself.</p>
      </div>
      <div class="about-meta">
        <h4>// IDENTITY</h4>
        <div class="meta-block"><span class="meta-label">Role</span><span class="meta-value">AI Consultant &amp; Entrepreneur</span></div>
        <div class="meta-block"><span class="meta-label">Focus</span><span class="meta-value">AI Visibility / GEO</span></div>
        <div class="meta-block"><span class="meta-label">Building</span><span class="meta-value">Atlas One</span></div>
        <div class="meta-block"><span class="meta-label">Orientation</span><span class="meta-value">Product / Systems / Defensibility</span></div>
        <div class="meta-block"><span class="meta-label">Mode</span><span class="meta-value">Ship MVP → Compound</span></div>
      </div>
    </div>
  </section>

  <!-- WHAT I BUILD -->
  <section class="work" id="work">
    <div class="section-header">
      <span class="num">03</span>
      <span class="title">What I Build</span>
      <span class="line"></span>
    </div>

    <!-- Atlas One (featured) -->
    <div class="project-card featured">
      <div class="project-meta">
        <span class="tag">[001] FLAGSHIP</span>
        <span>STATUS: IN DEVELOPMENT</span>
      </div>
      <h3 class="project-name">Atlas One</h3>
      <p class="project-tagline">"See What AI Sees."</p>
      <p class="project-desc">AI visibility &amp; discovery intelligence platform. Building the intelligence layer for how brands, entities, and information appear across generative AI systems. Proprietary datasets. Data moats. Defensible architecture over feature bloat. MVP first — enterprise capabilities later.</p>
      <div class="project-grid">
        <div><span class="meta-label">Stack</span><div>[ to be added ]</div></div>
        <div><span class="meta-label">Status</span><div>Building</div></div>
        <div><span class="meta-label">Vision</span><div>Category-defining AI visibility layer</div></div>
      </div>
      <div class="project-links">
        <a href="#" target="_blank" rel="noopener">→ Repository</a>
        <a href="#" target="_blank" rel="noopener">→ Live</a>
        <a href="#" target="_blank" rel="noopener">→ Docs</a>
      </div>
    </div>

    <!-- Interakt (placeholder) -->
    <div class="project-card placeholder">
      <div class="project-meta">
        <span class="tag">[002] PROJECT</span>
        <span>STATUS: [ update ]</span>
      </div>
      <h3 class="project-name">Interakt</h3>
      <p class="project-tagline">[ Add latest accurate description ]</p>
      <p class="project-desc">[ Project description pending your input. Replace this with the current positioning of Interakt / Interaktion — what it does, who it's for, and what makes it interesting. ]</p>
      <div class="project-grid">
        <div><span class="meta-label">Stack</span><div>[ TBD ]</div></div>
        <div><span class="meta-label">Status</span><div>[ TBD ]</div></div>
        <div><span class="meta-label">Repo</span><div>[ TBD ]</div></div>
      </div>
      <div class="project-links"><a href="#" target="_blank" rel="noopener">→ Repository</a></div>
    </div>

    <!-- Additional project slot -->
    <div class="project-card placeholder">
      <div class="project-meta">
        <span class="tag">[003] PROJECT</span>
        <span>STATUS: [ add ]</span>
      </div>
      <h3 class="project-name">[ Your Project ]</h3>
      <p class="project-tagline">[ One-line description ]</p>
      <p class="project-desc">[ Add a project you want to showcase — software, AI experiment, dev tool, or anything that reflects your builder identity. ]</p>
      <div class="project-grid">
        <div><span class="meta-label">Stack</span><div>[ TBD ]</div></div>
        <div><span class="meta-label">Status</span><div>[ TBD ]</div></div>
        <div><span class="meta-label">Repo</span><div>[ TBD ]</div></div>
      </div>
      <div class="project-links"><a href="#" target="_blank" rel="noopener">→ Repository</a></div>
    </div>
  </section>

  <!-- CURRENTLY -->
  <section class="now" id="now">
    <div class="section-header">
      <span class="num">04</span>
      <span class="title">Currently</span>
      <span class="line"></span>
    </div>
    <div class="now-grid">
      <div class="now-card">
        <span class="now-label">Building</span>
        <h4>Atlas One</h4>
        <p>AI visibility &amp; discovery intelligence platform. Long-term product direction.</p>
      </div>
      <div class="now-card">
        <span class="now-label">Researching</span>
        <h4>GEO / Generative Engine Optimization</h4>
        <p>How information surfaces across LLMs and generative systems.</p>
      </div>
      <div class="now-card">
        <span class="now-label">Experimenting</span>
        <h4>AI discovery patterns</h4>
        <p>Datasets, retrieval signals, and entity-level visibility signals.</p>
      </div>
      <div class="now-card">
        <span class="now-label">Thinking about</span>
        <h4>Defensibility</h4>
        <p>Proprietary datasets, data moats, and long-term product architecture.</p>
      </div>
    </div>
  </section>

  <!-- STACK -->
  <section class="stack" id="stack">
    <div class="section-header">
      <span class="num">05</span>
      <span class="title">Stack</span>
      <span class="line"></span>
    </div>
    <div class="stack-grid">
      <div class="stack-col">
        <h4>AI / LLM</h4>
        <ul><li>[ your stack ]</li><li>[ frameworks ]</li><li>[ models / providers ]</li></ul>
      </div>
      <div class="stack-col">
        <h4>Backend</h4>
        <ul><li>[ language ]</li><li>[ framework ]</li><li>[ runtime ]</li></ul>
      </div>
      <div class="stack-col">
        <h4>Frontend</h4>
        <ul><li>[ framework ]</li><li>[ styling ]</li><li>[ tooling ]</li></ul>
      </div>
      <div class="stack-col">
        <h4>Data</h4>
        <ul><li>[ database ]</li><li>[ vector store ]</li><li>[ pipeline ]</li></ul>
      </div>
      <div class="stack-col">
        <h4>Infrastructure</h4>
        <ul><li>[ cloud ]</li><li>[ deployment ]</li><li>[ orchestration ]</li></ul>
      </div>
      <div class="stack-col">
        <h4>Automation / Tools</h4>
        <ul><li>[ scripting ]</li><li>[ CI/CD ]</li><li>[ dev tools ]</li></ul>
      </div>
    </div>
  </section>

  <!-- PHILOSOPHY -->
  <section class="philosophy">
    <div class="section-header">
      <span class="num">06</span>
      <span class="title">Builder Philosophy</span>
      <span class="line"></span>
    </div>
    <div class="quote-box">
      <div class="quote-mark">"</div>
      <p class="quote-text">Most build for the <span class="strike">demo</span>. I build for the <span class="hl">dataset</span>. Ship the smallest thing that earns the right to exist — then defend it with data, architecture, and patience.</p>
      <div class="quote-attr">— TK / Building Notes</div>
    </div>
  </section>

  <!-- GITHUB ACTIVITY -->
  <section class="activity" id="activity">
    <div class="section-header">
      <span class="num">07</span>
      <span class="title">GitHub Activity</span>
      <span class="line"></span>
    </div>
    <div class="activity-grid">
      <div class="activity-card">
        <span class="activity-label">→ STATS</span>
        <img src="https://github-readme-stats.vercel.app/api?username=tasbirkabir&show_icons=true&theme=default&hide_border=true" alt="GitHub Stats" loading="lazy">
      </div>
      <div class="activity-card">
        <span class="activity-label">→ STREAK</span>
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=tasbirkabir&theme=default&hide_border=true" alt="GitHub Streak" loading="lazy">
      </div>
      <div class="activity-card full">
        <span class="activity-label">→ CONTRIBUTION GRAPH</span>
        <img src="https://github-readme-activity-graph.vercel.app/graph?username=tasbirkabir&theme=default&hide_border=true" alt="Activity Graph" loading="lazy">
      </div>
    </div>
  </section>

  <!-- CONNECT -->
  <section class="connect" id="connect">
    <div class="section-header">
      <span class="num">08</span>
      <span class="title">Connect</span>
      <span class="line"></span>
    </div>
    <div class="connect-grid">
      <a href="https://github.com/tasbirkabir" class="connect-card" target="_blank" rel="noopener">
        <span class="mono">→ GitHub</span>
        <span class="link-value">@tasbirkabir</span>
      </a>
      <a href="mailto:tasbir777x@gmail.com" class="connect-card">
        <span class="mono">→ Email</span>
        <span class="link-value">tasbir777x@gmail.com</span>
      </a>
      <div class="connect-card placeholder">
        <span class="mono">→ LinkedIn</span>
        <span class="link-value">[ add url ]</span>
      </div>
      <div class="connect-card placeholder">
        <span class="mono">→ Website</span>
        <span class="link-value">[ add url ]</span>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <div class="footer">
    <span>● END OF FILE</span>
    <span>TASBIRKABIR / ATLAS ONE</span>
    <span>v1.0</span>
  </div>

</div>
</body>
</html>
