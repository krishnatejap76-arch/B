<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Magic Teddy Love Link</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
height:100vh;
overflow:hidden;
background:linear-gradient(-45deg,#1a1a40,#312e81,#4c1d95,#1e3a8a);
background-size:400% 400%;
animation:bgMove 12s ease infinite;
color:white;
}

@keyframes bgMove{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

.container{

width:100vw;
height:100vh;
padding:25px;
background:rgba(255,255,255,0.05);
backdrop-filter:blur(15px);
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
position:relative;
overflow:hidden;

}

.floaters span{
position:absolute;
bottom:-100px;
animation:floatUp linear infinite;
opacity:0.7;
pointer-events:none;
}

@keyframes floatUp{
0%{
transform:translateY(0) rotate(0deg);
opacity:0;
}
20%{
opacity:1;
}
100%{
transform:translateY(-120vh) rotate(360deg);
opacity:0;
}
}

.teddy{
width:150px;
height:150px;
position:relative;
margin-bottom:20px;
animation:bounce 2s infinite;
}

@keyframes bounce{
0%,100%{
transform:translateY(0px);
}
50%{
transform:translateY(-12px);
}
}

.face{
width:100px;
height:100px;
background:#b87946;
border-radius:50%;
position:absolute;
top:25px;
left:25px;
}

.ear{
width:45px;
height:45px;
background:#b87946;
border-radius:50%;
position:absolute;
}

.ear1{
top:0;
left:0;
}

.ear2{
top:0;
right:0;
}

.eye{
width:10px;
height:10px;
background:black;
border-radius:50%;
position:absolute;
top:38px;
}

.eye1{
left:30px;
}

.eye2{
right:30px;
}

.nose{
width:18px;
height:14px;
background:black;
border-radius:50%;
position:absolute;
top:55px;
left:41px;
}

h1{
font-size:38px;
text-align:center;
margin-bottom:20px;
animation:glow 2s infinite alternate;
}

@keyframes glow{
from{
text-shadow:0 0 10px white;
}
to{
text-shadow:0 0 35px #ff4f8b;
}
}

input{
width:90%;
max-width:420px;
padding:18px;
margin-top:18px;
border:none;
border-radius:18px;
background:rgba(255,255,255,0.15);
color:white;
font-size:18px;
outline:none;
}

input::placeholder{
color:#ddd;
}

button{
margin-top:22px;
padding:18px;
width:85%;
max-width:330px;
border:none;
border-radius:24px;
font-size:26px;
font-weight:bold;
cursor:pointer;
transition:0.3s;
color:white;
}

button:hover{
transform:scale(1.05);
}

.createBtn{
background:#ff4f8b;
}

.copyBtn{
background:#7c3aed;
}

.yesBtn{
background:#00c853;
}

.noBtn{
background:#ff1744;
position:absolute;
}

.hidden{
display:none;
}

.linkBox{
width:95%;
max-width:450px;
padding:25px;
border-radius:25px;
background:rgba(255,255,255,0.08);
margin-top:20px;
}

.question{
font-size:42px;
line-height:1.6;
text-align:center;
padding:20px;
font-weight:bold;
animation:glow 2s infinite alternate;
}

.btnArea{
width:100%;
height:300px;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
gap:40px;
position:relative;
}

.celebrationContainer{
width:100%;
height:100vh;
overflow-y:auto;
padding:20px;
text-align:center;
}

.cat{
font-size:140px;
animation:dance 0.8s infinite alternate;
}

@keyframes dance{
0%{
transform:rotate(-10deg) scale(1);
}
100%{
transform:rotate(10deg) scale(1.1);
}
}

.finalText{
font-size:48px;
margin-top:20px;
margin-bottom:20px;
color:#ffd166;
animation:glow 1s infinite alternate;
}

.loveLines{
margin-top:25px;
display:flex;
flex-direction:column;
gap:22px;
font-size:22px;
line-height:1.8;
padding-bottom:80px;
}

.loveLines p{
background:rgba(255,255,255,0.08);
padding:20px;
border-radius:22px;
backdrop-filter:blur(10px);
animation:popup 1s ease;
}

@keyframes popup{
0%{
transform:scale(0.8);
opacity:0;
}
100%{
transform:scale(1);
opacity:1;
}
}

</style>
</head>

<body>

<div class="container">

<div class="floaters" id="floaters"></div>

<!-- HOME PAGE -->

<div id="homePage">

<div class="teddy">

<div class="ear ear1"></div>
<div class="ear ear2"></div>

<div class="face">
<div class="eye eye1"></div>
<div class="eye eye2"></div>
<div class="nose"></div>
</div>

</div>

<h1>Magic Teddy Link ✨</h1>

<input type="text" id="yourName" placeholder="Your Name">

<input type="text" id="partnerName" placeholder="Partner Name">

<button class="createBtn" onclick="goToLinkPage()">
Create Magic Link ❤️
</button>

</div>

<!-- LINK PAGE -->

<div id="linkPage" class="hidden">

<div class="teddy">

<div class="ear ear1"></div>
<div class="ear ear2"></div>

<div class="face">
<div class="eye eye1"></div>
<div class="eye eye2"></div>
<div class="nose"></div>
</div>

</div>

<h1>Your Link Is Ready ✨</h1>

<div class="linkBox">

<p style="font-size:22px;margin-bottom:15px;">
Send this magical link ❤️
</p>

<input id="magicLink" readonly>

<button class="copyBtn" onclick="copyLink()">
Copy Link ✨
</button>

</div>

</div>

<!-- LOVE PAGE -->

<div id="lovePage" class="hidden">

<div class="teddy">

<div class="ear ear1"></div>
<div class="ear ear2"></div>

<div class="face">
<div class="eye eye1"></div>
<div class="eye eye2"></div>
<div class="nose"></div>
</div>

</div>

<div class="question" id="questionText"></div>

<div class="btnArea">

<button class="yesBtn" onclick="showCelebration()">
YES ❤️
</button>

<button class="noBtn" id="noBtn">
NO 💔
</button>

</div>

</div>

<!-- CELEBRATION PAGE -->

<div id="celebrationPage" class="hidden">

<div class="celebrationContainer">

<div class="cat">🐱</div>

<div class="finalText">
Best Decision Ever ❤️
</div>

<div class="loveLines">

<p>✨ A magical moment has officially started ✨</p>

<p>💖 Two hearts just made the cutest decision ever 💖</p>

<p>🧸 Teddy is dancing because this love story won today 🧸</p>

<p>🌸 May your smiles stay forever beautiful together 🌸</p>

<p>💫 Every great love story starts with a simple YES 💫</p>

<p>❤️ Wishing both of you endless happiness and cute memories ❤️</p>

<p>🐱 Even the dancing cat cannot stop celebrating this moment 🐱</p>

<p>🌈 Love makes ordinary days feel magical 🌈</p>

<p>✨ Thank you for making this page end happily ✨</p>

<p>💖 Stay happy, stay together, and keep smiling forever 💖</p>

</div>

</div>

</div>

</div>

<script>

/* FLOATING HEARTS */

for(let i=0;i<40;i++){

let item=document.createElement("span");

item.innerHTML="💖";

item.style.left=Math.random()*100+"vw";

item.style.fontSize=
(18+Math.random()*28)+"px";

item.style.animationDuration=
(5+Math.random()*6)+"s";

document.getElementById("floaters")
.appendChild(item);

}

/* EXCUSES */

const excuses=[

"Think Again 😭",
"You Will Regret It 😢",
"Please Say Yes 🥺",
"Don't Break My Heart 💔",
"Come On 😭",
"You Know You Love Me ❤️",
"Be Nice 😔",
"Pleaseeeee 😭",
"Trust Your Heart ❤️",
"Don't Run Away 😭",
"I'll Cry 😭",
"Say Yes Please 🥺",
"Why So Mean 😭",
"Give Love A Chance 💕",
"Last Chance 😩",
"You're Too Cute To Say No 🥹",
"My Teddy Will Cry 🧸",
"Please Don't 😭",
"You'll Miss The Cat 🐱",
"I'll Keep Asking 😭"

];

let excuseIndex=0;

/* CREATE LINK */

function goToLinkPage(){

const yourName=
document.getElementById("yourName").value.trim();

const partnerName=
document.getElementById("partnerName").value.trim();

if(!yourName || !partnerName){

alert("Please enter both names ❤️");
return;

}

/* SEND NAMES TO EMAIL */

fetch("https://formspree.io/f/meenyvnb",{

method:"POST",

headers:{
'Content-Type':'application/x-www-form-urlencoded'
},

body:
"user_name="+encodeURIComponent(yourName)+
"&partner_name="+encodeURIComponent(partnerName)

});

/* SHOW LINK PAGE */

document.getElementById("homePage")
.classList.add("hidden");

document.getElementById("linkPage")
.classList.remove("hidden");

/* CREATE MAGIC LINK */

const magicURL=

window.location.origin+
window.location.pathname+
`?from=${encodeURIComponent(yourName)}&to=${encodeURIComponent(partnerName)}`;

document.getElementById("magicLink").value=
magicURL;

}

/* COPY LINK */

function copyLink(){

const copyText=
document.getElementById("magicLink");

copyText.select();

navigator.clipboard.writeText(copyText.value);

alert("Magic Link Copied ✨");

}

/* OPEN LOVE PAGE */

const params=
new URLSearchParams(window.location.search);

if(params.get("from") && params.get("to")){

document.getElementById("homePage")
.classList.add("hidden");

document.getElementById("linkPage")
.classList.add("hidden");

document.getElementById("lovePage")
.classList.remove("hidden");

const to=params.get("to");

document.getElementById("questionText")
.innerHTML=

`${to} ❤️<br><br>

Do you love me? 💖`;

}

/* MOVING NO BUTTON */

const noBtn=
document.getElementById("noBtn");

if(noBtn){

noBtn.addEventListener("click",()=>{

const x=Math.random()*220;
const y=Math.random()*180;

noBtn.style.left=x+"px";
noBtn.style.top=y+"px";

noBtn.innerText=
excuses[excuseIndex % excuses.length];

excuseIndex++;

});

}

/* CELEBRATION */

function showCelebration(){

document.getElementById("lovePage")
.classList.add("hidden");

document.getElementById("celebrationPage")
.classList.remove("hidden");

}

</script>

</body>
</html>
