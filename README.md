<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>KAPTEN STORE</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{
font-family:Arial,sans-serif;
background:#080b12;color:#fff;
overflow-x:hidden;
transition:.3s
}
button,input,select{font:inherit}
button{cursor:pointer;border:0}
.hidden{display:none!important}

/* INTRO */
#intro{
position:fixed;inset:0;z-index:9999;
background:#080b12;
display:flex;align-items:center;justify-content:center;
text-align:center;
transition:.6s ease
}
.introBox{animation:intro .8s ease}
.logo{
width:82px;height:82px;border-radius:25px;
display:flex;align-items:center;justify-content:center;
margin:auto;
font-size:52px;font-weight:900;
background:linear-gradient(135deg,#00e5ff,#6c3cff);
box-shadow:0 0 35px #00d9ff55;
animation:float 2s infinite ease-in-out
}
.introTitle{
font-size:27px;font-weight:900;
margin-top:18px;
letter-spacing:2px
}
.introSub{color:#8993a8;margin:8px 0 25px}
.enter{
padding:13px 35px;border-radius:14px;
background:#00d9ff;color:#001018;
font-weight:900;
box-shadow:0 8px 25px #00d9ff33;
transition:.2s
}
.enter:active{transform:scale(.92)}

@keyframes intro{
from{opacity:0;transform:translateY(25px) scale(.94)}
to{opacity:1;transform:none}
}
@keyframes float{
50%{transform:translateY(-7px)}
}

/* APP */
#app{min-height:100vh}
header{
position:sticky;top:0;z-index:50;
padding:14px;
background:#0c111b;
border-bottom:1px solid #202838;
display:flex;align-items:center;gap:12px
}
.headerLogo{
width:42px;height:42px;border-radius:13px;
background:linear-gradient(135deg,#00e5ff,#693cff);
display:flex;align-items:center;justify-content:center;
font-size:26px;font-weight:900
}
.headText b{font-size:17px}
.headText small{display:block;color:#7e8a9e;margin-top:2px}

.page{padding:15px 15px 95px;max-width:700px;margin:auto}
.section{display:none}
.section.active{
display:block;
animation:pageIn .35s ease
}
@keyframes pageIn{
from{opacity:0;transform:translateY(12px)}
to{opacity:1;transform:none}
}

/* SEARCH */
.search{
width:100%;padding:13px 15px;
border-radius:15px;border:1px solid #273143;
background:#101621;color:#fff;
outline:none;margin-bottom:15px
}
.search:focus{border-color:#00d9ff}

/* BANNER */
.banner{
padding:20px;border-radius:20px;
background:linear-gradient(135deg,#101e30,#15102b);
border:1px solid #253650;
margin-bottom:18px;
overflow:hidden;position:relative
}
.banner:after{
content:"";
position:absolute;width:120px;height:120px;
right:-40px;top:-40px;
border-radius:50%;background:#00d9ff18;
animation:float 3s infinite
}
.banner h2{font-size:22px;margin-bottom:7px}
.banner p{color:#9ba7ba;font-size:13px}

/* GRID */
.grid{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:11px
}
.card{
background:#101621;
border:1px solid #202b3d;
border-radius:18px;
padding:15px;
transition:.25s;
animation:cardIn .4s both
}
.card:nth-child(2){animation-delay:.04s}
.card:nth-child(3){animation-delay:.08s}
.card:nth-child(4){animation-delay:.12s}
.card:nth-child(5){animation-delay:.16s}
.card:active{transform:scale(.96)}
.card:hover{border-color:#00d9ff66}
.gameIcon{
height:65px;border-radius:15px;
display:flex;align-items:center;justify-content:center;
font-size:35px;margin-bottom:10px;
background:#182131
}
.card h3{font-size:14px}
.card p{color:#7f8ba0;font-size:12px;margin-top:4px}
@keyframes cardIn{
from{opacity:0;transform:translateY(12px)}
to{opacity:1;transform:none}
}

/* BUTTONS */
.btn{
width:100%;padding:12px;
border-radius:12px;
background:#00d9ff;color:#001018;
font-weight:800;margin-top:10px;
transition:.2s
}
.btn:active{transform:scale(.96)}
.btn.secondary{
background:#182131;color:#fff;
border:1px solid #29364b
}
.btn.red{background:#ff4d67;color:#fff}

/* MENU */
.menuGrid{
display:grid;
grid-template-columns:repeat(3,1fr);
gap:9px;margin-bottom:18px
}
.menuBtn{
padding:13px 5px;border-radius:15px;
background:#101621;border:1px solid #202b3d;
color:#fff;font-size:11px;
transition:.2s
}
.menuBtn span{display:block;font-size:22px;margin-bottom:5px}
.menuBtn:active{transform:scale(.91)}

/* FORM */
.form{
background:#101621;border:1px solid #202b3d;
padding:16px;border-radius:18px
}
.form h2{margin-bottom:13px}
label{
display:block;color:#8d99ac;
font-size:12px;margin:12px 0 6px
}
input,select{
width:100%;padding:12px;
background:#080d15;
border:1px solid #273143;
border-radius:12px;
color:#fff;outline:none
}

/* PRODUCT */
.product{
display:flex;gap:12px;
padding:13px;
background:#101621;
border:1px solid #202b3d;
border-radius:16px;
margin-bottom:10px;
align-items:center
}
.productIcon{
width:48px;height:48px;border-radius:13px;
display:flex;align-items:center;justify-content:center;
font-size:25px;background:#192334
}
.productInfo{flex:1}
.productInfo b{font-size:14px}
.productInfo small{
display:block;color:#8590a3;margin-top:4px
}
.price{color:#00e5ff;font-weight:900}

/* PROFILE */
.profile{
text-align:center;
background:#101621;
border:1px solid #202b3d;
border-radius:20px;padding:22px
}
.avatar{
width:75px;height:75px;border-radius:50%;
margin:auto;
display:flex;align-items:center;justify-content:center;
font-size:35px;
background:linear-gradient(135deg,#00d9ff,#693cff)
}
.profile h2{margin-top:10px}
.profile small{color:#8994a8}
.stats{
display:grid;grid-template-columns:repeat(3,1fr);
gap:8px;margin-top:18px
}
.stat{
background:#182131;padding:12px;border-radius:13px
}
.stat b{display:block;color:#00d9ff}
.stat small{font-size:10px}

/* FAVORITE */
.fav{
color:#ff4e76;
font-size:22px;
float:right;
background:none
}

/* BOTTOM */
nav{
position:fixed;bottom:0;left:0;right:0;
z-index:100;
background:#0c111b;
border-top:1px solid #202838;
display:grid;grid-template-columns:repeat(5,1fr);
padding:7px 4px
}
nav button{
background:none;color:#68758a;
font-size:10px;padding:5px;
transition:.2s
}
nav span{display:block;font-size:20px;margin-bottom:2px}
nav button.active{color:#00d9ff;transform:translateY(-3px)}

/* TOAST */
#toast{
position:fixed;
left:50%;bottom:85px;
transform:translateX(-50%) translateY(20px);
background:#182131;
border:1px solid #30405a;
padding:11px 17px;border-radius:13px;
font-size:12px;
opacity:0;pointer-events:none;
transition:.3s;z-index:999
}
#toast.show{
opacity:1;transform:translateX(-50%) translateY(0)
}

/* MODAL */
.modal{
position:fixed;inset:0;
background:#0009;z-index:500;
display:none;align-items:flex-end
}
.modal.show{display:flex}
.modalBox{
width:100%;max-width:700px;margin:auto;
background:#101621;
border:1px solid #29364b;
border-radius:22px 22px 0 0;
padding:20px;
animation:modalIn .3s ease
}
@keyframes modalIn{
from{transform:translateY(100%)}
to{transform:none}
}
.close{
float:right;background:#202b3d;
color:#fff;border-radius:10px;
padding:6px 10px
}

/* LIGHT MODE */
body.light{
background:#f2f5f9;color:#111
}
body.light header,
body.light nav,
body.light .card,
body.light .banner,
body.light .form,
body.light .product,
body.light .profile,
body.light .menuBtn,
body.light .modalBox{
background:#fff;border-color:#dce2ea
}
body.light .search,
body.light input,
body.light select{
background:#fff;color:#111;border-color:#ccd4df
}
body.light .gameIcon,
body.light .productIcon,
body.light .stat{
background:#eef2f7
}
</style>
</head>

<body>

<!-- INTRO -->
<div id="intro">
<div class="introBox">
<div class="logo">K</div>
<div class="introTitle">KAPTEN STORE</div>
<div class="introSub">Marketplace Game • Cepat • Praktis</div>
<button class="enter" onclick="masuk()">MASUK KE STORE</button>
</div>
</div>

<div id="app" class="hidden">

<header>
<div class="headerLogo">K</div>
<div class="headText">
<b>KAPTEN STORE</b>
<small>Marketplace Game</small>
</div>
</header>

<div class="page">

<!-- HOME -->
<section id="home" class="section active">

<div class="banner">
<h2>🔥 KAPTEN STORE</h2>
<p>Beli akun, jual akun, dan top up game dalam satu tempat.</p>
</div>

<input class="search" id="search"
placeholder="🔎 Cari game..."
oninput="cariGame()">

<div class="menuGrid">
<button class="menuBtn" onclick="page('beli')"><span>🛒</span>Beli</button>
<button class="menuBtn" onclick="page('jual')"><span>💰</span>Jual</button>
<button class="menuBtn" onclick="page('topup')"><span>⚡</span>Top Up</button>
<button class="menuBtn" onclick="page('fav')"><span>❤️</span>Favorit</button>
<button class="menuBtn" onclick="page('promo')"><span>🎟️</span>Promo</button>
<button class="menuBtn" onclick="page('reward')"><span>🎁</span>Reward</button>
</div>

<h3 style="margin-bottom:12px">🎮 Pilih Game</h3>

<div class="grid" id="gameGrid">

<div class="card game" data-name="mobile legends">
<button class="fav" onclick="favorite('Mobile Legends')">♡</button>
<div class="gameIcon">⚔️</div>
<h3>Mobile Legends</h3>
<p>Akun • Top Up</p>
<button class="btn" onclick="pilihGame('Mobile Legends')">Lihat</button>
</div>

<div class="card game" data-name="free fire">
<button class="fav" onclick="favorite('Free Fire')">♡</button>
<div class="gameIcon">🔥</div>
<h3>Free Fire</h3>
<p>Akun • Top Up</p>
<button class="btn" onclick="pilihGame('Free Fire')">Lihat</button>
</div>

<div class="card game" data-name="roblox">
<button class="fav" onclick="favorite('Roblox')">♡</button>
<div class="gameIcon">🟥</div>
<h3>Roblox</h3>
<p>Akun • Robux</p>
<button class="btn" onclick="pilihGame('Roblox')">Lihat</button>
</div>

<div class="card game" data-name="pubg mobile">
<button class="fav" onclick="favorite('PUBG Mobile')">♡</button>
<div class="gameIcon">🔫</div>
<h3>PUBG Mobile</h3>
<p>Akun • UC</p>
<button class="btn" onclick="pilihGame('PUBG Mobile')">Lihat</button>
</div>

<div class="card game" data-name="minecraft">
<button class="fav" onclick="favorite('Minecraft')">♡</button>
<div class="gameIcon">⛏️</div>
<h3>Minecraft</h3>
<p>Akun • Game</p>
<button class="btn" onclick="pilihGame('Minecraft')">Lihat</button>
</div>

</div>
</section>

<!-- BELI -->
<section id="beli" class="section">
<h2>🛒 Beli Akun</h2>
<p style="color:#8994a8;margin:6px 0 15px">Pilih game yang ingin dicari.</p>

<div class="product">
<div class="productIcon">🔥</div>
<div class="productInfo">
<b>Free Fire</b>
<small>Akun random • Siap dimainkan</small>
</div>
<div class="price">Rp50K</div>
</div>

<div class="product">
<div class="productIcon">⚔️</div>
<div class="productInfo">
<b>Mobile Legends</b>
<small>Akun dengan koleksi skin</small>
</div>
<div class="price">Rp75K</div>
</div>

<div class="product">
<div class="productIcon">🟥</div>
<div class="productInfo">
<b>Roblox</b>
<small>Akun Roblox</small>
</div>
<div class="price">Rp40K</div>
</div>

<button class="btn" onclick="pesan('Beli akun game')">💬 Pesan via WhatsApp</button>
</section>

<!-- JUAL -->
<section id="jual" class="section">
<div class="form">
<h2>💰 Jual Akun</h2>

<label>Game</label>
<select id="jualGame">
<option>Mobile Legends</option>
<option>Free Fire</option>
<option>Roblox</option>
<option>PUBG Mobile</option>
<option>Minecraft</option>
</select>

<label>Nama akun</label>
<input id="jualNama" placeholder="Nama akun">

<label>Harga yang diinginkan</label>
<input id="jualHarga" type="number" placeholder="Contoh: 100000">

<label>Deskripsi</label>
<input id="jualDesc" placeholder="Contoh: banyak skin">

<button class="btn" onclick="jualAkun()">📤 Ajukan Penjualan</button>
</div>
</section>

<!-- TOPUP -->
<section id="topup" class="section">
<div class="form">
<h2>⚡ Top Up Game</h2>

<label>Game</label>
<select id="topGame">
<option>Mobile Legends</option>
<option>Free Fire</option>
<option>Roblox</option>
<option>PUBG Mobile</option>
</select>

<label>ID Game</label>
<input id="gameID" placeholder="Masukkan ID">

<label>Nominal</label>
<select id="nominal">
<option>Rp10.000</option>
<option>Rp20.000</option>
<option>Rp50.000</option>
<option>Rp100.000</option>
<option>Rp200.000</option>
</select>

<button class="btn" onclick="topup()">⚡ Lanjut Top Up</button>
</div>
</section>

<!-- FAVORIT -->
<section id="fav" class="section">
<h2>❤️ Favorit</h2>
<p style="color:#8994a8;margin:7px 0 15px">
Game favorit kamu.
</p>
<div id="favList"></div>
</section>

<!-- PROMO -->
<section id="promo" class="section">
<h2>🎟️ Promo</h2>

<div class="product">
<div class="productIcon">🔥</div>
<div class="productInfo">
<b>WELCOME10</b>
<small>Promo pengguna baru</small>
</div>
<button class="btn" style="width:auto" onclick="copyText('WELCOME10')">SALIN</button>
</div>

<div class="product">
<div class="productIcon">🎁</div>
<div class="productInfo">
<b>KAPTEN5</b>
<small>Voucher promo khusus</small>
</div>
<button class="btn" style="width:auto" onclick="copyText('KAPTEN5')">SALIN</button>
</div>
</section>

<!-- REWARD -->
<section id="reward" class="section">
<div class="profile">
<div class="avatar">🎁</div>
<h2>Reward Kamu</h2>
<p style="color:#8994a8;margin-top:5px">Kumpulkan poin dari aktivitas.</p>

<div class="stats">
<div class="stat"><b id="points">0</b><small>Poin</small></div>
<div class="stat"><b id="streak">1</b><small>Hari</small></div>
<div class="stat"><b>🎁</b><small>Reward</small></div>
</div>

<button class="btn" onclick="claimReward()">🎁 Ambil Reward</button>
</div>
</section>

<!-- PESANAN -->
<section id="pesanan" class="section">
<h2>📦 Pesanan</h2>
<div id="history"></div>
</section>

<!-- PROFIL -->
<section id="profil" class="section">
<div class="profile">
<div class="avatar">👤</div>
<h2 id="profileName">Pengguna</h2>
<small>Member KAPTEN STORE</small>

<div class="stats">
<div class="stat"><b id="orderCount">0</b><small>Pesanan</small></div>
<div class="stat"><b id="favCount">0</b><small>Favorit</small></div>
<div class="stat"><b id="coinCount">0</b><small>Koin</small></div>
</div>

<button class="btn secondary" onclick="editProfile()">✏️ Ganti Nama</button>
<button class="btn secondary" onclick="toggleTheme()">🌙 Ganti Tema</button>
<button class="btn red" onclick="clearData()">🗑️ Reset Data</button>
</div>
</section>

</div>

<!-- NAV -->
<nav>
<button class="active" onclick="page('home')"><span>🏠</span>Home</button>
<button onclick="page('beli')"><span>🛒</span>Beli</button>
<button onclick="page('topup')"><span>⚡</span>Top Up</button>
<button onclick="page('pesanan')"><span>📦</span>Pesanan</button>
<button onclick="page('profil')"><span>👤</span>Profil</button>
</nav>

</div>

<div id="toast">Berhasil!</div>

<script>
const WA="6282147990783";

let orders=JSON.parse(localStorage.getItem("kapten_orders")||"[]");
let favs=JSON.parse(localStorage.getItem("kapten_favs")||"[]");
let points=Number(localStorage.getItem("kapten_points")||0);
let name=localStorage.getItem("kapten_name")||"Pengguna";

document.getElementById("profileName").textContent=name;
updateStats();

function masuk(){
const intro=document.getElementById("intro");
intro.style.opacity="0";
intro.style.transform="scale(1.04)";
setTimeout(()=>{
intro.style.display="none";
document.getElementById("app").classList.remove("hidden");
},500);
}

function page(id){
document.querySelectorAll(".section").forEach(x=>x.classList.remove("active"));
document.getElementById(id).classList.add("active");

document.querySelectorAll("nav button").forEach(x=>x.classList.remove("active"));

const map={
home:0,beli:1,topup:2,pesanan:3,profil:4
};

if(map[id]!==undefined)
document.querySelectorAll("nav button")[map[id]].classList.add("active");

if(id==="pesanan")showHistory();
if(id==="fav")showFav();
}

function pilihGame(game){
toast("Memilih "+game);
page("beli");
}

function cariGame(){
let q=document.getElementById("search").value.toLowerCase();

document.querySelectorAll(".game").forEach(card=>{
let name=card.dataset.name;
card.style.display=name.includes(q)?"block":"none";
});
}

function favorite(game){
if(!favs.includes(game)){
favs.push(game);
toast(game+" masuk favorit ❤️");
}else{
favs=favs.filter(x=>x!==game);
toast(game+" dihapus dari favorit");
}

localStorage.setItem("kapten_favs",JSON.stringify(favs));
updateStats();
}

function showFav(){
let box=document.getElementById("favList");

if(!favs.length){
box.innerHTML='<div class="form"><p style="color:#8994a8">Belum ada game favorit.</p></div>';
return;
}

box.innerHTML=favs.map(g=>`
<div class="product">
<div class="productIcon">🎮</div>
<div class="productInfo">
<b>${g}</b>
<small>Game favorit</small>
</div>
<button class="btn" style="width:auto" onclick="pilihGame('${g}')">BUKA</button>
</div>
`).join("");
}

function pesan(text){
addOrder(text);
let url="https://wa.me/"+WA+"?text="+encodeURIComponent("Halo Admin KAPTEN STORE, saya ingin "+text+".");
window.open(url,"_blank");
}

function jualAkun(){
let game=document.getElementById("jualGame").value;
let nama=document.getElementById("jualNama").value;
let harga=document.getElementById("jualHarga").value;
let desc=document.getElementById("jualDesc").value;

if(!nama||!harga){
toast("Lengkapi data dulu!");
return;
}

let text=
"Saya ingin jual akun "+game+
"\nNama: "+nama+
"\nHarga: Rp"+harga+
"\nDeskripsi: "+desc;

addOrder("Jual akun "+game);

window.open(
"https://wa.me/"+WA+"?text="+encodeURIComponent(text),
"_blank"
);
}

function topup(){
let game=document.getElementById("topGame").value;
let id=document.getElementById("gameID").value;
let nominal=document.getElementById("nominal").value;

if(!id){
toast("Masukkan ID game!");
return;
}

let text=
"Saya ingin top up "+game+
"\nID: "+id+
"\nNominal: "+nominal;

addOrder("Top Up "+game+" "+nominal);

window.open(
"https://wa.me/"+WA+"?text="+encodeURIComponent(text),
"_blank"
);
}

function addOrder(text){
orders.unshift({
text:text,
date:new Date().toLocaleString("id-ID")
});

localStorage.setItem("kapten_orders",JSON.stringify(orders));

points+=10;
localStorage.setItem("kapten_points",points);

updateStats();
toast("Pesanan berhasil dicatat 📦");
}

function showHistory(){
let box=document.getElementById("history");

if(!orders.length){
box.innerHTML='<div class="form"><p style="color:#8994a8">Belum ada pesanan.</p></div>';
return;
}

box.innerHTML=orders.map((o,i)=>`
<div class="product">
<div class="productIcon">📦</div>
<div class="productInfo">
<b>${o.text}</b>
<small>${o.date}</small>
</div>
</div>
`).join("");
}

function editProfile(){
let n=prompt("Masukkan nama baru:",name);

if(n&&n.trim()){
name=n.trim();
localStorage.setItem("kapten_name",name);
document.getElementById("profileName").textContent=name;
toast("Nama berhasil diubah");
}
}

function claimReward(){
let today=new Date().toDateString();
let last=localStorage.getItem("kapten_reward");

if(last===today){
toast("Reward hari ini sudah diambil 🎁");
return;
}

points+=25;
localStorage.setItem("kapten_points",points);
localStorage.setItem("kapten_reward",today);

updateStats();
toast("+25 poin berhasil didapat 🎉");
}

function updateStats(){
document.getElementById("orderCount").textContent=orders.length;
document.getElementById("favCount").textContent=favs.length;
document.getElementById("coinCount").textContent=points;
document.getElementById("points").textContent=points;
}

function toggleTheme(){
document.body.classList.toggle("light");

localStorage.setItem(
"kapten_theme",
document.body.classList.contains("light")?"light":"dark"
);

toast("Tema diganti ✨");
}

if(localStorage.getItem("kapten_theme")==="light")
document.body.classList.add("light");

function copyText(text){
navigator.clipboard.writeText(text);
toast("Kode "+text+" disalin 🎟️");
}

function clearData(){
if(confirm("Hapus semua data KAPTEN STORE?")){
localStorage.clear();
location.reload();
}
}

function toast(text){
let t=document.getElementById("toast");
t.textContent=text;
t.classList.add("show");

clearTimeout(window.toastTimer);
window.toastTimer=setTimeout(()=>{
t.classList.remove("show");
},2200);
}
</script>

</body>
</html>
