 :root {
  --bg: #f4f8f2;
  --panel: #ffffff;
  --panel-soft: #eef5ee;
  --primary: #1d7a4d;
  --primary-dark: #145a3a;
  --primary-soft: #dff4e7;
  --accent: #f8b84e;
  --danger: #d95555;
  --text: #102018;
  --muted: #66776d;
  --border: #dfeae2;
  --shadow: 0 18px 50px rgba(16, 32, 24, 0.08);
}

* {
  box-sizing: border-box;
}

html, body, #root {
  margin: 0;
  min-height: 100%;
  font-family: Inter, 'Segoe UI', sans-serif;
  background: linear-gradient(180deg, #eef7ef 0%, #f7faf6 100%);
  color: var(--text);
}

button {
  font: inherit;
}

.app-shell {
  max-width: 1440px;
  margin: 32px auto;
  min-height: calc(100vh - 64px);
  display: grid;
  grid-template-columns: 260px 1fr;
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(8px);
  border: 1px solid rgba(255, 255, 255, 0.5);
  border-radius: 28px;
  box-shadow: var(--shadow);
  overflow: hidden;
}

.sidebar {
  background: linear-gradient(180deg, #143d2a 0%, #0d2a1d 100%);
  color: #fff;
  padding: 26px 22px;
}

.brand-block {
  display: flex;
  align-items: center;
  gap: 14px;
  margin-bottom: 26px;
}

.logo {
  width: 42px;
  height: 42px;
  border-radius: 14px;
  display: grid;
  place-items: center;
  font-size: 1.3rem;
  font-weight: 700;
  background: linear-gradient(135deg, #76d9a6 0%, #31a46e 100%);
  color: #092c1d;
}

.brand-block h1 {
  margin: 0;
  font-size: 1.5rem;
}

.eyebrow {
  margin: 0 0 6px;
  font-size: 0.72rem;
  text-transform: uppercase;
  letter-spacing: 0.14em;
  color: #9dc9ae;
}

.eyebrow.muted {
  color: var(--muted);
  letter-spacing: 0.1em;
}

.nav {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-top: 18px;
}

.nav-item {
  width: 100%;
  background: transparent;
  border: 1px solid rgba(255, 255, 255, 0.08);
  color: rgba(255, 255, 255, 0.78);
  border-radius: 12px;
  padding: 12px 14px;
  text-align: left;
  cursor: pointer;
  transition: 0.2s ease;
}

.nav-item.active,
.nav-item:hover {
  background: rgba(111, 217, 165, 0.12);
  border-color: rgba(111, 217, 165, 0.28);
  color: #fff;
}

.pump-card {
  margin-top: 36px;
  padding: 18px 16px;
  border-radius: 18px;
  background: rgba(255, 255, 255, 0.06);
  border: 1px solid rgba(255, 255, 255, 0.08);
}

.pump-card p {
  margin: 18px 0 0;
  color: rgba(255, 255, 255, 0.74);
  font-size: 0.9rem;
}

.mini-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
}

.toggle {
  width: 50px;
  height: 28px;
  border-radius: 999px;
  border: none;
  background: rgba(255,255,255,0.18);
  position: relative;
  cursor: pointer;
}

.toggle span {
  position: absolute;
  top: 4px;
  left: 6px;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background: white;
  transition: all 0.2s ease;
}

.toggle.on {
  background: #44c980;
}

.toggle.on span {
  left: 26px;
}

.main-panel {
  padding: 28px 26px 30px;
}

.topbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
  margin-bottom: 24px;
}

.topbar h2 {
  margin: 0;
  font-size: clamp(1.7rem, 2vw, 2.3rem);
}

.header-actions {
  display: flex;
  gap: 12px;
}

.ghost-btn,
.primary-btn {
  border-radius: 12px;
  border: none;
  padding: 11px 16px;
  cursor: pointer;
}

.ghost-btn {
  background: var(--panel-soft);
  color: var(--text);
}

.primary-btn {
  background: linear-gradient(135deg, #1d7a4d 0%, #2ea566 100%);
  color: #fff;
}

.metrics-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 18px;
  margin-bottom: 22px;
}

.metric-card {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 20px;
  padding: 20px 18px;
  box-shadow: 0 10px 24px rgba(21, 65, 45, 0.04);
}

.metric-card.accent {
  background: linear-gradient(135deg, #eefaf2 0%, #f4fff7 100%);
}

.metric-card span,
.sensor-box span,
.detail-footer span {
  display: block;
  color: var(--muted);
  font-size: 0.8rem;
}

.metric-card strong {
  display: block;
  font-size: clamp(1.7rem, 3vw, 2.3rem);
  margin: 8px 0 4px;
}

.metric-card small {
  color: var(--muted);
}

.content-grid {
  display: grid;
  grid-template-columns: 390px 1fr;
  gap: 22px;
}

.panel {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 24px;
  padding: 18px 16px 16px;
}

.panel-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 18px;
}

.panel-header h3 {
  margin: 0;
  font-size: 1.2rem;
}

.status-pill {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 28px;
  padding: 0 10px;
  border-radius: 999px;
  font-size: 0.78rem;
  font-weight: 600;
}

.status-pill.live {
  background: #e8fff1;
  color: var(--primary);
}

.status-pill.neutral {
  background: #eef5ee;
  color: var(--muted);
}

.field-list {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.field-item {
  width: 100%;
  background: #f8faf8;
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 14px 14px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-align: left;
  cursor: pointer;
  transition: all 0.2s ease;
}

.field-item.selected {
  background: #ebf9f0;
  border-color: #bfe6cb;
}

.field-item h4,
.field-item p {
  margin: 0;
}

.field-item h4 {
  font-size: 1rem;
}

.field-item p {
  color: var(--muted);
  margin-top: 4px;
}

.field-meta {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 8px;
}

.field-meta strong {
  font-size: 1.1rem;
}

.status-badge {
  padding: 7px 10px;
  border-radius: 999px;
  font-size: 0.7rem;
  font-weight: 600;
}

.status-badge.healthy,
.status-badge.optimal {
  background: #e8fff1;
  color: #1f8f59;
}

.status-badge.needs-water {
  background: #fff2d9;
  color: #a56a00;
}

.status-badge.critical {
  background: #ffe2e2;
  color: #c04d4d;
}

.sensor-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 14px;
}

.sensor-box {
  background: #f9fbf9;
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 16px 14px;
  min-height: 120px;
}

.sensor-box strong {
  display: block;
  margin-top: 8px;
  font-size: 1.6rem;
}

.moisture-box {
  background: linear-gradient(180deg, #ebfaf1 0%, #f5fff8 100%);
}

.bar-track {
  width: 100%;
  height: 10px;
  background: rgba(29, 122, 77, 0.12);
  border-radius: 999px;
  overflow: hidden;
  margin-top: 14px;
}

.bar-fill {
  height: 100%;
  border-radius: inherit;
}

.bar-fill.moisture {
  background: linear-gradient(90deg, #69d697 0%, #1d7a4d 100%);
}

.recommendation-box {
  margin-top: 18px;
  background: linear-gradient(135deg, #f7f5df 0%, #fffef3 100%);
  border: 1px solid #efe7b7;
  border-radius: 20px;
  padding: 18px 16px;
}

.recommendation-box h4 {
  margin: 0 0 8px;
  font-size: 1.15rem;
}

.recommendation-box p {
  margin: 0;
  color: #5a583c;
  line-height: 1.6;
}

.detail-footer {
  margin-top: 18px;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 12px;
}

.detail-footer > div {
  background: #f7faf7;
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 12px 14px;
}

.detail-footer strong {
  display: block;
  margin-top: 8px;
  font-size: 1.1rem;
}

@media (max-width: 980px) {
  .app-shell {
    grid-template-columns: 1fr;
    margin: 16px;
  }

  .sidebar {
    border-radius: 24px 24px 0 0;
  }

  .content-grid {
    grid-template-columns: 1fr;
  }

  .metrics-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 560px) {
  .main-panel {
    padding: 18px 14px 22px;
  }

  .metrics-grid,
  .sensor-grid,
  .detail-footer {
    grid-template-columns: 1fr;
  }

  .topbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .header-actions {
    width: 100%;
  }

  .header-actions button {
    flex: 1;
  }
}
