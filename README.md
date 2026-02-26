<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Favour @15</title>

<style>
body{
margin:0;
overflow:hidden;
font-family:Arial, sans-serif;
background: linear-gradient(135deg,#0a0f3c,#2b0f54,#3d0f4f,#140a2e,#1a0f3d);
background-size:400% 400%;
animation: marble 18s ease infinite;
color:white;
text-align:center;
transition:background 0.5s, opacity 0.8s;
}

@keyframes marble{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

.page{
position:absolute;
width:100%;
height:100%;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
padding:20px;
}

h1,h2,p{
font-weight:900;
margin:15px 0;
}

h1{font-size:60px;}
h2{font-size:50px;}
p{font-size:30px;max-width:80%;}

button{
padding:22px 50px;
font-size:30px;
font-weight:900;
border:none;
border-radius:15px;
margin:20px;
cursor:pointer;
background:#111;
color:white;
transition:transform 0.2s;
}

button:hover{
transform:scale(1.1);
}

/* GOLD FLASH */
.flashGold{
animation: goldFlash 0.6s;
}

@keyframes goldFlash{
0%{background:#000;}
50%{background:#6b5b00;}
100%{background: linear-gradient(135deg,#0a0f3c,#2b0f54,#3d0f4f,#140a2e,#1a0f3d);}
}

/* RED FLASH */
.flashRed{
animation: redFlash 0.6s;
}

@keyframes redFlash{
0%{background:#000;}
50%{background:#5c0000;}
100%{background: linear-gradient(135deg,#0a0f3c,#2b0f54,#3d0f4f,#140a2e,#1a0f3d);}
}

/* Vibrate */
.vibrate{
animation: vibrate 0.3s linear infinite;
}

@keyframes vibrate{
0%{transform:translate(3px,3px);}
25%{transform:translate(-3px,-3px);}
50%{transform:translate(3px,-3px);}
75%{transform:translate(-3px,3px);}
100%{transform:translate(3px,3px);}
}

/* Floating objects */
.float{
position:absolute;
font-size:55px;
animation: fall linear infinite;
}

@keyframes fall{
0%{transform:translateY(-100px) rotate(0deg);}
100%{transform:translateY(110vh) rotate(360deg);}
}
</style>
</head>

<body>

<div id="page1" class="page">
<h1>IN A WORLD...</h1>
<h1>WHERE LEGENDS ARE BORN...</h1>
<button onclick="nextPage()">REVEAL HER DESTINY</button>
</div>

<div id="page2" class="page" style="display:none;">
<h2>🔴SYSTEM UPDATE COMPLETE🔴 ✅</h2>
<h2>FAVOUR 14❌... 15✅💯</h2>
<h2>FAVOUR @15 INSTALLED</h2>

<h1>+1000 AURA</h1>
<h1>+500 BEAUTY</h1>
<h1>+INFINITE BLESSINGS</h1>

<button onclick="finalPage()">READ MESSAGE</button>
<button onclick="chaos()">DON'T PRESS THIS</button>
</div>

<div id="page3" class="page" style="display:none;">
<h1>Happy birthday, my nigga</h1>
<p>May your life be filled with peace, success and laughter.</p>
<p>May all you dreams come through for and may you always get the best of the world.</p>
<h1>LONG LIVE THE QUEEN 👑</h1>
</div>

<script>

function nextPage(){
document.getElementById("page1").style.display="none";
document.getElementById("page2").style.display="flex";

document.body.classList.add("flashGold");
setTimeout(()=>document.body.classList.remove("flashGold"),600);

createChaos();
}

function finalPage(){
document.getElementById("page2").style.display="none";
document.getElementById("page3").style.display="flex";

document.body.classList.add("flashGold");
setTimeout(()=>document.body.classList.remove("flashGold"),600);
}

function chaos(){
document.body.classList.add("flashRed");

setTimeout(()=>{
document.body.classList.remove("flashRed");
document.body.classList.add("vibrate");

setTimeout(()=>{
document.body.style.opacity="0";
},900);

},600);
}

function createChaos(){
for(let i=0;i<70;i++){

let item=document.createElement("div");
item.className="float";

let emojis=["🎉","💜","🎈"];
item.innerHTML=emojis[Math.floor(Math.random()*emojis.length)];

item.style.left=Math.random()*100+"vw";
item.style.animationDuration=(Math.random()*3+3)+"s";

document.body.appendChild(item);
}
}

</script>

</body>
</html>
