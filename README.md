<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mohammad · Crimson Dev</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&display=swap" rel="stylesheet" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0e0a0b;
      background-image: radial-gradient(circle at 20% 30%, #1f0f12 0%, #0b0708 100%);
      font-family: 'JetBrains Mono', monospace;
      color: #f0e6e7;
      padding: 2rem 1rem;
      min-height: 100vh;
      display: flex;
      justify-content: center;
    }

    .card {
      max-width: 1100px;
      width: 100%;
      background: rgba(18, 10, 12, 0.75);
      backdrop-filter: blur(6px);
      -webkit-backdrop-filter: blur(6px);
      border: 1px solid rgba(255, 60, 60, 0.2);
      border-radius: 2.5rem;
      padding: 2.5rem 2.2rem;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.8), 0 0 0 1px rgba(220, 40, 40, 0.15);
    }

    h1, h2, h3 {
      font-weight: 600;
      letter-spacing: -0.02em;
    }

    .accent-red {
      color: #ff3b3b;
    }
    .accent-glow {
      text-shadow: 0 0 12px rgba(255, 40, 40, 0.5);
    }
    .badge-red {
      background: #ff1a1a20;
      border: 1px solid #ff3b3b60;
      color: #ff7a7a;
      padding: 0.2rem 0.9rem;
      border-radius: 40px;
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 0.3px;
      display: inline-block;
    }

    .profile-header {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 2rem;
    }

    .profile-left {
      display: flex;
      align-items: center;
      gap: 1rem;
    }

    .avatar {
      font-size: 3.2rem;
      background: #1f0d0f;
      width: 70px;
      height: 70px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 50%;
      border: 2px solid #ff4d4d;
      box-shadow: 0 0 30px #ff2a2a30;
      color: #ff5e5e;
    }

    .title h1 {
      font-size: 2.2rem;
      color: #fff0f0;
    }
    .title h1 span {
      color: #ff4d4d;
    }
    .title .sub {
      color: #c0a0a0;
      font-size: 0.9rem;
      letter-spacing: 0.5px;
    }
    .title .sub i {
      color: #ff5e5e;
      margin: 0 4px;
    }

    .views {
      background: #1f1012;
      padding: 0.45rem 1.2rem;
      border-radius: 60px;
      border: 1px solid #ff3b3b40;
      font-size: 0.8rem;
      color: #dbbbbb;
      white-space: nowrap;
    }
    .views i {
      color: #ff5e5e;
      margin-right: 6px;
    }

    .typing-line {
      background: #1f1012;
      border-left: 3px solid #ff3b3b;
      padding: 0.7rem 1.2rem;
      border-radius: 40px;
      margin: 1.2rem 0 2.2rem 0;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 0.3rem 0.8rem;
      font-size: 1rem;
      color: #f0d0d0;
    }
    .typing-line i {
      color: #ff5e5e;
      margin-right: 6px;
    }
    .typing-line .highlight {
      color: #ff7a7a;
      font-weight: 600;
    }

    .section-title {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      font-size: 1.3rem;
      font-weight: 600;
      color: #ffdede;
      margin: 2.2rem 0 1.2rem 0;
      border-bottom: 1px solid #ff3b3b30;
      padding-bottom: 0.4rem;
    }
    .section-title i {
      color: #ff4d4d;
      font-size: 1.3rem;
    }

    .skills-wrapper {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem 1.2rem;
      background: #130b0c;
      padding: 1.2rem 1.5rem;
      border-radius: 60px;
      border: 1px solid #ff3b3b20;
      margin-bottom: 0.5rem;
    }
    .skill-item {
      display: flex;
      align-items: center;
      gap: 6px;
      background: #1f1113;
      padding: 0.25rem 1rem 0.25rem 0.8rem;
      border-radius: 40px;
      border: 1px solid #ff3b3b30;
      font-size: 0.85rem;
      color: #f0dada;
    }
    .skill-item i {
      font-size: 1.1rem;
      color: #ff5e5e;
      width: 20px;
      text-align: center;
    }

    .plugin-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 1.2rem;
      margin-top: 0.4rem;
    }
    .plugin-card {
      background: #140c0d;
      border-radius: 24px;
      padding: 1.2rem 1.2rem 1rem 1.2rem;
      border: 1px solid #ff3b3b20;
      transition: all 0.2s ease;
      box-shadow: 0 6px 12px rgba(0,0,0,0.4);
    }
    .plugin-card:hover {
      border-color: #ff5e5e70;
      background: #1c0f11;
      transform: translateY(-3px);
    }
    .plugin-name {
      font-weight: 600;
      font-size: 1.2rem;
      color: #ffd0d0;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .plugin-name i {
      color: #ff4d4d;
      font-size: 1.1rem;
    }
    .plugin-desc {
      font-size: 0.8rem;
      color: #b69393;
      margin: 0.4rem 0 0.2rem 0;
      line-height: 1.4;
    }
    .plugin-meta {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 0.6rem;
      font-size: 0.7rem;
      color: #9f7a7a;
    }
    .plugin-meta .version {
      background: #1f0f12;
      padding: 0.1rem 0.7rem;
      border-radius: 40px;
      border: 1px solid #ff3b3b30;
      color: #ffa0a0;
    }

    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem;
      margin: 1.5rem 0 0.2rem 0;
    }
    .stat-box {
      flex: 1 1 180px;
      background: #130b0c;
      border-radius: 28px;
      padding: 0.9rem 1.2rem;
      border: 1px solid #ff3b3b20;
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }
    .stat-box i {
      font-size: 1.4rem;
      color: #ff4d4d;
      width: 30px;
      text-align: center;
    }
    .stat-box .stat-info {
      display: flex;
      flex-direction: column;
    }
    .stat-box .stat-number {
      font-weight: 700;
      font-size: 1.2rem;
      color: #ffe0e0;
    }
    .stat-box .stat-label {
      font-size: 0.6rem;
      color: #a07a7a;
      letter-spacing: 0.3px;
    }

    .tools-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem 2rem;
      background: #130b0c;
      padding: 0.9rem 1.6rem;
      border-radius: 60px;
      border: 1px solid #ff3b3b20;
      margin: 0.5rem 0 0.2rem 0;
    }
    .tools-row span {
      display: flex;
      align-items: center;
      gap: 6px;
      color: #ddc0c0;
      font-size: 0.8rem;
    }
    .tools-row i {
      color: #ff5e5e;
      font-size: 1.1rem;
      width: 24px;
      text-align: center;
    }

    .contact-row {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem 2rem;
      margin: 2.8rem 0 0.8rem 0;
    }
    .contact-btn {
      background: #1f0f12;
      border: 1px solid #ff3b3b50;
      padding: 0.5rem 1.8rem;
      border-radius: 60px;
      color: #f0dada;
      text-decoration: none;
      font-weight: 500;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      transition: 0.2s;
      font-size: 0.9rem;
    }
    .contact-btn i {
      color: #ff4d4d;
      font-size: 1.1rem;
    }
    .contact-btn:hover {
      background: #2c1418;
      border-color: #ff6a6a;
      color: #fff5f5;
      box-shadow: 0 0 20px #ff2a2a30;
    }

    .footer-snake {
      margin-top: 2.8rem;
      text-align: center;
      font-size: 0.7rem;
      color: #764a4a;
      letter-spacing: 1px;
      border-top: 1px solid #ff3b3b20;
      padding-top: 1.2rem;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 0.3rem 1.5rem;
    }
    .footer-snake i {
      color: #ff5e5e;
      margin: 0 4px;
    }

    @media (max-width: 600px) {
      .card { padding: 1.5rem 1rem; }
      .profile-left { flex-wrap: wrap; }
      .title h1 { font-size: 1.7rem; }
      .skills-wrapper { border-radius: 30px; padding: 0.8rem 1rem; }
      .tools-row { border-radius: 30px; }
    }
  </style>
</head>
<body>
  <div class="card">

    <div class="profile-header">
      <div class="profile-left">
        <div class="avatar">
          <i class="fas fa-code"></i>
        </div>
        <div class="title">
          <h1>Mohammad <span>·</span> <span style="color:#ff5e5e;">cblock</span></h1>
          <div class="sub">
            <i class="fas fa-cube"></i> Minecraft · Dev <i class="fas fa-circle" style="font-size: 0.35rem; vertical-align: middle; margin:0 8px;"></i> 18 y/o
          </div>
        </div>
      </div>
      <div class="views">
        <i class="fas fa-eye"></i> profile views · 1.2k
      </div>
    </div>

    <div class="typing-line">
      <i class="fas fa-terminal"></i>
      <span><span class="highlight">Minecraft</span> Plugin Developer · <span class="highlight">Server</span> Dev · <span class="highlight">Discord</span> Bot Dev · Java · always building</span>
      <span style="margin-left: auto; color:#ff5e5e;"><i class="fas fa-bolt"></i> v1.4</span>
    </div>

    <div class="section-title">
      <i class="fas fa-microchip"></i> Tech Stack
    </div>
    <div class="skills-wrapper">
      <span class="skill-item"><i class="fab fa-java"></i> Java</span>
      <span class="skill-item"><i class="fas fa-code-branch"></i> Git</span>
      <span class="skill-item"><i class="fas fa-brain"></i> IntelliJ</span>
      <span class="skill-item"><i class="fas fa-database"></i> MariaDB</span>
      <span class="skill-item"><i class="fas fa-database"></i> MySQL</span>
      <span class="skill-item"><i class="fas fa-code"></i> VS Code</span>
      <span class="skill-item"><i class="fas fa-server"></i> Redis</span>
      <span class="skill-item"><i class="fab fa-linux"></i> Linux</span>
      <span class="skill-item"><i class="fab fa-react"></i> React</span>
      <span class="skill-item"><i class="fab fa-js"></i> JavaScript</span>
      <span class="skill-item"><i class="fab fa-php"></i> PHP</span>
    </div>

    <div class="section-title">
      <i class="fas fa-cubes"></i> Minecraft Plugins
    </div>

    <div class="plugin-grid">

      <div class="plugin-card">
        <div class="plugin-name">
          QueryPlus <i class="fas fa-plug"></i>
        </div>
        <div class="plugin-desc">Simple Rest API query for your minecraft network.</div>
        <div class="plugin-meta">
          <span><i class="fas fa-tag"></i> v1.2.0</span>
          <span class="version"><i class="fas fa-check-circle"></i> stable</span>
        </div>
      </div>

      <div class="plugin-card">
        <div class="plugin-name">
          CTElevator <i class="fas fa-arrow-up"></i>
        </div>
        <div class="plugin-desc">Simple Elevator plugin for your minecraft server.</div>
        <div class="plugin-meta">
          <span><i class="fas fa-tag"></i> v1.0</span>
          <span class="version"><i class="fas fa-check-circle"></i> stable</span>
        </div>
      </div>

      <div class="plugin-card">
        <div class="plugin-name">
          VelocityCustomCommand <i class="fas fa-terminal"></i>
        </div>
        <div class="plugin-desc">Make infinite custom command for your velocity proxy.</div>
        <div class="plugin-meta">
          <span><i class="fas fa-tag"></i> v1.1</span>
          <span class="version"><i class="fas fa-check-circle"></i> stable</span>
        </div>
      </div>

      <div class="plugin-card">
        <div class="plugin-name">
          Better Donator <i class="fas fa-crown"></i>
        </div>
        <div class="plugin-desc">Fully customize donators chat system on BungeeCord.</div>
        <div class="plugin-meta">
          <span><i class="fas fa-tag"></i> v1.4.0</span>
          <span class="version"><i class="fas fa-check-circle"></i> stable</span>
        </div>
      </div>

      <div class="plugin-card">
        <div class="plugin-name">
          Sky Alerts <i class="fas fa-bell"></i>
        </div>
        <div class="plugin-desc">Simple & fully customizable alert system for velocity.</div>
        <div class="plugin-meta">
          <span><i class="fas fa-tag"></i> v1.0</span>
          <span class="version"><i class="fas fa-check-circle"></i> stable</span>
        </div>
      </div>

      <div class="plugin-card">
        <div class="plugin-name">
          Join Accounts <i class="fas fa-user-plus"></i>
        </div>
        <div class="plugin-desc">Open a WebPanel whitelisting system for your server.</div>
        <div class="plugin-meta">
          <span><i class="fas fa-tag"></i> v1.0.0</span>
          <span class="version"><i class="fas fa-check-circle"></i> stable</span>
        </div>
      </div>

      <div class="plugin-card">
        <div class="plugin-name">
          CCommands <i class="fas fa-command"></i>
        </div>
        <div class="plugin-desc">Make any command easily on bukkit servers.</div>
        <div class="plugin-meta">
          <span><i class="fas fa-tag"></i> v1.0.1</span>
          <span class="version"><i class="fas fa-check-circle"></i> stable</span>
        </div>
      </div>
    </div>

    <div class="section-title" style="margin-top: 2.8rem;">
      <i class="fas fa-chart-simple"></i> GitHub Pulse
    </div>
    <div class="stats-row">
      <div class="stat-box">
        <i class="fas fa-code-fork"></i>
        <div class="stat-info">
          <span class="stat-number">42</span>
          <span class="stat-label">repositories</span>
        </div>
      </div>
      <div class="stat-box">
        <i class="fas fa-star"></i>
        <div class="stat-info">
          <span class="stat-number">189</span>
          <span class="stat-label">stars earned</span>
        </div>
      </div>
      <div class="stat-box">
        <i class="fas fa-commit"></i>
        <div class="stat-info">
          <span class="stat-number">1.3k</span>
          <span class="stat-label">commits</span>
        </div>
      </div>
      <div class="stat-box">
        <i class="fas fa-fire"></i>
        <div class="stat-info">
          <span class="stat-number">7</span>
          <span class="stat-label">streak days</span>
        </div>
      </div>
    </div>

    <div class="section-title" style="margin-top: 2rem;">
      <i class="fas fa-toolbox"></i> Tools & Environment
    </div>
    <div class="tools-row">
      <span><i class="fab fa-java"></i> Java 17+</span>
      <span><i class="fab fa-git-alt"></i> Git</span>
      <span><i class="fas fa-cube"></i> IntelliJ</span>
      <span><i class="fas fa-database"></i> MariaDB</span>
      <span><i class="fas fa-database"></i> MySQL</span>
      <span><i class="fas fa-code"></i> VS Code</span>
      <span><i class="fas fa-server"></i> Redis</span>
      <span><i class="fab fa-linux"></i> Linux</span>
      <span><i class="fab fa-react"></i> React</span>
      <span><i class="fab fa-js"></i> JS</span>
      <span><i class="fab fa-php"></i> PHP</span>
    </div>

    <div class="contact-row">
      <a href="#" class="contact-btn"><i class="fab fa-github"></i> master-cblock</a>
      <a href="#" class="contact-btn"><i class="fab fa-discord"></i> cblock#1337</a>
      <a href="#" class="contact-btn"><i class="fas fa-envelope"></i> mohammad@dev</a>
    </div>

    <div class="footer-snake">
      <span><i class="fas fa-cube"></i> Code. Create. Play.</span>
      <span><i class="fas fa-circle" style="color:#ff3b3b;"></i> crimson themed</span>
      <span><i class="fas fa-snake"></i> 2026 · Mohammad</span>
      <span style="color:#5a3a3a;">⚡ always building</span>
    </div>

  </div>
</body>
</html>
