

<style>
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600&family=Space+Grotesk:wght@400;500;600&display=swap');

* { box-sizing: border-box; margin: 0; padding: 0; }

.profile-root {
  font-family: 'Space Grotesk', sans-serif;
  color: var(--color-text-primary);
  padding: 2rem 1.5rem;
  max-width: 680px;
}

.scanline {
  position: relative;
  overflow: hidden;
}

.header {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  margin-bottom: 2rem;
  padding-bottom: 1.5rem;
  border-bottom: 0.5px solid var(--color-border-tertiary);
}

.avatar {
  width: 72px;
  height: 72px;
  border-radius: 50%;
  background: linear-gradient(135deg, #1D9E75, #378ADD);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 22px;
  font-weight: 600;
  color: white;
  flex-shrink: 0;
}

.header-text h1 {
  font-size: 20px;
  font-weight: 600;
  letter-spacing: -0.3px;
  color: var(--color-text-primary);
}

.header-text p {
  font-size: 13px;
  color: var(--color-text-secondary);
  margin-top: 4px;
  font-family: 'IBM Plex Mono', monospace;
}

.tag-row {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
  margin-top: 10px;
}

.tag {
  font-size: 11px;
  font-family: 'IBM Plex Mono', monospace;
  padding: 3px 10px;
  border-radius: 100px;
  border: 0.5px solid var(--color-border-tertiary);
  color: var(--color-text-secondary);
  background: var(--color-background-secondary);
}

.tag.green {
  background: #E1F5EE;
  color: #0F6E56;
  border-color: #5DCAA5;
}

.tag.blue {
  background: #E6F1FB;
  color: #185FA5;
  border-color: #85B7EB;
}

.section-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--color-text-tertiary);
  margin-bottom: 12px;
}

.section {
  margin-bottom: 1.75rem;
}

.info-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 8px;
}

.info-card {
  background: var(--color-background-secondary);
  border-radius: var(--border-radius-md);
  padding: 12px 14px;
  display: flex;
  align-items: flex-start;
  gap: 10px;
}

.info-icon {
  width: 28px;
  height: 28px;
  border-radius: 6px;
  background: var(--color-background-primary);
  border: 0.5px solid var(--color-border-tertiary);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  font-size: 13px;
}

.info-text label {
  display: block;
  font-size: 10px;
  color: var(--color-text-tertiary);
  font-family: 'IBM Plex Mono', monospace;
  text-transform: uppercase;
  letter-spacing: 0.8px;
  margin-bottom: 2px;
}

.info-text span {
  font-size: 13px;
  font-weight: 500;
  color: var(--color-text-primary);
}

.info-text a {
  font-size: 13px;
  font-weight: 500;
  color: #185FA5;
  text-decoration: none;
}

.profiles-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 8px;
}

.profile-card {
  border: 0.5px solid var(--color-border-tertiary);
  border-radius: var(--border-radius-md);
  padding: 12px 14px;
  background: var(--color-background-primary);
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  transition: background 0.15s;
  cursor: pointer;
}

.profile-card:hover {
  background: var(--color-background-secondary);
}

.platform-dot {
  width: 32px;
  height: 32px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 14px;
  font-weight: 700;
  flex-shrink: 0;
  font-family: 'IBM Plex Mono', monospace;
}

.dot-pico { background: #E6F1FB; color: #185FA5; }
.dot-thm  { background: #FCEBEB; color: #A32D2D; }
.dot-lc   { background: #FAEEDA; color: #854F0B; }
.dot-cf   { background: #E6F1FB; color: #185FA5; }

.profile-info label {
  display: block;
  font-size: 10px;
  color: var(--color-text-tertiary);
  font-family: 'IBM Plex Mono', monospace;
  text-transform: uppercase;
  letter-spacing: 0.8px;
  margin-bottom: 1px;
}

.profile-info span {
  font-size: 13px;
  font-weight: 500;
  color: var(--color-text-primary);
}

.tools-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(0, 1fr));
  gap: 6px;
}

.tool-pill {
  background: var(--color-background-secondary);
  border: 0.5px solid var(--color-border-tertiary);
  border-radius: 100px;
  padding: 5px 12px;
  font-size: 12px;
  font-family: 'IBM Plex Mono', monospace;
  color: var(--color-text-secondary);
  text-align: center;
  white-space: nowrap;
}

.tool-pill.highlight {
  background: #E1F5EE;
  color: #0F6E56;
  border-color: #5DCAA5;
}

.footer-bar {
  border-top: 0.5px solid var(--color-border-tertiary);
  padding-top: 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.footer-bar span {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 11px;
  color: var(--color-text-tertiary);
}

.status-dot {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 11px;
  color: #0F6E56;
}

.status-dot::before {
  content: '';
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: #1D9E75;
  display: inline-block;
  animation: pulse 2s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.4; }
}
</style>

<div class="profile-root">
  <div class="header">
    <div class="avatar">RA</div>
    <div class="header-text">
      <h1>Raghupathi.A</h1>
      <p>timelessdebugger</p>
      <div class="tag-row">
        <span class="tag green">Cybersecurity</span>
        <span class="tag blue">CTF Player</span>
        <span class="tag">Full-Stack Dev</span>
        <span class="tag">India 🇮🇳</span>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">Currently learning</div>
    <div class="info-grid">
      <div class="info-card">
        <div class="info-icon">🐧</div>
        <div class="info-text">
          <label>OS</label>
          <span>Linux</span>
        </div>
      </div>
      <div class="info-card">
        <div class="info-icon">🔐</div>
        <div class="info-text">
          <label>Focus</label>
          <span>Web Security</span>
        </div>
      </div>
      <div class="info-card">
        <div class="info-icon">⚡</div>
        <div class="info-text">
          <label>Stack</label>
          <span>Full-Stack Dev</span>
        </div>
      </div>
      <div class="info-card">
        <div class="info-icon">📫</div>
        <div class="info-text">
          <label>Contact</label>
          <a href="mailto:timelessdebugger@duck.com">@duck.com</a>
        </div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">CTF & Coding profiles</div>
    <div class="profiles-grid">
      <a class="profile-card" href="https://play.picoctf.org/users/TimelessDebugger" target="_blank">
        <div class="platform-dot dot-pico">Pi</div>
        <div class="profile-info">
          <label>PicoCTF</label>
          <span>TimelessDebugger</span>
        </div>
      </a>
      <a class="profile-card" href="https://tryhackme.com/p/TimelessDebugger" target="_blank">
        <div class="platform-dot dot-thm">TH</div>
        <div class="profile-info">
          <label>TryHackMe</label>
          <span>TimelessDebugger</span>
        </div>
      </a>
      <a class="profile-card" href="https://leetcode.com/u/raghupathi_321/" target="_blank">
        <div class="platform-dot dot-lc">LC</div>
        <div class="profile-info">
          <label>LeetCode</label>
          <span>raghupathi_321</span>
        </div>
      </a>
      <a class="profile-card" href="https://codeforces.com/profile/TimelessDebugger" target="_blank">
        <div class="platform-dot dot-cf">CF</div>
        <div class="profile-info">
          <label>Codeforces</label>
          <span>TimelessDebugger</span>
        </div>
      </a>
    </div>
  </div>

  <div class="section">
    <div class="section-label">Languages & tools</div>
    <div style="display: flex; flex-wrap: wrap; gap: 6px;">
      <span class="tool-pill highlight">Python</span>
      <span class="tool-pill highlight">Linux</span>
      <span class="tool-pill highlight">JavaScript</span>
      <span class="tool-pill">C</span>
      <span class="tool-pill">Java</span>
      <span class="tool-pill">PHP</span>
      <span class="tool-pill">MySQL</span>
      <span class="tool-pill">HTML5</span>
      <span class="tool-pill">CSS3</span>
      <span class="tool-pill">Vue.js</span>
      <span class="tool-pill">Bootstrap</span>
      <span class="tool-pill">Git</span>
      <span class="tool-pill">GCP</span>
      <span class="tool-pill">Arduino</span>
    </div>
  </div>

  <div class="footer-bar">
    <span class="status-dot">open to opportunities</span>
    <a href="https://timelessdebugger.netlify.app/" target="_blank" style="font-family: 'IBM Plex Mono', monospace; font-size: 11px; color: #185FA5; text-decoration: none;">timelessdebugger.netlify.app ↗</a>
  </div>
</div>
