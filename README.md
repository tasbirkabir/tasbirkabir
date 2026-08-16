<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tasbir Kabir — Prototype</title>
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
  body{
    font-family:'Space Grotesk',sans-serif;
    background:var(--paper);
    color:var(--black);
    line-height:1.5;
    background-image:
      linear-gradient(rgba(10,10,10,.04) 1px,transparent 1px),
      linear-gradient(90deg,rgba(10,10,10,.04) 1px,transparent 1px);
    background-size:48px 48px;
    padding:40px;
  }
  .container{max-width:900px;margin:0 auto;}
  .hero{
    border:4px solid var(--black);background:var(--black);color:var(--paper);
    padding:30px;box-shadow:14px 14px 0 var(--accent);
    display:grid;grid-template-columns:200px 1fr;gap:30px;align-items:center;
  }
  .hero-avatar{
    width:200px;height:200px;background:var(--accent);
    border:4px solid var(--black);overflow:hidden;
  }
  .hero-avatar img{width:100%;height:100%;object-fit:cover;}
  .hero h1{font-family:'Archivo Black',sans-serif;font-size:64px;line-height:.9;color:var(--accent);text-transform:uppercase;}
  .hero h3{font-size:18px;color:#fff;margin-top:10px;}
  .hero p{font-size:15px;margin-top:10px;color:#ccc;}
  
  .section-header{display:flex;justify-content:space-between;background:var(--black);color:var(--accent);padding:10px 15px;border:3px solid var(--black);margin-top:40px;font-family:'Space Mono',monospace;font-weight:700;text-transform:uppercase;font-size:12px;}
  
  .about-text{font-size:18px;padding:20px 0;}
  
  .grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;}
  .card{border:3px solid var(--black);background:var(--card);padding:20px;box-shadow:8px 8px 0 var(--black);}
  .card h4{font-family:'Archivo Black',sans-serif;margin-bottom:8px;}
  
  .work-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;}
  .project{border:3px solid var(--black);padding:20px;box-shadow:8px 8px 0 var(--black);}
  .project.yellow{background:var(--accent);}
  .project h4{font-family:'Archivo Black',sans-serif;font-size:24px;text-transform:uppercase;margin-bottom:5px;}
  .project p{font-size:14px;margin-top:10px;}
  
  .quote-box{
    border:4px solid var(--black);background:var(--black);color:var(--paper);
    padding:40px;box-shadow:14px 14px 0 var(--accent);margin-top:20px;
  }
  .quote-box h2{font-family:'Archivo Black',sans-serif;font-size:36px;color:#fff;line-height:1.2;}
  .quote-box .hl{background:var(--accent);color:var(--black);padding:0 5px;}
  .quote-box p{color:#ccc;margin-top:15px;}
  .quote-box .attr{color:var(--accent);margin-top:20px;font-weight:700;}
  
  .connect-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;}
  .connect-card{border:3px solid var(--black);padding:20px;text-align:center;text-decoration:none;color:var(--black);font-weight:700;box-shadow:8px 8px 0 var(--black);}
  .connect-card.yellow{background:var(--accent);}
</style>
</head>
<body>
<div class="container">
  
  <div class="hero">
    <div class="hero-avatar">
      <img src="https://z-cdn-media.chatglm.cn/files/3b06aca2-2d2a-410f-9429-310660f36002.png?auth_key=1886908358-3fc867299add4e188649512e720656e8-0-1534c36492bab359bb8395485f1bb671" alt="Tasbir Kabir">
    </div>
    <div>
      <h1>TASBIR KABIR</h1>
      <h3>Entrepreneur | Building AI-native SaaS with Agentic Engineering.</h3>
      <p>I build AI-native software, explore agentic engineering, and turn concepts into systems. SaaS. Automation. Intelligent Infrastructure.</p>
    </div>
  </div>

  <div class="section-header">
    <span>[01] ABOUT</span>
    <span>// IDENTITY</span>
  </div>
  <div class="about-text">
    I build AI-native products—not just demos. I care about agentic engineering, software systems, and long-term value. I experiment across AI, SaaS, and automation to turn concepts into usable software. <br><br>Person first. Builder second. Systems always.
  </div>

  <div class="section-header">
    <span>[02] WHAT I BUILD</span>
    <span>// FOCUS</span>
  </div>
  <div class="grid-3" style="margin-top:20px;">
    <div class="card">
      <h4>AI-Native SaaS</h4>
      Building software with AI at the core, not as an add-on feature.
    </div>
    <div class="card">
      <h4>Agentic Engineering</h4>
      Designing systems where autonomous agents execute complex workflows.
    </div>
    <div class="card">
      <h4>Intelligent Infra</h4>
      Creating the data and automation pipelines that power leverage.
    </div>
  </div>

  <div class="section-header">
    <span>[03] SELECTED WORK</span>
    <span>// PROJECTS</span>
  </div>
  <div class="work-grid" style="margin-top:20px;">
    <div class="project yellow">
      <h4>ATLAS ONE</h4>
      <i>"See What AI Sees."</i>
      <p>AI visibility / discovery intelligence platform.</p>
    </div>
    <div class="project">
      <h4>INTERAKT</h4>
      <p>Description pending.</p>
    </div>
  </div>
  <div class="work-grid" style="grid-template-columns:1fr; margin-top:20px;">
    <div class="project">
      <h4>DAYMARK</h4>
      <p>Description pending.</p>
    </div>
  </div>

  <div class="section-header">
    <span>[04] CURRENTLY</span>
    <span>// NOW</span>
  </div>
  <div class="grid-3" style="margin-top:20px;">
    <div class="card"><h4>BUILDING</h4>AI-native SaaS products and systems.</div>
    <div class="card"><h4>EXPLORING</h4>Agentic engineering and autonomous workflows.</div>
    <div class="card"><h4>THINKING ABOUT</h4>Intelligent infrastructure and long-term system defensibility.</div>
  </div>

  <div class="section-header">
    <span>[05] BUILDER PHILOSOPHY</span>
    <span>// APPROACH</span>
  </div>
  <div class="quote-box">
    <h2>Most build for the demo. I build for the <span class="hl">system</span>.</h2>
    <p>Ship the smallest useful thing that earns the right to exist. Build defensibility through architecture. Prefer substance over feature bloat.</p>
    <div class="attr">— TK</div>
  </div>

  <div class="section-header">
    <span>[06] CONNECT</span>
    <span>// LINKS</span>
  </div>
  <div class="connect-grid" style="margin-top:20px;">
    <a href="https://github.com/tasbirkabir" class="connect-card">GITHUB<br>@tasbirkabir</a>
    <a href="https://www.linkedin.com/in/tasbirrkabir/" class="connect-card yellow">LINKEDIN<br>/in/tasbirrkabir</a>
    <a href="https://x.com/tasbirrkabir" class="connect-card">X / TWITTER<br>@tasbirrkabir</a>
  </div>

</div>
</body>
</html>
