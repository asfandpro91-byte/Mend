# Mend
Site
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MEND — Recovery Companion</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0f0d;
    --surface: #111a15;
    --surface2: #162019;
    --border: #1e2e23;
    --green: #2dff6e;
    --green-dim: #1a9943;
    --amber: #ffb830;
    --red: #ff4d5a;
    --blue: #38d1ff;
    --text: #e8f0ea;
    --muted: #5a7060;
    --font-head: 'Syne', sans-serif;
    --font-mono: 'DM Mono', monospace;
  }
  * { margin:0; padding:0; box-sizing:border-box; }
  body { background:var(--bg); color:var(--text); font-family:var(--font-head); min-height:100vh; overflow-x:hidden; }

  /* ── SCREENS ── */
  .screen { display:none; min-height:100vh; padding-bottom:80px; }
  .screen.active { display:block; }

  /* ── HEADER ── */
  header {
    display:flex; align-items:center; justify-content:space-between;
    padding:16px 20px; border-bottom:1px solid var(--border);
    background:var(--surface); position:sticky; top:0; z-index:100;
  }
  .logo { font-size:1.4rem; font-weight:800; letter-spacing:-0.04em; color:var(--green); }
  .logo span { color:var(--muted); font-size:0.55rem; font-family:var(--font-mono); display:block; letter-spacing:0.2em; }
  .day-badge { font-family:var(--font-mono); font-size:0.7rem; color:var(--muted); background:var(--border); padding:5px 10px; border-radius:20px; }
  .day-badge strong { color:var(--green); }

  /* ── HERO ── */
  .hero { padding:24px 20px 16px; display:grid; grid-template-columns:1fr auto; gap:16px; align-items:start; }
  .greeting { font-size:0.65rem; font-family:var(--font-mono); color:var(--muted); letter-spacing:0.15em; text-transform:uppercase; margin-bottom:4px; }
  .patient-name { font-size:1.8rem; font-weight:800; letter-spacing:-0.04em; line-height:1; }
  .recovery-label { font-size:0.7rem; font-family:var(--font-mono); color:var(--green); margin-top:4px; }

  /* Ring */
  .ring-container { position:relative; width:80px; height:80px; }
  .ring-container svg { transform:rotate(-90deg); }
  .ring-bg { fill:none; stroke:var(--border); stroke-width:7; }
  .ring-progress { fill:none; stroke:var(--green); stroke-width:7; stroke-linecap:round; stroke-dasharray:220; stroke-dashoffset:220; filter:drop-shadow(0 0 8px var(--green)); transition:stroke-dashoffset 1.5s cubic-bezier(0.4,0,0.2,1); }
  .ring-label { position:absolute; top:50%; left:50%; transform:translate(-50%,-50%); text-align:center; }
  .ring-pct { font-size:1.2rem; font-weight:800; color:var(--green); line-height:1; }
  .ring-sub { font-size:0.48rem; font-family:var(--font-mono); color:var(--muted); letter-spacing:0.1em; }

  /* ── METRICS ── */
  .metrics { display:grid; grid-template-columns:repeat(3,1fr); gap:1px; background:var(--border); border-top:1px solid var(--border); border-bottom:1px solid var(--border); margin-bottom:20px; }
  .metric { background:var(--surface); padding:14px 16px; text-align:center; }
  .metric-val { font-size:1.4rem; font-weight:700; letter-spacing:-0.03em; line-height:1; }
  .metric-val.good { color:var(--green); }
  .metric-val.warn { color:var(--amber); }
  .metric-val.crit { color:var(--red); }
  .metric-label { font-size:0.58rem; font-family:var(--font-mono); color:var(--muted); letter-spacing:0.1em; text-transform:uppercase; margin-top:3px; }

  /* ── SECTION HEADERS ── */
  .section-head { display:flex; align-items:center; justify-content:space-between; padding:0 20px 10px; }
  .section-title { font-size:0.62rem; font-family:var(--font-mono); letter-spacing:0.2em; text-transform:uppercase; color:var(--muted); }
  .section-action { font-size:0.62rem; font-family:var(--font-mono); color:var(--green-dim); cursor:pointer; }

  /* ── EXERCISE CARDS ── */
  .cards { padding:0 16px; display:flex; flex-direction:column; gap:8px; margin-bottom:24px; }
  .card { background:var(--surface); border:1px solid var(--border); border-radius:12px; padding:14px; display:grid; grid-template-columns:48px 1fr auto; gap:12px; align-items:center; cursor:pointer; transition:border-color 0.2s,background 0.2s; position:relative; overflow:hidden; }
  .card:hover { border-color:var(--green-dim); background:var(--surface2); }
  .card.completed { opacity:0.55; }
  .card.completed::after,.card.active::after { content:''; position:absolute; left:0;top:0;bottom:0; width:3px; border-radius:3px 0 0 3px; }
  .card.completed::after { background:var(--green); }
  .card.active { border-color:var(--green); background:var(--surface2); }
  .card.active::after { background:var(--green); box-shadow:0 0 12px var(--green); }
  .card-icon { width:48px; height:48px; border-radius:10px; background:var(--surface2); border:1px solid var(--border); display:flex; align-items:center; justify-content:center; font-size:1.3rem; }
  .card.active .card-icon { background:rgba(45,255,110,0.08); border-color:var(--green-dim); }
  .card-title { font-size:0.9rem; font-weight:700; letter-spacing:-0.02em; margin-bottom:2px; }
  .card-meta { font-size:0.62rem; font-family:var(--font-mono); color:var(--muted); }
  .card-tag { font-size:0.55rem; font-family:var(--font-mono); padding:3px 7px; border-radius:20px; letter-spacing:0.08em; text-transform:uppercase; white-space:nowrap; }
  .tag-easy { background:rgba(45,255,110,0.1); color:var(--green); border:1px solid rgba(45,255,110,0.2); }
  .tag-med  { background:rgba(255,184,48,0.1); color:var(--amber); border:1px solid rgba(255,184,48,0.2); }
  .tag-hard { background:rgba(255,77,90,0.1); color:var(--red); border:1px solid rgba(255,77,90,0.2); }
  .tag-done { background:rgba(45,255,110,0.05); color:var(--muted); border:1px solid var(--border); }

  /* ── PAIN MAP ── */
  .pain-section { padding:0 16px 24px; }
  .body-map { background:var(--surface); border:1px solid var(--border); border-radius:12px; padding:16px; display:flex; gap:16px; align-items:center; }
  .body-svg-wrap { flex-shrink:0; position:relative; }
  .pain-dot { position:absolute; width:14px; height:14px; border-radius:50%; transform:translate(-50%,-50%); cursor:pointer; transition:transform 0.2s; }
  .pain-dot:hover { transform:translate(-50%,-50%) scale(1.4); }
  .pain-dot.low { background:var(--amber); box-shadow:0 0 8px var(--amber); }
  .pain-dot.high { background:var(--red); box-shadow:0 0 12px var(--red); animation:pdot 1.4s infinite; }
  @keyframes pdot { 0%,100%{box-shadow:0 0 6px var(--red);transform:translate(-50%,-50%) scale(1);}50%{box-shadow:0 0 18px var(--red);transform:translate(-50%,-50%) scale(1.2);} }
  .pain-legend { flex:1; }
  .pain-legend h4 { font-size:0.65rem; font-family:var(--font-mono); color:var(--muted); letter-spacing:0.15em; text-transform:uppercase; margin-bottom:10px; }
  .pain-item { display:flex; align-items:center; gap:8px; margin-bottom:8px; }
  .pain-dot-sm { width:8px; height:8px; border-radius:50%; flex-shrink:0; }
  .pain-text { font-size:0.72rem; font-weight:600; }
  .pain-sub { font-size:0.58rem; font-family:var(--font-mono); color:var(--muted); }

  /* ── PAIN SLIDER ── */
  .pain-log-card { background:var(--surface); border:1px solid var(--border); border-radius:12px; padding:16px; margin-bottom:16px; }
  .pain-log-card h3 { font-size:0.9rem; font-weight:700; margin-bottom:12px; }
  .pain-slider-row { display:flex; align-items:center; gap:12px; margin-bottom:8px; }
  .pain-slider-row label { font-size:0.65rem; font-family:var(--font-mono); color:var(--muted); width:90px; }
  input[type=range] { flex:1; accent-color:var(--green); }
  .pain-val { font-size:0.9rem; font-weight:700; color:var(--green); width:24px; text-align:right; font-family:var(--font-mono); }
  .btn-primary { background:var(--green); color:#0a0f0d; border:none; padding:10px 16px; border-radius:8px; font-family:var(--font-head); font-size:0.75rem; font-weight:700; cursor:pointer; transition:opacity 0.2s,transform 0.15s; }
  .btn-primary:hover { opacity:0.85; transform:translateY(-1px); }
  .btn-ghost { background:transparent; color:var(--muted); border:1px solid var(--border); padding:10px 16px; border-radius:8px; font-family:var(--font-head); font-size:0.75rem; font-weight:600; cursor:pointer; transition:border-color 0.2s,color 0.2s; }
  .btn-ghost:hover { border-color:var(--muted); color:var(--text); }

  /* ── PROGRESS SCREEN ── */
  .progress-section { padding:0 16px 24px; }
  .progress-card { background:var(--surface); border:1px solid var(--border); border-radius:12px; padding:16px; margin-bottom:12px; }
  .progress-card h3 { font-size:0.85rem; font-weight:700; margin-bottom:12px; }
  .bar-row { margin-bottom:10px; }
  .bar-label { display:flex; justify-content:space-between; font-size:0.65rem; font-family:var(--font-mono); color:var(--muted); margin-bottom:4px; }
  .bar-track { background:var(--border); border-radius:4px; height:8px; overflow:hidden; }
  .bar-fill { height:100%; border-radius:4px; background:var(--green); transition:width 1s ease; }
  .bar-fill.amber { background:var(--amber); }
  .bar-fill.red { background:var(--red); }
  .stat-grid { display:grid; grid-template-columns:repeat(2,1fr); gap:10px; }
  .stat-box { background:var(--surface2); border:1px solid var(--border); border-radius:10px; padding:14px; text-align:center; }
  .stat-num { font-size:1.6rem; font-weight:800; color:var(--green); letter-spacing:-0.04em; }
  .stat-label { font-size:0.6rem; font-family:var(--font-mono); color:var(--muted); letter-spacing:0.08em; margin-top:2px; }

  /* ── COACH SCREEN ── */
  .coach-section { padding:0 16px 24px; }
  .coach-card { background:linear-gradient(135deg,rgba(45,255,110,0.05),rgba(56,209,255,0.05)); border:1px solid rgba(45,255,110,0.2); border-radius:12px; padding:16px; margin-bottom:12px; }
  .coach-header { display:flex; align-items:center; gap:10px; margin-bottom:10px; }
  .coach-avatar { width:32px; height:32px; border-radius:50%; background:linear-gradient(135deg,var(--green),var(--blue)); display:flex; align-items:center; justify-content:center; font-size:0.9rem; flex-shrink:0; }
  .coach-name { font-size:0.68rem; font-family:var(--font-mono); color:var(--green); }
  .coach-role { font-size:0.58rem; font-family:var(--font-mono); color:var(--muted); }
  .coach-message { font-size:0.82rem; line-height:1.55; color:var(--text); opacity:0.9; }
  .coach-message strong { color:var(--green); }
  .coach-input-wrap { background:var(--surface); border:1px solid var(--border); border-radius:12px; padding:16px; }
  .coach-input-wrap h3 { font-size:0.85rem; font-weight:700; margin-bottom:10px; }
  .input-row { display:flex; gap:8px; }
  textarea { flex:1; background:var(--surface2); border:1px solid var(--border); border-radius:8px; padding:10px; color:var(--text); font-family:var(--font-head); font-size:0.8rem; resize:none; outline:none; transition:border-color 0.2s; }
  textarea:focus { border-color:var(--green-dim); }
  .coach-responses { margin-top:12px; display:flex; flex-direction:column; gap:8px; }
  .coach-response-item { background:var(--surface2); border:1px solid var(--border); border-radius:8px; padding:12px; font-size:0.8rem; line-height:1.5; }
  .coach-response-item .q { font-size:0.65rem; font-family:var(--font-mono); color:var(--muted); margin-bottom:4px; }

  /* ── SETTINGS SCREEN ── */
  .settings-section { padding:0 16px 24px; }
  .settings-card { background:var(--surface); border:1px solid var(--border); border-radius:12px; padding:16px; margin-bottom:12px; }
  .settings-card h3 { font-size:0.85rem; font-weight:700; margin-bottom:14px; color:var(--green); }
  .setting-row { display:flex; align-items:center; justify-content:space-between; padding:10px 0; border-bottom:1px solid var(--border); }
  .setting-row:last-child { border-bottom:none; }
  .setting-label { font-size:0.8rem; font-weight:600; }
  .setting-sub { font-size:0.62rem; font-family:var(--font-mono); color:var(--muted); margin-top:2px; }
  .toggle { width:44px; height:24px; background:var(--border); border-radius:12px; position:relative; cursor:pointer; transition:background 0.3s; flex-shrink:0; }
  .toggle.on { background:var(--green); }
  .toggle::after { content:''; position:absolute; width:18px; height:18px; background:#fff; border-radius:50%; top:3px; left:3px; transition:left 0.3s; }
  .toggle.on::after { left:23px; }
  .setting-input { background:var(--surface2); border:1px solid var(--border); border-radius:6px; padding:6px 10px; color:var(--text); font-family:var(--font-mono); font-size:0.8rem; width:100px; outline:none; text-align:center; }
  .setting-select { background:var(--surface2); border:1px solid var(--border); border-radius:6px; padding:6px 10px; color:var(--text); font-family:var(--font-mono); font-size:0.75rem; outline:none; cursor:pointer; }

  /* ── STREAK ── */
  .streak-section { padding:0 16px 24px; }
  .streak-row { background:var(--surface); border:1px solid var(--border); border-radius:12px; padding:16px; }
  .streak-header { display:flex; justify-content:space-between; margin-bottom:12px; }
  .streak-title { font-size:0.82rem; font-weight:700; }
  .streak-count { font-family:var(--font-mono); font-size:0.68rem; color:var(--amber); }
  .week-dots { display:flex; gap:4px; justify-content:space-between; }
  .week-day { flex:1; text-align:center; }
  .week-dot { width:100%; aspect-ratio:1; border-radius:6px; margin:0 auto 4px; max-width:34px; }
  .week-dot.done { background:var(--green); box-shadow:0 0 6px rgba(45,255,110,0.3); }
  .week-dot.today { background:var(--surface2); border:2px solid var(--green); animation:glow 2s infinite; }
  .week-dot.missed { background:var(--surface2); border:1px solid var(--border); }
  @keyframes glow { 0%,100%{box-shadow:0 0 0 rgba(45,255,110,0);}50%{box-shadow:0 0 10px rgba(45,255,110,0.4);} }
  .week-label { font-size:0.52rem; font-family:var(--font-mono); color:var(--muted); }

  /* ── NAV ── */
  nav { position:fixed; bottom:0;left:0;right:0; background:var(--surface); border-top:1px solid var(--border); display:grid; grid-template-columns:repeat(4,1fr); padding:8px 0 18px; z-index:100; }
  .nav-item { display:flex; flex-direction:column; align-items:center; gap:3px; cursor:pointer; opacity:0.4; transition:opacity 0.2s; }
  .nav-item.active { opacity:1; }
  .nav-icon { font-size:1.2rem; }
  .nav-label { font-size:0.52rem; font-family:var(--font-mono); letter-spacing:0.08em; color:var(--muted); }
  .nav-item.active .nav-label { color:var(--green); }

  /* ── MODAL ── */
  .modal-overlay { position:fixed; inset:0; background:rgba(0,0,0,0.85); display:flex; align-items:flex-end; z-index:200; opacity:0; pointer-events:none; transition:opacity 0.3s; }
  .modal-overlay.open { opacity:1; pointer-events:all; }
  .modal { background:var(--surface); border:1px solid var(--border); border-radius:20px 20px 0 0; padding:20px; width:100%; transform:translateY(100%); transition:transform 0.4s cubic-bezier(0.4,0,0.2,1); max-height:85vh; overflow-y:auto; }
  .modal-overlay.open .modal { transform:translateY(0); }
  .modal-handle { width:40px; height:4px; background:var(--border); border-radius:2px; margin:0 auto 16px; }
  .modal-title { font-size:1.2rem; font-weight:800; letter-spacing:-0.03em; margin-bottom:4px; }
  .modal-meta { font-size:0.68rem; font-family:var(--font-mono); color:var(--muted); margin-bottom:16px; }
  .timer-display { text-align:center; padding:20px; border:1px solid var(--border); border-radius:10px; margin-bottom:14px; background:var(--surface2); }
  .timer-num { font-size:3rem; font-weight:800; letter-spacing:-0.06em; color:var(--green); font-variant-numeric:tabular-nums; }
  .timer-label { font-size:0.6rem; font-family:var(--font-mono); color:var(--muted); letter-spacing:0.15em; text-transform:uppercase; }
  .reps-row { display:grid; grid-template-columns:repeat(3,1fr); gap:8px; margin-bottom:14px; }
  .rep-box { background:var(--surface2); border:1px solid var(--border); border-radius:8px; padding:10px; text-align:center; cursor:pointer; transition:border-color 0.2s,background 0.2s; font-weight:700; font-size:1rem; }
  .rep-box:hover { border-color:var(--green-dim); }
  .rep-box.done { background:rgba(45,255,110,0.1); border-color:var(--green); color:var(--green); }
  .rep-sub { font-size:0.52rem; font-family:var(--font-mono); color:var(--muted); display:block; margin-top:2px; font-weight:400; }
  .pain-during { margin-bottom:14px; }
  .pain-during label { font-size:0.65rem; font-family:var(--font-mono); color:var(--muted); display:block; margin-bottom:6px; }

  /* ── TOAST ── */
  .toast { position:fixed; top:80px; left:50%; transform:translateX(-50%) translateY(-20px); background:var(--green); color:#0a0f0d; padding:10px 20px; border-radius:30px; font-size:0.78rem; font-weight:700; opacity:0; transition:all 0.3s; z-index:300; white-space:nowrap; pointer-events:none; }
  .toast.show { opacity:1; transform:translateX(-50%) translateY(0); }

  /* ── ADD EXERCISE FORM ── */
  .add-form { background:var(--surface); border:1px solid var(--border); border-radius:12px; padding:16px; margin:0 16px 16px; }
  .add-form h3 { font-size:0.85rem; font-weight:700; margin-bottom:12px; color:var(--green); }
  .form-row { margin-bottom:10px; }
  .form-row label { font-size:0.62rem; font-family:var(--font-mono); color:var(--muted); display:block; margin-bottom:4px; letter-spacing:0.1em; }
  .form-row input, .form-row select { width:100%; background:var(--surface2); border:1px solid var(--border); border-radius:8px; padding:8px 12px; color:var(--text); font-family:var(--font-head); font-size:0.8rem; outline:none; transition:border-color 0.2s; }
  .form-row input:focus, .form-row select:focus { border-color:var(--green-dim); }
  .form-row select option { background:var(--surface2); }
  .form-grid { display:grid; grid-template-columns:1fr 1fr; gap:10px; }

  /* animations */
  @keyframes fadeUp { from{opacity:0;transform:translateY(14px);}to{opacity:1;transform:translateY(0);} }
  .hero{animation:fadeUp 0.4s ease both;}
  .metrics{animation:fadeUp 0.4s 0.08s ease both;}
</style>
</head>
<body>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<!-- ═══ SCREEN: HOME ═══ -->
<div class="screen active" id="screen-home">
  <header>
    <div class="logo">MEND<span>RECOVERY COMPANION</span></div>
    <div class="day-badge">Day <strong id="day-num">1</strong> of <strong id="total-days">42</strong></div>
  </header>

  <div class="hero">
    <div>
      <div class="greeting">// Good morning</div>
      <div class="patient-name" id="display-name">Marcus</div>
      <div class="recovery-label" id="progress-label">↑ Starting your recovery</div>
    </div>
    <div class="ring-container">
      <svg width="80" height="80" viewBox="0 0 80 80">
        <circle class="ring-bg" cx="40" cy="40" r="35"/>
        <circle class="ring-progress" id="ring" cx="40" cy="40" r="35"/>
      </svg>
      <div class="ring-label">
        <div class="ring-pct" id="ring-pct">0%</div>
        <div class="ring-sub">TODAY</div>
      </div>
    </div>
  </div>

  <div class="metrics">
    <div class="metric">
      <div class="metric-val good" id="streak-val">0</div>
      <div class="metric-label">Streak</div>
    </div>
    <div class="metric">
      <div class="metric-val warn" id="pain-val">—</div>
      <div class="metric-label">Pain</div>
    </div>
    <div class="metric">
      <div class="metric-val good" id="done-val">0/0</div>
      <div class="metric-label">Done</div>
    </div>
  </div>

  <div class="section-head">
    <div class="section-title">// Today's Protocol</div>
    <div class="section-action" onclick="showAddForm()">+ add exercise</div>
  </div>

  <!-- Add exercise form (hidden by default) -->
  <div class="add-form" id="add-form" style="display:none;">
    <h3>+ New Exercise</h3>
    <div class="form-row">
      <label>EXERCISE NAME</label>
      <input type="text" id="new-name" placeholder="e.g. Wall Slides">
    </div>
    <div class="form-grid">
      <div class="form-row">
        <label>SETS</label>
        <input type="number" id="new-sets" value="3" min="1" max="10">
      </div>
      <div class="form-row">
        <label>REPS</label>
        <input type="number" id="new-reps" value="12" min="1" max="50">
      </div>
    </div>
    <div class="form-grid">
      <div class="form-row">
        <label>BODY PART</label>
        <input type="text" id="new-part" placeholder="Shoulder">
      </div>
      <div class="form-row">
        <label>DIFFICULTY</label>
        <select id="new-diff">
          <option value="easy">Easy</option>
          <option value="med" selected>Medium</option>
          <option value="hard">Hard</option>
        </select>
      </div>
    </div>
    <div class="form-row">
      <label>ICON (emoji)</label>
      <input type="text" id="new-icon" placeholder="💪" maxlength="2" value="🏋️">
    </div>
    <div style="display:flex;gap:8px;margin-top:4px;">
      <button class="btn-primary" onclick="addExercise()" style="flex:1;">Add Exercise</button>
      <button class="btn-ghost" onclick="hideAddForm()">Cancel</button>
    </div>
  </div>

  <div class="cards" id="exercise-list"></div>

  <div class="section-head">
    <div class="section-title">// Pain Log</div>
  </div>
  <div class="pain-section">
    <div class="body-map">
      <div class="body-svg-wrap">
        <svg width="76" height="130" viewBox="0 0 76 130" style="opacity:0.25;">
          <ellipse cx="38" cy="13" rx="11" ry="12" fill="#5a7060"/>
          <rect x="22" y="26" width="30" height="40" rx="8" fill="#5a7060"/>
          <rect x="5" y="28" width="15" height="34" rx="7" fill="#5a7060"/>
          <rect x="56" y="28" width="15" height="34" rx="7" fill="#5a7060"/>
          <rect x="23" y="68" width="13" height="42" rx="7" fill="#5a7060"/>
          <rect x="40" y="68" width="13" height="42" rx="7" fill="#5a7060"/>
        </svg>
        <div id="pain-dots"></div>
      </div>
      <div class="pain-legend">
        <h4>// Pain Points</h4>
        <div id="pain-legend-list">
          <div style="font-size:0.68rem;color:var(--muted);font-family:var(--font-mono);">No pain logged yet.</div>
        </div>
        <div style="margin-top:12px;">
          <button class="btn-ghost" style="width:100%;font-size:0.62rem;padding:7px;" onclick="goTo('screen-bodymap')">+ Log pain point</button>
        </div>
      </div>
    </div>
  </div>

  <div class="section-head">
    <div class="section-title">// This Week</div>
    <span class="streak-count" id="streak-label">🔥 0-day streak</span>
  </div>
  <div class="streak-section">
    <div class="streak-row">
      <div class="week-dots" id="week-dots"></div>
    </div>
  </div>
</div>

<!-- ═══ SCREEN: PROGRESS ═══ -->
<div class="screen" id="screen-progress">
  <header>
    <div class="logo">MEND<span>PROGRESS</span></div>
    <div class="day-badge">Week <strong id="week-num">1</strong></div>
  </header>
  <div style="padding:20px 0 0;">
    <div class="section-head"><div class="section-title">// Recovery Stats</div></div>
    <div class="progress-section">
      <div class="stat-grid" style="margin-bottom:12px;">
        <div class="stat-box"><div class="stat-num" id="p-completed">0</div><div class="stat-label">EXERCISES DONE</div></div>
        <div class="stat-box"><div class="stat-num" id="p-streak">0</div><div class="stat-label">DAY STREAK</div></div>
        <div class="stat-box"><div class="stat-num" id="p-avgpain" style="color:var(--amber);">—</div><div class="stat-label">AVG PAIN</div></div>
        <div class="stat-box"><div class="stat-num" id="p-days">0</div><div class="stat-label">DAYS ACTIVE</div></div>
      </div>

      <div class="progress-card">
        <h3>Weekly Completion</h3>
        <div id="weekly-bars"></div>
      </div>

      <div class="progress-card">
        <h3>Pain Trend (this week)</h3>
        <div id="pain-trend-bars"></div>
      </div>
    </div>
  </div>
</div>

<!-- ═══ SCREEN: BODY MAP ═══ -->
<div class="screen" id="screen-bodymap">
  <header>
    <div class="logo">MEND<span>PAIN MAP</span></div>
  </header>
  <div style="padding:20px;">
    <div class="section-head" style="padding:0 0 12px;"><div class="section-title">// Log a Pain Point</div></div>

    <div class="pain-log-card">
      <h3>Add Pain Location</h3>
      <div class="form-row">
        <label>BODY AREA</label>
        <select id="pain-area" class="setting-select" style="width:100%;">
          <option>Right Shoulder</option>
          <option>Left Shoulder</option>
          <option>Upper Back</option>
          <option>Lower Back</option>
          <option>Right Knee</option>
          <option>Left Knee</option>
          <option>Right Hip</option>
          <option>Left Hip</option>
          <option>Neck</option>
          <option>Right Elbow</option>
          <option>Left Elbow</option>
          <option>Right Wrist</option>
          <option>Left Wrist</option>
        </select>
      </div>
      <div class="pain-slider-row" style="margin-top:10px;">
        <label>PAIN LEVEL</label>
        <input type="range" min="1" max="10" value="5" id="pain-level" oninput="document.getElementById('pain-level-val').textContent=this.value;updatePainColor(this.value)">
        <div class="pain-val" id="pain-level-val">5</div>
      </div>
      <div style="display:flex;justify-content:space-between;font-size:0.58rem;font-family:var(--font-mono);color:var(--muted);margin-bottom:14px;">
        <span>Mild</span><span>Moderate</span><span>Severe</span>
      </div>
      <div class="form-row">
        <label>TYPE</label>
        <select id="pain-type" class="setting-select" style="width:100%;">
          <option>Post-exercise</option>
          <option>Constant ache</option>
          <option>Sharp pain</option>
          <option>Stiffness</option>
          <option>Tension</option>
          <option>Swelling</option>
        </select>
      </div>
      <button class="btn-primary" style="width:100%;margin-top:8px;" onclick="logPainPoint()">Log Pain Point</button>
    </div>

    <div class="section-head" style="padding:0 0 10px;"><div class="section-title">// Current Pain Points</div></div>
    <div id="pain-list-full" style="display:flex;flex-direction:column;gap:8px;"></div>
  </div>
</div>

<!-- ═══ SCREEN: COACH ═══ -->
<div class="screen" id="screen-coach">
  <header>
    <div class="logo">MEND<span>AI COACH</span></div>
  </header>
  <div style="padding:20px 0 0;">
    <div class="section-head"><div class="section-title">// Daily Insight</div></div>
    <div class="coach-section">
      <div class="coach-card">
        <div class="coach-header">
          <div class="coach-avatar">🤖</div>
          <div><div class="coach-name">MEND AI</div><div class="coach-role">Recovery Specialist</div></div>
        </div>
        <div class="coach-message" id="daily-insight">Loading your personalised insight...</div>
      </div>

      <div class="coach-input-wrap">
        <h3>Ask your coach</h3>
        <div class="input-row">
          <textarea id="coach-question" rows="2" placeholder="e.g. Should I rest today? My shoulder is sore..."></textarea>
          <button class="btn-primary" onclick="askCoach()" style="align-self:flex-end;">Ask</button>
        </div>
        <div class="coach-responses" id="coach-responses"></div>
      </div>
    </div>
  </div>
</div>

<!-- ═══ SCREEN: SETTINGS (accessed via name tap) ═══ -->
<div class="screen" id="screen-settings">
  <header>
    <div class="logo">MEND<span>SETTINGS</span></div>
    <button class="btn-ghost" onclick="goTo('screen-home')" style="font-size:0.65rem;padding:6px 12px;">← Back</button>
  </header>
  <div style="padding:20px 0 0;">
    <div class="section-head"><div class="section-title">// Your Profile</div></div>
    <div class="settings-section">
      <div class="settings-card">
        <h3>Patient Info</h3>
        <div class="setting-row">
          <div><div class="setting-label">Name</div><div class="setting-sub">Shown on home screen</div></div>
          <input class="setting-input" id="set-name" type="text" value="Marcus" oninput="updateName()">
        </div>
        <div class="setting-row">
          <div><div class="setting-label">Recovery Day</div><div class="setting-sub">Current day in program</div></div>
          <input class="setting-input" id="set-day" type="number" value="1" min="1" oninput="updateDay()">
        </div>
        <div class="setting-row">
          <div><div class="setting-label">Program Length</div><div class="setting-sub">Total days</div></div>
          <input class="setting-input" id="set-total" type="number" value="42" min="1" oninput="updateTotal()">
        </div>
        <div class="setting-row">
          <div><div class="setting-label">Injury Type</div></div>
          <select class="setting-select" id="set-injury" onchange="updateInjury()">
            <option>Shoulder</option>
            <option>Knee</option>
            <option>Hip</option>
            <option>Back</option>
            <option>Elbow</option>
            <option>Wrist</option>
            <option>Ankle</option>
          </select>
        </div>
      </div>

      <div class="settings-card">
        <h3>Notifications</h3>
        <div class="setting-row">
          <div><div class="setting-label">Daily Reminder</div><div class="setting-sub">Remind me to exercise</div></div>
          <div class="toggle on" id="toggle-remind" onclick="toggleSetting(this)"></div>
        </div>
        <div class="setting-row">
          <div><div class="setting-label">Pain Check-in</div><div class="setting-sub">Evening pain logging prompt</div></div>
          <div class="toggle on" id="toggle-pain" onclick="toggleSetting(this)"></div>
        </div>
        <div class="setting-row">
          <div><div class="setting-label">Coach Insights</div><div class="setting-sub">Daily AI tip</div></div>
          <div class="toggle on" id="toggle-coach" onclick="toggleSetting(this)"></div>
        </div>
      </div>

      <div class="settings-card">
        <h3>Display</h3>
        <div class="setting-row">
          <div><div class="setting-label">Rest Timer Duration</div><div class="setting-sub">Seconds between sets</div></div>
          <input class="setting-input" id="set-timer" type="number" value="30" min="10" max="120">
        </div>
        <div class="setting-row">
          <div><div class="setting-label">Theme</div></div>
          <select class="setting-select" id="set-theme" onchange="applyTheme()">
            <option value="dark">Dark (default)</option>
            <option value="teal">Teal</option>
            <option value="blue">Blue</option>
            <option value="red">Red</option>
          </select>
        </div>
      </div>

      <button class="btn-ghost" style="width:calc(100% - 0px);padding:12px;" onclick="resetAll()">Reset All Data</button>
    </div>
  </div>
</div>

<!-- ── NAV ── -->
<nav>
  <div class="nav-item active" id="nav-home" onclick="goTo('screen-home')">
    <div class="nav-icon">🏠</div><div class="nav-label">TODAY</div>
  </div>
  <div class="nav-item" id="nav-progress" onclick="goTo('screen-progress')">
    <div class="nav-icon">📈</div><div class="nav-label">PROGRESS</div>
  </div>
  <div class="nav-item" id="nav-bodymap" onclick="goTo('screen-bodymap')">
    <div class="nav-icon">🗺️</div><div class="nav-label">BODY MAP</div>
  </div>
  <div class="nav-item" id="nav-coach" onclick="goTo('screen-coach')">
    <div class="nav-icon">💬</div><div class="nav-label">COACH</div>
  </div>
</nav>

<!-- ── EXERCISE MODAL ── -->
<div class="modal-overlay" id="modal" onclick="closeModalOutside(event)">
  <div class="modal">
    <div class="modal-handle"></div>
    <div class="modal-title" id="modal-title">Exercise</div>
    <div class="modal-meta" id="modal-meta"></div>
    <div class="timer-display">
      <div class="timer-num" id="timer">00:30</div>
      <div class="timer-label">Rest Timer — tap a set to start</div>
    </div>
    <div class="reps-row" id="sets-container"></div>
    <div class="pain-during">
      <label>PAIN DURING THIS EXERCISE (1–10)</label>
      <div style="display:flex;align-items:center;gap:12px;">
        <input type="range" min="1" max="10" value="3" id="exercise-pain" style="flex:1;" oninput="document.getElementById('ex-pain-val').textContent=this.value">
        <span id="ex-pain-val" style="font-family:var(--font-mono);color:var(--green);font-weight:700;">3</span>
      </div>
    </div>
    <button class="btn-primary" style="width:100%;padding:12px;font-size:0.82rem;" onclick="completeExercise()">Mark Complete ✓</button>
  </div>
</div>

<script>
// ═══════════════════════════════════════
// STATE
// ═══════════════════════════════════════
let state = {
  name: 'Marcus',
  day: 1,
  totalDays: 42,
  injury: 'Shoulder',
  streak: 0,
  daysActive: 0,
  exercises: [
    { id:1, icon:'🔄', title:'Pendulum Swings',    sets:3, reps:20, part:'Shoulder',    diff:'easy', done:false },
    { id:2, icon:'🧱', title:'Wall Slides',         sets:3, reps:12, part:'Scapula',     diff:'easy', done:false },
    { id:3, icon:'💪', title:'Isometric Hold',      sets:3, reps:3,  part:'Rotator Cuff',diff:'med',  done:false },
    { id:4, icon:'🎯', title:'Band External Rotation',sets:3,reps:15,part:'Rotator Cuff',diff:'med',  done:false },
  ],
  painPoints: [],
  weekData: [true,true,true,true,true,false,false],
  timerDuration: 30,
  completedTotal: 0,
  avgPain: null,
  painHistory: [null,null,null,null,null,null,null],
};

let currentExerciseId = null;
let timerInterval = null;
let timerSeconds = 30;

// ═══════════════════════════════════════
// NAVIGATION
// ═══════════════════════════════════════
function goTo(screenId) {
  document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
  document.getElementById(screenId).classList.add('active');
  document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
  const map = {'screen-home':'nav-home','screen-progress':'nav-progress','screen-bodymap':'nav-bodymap','screen-coach':'nav-coach'};
  if(map[screenId]) document.getElementById(map[screenId]).classList.add('active');
  if(screenId==='screen-progress') renderProgress();
  if(screenId==='screen-coach') renderCoachInsight();
  if(screenId==='screen-bodymap') renderPainListFull();
}

// ═══════════════════════════════════════
// RENDER HOME
// ═══════════════════════════════════════
function renderHome() {
  // Name & day
  document.getElementById('display-name').textContent = state.name + '.';
  document.getElementById('display-name').onclick = () => goTo('screen-settings');
  document.getElementById('display-name').style.cursor = 'pointer';
  document.getElementById('day-num').textContent = state.day;
  document.getElementById('total-days').textContent = state.totalDays;

  // Progress label
  const done = state.exercises.filter(e=>e.done).length;
  const total = state.exercises.length;
  const pct = total ? Math.round((done/total)*100) : 0;
  document.getElementById('progress-label').textContent = pct >= 100 ? '🎉 All done today!' : `↑ ${pct}% complete today`;

  // Ring
  const ring = document.getElementById('ring');
  const offset = 220 - (220 * pct / 100);
  ring.style.strokeDashoffset = offset;
  document.getElementById('ring-pct').textContent = pct + '%';

  // Metrics
  document.getElementById('streak-val').textContent = state.streak;
  document.getElementById('pain-val').textContent = state.avgPain !== null ? state.avgPain+'/10' : '—';
  document.getElementById('done-val').textContent = done+'/'+total;

  // Exercises
  renderExercises();

  // Pain dots on map
  renderPainDots();

  // Week streak
  renderWeek();
}

function renderExercises() {
  const list = document.getElementById('exercise-list');
  list.innerHTML = '';
  if(state.exercises.length === 0) {
    list.innerHTML = '<div style="text-align:center;padding:24px;color:var(--muted);font-family:var(--font-mono);font-size:0.72rem;">No exercises yet. Add one above.</div>';
    return;
  }
  state.exercises.forEach((ex, i) => {
    const isNext = !ex.done && !state.exercises.slice(0,i).find(e=>!e.done);
    const tagClass = ex.done ? 'tag-done' : (ex.diff==='easy'?'tag-easy':ex.diff==='med'?'tag-med':'tag-hard');
    const tagText = ex.done ? 'Done' : (ex.diff==='easy'?'Easy':ex.diff==='med'?'Medium':'Hard');
    const div = document.createElement('div');
    div.className = 'card' + (ex.done?' completed':'') + (isNext&&!ex.done?' active':'');
    div.innerHTML = `
      <div class="card-icon">${ex.icon}</div>
      <div>
        <div class="card-title">${ex.title}</div>
        <div class="card-meta">${ex.sets} sets · ${ex.reps} reps · ${ex.part}</div>
      </div>
      <div class="card-tag ${tagClass}">${tagText}</div>`;
    div.onclick = () => openExerciseModal(ex.id);
    list.appendChild(div);
  });
}

function renderPainDots() {
  const container = document.getElementById('pain-dots');
  container.innerHTML = '';
  const positions = {
    'Right Shoulder':{left:'62px',top:'38px'},'Left Shoulder':{left:'14px',top:'38px'},
    'Upper Back':{left:'38px',top:'55px'},'Lower Back':{left:'38px',top:'72px'},
    'Right Knee':{left:'54px',top:'100px'},'Left Knee':{left:'22px',top:'100px'},
    'Neck':{left:'38px',top:'22px'},'Right Hip':{left:'52px',top:'78px'},'Left Hip':{left:'24px',top:'78px'},
  };
  const legend = document.getElementById('pain-legend-list');
  legend.innerHTML = '';
  if(state.painPoints.length === 0) {
    legend.innerHTML = '<div style="font-size:0.68rem;color:var(--muted);font-family:var(--font-mono);">No pain logged yet.</div>';
    return;
  }
  state.painPoints.forEach(p => {
    const pos = positions[p.area] || {left:'38px',top:'60px'};
    const dot = document.createElement('div');
    dot.className = 'pain-dot ' + (p.level >= 6 ? 'high' : 'low');
    dot.style.left = pos.left; dot.style.top = pos.top;
    dot.title = p.area + ' – ' + p.level + '/10';
    container.appendChild(dot);
    const item = document.createElement('div');
    item.className = 'pain-item';
    item.innerHTML = `<div class="pain-dot-sm" style="background:${p.level>=6?'var(--red)':'var(--amber)'};box-shadow:0 0 6px ${p.level>=6?'var(--red)':'var(--amber)'}"></div>
      <div><div class="pain-text">${p.area}</div><div class="pain-sub">${p.level}/10 · ${p.type}</div></div>`;
    legend.appendChild(item);
  });
}

function renderWeek() {
  const days = ['MON','TUE','WED','THU','FRI','SAT','SUN'];
  const container = document.getElementById('week-dots');
  container.innerHTML = '';
  const today = new Date().getDay();
  const todayIdx = today === 0 ? 6 : today - 1;
  state.weekData.forEach((done, i) => {
    const isToday = i === todayIdx;
    const div = document.createElement('div');
    div.className = 'week-day';
    const dotClass = isToday ? 'today' : (done ? 'done' : 'missed');
    div.innerHTML = `<div class="week-dot ${dotClass}"></div><div class="week-label" style="${isToday?'color:var(--green)':''}">${days[i]}</div>`;
    container.appendChild(div);
  });
  const streak = state.streak;
  document.getElementById('streak-label').textContent = `🔥 ${streak}-day streak`;
}

// ═══════════════════════════════════════
// EXERCISE MODAL
// ═══════════════════════════════════════
function openExerciseModal(id) {
  const ex = state.exercises.find(e=>e.id===id);
  if(!ex) return;
  currentExerciseId = id;
  document.getElementById('modal-title').textContent = ex.title;
  document.getElementById('modal-meta').textContent = `${ex.sets} sets · ${ex.reps} reps · ${ex.part}`;
  const container = document.getElementById('sets-container');
  container.innerHTML = '';
  for(let i=1;i<=ex.sets;i++){
    const div = document.createElement('div');
    div.className = 'rep-box';
    div.id = 'set-'+i;
    div.onclick = () => markSet(div, i);
    div.innerHTML = `Set ${i}<span class="rep-sub">${ex.reps} reps</span>`;
    container.appendChild(div);
  }
  timerSeconds = parseInt(document.getElementById('set-timer')?.value || 30);
  resetTimer();
  document.getElementById('exercise-pain').value = 3;
  document.getElementById('ex-pain-val').textContent = 3;
  document.getElementById('modal').classList.add('open');
}

function closeModalOutside(e) {
  if(e.target === document.getElementById('modal')) {
    document.getElementById('modal').classList.remove('open');
    clearInterval(timerInterval); timerInterval = null;
  }
}

function markSet(el, num) {
  el.classList.toggle('done');
  if(el.classList.contains('done')) { resetTimer(); startTimer(); }
}

function resetTimer() {
  clearInterval(timerInterval); timerInterval = null;
  timerSeconds = parseInt(document.getElementById('set-timer')?.value || state.timerDuration);
  const m = String(Math.floor(timerSeconds/60)).padStart(2,'0');
  const s = String(timerSeconds%60).padStart(2,'0');
  document.getElementById('timer').textContent = `${m}:${s}`;
  document.getElementById('timer').style.color = 'var(--green)';
}

function startTimer() {
  timerInterval = setInterval(()=>{
    timerSeconds--;
    const m = String(Math.floor(timerSeconds/60)).padStart(2,'0');
    const s = String(timerSeconds%60).padStart(2,'0');
    document.getElementById('timer').textContent = `${m}:${s}`;
    if(timerSeconds<=0){
      clearInterval(timerInterval);
      document.getElementById('timer').textContent = 'GO!';
      document.getElementById('timer').style.color = 'var(--amber)';
    }
  },1000);
}

function completeExercise() {
  const ex = state.exercises.find(e=>e.id===currentExerciseId);
  if(!ex) return;
  const painVal = parseInt(document.getElementById('exercise-pain').value);
  ex.done = true;
  state.completedTotal++;
  // Update avg pain
  const allPains = state.exercises.filter(e=>e.done).map(()=>painVal);
  state.avgPain = painVal;
  // Update week
  const today = new Date().getDay();
  const todayIdx = today===0?6:today-1;
  state.weekData[todayIdx] = true;
  // Streak
  let streak = 0;
  for(let i=todayIdx;i>=0;i--){ if(state.weekData[i]) streak++; else break; }
  state.streak = streak;
  state.daysActive = state.weekData.filter(Boolean).length;
  document.getElementById('modal').classList.remove('open');
  clearInterval(timerInterval); timerInterval = null;
  showToast('Exercise complete! 🎉');
  renderHome();
}

// ═══════════════════════════════════════
// ADD EXERCISE
// ═══════════════════════════════════════
function showAddForm() { document.getElementById('add-form').style.display='block'; }
function hideAddForm() { document.getElementById('add-form').style.display='none'; }

function addExercise() {
  const name = document.getElementById('new-name').value.trim();
  if(!name){ showToast('Please enter an exercise name'); return; }
  const newEx = {
    id: Date.now(),
    icon: document.getElementById('new-icon').value || '💪',
    title: name,
    sets: parseInt(document.getElementById('new-sets').value)||3,
    reps: parseInt(document.getElementById('new-reps').value)||12,
    part: document.getElementById('new-part').value||'General',
    diff: document.getElementById('new-diff').value,
    done: false,
  };
  state.exercises.push(newEx);
  hideAddForm();
  document.getElementById('new-name').value='';
  showToast('Exercise added! ✓');
  renderHome();
}

// ═══════════════════════════════════════
// PAIN LOGGING
// ═══════════════════════════════════════
function logPainPoint() {
  const area = document.getElementById('pain-area').value;
  const level = parseInt(document.getElementById('pain-level').value);
  const type = document.getElementById('pain-type').value;
  // Remove existing entry for same area
  state.painPoints = state.painPoints.filter(p=>p.area!==area);
  state.painPoints.push({area,level,type});
  state.avgPain = Math.round(state.painPoints.reduce((s,p)=>s+p.level,0)/state.painPoints.length);
  showToast('Pain point logged ✓');
  renderHome();
  renderPainListFull();
}

function updatePainColor(val) {
  const colors = {1:'var(--green)',2:'var(--green)',3:'var(--green)',4:'var(--amber)',5:'var(--amber)',6:'var(--amber)',7:'var(--red)',8:'var(--red)',9:'var(--red)',10:'var(--red)'};
  document.getElementById('pain-level-val').style.color = colors[val]||'var(--green)';
}

function renderPainListFull() {
  const el = document.getElementById('pain-list-full');
  if(!el) return;
  el.innerHTML = '';
  if(state.painPoints.length===0){
    el.innerHTML='<div style="text-align:center;padding:20px;color:var(--muted);font-family:var(--font-mono);font-size:0.72rem;">No pain points logged yet.</div>';
    return;
  }
  state.painPoints.forEach((p,i)=>{
    const col = p.level>=7?'var(--red)':p.level>=4?'var(--amber)':'var(--green)';
    const div = document.createElement('div');
    div.style.cssText='background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:14px;display:flex;align-items:center;justify-content:space-between;';
    div.innerHTML=`<div>
      <div style="font-weight:700;font-size:0.85rem;">${p.area}</div>
      <div style="font-size:0.62rem;font-family:var(--font-mono);color:var(--muted);margin-top:2px;">${p.type}</div>
    </div>
    <div style="display:flex;align-items:center;gap:10px;">
      <div style="font-size:1.2rem;font-weight:800;color:${col};font-family:var(--font-mono);">${p.level}/10</div>
      <button onclick="removePain(${i})" style="background:none;border:1px solid var(--border);color:var(--muted);border-radius:6px;padding:4px 8px;cursor:pointer;font-size:0.7rem;">✕</button>
    </div>`;
    el.appendChild(div);
  });
}

function removePain(idx) {
  state.painPoints.splice(idx,1);
  state.avgPain = state.painPoints.length ? Math.round(state.painPoints.reduce((s,p)=>s+p.level,0)/state.painPoints.length) : null;
  renderPainListFull();
  renderHome();
  showToast('Pain point removed');
}

// ═══════════════════════════════════════
// PROGRESS SCREEN
// ═══════════════════════════════════════
function renderProgress() {
  document.getElementById('p-completed').textContent = state.completedTotal;
  document.getElementById('p-streak').textContent = state.streak;
  document.getElementById('p-avgpain').textContent = state.avgPain !== null ? state.avgPain+'/10' : '—';
  document.getElementById('p-days').textContent = state.daysActive;
  document.getElementById('week-num').textContent = Math.ceil(state.day/7)||1;

  // Weekly bars
  const days=['Mon','Tue','Wed','Thu','Fri','Sat','Sun'];
  const wb = document.getElementById('weekly-bars');
  wb.innerHTML='';
  days.forEach((d,i)=>{
    const val = state.weekData[i] ? 100 : 0;
    wb.innerHTML+=`<div class="bar-row">
      <div class="bar-label"><span>${d}</span><span>${val}%</span></div>
      <div class="bar-track"><div class="bar-fill" style="width:${val}%"></div></div>
    </div>`;
  });

  // Pain trend
  const ptb = document.getElementById('pain-trend-bars');
  ptb.innerHTML='';
  days.forEach((d,i)=>{
    const val = state.painHistory[i];
    const pct = val ? (val/10)*100 : 0;
    const cls = val>=7?'red':val>=4?'amber':'';
    ptb.innerHTML+=`<div class="bar-row">
      <div class="bar-label"><span>${d}</span><span>${val?val+'/10':'—'}</span></div>
      <div class="bar-track"><div class="bar-fill ${cls}" style="width:${pct}%"></div></div>
    </div>`;
  });
}

// ═══════════════════════════════════════
// COACH
// ═══════════════════════════════════════
function renderCoachInsight() {
  const done = state.exercises.filter(e=>e.done).length;
  const total = state.exercises.length;
  const pain = state.avgPain;
  let msg = '';
  if(done===0) msg = `Morning, <strong>${state.name}</strong>! You have <strong>${total} exercises</strong> planned today. Start with the first one — consistency is what builds tissue. Go steady.`;
  else if(done===total) msg = `🎉 All done today, <strong>${state.name}</strong>! Incredible consistency. Recovery happens during rest now — sleep well, hydrate, and come back tomorrow.`;
  else if(pain !== null && pain >= 7) msg = `You're pushing through some real pain today (<strong>${pain}/10</strong>). Consider reducing intensity on remaining exercises by 30%. Pain above 7 is your body asking to slow down — listen to it.`;
  else msg = `You're <strong>${done}/${total}</strong> through today's session, ${state.name}. ${pain?`Pain level: <strong>${pain}/10</strong> — manageable. ` : ''}Keep going, you're building real strength.`;
  document.getElementById('daily-insight').innerHTML = msg;
}

const coachResponses = {
  rest: "If your pain is above 6/10 or you didn't sleep well, take the rest. One rest day won't set you back — pushing through the wrong pain will.",
  pain: "Some pain is normal in rehab — muscle soreness means adaptation. Sharp, sudden or joint pain is a stop signal. Track the type and intensity over days to spot patterns.",
  progress: "Recovery isn't linear. Expect good days and hard days. What matters is the weekly trend, not how you feel today.",
  exercise: "Technique over load, always. Doing 8 clean reps is far more valuable than 15 sloppy ones. Slow down and feel the muscle working.",
  sleep: "Sleep is when tissue repair peaks — growth hormone surges at night. Aim for 8 hours. Poor sleep literally slows healing.",
  default: "Stay consistent, track your pain, and trust the process. Recovery is cumulative — every session adds up even when it doesn't feel like it."
};

function askCoach() {
  const q = document.getElementById('coach-question').value.trim();
  if(!q) return;
  let answer = coachResponses.default;
  const ql = q.toLowerCase();
  if(ql.includes('rest')||ql.includes('skip')) answer = coachResponses.rest;
  else if(ql.includes('pain')||ql.includes('sore')||ql.includes('hurt')) answer = coachResponses.pain;
  else if(ql.includes('progress')||ql.includes('slow')||ql.includes('better')) answer = coachResponses.progress;
  else if(ql.includes('exercise')||ql.includes('reps')||ql.includes('form')) answer = coachResponses.exercise;
  else if(ql.includes('sleep')) answer = coachResponses.sleep;

  const responses = document.getElementById('coach-responses');
  const div = document.createElement('div');
  div.className = 'coach-response-item';
  div.innerHTML = `<div class="q">You asked: "${q}"</div>${answer}`;
  responses.insertBefore(div, responses.firstChild);
  document.getElementById('coach-question').value='';
  showToast('Coach responded ✓');
}

// ═══════════════════════════════════════
// SETTINGS
// ═══════════════════════════════════════
function updateName() { state.name = document.getElementById('set-name').value || 'Patient'; renderHome(); }
function updateDay() { state.day = parseInt(document.getElementById('set-day').value)||1; renderHome(); }
function updateTotal() { state.totalDays = parseInt(document.getElementById('set-total').value)||42; renderHome(); }
function updateInjury() { state.injury = document.getElementById('set-injury').value; }
function toggleSetting(el) { el.classList.toggle('on'); }

function applyTheme() {
  const theme = document.getElementById('set-theme').value;
  const themes = {
    dark:  { '--green':'#2dff6e','--green-dim':'#1a9943','--bg':'#0a0f0d','--surface':'#111a15','--surface2':'#162019','--border':'#1e2e23' },
    teal:  { '--green':'#00e5cc','--green-dim':'#009980','--bg':'#080f0e','--surface':'#0e1a18','--surface2':'#132220','--border':'#1a2e2b' },
    blue:  { '--green':'#38d1ff','--green-dim':'#1a8aaa','--bg':'#080c14','--surface':'#0e1420','--surface2':'#131b28','--border':'#1a2535' },
    red:   { '--green':'#ff6b6b','--green-dim':'#cc3333','--bg':'#100808','--surface':'#1a0e0e','--surface2':'#1f1212','--border':'#2e1a1a' },
  };
  const vars = themes[theme] || themes.dark;
  Object.entries(vars).forEach(([k,v])=>document.documentElement.style.setProperty(k,v));
  showToast('Theme updated ✓');
}

function resetAll() {
  if(confirm('Reset all data? This cannot be undone.')) {
    state.exercises = [];
    state.painPoints = [];
    state.streak = 0;
    state.avgPain = null;
    state.completedTotal = 0;
    state.weekData = [false,false,false,false,false,false,false];
    renderHome();
    showToast('Data reset');
  }
}

// ═══════════════════════════════════════
// TOAST
// ═══════════════════════════════════════
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(()=>t.classList.remove('show'), 2200);
}

// ═══════════════════════════════════════
// INIT
// ═══════════════════════════════════════
renderHome();
setTimeout(()=>{
  const ring = document.getElementById('ring');
  const done = state.exercises.filter(e=>e.done).length;
  const total = state.exercises.length;
  const pct = total ? Math.round((done/total)*100) : 0;
  ring.style.strokeDashoffset = 220 - (220*pct/100);
},100);
</script>
</body>
</html>
