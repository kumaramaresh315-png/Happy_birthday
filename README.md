<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday Navya ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}
body{
    background:linear-gradient(120deg,#0f0c29,#302b63,#24243e);
    color:white;
    overflow:hidden;
}
.slide{
    display:none;
    height:100vh;
    width:100%;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    text-align:center;
    padding:20px;
    animation:fade 1s ease;
}
.slide.active{display:flex;}
@keyframes fade{
    from{opacity:0;transform:scale(0.9);}
    to{opacity:1;transform:scale(1);}
}
h1{font-size:3rem;text-shadow:0 0 20px pink;}
p{font-size:1.3rem;margin-top:15px;max-width:720px;}
button{
    margin-top:30px;
    padding:12px 35px;
    border:none;
    border-radius:30px;
    background:#ff4d6d;
    color:white;
    font-size:1.1rem;
    cursor:pointer;
}
button:hover{background:#ff1c4b;}

/* Cake */
.cake{
    width:240px;height:160px;
    background:#ffb703;
    border-radius:15px;
    position:relative;
    margin-top:25px;
}
.layer{position:absolute;width:100%;height:45px;background:#fb8500;top:55px;}
.candle{width:12px;height:45px;background:white;position:absolute;top:-45px;left:50%;transform:translateX(-50%);}
.flame{width:18px;height:18px;background:orange;border-radius:50%;position:absolute;top:-18px;left:-3px;animation:flicker .3s infinite alternate;}
@keyframes flicker{from{transform:scale(1);}to{transform:scale(1.2);}}

/* Knife */
.knife{
    width:140px;height:8px;background:silver;
    position:absolute;top:60%;left:-150px;border-radius:5px;
    animation:cut 3s forwards;
}
@keyframes cut{to{left:50%;transform:translateX(-50%);}}

/* Anime avatar */
.avatar{
    width:140px;height:140px;border-radius:50%;
    background:#ffd6e0;font-size:3rem;
    display:flex;align-items:center;justify-content:center;
}

/* Message box */
.msg-box{
    background:white;color:black;
    padding:18px 28px;border-radius:22px;
    margin-top:20px;animation:pop 1s ease;
}
@keyframes pop{from{transform:scale(0);}to{transform:scale(1);}}

/* Hearts */
.heart{
    position:absolute;color:red;font-size:20px;
    animation:float 2s infinite;
}
@keyframes float{
    from{transform:translateY(0);opacity:1;}
    to{transform:translateY(-120px);opacity:0;}
}

/* Confetti */
.confetti{
    position:absolute;width:6px;height:6px;
    animation:fall 3s infinite;
}
@keyframes fall{
    from{transform:translateY(-100px);}
    to{transform:translateY(110vh);}
}

/* Popup */
.popup{
    position:fixed;top:0;left:0;
    width:100%;height:100%;
    background:rgba(0,0,0,.7);
    display:none;justify-content:center;align-items:center;
}
.popup-content{
    background:white;color:black;
    padding:30px;border-radius:20px;
    text-align:center;max-width:300px;
}
</style>
</head>

<body>

<!-- Music -->
<audio autoplay loop>
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
</audio>

<!-- Slide 1 -->
<div class="slide active">
    <h1>🎉 Happy Birthday Navya 🎉</h1>
    <p>You are the most precious gift of my life 💖</p>
    <button onclick="nextSlide()">Next ➜</button>
</div>

<!-- Slide 2 -->
<div class="slide">
    <h1>🎂 Cake Cutting Time 🎂</h1>
    <div class="cake">
        <div class="layer"></div>
        <div class="candle"><div class="flame"></div></div>
        <div class="knife"></div>
    </div>
    <p>Let’s celebrate your beautiful smile 🥰</p>
    <button onclick="nextSlide()">Next ➜</button>
</div>

<!-- Slide 3 -->
<div class="slide">
    <h1>💌 From My Heart 💌</h1>
    <p id="typewriter"></p>
    <button onclick="nextSlide()">Next ➜</button>
</div>

<!-- Slide 4 -->
<div class="slide">
    <div class="avatar">😊</div>
    <div class="msg-box">
        I love you Navya ❤️<br>Forever & Always 💞
        <div class="heart">❤️</div>
        <div class="heart" style="left:40px;">❤️</div>
        <div class="heart" style="left:80px;">❤️</div>
    </div>
    <p>You are my sweetest emotion 💕</p>
    <button onclick="showPopup()">Final Surprise 🎁</button>
</div>

<!-- Popup -->
<div class="popup" id="popup">
    <div class="popup-content">
        <h2>💖 Navya 💖</h2>
        <p>Will you always stay with me and share every smile together? 🥺❤️</p>
        <button onclick="closePopup()">Yes ❤️</button>
    </div>
</div>

<script>
let slides=document.querySelectorAll(".slide");
let index=0;
function nextSlide(){
    slides[index].classList.remove("active");
    index++;
    if(index>=slides.length) index=slides.length-1;
    slides[index].classList.add("active");
}

/* Typewriter */
let text="Every heartbeat of mine whispers your name. You are my today, my tomorrow, and my forever ❤️";
let i=0;
function type(){
    if(i<text.length){
        document.getElementById("typewriter").innerHTML+=text.charAt(i);
        i++;setTimeout(type,60);
    }
}
type();

/* Popup */
function showPopup(){document.getElementById("popup").style.display="flex";}
function closePopup(){document.getElementById("popup").style.display="none";}

/* Confetti */
for(let i=0;i<120;i++){
    let c=document.createElement("div");
    c.className="confetti";
    c.style.left=Math.random()*100+"%";
    c.style.background=`hsl(${Math.random()*360},100%,50%)`;
    c.style.animationDelay=Math.random()*3+"s";
    document.body.appendChild(c);
}
</script>

</body>
</html>
# ❤️ Proposal Website

Make your proposal unforgettable with this beautifully designed Proposal Website.
With soft animations, heartfelt messages, and an elegant UI, this site turns a simple “I love you” into a magical and memorable experience. ✨

> ⚠️ This is a **free version**, so some features like background music, some animations are not included. Premium version includes all features.
> You can **buy the premium code** from my store [here](https://www.anujbuilds.in/products/proposal-site).

---

## 🛠 Tech Stack

- ⚛️ **Next.js** – React Framework for building fast UI
- 🎨 **Tailwind CSS** – For modern and responsive styling
- 🎞️ **Motion** – Smooth entrance and fade animations
- 🖼️ **Swiper.js** – For smooth image/cards slideshow

---

## 🖥 Local Setup

To run this project locally, follow these steps:

```bash
# Clone the repository
git clone https://github.com/Anuj579/proposal-site.git

# Navigate into the folder
cd proposal-site

# Install dependencies
npm install

# Start the development server
npm run dev
```

