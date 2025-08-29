<!doctype html>
<html lang="de"><head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Willkommen!</title><meta http-equiv="Cache-Control" content="no-store">
<style>
:root{--bg:#0b0f14;--card:#0f1620;--muted:#8aa0b3;--accent:#73d7ff;}
html,body{height:100%}body{margin:0;background:radial-gradient(900px 600px at 90% -10%,#132033 0%,transparent 60%),#0b0f14;
color:#e8f0f7;font:16px/1.4 system-ui,-apple-system,"Segoe UI",Roboto,Ubuntu,"Helvetica Neue",Arial;}
.wrap{min-height:100%;display:flex;align-items:center;justify-content:center;padding:24px}
.card{width:min(800px,94vw);background:linear-gradient(180deg,var(--card),#0c121a);border:1px solid #1a2634;border-radius:16px;padding:26px 28px}
h1{margin:0 0 8px;font-size:26px}h2{margin:18px 0 6px;font-size:18px;color:#cfe6ff}
.meta{color:var(--muted);font-size:14px;margin-bottom:10px}
.rule{display:flex;gap:10px;align-items:flex-start;margin:8px 0}
.dot{width:8px;height:8px;border-radius:50%;background:var(--accent);margin-top:7px;box-shadow:0 0 16px rgba(115,215,255,.5)}
.row{display:grid;grid-template-columns:1fr 1fr;gap:16px}
.box{border:1px solid #1a2634;border-radius:14px;padding:14px;background:#0c131c}
.btn{display:inline-block;border:1px solid #2a3a4f;background:#0b1320;padding:10px 14px;border-radius:10px;text-decoration:none;color:#e8f0f7}
.btn:hover{border-color:#3d5a7a}
.kbd{border:1px solid #2a3a4f;background:#0b1320;border-radius:6px;padding:2px 6px}
.foot{margin-top:14px;color:var(--muted);font-size:13px}
</style>
</head><body>
<div class="wrap"><div class="card">
  <div class="meta">Hallo <span id="nick">Spieler</span> — willkommen auf <strong id="host">TTT</strong>!</div>
  <h1>Kurzer Überblick</h1>
  <div class="row">
    <div class="box">
      <h2>Regeln</h2>
      <div class="rule"><div class="dot"></div><div>Kein RDM / Metagaming / Ghosting.</div></div>
      <div class="rule"><div class="dot"></div><div>Höflicher Umgangston, keine Beleidigungen.</div></div>
      <div class="rule"><div class="dot"></div><div>Admin-Anweisungen folgen.</div></div>
    </div>
    <div class="box">
      <h2>Quick-Keys</h2>
      <div class="rule"><div class="dot"></div><div><span class="kbd">F1</span> Hilfe/Regeln • <span class="kbd">F2</span> Shop</div></div>
      <div class="rule"><div class="dot"></div><div><span class="kbd">Tab</span> Rollenübersicht • <span class="kbd">C</span> Karma/Shop</div></div>
      <a class="btn" id="discord" href="#" target="_blank" rel="noopener">Discord beitreten</a>
    </div>
  </div>
  <div class="foot">Map: <span id="map">…</span> • Modus: <span id="gm">TTT2</span></div>
</div></div>
<script>
(function(){
  const p=new URLSearchParams(location.search);
  const safe=t=>t?String(t).replace(/[<>]/g,''):''; 
  document.getElementById('nick').textContent=safe(p.get('name')||'Spieler');
  document.getElementById('host').textContent=safe(p.get('host')||'TTT Server');
  document.getElementById('map').textContent=safe(p.get('map')||'Unbekannt');
  document.getElementById('gm').textContent=safe(p.get('gm')||'TTT2');
  const dc=document.getElementById('discord'); if(dc && p.get('discord')) dc.href=p.get('discord');
})();
</script>
</body></html>
