# Extending Royal Legacy 
<AwoSwamiG@gmail.com>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="theme-color" content="#0b0b0f" />
  <meta name="color-scheme" content="dark" />
  <title>SwamiG Institute 70-888-Swami — Ifá • Isésé • Orisha | Spiritual Education, Initiation & Divination</title>
  <meta name="description" content="SwamiG Institute offers Ifá / Isésé / Orisha education, divination, rites of passage, and priesthood preparation. Michigan nonprofit — 501(c)(3) recognition pending" />
  <style>
    :root{--bg:#0b0b0f;--ink:#eaeaf2;--muted:#b5b5c4;--accent:#bb66ff;--radius:20px}
    *{box-sizing:border-box}
    html,body{scroll-behavior:smooth}
    body{margin:0;font:400 16px/1.55 system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;background:var(--bg);color:var(--ink)}

    /* Accessibility + reduced motion */
    :focus-visible{outline:2px solid var(--accent);outline-offset:3px;border-radius:8px}
    @media (prefers-reduced-motion:reduce){
      .top-card,.card,.btn.pulse{transition:none!important;animation:none!important}
    }

    /* Top notice */
    .noticebar{width:100%;text-align:center;font-size:12px;color:#d9c6ff;background:rgba(187,102,255,.12);border-bottom:1px solid rgba(187,102,255,.25);padding:6px 10px}

    /* Top Cards (now non-clickable) */
    .top-cards-wrap{background:rgba(11,11,15,.85);border-bottom:1px solid rgba(255,255,255,.08)}
    .top-cards{max-width:1100px;margin:0 auto;padding:16px 20px;display:grid;gap:16px}
    @media(min-width:900px){.top-cards{grid-template-columns:repeat(auto-fit,minmax(170px,1fr))}}
    @media(max-width:899px){.top-cards{grid-template-columns:1fr 1fr}}
    .top-card,.grid .card{position:relative;border-radius:16px;padding:16px;border:1px solid rgba(255,255,255,.12);color:var(--ink);background:linear-gradient(145deg,rgba(30,30,40,.95),rgba(18,18,25,.95));box-shadow:0 2px 6px rgba(0,0,0,.35);transition:transform .25s ease,box-shadow .25s ease,border-color .25s ease}
    .top-card{cursor:default} /* no click */
    .top-card:hover,.grid .card:hover{transform:translateY(-6px) scale(1.03);border-color:rgba(255,255,255,.22)}
    .top-card h3,.card h3{margin:0 0 8px;font:700 20px/1.2 system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif}
    .top-card p,.card p{margin:0 0 12px;color:var(--muted);font-size:14px}

    /* Lightweight accent glows on hover (visual only) */
    .top-cards .top-card:nth-child(1):hover,.grid .card#divination:hover{box-shadow:0 0 18px rgba(187,102,255,.55)}
    .top-cards .top-card:nth-child(2):hover,.grid .card#ilekes:hover{box-shadow:0 0 18px rgba(102,187,255,.50)}
    .top-cards .top-card:nth-child(3):hover,.grid .card#warriors:hover{box-shadow:0 0 18px rgba(255,102,187,.50)}
    .top-cards .top-card:nth-child(4):hover,.grid .card#hand-of-ifa:hover{box-shadow:0 0 18px rgba(187,255,102,.50)}
    .top-cards .top-card:nth-child(5):hover,.grid .card#orisha-initiation:hover{box-shadow:0 0 18px rgba(255,187,102,.50)}

    /* Layout */
    .wrap{max-width:1100px;margin:auto;padding:24px 20px}

    /* Hero (centered) */
    .hero{display:flex;flex-direction:column;align-items:center;text-align:center;margin:30px 0 34px}
    .logo{width:176px;height:176px;border-radius:50%;overflow:hidden;display:grid;place-items:center;border:1px solid rgba(255,255,255,.1);box-shadow:0 0 12px rgba(187,102,255,.30);margin-bottom:18px}
    h1{margin:0;font-weight:800;font-size:44px;line-height:1.08;letter-spacing:.3px}
    @media(min-width:960px){h1{font-size:48px}}
    .tag{color:var(--muted);font-size:16px;margin-top:10px}
    .badge{margin-top:10px;font-size:13px;color:#f4d3ff}
    .actions{margin-top:16px;display:flex;flex-wrap:wrap;gap:12px;justify-content:center}

    .callout{background:linear-gradient(180deg,rgba(187,102,255,.10),rgba(187,102,255,.04));border:1px solid rgba(187,102,255,.35);border-radius:var(--radius);padding:18px 16px}

    .grid{display:grid;gap:18px;margin-top:20px}
    @media(min-width:880px){.grid{grid-template-columns:repeat(3,1fr)}}

    .btn{border:0;border-radius:12px;padding:10px 14px;font-weight:700;text-decoration:none;display:inline-flex;align-items:center;gap:8px;cursor:pointer}
    .primary{background:var(--accent);color:#120724}
    .ghost{border:1px solid rgba(255,255,255,.25);background:transparent;color:var(--ink)}

    /* Footer */
    .footer{display:flex;flex-wrap:wrap;gap:12px;justify-content:space-between;align-items:center;border-top:1px dashed rgba(255,255,255,.15);padding-top:16px;margin-top:28px;color:var(--muted)}
    .small{font-size:12px;color:var(--muted)}
    .quote{font-style:italic;color:var(--muted)}

    /* Micro note (barely visible) */
    .micro-note{font-size:9px;color:rgba(200,180,255,.22);text-align:center;margin:8px 0 14px}

    /* Gentle CTA pulse */
    @keyframes pulseGlow{0%{box-shadow:0 0 10px rgba(187,102,255,.35)}50%{box-shadow:0 0 22px rgba(187,102,255,.7)}100%{box-shadow:0 0 10px rgba(187,102,255,.35)}}
    .grid .card#divination{animation:pulseGlow 4s ease-in-out infinite}
    .grid .card#divination .btn.primary,.actions .btn.primary.pulse{animation:pulseGlow 3s ease-in-out infinite}
  </style>
  <script>
    // Load Calendly on demand only (keeps page fast)
    function openCalendly(url){
      if(!window.__calendlyLoaded){
        const l=document.createElement('link'); l.rel='stylesheet'; l.href='https://assets.calendly.com/assets/external/widget.css';
        const s=document.createElement('script'); s.async=true; s.src='https://assets.calendly.com/assets/external/widget.js';
        s.onload=function(){ window.__calendlyLoaded=true; Calendly.initPopupWidget({url}); };
        document.head.appendChild(l); document.head.appendChild(s);
      }else{
        Calendly.initPopupWidget({url});
      }
      return false;
    }
  </script>
</head>
<body>
  <div class="noticebar">Call <strong>70-888-Swami</strong> • Michigan nonprofit — 501(c)(3) recognition pending</div>

  <!-- Top Cards (non-clickable) -->
  <div class="top-cards-wrap">
    <div class="top-cards" aria-label="Quick actions">
      <div class="top-card"><h3>1 — Divination</h3><p>How to Divine classes w/ assignments</p></div>
      <div class="top-card"><h3>2 — Ilekes</h3><p>Coursework, rituals, consecrated beads & support</p></div>
      <div class="top-card"><h3>3 — Warriors</h3><p>È&#7779;ù • Ògún • Ò&#7779;óòsì • Ò&#7779;un</p></div>
      <div class="top-card"><h3>4 — Hand of Ifá</h3><p>Ìkín consecration / Ì&#7779;&#7865;&#768;&#7779;e</p></div>
      <div class="top-card"><h3>5 — Orisha Initiation</h3><p>Full consecration & training</p></div>
    </div>
  </div>

  <div class="wrap">
    <!-- HERO -->
    <div class="hero">
      <div class="logo">
        <img src="SwamiG.gif" alt="SwamiG logo" width="176" height="176" loading="lazy" decoding="async" fetchpriority="high" />
      </div>
      <h1>SwamiG Institute</h1>
      <div class="tag">Ifá • Isésé • Orisha — Spiritual Education, Rites & Divination</div>
      <div class="badge">Michigan nonprofit • <strong>501(c)(3) recognition pending — $DrSwamiG</strong></div>
      <div class="actions">
        <a class="btn primary pulse" href="#" onclick="return openCalendly('https://calendly.com/awoswamig/30min');">See SwamiG</a>
        <a class="btn ghost" href="mailto:AwoSwamiG@gmail.com">Email Us</a>
      </div>
    </div>

    <!-- MISSION -->
    <section class="callout" aria-labelledby="mission">
      <strong id="mission">Our Mission</strong>
      <p>The mission of SwamiG Institute is to provide lesson plans, agendas, and learning modules for spiritual seekers and groups of the uninitiated, grounded in two principles:</p>
      <ul style="margin:8px 0 0 18px;color:var(--muted)">
        <li><em>Extending Royal Legacy</em></li>
        <li><em>On the shoulders of Enlightened ancestors</em></li>
      </ul>
    </section>

    <!-- OFFERINGS -->
    <section class="grid" aria-label="Offerings">
      <article class="card" id="divination" aria-labelledby="divination-title">
        <h3 id="divination-title">Spiritual Divination Session</h3>
        <p>30–60 minute Ifá divination with actionable guidance and written follow-up notes.</p>
        <div class="btns">
          <a class="btn primary" href="#" onclick="return openCalendly('https://calendly.com/awoswamig/30min');">Schedule</a>
          <a class="btn ghost" href="https://www.paypal.com/ncp/payment/5M949GKNMDHJN" target="_blank" rel="noopener">Pay</a>
        </div>
      </article>

      <article class="card" id="ilekes" aria-labelledby="ilekes-title">
        <h3 id="ilekes-title">Ilekes <em>(Authentic Self)</em></h3>
        <p>Consecrated ilekes prepared according to lineage practice. Includes orientation + debriefing.</p>
        <div class="btns">
          <a class="btn primary" href="#" onclick="return openCalendly('https://calendly.com/awoswamig/30min');">Book</a>
          <a class="btn ghost" href="https://www.paypal.com/ncp/payment/5M949GKNMDHJN" target="_blank" rel="noopener">Pay</a>
        </div>
      </article>

      <article class="card" id="warriors" aria-labelledby="warriors-title">
        <h3 id="warriors-title">Warrior Set <em>(Ancestral Cleansing)</em></h3>
        <p>Consecration and instruction for daily veneration. Includes safety & care guide, plus mentoring.</p>
        <div class="btns">
          <a class="btn primary" href="#" onclick="return openCalendly('https://calendly.com/awoswamig/30min');">Book</a>
          <a class="btn ghost" href="https://www.paypal.com/ncp/payment/5M949GKNMDHJN" target="_blank" rel="noopener">Pay</a>
        </div>
      </article>

      <article class="card" id="hand-of-ifa" aria-labelledby="hand-title">
        <h3 id="hand-title">Hand of Ifá <em>(Animating Deity Within)</em></h3>
        <p>Foundational rite conferring Odu guidance, taboos, and prescriptions.</p>
        <div class="btns">
          <a class="btn primary" href="#" onclick="return openCalendly('https://calendly.com/awoswamig/30min');">Book</a>
          <a class="btn ghost" href="mailto:AwoSwamiG@gmail.com">Ask</a>
        </div>
      </article>

      <article class="card" id="orisha-initiation" aria-labelledby="orisha-title">
        <h3 id="orisha-title">Orisha Initiation</h3>
        <p>Comprehensive initiation rites into Òrì&#7779;à tradition. Includes interviews, preparation, and mentorship.</p>
        <div class="btns">
          <a class="btn primary" href="#" onclick="return openCalendly('https://calendly.com/awoswamig/30min');">Apply</a>
          <a class="btn ghost" href="mailto:AwoSwamiG@gmail.com">Ask a Question</a>
        </div>
      </article>
    </section>

    <!-- FOOTER -->
    <section class="footer">
      <div>
        <div class="quote">“Extending Royal Legacy. On the shoulders of enlightened ancestors.”</div>
        <div class="small">© 2025 SwamiG Institute • SwamiGInstitute.com • <a href="mailto:AwoSwamiG@gmail.com">AwoSwamiG@gmail.com</a></div>
      </div>
    </section>

    <div class="micro-note">
      Governered by [Herukhuti(+)/Het Heru(-)] / [Ogbe/Okanran(+) Sebek(Ogbe)]
    </div>
  </div>
</body>
</html>
