<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>SHADAB AI</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
height:100vh;
overflow:hidden;
background:linear-gradient(135deg,#ffb6d9,#ffc2e2,#ffd4ec);
display:flex;
justify-content:center;
align-items:center;
position:relative;
}

/* Animated Background */

body::before{
content:'';
position:absolute;
width:200%;
height:200%;
background:
radial-gradient(circle at center,rgba(255,255,255,0.4),transparent 20%);
animation:moveBg 12s linear infinite;
}

@keyframes moveBg{
0%{
transform:translate(-10%,-10%) rotate(0deg);
}
100%{
transform:translate(-20%,-20%) rotate(360deg);
}
}

/* Main AI Box */

.ai-container{
position:relative;
width:95%;
max-width:1400px;
height:92vh;
background:rgba(255,255,255,0.18);
backdrop-filter:blur(18px);
border:1px solid rgba(255,255,255,0.25);
border-radius:35px;
overflow:hidden;
box-shadow:
0 10px 40px rgba(0,0,0,0.15),
inset 0 0 30px rgba(255,255,255,0.3);
display:flex;
flex-direction:column;
}

/* Header */

.header{
padding:25px 40px;
display:flex;
justify-content:space-between;
align-items:center;
border-bottom:1px solid rgba(255,255,255,0.2);
}

.logo{
font-size:40px;
font-weight:700;
letter-spacing:2px;
background:linear-gradient(90deg,#5a2d0c,#7a4318,#9f5c26);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
animation:glow 2s infinite alternate;
}

@keyframes glow{
from{
filter:drop-shadow(0 0 5px rgba(120,60,20,0.2));
}
to{
filter:drop-shadow(0 0 18px rgba(120,60,20,0.7));
}
}

/* Deep Think Buttons */

.top-buttons{
display:flex;
gap:15px;
}

.ai-btn{
padding:12px 22px;
border:none;
border-radius:18px;
background:rgba(255,255,255,0.25);
backdrop-filter:blur(8px);
font-size:15px;
font-weight:600;
cursor:pointer;
transition:0.4s;
color:#5c2e0f;
box-shadow:0 4px 15px rgba(0,0,0,0.08);
}

.ai-btn:hover{
transform:translateY(-5px) scale(1.05);
background:white;
}

/* Flower AI Center */

.center{
flex:1;
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
position:relative;
}

/* Flower */

.flower{
position:relative;
width:240px;
height:240px;
display:flex;
justify-content:center;
align-items:center;
animation:rotateFlower 20s linear infinite;
}

@keyframes rotateFlower{
100%{
transform:rotate(360deg);
}
}

.petal{
position:absolute;
width:90px;
height:90px;
background:linear-gradient(145deg,#ff4fa3,#ff8dc2);
border-radius:50%;
box-shadow:
0 0 25px rgba(255,0,128,0.5),
inset 0 0 20px rgba(255,255,255,0.5);
}

.petal:nth-child(1){top:0;left:75px;}
.petal:nth-child(2){bottom:0;left:75px;}
.petal:nth-child(3){left:0;top:75px;}
.petal:nth-child(4){right:0;top:75px;}
.petal:nth-child(5){top:25px;left:25px;}
.petal:nth-child(6){top:25px;right:25px;}
.petal:nth-child(7){bottom:25px;left:25px;}
.petal:nth-child(8){bottom:25px;right:25px;}

.flower-center{
position:absolute;
width:110px;
height:110px;
background:linear-gradient(145deg,#5a2d0c,#8a4d1d);
border-radius:50%;
display:flex;
justify-content:center;
align-items:center;
font-size:20px;
font-weight:700;
color:white;
box-shadow:
0 0 30px rgba(90,45,12,0.6);
animation:float 3s ease-in-out infinite;
}

@keyframes float{
0%,100%{
transform:translateY(0px);
}
50%{
transform:translateY(-10px);
}
}

/* AI Input */

.input-area{
padding:30px;
display:flex;
justify-content:center;
align-items:center;
gap:20px;
}

.ai-input{
width:70%;
height:65px;
border:none;
outline:none;
border-radius:20px;
padding:0 25px;
font-size:18px;
background:rgba(255,255,255,0.35);
backdrop-filter:blur(10px);
color:#5a2d0c;
box-shadow:0 4px 20px rgba(0,0,0,0.1);
}

.ai-input::placeholder{
color:#7d4d2f;
}

.send-btn{
width:65px;
height:65px;
border:none;
border-radius:20px;
cursor:pointer;
font-size:22px;
background:linear-gradient(145deg,#5a2d0c,#8a4d1d);
color:white;
transition:0.3s;
box-shadow:0 8px 25px rgba(90,45,12,0.4);
}

.send-btn:hover{
transform:scale(1.08);
}

/* AI Response */

.response-box{
position:absolute;
bottom:120px;
width:80%;
max-height:220px;
overflow:auto;
padding:25px;
background:rgba(255,255,255,0.18);
backdrop-filter:blur(10px);
border-radius:25px;
color:#5a2d0c;
font-size:18px;
line-height:1.7;
box-shadow:0 10px 25px rgba(0,0,0,0.08);
}

/* Mobile */

@media(max-width:768px){

.logo{
font-size:28px;
}

.ai-btn{
padding:10px 14px;
font-size:13px;
}

.flower{
transform:scale(0.8);
}

.ai-input{
width:65%;
font-size:15px;
}

}

</style>
</head>

<body>

<div class="ai-container">

<div class="header">

<div class="logo">
SHADAB AI
</div>

<div class="top-buttons">
<button class="ai-btn">Deep Think</button>
<button class="ai-btn">Create Image</button>
<button class="ai-btn">Write Article</button>
</div>

</div>

<div class="center">

<div class="flower">

<div class="petal"></div>
<div class="petal"></div>
<div class="petal"></div>
<div class="petal"></div>
<div class="petal"></div>
<div class="petal"></div>
<div class="petal"></div>
<div class="petal"></div>

<div class="flower-center">
SHADAB AI
</div>

</div>

<div class="response-box" id="response">
Hello Shadab 👋<br><br>
I am your advanced futuristic AI assistant.<br>
Ask anything...
</div>

</div>

<div class="input-area">

<input
type="text"
class="ai-input"
id="userInput"
placeholder="Ask SHADAB AI anything..."
>

<button class="send-btn" onclick="sendMessage()">
➤
</button>

</div>

</div>

<script>

function sendMessage(){

let input=document.getElementById("userInput").value;
let response=document.getElementById("response");

if(input.trim()===""){
return;
}

response.innerHTML=`
<b>You:</b> ${input}
<br><br>
<b>SHADAB AI:</b><br>
Processing with Deep Think Engine...
`;

setTimeout(()=>{

response.innerHTML=`
<b>You:</b> ${input}
<br><br>
<b>SHADAB AI:</b><br>
This is a futuristic AI response generated for:
"${input}"
`;

},2000);

document.getElementById("userInput").value="";

}

</script>

</body>
</html># ShadabAi
