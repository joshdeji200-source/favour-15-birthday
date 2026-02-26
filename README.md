<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Favour @15</title>

<style>
body{
margin:0;
overflow:hidden;
font-family:Impact, Arial Black, sans-serif;
background: linear-gradient(135deg,#0a0f3c,#2b0f54,#3d0f4f,#140a2e,#1a0f3d);
background-size:400% 400%;
animation: marble 20s ease infinite;
color:white;
text-align:center;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
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
text-align:center;
}

h1,h2,p{
font-weight:900;
margin:20px 0;
text-align:center;
}

h1{font-size:75px;}
h2{font-size:60px;}
p{font-size:40px; max-width:90%;}

button{
padding:25px 60px;
font-size:35px;
font-weight:900;
border:none;
border-radius:18px;
margin:25px;
cursor:pointer;
background:#111;
color:white;
}

button:hover{
transform:scale(1.1);
}

/* GOLD FLASH */
.flashGold{
animation: goldFlash 0.7s;
}

@keyframes goldFlash{
0%{background:#000;}
50%{background:#5f5200;}
100%{background: linear-gradient(135deg,#0a0f3c,#2b0f54,#3d0f4f,#140a2e,#1a0f3d);}
}

/* RED FLASH */
.flashRed{
animation: redFlash 0.7s;
}

@keyframes redFlash{
0%{background:#000;}
50%{background:#4d0000;}
100%{background: linear-gradient(135deg,#0a0f3c,#2b0f54,#3d0f4f,#140a2e,#1a0f3d);}
}

/* Vibrate */
.vibrate{
animation: vibrate 0.3s linear infinite;
}

@keyframes vibrate{
0%{transform:translate(4px,4px);}
25%{transform:translate(-4px,-4px);}
50%{transform:translate(4px,-4px);}
75%{transform:translate(-4px,4px);}
100%{transform:translate(4px,4px);}
}

/* Floating objects */
.float{
position:absolute;
font-size:70px;
animation: fall linear infinite;
}

@keyframes fall{
0%{transform:translateY(-120px) rotate(0deg);}
100%{transform:translateY(120vh) rotate(360deg);}
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
<h1>HAPPY BIRTHDAY, MY NIGGA</h1>
<p>MAY YOUR LIFE BE FILLED WITH PEACE, SUCCESS AND LAUGHTER.</p>
<p>MAY ALL YOU DREAMS COME THROUGH FOR AND MAY YOU ALWAYS GET THE BEST OF THE WORLD.</p>
<h1>LONG LIVE THE QUEEN 👑</h1>
</div>

<script>

function nextPage(){
document.getElementById("page1").style.display="none";
document.getElementById("page2").style.display="flex";

document.body.classList.add("flashGold");
setTimeout(()=>document.body.classList.remove("flashGold"),700);

createChaos();
}

function finalPage(){
document.getElementById("page2").style.display="none";
document.getElementById("page3").style.display="flex";

document.body.classList.add("flashGold");
setTimeout(()=>document.body.classList.remove("flashGold"),700);
}

function chaos(){
document.body.classList.add("flashRed");

setTimeout(()=>{
document.body.classList.remove("flashRed");
document.body.classList.add("vibrate");

setTimeout(()=>{
document.body.style.opacity="0";
},1000);

},700);
}

function createChaos(){
for(let i=0;i<80;i++){

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
