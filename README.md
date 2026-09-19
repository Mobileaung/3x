<!DOCTYPE html>
<html lang="my" dir="ltr" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="theme-color" content="#0b0e14">
<title>Phyo Ko VPN | User Panel</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Noto+Sans+Myanmar:wght@400;500;600;700;800&display=swap');

:root{
  --bg:#070a12;
  --card:#0e1422;
  --card2:#111a2b;
  --border:rgba(255,255,255,.09);
  --text:#f4f7ff;
  --muted:#8d9ab3;

  --blue:#38bdf8;
  --blue2:#2563eb;
  --indigo:#818cf8;

  --green:#22c55e;
  --yellow:#f59e0b;
  --red:#ef4444;

  --shadow:0 18px 50px rgba(0,0,0,.35);
  --radius:22px;
}

*{
  box-sizing:border-box;
}

html{
  scroll-behavior:smooth;
}

body{
  margin:0;
  min-height:100vh;
  font-family:
    Inter,
    "Noto Sans Myanmar",
    "Myanmar Text",
    sans-serif;
  color:var(--text);
  background:
    radial-gradient(circle at 85% -10%,rgba(37,99,235,.28),transparent 35%),
    radial-gradient(circle at -10% 30%,rgba(56,189,248,.10),transparent 30%),
    var(--bg);
  overflow-x:hidden;
}

/* ---------- GLOBAL ---------- */

button{
  font-family:inherit;
}

.container{
  width:min(1120px,100%);
  margin:auto;
  padding:18px 16px 105px;
}

.card{
  background:rgba(14,20,34,.86);
  border:1px solid var(--border);
  border-radius:var(--radius);
  box-shadow:var(--shadow);
  backdrop-filter:blur(18px);
  margin-bottom:16px;
}

.hidden{
  display:none!important;
}

/* ---------- HEADER ---------- */

.header{
  padding:14px 16px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:12px;
}

.brand{
  display:flex;
  align-items:center;
  gap:12px;
}

.logo{
  width:48px;
  height:48px;
  border-radius:16px;
  display:grid;
  place-items:center;
  background:
    linear-gradient(145deg,#2563eb,#38bdf8);
  box-shadow:
    0 8px 28px rgba(37,99,235,.38);
  font-size:23px;
  font-weight:800;
  color:white;
}

.brand h1{
  margin:0;
  font-size:16px;
  font-weight:800;
}

.brand p{
  margin:3px 0 0;
  font-size:11px;
  color:var(--muted);
}

.header-actions{
  display:flex;
  gap:8px;
}

.icon-btn{
  width:42px;
  height:42px;
  border:1px solid var(--border);
  border-radius:13px;
  background:#0d1422;
  color:white;
  cursor:pointer;
  font-size:17px;
}

/* ---------- PROFILE ---------- */

.profile{
  padding:22px;
}

.profile-top{
  display:flex;
  align-items:center;
  gap:15px;
}

.avatar{
  width:64px;
  height:64px;
  border-radius:50%;
  display:grid;
  place-items:center;
  background:linear-gradient(145deg,#2563eb,#818cf8);
  font-size:23px;
  font-weight:800;
  box-shadow:0 10px 28px rgba(37,99,235,.35);
}

.profile-info{
  flex:1;
  min-width:0;
}

.username{
  margin:0;
  font-size:21px;
  font-weight:800;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
}

.email{
  margin:4px 0 0;
  color:var(--muted);
  font-size:12px;
}

.status{
  display:inline-flex;
  align-items:center;
  gap:6px;
  margin-top:9px;
  padding:6px 10px;
  border-radius:999px;
  background:rgba(34,197,94,.10);
  color:var(--green);
  border:1px solid rgba(34,197,94,.25);
  font-size:11px;
  font-weight:700;
}

.status-dot{
  width:7px;
  height:7px;
  border-radius:50%;
  background:var(--green);
  box-shadow:0 0 9px var(--green);
}

.profile-actions{
  display:flex;
  gap:8px;
  margin-top:18px;
  flex-wrap:wrap;
}

.btn{
  border:1px solid var(--border);
  background:#101827;
  color:white;
  border-radius:13px;
  padding:10px 15px;
  cursor:pointer;
  font-size:12px;
  font-weight:700;
}

.btn.primary{
  border:0;
  background:linear-gradient(135deg,#2563eb,#38bdf8);
  box-shadow:0 7px 20px rgba(37,99,235,.25);
}

/* ---------- HERO ---------- */

.hero-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:12px;
}

.hero{
  padding:20px;
  min-height:135px;
  position:relative;
  overflow:hidden;
}

.hero::after{
  content:"";
  position:absolute;
  width:170px;
  height:170px;
  right:-65px;
  top:-70px;
  border-radius:50%;
  background:rgba(56,189,248,.10);
}

.label{
  color:var(--muted);
  font-size:12px;
  font-weight:600;
}

.big{
  margin-top:10px;
  font-size:27px;
  font-weight:800;
}

.blue{
  color:var(--blue);
}

.small{
  margin-top:5px;
  color:var(--muted);
  font-size:11px;
}

/* ---------- USAGE ---------- */

.section{
  padding:20px;
}

.section-title{
  display:flex;
  align-items:center;
  justify-content:space-between;
  margin-bottom:16px;
}

.section-title h2{
  margin:0;
  font-size:16px;
}

.section-title span{
  color:var(--muted);
  font-size:11px;
}

.usage-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:12px;
}

.usage{
  padding:18px;
  border-radius:18px;
  background:#101827;
  border:1px solid var(--border);
}

.usage-head{
  display:flex;
  justify-content:space-between;
  font-size:12px;
  color:var(--muted);
}

.progress{
  height:8px;
  background:#1a2435;
  border-radius:99px;
  margin-top:13px;
  overflow:hidden;
}

.progress i{
  display:block;
  height:100%;
  border-radius:99px;
  background:linear-gradient(90deg,#2563eb,#38bdf8);
}

.usage-value{
  margin-top:10px;
  font-size:15px;
  font-weight:800;
}

/* ---------- STATS ---------- */

.stats{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:10px;
}

.stat{
  padding:16px;
  border-radius:17px;
  background:#101827;
  border:1px solid var(--border);
}

.stat-icon{
  width:34px;
  height:34px;
  border-radius:11px;
  display:grid;
  place-items:center;
  background:rgba(56,189,248,.10);
  color:var(--blue);
  font-size:16px;
}

.stat-label{
  margin-top:11px;
  color:var(--muted);
  font-size:11px;
}

.stat-value{
  margin-top:5px;
  font-size:15px;
  font-weight:800;
}

/* ---------- SERVER ---------- */

.server-list{
  display:flex;
  flex-direction:column;
  gap:9px;
}

.server{
  padding:14px;
  border:1px solid var(--border);
  border-radius:17px;
  background:#101827;
  display:flex;
  align-items:center;
  gap:12px;
}

.server-icon{
  width:43px;
  height:43px;
  border-radius:13px;
  display:grid;
  place-items:center;
  background:rgba(37,99,235,.13);
  font-size:21px;
}

.server-info{
  flex:1;
  min-width:0;
}

.server-name{
  font-size:13px;
  font-weight:800;
}

.server-location{
  color:var(--muted);
  font-size:10px;
  margin-top:4px;
}

.ping{
  font-size:11px;
  font-weight:700;
  color:var(--green);
}

/* ---------- CONFIG ---------- */

.config{
  padding:15px;
  border-radius:17px;
  background:#101827;
  border:1px solid var(--border);
  margin-bottom:9px;
}

.config-top{
  display:flex;
  justify-content:space-between;
  gap:10px;
}

.config-name{
  font-size:13px;
  font-weight:800;
}

.badge{
  padding:5px 8px;
  border-radius:8px;
  font-size:9px;
  font-weight:700;
  color:var(--green);
  background:rgba(34,197,94,.10);
}

.config-code{
  margin-top:10px;
  padding:11px;
  background:#080d17;
  border-radius:11px;
  color:#8fb8ff;
  font-family:monospace;
  font-size:10px;
  word-break:break-all;
  border:1px solid rgba(255,255,255,.05);
}

.copy{
  width:100%;
  margin-top:9px;
  padding:10px;
  border:0;
  border-radius:11px;
  background:#17243a;
  color:white;
  cursor:pointer;
  font-size:11px;
  font-weight:700;
}

/* ---------- APPS ---------- */

.apps{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:10px;
}

.app{
  padding:18px 10px;
  text-align:center;
  border:1px solid var(--border);
  background:#101827;
  border-radius:17px;
}

.app-icon{
  font-size:27px;
}

.app-name{
  margin-top:8px;
  font-size:12px;
  font-weight:700;
}

.app button{
  margin-top:10px;
  padding:7px 12px;
  border:0;
  border-radius:9px;
  background:#17243a;
  color:white;
  font-size:10px;
  cursor:pointer;
}

/* ---------- BOTTOM NAV ---------- */

.bottom-nav{
  position:fixed;
  z-index:100;
  left:50%;
  bottom:15px;
  transform:translateX(-50%);
  width:min(560px,calc(100% - 24px));
  padding:8px;
  border:1px solid rgba(56,189,248,.14);
  border-radius:22px;
  background:rgba(10,15,27,.94);
  backdrop-filter:blur(20px);
  box-shadow:0 15px 45px rgba(0,0,0,.45);
  display:grid;
  grid-template-columns:repeat(3,1fr);
}

.nav-btn{
  border:0;
  background:transparent;
  color:#71809b;
  padding:9px 5px;
  border-radius:15px;
  cursor:pointer;
  font-family:inherit;
}

.nav-btn .nav-icon{
  display:block;
  font-size:18px;
}

.nav-btn span:last-child{
  display:block;
  margin-top:3px;
  font-size:9px;
}

.nav-btn.active{
  color:white;
  background:linear-gradient(135deg,rgba(37,99,235,.75),rgba(56,189,248,.25));
}

/* ---------- VIEW ---------- */

.view{
  display:none;
  animation:fade .25s ease;
}

.view.active{
  display:block;
}

@keyframes fade{
  from{
    opacity:0;
    transform:translateY(7px);
  }
  to{
    opacity:1;
    transform:none;
  }
}

/* ---------- RESPONSIVE ---------- */

@media(max-width:700px){

  .stats{
    grid-template-columns:1fr 1fr;
  }

  .apps{
    grid-template-columns:1fr 1fr 1fr;
  }
}

@media(max-width:520px){

  .container{
    padding-left:12px;
    padding-right:12px;
  }

  .hero-grid{
    grid-template-columns:1fr;
  }

  .usage-grid{
    grid-template-columns:1fr;
  }

  .profile{
    padding:17px;
  }

  .section{
    padding:17px;
  }

  .big{
    font-size:25px;
  }
}
</style>
</head>

<body>

<div class="container">

  <!-- HEADER -->
  <header class="card header">

    <div class="brand">

      <div class="logo">
        PK
      </div>

      <div>
        <h1>Phyo Ko VPN</h1>
        <p>Secure VPN User Panel</p>
      </div>

    </div>

    <div class="header-actions">

      <button class="icon-btn" onclick="toggleTheme()" title="Theme">
        ☀️
      </button>

      <button class="icon-btn" onclick="showNotice()" title="Notification">
        🔔
      </button>

    </div>

  </header>


  <!-- ACCOUNT VIEW -->

  <main id="accountView" class="view active">

    <!-- PROFILE -->

    <section class="card profile">

      <div class="profile-top">

        <div class="avatar">
          PK
        </div>

        <div class="profile-info">

          <h2 class="username">
            Phyo Ko User
          </h2>

          <p class="email">
            user@phyoko.vpn
          </p>

          <div class="status">
            <span class="status-dot"></span>
            Active / အသုံးပြုနေသည်
          </div>

        </div>

      </div>

      <div class="profile-actions">

        <button class="btn primary" onclick="copyUser()">
          📋 Copy ID
        </button>

        <button class="btn" onclick="showNotice()">
          💬 Support / အကူအညီ
        </button>

      </div>

    </section>


    <!-- HERO -->

    <div class="hero-grid">

      <section class="card hero">

        <div class="label">
          Current Time / လက်ရှိအချိန်
        </div>

        <div class="big blue" id="clock">
          00:00:00
        </div>

        <div class="small" id="date">
          Loading...
        </div>

      </section>


      <section class="card hero">

        <div class="label">
          Expiry Date / သက်တမ်းကုန်ဆုံးရက်
        </div>

        <div class="big">
          31 Dec 2026
        </div>

        <div class="small">
          One Year Plan / တစ်နှစ်စာ
        </div>

      </section>

    </div>


    <!-- USAGE -->

    <section class="card section">

      <div class="section-title">

        <div>
          <h2>Traffic Usage</h2>
          <span>ဒေတာအသုံးပြုမှု</span>
        </div>

        <span>Monthly / လစဉ်</span>

      </div>

      <div class="usage-grid">

        <div class="usage">

          <div class="usage-head">
            <span>Download</span>
            <span>65%</span>
          </div>

          <div class="progress">
            <i style="width:65%"></i>
          </div>

          <div class="usage-value">
            65 GB
          </div>

        </div>


        <div class="usage">

          <div class="usage-head">
            <span>Upload</span>
            <span>35%</span>
          </div>

          <div class="progress">
            <i style="width:35%"></i>
          </div>

          <div class="usage-value">
            35 GB
          </div>

        </div>

      </div>

    </section>


    <!-- STATISTICS -->

    <section class="card section">

      <div class="section-title">

        <div>
          <h2>Account Overview</h2>
          <span>အကောင့်အချက်အလက်</span>
        </div>

      </div>

      <div class="stats">

        <div class="stat">
          <div class="stat-icon">🌐</div>
          <div class="stat-label">Total Traffic</div>
          <div class="stat-value">100 GB</div>
        </div>

        <div class="stat">
          <div class="stat-icon">⏱️</div>
          <div class="stat-label">Remaining</div>
          <div class="stat-value">103 Days</div>
        </div>

        <div class="stat">
          <div class="stat-icon">📱</div>
          <div class="stat-label">Devices</div>
          <div class="stat-value">3 Devices</div>
        </div>

        <div class="stat">
          <div class="stat-icon">🟢</div>
          <div class="stat-label">Status</div>
          <div class="stat-value">Active</div>
        </div>

      </div>

    </section>


    <!-- SERVER -->

    <section class="card section">

      <div class="section-title">

        <div>
          <h2>VPN Servers</h2>
          <span>ချိတ်ဆက်နိုင်သော Server များ</span>
        </div>

      </div>

      <div class="server-list">

        <div class="server">

          <div class="server-icon">
            🇲🇲
          </div>

          <div class="server-info">

            <div class="server-name">
              Myanmar Server
            </div>

            <div class="server-location">
              Myanmar Region
            </div>

          </div>

          <div class="ping">
            32 ms
          </div>

        </div>


        <div class="server">

          <div class="server-icon">
            🇸🇬
          </div>

          <div class="server-info">

            <div class="server-name">
              Singapore Server
            </div>

            <div class="server-location">
              Singapore Region
            </div>

          </div>

          <div class="ping">
            58 ms
          </div>

        </div>


        <div class="server">

          <div class="server-icon">
            🇭🇰
          </div>

          <div class="server-info">

            <div class="server-name">
              Hong Kong Server
            </div>

            <div class="server-location">
              Hong Kong Region
            </div>

          </div>

          <div class="ping">
            74 ms
          </div>

        </div>

      </div>

    </section>

  </main>


  <!-- CONFIG VIEW -->

  <main id="configView" class="view">

    <section class="card section">

      <div class="section-title">

        <div>
          <h2>VPN Configurations</h2>
          <span>VPN ချိတ်ဆက်ရန် Config များ</span>
        </div>

      </div>


      <div class="config">

        <div class="config-top">

          <div class="config-name">
            🇲🇲 Myanmar Reality
          </div>

          <div class="badge">
            ACTIVE
          </div>

        </div>

        <div class="config-code" id="config1">
          vless://example-user@server.example.com:443
        </div>

        <button class="copy" onclick="copyConfig('config1',this)">
          📋 Copy Configuration
        </button>

      </div>


      <div class="config">

        <div class="config-top">

          <div class="config-name">
            🇸🇬 Singapore Reality
          </div>

          <div class="badge">
            ACTIVE
          </div>

        </div>

        <div class="config-code" id="config2">
          vless://example-user@sg.example.com:443
        </div>

        <button class="copy" onclick="copyConfig('config2',this)">
          📋 Copy Configuration
        </button>

      </div>


      <div class="config">

        <div class="config-top">

          <div class="config-name">
            🇭🇰 Hong Kong Reality
          </div>

          <div class="badge">
            ACTIVE
          </div>

        </div>

        <div class="config-code" id="config3">
          vless://example-user@hk.example.com:443
        </div>

        <button class="copy" onclick="copyConfig('config3',this)">
          📋 Copy Configuration
        </button>

      </div>

    </section>

  </main>


  <!-- APPS VIEW -->

  <main id="appsView" class="view">

    <section class="card section">

      <div class="section-title">

        <div>
          <h2>VPN Apps</h2>
          <span>အသုံးပြုနိုင်သော Application များ</span>
        </div>

      </div>


      <div class="apps">

        <div class="app">

          <div class="app-icon">🤖</div>

          <div class="app-name">
            Android
          </div>

          <button onclick="showNotice()">
            Download
          </button>

        </div>


        <div class="app">

          <div class="app-icon">🍎</div>

          <div class="app-name">
            iOS
          </div>

          <button onclick="showNotice()">
            Download
          </button>

        </div>


        <div class="app">

          <div class="app-icon">🪟</div>

          <div class="app-name">
            Windows
          </div>

          <button onclick="showNotice()">
            Download
          </button>

        </div>


        <div class="app">

          <div class="app-icon">💻</div>

          <div class="app-name">
            macOS
          </div>

          <button onclick="showNotice()">
            Download
          </button>

        </div>


        <div class="app">

          <div class="app-icon">📱</div>

          <div class="app-name">
            Clash Meta
          </div>

          <button onclick="showNotice()">
            Download
          </button>

        </div>


        <div class="app">

          <div class="app-icon">🛡️</div>

          <div class="app-name">
            Hiddify
          </div>

          <button onclick="showNotice()">
            Download
          </button>

        </div>

      </div>

    </section>

  </main>

</div>


<!-- BOTTOM NAV -->

<nav class="bottom-nav">

  <button class="nav-btn active" onclick="changeView('account',this)">
    <span class="nav-icon">👤</span>
    <span>Account / အကောင့်</span>
  </button>

  <button class="nav-btn" onclick="changeView('config',this)">
    <span class="nav-icon">🔐</span>
    <span>Config / ချိတ်ဆက်ရန်</span>
  </button>

  <button class="nav-btn" onclick="changeView('apps',this)">
    <span class="nav-icon">📱</span>
    <span>Apps / App များ</span>
  </button>

</nav>


<script>

/* ---------- CLOCK ---------- */

function updateClock(){

  const now = new Date();

  const time =
    now.toLocaleTimeString('en-GB',{
      hour12:false
    });

  const date =
    now.toLocaleDateString('en-GB',{
      weekday:'short',
      day:'2-digit',
      month:'short',
      year:'numeric'
    });

  document.getElementById('clock').textContent = time;
  document.getElementById('date').textContent = date;
}

updateClock();
setInterval(updateClock,1000);


/* ---------- NAVIGATION ---------- */

function changeView(view,button){

  document
    .querySelectorAll('.view')
    .forEach(v => v.classList.remove('active'));

  document
    .querySelectorAll('.nav-btn')
    .forEach(b => b.classList.remove('active'));

  document
    .getElementById(view + 'View')
    .classList.add('active');

  button.classList.add('active');

  window.scrollTo({
    top:0,
    behavior:'smooth'
  });
}


/* ---------- THEME ---------- */

function toggleTheme(){

  const body = document.body;

  if(body.dataset.theme === 'light'){

    body.dataset.theme = 'dark';

    document.documentElement.style.setProperty(
      '--bg',
      '#070a12'
    );

  }else{

    body.dataset.theme = 'light';

    document.documentElement.style.setProperty(
      '--bg',
      '#eaf1fb'
    );

  }

}


/* ---------- COPY CONFIG ---------- */

function copyConfig(id,button){

  const text =
    document.getElementById(id).textContent.trim();

  navigator.clipboard.writeText(text)
    .then(()=>{

      const old = button.textContent;

      button.textContent =
        '✓ Copied / ကူးယူပြီးပါပြီ';

      setTimeout(()=>{
        button.textContent = old;
      },1500);

    });

}


/* ---------- COPY USER ID ---------- */

function copyUser(){

  navigator.clipboard.writeText(
    'PHYOKO-USER-001'
  );

  showNotice('User ID copied / User ID ကူးယူပြီးပါပြီ');
}


/* ---------- NOTICE ---------- */

function showNotice(message){

  if(!message){
    message =
      'Support is available 24/7 / အကူအညီ ၂၄ နာရီ ရရှိနိုင်ပါသည်။';
  }

  const box = document.createElement('div');

  box.textContent = message;

  box.style.position = 'fixed';
  box.style.left = '50%';
  box.style.bottom = '95px';
  box.style.transform = 'translateX(-50%)';
  box.style.padding = '12px 18px';
  box.style.borderRadius = '13px';
  box.style.background = '#111a2b';
  box.style.border = '1px solid rgba(56,189,248,.25)';
  box.style.color = '#f4f7ff';
  box.style.fontSize = '12px';
  box.style.zIndex = '9999';
  box.style.boxShadow = '0 12px 35px rgba(0,0,0,.4)';
  box.style.whiteSpace = 'nowrap';

  document.body.appendChild(box);

  setTimeout(()=>{
    box.remove();
  },2200);
}

</script>

</body>
</html>
