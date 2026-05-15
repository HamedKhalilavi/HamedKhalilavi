
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Space+Grotesk:wght@300;400;500;600&display=swap');
  *{box-sizing:border-box;margin:0;padding:0}
  :root{
    --bg:#0d1117;--bg2:#161b22;--bg3:#21262d;--bg4:#30363d;
    --border:#30363d;--border2:#444c56;
    --text:#e6edf3;--text2:#8b949e;--text3:#6e7681;
    --accent:#58a6ff;--accent2:#1f6feb;--accent3:#388bfd;
    --green:#3fb950;--orange:#d29922;--purple:#bc8cff;--pink:#ff7b72;
    --teal:#39d353;
  }
  body{background:var(--bg);color:var(--text);font-family:'Space Grotesk',sans-serif;line-height:1.6}
  .profile-wrap{max-width:900px;margin:0 auto;padding:2rem 1.5rem}

  /* Header */
  .header{text-align:center;padding:3rem 0 2rem;position:relative}
  .avatar-ring{display:inline-block;padding:3px;background:linear-gradient(135deg,var(--accent2),var(--purple),var(--pink));border-radius:50%;margin-bottom:1.5rem}
  .avatar-inner{width:100px;height:100px;border-radius:50%;background:var(--bg3);display:flex;align-items:center;justify-content:center;font-family:'JetBrains Mono',monospace;font-size:2rem;font-weight:700;color:var(--accent);border:3px solid var(--bg)}
  .name{font-size:2rem;font-weight:600;color:var(--text);letter-spacing:-0.5px}
  .title{font-family:'JetBrains Mono',monospace;font-size:0.85rem;color:var(--text2);margin:0.4rem 0 1.2rem;letter-spacing:0.5px}
  .tagline{font-size:0.95rem;color:var(--text2);font-style:italic;margin-bottom:1.5rem}
  .badges{display:flex;gap:10px;justify-content:center;flex-wrap:wrap}
  .badge{display:inline-flex;align-items:center;gap:6px;padding:6px 14px;border-radius:6px;font-size:0.78rem;font-weight:500;text-decoration:none;border:1px solid var(--border2);transition:border-color 0.2s,color 0.2s}
  .badge:hover{border-color:var(--accent);color:var(--accent)}
  .badge-tg{color:#2CA5E0}
  .badge-li{color:#0A66C2}
  .badge-gm{color:#EA4335}
  .badge i{font-size:14px}

  /* Divider */
  .divider{height:1px;background:var(--border);margin:2rem 0}

  /* Section title */
  .sec-title{font-family:'JetBrains Mono',monospace;font-size:0.75rem;color:var(--text3);letter-spacing:2px;text-transform:uppercase;margin-bottom:1.2rem;display:flex;align-items:center;gap:8px}
  .sec-title::after{content:'';flex:1;height:1px;background:var(--border)}

  /* About */
  .about-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
  .about-item{display:flex;align-items:flex-start;gap:10px;padding:10px 14px;background:var(--bg2);border:1px solid var(--border);border-radius:8px;font-size:0.875rem;color:var(--text2)}
  .about-item .dot{width:6px;height:6px;border-radius:50%;background:var(--accent);margin-top:7px;flex-shrink:0}
  .about-item strong{color:var(--text);font-weight:500}

  /* Skills grid */
  .skills-section{margin-bottom:2rem}
  .skill-category{margin-bottom:1.5rem}
  .cat-header{font-family:'JetBrains Mono',monospace;font-size:0.7rem;color:var(--accent);letter-spacing:1.5px;text-transform:uppercase;margin-bottom:0.7rem;display:flex;align-items:center;gap:8px}
  .cat-header .cat-num{color:var(--text3);font-size:0.65rem}
  .skill-tags{display:flex;flex-wrap:wrap;gap:6px}
  .stag{padding:4px 10px;border-radius:4px;font-size:0.75rem;font-family:'JetBrains Mono',monospace;border:1px solid;transition:opacity 0.2s}
  .stag:hover{opacity:0.8}
  .stag-blue{background:#0d2240;color:#58a6ff;border-color:#1f6feb}
  .stag-purple{background:#1e1540;color:#bc8cff;border-color:#6e40c9}
  .stag-green{background:#0d2818;color:#3fb950;border-color:#2ea043}
  .stag-orange{background:#2b1d09;color:#d29922;border-color:#9e6a03}
  .stag-pink{background:#2b0a12;color:#ff7b72;border-color:#b22c2c}
  .stag-teal{background:#0a2328;color:#39d353;border-color:#196c2e}
  .stag-gray{background:#1c2128;color:#8b949e;border-color:#30363d}

  /* Tech badges row */
  .tech-row{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:1rem}
  .tech-badge{display:inline-flex;align-items:center;gap:5px;padding:3px 10px;border-radius:20px;font-size:0.72rem;font-weight:500;border:1px solid var(--border);background:var(--bg3);color:var(--text2)}

  /* Stats */
  .stats-grid{display:grid;grid-template-columns:1fr 1fr 1fr;gap:12px;margin-bottom:2rem}
  .stat-card{background:var(--bg2);border:1px solid var(--border);border-radius:10px;padding:1rem;text-align:center}
  .stat-card img{width:100%;height:auto;border-radius:4px;filter:invert(0)}
  .stat-img{border-radius:6px;border:1px solid var(--border2)}

  /* Projects */
  .projects-table{width:100%;border-collapse:collapse;font-size:0.85rem}
  .projects-table th{font-family:'JetBrains Mono',monospace;font-size:0.65rem;letter-spacing:1.5px;text-transform:uppercase;color:var(--text3);padding:8px 12px;border-bottom:1px solid var(--border);text-align:left}
  .projects-table td{padding:10px 12px;border-bottom:1px solid var(--border);color:var(--text2)}
  .projects-table td:first-child{color:var(--text);font-weight:500}
  .projects-table tr:last-child td{border-bottom:none}
  .projects-table tr:hover td{background:var(--bg2)}
  .stack-chip{display:inline;font-family:'JetBrains Mono',monospace;font-size:0.7rem;color:var(--accent);margin-right:4px}

  /* Trophy section */
  .trophy-wrap{text-align:center;margin:1rem 0}
  .trophy-wrap img{max-width:100%;border-radius:8px}

  /* Footer */
  .footer{text-align:center;padding:2rem 0 1rem;font-family:'JetBrains Mono',monospace;font-size:0.72rem;color:var(--text3);letter-spacing:1px}

  /* Responsive */
  @media(max-width:600px){
    .about-grid{grid-template-columns:1fr}
    .stats-grid{grid-template-columns:1fr}
  }
</style>

<div class="profile-wrap">

  <div class="header">
    <div class="avatar-ring">
      <div class="avatar-inner">HK</div>
    </div>
    <h1 class="name">Hamed Khalilavi</h1>
    <p class="title">ML/DL Engineer · Data Scientist · Python Developer</p>
    <p class="tagline">Turning data into decisions — one model at a time.</p>
    <div class="badges">
      <a class="badge badge-tg" href="https://t.me/Hamed_Khalilavi" target="_blank"><i class="ti ti-brand-telegram"></i> Telegram</a>
      <a class="badge badge-li" href="http://linkedin.com/in/hamedkhalilavi/" target="_blank"><i class="ti ti-brand-linkedin"></i> LinkedIn</a>
      <a class="badge badge-gm" href="mailto:h.khalilavi.pro@gmail.com"><i class="ti ti-mail"></i> Gmail</a>
    </div>
  </div>

  <div class="divider"></div>

  <p class="sec-title">About me</p>
  <div class="about-grid" style="margin-bottom:2rem">
    <div class="about-item"><span class="dot"></span><span><strong>Deep Learning</strong> — neural networks & model architectures</span></div>
    <div class="about-item"><span class="dot"></span><span><strong>NLP & LLMs</strong> — large language model applications</span></div>
    <div class="about-item"><span class="dot"></span><span><strong>MLOps</strong> — bringing models to production at scale</span></div>
    <div class="about-item"><span class="dot"></span><span><strong>Data Engineering</strong> — pipelines, ETL, and infrastructure</span></div>
    <div class="about-item"><span class="dot"></span><span><strong>Agentic Systems</strong> — multi-modal autonomous workflows</span></div>
    <div class="about-item"><span class="dot"></span><span><strong>Always learning</strong> — curious, building, shipping</span></div>
  </div>

  <div class="divider"></div>
  <p class="sec-title">Skill domains</p>

  <div class="skills-section">

    <div class="skill-category">
      <div class="cat-header"><span class="cat-num">01</span> Core AI & Research</div>
      <div class="skill-tags">
        <span class="stag stag-purple">Machine Learning</span>
        <span class="stag stag-purple">Deep Learning</span>
        <span class="stag stag-purple">Computer Vision</span>
        <span class="stag stag-purple">NLP</span>
        <span class="stag stag-purple">Model Fine-tuning</span>
        <span class="stag stag-purple">Quantization</span>
        <span class="stag stag-purple">Multi-modal Systems</span>
        <span class="stag stag-purple">Agentic Workflows</span>
      </div>
    </div>

    <div class="skill-category">
      <div class="cat-header"><span class="cat-num">02</span> Low-Code AI & Automation</div>
      <div class="skill-tags">
        <span class="stag stag-blue">Dify</span>
        <span class="stag stag-blue">Flowise</span>
        <span class="stag stag-blue">n8n</span>
        <span class="stag stag-blue">Make</span>
        <span class="stag stag-blue">Custom Nodes</span>
        <span class="stag stag-blue">RAG-as-a-Service</span>
        <span class="stag stag-blue">LLM-native Apps</span>
        <span class="stag stag-blue">Chain Management</span>
      </div>
    </div>

    <div class="skill-category">
      <div class="cat-header"><span class="cat-num">03</span> Audio & Speech</div>
      <div class="skill-tags">
        <span class="stag stag-teal">STT / TTS</span>
        <span class="stag stag-teal">Voice Cloning</span>
        <span class="stag stag-teal">DSP</span>
        <span class="stag stag-teal">Audio Intelligence</span>
        <span class="stag stag-teal">Emotion Recognition</span>
        <span class="stag stag-teal">Source Separation</span>
      </div>
    </div>

    <div class="skill-category">
      <div class="cat-header"><span class="cat-num">04</span> Development & LLM Integration</div>
      <div class="skill-tags">
        <span class="stag stag-green">RAG Systems</span>
        <span class="stag stag-green">Function Calling</span>
        <span class="stag stag-green">FastAPI</span>
        <span class="stag stag-green">PyDantic</span>
        <span class="stag stag-green">Telegram Bots</span>
        <span class="stag stag-green">Prompt Engineering</span>
        <span class="stag stag-green">Ragas</span>
        <span class="stag stag-green">LangSmith</span>
        <span class="stag stag-green">Agentic Systems</span>
      </div>
    </div>

    <div class="skill-category">
      <div class="cat-header"><span class="cat-num">05</span> Infrastructure & MLOps</div>
      <div class="skill-tags">
        <span class="stag stag-orange">Triton</span>
        <span class="stag stag-orange">BentoML</span>
        <span class="stag stag-orange">KServe</span>
        <span class="stag stag-orange">Model Monitoring</span>
        <span class="stag stag-orange">Drift Detection</span>
        <span class="stag stag-orange">Qdrant</span>
        <span class="stag stag-orange">Milvus</span>
        <span class="stag stag-orange">FAISS</span>
        <span class="stag stag-orange">Airflow</span>
        <span class="stag stag-orange">Dagster</span>
      </div>
    </div>

    <div class="skill-category">
      <div class="cat-header"><span class="cat-num">06</span> AI Products & Business Solutions</div>
      <div class="skill-tags">
        <span class="stag stag-pink">AI Trading Systems</span>
        <span class="stag stag-pink">SignalFlow</span>
        <span class="stag stag-pink">Document AI</span>
        <span class="stag stag-pink">OCR Systems</span>
        <span class="stag stag-pink">BPA</span>
        <span class="stag stag-pink">Custom AI Installers</span>
        <span class="stag stag-pink">Offline AI Packages</span>
      </div>
    </div>

    <div class="skill-category">
      <div class="cat-header"><span class="cat-num">07</span> Security, Privacy & Tools</div>
      <div class="skill-tags">
        <span class="stag stag-gray">AI Security</span>
        <span class="stag stag-gray">Guardrails</span>
        <span class="stag stag-gray">Prompt Injection Defense</span>
        <span class="stag stag-gray">Docker</span>
        <span class="stag stag-gray">Kubernetes</span>
        <span class="stag stag-gray">CI/CD</span>
        <span class="stag stag-gray">Streamlit</span>
        <span class="stag stag-gray">Gradio</span>
      </div>
    </div>

  </div>

  <div class="divider"></div>
  <p class="sec-title">Tech stack</p>

  <div style="margin-bottom:0.5rem;font-family:'JetBrains Mono',monospace;font-size:0.68rem;color:var(--text3);letter-spacing:1px">LANGUAGES</div>
  <div class="tech-row">
    <span class="tech-badge">🐍 Python</span>
    <span class="tech-badge">🗄️ SQL</span>
    <span class="tech-badge">🐚 Bash</span>
  </div>

  <div style="margin-bottom:0.5rem;font-family:'JetBrains Mono',monospace;font-size:0.68rem;color:var(--text3);letter-spacing:1px">ML / DL FRAMEWORKS</div>
  <div class="tech-row">
    <span class="tech-badge">🔥 PyTorch</span>
    <span class="tech-badge">🟡 TensorFlow</span>
    <span class="tech-badge">🔴 Keras</span>
    <span class="tech-badge">🟠 scikit-learn</span>
    <span class="tech-badge">🤗 Hugging Face</span>
    <span class="tech-badge">🦜 LangChain</span>
  </div>

  <div style="margin-bottom:0.5rem;font-family:'JetBrains Mono',monospace;font-size:0.68rem;color:var(--text3);letter-spacing:1px">DATA & ENGINEERING</div>
  <div class="tech-row">
    <span class="tech-badge">🐼 Pandas</span>
    <span class="tech-badge">🔢 NumPy</span>
    <span class="tech-badge">✦ Apache Spark</span>
    <span class="tech-badge">🌬️ Airflow</span>
  </div>

  <div style="margin-bottom:0.5rem;font-family:'JetBrains Mono',monospace;font-size:0.68rem;color:var(--text3);letter-spacing:1px">MLOPS & TOOLS</div>
  <div class="tech-row">
    <span class="tech-badge">🐳 Docker</span>
    <span class="tech-badge">📈 MLflow</span>
    <span class="tech-badge">🪄 W&B</span>
    <span class="tech-badge">🔀 Git</span>
    <span class="tech-badge">🐧 Linux</span>
  </div>

  <div class="divider"></div>
  <p class="sec-title">GitHub stats</p>

  <div class="stats-grid">
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api?username=hamedkhalilavi&show_icons=true&theme=github_dark&hide_border=true&count_private=true&bg_color=161b22&title_color=58a6ff&text_color=8b949e&icon_color=3fb950" alt="GitHub Stats" class="stat-img" />
    </div>
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=hamedkhalilavi&layout=compact&theme=github_dark&hide_border=true&bg_color=161b22&title_color=58a6ff&text_color=8b949e" alt="Top Languages" class="stat-img" />
    </div>
    <div class="stat-card">
      <img src="https://streak-stats.demolab.com?user=hamedkhalilavi&theme=github-dark-blue&hide_border=true&background=161b22&stroke=30363d&ring=58a6ff&fire=d29922&currStreakLabel=58a6ff" alt="GitHub Streak" class="stat-img" />
    </div>
  </div>

  <div class="divider"></div>
  <p class="sec-title">Notable projects</p>

  <table class="projects-table" style="margin-bottom:2rem">
    <thead>
      <tr>
        <th>Project</th>
        <th>Description</th>
        <th>Stack</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>🔬 Coming soon</td>
        <td>Deep learning research project</td>
        <td><span class="stack-chip">PyTorch</span><span class="stack-chip">Python</span></td>
      </tr>
      <tr>
        <td>📊 Coming soon</td>
        <td>End-to-end data pipeline</td>
        <td><span class="stack-chip">Airflow</span><span class="stack-chip">Spark</span><span class="stack-chip">SQL</span></td>
      </tr>
      <tr>
        <td>🤖 Coming soon</td>
        <td>LLM-powered application</td>
        <td><span class="stack-chip">LangChain</span><span class="stack-chip">Hugging Face</span></td>
      </tr>
      <tr>
        <td>📈 SignalFlow</td>
        <td>AI-powered trading system for financial market analysis</td>
        <td><span class="stack-chip">Python</span><span class="stack-chip">ML</span><span class="stack-chip">FastAPI</span></td>
      </tr>
    </tbody>
  </table>

  <div class="divider"></div>
  <p class="sec-title">GitHub trophies</p>

  <div class="trophy-wrap">
    <img src="https://github-profile-trophy.vercel.app/?username=hamedkhalilavi&theme=darkhub&no-frame=true&column=6&margin-w=4" alt="GitHub Trophies" />
  </div>

  <div class="divider"></div>

  <div class="footer">
    // open to collaborations · research · interesting problems
  </div>

</div>
