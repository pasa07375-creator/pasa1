<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

body{
    overflow:hidden;
    background:linear-gradient(135deg,#ff7eb3,#c084fc);
    height:100vh;
}

.slide{
    width:100%;
    height:100vh;
    display:none;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    color:white;
    padding:20px;
}

.active{
    display:flex;
}

h1{
    font-size:3rem;
    margin-bottom:20px;
    text-shadow:0 0 15px rgba(255,255,255,.6);
}

p{
    max-width:700px;
    line-height:1.8;
}

.buttons{
    display:flex;
    gap:20px;
    margin-top:25px;
}

button{
    border:none;
    padding:15px 35px;
    border-radius:50px;
    font-size:1.1rem;
    cursor:pointer;
    transition:.3s;
    font-weight:bold;
}

.yes{
    background:#ff4fa3;
    color:white;
}

.no{
    background:white;
    color:#ff4fa3;
}

.gifts{
    display:flex;
    gap:20px;
    flex-wrap:wrap;
    justify-content:center;
    margin-top:30px;
}

.gift{
    width:180px;
    height:180px;
    background:rgba(255,255,255,.2);
    border:2px solid rgba(255,255,255,.5);
    border-radius:25px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:1.5rem;
    cursor:pointer;
    transition:.3s;
    backdrop-filter:blur(8px);
}

.gift:hover{
    transform:translateY(-10px) scale(1.05);
}

.letter{
    background:rgba(255,255,255,.18);
    backdrop-filter:blur(10px);
    padding:30px;
    border-radius:25px;
    max-width:800px;
    border:1px solid rgba(255,255,255,.3);
}

.balloon{
    position:absolute;
    font-size:40px;
    animation:float 6s infinite ease-in-out;
}

@keyframes float{
    0%,100%{transform:translateY(0);}
    50%{transform:translateY(-25px);}
}

.b1{top:10%;left:10%;}
.b2{top:20%;right:15%;}
.b3{bottom:15%;left:20%;}
.b4{bottom:20%;right:10%;}

.confetti{
    font-size:35px;
    position:absolute;
}

.c1{top:8%;left:45%;}
.c2{top:80%;left:50%;}
.c3{top:35%;left:80%;}
.c4{top:60%;left:8%;}
</style>
</head>

<body>

<div class="balloon b1">🎈</div>
<div class="balloon b2">🎂</div>
<div class="balloon b3">🎁</div>
<div class="balloon b4">🎉</div>

<div class="confetti c1">✨</div>
<div class="confetti c2">💜</div>
<div class="confetti c3">🌸</div>
<div class="confetti c4">💖</div>

<!-- SLIDE 1 -->
<section class="slide active" id="slide1">
    <h1>Will You Be My Ulang Tahun? 💖</h1>
    <p>
        Hari ini spesial banget, jadi aku punya pertanyaan penting untukmu...
    </p>

    <div class="buttons">
        <button class="yes" id="yesBtn">YES 💕</button>
        <button class="no" id="noBtn">NO 🙈</button>
    </div>
</section>

<!-- SLIDE 2 -->
<section class="slide" id="slide2">
    <h1>Pilih Hadiah Ulang Tahun 🎁</h1>
    <p>Pilih salah satu gift di bawah ini</p>

    <div class="gifts">
        <div class="gift" onclick="openLetter()">🎁 Gift 1</div>
        <div class="gift" onclick="openLetter()">🎀 Gift 2</div>
        <div class="gift" onclick="openLetter()">💝 Gift 3</div>
    </div>
</section>

<!-- SLIDE 3 -->
<section class="slide" id="slide3">
    <div class="letter">
        <h1>🎂 Happy Birthday 🎂</h1>

        <p style="margin-top:20px;">
            Selamat ulang tahun untuk sayanggggg🤍🤍
            Semoga di usia yang baru ini semua impianmu semakin dekat,
            kesehatan selalu menyertai, kebahagiaan tidak pernah habis,
            dan setiap harimu dipenuhi tawa serta cinta.
            <br><br>
            Terima kasih sudah menjadi pribadi yang luar biasa.
            Tetaplah bersinar, tetaplah menjadi dirimu sendiri,
            dan semoga semua hal baik datang menghampirimu.
            <br><br>
            🎉 Selamat Ulang Tahun 🎉
            <br>
            💖 With Love 💖
        </p>
    </div>
</section>

<script>
let scale = 1;

const noBtn = document.getElementById("noBtn");
const yesBtn = document.getElementById("yesBtn");

noBtn.addEventListener("click", () => {
    scale += 0.3;
    yesBtn.style.transform = `scale(${scale})`;
});

yesBtn.addEventListener("click", () => {
    document.getElementById("slide1").classList.remove("active");
    document.getElementById("slide2").classList.add("active");
});

function openLetter(){
    document.getElementById("slide2").classList.remove("active");
    document.getElementById("slide3").classList.add("active");
}
</script>

</body>
</html>
