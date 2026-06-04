<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hulunbuir & Shenyang · Aug 2025</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,600;0,700;1,600&family=Jost:wght@300;400;500&family=DM+Mono:wght@400&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#faf7f2;
  --surface:#ffffff;
  --surface2:#f2ede4;
  --ink:#1a1610;
  --ink2:#38322a;
  --ink3:#7a7060;
  --border:#ddd4c4;
  --border2:#ccc0b0;
  --gold:#b8822a;
  --gold-light:#d4a44e;
  --gold-pale:#f5e8cc;
  --food-accent:#b86020;
  --food-pale:#f8ede4;
}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--ink);font-family:'Jost',sans-serif;font-weight:400;line-height:1.65;overflow-x:hidden}
 
/* ── HERO ─────────────────────────────── */
.hero{
  position:relative;overflow:hidden;
  padding:90px 60px 72px;
  min-height:440px;
  display:flex;flex-direction:column;justify-content:flex-end;
  background:linear-gradient(155deg,#141c12 0%,#1a2818 45%,#1e1e28 100%);
}
.hero::before{
  content:'';position:absolute;inset:0;
  background:
    radial-gradient(ellipse 60% 50% at 90% 10%,#4aaa6818 0%,transparent 65%),
    radial-gradient(ellipse 40% 60% at 5% 90%,#2a7a7a14 0%,transparent 55%);
}
.hero-hills{position:absolute;bottom:0;left:0;right:0;height:200px;opacity:.2;z-index:0}
.hero-content{position:relative;z-index:1;max-width:700px}
.hero-eyebrow{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:4px;color:#7acc90;text-transform:uppercase;margin-bottom:18px;opacity:0;animation:fup .7s .1s ease forwards}
.hero h1{font-family:'Cormorant Garamond',serif;font-size:clamp(46px,7vw,84px);font-weight:700;line-height:.95;color:#f0ece4;margin-bottom:14px;opacity:0;animation:fup .7s .25s ease forwards}
.hero h1 em{font-style:italic;color:#7acc90;display:block}
.hero h1 span{color:#c8a060}
.hero-sub{font-size:14.5px;color:#8a9888;margin-bottom:28px;opacity:0;animation:fup .7s .4s ease forwards}
.hero-pills{display:flex;gap:8px;flex-wrap:wrap;opacity:0;animation:fup .7s .55s ease forwards}
.hp{background:#ffffff0c;border:1px solid #ffffff14;border-radius:3px;padding:5px 13px;font-size:12px;color:#b8c8b0;font-weight:400}
.hp b{color:#dde8d8;font-weight:500}
 
/* Flight banner */
.flt-bar{background:var(--surface);border-bottom:1px solid var(--border);display:grid;grid-template-columns:1fr 40px 1fr;opacity:0;animation:fup .7s .7s ease forwards}
.flt-side{padding:20px 56px}
.flt-side.r{text-align:right;border-left:1px solid var(--border)}
.flt-lbl{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:3px;color:var(--ink3);text-transform:uppercase;margin-bottom:4px}
.flt-rt{font-family:'Cormorant Garamond',serif;font-size:28px;font-weight:700;color:var(--gold);letter-spacing:2px}
.flt-dt{font-size:12.5px;color:var(--ink3);margin-top:2px}
.flt-mid{display:flex;flex-direction:column;align-items:center;justify-content:center;color:var(--gold);font-size:15px}
.flt-vl{flex:1;width:1px;background:linear-gradient(transparent,var(--gold-pale),transparent)}
 
@media(max-width:600px){
  .hero{padding:64px 22px 52px}
  .flt-side{padding:16px 20px}
  .flt-bar{grid-template-columns:1fr 32px 1fr}
}
 
/* ── MAIN ─────────────────────────────── */
.main{max-width:880px;margin:0 auto;padding:64px 40px 120px}
@media(max-width:640px){.main{padding:40px 18px 80px}}
 
.sec-head{display:flex;align-items:center;gap:16px;margin-bottom:32px}
.sec-lbl{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:4px;color:var(--gold);text-transform:uppercase;white-space:nowrap}
.sec-line{flex:1;height:1px;background:var(--border2)}
 
/* Legend */
.legend{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:44px}
.leg-item{display:flex;align-items:center;gap:6px;font-size:12px;color:var(--ink3);padding:3px 10px 3px 8px;border:1px solid var(--border);border-radius:20px;background:var(--surface)}
.leg-dot{width:7px;height:7px;border-radius:50%;flex-shrink:0}
 
/* ── DAY CARDS (no timeline) ──────────── */
.days-stack{display:flex;flex-direction:column;gap:10px}
 
.day{opacity:0;transform:translateY(12px);transition:opacity .5s ease,transform .5s ease}
.day.vis{opacity:1;transform:none}
 
/* Card */
.card{
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:12px;
  overflow:hidden;
  transition:border-color .25s,box-shadow .25s;
}
.card:hover{
  border-color:color-mix(in srgb,var(--zc,var(--gold)) 50%,transparent);
  box-shadow:0 4px 24px rgba(0,0,0,.07);
}
.z-bar{height:4px;background:linear-gradient(90deg,var(--zc,var(--gold)),var(--zc-pale,var(--gold-pale)))}
 
/* Card header */
.card-hd{display:flex;align-items:stretch;cursor:pointer;user-select:none}
 
.badge{
  width:68px;flex-shrink:0;
  background:var(--zc-pale,var(--gold-pale));
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  gap:1px;border-right:1px solid var(--border);padding:14px 6px;
}
.badge-n{font-family:'Cormorant Garamond',serif;font-size:32px;font-weight:700;color:var(--zc,var(--gold));line-height:1}
.badge-m{font-family:'DM Mono',monospace;font-size:8px;letter-spacing:2px;color:var(--zc,var(--gold));opacity:.65;text-transform:uppercase}
 
.card-info{flex:1;padding:15px 20px}
.card-title{font-family:'Cormorant Garamond',serif;font-size:19px;font-weight:700;color:var(--ink);margin-bottom:3px;line-height:1.25}
.card-loc{font-size:12px;color:var(--ink3);margin-bottom:10px}
 
.tags{display:flex;flex-wrap:wrap;gap:5px}
.tag{font-size:11px;font-family:'DM Mono',monospace;letter-spacing:.3px;padding:2px 8px;border-radius:3px;white-space:nowrap}
.tz{background:var(--zc-pale,var(--gold-pale));color:var(--zc,var(--gold))}
.tn{background:var(--surface2);color:var(--ink3)}
.tw{background:#fff3d8;color:#9a5f10}
.tf{background:var(--food-pale);color:var(--food-accent)}
 
.caret{width:44px;flex-shrink:0;display:flex;align-items:center;justify-content:center;color:var(--ink3);font-size:18px;transition:transform .25s,color .25s}
.card.open .caret{transform:rotate(90deg);color:var(--zc,var(--gold))}
 
/* Body */
.card-body{max-height:0;overflow:hidden;transition:max-height .45s cubic-bezier(.4,0,.2,1)}
.card.open .card-body{max-height:1800px}
.body-in{padding:24px 28px 28px;border-top:1px solid var(--border)}
@media(max-width:600px){.body-in{padding:16px 18px 22px}}
 
/* Transport strip */
.t-strip{
  display:flex;align-items:center;gap:10px;
  background:var(--surface2);border-radius:6px;
  padding:9px 14px;margin-bottom:20px;
  font-size:13px;color:var(--ink2);
  font-family:'DM Mono',monospace;letter-spacing:.3px;
}
 
/* ── ACTIVITY LIST ── clean icon rows ─── */
.act-list{
  list-style:none;
  display:flex;flex-direction:column;
  gap:0;
  margin-bottom:20px;
  border:1px solid var(--border);
  border-radius:8px;
  overflow:hidden;
}
 
.act-item{
  display:flex;
  align-items:flex-start;
  gap:14px;
  padding:12px 16px;
  border-bottom:1px solid var(--border);
  transition:background .15s;
}
.act-item:last-child{border-bottom:none}
.act-item:hover{background:#faf7f0}
 
.act-icon{
  width:30px;height:30px;
  border-radius:8px;
  background:var(--zc-pale,var(--gold-pale));
  display:flex;align-items:center;justify-content:center;
  font-size:15px;flex-shrink:0;
  margin-top:1px;
}
 
.act-text{flex:1}
.act-title{font-size:14.5px;font-weight:500;color:var(--ink);line-height:1.35;margin-bottom:2px}
.act-desc{font-size:13px;color:var(--ink3);line-height:1.5}
 
/* Section label inside body */
.body-sec{
  font-family:'DM Mono',monospace;font-size:9px;letter-spacing:3px;
  color:var(--ink3);text-transform:uppercase;
  margin-bottom:12px;margin-top:4px;
}
 
/* Tip */
.tip{
  display:flex;gap:10px;
  background:var(--gold-pale);border-radius:6px;
  padding:10px 14px;margin-bottom:20px;
  font-size:13.5px;color:#6a420c;line-height:1.6;
  border-left:3px solid var(--gold);
}
 
/* Options */
.opts{border:1px solid var(--border);border-radius:8px;overflow:hidden;margin-bottom:20px}
.opts-hd{background:var(--surface2);padding:8px 15px;font-family:'DM Mono',monospace;font-size:9px;letter-spacing:3px;color:var(--gold);text-transform:uppercase;border-bottom:1px solid var(--border)}
.opts-g{display:grid;grid-template-columns:1fr 1fr}
@media(max-width:540px){.opts-g{grid-template-columns:1fr}}
.opt-c{padding:13px 16px;font-size:13.5px;color:var(--ink2);border-right:1px solid var(--border);line-height:1.6}
.opt-c:last-child{border-right:none}
.opt-c strong{display:block;font-family:'DM Mono',monospace;font-size:9px;letter-spacing:2px;color:var(--gold-light);font-weight:500;margin-bottom:4px}
 
/* Food */
.food-hd{display:flex;align-items:center;gap:12px;margin:0 0 13px}
.food-lbl{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:3px;color:var(--food-accent);text-transform:uppercase;white-space:nowrap}
.food-ln{flex:1;height:1px;background:#e0c8b8}
.food-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:10px}
 
.fc{
  background:var(--surface);border:1px solid var(--border);
  border-radius:8px;padding:14px 16px;
  position:relative;overflow:hidden;
  transition:border-color .2s,box-shadow .2s;
}
.fc::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--food-accent),#f0c0a0)}
.fc:hover{border-color:#d09070;box-shadow:0 3px 14px rgba(0,0,0,.05)}
.fc-meal{font-family:'DM Mono',monospace;font-size:8px;letter-spacing:2px;color:var(--food-accent);text-transform:uppercase;margin-bottom:5px}
.fc-name{font-family:'Cormorant Garamond',serif;font-size:15px;font-weight:700;color:var(--ink);line-height:1.25;margin-bottom:2px}
.fc-zh{font-size:11.5px;color:var(--ink3);margin-bottom:7px}
.fc-desc{font-size:13px;color:var(--ink2);line-height:1.55;margin-bottom:8px}
.fc-order{font-size:12.5px;color:var(--food-accent);font-style:italic;padding-top:8px;border-top:1px solid var(--border);line-height:1.45}
 
/* Notes */
.notes-g{display:grid;grid-template-columns:1fr 1fr;gap:14px}
@media(max-width:600px){.notes-g{grid-template-columns:1fr}}
.nc{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:18px 22px}
.nc h3{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:3px;color:var(--gold);text-transform:uppercase;margin-bottom:10px;padding-bottom:8px;border-bottom:1px solid var(--border)}
.nc ul{list-style:none;display:flex;flex-direction:column;gap:7px}
.nc li{font-size:13.5px;color:var(--ink2);display:flex;gap:9px;line-height:1.55}
.nc li::before{content:'—';color:var(--gold);opacity:.5;flex-shrink:0}
 
footer{text-align:center;padding:48px 20px;border-top:1px solid var(--border);margin-top:72px}
footer p:first-child{font-family:'Cormorant Garamond',serif;font-size:18px;font-style:italic;color:var(--ink3);margin-bottom:7px}
footer p:last-child{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:3px;color:var(--ink3);opacity:.45}
 
@keyframes fup{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:translateY(0)}}
</style>
</head>
<body>
 
<header class="hero">
  <svg class="hero-hills" viewBox="0 0 1440 200" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
    <path fill="#4aaa68" d="M0,120 C120,95 240,140 360,118 C480,96 560,80 680,100 C800,120 880,135 1000,115 C1120,95 1280,105 1440,118 L1440,200 L0,200 Z"/>
    <path fill="#2e7a48" d="M0,148 C160,128 300,155 460,142 C620,129 720,118 900,138 C1080,158 1240,145 1440,150 L1440,200 L0,200 Z" opacity=".7"/>
  </svg>
  <div class="hero-content">
    <div class="hero-eyebrow">Group Travel · 11 Days · August 2025 · Option B — Hulunbuir</div>
    <h1><em>Hulunbuir</em> <span>&amp; Shenyang</span></h1>
    <p class="hero-sub">World's Finest Grassland · Wetlands · Russian Border · The Qing Dynasty</p>
    <div class="hero-pills">
      <div class="hp">✈ <b>SQ810</b> 1 Aug · SIN → PKX</div>
      <div class="hp">✈ <b>SQ801</b> 11 Aug · PEK → SIN</div>
      <div class="hp">👥 <b>Large Group</b> 6+ pax</div>
      <div class="hp">🗺 PKX → Hailar → Shenyang → PEK</div>
    </div>
  </div>
</header>
 
<div class="flt-bar">
  <div class="flt-side"><div class="flt-lbl">Outbound Flight</div><div class="flt-rt">SIN → PKX</div><div class="flt-dt">SQ810 · 1 August · Dep 12:30 PM / Arr 6:35 AM +1</div></div>
  <div class="flt-mid"><div class="flt-vl"></div>✈<div class="flt-vl"></div></div>
  <div class="flt-side r"><div class="flt-lbl">Return Flight</div><div class="flt-rt">PEK → SIN</div><div class="flt-dt">SQ801 · 11 August · Dep 12:05 PM / Arr 6:25 AM +1</div></div>
</div>
 
<main class="main">
 
  <div class="sec-head" style="margin-top:0"><div class="sec-lbl">Day by Day</div><div class="sec-line"></div></div>
 
  <div class="legend">
    <div class="leg-item"><div class="leg-dot" style="background:#7a6a58"></div>Transit</div>
    <div class="leg-item"><div class="leg-dot" style="background:#2e7a48"></div>Hulunbuir Grassland</div>
    <div class="leg-item"><div class="leg-dot" style="background:#2a7a7a"></div>Ergun Wetland</div>
    <div class="leg-item"><div class="leg-dot" style="background:#6a8a30"></div>Birch Forest / Shiwei</div>
    <div class="leg-item"><div class="leg-dot" style="background:#6a4a9a"></div>Manzhouli Border</div>
    <div class="leg-item"><div class="leg-dot" style="background:#2a5a8a"></div>Shenyang</div>
    <div class="leg-item"><div class="leg-dot" style="background:#9a6a2a"></div>Beijing</div>
  </div>
 
  <div class="days-stack" id="ds"></div>
 
  <div style="margin-top:64px">
    <div class="sec-head"><div class="sec-lbl">Travel Notes</div><div class="sec-line"></div></div>
    <div class="notes-g">
      <div class="nc">
        <h3>✈ PKX → Hailar Options</h3>
        <ul>
          <li>Fly PKX/PEK → Hailar HLD (~2.5 hrs, 13–15 daily flights). Aim for a morning departure to maximise Day 1</li>
          <li>No practical train option — flying is the only choice for a large group</li>
          <li>Book well in advance; August is peak grassland season and flights sell out</li>
          <li>Chartered private vehicle is essential throughout Hulunbuir — sites are spread across vast distances with no public transport</li>
        </ul>
      </div>
      <div class="nc">
        <h3>🌿 Hulunbuir Tips</h3>
        <ul>
          <li>Waterproof boots essential — heavy dew on grassland mornings even in August</li>
          <li>Big temperature swings: warm days, cool nights (15–18°C). Pack a fleece and light jacket</li>
          <li>Bring cash — signal and card readers unreliable near Shiwei and Manzhouli border areas</li>
          <li>Book yurts and Heishantou ranch experiences well in advance for groups of 6+</li>
        </ul>
      </div>
      <div class="nc">
        <h3>🏯 Shenyang Tips</h3>
        <ul>
          <li>Direct flight Hailar HLD → Shenyang SHE (~2 hrs, Ruili / Juneyao Airlines). Confirm route is running in August</li>
          <li>Mukden Palace: book tickets online in advance for large groups</li>
          <li>Laobian Dumplings: request a private room (包间) when booking for 6+</li>
          <li>Shenyang stays cool in August (~25–28°C) — ideal for full days outdoors</li>
        </ul>
      </div>
      <div class="nc">
        <h3>⚠ Critical Reminders</h3>
        <ul>
          <li>Return flight departs PEK (Capital Airport) — NOT PKX (Daxing). Different airports, 67 km apart</li>
          <li>Shenyang → Beijing: G138 (17:14–19:44) or G122 (18:19–20:49), both Shenyang North → Beijing South (~2.5 hrs)</li>
          <li>Day 11: aim to reach PEK by 9:30 AM. Leave hotel by 9:00 AM latest</li>
          <li>Manzhouli is a border area — carry passport at all times, be aware of photography restrictions near the national gate</li>
        </ul>
      </div>
    </div>
  </div>
</main>
 
<footer>
  <p>Have a wonderful journey</p>
  <p>草原再见 · Cǎoyuán Zàijiàn · Farewell, Grassland</p>
</footer>
 
<script>
const Z={
  transit:  {c:'#7a6a58',p:'#ede8e0'},
  grassland:{c:'#2e7a48',p:'#dff0e6'},
  wetland:  {c:'#2a7a7a',p:'#d8f0f0'},
  birch:    {c:'#6a8a30',p:'#eef5d8'},
  border:   {c:'#6a4a9a',p:'#eee8f8'},
  hailar:   {c:'#3a7a50',p:'#e4f0e8'},
  shenyang: {c:'#2a5a8a',p:'#dde8f5'},
  beijing:  {c:'#9a6a2a',p:'#f0e4d0'},
  depart:   {c:'#8a5a38',p:'#f0e4d8'},
};
 
// Each activity: { icon, title, desc }
const days=[
  {
    d:1, z:'transit',
    title:'Arrive Beijing → Fly to Hailar',
    loc:'PKX Daxing Airport → Hailar, Hulunbuir (HLD)',
    tags:[['w','Arrival 6:35 AM'],['n','Fly to Hailar ~2.5 hrs'],['n','Rest evening']],
    transport:null,
    acts:[
      {icon:'✈️', title:'Land at PKX Daxing Airport (~6:35 AM)', desc:'Clear immigration, collect luggage, and head straight to the departures hall for your onward flight to Hailar.'},
      {icon:'🛫', title:'Fly to Hailar (HLD) — ~2.5 hrs', desc:'Morning departure recommended (~8–9 AM). Arrive Hailar by 11 AM – early afternoon. See transport options below.'},
      {icon:'🏨', title:'Check into hotel in Hailar', desc:'Freshen up and let the group rest after the overnight flight and second transit.'},
      {icon:'🚶', title:'Easy afternoon — Hailar city orientation', desc:'Short walk around the city centre, pick up snacks, get a feel for the pace of Hulunbuir life.'},
      {icon:'🌙', title:'Early dinner and early night', desc:'Tomorrow the grassland begins in earnest. Rest well.'},
    ],
    tip:'Book a morning flight from PKX or PEK to Hailar (HLD) well in advance — August is peak season and seats sell out. There is no practical train option for a large group.',
    options:{title:'PKX → Hailar — Two Timing Options',
      a:{label:'Early Flight (Arrive ~11 AM)',desc:'Depart ~8–9 AM from PKX/PEK. Tight after a 6:35 AM landing but doable if immigration is smooth. Arrive Hailar by 11 AM with a full afternoon.'},
      b:{label:'Later Flight (Arrive ~2–3 PM)',desc:'Depart ~11 AM–12 PM for a more relaxed morning after the overnight flight. Arrive Hailar by early afternoon. Rest, check in, easy first evening.'}
    },
    food:[
      {meal:'Dinner',name:'Nomintala Milk Tea House',zh:'诺敏塔拉奶茶馆',desc:'A beloved Hailar institution. Authentic Mongolian milk tea, hand-pulled meat, and Buryat steamed buns — the ideal introduction to Hulunbuir cuisine.',order:'Hand-pulled mutton (手抓肉), Buryat steamed buns (布里亚特包子), salty Mongolian milk tea'},
      {meal:'Dinner Alt.',name:'Hailar Mongolian Restaurant',zh:'海拉尔蒙餐',desc:'Ask your hotel or guide to recommend a well-regarded local spot near the city centre. Any authentic Mongolian restaurant will be an excellent start.',order:'Iron pot stew (铁锅炖), grilled lamb chops (烤羊排), warm milk tea'},
    ]
  },
  {
    d:2, z:'grassland',
    title:'Hulunbuir Grassland & Morigele River',
    loc:'Hulunbuir Grassland · Morigele River (莫日格勒河) · Ergun',
    tags:[['z','Hulunbuir Prairie'],['z','Morigele River'],['z','Ergun Wetland']],
    transport:'Chartered vehicle: Hailar → Morigele River → Ergun (~120 km, ~2 hrs)',
    acts:[
      {icon:'🌅', title:'Drive out into the Hulunbuir Grassland', desc:'Leave Hailar early as the city dissolves and the open steppe stretches out in every direction. One of the world\'s top four grasslands — at its absolute peak in August.'},
      {icon:'🌊', title:'Morigele River — "First Bend of the World"', desc:'A serpentine river looping in hypnotic curves through the green plain. Elevated viewing platforms give sweeping panoramas of the river\'s course — one of the most photographed landscapes in Inner Mongolia.'},
      {icon:'🐎', title:'Horseback ride on the open grassland', desc:'Ride across the Hulunbuir steppe with a local guide — open, exhilarating, and the most immersive way to experience the scale of the landscape.'},
      {icon:'🌿', title:'Ergun Wetland — Asia\'s largest wetland', desc:'A mosaic of channels, marshes, and grassland at the foot of the Greater Khingan mountains, home to thousands of migratory birds. Arrive before sunset for extraordinary golden light.'},
      {icon:'🏕️', title:'Check into accommodation in Ergun', desc:'Stay overnight in Ergun to wake up fresh for the birch forest drive tomorrow.'},
    ],
    tip:'Waterproof boots are essential — the grassland is heavily dewy in the morning even in August. Dress in layers; warm days, cool evenings.',
    food:[
      {meal:'Lunch',name:'Roadside Herder Stop',zh:'草原途中餐',desc:'On a full driving day, lunch is typically at a simple local herder restaurant en route. Your guide will know the best spots for fresh, authentic food.',order:'Mutton noodle soup (羊肉面条), steamed buns, fresh yoghurt from roadside herders'},
      {meal:'Dinner',name:'Ergun Riverside Restaurant',zh:'额尔古纳河边餐厅',desc:'Dinner in Ergun by the river. Local restaurant specialising in river fish, wild Khingan mushrooms, and the region\'s famous iron pot stew.',order:'Iron pot fish stew (铁锅炖鱼), wild mushroom soup (野蘑菇汤), hand-pulled lamb, warm milk tea'},
    ]
  },
  {
    d:3, z:'birch',
    title:'Birch Forest & Shiwei Russian Township',
    loc:'Ergun → Primeval Birch Forest → Enhe → Shiwei (室韦)',
    tags:[['z','Birch Forest Drive'],['z','Enhe Township'],['z','Shiwei Border Village']],
    transport:'Chartered vehicle: Ergun → Enhe → Shiwei (~180 km along the Argun River border road, ~3 hrs)',
    acts:[
      {icon:'🌲', title:'Drive the Argun River border road', desc:'The natural border between China and Russia — one of the most scenic stretches of road in Inner Mongolia. White birch forests, river bends, and almost no traffic.'},
      {icon:'🏡', title:'Primeval birch forest of the Greater Khingan Range', desc:'White-trunked trees in every direction, birdsong, and a quiet rarely found this close to China\'s populated areas. Stop for photos and a walk.'},
      {icon:'☕', title:'Enhe Russian Ethnic Township — afternoon tea', desc:'A small village where descendants of Russian settlers still live. Russian-style afternoon tea in a timber house: black bread, local cheese, jam, strong tea.'},
      {icon:'🏘️', title:'Arrive Shiwei — the Russian border village', desc:'Timber homes, Russian Orthodox architecture, and an evening atmosphere that feels completely unlike anywhere else in China. Overnight in Shiwei.'},
      {icon:'🌆', title:'Evening stroll through Shiwei village', desc:'Walk the main street at dusk, browse local craft stalls, and take in the unusual cultural blend of Mongolian and Russian life on the border.'},
    ],
    tip:'The border road along the Argun River is narrow and beautiful — the drive itself is part of the experience. Signal is patchy; download offline maps before leaving Ergun. Bring cash.',
    food:[
      {meal:'Lunch',name:'Enhe Russian Afternoon Tea',zh:'恩和俄罗斯族下午茶',desc:'A genuine cultural stop mid-drive. Russian-style tea and bread served in a timber house by ethnic Russian descendants.',order:'Russian rye bread (俄式黑面包), local cheese and jam, black tea or coffee'},
      {meal:'Dinner',name:'Shiwei Border Village Dinner',zh:'室韦村庄晚餐',desc:'Dinner at a family-run guesthouse or local restaurant in Shiwei. Food blends Mongolian and Russian influences — a fitting meal in a town that straddles two cultures.',order:'Grilled lamb chops (烤羊排), borscht (罗宋汤), hand-pulled mutton, Russian sausage (香肠)'},
    ]
  },
  {
    d:4, z:'grassland',
    title:'Heishantou Ranch & Yurt Night',
    loc:'Shiwei → Heishantou Grassland (黑山头)',
    tags:[['z','Horseback Riding'],['z','Yurt Overnight'],['z','Bonfire Feast']],
    transport:'Chartered vehicle: Shiwei → Heishantou (~80 km, ~1.5 hrs)',
    acts:[
      {icon:'🐴', title:'Horseback riding at Heishantou Ranch', desc:'Considered the finest and most regulated horseback territory in all of Hulunbuir. Ride across the open plains — gallop, trot, or walk — across a landscape unchanged for a thousand years.'},
      {icon:'🏠', title:'Visit a herder family home', desc:'Milk cows, feed sheep, try on traditional Mongolian costumes, and learn about life on the steppe from a family who has lived this way for generations.'},
      {icon:'⛺', title:'Check into yurt camp for the night', desc:'Traditional Mongolian yurts arranged around a central fire area. Book a cluster for the group in advance — August fills fast.'},
      {icon:'🔥', title:'Bonfire feast with whole roast lamb', desc:'The centrepiece of the Hulunbuir experience. Whole lamb over open flame, Mongolian BBQ, horsehead fiddle music, and a sky of stars with zero light pollution.'},
      {icon:'🌟', title:'Stargazing from the open steppe', desc:'At this latitude and distance from any city, the night sky is extraordinary. One of those sights that stays with you.'},
    ],
    tip:'Book the Heishantou ranch experience and yurt camp in advance for a group of 6+. Look for ranches with English-speaking guides and proper insurance for horseback activities.',
    food:[
      {meal:'Lunch',name:'Heishantou Ranch Kitchen',zh:'黑山头牧场餐厅',desc:'Lunch at the ranch. Simple, fresh, and authentic — mutton stew, dairy products from the herder family, fresh milk straight from the herd.',order:'Mutton stew (羊肉炖), fresh milk (鲜奶), fried milk cake (奶饼), oat flatbread'},
      {meal:'Dinner',name:'Yurt Camp Bonfire Feast',zh:'蒙古包篝火晚宴',desc:'The trip\'s most memorable dinner. Whole lamb roasted over open fire, Mongolian BBQ, and traditional music around the flames under the Hulunbuir sky.',order:'Whole roast lamb (烤全羊 — book ahead), grilled lamb ribs (烤羊排), blood sausage (血肠), Mongolian milk wine (马奶酒)'},
    ]
  },
  {
    d:5, z:'border',
    title:'Manzhouli — The Border City',
    loc:'Manzhouli (满洲里) · China-Russia-Mongolia Tri-Border',
    tags:[['z','Matryoshka Square'],['z','National Gate'],['z','Barga Tribe']],
    transport:'Chartered vehicle: Heishantou → Manzhouli (~200 km, ~2.5 hrs)',
    acts:[
      {icon:'🪆', title:'Matryoshka Doll Square', desc:'200+ giant nesting dolls of every size and design, anchored by the world\'s largest matryoshka — a 30-metre structure with a Russian restaurant inside. Spectacular by night when it lights up completely.'},
      {icon:'🚉', title:'China-Russia National Gate Scenic Area', desc:'The ceremonial border gate with a memorial hall documenting the history of the Chinese Eastern Railway. Steam locomotive relics and views toward Russia.'},
      {icon:'🦅', title:'Barga Mongolian Tribe Experience', desc:'Eagle hunting demonstrations, traditional wrestling, reconstructed nomadic camp, and Mongolian archery. A vivid cultural counterpoint to the Russian architecture of the city.'},
      {icon:'🌃', title:'Evening at the illuminated Matryoshka Square', desc:'The square is best experienced at night. The light show is genuinely spectacular — wander the plaza, eat from the night market stalls, and take in the fairytale atmosphere.'},
    ],
    tip:'Carry your passport at all times in Manzhouli — it is a border area. Photography restrictions apply near the national gate. Card readers are unreliable; bring cash.',
    food:[
      {meal:'Lunch',name:'Rublyov Restaurant (Giant Matryoshka)',zh:'鲁布廖夫西餐厅',desc:'Inside the world\'s largest matryoshka doll. Russian aristocratic décor, borscht, braised beef, and kvass. Quirky and very well-suited to a large group.',order:'Borscht (罗宋汤), braised beef (炖牛肉), Russian dark bread, kvass (格瓦斯)'},
      {meal:'Dinner',name:'Manzhouli Night Market',zh:'满洲里夜市',desc:'As the square lights up, the surrounding night market comes alive. Grilled lamb from Hulunbuir herders, dairy pancakes, Russian sausages, milk tea — best eaten while wandering.',order:'Grilled lamb leg (烤羊腿), dairy pancakes (奶皮饼), Russian sausage (俄式香肠), cold kvass'},
    ]
  },
  {
    d:6, z:'hailar',
    title:'Hailar City & Hulun Lake',
    loc:'Hailar District, Hulunbuir City',
    tags:[['z','Hailar Ancient City'],['n','Hulun Lake'],['n','Buffer Day']],
    transport:'Return drive: Manzhouli → Hailar (~230 km, ~2.5 hrs)',
    acts:[
      {icon:'🚗', title:'Drive back to Hailar', desc:'A scenic return across the western grasslands. Use the drive time to reflect on what the group has seen — and to sleep, if needed.'},
      {icon:'🏯', title:'Hailar Ancient City Site', desc:'A well-preserved Mongolian fortification from the Jin Dynasty on the edge of the city. Understated but genuinely interesting — a historical anchor for the whole Hulunbuir experience.'},
      {icon:'💧', title:'Hulun Lake (optional) — afternoon visit', desc:'One of China\'s largest lakes and a major wetland reserve. A beautiful, quiet afternoon stop before the farewell dinner.'},
      {icon:'🛍️', title:'Free time — last shopping and packing', desc:'Pick up cashmere, dried milk snacks, and any Hulunbuir souvenirs before flying out to Shenyang tomorrow.'},
      {icon:'🌙', title:'Farewell dinner in Hailar', desc:'Last meal in the grassland world. Ask your guide to book a proper group dinner at a well-regarded Mongolian restaurant.'},
    ],
    tip:'Use this day at the group\'s pace. Confirm flights to Shenyang for tomorrow — the Hailar → Shenyang route operates on Ruili Airlines and Juneyao Airlines.',
    food:[
      {meal:'Lunch',name:'Hailar Local Noodle House',zh:'海拉尔面馆',desc:'A simple, satisfying return lunch in Hailar. Braised mutton noodles and fried bread are the staples to look for.',order:'Braised mutton noodles (红烧羊肉面), fried bread (油条), mutton soup (羊汤)'},
      {meal:'Dinner',name:'Hulunbuir Farewell Feast',zh:'呼伦贝尔告别晚宴',desc:'Final night in Hulunbuir. Ask your guide to book a group dinner at a well-regarded Mongolian restaurant — a fitting send-off from the grassland world.',order:'Iron pot stew (铁锅炖), Buryat buns, fresh yoghurt, Mongolian milk wine (马奶酒)'},
    ]
  },
  {
    d:7, z:'shenyang',
    title:'Hailar → Shenyang',
    loc:'Shenyang, Liaoning Province',
    tags:[['z','Direct Flight ~2 hrs'],['z','Shenyang Arrival']],
    transport:'Fly: Hailar HLD → Shenyang SHE (~2 hrs direct, Ruili Airlines / Juneyao Airlines)',
    acts:[
      {icon:'✈️', title:'Morning flight to Shenyang (~2 hrs direct)', desc:'A direct flight from the grassland world of Hulunbuir to Shenyang — a city of an entirely different character: industrial, imperial, and genuinely undervisited.'},
      {icon:'🏨', title:'Check into hotel near Shenhe District', desc:'Close to Mukden Palace and the best food streets — the right base for the next two days.'},
      {icon:'🚶', title:'Afternoon: Zhongjie (Middle Street) orientation', desc:'The historic commercial spine of Shenyang. A relaxed first walk to get oriented before the cultural intensity of Day 8.'},
      {icon:'🏛️', title:'Zhang Xueliang\'s Former Mansion', desc:'The Republican-era residence of the "Young Marshal" — one of the most compelling museums in Shenyang and a window into a pivotal period of modern Chinese history.'},
      {icon:'🍖', title:'Evening on Xita Korean Street', desc:'Shenyang\'s Korean-Chinese strip. Lively, communal, and ideal for a large group settling into a new city.'},
    ],
    tip:'Confirm the Hailar → Shenyang direct flight is running in August before finalising. Ruili Airlines and Juneyao Airlines both operate the route.',
    food:[
      {meal:'Lunch',name:'Airport Bite / Arrival Noodles',zh:'',desc:'Keep lunch light at Hailar airport or on arrival. Save appetite — Xita Korean Street is one of the trip\'s best dinner spots.',order:'Quick buns or noodles at the airport; arrive hungry for dinner'},
      {meal:'Dinner',name:'Xita Korean BBQ Street',zh:'西塔朝鲜族美食街',desc:'Shenyang\'s famous Korean-Chinese strip in Heping District. Tabletop grills, cold noodles, stone pot rice — perfect for a large, informal group dinner.',order:'Tabletop Korean BBQ (삼겹살), Xita cold noodles (西塔冷面), stone pot bibimbap'},
    ]
  },
  {
    d:8, z:'shenyang',
    title:'Shenyang: Imperial Palace & Culture',
    loc:'Shenyang, Liaoning Province',
    tags:[['z','Mukden Palace'],['n','Liaoning Museum'],['n','Beiling Park']],
    transport:null,
    acts:[
      {icon:'🏯', title:'Mukden Palace (沈阳故宫) — 2–3 hrs', desc:'Built in 1625, predating Beijing\'s Forbidden City. 114 buildings of ceremonial halls, imperial quarters, and royal gardens. The birthplace of the Qing Dynasty.'},
      {icon:'🔭', title:'Shengjing Dept Store Observation Deck', desc:'The building opposite the Palace has an observation deck with a bird\'s-eye view over the entire complex — worth 15 minutes.'},
      {icon:'🏛️', title:'Liaoning Provincial Museum (free entry)', desc:'22 exhibition halls and over 115,000 artefacts from the Hongshan Culture to the Qing Dynasty. Consistently underrated — budget a full afternoon.'},
      {icon:'🌳', title:'Beiling Park (北陵公园)', desc:'A vast imperial tomb park where locals practise tai chi in the mornings and stroll in the afternoons. A calm and restorative end to a full culture day.'},
    ],
    tip:'Book Mukden Palace tickets online in advance for large groups. The Palace is best when it opens — arrive early before the tour coaches.',
    food:[
      {meal:'Lunch',name:'Laobian Dumpling Restaurant',zh:'老边饺子馆 (中街店)',desc:'Guinness World Record holder: the oldest Chinese dumpling restaurant (est. 1829). Multi-storey on Zhongjie, walking distance from Mukden Palace. Ask for a private room (包间) for the group.',order:'Snow-flower pan-fried dumplings (雪花煎饺), pork & fennel steamed dumplings, the house "Angela Merkel" special'},
      {meal:'Dinner',name:'Daqinghua Dumpling Restaurant',zh:'大清花饺子馆',desc:'Keeps the distinctive Manchu dumpling tradition alive. Murals of Manchu horsemen on the walls. Spacious, suited to large groups, and impressively generous portions.',order:'Manchu-style steamed dumplings (满族蒸饺), northeast pork dumplings (东北猪肉饺), braised pork belly'},
    ]
  },
  {
    d:9, z:'shenyang',
    title:'Shenyang: History & Farewell',
    loc:'Shenyang, Liaoning Province',
    tags:[['z','Sept. 18th Museum'],['z','Qipan Mountain'],['n','Farewell Dinner']],
    transport:null,
    acts:[
      {icon:'🏛️', title:'September 18th History Museum', desc:'Documents the 1931 Mukden Incident and the Japanese occupation of Manchuria — a sobering and important piece of modern history, presented with clarity and depth.'},
      {icon:'⛪', title:'Catholic South Cathedral (南关天主教堂)', desc:'A striking Gothic church in the city centre, free to enter and frequently overlooked by visitors. A quiet and beautiful 20-minute stop.'},
      {icon:'⛰️', title:'Qipan Mountain Scenic Area', desc:'Hiking trails and solid panoramic views of the city. A welcome outdoor counterbalance to the morning\'s museums.'},
      {icon:'🛍️', title:'Taiyuan Street — last shopping', desc:'Free time for any remaining souvenirs or gifts before the train to Beijing tomorrow.'},
      {icon:'🍖', title:'Farewell BBQ dinner — northeast style', desc:'Classic northeast Chinese open-air BBQ: cumin-dusted lamb and pork skewers over charcoal. Communal, informal, and the right way to close out Shenyang.'},
    ],
    tip:'Shenyang is genuinely pleasant in August (~25–28°C). Enjoy the outdoor sightseeing — it\'s notably more comfortable than much of China at this time of year.',
    food:[
      {meal:'Lunch',name:'Caita Stir-Fried Stew',zh:'菜塔炒炖',desc:'A must-eat Shenyang street experience. Stir-fried stew with mashed potato, thick savoury sauce, and choice of protein. At the entrance to Caita Night Market. Always a queue — always worth it.',order:'Signature stir-fried stew (炒炖) — pork belly or mixed vegetable version'},
      {meal:'Dinner',name:'Northeast BBQ (Dongbei Kaorou)',zh:'东北烤串大排档',desc:'Classic northeast open-air BBQ — cumin-dusted skewers over charcoal at a da pai dong near Taiyuan Street. Loud, smoky, and a perfect group farewell.',order:'Lamb skewers (羊肉串), pork belly skewers (五花肉串), grilled corn, cold Shenyang beer'},
    ]
  },
  {
    d:10, z:'beijing',
    title:'Shenyang → Beijing',
    loc:'Beijing',
    tags:[['z','Train ~3 hr 47 min'],['n','Final Evening Beijing']],
    transport:'Train: Shenyang North → Beijing South · G138 (17:14–19:44) or G122 (18:19–20:49)',
    acts:[
      {icon:'🚄', title:'Two train options — choose based on your afternoon plans', desc:'G138 departs 17:14, arrives Beijing South 19:44 (2 hr 30 min). G122 departs 18:19, arrives Beijing South 20:49 (2 hr 30 min). Both run Shenyang North → Beijing South.'},
      {icon:'🎒', title:'Arrive Beijing early afternoon — store luggage', desc:'Check into hotel near PEK or city centre. Drop bags and head out for a final taste of the capital.'},
      {icon:'🏛️', title:'Optional: Tiananmen Square or Summer Palace', desc:'A final afternoon in Beijing — take what the group has energy for. Wangfujing Street for any last shopping is also a good option.'},
      {icon:'🦆', title:'Final group dinner — Peking Duck', desc:'The only acceptable last dinner in Beijing. Book Da Dong (大董) or Quanjude (全聚德) well in advance for a party of 6+. Request a private room.'},
      {icon:'🌙', title:'Early night — PEK departure tomorrow at 12:05 PM', desc:'Aim to be at PEK Capital Airport by 9:30 AM. Depart hotel no later than 9:00 AM.'},
    ],
    tip:'G138 gives a fuller afternoon in Shenyang; G122 gives an extra hour but arrives later in Beijing. Both arrive at Beijing South Station — allow ~1 hr to reach your hotel or PEK airport. Return flight departs PEK 12:05 PM; leave hotel by 9:00 AM on Day 11.',
    food:[
      {meal:'Lunch',name:'Train Dining Car',zh:'高铁餐车',desc:'The G240 dining car serves decent hot set meals. Alternatively, grab a bento box (盒饭) from the Shenyang North platform before boarding.',order:'Braised pork rice box, noodle soup, or whatever looks good from the trolley'},
      {meal:'Dinner',name:'Peking Duck',zh:'北京烤鸭',desc:'The only acceptable final dinner in Beijing. Book Da Dong (大董) or Quanjude (全聚德) in advance for a large group. Request a private room.',order:'Whole Peking duck (北京烤鸭), duck bone soup, spring pancakes with scallion and cucumber, duck liver pâté'},
    ]
  },
  {
    d:11, z:'depart',
    title:'Departure — Beijing to Singapore',
    loc:'Beijing Capital Airport (PEK)',
    tags:[['w','Depart 12:05 PM'],['n','Arrive SIN 6:25 AM +1']],
    transport:null,
    acts:[
      {icon:'🌅', title:'Final breakfast and hotel checkout', desc:'Take your time over a last breakfast before heading to PEK Capital Airport.'},
      {icon:'🚖', title:'Transfer to PEK Capital Airport', desc:'Allow at least 2.5 hours before departure for check-in and security. Depart hotel by 9:00 AM latest.'},
      {icon:'✈️', title:'SQ801 departs 12:05 PM', desc:'Arrives Singapore Changi Airport at 6:25 AM on 12 August.'},
      {icon:'🌿', title:'草原再见 — Farewell, Grassland', desc:'Eleven days across the world\'s finest prairie, the wetlands of Ergun, the Russian border villages, the Qing Dynasty\'s birthplace, and a final night in Beijing.'},
    ],
    tip:null,
    food:[]
  }
];
 
function build(d){
  const z=Z[d.z];
  const wrap=document.createElement('div');
  wrap.className='day';
  wrap.style.cssText=`--zc:${z.c};--zc-pale:${z.p}`;
 
  const tagsHtml=d.tags.map(([t,l])=>{
    const cl=t==='z'?'tz':t==='w'?'tw':'tn';
    return `<span class="tag ${cl}">${l}</span>`;
  }).join('')+(d.food&&d.food.length?`<span class="tag tf">🍜 Restaurants</span>`:'');
 
  const tHtml=d.transport?`<div class="t-strip"><span>🚄</span><span>${d.transport}</span></div>`:'';
 
  const actsHtml=d.acts.map(a=>`
    <li class="act-item">
      <div class="act-icon">${a.icon}</div>
      <div class="act-text">
        <div class="act-title">${a.title}</div>
        ${a.desc?`<div class="act-desc">${a.desc}</div>`:''}
      </div>
    </li>`).join('');
 
  const tipHtml=d.tip?`<div class="tip"><span>💡</span><span>${d.tip}</span></div>`:'';
 
  let optsHtml='';
  if(d.options){
    optsHtml=`<div class="opts"><div class="opts-hd">${d.options.title}</div><div class="opts-g">
      <div class="opt-c"><strong>${d.options.a.label}</strong>${d.options.a.desc}</div>
      <div class="opt-c"><strong>${d.options.b.label}</strong>${d.options.b.desc}</div>
    </div></div>`;
  }
 
  let foodHtml='';
  if(d.food&&d.food.length){
    const cards=d.food.map(f=>`<div class="fc">
      <div class="fc-meal">${f.meal}</div>
      <div class="fc-name">${f.name}</div>
      ${f.zh?`<div class="fc-zh">${f.zh}</div>`:''}
      <div class="fc-desc">${f.desc}</div>
      <div class="fc-order">Order: ${f.order}</div>
    </div>`).join('');
    foodHtml=`<div class="food-hd"><div class="food-lbl">Where to Eat</div><div class="food-ln"></div></div>
    <div class="food-grid">${cards}</div>`;
  }
 
  wrap.innerHTML=`
    <div class="card">
      <div class="z-bar"></div>
      <div class="card-hd" onclick="this.closest('.card').classList.toggle('open')">
        <div class="badge"><div class="badge-n">${d.d}</div><div class="badge-m">Aug</div></div>
        <div class="card-info">
          <div class="card-title">${d.title}</div>
          <div class="card-loc">📍 ${d.loc}</div>
          <div class="tags">${tagsHtml}</div>
        </div>
        <div class="caret">›</div>
      </div>
      <div class="card-body">
        <div class="body-in">
          ${tHtml}
          <div class="body-sec">Activities</div>
          <ul class="act-list">${actsHtml}</ul>
          ${optsHtml}${tipHtml}
          ${d.food&&d.food.length?foodHtml:''}
        </div>
      </div>
    </div>`;
  return wrap;
}
 
const ds=document.getElementById('ds');
days.forEach(d=>ds.appendChild(build(d)));
 
const io=new IntersectionObserver(entries=>{
  entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('vis');io.unobserve(e.target)}});
},{threshold:0.04});
document.querySelectorAll('.day').forEach(el=>io.observe(el));
</script>
</body>
</html>
