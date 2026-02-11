<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>To My Baby 💖</title>
<style>
body {
    margin: 0;
    padding: 0;
    text-align: center;
    font-family: 'Georgia', serif;
    background: linear-gradient(to right, #ffdde1, #ee9ca7);
    color: #d6336c;
    overflow: hidden;
}

h1 {
    font-size: 2.8em;
    margin-top: 80px;
}

h2 {
    font-size: 1.8em;
    font-weight: normal;
    margin: 30px 20px;
}

button {
    padding: 15px 40px;
    font-size: 20px;
    border-radius: 50px;
    border: none;
    cursor: pointer;
    margin: 20px;
    background-color: #ff4d6d;
    color: white;
    transition: 0.3s;
}

button:hover {
    transform: scale(1.1);
}

#message {
    margin-top: 40px;
    font-size: 22px;
    color: #c9184a;
    display: none;
}

.heart {
    position: fixed;
    color: red;
    animation: float 5s linear infinite;
}

@keyframes float {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-700px); opacity: 0; }
}

.music-player {
    margin-top: 20px;
}
</style>
</head>
<body>

<h1>To the Best Girl I Know 💖</h1>
<h2>
Thank you for your love and patience bby, might not be physically present or send the best gifts,  
but I promise to come see you soon. I promise and I mean it. <br><br>
Could you be my Valentine, ujubby? 🥰
</h2>

<!-- Embedded YouTube Music Player -->
<div class="music-player">
  <iframe
    width="300"
    height="170"
    src="https://www.youtube.com/embed/4IuUYpS9RjE?autoplay=1&loop=1&playlist=4IuUYpS9RjE"
    title="Asake ft Wizkid – Jogodo"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen>
  </iframe>
</div>

<!-- ONLY YES BUTTON, NO 'NO' BUTTON -->
<button id="yesBtn" onclick="acceptLove()">Yes 💖</button>

<div id="message"></div>
<div style="margin-top:30px; font-size:18px; color:#c9184a;">Forever Yours, Akin 💌</div>

<script>
function acceptLove() {
    document.getElementById("message").style.display = "block";
    document.getElementById("message").innerHTML = 
        "Yayyyy my love! 💖🥰<br><br>Thank you for saying YES! You mean the world to me 💘";

    createHearts();

    // WhatsApp auto-message (optional, replace with your number)
    let phoneNumber = "234XXXXXXXXXX"; 
    let message = "Bby 💖 I said YES! Can't wait to see you ❤️🥰";
    let url = "https://wa.me/" + phoneNumber + "?text=" + encodeURIComponent(message);

    setTimeout(function() {
        window.open(url, "_blank");
    }, 2000);
}

function createHearts() {
    setInterval(function() {
        let heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * window.innerWidth + "px";
        heart.style.bottom = "0px";
        heart.style.fontSize = (Math.random() * 30 + 20) + "px";
        document.body.appendChild(heart);

        setTimeout(function() {
            heart.remove();
        }, 5000);
    }, 200);
}
</script>

</body>
</html>
