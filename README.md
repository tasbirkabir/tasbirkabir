<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tasbir Kabir — Entrepreneur / AI-native SaaS</title>
<style>
  :root{
    --ink:#101010;
    --paper:#f4f0e6;
    --white:#fffdf8;
    --yellow:#ffe500;
    --orange:#ff4d00;
    --muted:#686868;
    --grid:rgba(16,16,16,.07);
    --shadow:10px 10px 0 var(--ink);
    --shadow-sm:7px 7px 0 var(--ink);
  }

  *{box-sizing:border-box;margin:0;padding:0}

  html{scroll-behavior:smooth}

  body{
    background:var(--paper);
    color:var(--ink);
    font-family:Arial, Helvetica, sans-serif;
    line-height:1.45;
    overflow-x:hidden;
    background-image:
      linear-gradient(var(--grid) 1px, transparent 1px),
      linear-gradient(90deg, var(--grid) 1px, transparent 1px);
    background-size:42px 42px;
  }

  a{color:inherit}
  ::selection{background:var(--yellow);color:var(--ink)}

  .wrap{
    width:min(1180px, calc(100% - 34px));
    margin:0 auto;
    padding:22px 0 70px;
  }

  .mono{
    font-family:"Courier New", Courier, monospace;
    letter-spacing:.08em;
    text-transform:uppercase;
  }

  .topbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:20px;
    background:var(--ink);
    color:var(--paper);
    border:4px solid var(--ink);
    padding:11px 16px;
    box-shadow:6px 6px 0 var(--yellow);
    margin-bottom:42px;
  }

  .topbar .brand{
    font:700 12px "Courier New", monospace;
  }

  .status{
    display:inline-flex;
    align-items:center;
    gap:8px;
  }

  .status::before{
    content:"";
    width:9px;
    height:9px;
    background:var(--orange);
    border:2px solid var(--paper);
    display:inline-block;
  }

  .nav{
    display:flex;
    gap:18px;
    flex-wrap:wrap;
    font:700 11px "Courier New", monospace;
  }

  .nav a{
    text-decoration:none;
    color:var(--paper);
  }

  .nav a:hover{color:var(--yellow)}

  .section-kicker{
    display:flex;
    align-items:center;
    gap:14px;
    margin:68px 0 22px;
  }

  .section-kicker .num{
    background:var(--ink);
    color:var(--yellow);
    border:3px solid var(--ink);
    padding:5px 9px;
    font:700 12px "Courier New", monospace;
  }

  .section-kicker h2{
    font-size:clamp(25px, 5vw, 46px);
    line-height:1;
    text-transform:uppercase;
    letter-spacing:-.04em;
  }

  .section-kicker .line{
    height:4px;
    background:var(--ink);
    flex:1;
  }

  .hero{
    border:4px solid var(--ink);
    background:var(--white);
    box-shadow:15px 15px 0 var(--ink);
    padding:25px;
  }

  .hero-meta{
    display:flex;
    justify-content:space-between;
    gap:20px;
    padding-bottom:13px;
    margin-bottom:25px;
    border-bottom:2px dashed var(--ink);
    font:700 11px "Courier New", monospace;
  }

  .hero-grid{
    display:grid;
    grid-template-columns:minmax(0, 1.6fr) minmax(250px, .75fr);
    gap:28px;
    align-items:end;
  }

  .hero h1{
    font-size:clamp(64px, 12vw, 144px);
    line-height:.84;
    letter-spacing:-.07em;
    text-transform:uppercase;
    font-weight:1000;
  }

  .hero h1 .offset{
    display:block;
    margin-left:clamp(18px, 7vw, 90px);
    position:relative;
  }

  .hero h1 .offset::before{
    content:"";
    position:absolute;
    left:-31px;
    top:50%;
    transform:translateY(-50%);
    width:18px;
    height:18px;
    background:var(--orange);
    border:4px solid var(--ink);
  }

  .positioning{
    margin-top:27px;
    max-width:700px;
    font-size:clamp(19px, 2.8vw, 27px);
    line-height:1.22;
    font-weight:800;
  }

  .positioning strong{
    background:var(--yellow);
    padding:1px 5px;
  }

  .hero-sub{
    margin-top:13px;
    max-width:690px;
    font-size:17px;
    color:#2f2f2f;
  }

  .links{
    display:flex;
    gap:12px;
    flex-wrap:wrap;
    margin-top:25px;
  }

  .btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:8px;
    border:3px solid var(--ink);
    padding:10px 14px;
    background:var(--white);
    text-decoration:none;
    font:700 12px "Courier New", monospace;
    box-shadow:var(--shadow-sm);
    transition:.15s ease;
  }

  .btn:hover{
    transform:translate(3px,3px);
    box-shadow:3px 3px 0 var(--ink);
    background:var(--yellow);
  }

  .avatar-box{
    aspect-ratio:1;
    border:4px solid var(--ink);
    background:var(--yellow);
    box-shadow:11px 11px 0 var(--ink);
    position:relative;
    overflow:hidden;
  }

  .avatar-box img{
    width:100%;
    height:100%;
    object-fit:cover;
    display:block;
    filter:grayscale(100%) contrast(1.05);
  }

  .avatar-label{
    position:absolute;
    right:10px;
    bottom:10px;
    background:var(--ink);
    color:var(--yellow);
    padding:4px 8px;
    font:700 10px "Courier New", monospace;
  }

  .hero-footer{
    display:flex;
    justify-content:space-between;
    flex-wrap:wrap;
    gap:9px 22px;
    margin-top:29px;
    padding-top:15px;
    border-top:2px dashed var(--ink);
    font:700 10px "Courier New", monospace;
  }

  .hero-footer .hl{
    background:var(--ink);
    color:var(--yellow);
    padding:3px 7px;
  }

  .about-grid{
    display:grid;
    grid-template-columns:minmax(0, 1.45fr) minmax(260px, .8fr);
    gap:24px;
  }

  .about-copy,
  .meta-card,
  .focus-card,
  .project,
  .stack-card,
  .connect-card{
    background:var(--white);
    border:3px solid var(--ink);
    box-shadow:var(--shadow-sm);
  }

  .about-copy{
    padding:25px;
    font-size:17px;
  }

  .about-copy p + p{margin-top:18px}
  .about-copy strong{background:var(--yellow);padding:0 4px}

  .meta-card{padding:22px}

  .meta-card h3{
    font:700 11px "Courier New", monospace;
    border-bottom:2px solid var(--ink);
    padding-bottom:9px;
    margin-bottom:14px;
  }

  .meta-row{
    display:grid;
    grid-template-columns:95px 1fr;
    gap:12px;
    padding:9px 0;
    border-bottom:1px dashed #b5b5b5;
  }

  .meta-row:last-child{border-bottom:0}
  .meta-row .label{
    color:var(--muted);
    font:700 10px "Courier New", monospace;
    text-transform:uppercase;
  }
  .meta-row .value{font-weight:700}

  .build-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:18px;
  }

  .focus-card{
    padding:20px;
    min-height:175px;
    position:relative;
  }

  .focus-card:nth-child(1){background:var(--yellow)}
  .focus-card:nth-child(4){background:var(--ink);color:var(--paper)}
  .focus-card:nth-child(4) .tag{color:var(--yellow)}

  .tag{
    display:inline-block;
    border:2px solid currentColor;
    padding:4px 7px;
    font:700 10px "Courier New", monospace;
    margin-bottom:14px;
  }

  .focus-card h3{
    font-size:25px;
    line-height:1;
    letter-spacing:-.03em;
    text-transform:uppercase;
    margin-bottom:8px;
  }

  .focus-card p{
    font-size:14px;
    color:inherit;
    opacity:.86;
  }

  .work-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:20px;
  }

  .project{
    padding:22px;
    min-height:230px;
    position:relative;
    overflow:hidden;
  }

  .project.featured{
    background:var(--yellow);
    grid-column:span 2;
  }

  .project .topline{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:14px;
    margin-bottom:17px;
    font:700 10px "Courier New", monospace;
  }

  .project .badge{
    background:var(--ink);
    color:var(--yellow);
    padding:4px 8px;
  }

  .project h3{
    font-size:clamp(30px, 5vw, 52px);
    letter-spacing:-.055em;
    line-height:.95;
    text-transform:uppercase;
    margin-bottom:10px;
  }

  .project .one-liner{
    font:italic 700 14px "Courier New", monospace;
    margin-bottom:12px;
  }

  .project p{
    max-width:800px;
    font-size:15px;
  }

  .project .project-footer{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
    margin-top:18px;
    padding-top:15px;
    border-top:2px dashed var(--ink);
  }

  .project .mini{
    border:2px solid var(--ink);
    padding:6px 9px;
    font:700 10px "Courier New", monospace;
    background:rgba(255,255,255,.55);
  }

  .project.small .project-footer{
    position:absolute;
    bottom:20px;
    left:22px;
    right:22px;
  }

  .stack-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
  }

  .stack-card{padding:20px}
  .stack-card h3{
    font-size:18px;
    text-transform:uppercase;
    border-bottom:2px solid var(--ink);
    padding-bottom:9px;
    margin-bottom:11px;
  }
  .stack-card ul{list-style:none}
  .stack-card li{
    padding:6px 0;
    border-bottom:1px dashed #c4c4c4;
    font:13px "Courier New", monospace;
  }
  .stack-card li:last-child{border-bottom:0}
  .stack-card li::before{
    content:"→ ";
    color:var(--orange);
    font-weight:700;
  }

  .quote{
    background:var(--ink);
    color:var(--paper);
    border:4px solid var(--ink);
    box-shadow:15px 15px 0 var(--yellow);
    padding:47px 42px 42px;
    position:relative;
  }

  .quote-mark{
    position:absolute;
    left:25px;
    top:-28px;
    background:var(--yellow);
    color:var(--ink);
    padding:0 17px;
    font-size:72px;
    line-height:1;
    font-weight:1000;
  }

  .quote p{
    font-size:clamp(28px, 4vw, 48px);
    line-height:1.1;
    font-weight:1000;
    letter-spacing:-.04em;
    max-width:920px;
  }

  .quote p span{
    background:var(--yellow);
    color:var(--ink);
    padding:0 5px;
  }

  .quote .attr{
    margin-top:25px;
    color:var(--yellow);
    font:700 11px "Courier New", monospace;
  }

  .connect-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
  }

  .connect-card{
    padding:20px;
    text-decoration:none;
    transition:.15s ease;
  }

  .connect-card:hover{
    transform:translate(3px,3px);
    box-shadow:3px 3px 0 var(--ink);
    background:var(--yellow);
  }

  .connect-card .label{
    font:700 10px "Courier New", monospace;
    margin-bottom:10px;
  }

  .connect-card .value{
    font-size:17px;
    font-weight:900;
    overflow-wrap:anywhere;
  }

  .connect-card.missing{
    cursor:default;
    background:#ebe6d8;
  }

  .connect-card.missing:hover{
    transform:none;
    box-shadow:var(--shadow-sm);
    background:#ebe6d8;
  }

  .footer{
    margin-top:76px;
    padding-top:14px;
    border-top:4px solid var(--ink);
    display:flex;
    justify-content:space-between;
    gap:15px;
    flex-wrap:wrap;
    font:700 10px "Courier New", monospace;
  }

  @media (max-width: 950px){
    .build-grid{grid-template-columns:repeat(2,1fr)}
    .stack-grid{grid-template-columns:repeat(2,1fr)}
    .connect-grid{grid-template-columns:1fr 1fr}
  }

  @media (max-width: 720px){
    .topbar{align-items:flex-start}
    .nav{display:none}
    .hero-grid,
    .about-grid,
    .work-grid{grid-template-columns:1fr}
    .project.featured{grid-column:span 1}
    .build-grid,
    .stack-grid,
    .connect-grid{grid-template-columns:1fr}
    .hero h1 .offset{margin-left:0}
    .hero h1 .offset::before{display:none}
    .hero{padding:20px}
    .quote{padding:40px 25px 28px}
  }

  @media (max-width: 480px){
    .wrap{width:min(100% - 20px, 1180px)}
    .hero h1{font-size:58px}
    .positioning{font-size:18px}
    .section-kicker{margin-top:52px}
  }
</style>
</head>

<body>
<div class="wrap">

  <header class="topbar">
    <div class="brand status">LIVE / TASBIRKABIR</div>
    <nav class="nav">
      <a href="#about">ABOUT</a>
      <a href="#build">BUILD</a>
      <a href="#work">WORK</a>
      <a href="#stack">STACK</a>
      <a href="#connect">CONNECT</a>
    </nav>
  </header>

  <main>

    <section class="hero" aria-labelledby="hero-title">
      <div class="hero-meta">
        <span>[01] IDENTITY</span>
        <span>FILE: TASBIRKABIR.PROFILE / V1.0</span>
      </div>

      <div class="hero-grid">
        <div>
          <h1 id="hero-title">
            TASBIR
            <span class="offset">KABIR</span>
          </h1>

          <p class="positioning">
            <strong>Entrepreneur</strong> | Building AI-native SaaS with Agentic Engineering.
          </p>

          <p class="hero-sub">
            Building products, systems, and experiments where AI, software, automation, and product thinking meet.
          </p>

          <div class="links">
            <a class="btn" href="https://github.com/tasbirkabir" target="_blank" rel="noopener">→ GITHUB</a>
            <a class="btn" href="#" title="Add your LinkedIn URL">→ LINKEDIN</a>
            <a class="btn" href="#work">→ SEE WORK</a>
          </div>
        </div>

        <div class="avatar-box">
          <img
            src="https://avatars.githubusercontent.com/u/225493814?v=4"
            alt="Tasbir Kabir"
            onerror="this.style.display='none';this.parentElement.classList.add('fallback')"
          >
          <div class="avatar-label">@TASBIRKABIR</div>
        </div>
      </div>

      <div class="hero-footer">
        <span>@TASBIRKABIR</span>
        <span>AI-NATIVE SAAS / AGENTIC ENGINEERING</span>
        <span class="hl">BUILD → SHIP → COMPOUND</span>
      </div>
    </section>

    <section id="about">
      <div class="section-kicker">
        <span class="num">02</span>
        <h2>About</h2>
        <span class="line"></span>
      </div>

      <div class="about-grid">
        <div class="about-copy">
          <p>
            I build software products around emerging AI capabilities — from AI-native SaaS to
            automation, intelligent systems, and product experiments.
          </p>
          <p>
            My focus is not just on using AI, but on exploring how <strong>agentic engineering</strong>
            can change the way software gets built, operated, and improved.
          </p>
          <p>
            I like turning ideas into working products, learning from what actually ships,
            and building systems that can compound over time.
          </p>
        </div>

        <aside class="meta-card">
          <h3>// PROFILE</h3>
          <div class="meta-row">
            <span class="label">ROLE</span>
            <span class="value">Entrepreneur</span>
          </div>
          <div class="meta-row">
            <span class="label">BUILDING</span>
            <span class="value">AI-native SaaS</span>
          </div>
          <div class="meta-row">
            <span class="label">FOCUS</span>
            <span class="value">Agentic Engineering</span>
          </div>
          <div class="meta-row">
            <span class="label">MODE</span>
            <span class="value">Ship &amp; iterate</span>
          </div>
        </aside>
      </div>
    </section>

    <section id="build">
      <div class="section-kicker">
        <span class="num">03</span>
        <h2>What I Build</h2>
        <span class="line"></span>
      </div>

      <div class="build-grid">
        <article class="focus-card">
          <span class="tag">01 / AI-NATIVE</span>
          <h3>SaaS</h3>
          <p>Products that use AI as a core capability rather than a bolt-on feature.</p>
        </article>

        <article class="focus-card">
          <span class="tag">02 / AGENTIC</span>
          <h3>Engineering</h3>
          <p>New approaches to building software with agents, automation, and AI-assisted execution.</p>
        </article>

        <article class="focus-card">
          <span class="tag">03 / PRODUCT</span>
          <h3>Systems</h3>
          <p>Software shaped around real problems, useful workflows, and measurable outcomes.</p>
        </article>

        <article class="focus-card">
          <span class="tag">04 / EXPERIMENT</span>
          <h3>Ideas → Software</h3>
          <p>Fast experiments, prototypes, and product directions that can earn the right to grow.</p>
        </article>
      </div>
    </section>

    <section id="work">
      <div class="section-kicker">
        <span class="num">04</span>
        <h2>Selected Work</h2>
        <span class="line"></span>
      </div>

      <div class="work-grid">

        <article class="project featured">
          <div class="topline">
            <span class="badge">[001] FEATURED</span>
            <span>ATLAS ONE</span>
          </div>
          <h3>Atlas One</h3>
          <div class="one-liner">“See What AI Sees.”</div>
          <p>
            An AI visibility / discovery intelligence direction focused on understanding how
            brands, entities, and information surface across generative AI systems.
          </p>
          <div class="project-footer">
            <span class="mini">AI VISIBILITY</span>
            <span class="mini">DISCOVERY INTELLIGENCE</span>
            <span class="mini">IN DEVELOPMENT</span>
          </div>
        </article>

        <article class="project small">
          <div class="topline">
            <span class="badge">[002] PROJECT</span>
            <span>INTERAKT</span>
          </div>
          <h3>Interakt</h3>
          <div class="one-liner">Selected work / details to finalize.</div>
          <p>
            A project from my broader product-building work. Final public description can be
            added once the current positioning is confirmed.
          </p>
          <div class="project-footer">
            <span class="mini">PROJECT</span>
            <span class="mini">DETAILS PENDING</span>
          </div>
        </article>

        <article class="project small">
          <div class="topline">
            <span class="badge">[003] PROJECT</span>
            <span>DAYMARK</span>
          </div>
          <h3>Daymark</h3>
          <div class="one-liner">Selected work / details to finalize.</div>
          <p>
            Another project in my product-building portfolio. Final public description can be
            added once the current positioning is confirmed.
          </p>
          <div class="project-footer">
            <span class="mini">PROJECT</span>
            <span class="mini">DETAILS PENDING</span>
          </div>
        </article>

      </div>
    </section>

    <section>
      <div class="section-kicker">
        <span class="num">05</span>
        <h2>Currently</h2>
        <span class="line"></span>
      </div>

      <div class="build-grid">
        <article class="focus-card">
          <span class="tag">BUILDING</span>
          <h3>AI-native SaaS</h3>
          <p>Turning emerging AI capabilities into products people can actually use.</p>
        </article>

        <article class="focus-card">
          <span class="tag">EXPLORING</span>
          <h3>Agentic Engineering</h3>
          <p>How agents change software creation, execution, and iteration.</p>
        </article>

        <article class="focus-card">
          <span class="tag">EXPERIMENTING</span>
          <h3>AI Systems</h3>
          <p>Automation, intelligent workflows, developer tooling, and product patterns.</p>
        </article>

        <article class="focus-card">
          <span class="tag">THINKING ABOUT</span>
          <h3>Leverage</h3>
          <p>How small teams can build disproportionately useful software with AI.</p>
        </article>
      </div>
    </section>

    <section id="stack">
      <div class="section-kicker">
        <span class="num">06</span>
        <h2>Stack</h2>
        <span class="line"></span>
      </div>

      <div class="stack-grid">
        <article class="stack-card">
          <h3>AI / LLM</h3>
          <ul>
            <li>Generative AI</li>
            <li>Agentic workflows</li>
            <li>LLM tooling</li>
          </ul>
        </article>

        <article class="stack-card">
          <h3>Product</h3>
          <ul>
            <li>AI-native SaaS</li>
            <li>Rapid prototyping</li>
            <li>Product iteration</li>
          </ul>
        </article>

        <article class="stack-card">
          <h3>Engineering</h3>
          <ul>
            <li>Automation</li>
            <li>Backend systems</li>
            <li>Developer tooling</li>
          </ul>
        </article>
      </div>
    </section>

    <section>
      <div class="section-kicker">
        <span class="num">07</span>
        <h2>Builder Philosophy</h2>
        <span class="line"></span>
      </div>

      <div class="quote">
        <div class="quote-mark">"</div>
        <p>
          Build the thing. <span>Learn from reality.</span> Then make the system better than the
          version you started with.
        </p>
        <div class="attr">— TASBIR / BUILDING NOTES</div>
      </div>
    </section>

    <section>
      <div class="section-kicker">
        <span class="num">08</span>
        <h2>GitHub Activity</h2>
        <span class="line"></span>
      </div>

      <div class="about-grid">
        <div class="about-copy">
          <p><strong>@tasbirkabir</strong></p>
          <p>
            GitHub activity, contribution graphs, and selected repository highlights can be
            embedded here later using GitHub-compatible image endpoints.
          </p>
        </div>
        <aside class="meta-card">
          <h3>// STATS</h3>
          <div class="meta-row">
            <span class="label">PROFILE</span>
            <span class="value">github.com/tasbirkabir</span>
          </div>
          <div class="meta-row">
            <span class="label">RENDER</span>
            <span class="value">GitHub README compatible</span>
          </div>
          <div class="meta-row">
            <span class="label">MODE</span>
            <span class="value">Dynamic / external image</span>
          </div>
        </aside>
      </div>
    </section>

    <section id="connect">
      <div class="section-kicker">
        <span class="num">09</span>
        <h2>Connect</h2>
        <span class="line"></span>
      </div>

      <div class="connect-grid">
        <a class="connect-card" href="https://github.com/tasbirkabir" target="_blank" rel="noopener">
          <div class="label">→ GITHUB</div>
          <div class="value">@tasbirkabir</div>
        </a>

        <a class="connect-card missing" href="#" title="Replace with your LinkedIn URL">
          <div class="label">→ LINKEDIN</div>
          <div class="value">ADD LINK</div>
        </a>

        <a class="connect-card missing" href="#" title="Replace with your website URL">
          <div class="label">→ WEBSITE</div>
          <div class="value">ADD LINK</div>
        </a>
      </div>
    </section>

  </main>

  <footer class="footer">
    <span>● END OF FILE</span>
    <span>TASBIRKABIR / PERSONAL PROFILE</span>
    <span>V1.0</span>
  </footer>
</div>
</body>
</html>
