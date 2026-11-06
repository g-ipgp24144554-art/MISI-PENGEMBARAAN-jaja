<!DOCTYPE html>
<html lang="ms"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>Misi Pengembaraan Udara Bersih</title>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;700;800&display=swap" rel="stylesheet">
<style>
:root{--ink:#27406b;--sun:#ffd84a;--bg:#bfe8ff;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#14233f}}
:root[data-theme="dark"]{--bg:#14233f}
html,body{margin:0;height:100%;background:var(--bg);overflow:hidden;font-family:'Baloo 2','Comic Sans MS',system-ui,sans-serif}
body{display:flex;align-items:center;justify-content:center}
#wrap{position:relative;overflow:hidden;background:#bfe8ff;user-select:none;-webkit-user-select:none;touch-action:manipulation;color:var(--ink)}
#c{position:absolute;inset:0;width:100%;height:100%}
#hud{position:absolute;left:1.2%;top:2%;display:none;gap:.5em;font-weight:800;font-size:1.5em;pointer-events:none;z-index:1}
.in #hud,.in #zn{display:flex}
.pill{background:#fffbe8;border:.14em solid var(--ink);border-radius:2em;padding:.05em .7em;white-space:nowrap}
#ml span{margin:0 .1em;opacity:.3;filter:grayscale(1)}#ml span.d{opacity:1;filter:none}
#zn{position:absolute;left:50%;top:12%;transform:translateX(-50%);display:none;font-size:1.4em;font-weight:800;z-index:1}
#tools{position:absolute;right:1.2%;top:2%;display:flex;gap:.4em;z-index:5}
.ib{font-size:1.6em;width:1.8em;height:1.8em;border-radius:50%;border:.1em solid var(--ink);background:#fffbe8;cursor:pointer;padding:0}
#bub{position:absolute;left:3%;top:19%;max-width:46%;background:#fff;border:.14em solid var(--ink);border-radius:1em;padding:.4em .8em;font-size:1.6em;font-weight:700;z-index:2;opacity:0;transition:opacity .3s;pointer-events:none}
#bub.on{opacity:1}
#pr{position:absolute;left:50%;bottom:27%;transform:translateX(-50%);background:var(--sun);border:.12em solid var(--ink);border-radius:2em;padding:.1em 1em;font-size:2em;font-weight:800;display:none;z-index:2;cursor:pointer;animation:pu 1s infinite}
@keyframes pu{50%{transform:translateX(-50%) scale(1.07)}}
.tb{position:absolute;bottom:4%;width:5.6em;height:5.6em;border-radius:50%;border:.12em solid #fff;background:rgba(39,64,107,.55);color:#fff;font-size:1.5em;font-family:inherit;display:none;z-index:2;touch-action:none;padding:0}
.touch.in .tb{display:block}
#bl{left:2%}#br{left:17%}#bj{right:17%;background:rgba(43,183,163,.65)}#be{right:2%;background:rgba(255,122,168,.7)}
.scr{position:absolute;inset:0;display:none;flex-direction:column;align-items:center;justify-content:center;gap:.5em;text-align:center;background:rgba(30,60,110,.45);z-index:3}
.scr.on{display:flex}
.panel{background:#fffdf2;border:.18em solid var(--ink);border-radius:1.2em;padding:.8em 1.5em;color:var(--ink);max-width:86%}
.btn{font:inherit;font-weight:800;font-size:2em;padding:.12em 1em;border-radius:1.4em;border:.1em solid var(--ink);box-shadow:0 .12em 0 var(--ink);background:var(--sun);color:var(--ink);cursor:pointer}
.btn:active{transform:translateY(.08em)}
.g{background:#7be08a}.p{background:#ff9cc0}.b{background:#8ed3ff}
#home{background:transparent;align-items:flex-start;padding-left:6%;box-sizing:border-box}
h1{margin:0 0 .2em;font-size:3.1em;line-height:1;color:#fff;text-align:left;text-shadow:0 .07em 0 #2a4d9b,.05em .05em 0 #2a4d9b,-.05em .05em 0 #2a4d9b,0 -.03em 0 #2a4d9b}
h1 span{color:var(--sun)}
.sub{background:#fffbe8;border:.12em solid var(--ink);border-radius:2em;padding:0 .9em;font-size:1.6em;font-weight:700}
#home .btn{min-width:11em}
h2{margin:.1em 0;font-size:2.2em}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:.6em;margin:.3em 0}
.grid div{background:#fff;border:.1em solid var(--ink);border-radius:.8em;padding:.3em .5em;font-size:1.4em;font-weight:700}
.grid b{display:block;font-size:2.2em;line-height:1.1}
.big{font-size:5em;line-height:1}
.q{font-size:2em;font-weight:800;margin:.1em 0}
#qo{display:flex;gap:.6em;justify-content:center;margin:.2em 0}
.opt{display:flex;flex-direction:column;align-items:center;font:inherit;border-radius:1em;border:.12em solid var(--ink);background:#fff;padding:.2em .7em;min-width:7em;cursor:pointer;color:var(--ink)}
.opt span{font-size:3.2em;line-height:1.1}.opt small{font-size:1.3em;font-weight:700;max-width:7em}
.opt.ok{background:#b6f2bd;border-color:#1f9b3a}.opt.no{background:#ffd0d0;animation:sh .4s}
@keyframes sh{25%{transform:translateX(-.4em)}75%{transform:translateX(.4em)}}
#qf{font-size:1.5em;font-weight:700;min-height:2.6em;max-width:30em}
.fly{position:absolute;font-size:4em;animation:fl 1.2s forwards;pointer-events:none}
@keyframes fl{from{transform:scale(.3);opacity:1}to{transform:translateY(-3em) scale(1.6);opacity:0}}
.row{display:flex;gap:.8em;align-items:center;justify-content:center}
.cf{position:absolute;top:-3em;font-style:normal;animation:fall linear infinite;pointer-events:none}
@keyframes fall{to{transform:translateY(32em) rotate(360deg)}}
#rot{display:none;position:fixed;inset:0;z-index:99;background:#27406b;color:#fff;font-size:1.6em;text-align:center;align-items:center;justify-content:center}
@media (orientation:portrait) and (max-width:700px){#rot{display:flex}}
@media (prefers-reduced-motion:reduce){.cf,#pr{animation:none}}
</style></head><body>
<div id="rot"><div>🔄<br>Putarkan peranti anda ke mod mendatar</div></div>
<div id="wrap">
<canvas id="c" width="960" height="540"></canvas>
<div id="hud"><span class="pill">⭐ BINTANG: <b id="st">0</b>/5</span><span class="pill">🎯 MISI: <b id="ms">0</b>/5</span><span class="pill" id="ml"></span></div>
<div id="zn" class="pill"></div>
<div id="tools"><button class="ib" id="bs" title="Bunyi">🔊</button><button class="ib" id="bm" title="Muzik">🎵</button><button class="ib" id="bf" title="Skrin penuh">⛶</button></div>
<div id="bub"></div><div id="pr">👆 Tekan untuk mengetahui!</div>
<button class="tb" id="bl">◀</button><button class="tb" id="br">▶</button><button class="tb" id="bj">⬆</button><button class="tb" id="be">👆</button>

<div id="home" class="scr on"><h1><span>MISI</span> PENGEMBARAAN<br>UDARA BERSIH</h1><div class="sub">Jom cari punca pencemaran udara!</div><br>
<button class="btn g" id="bPlay">▶ MULA PERMAINAN</button><button class="btn b" id="bHow">❓ CARA BERMAIN</button><button class="btn p" id="bCred">💛 KREDIT</button></div>

<div id="how" class="scr"><div class="panel"><h2>CARA BERMAIN</h2><div class="grid" id="hg"></div><div style="font-size:1.2em">Papan kekunci: ← → berjalan · Space melompat · E berinteraksi</div></div><button class="btn" data-back>KEMBALI</button></div>

<div id="cred" class="scr"><div class="panel"><h2>KREDIT</h2><div style="font-size:1.5em;font-weight:700;line-height:1.3">Misi Pengembaraan Udara Bersih<br>Permainan digital pendidikan prasekolah (5–6 tahun)<br>Tema: Pencemaran Udara<br>Dibina dengan HTML5, CSS3, JavaScript dan Canvas<br>Untuk Pengajaran dan Pembelajaran (PdP) prasekolah</div></div><button class="btn" data-back>KEMBALI</button></div>

<div id="card" class="scr"><div class="panel"><div class="big" id="cE"></div><h2 id="cT"></h2><div class="q" id="cX" style="max-width:20em"></div></div><button class="btn g" id="cB">SAYA FAHAM!</button></div>

<div id="quiz" class="scr"><div class="panel" id="qp" style="position:relative"><div id="qL" style="font-size:1.3em;font-weight:800"></div><div class="big" id="qS"></div><div id="qC" style="font-size:1.2em;font-weight:700"></div>
<div class="q" id="qQ"></div><div id="qo"></div><div id="qf"></div></div>
<div class="row"><button class="btn b" id="qH" style="font-size:1.5em">🔈 Dengar</button><button class="btn g" id="qN" style="display:none">TERUSKAN ▶</button></div></div>

<div id="win" class="scr"><div class="row"><canvas id="gc" width="220" height="280" style="width:16em"></canvas>
<div class="panel"><h2 style="color:#e0527f">TAHNIAH! KAMU HEBAT!</h2><div style="font-size:1.5em;font-weight:700;max-width:16em">KAMU TELAH BERJAYA MENYELESAIKAN MISI PENGEMBARAAN UDARA BERSIH!</div>
<div class="big" style="font-size:3em">⭐⭐⭐⭐⭐</div><div style="font-size:1.6em;font-weight:800">Soalan betul: <span id="wq"></span><br>Misi selesai: <span id="wm"></span></div></div></div>
<div class="row"><button class="btn g" id="bAgain">MAIN SEMULA</button><button class="btn b" id="bAch">LIHAT PENCAPAIAN</button></div></div>

<div id="ach" class="scr"><div class="panel"><h2>PENCAPAIAN 🏆</h2><div id="al" style="font-size:1.6em;font-weight:800;text-align:left;line-height:1.5"></div></div><button class="btn" id="aB">KEMBALI</button></div>
</div>
<script>
const $=id=>document.getElementById(id),wrap=$('wrap'),g=$('c').getContext('2d'),W=960,H=540,GY=455,WORLD=5000;
function fit(){const w=Math.min(innerWidth,innerHeight*16/9);wrap.style.width=w+'px';wrap.style.height=w*9/16+'px';wrap.style.fontSize=w/70+'px'}
addEventListener('resize',fit);fit();
if(matchMedia('(pointer:coarse)').matches||'ontouchstart' in window)wrap.classList.add('touch');
const h2=s=>[1,3,5].map(i=>parseInt(s.substr(i,2),16));
const Z=[['#7fd4ff','#dff4ff','#a8e6b0','#7fd08a','#9aa3b2'],['#9fbfd4','#e2eaf0','#b9d0c4','#9bbfae','#b9bec9'],['#a9c9dc','#eef0e4','#c9d7b6','#b2c796','#dcc593'],['#7fd4ff','#e2f7ff','#a8e6b0','#7fd08a','#93df8d'],['#a9c7bd','#e8eed9','#8fcf9f','#5fb87a','#62c077']].map(r=>({t:h2(r[0]),b:h2(r[1]),f:h2(r[2]),n:h2(r[3]),gr:h2(r[4])}));
const ZN=['🏠 Kawasan Perumahan','🏭 Kawasan Kilang','🗑️ Kawasan Lapang','🌳 Kawasan Taman','🌲 Kawasan Hutan'],ZS=['🏠 Perumahan','🏭 Kilang','🗑️ Lapang','🌳 Taman','🌲 Hutan'];
const OBJ=[
{x:640,top:125,ico:'🚗',t:'Asap Kenderaan',info:'Bagus! Asap daripada kenderaan boleh mencemarkan udara.',scene:'🚗💨',q:'Adik, cuba lihat! Apa yang keluar dari belakang kereta?',o:[['🌸','Bunga'],['💨','Asap'],['🦋','Rama-rama']],a:1,fb:'Pandainya! Asap kereta boleh mencemarkan udara.',h:'Lihat belakang kereta. Ia kelabu dan berkepul-kepul.',hint:'Jom kita cari sesuatu yang mengeluarkan asap di jalan raya!'},
{x:1590,top:345,ico:'🏭',t:'Asap Kilang',info:'Pandai! Asap daripada kilang boleh mencemarkan udara.',scene:'🏭💨',q:'Lihat cerobong kilang itu. Apa yang keluar daripadanya?',o:[['💨','Asap'],['🌈','Pelangi'],['🌼','Bunga']],a:0,fb:'Betul! Asap kilang boleh mencemarkan udara.',h:'Lihat atas cerobong. Apa yang naik ke langit?',hint:'Adakah kamu nampak kilang di hadapan?'},
{x:2610,top:140,ico:'🔥',t:'Pembakaran Terbuka',info:'Hebat! Pembakaran sampah menghasilkan asap yang mencemarkan udara.',scene:'🗑️🔥💨',q:'Adakah membakar sampah boleh menyebabkan udara tercemar?',o:[['👍','Ya'],['👎','Tidak']],a:0,fb:'Hebat! Membakar sampah menghasilkan asap yang mencemarkan udara.',h:'Fikir tentang asap daripada api itu.',hint:'Mari cari kawasan lapang berhampiran tong sampah!'},
{x:3720,top:185,ico:'🚬',t:'Asap Rokok',info:'Bagus! Asap rokok boleh menjejaskan kesihatan kita.',scene:'🚬💨',q:'Adakah asap rokok baik untuk kesihatan kita?',o:[['👍','Ya'],['👎','Tidak']],a:1,fb:'Betul! Asap rokok tidak baik untuk kesihatan.',h:'Asap membuat kita batuk. Adakah itu baik?',hint:'Ada seseorang di taman. Mari lihat dari jauh!'},
{x:4660,top:215,ico:'🌲',t:'Kebakaran Hutan',info:'Bijak! Asap daripada kebakaran hutan boleh mencemarkan udara.',scene:'🌲🔥💨',q:'Apa yang berlaku kepada udara apabila hutan terbakar?',o:[['🌫️','Udara tercemar dengan asap.'],['🌈','Udara menjadi lebih bersih.']],a:0,fb:'Tahniah! Asap kebakaran hutan boleh mencemarkan udara.',h:'Lihat langit di atas hutan itu.',hint:'Mari masuk ke dalam hutan. Ada sesuatu yang pelik!'}];
const TH=[
{lv:'Tahap 1: Kenal Pasti',scene:'🔍',q:'Yang manakah mengeluarkan asap?',o:[['🚗💨','Kereta'],['🌸','Bunga'],['🦋','Rama-rama']],a:0,fb:'Betul! Kereta mengeluarkan asap.',h:'Cari gambar yang ada kepulan asap.'},
{lv:'Tahap 2: Bezakan',scene:'🌬️',q:'Adik, gambar manakah menunjukkan udara tercemar?',o:[['🌳🌸☀️','Gambar A: Hijau dan cerah'],['🏭💨💨','Gambar B: Kilang, asap tebal']],a:1,fb:'Pandai! Asap tebal membuat udara tercemar.',h:'Udara tercemar ada banyak asap.'},
{lv:'Tahap 3: Pilih Tindakan',scene:'🌱 🚶 🚌 🔥',c:'Menanam pokok · Berjalan kaki · Bas bersama · Membakar sampah',q:'Apakah yang boleh kita lakukan untuk menjaga udara?',o:[['🌱','Menanam pokok'],['🔥','Membakar sampah'],['🗑️🔥','Membiarkan sampah dibakar']],a:0,fb:'Hebat! Menanam pokok, berjalan kaki dan menaiki bas bersama menjaga udara bersih.',h:'Pilih perkara yang baik untuk alam.'}];
// ---------- audio ----------
let AC,snd=true,mus=true,mT;
function ac(){if(!AC){try{AC=new(window.AudioContext||window.webkitAudioContext)()}catch(e){}}if(AC&&AC.state==='suspended')AC.resume();return AC}
function tone(f,d,tp,v,at){const a=ac();if(!a)return;const o=a.createOscillator(),n=a.createGain(),s=a.currentTime+(at||0);o.type=tp||'sine';o.frequency.value=f;n.gain.setValueAtTime(0,s);n.gain.linearRampToValueAtTime(v,s+.02);n.gain.exponentialRampToValueAtTime(.0001,s+d);o.connect(n);n.connect(a.destination);o.start(s);o.stop(s+d+.05)}
function sfx(k){if(!snd)return;if(k==='ok')[523,659,784,1047].forEach((f,i)=>tone(f,.25,'triangle',.09,i*.1));else if(k==='no'){tone(300,.2,'sine',.07);tone(250,.25,'sine',.07,.15)}else if(k==='jump')tone(520,.12,'sine',.05);else tone(660,.08,'triangle',.06)}
const MN=[262,330,392,330,294,392,440,392];let mi=0;
function musicLoop(){clearInterval(mT);if(mus)mT=setInterval(()=>{tone(MN[mi%8]*(mi%16<8?1:.75),.35,'triangle',.03);mi++},450)}
function say(t){if(!snd||!window.speechSynthesis)return;try{speechSynthesis.cancel();const u=new SpeechSynthesisUtterance(t.replace(/[^\p{L}\p{N}\s.,!?:]/gu,''));u.lang='ms-MY';u.rate=.9;u.pitch=1.25;const v=speechSynthesis.getVoices().find(v=>/^ms/i.test(v.lang))||speechSynthesis.getVoices().find(v=>/^id/i.test(v.lang));if(v)u.voice=v;speechSynthesis.speak(u)}catch(e){}}
// ---------- drawing helpers ----------
function rr(c,x,y,w,h,r){c.beginPath();if(c.roundRect)c.roundRect(x,y,w,h,r);else c.rect(x,y,w,h)}
function box(x,y,w,h,col,r){rr(g,x,y,w,h,r||0);g.fillStyle=col;g.fill()}
function o(x,y,r,col){g.fillStyle=col;g.beginPath();g.arc(x,y,r,0,7);g.fill()}
function girl(c,x,y,s,st,t,f,ph){
c.save();c.translate(x,y);c.scale(s*f,s);let sw=0,bob=0,arm=.25;
if(st==='walk'){sw=Math.sin(ph)*.7;bob=-Math.abs(Math.sin(ph))*3;arm=Math.sin(ph)*.8}
if(st==='jump'){sw=.55;arm=-2.2}
if(st==='happy'){bob=-Math.abs(Math.sin(t*8))*14;arm=-2.6+Math.sin(t*14)*.35;sw=.1}
if(st==='idle')bob=Math.sin(t*3)*1.2;
c.translate(0,bob);
[1,-1].forEach(d=>{c.save();c.translate(0,-38);c.rotate(sw*d);c.fillStyle='#ffd7b5';rr(c,-4.5,0,9,31,4);c.fill();c.fillStyle='#e8548c';rr(c,-6,27,17,10,5);c.fill();c.restore()});
c.fillStyle='#2bb7a3';rr(c,-29,-72,17,32,7);c.fill();
c.fillStyle='#ff8fb8';c.beginPath();c.moveTo(-14,-44);c.lineTo(14,-44);c.lineTo(22,-24);c.lineTo(-22,-24);c.fill();
c.fillStyle='#ffd84a';rr(c,-13,-74,26,34,9);c.fill();
[1,-1].forEach(d=>{c.save();c.translate(0,-66);c.rotate(arm*d);c.fillStyle='#ffd84a';rr(c,-5,-2,10,13,5);c.fill();c.fillStyle='#ffd7b5';rr(c,-4,8,8,18,4);c.fill();c.beginPath();c.arc(0,27,5,0,7);c.fill();c.restore()});
c.fillStyle='#6b3f2a';c.beginPath();c.arc(0,-88,23,0,7);c.fill();c.beginPath();c.arc(-25,-76,9,0,7);c.fill();
c.fillStyle='#ff5c93';c.beginPath();c.arc(-21,-96,6,0,7);c.fill();
c.fillStyle='#ffd7b5';c.beginPath();c.arc(2,-86,19,0,7);c.fill();
c.fillStyle='#6b3f2a';c.beginPath();c.arc(2,-90,20,Math.PI,2*Math.PI);c.fill();
c.fillStyle='#2b2b3a';c.beginPath();c.arc(7,-84,3,0,7);c.arc(17,-84,3,0,7);c.fill();
c.fillStyle='#fff';c.beginPath();c.arc(8,-85,1.1,0,7);c.arc(18,-85,1.1,0,7);c.fill();
c.fillStyle='rgba(255,110,140,.45)';c.beginPath();c.arc(3,-77,3.6,0,7);c.arc(19,-77,3.6,0,7);c.fill();
c.strokeStyle=c.fillStyle='#b0453e';c.lineWidth=2;c.beginPath();
if(st==='happy'){c.arc(12,-79,5,0,Math.PI);c.fill()}else{c.arc(12,-79,4.5,.15*Math.PI,.85*Math.PI);c.stroke()}
c.restore()}
function adult(x,s){g.save();g.translate(x,GY);g.scale(-s,s);box(-10,-42,9,42,'#4a5d8f',3);box(1,-42,9,42,'#4a5d8f',3);box(-12,-6,14,6,'#333',3);box(0,-6,14,6,'#333',3);box(-14,-84,28,46,'#7aa8e0',9);box(8,-80,22,9,'#7aa8e0',4);o(31,-76,4.5,'#f2c9a0');box(33,-79,14,4,'#fff');box(45,-79,4,4,'#ff7a3a');o(0,-100,17,'#f2c9a0');g.fillStyle='#4a3020';g.beginPath();g.arc(0,-103,17,Math.PI,2*Math.PI);g.fill();o(7,-101,2.4,'#222');g.restore()}
function tree(x,s,c){c=c||'#4fbf6a';box(x-6*s,GY-62*s,12*s,62*s,'#a9744a',3*s);o(x,GY-84*s,30*s,c);o(x-20*s,GY-62*s,22*s,c);o(x+20*s,GY-62*s,22*s,c);o(x-9*s,GY-95*s,11*s,'rgba(255,255,255,.2)')}
function house(x,w,h,wall,roof){box(x,GY-h,w,h,wall,10);g.fillStyle=roof;g.beginPath();g.moveTo(x-14,GY-h+4);g.lineTo(x+w/2,GY-h-62);g.lineTo(x+w+14,GY-h+4);g.fill();box(x+w/2-16,GY-58,32,58,'#c98b57',8);box(x+14,GY-h+24,34,34,'#bfe8ff',6);box(x+w-48,GY-h+24,34,34,'#bfe8ff',6)}
function flame(x,y,s,t){g.save();g.translate(x,y);g.scale(s,s);const k=Math.sin(t*9+x)*6;[['#ff8a2b',1],['#ffd84a',.55]].forEach(a=>{g.save();g.scale(a[1],a[1]);g.fillStyle=a[0];g.beginPath();g.moveTo(0,-42-k);g.bezierCurveTo(28,-14,26,0,0,0);g.bezierCurveTo(-26,0,-28,-14,0,-42-k);g.fill();g.restore()});g.restore()}
function sign(x,txt){box(x-6,GY-100,12,100,'#a9744a',3);box(x-82,GY-142,164,52,'#ffe9a8',12);g.strokeStyle='#b9803f';g.lineWidth=4;rr(g,x-82,GY-142,164,52,12);g.stroke();g.fillStyle='#6a3f1b';g.font="800 21px 'Baloo 2',sans-serif";g.textAlign='center';g.fillText(txt,x,GY-107)}
function bin(x){box(x-22,GY-52,44,52,'#3fae66',6);box(x-26,GY-60,52,10,'#2c8a4e',4);g.fillStyle='#fff';g.font='700 24px sans-serif';g.textAlign='center';g.fillText('♻',x,GY-18)}
function bush(x,s){o(x,GY-14*s,18*s,'#8fcf7a');o(x+18*s,GY-10*s,14*s,'#7bc26a');o(x-18*s,GY-10*s,14*s,'#7bc26a')}
function flowers(x0,x1,y){const cols=['#ff7aa8','#ffd84a','#fff','#b58cff'];x0=Math.max(x0,Math.floor((cam-20)/47)*47);for(let x=x0;x<x1&&x<cam+W+20;x+=47){const i=(x/47)|0;g.fillStyle='#3fae66';g.fillRect(x,y-8+(i%3)*5,2,10);o(x+1,y-9+(i%3)*5,5,cols[i%4])}}
// ---------- state ----------
let state='home',cam=0,stars=0,miss=0,corr=0,curZ=-1,seen=[],idle=0,near=null,solved=false,T=0,bubT,K={};
const p={x:120,y:GY,vx:0,vy:0,g:true,f:1,ph:0,hp:0,an:'idle'};
const SRC=[{x:570,y:GY-26,r:3,s:.8},{x:1548,y:GY-308,r:3.5,s:1.3},{x:1638,y:GY-308,r:3.5,s:1.3},{x:2610,y:GY-98,r:5,s:1.2},{x:3662,y:GY-96,r:1.3,s:.35},{x:4630,y:GY-150,r:5,s:1.5},{x:4690,y:GY-130,r:4,s:1.3}],PT=[];
function mix(k){const f=Math.min(4.999,Math.max(0,(cam+W/2)/1000)),i=f|0,a=Z[i][k],b=Z[Math.min(4,i+1)][k],t=Math.max(0,(f-i-.55)/.45);return 'rgb('+a.map((v,j)=>(v+(b[j]-v)*t)|0).join()+')'}
function hills(par,base,amp,col,ph){g.fillStyle=col;g.beginPath();g.moveTo(0,H);for(let x=0;x<=W;x+=16){g.lineTo(x,base+Math.sin((x+cam*par)/170+ph)*amp+Math.sin((x+cam*par)/70+ph*2)*amp*.3)}g.lineTo(W,H);g.fill()}
function scenery(t){
for(let z=0;z<5;z++){g.fillStyle='rgb('+Z[z].gr+')';g.fillRect(z*1000-1,GY-10,1002,H-GY+10);g.fillStyle='rgba(255,255,255,.3)';g.fillRect(z*1000-1,GY-10,1002,8)}
g.fillStyle='#7fd08a';g.fillRect(0,GY-10,1000,6);for(let x=0;x<1000;x+=90)box(x,GY+48,50,6,'#fff',3);
// z0
[90,360,590,930].forEach((x,i)=>tree(x,.9+i%2*.25));house(190,150,120,'#ffd1dc','#ff8a8a');house(420,170,140,'#d1ecff','#6fa8ff');house(770,150,120,'#fff0b3','#ffa94d');flowers(150,980,GY-2);
const cx=640;box(cx-60,GY-48,120,32,'#ff6b6b',12);box(cx-35,GY-78,70,36,'#ff6b6b',14);box(cx-28,GY-72,26,24,'#bfe8ff',6);box(cx+2,GY-72,26,24,'#bfe8ff',6);box(cx-68,GY-28,12,8,'#666',3);[-35,35].forEach(d=>{o(cx+d,GY-14,15,'#333');o(cx+d,GY-14,6,'#bbb')});o(cx+57,GY-36,5,'#ffe27a');
// z1
box(1250,GY-150,240,150,'#f2b8b0',8);for(let i=0;i<4;i++)box(1270+i*55,GY-125,34,30,'#bfe8ff',5);box(1355,GY-52,45,52,'#a8794d',6);
box(1500,GY-195,180,195,'#b8c7e8',8);box(1530,GY-300,36,110,'#fff',4);box(1620,GY-300,36,110,'#fff',4);[0,1].forEach(i=>[GY-295,GY-265].forEach(y=>box(1530+i*90,y,36,14,'#ff6b6b',2)));for(let i=0;i<3;i++)box(1520+i*52,GY-165+i%2*0,34,30,'#fff3b0',5),box(1520+i*52,GY-110,34,30,'#fff3b0',5);bush(1210,1);bush(1720,1.1);
// z2
bush(2150,1.2);bush(2950,1.1);bin(2440);bin(2790);[[2500,'#ff7a7a'],[2700,'#7ab8ff'],[2330,'#ffd84a']].forEach(a=>box(a[0],GY-10,16,10,a[1],3));
o(2575,GY-16,22,'#6b7a8f');o(2615,GY-18,24,'#7a5c3a');o(2648,GY-13,18,'#6aa56f');o(2592,GY-40,20,'#8f8f9f');o(2625,GY-44,18,'#a67c52');flame(2588,GY-52,1,t);flame(2618,GY-56,1.3,t);flame(2645,GY-36,.8,t);
// z3
[3050,3330,3930].forEach((x,i)=>tree(x,1+i*.1));flowers(3000,3990,GY+14);flowers(3000,3990,GY+36);
g.strokeStyle='#e8548c';g.lineWidth=8;g.lineCap='round';[[3220,GY],[3290,GY]].forEach(a=>{g.beginPath();g.moveTo(a[0],GY);g.lineTo(a[0]+(a[0]<3250?25:-25),GY-120);g.stroke()});g.beginPath();g.moveTo(3245,GY-120);g.lineTo(3270,GY-120);g.stroke();const sg=Math.sin(t*2.5)*.35;g.save();g.translate(3257,GY-120);g.rotate(sg);g.lineWidth=3;g.strokeStyle='#555';g.beginPath();g.moveTo(-12,0);g.lineTo(-12,70);g.moveTo(12,0);g.lineTo(12,70);g.stroke();box(-18,68,36,8,'#ffd84a',3);g.restore();
box(3395,GY-110,14,110,'#5aa9f0',4);box(3470,GY-24,50,24,'#5aa9f0',4);g.strokeStyle='#ffb347';g.lineWidth=14;g.beginPath();g.moveTo(3402,GY-108);g.lineTo(3500,GY-26);g.stroke();
box(3550,GY-40,90,10,'#c98b57',4);box(3555,GY-30,8,30,'#8a5a30',2);box(3627,GY-30,8,30,'#8a5a30',2);box(3550,GY-70,90,8,'#c98b57',4);adult(3720,1.25);
// z4
for(let x=4020;x<5000;x+=83)tree(x,.65+((x/83|0)%3)*.12,'#8fd6a0');
for(let x=4040;x<5000;x+=70){const b=x>4590&&x<4730,i=x/70|0;tree(x,1+(i%3)*.3,b?'#e89a4a':(i%2?'#3fae66':'#5fc87a'))}
flame(4620,GY-95,1.1,t);flame(4665,GY-120,1.4,t);flame(4710,GY-100,1.1,t);flame(4650,GY-70,.8,t);
for(let z=0;z<5;z++)sign(z*1000+130,ZS[z])}
function drawWorld(t){
const tp=mix('t'),bt=mix('b'),gr=g.createLinearGradient(0,0,0,GY);gr.addColorStop(0,tp);gr.addColorStop(1,bt);g.fillStyle=gr;g.fillRect(0,0,W,H);
o(850,85,46,'rgba(255,230,120,.45)');o(850,85,32,'#ffe27a');
[[100,70,1],[380,110,1.3],[640,55,.9],[900,130,1.1],[1150,80,1.2]].forEach(c=>{const x=((c[0]-cam*.15+t*10)%1400+1400)%1400-200,s=c[2];g.globalAlpha=.92;o(x,c[1],24*s,'#fff');o(x+26*s,c[1]+6*s,20*s,'#fff');o(x-26*s,c[1]+8*s,18*s,'#fff');g.globalAlpha=1});
hills(.25,GY-120,45,mix('f'),0);hills(.5,GY-60,35,mix('n'),2);
g.save();g.translate(-Math.round(cam),0);scenery(t);
OBJ.forEach(b=>{const by=GY-b.top+Math.sin(t*4+b.x)*6,nr=near===b?1.25:1;if(b.done){g.font='46px serif';g.textAlign='center';g.fillText('⭐',b.x,by+14)}else{g.save();g.translate(b.x,by);g.scale(nr,nr);o(0,0,26,'#ffd84a');g.strokeStyle='#e29a00';g.lineWidth=4;g.stroke();g.fillStyle='#7a4a00';g.font="800 34px 'Baloo 2',sans-serif";g.textAlign='center';g.fillText('?',0,12);g.restore()}});
if(state!=='home')girl(g,p.x,p.y,1.1,p.an,t,p.f,p.ph);
PT.forEach(q=>{const a=.7*(1-q.l/q.m);g.fillStyle='rgba(140,146,158,'+a+')';g.beginPath();g.arc(q.x,q.y,q.r,0,7);g.fill();g.fillStyle='rgba(205,210,220,'+a*.7+')';g.beginPath();g.arc(q.x-q.r*.25,q.y-q.r*.25,q.r*.55,0,7);g.fill()});
g.restore()}
function render(t){
if(state==='home')cam=0;
drawWorld(t);
if(state==='home')girl(g,790,GY+12,2.3,'happy',t,1,0);
else if(state==='play'||state==='modal'){const n=OBJ.find(b=>!b.done);if(n&&miss<5){const sx=n.x-cam;if(sx>W-40||sx<40){g.font='46px serif';g.textAlign='center';g.fillText(sx>0?'👉':'👈',sx>0?W-40:40,GY-170+Math.sin(t*5)*7)}}}
if(state==='win'){const c=$('gc').getContext('2d');c.clearRect(0,0,220,280);girl(c,110,262,2,'happy',t,1,0)}}
// ---------- UI ----------
const show=e=>e.classList.add('on'),hide=e=>e.classList.remove('on');
function hud(){$('st').textContent=stars;$('ms').textContent=miss;[...$('ml').children].forEach((s,i)=>s.classList.toggle('d',OBJ[i].done))}
OBJ.forEach(b=>{const s=document.createElement('span');s.textContent=b.ico;$('ml').appendChild(s)});
[['⬅️➡️','Tekan butang kiri dan kanan untuk berjalan'],['⬆️','Tekan butang lompat untuk melompat'],['💨','Cari objek yang mengeluarkan asap'],['👆','Tekan butang interaksi untuk mengetahui'],['❓','Jawab soalan untuk mendapatkan bintang'],['⭐','Cari kesemua lima punca pencemaran udara']].forEach(a=>{const d=document.createElement('div');d.innerHTML='<b>'+a[0]+'</b>'+a[1];$('hg').appendChild(d)});
function bubble(t,ms,sp){clearTimeout(bubT);$('bub').textContent='👧 '+t;$('bub').classList.add('on');if(sp)say(t);bubT=setTimeout(()=>$('bub').classList.remove('on'),ms||4500)}
function reset(){Object.assign(p,{x:120,y:GY,vx:0,vy:0,f:1,hp:0});cam=0;OBJ.forEach(b=>b.done=false);stars=miss=corr=0;seen=[];curZ=-1;idle=0;near=null;PT.length=0;document.querySelectorAll('.cf').forEach(e=>e.remove());hud()}
function start(){ac();reset();['home','how','cred','win','ach','card','quiz'].forEach(i=>hide($(i)));wrap.classList.add('in');state='play';musicLoop();bubble('Selamat datang ke Misi Pengembaraan Udara Bersih! Jom kita cari punca pencemaran udara!',6000,1)}
function interact(){if(state==='play'&&near)openCard(near)}
function openCard(b){state='modal';$('cE').textContent=b.ico;$('cT').textContent=b.t;$('cX').textContent=b.info;show($('card'));say(b.info);sfx('c');
$('cB').onclick=()=>{hide($('card'));quiz(b,()=>{if(miss>=5)tahap(0);else{state='play';p.hp=1.8;idle=0}},'Soalan: '+b.t)}}
function quiz(q,done,lv){state='modal';solved=false;$('qL').textContent=lv;$('qS').textContent=q.scene;$('qC').textContent=q.c||'';$('qQ').textContent=q.q;$('qf').textContent='';$('qN').style.display='none';const qo=$('qo');qo.innerHTML='';
q.o.forEach((a,i)=>{const b=document.createElement('button');b.className='opt';b.innerHTML='<span>'+a[0]+'</span><small>'+a[1]+'</small>';b.onclick=()=>{if(solved)return;
if(i===q.a){solved=true;b.classList.add('ok');corr++;if(q.x!==undefined&&!q.done){q.done=true;stars++;miss++;hud()}$('qf').textContent='⭐ Tahniah! Kamu hebat! '+q.fb;sfx('ok');say('Tahniah! Kamu hebat! '+q.fb);$('qN').style.display='';const f=document.createElement('div');f.className='fly';f.textContent='⭐';f.style.cssText='left:45%;top:30%';$('qp').appendChild(f);setTimeout(()=>f.remove(),1300)}
else{b.classList.add('no');b.disabled=true;$('qf').textContent='Tidak mengapa! Cuba lagi. '+q.h;sfx('no');say('Tidak mengapa! Cuba lagi.')}};qo.appendChild(b)});
const read=()=>say(q.q+' '+q.o.map(a=>a[1]).join('. Atau ')+'?');$('qH').onclick=read;
$('qN').onclick=()=>{hide($('quiz'));done()};show($('quiz'));read()}
function tahap(i){if(i>=TH.length){win();return}quiz(TH[i],()=>tahap(i+1),TH[i].lv)}
function win(){state='win';$('wq').textContent=corr+'/8';$('wm').textContent=miss+'/5';show($('win'));sfx('ok');say('Tahniah! Kamu hebat! Kamu telah berjaya menyelesaikan misi.');
for(let i=0;i<40;i++){const s=document.createElement('i');s.className='cf';s.textContent=['⭐','🎉','✨','🌟','🎈'][i%5];s.style.cssText='left:'+Math.random()*100+'%;animation-delay:'+Math.random()*3+'s;animation-duration:'+(3+Math.random()*3)+'s;font-size:'+(1.5+Math.random()*1.5)+'em';$('win').appendChild(s)}}
// ---------- loop ----------
function update(dt){
SRC.forEach(s=>{if(Math.abs(s.x-cam-W/2)>800)return;s.a=(s.a||0)+dt*s.r;while(s.a>=1&&PT.length<260){s.a--;PT.push({x:s.x+(Math.random()-.5)*8,y:s.y,vx:12+Math.random()*18,vy:-(28+Math.random()*25),r:s.s*(9+Math.random()*6),l:0,m:2.6+Math.random()})}s.a=Math.min(s.a,1)});
for(let i=PT.length-1;i>=0;i--){const q=PT[i];q.x+=q.vx*dt;q.y+=q.vy*dt;q.l+=dt;q.r+=dt*6;if(q.l>q.m)PT.splice(i,1)}
if(state!=='play'){if(state==='modal')p.vx=0;return}
const d=(K.r?1:0)-(K.l?1:0);p.vx+=(d*270-p.vx)*Math.min(1,dt*12);if(d)p.f=d;p.x=Math.max(25,Math.min(WORLD-40,p.x+p.vx*dt));
if(K.j&&p.g){p.vy=-650;p.g=false;sfx('jump')}p.vy+=1800*dt;p.y+=p.vy*dt;if(p.y>=GY){p.y=GY;p.vy=0;p.g=true}
if(p.hp>0)p.hp-=dt;p.ph+=dt*Math.abs(p.vx)/20;
p.an=!p.g?'jump':Math.abs(p.vx)>25?'walk':p.hp>0?'happy':'idle';
cam+=(Math.max(0,Math.min(WORLD-W,p.x-W*.42+p.f*60))-cam)*Math.min(1,dt*5);
const nb=OBJ.find(b=>!b.done&&Math.abs(b.x-p.x)<140)||null;if(nb!==near){near=nb;$('pr').style.display=nb?'block':'none';if(nb)sfx('c')}
const z=Math.max(0,Math.min(4,p.x/1000|0));if(z!==curZ){curZ=z;$('zn').textContent=ZN[z];if(!seen[z]){seen[z]=1;const n=OBJ.find(b=>!b.done);if(z>0&&n)bubble(n.hint,5000,1)}}
if(d||!p.g||near)idle=0;else idle+=dt;
if(idle>8){idle=0;const n=OBJ.find(b=>!b.done);if(n)bubble(n.hint+(n.x>p.x?' Mari cari di hadapan!':' Mari cari di belakang!'),5000,1)}}
if(state==='modal'||state==='win')$('pr').style.display='none';
let last=performance.now();
function loop(n){const dt=Math.min(.05,(n-last)/1000);last=n;T+=dt;update(dt);if(state!=='play')$('pr').style.display='none';render(T);requestAnimationFrame(loop)}
requestAnimationFrame(loop);
// ---------- input ----------
addEventListener('keydown',e=>{const k={ArrowLeft:'l',ArrowRight:'r',Space:'j',ArrowUp:'j'}[e.code];if(k){K[k]=1;e.preventDefault()}if(e.code==='KeyE'&&!e.repeat)interact()});
addEventListener('keyup',e=>{const k={ArrowLeft:'l',ArrowRight:'r',Space:'j',ArrowUp:'j'}[e.code];if(k)K[k]=0});
addEventListener('blur',()=>K={});
[['bl','l'],['br','r'],['bj','j']].forEach(a=>{const b=$(a[0]);b.addEventListener('pointerdown',e=>{e.preventDefault();K[a[1]]=1});['pointerup','pointerleave','pointercancel'].forEach(v=>b.addEventListener(v,()=>K[a[1]]=0))});
$('be').addEventListener('pointerdown',e=>{e.preventDefault();interact()});$('pr').onclick=interact;
document.addEventListener('click',e=>{if(e.target.closest('.btn'))sfx('c')});
$('bPlay').onclick=start;$('bAgain').onclick=start;
$('bHow').onclick=()=>{hide($('home'));show($('how'))};$('bCred').onclick=()=>{hide($('home'));show($('cred'))};
document.querySelectorAll('[data-back]').forEach(b=>b.onclick=()=>{hide($('how'));hide($('cred'));show($('home'))});
$('bAch').onclick=()=>{$('al').innerHTML=OBJ.map(b=>(b.done?'✅ ':'⬜ ')+b.ico+' '+b.t).join('<br>')+'<br>⭐ Bintang: '+stars+'/5';hide($('win'));show($('ach'))};
$('aB').onclick=()=>{hide($('ach'));show($('win'))};
$('bs').onclick=()=>{snd=!snd;$('bs').textContent=snd?'🔊':'🔇';if(!snd&&window.speechSynthesis)speechSynthesis.cancel()};
$('bm').onclick=()=>{mus=!mus;$('bm').style.opacity=mus?1:.4;ac();musicLoop()};
$('bf').onclick=()=>{try{if(document.fullscreenElement||document.webkitFullscreenElement)(document.exitFullscreen||document.webkitExitFullscreen).call(document);else{const r=document.documentElement;(r.requestFullscreen||r.webkitRequestFullscreen).call(r)}}catch(e){}};
</script></body></html>
