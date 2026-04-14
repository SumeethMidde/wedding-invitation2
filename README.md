<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sumeeth ❤️ Sumalatha</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400&display=swap" rel="stylesheet">

<style>

/* RESET */
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    overflow: hidden;
}

/* 🎬 INTRO */
.intro {
    position: fixed;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle, #2a1a3a, #000);
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: #e9d5ff;
    z-index: 10;
    cursor: pointer;
}

.intro h1 {
    font-family: 'Great Vibes', cursive;
    font-size: 55px;
}

.tap {
    margin-top: 15px;
    animation: blink 1.5s infinite;
}

@keyframes blink {
    50% {opacity: 0.3;}
}

/* 📜 MAIN SCENE */
.scene {
    display: none;
    height: 100vh;
    justify-content: center;
    align-items: center;
    background: linear-gradient(135deg, #f3e8ff, #ffffff);
}

/* 📜 SCROLL */
.scroll-box {
    width: 360px;
    height: 0;
    overflow: hidden;
    transition: height 1.5s ease;
    position: relative;
}

/* Tear effect */
.scroll-box::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 100%;
    background: white;
    top: 0;
    clip-path: polygon(0 0, 100% 0, 50% 0);
    transition: 1.5s;
    z-index: 2;
}

.scroll-box.open::before {
    clip-path: polygon(0 0, 100% 0, 50% 100%);
}

/* Paper */
.scroll {
    background: linear-gradient(#fff, #f8f5ff);
    padding: 20px;
    border-radius: 12px;
    text-align: center;
}

/* ✍️ HANDWRITING */
svg {
    width: 100%;
    height: 80px;
}

path {
    fill: none;
    stroke: #7e22ce;
    stroke-width: 2;
    stroke-dasharray: 500;
    stroke-dashoffset: 500;
    animation: write 4s forwards;
}

@keyframes write {
    to { stroke-dashoffset: 0; }
}

/* 💑 COUPLE SCENE */
.scene-wrapper {
    position: relative;
    height: 220px;
    border-radius: 10px;
    overflow: hidden;
}

/* Church */
.church-bg {
    position: absolute;
    width: 100%;
    height: 100%;
    background: url('https://images.unsplash.com/photo-1504198453319-5ce911bafcde') center/cover;
    animation: zoom 20s infinite alternate;
}

@keyframes zoom {
    from { transform: scale(1); }
    to { transform: scale(1.08); }
}

/* Couple */
.couple {
    position: absolute;
    bottom: 0;
    width: 100%;
    display: flex;
    justify-content: center;
    gap: 20px;
}

/* Groom */
.groom img {
    width: 100px;
    animation: groom 4s infinite;
}

@keyframes groom {
    50% { transform: translateY(-5px) rotate(1deg); }
}

/* Bride */
.bride {
    position: relative;
}

.bride img {
    width: 100px;
}

/* Veil */
.veil {
    position: absolute;
    top: 0;
    left: 20px;
    width: 70px;
    height: 50px;
    background: rgba(255,255,255,0.5);
    border-radius: 50%;
    animation: veil 3s infinite;
}

@keyframes veil {
    50% { transform: translateX(10px); }
}

/* Saree */
.saree {
    position: absolute;
    bottom: 0;
    left: 10px;
    width: 80px;
    height: 50px;
    background: linear-gradient(45deg, pink, transparent);
    border-radius: 50%;
    animation: saree 3s infinite;
}

@keyframes saree {
    50% { transform: skewX(8deg); }
}

/* 🌹 PETALS */
.petal {
    position: fixed;
    width: 10px;
    height: 14px;
    background: radial-gradient(circle, #ffb6c1, #e11d48);
    border-radius: 50%;
    animation: fall linear forwards;
}

@keyframes fall {
    to { transform: translateY(100vh); opacity: 0; }
}

/* 🕊️ DOVES */
.dove {
    position: fixed;
    width: 25px;
    height: 25px;
    background: white;
    clip-path: polygon(0 50%, 50% 0, 100% 50%, 50% 100%);
    animation: fly 10s linear;
}

@keyframes fly {
    from { transform: translateX(-10vw); }
    to { transform: translateX(110vw); }
}

/* BUTTON */
button {
    margin-top: 10px;
    padding: 10px 18px;
    border: none;
    border-radius: 20px;
    background: #d4af37;
    color: white;
}

</style>
</head>

<body>

<!-- 🎬 INTRO -->
<div class="intro" onclick="start()">
    <h1>Sumeeth & Sumalatha</h1>
    <div class="tap">Tap to Open</div>
</div>

<!-- 📜 MAIN -->
<div class="scene" id="scene">

<div class="scroll-box" id="scrollBox">

<div class="scroll">

<p><b>By the Grace of God</b></p>

<!-- ✍️ Names -->
<svg viewBox="0 0 500 100">
<path d="M10 50 Q 100 10 200 50 T 400 50"/>
</svg>

<!-- 💑 Couple -->
<div class="scene-wrapper">

<div class="church-bg"></div>

<div class="couple">

<div class="groom">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140047.png">
</div>

<div class="bride">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140048.png">
<div class="veil"></div>
<div class="saree"></div>
</div>

</div>
</div>

<p>
💒 30 April 2026 | 2:30 PM<br>
Bengaluru
</p>

<button onclick="map()">📍 Location</button>
<button onclick="rsvp()">RSVP</button>

<p>“Faith, Hope & Love — the greatest is Love”</p>

</div>
</div>
</div>

<audio id="music" loop>
<source src="https://www.bensound.com/bensound-music/bensound-love.mp3">
</audio>

<script>

function start(){
document.querySelector(".intro").style.display="none";
document.getElementById("scene").style.display="flex";

let box=document.getElementById("scrollBox");
box.style.height="520px";

setTimeout(()=>box.classList.add("open"),300);

document.getElementById("music").play();
petals();
doves();
}

function petals(){
setInterval(()=>{
let p=document.createElement("div");
p.className="petal";
p.style.left=Math.random()*100+"vw";
p.style.animationDuration=(4+Math.random()*3)+"s";
document.body.appendChild(p);
setTimeout(()=>p.remove(),7000);
},300);
}

function doves(){
setInterval(()=>{
let d=document.createElement("div");
d.className="dove";
d.style.top=Math.random()*80+"vh";
document.body.appendChild(d);
setTimeout(()=>d.remove(),10000);
},3000);
}

function map(){
window.open("https://www.google.com/maps/search/?api=1&query=Richmond+Town+Methodist+Church+Bangalore");
}

function rsvp(){
window.open("https://wa.me/919880987361");
}

</script>

</body>
</html>
