<!DOCTYPE html>
<html lang="en">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Little Date Invitation 💜</title>

<style>

@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=DM+Sans:wght@400;500;600;700&family=Pacifico&display=swap');

*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

html,body{
    min-height:100%;
}

body{
    font-family:'DM Sans',sans-serif;
    overflow-x:hidden;
    transition:background 1s ease;
}

/* =====================================================
   BTS THEME - PAGE 1 ONLY
===================================================== */

body.theme-bts{
    background:
        radial-gradient(circle at 20% 20%,rgba(255,255,255,.12),transparent 25%),
        radial-gradient(circle at 80% 80%,rgba(180,100,255,.15),transparent 30%),
        linear-gradient(135deg,#12051f,#241044,#4b1975);
    color:white;
}

/* =====================================================
   ROMANTIC THEME - ALL OTHER PAGES
===================================================== */

body.theme-romantic{
    background:
        radial-gradient(circle at 10% 10%,rgba(255,182,193,.25),transparent 25%),
        radial-gradient(circle at 90% 90%,rgba(255,210,220,.3),transparent 25%),
        #fff7f8;
    color:#4d3440;
}

.page{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    padding:25px 15px;
    position:relative;
}

.card{
    width:min(700px,94vw);
    min-height:600px;
    border-radius:30px;
    padding:35px 30px;
    text-align:center;
    position:relative;
    overflow:hidden;
    transition:all .8s ease;
}

/* BTS CARD */

.theme-bts .card{
    background:rgba(30,10,48,.84);
    border:1px solid rgba(255,255,255,.15);
    box-shadow:
        0 0 40px rgba(170,90,255,.25),
        inset 0 0 50px rgba(255,255,255,.03);
}

/* ROMANTIC CARD */

.theme-romantic .card{
    background:rgba(255,255,255,.96);
    border:1px solid #f5d9df;
    box-shadow:
        0 20px 60px rgba(150,80,100,.12);
}

/* =====================================================
   PAGE TRANSITIONS
===================================================== */

.step{
    display:none;
    opacity:0;
    transform:translateX(70px) scale(.96);
}

.step.active{
    display:block;
    animation:pageEnter .8s cubic-bezier(.22,1,.36,1) forwards;
}

@keyframes pageEnter{

    0%{
        opacity:0;
        transform:translateX(70px) scale(.94);
    }

    60%{
        opacity:1;
        transform:translateX(-8px) scale(1.01);
    }

    100%{
        opacity:1;
        transform:translateX(0) scale(1);
    }
}

/* =====================================================
   GENERAL
===================================================== */

h1{
    font-family:'Cormorant Garamond',serif;
    font-size:clamp(35px,7vw,58px);
    line-height:1.05;
    margin:20px 0;
}

h2{
    font-family:'Cormorant Garamond',serif;
    font-size:clamp(32px,6vw,48px);
    margin-bottom:15px;
}

p{
    font-size:17px;
    line-height:1.7;
}

.script{
    font-family:'Pacifico',cursive;
}

.subtitle{
    margin:10px auto 25px;
    max-width:520px;
}

button{
    border:none;
    cursor:pointer;
    font-family:inherit;
    transition:.3s ease;
}

.primary-btn{
    padding:14px 28px;
    border-radius:50px;
    font-size:16px;
    font-weight:700;
    margin:8px;
}

.theme-bts .primary-btn{
    background:linear-gradient(135deg,#b65cff,#7b2cbf);
    color:white;
    box-shadow:0 8px 25px rgba(150,60,255,.3);
}

.theme-romantic .primary-btn{
    background:linear-gradient(135deg,#e889a5,#d9688b);
    color:white;
    box-shadow:0 8px 20px rgba(210,100,130,.22);
}

.primary-btn:hover{
    transform:translateY(-4px) scale(1.04);
}

.secondary-btn{
    padding:12px 23px;
    border-radius:50px;
    margin:8px;
    background:transparent;
}

.theme-bts .secondary-btn{
    color:white;
    border:1px solid rgba(255,255,255,.3);
}

.theme-romantic .secondary-btn{
    color:#a6536d;
    border:1px solid #e8bac7;
}

/* =====================================================
   FIRST PAGE
===================================================== */

.hero{
    width:190px;
    height:190px;
    border-radius:50%;
    margin:10px auto 25px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:85px;
    animation:float 3s ease-in-out infinite;
}

.theme-bts .hero{
    background:radial-gradient(circle,#c878ff,#5d238b);
    box-shadow:0 0 50px rgba(200,110,255,.4);
}

@keyframes float{

    0%,100%{
        transform:translateY(0)
    }

    50%{
        transform:translateY(-12px)
    }
}

.bts-label{
    display:inline-block;
    padding:7px 17px;
    border-radius:30px;
    background:rgba(255,255,255,.1);
    border:1px solid rgba(255,255,255,.15);
    letter-spacing:2px;
    font-size:12px;
    margin-bottom:5px;
}

.no-btn{
    position:relative;
}

.question-area{
    min-height:80px;
    position:relative;
}

/* =====================================================
   FORM
===================================================== */

.field{
    margin:20px 0;
    text-align:left;
}

.field label{
    display:block;
    margin-bottom:8px;
    font-weight:600;
}

input,select{
    width:100%;
    padding:14px 16px;
    border-radius:15px;
    outline:none;
    font-size:16px;
    font-family:inherit;
}

.theme-romantic input,
.theme-romantic select{
    border:1px solid #edcbd4;
    background:#fffafa;
    color:#51343f;
}

.theme-bts input,
.theme-bts select{
    border:1px solid #714493;
    background:#28143b;
    color:white;
}

/* =====================================================
   OPTIONS
===================================================== */

.options{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:14px;
    margin:25px 0;
}

.option{
    padding:20px 14px;
    border-radius:20px;
    cursor:pointer;
    transition:.3s ease;
}

.theme-romantic .option{
    background:#fff5f7;
    border:1px solid #f2d8df;
}

.theme-bts .option{
    background:rgba(255,255,255,.07);
    border:1px solid rgba(255,255,255,.13);
}

.option:hover{
    transform:translateY(-5px);
}

.option.selected{
    transform:scale(1.03);
}

.theme-romantic .option.selected{
    background:#fce4eb;
    border-color:#db7694;
}

.theme-bts .option.selected{
    background:rgba(173,91,255,.25);
    border-color:#c176ff;
    box-shadow:0 0 20px rgba(170,80,255,.2);
}

.option .emoji{
    display:block;
    font-size:35px;
    margin-bottom:7px;
}

/* =====================================================
   CAFE CARDS
===================================================== */

.cafes{
    display:grid;
    gap:14px;
    margin:25px 0;
}

.cafe{
    padding:18px;
    border-radius:20px;
    text-align:left;
    transition:.3s ease;
}

.theme-romantic .cafe{
    background:#fff8f9;
    border:1px solid #f0d7de;
}

.cafe:hover{
    transform:translateY(-3px);
}

.cafe h3{
    font-family:'Cormorant Garamond',serif;
    font-size:24px;
}

.cafe-actions{
    margin-top:12px;
}

.map-btn{
    display:inline-block;
    padding:8px 15px;
    border-radius:20px;
    text-decoration:none;
    font-size:13px;
    margin-right:5px;
    background:#f3e1e7;
    color:#9a4e68;
}

.choose-btn{
    padding:8px 15px;
    border-radius:20px;
    background:#d97794;
    color:white;
    font-size:13px;
}

/* =====================================================
   CONFIRM TEXT JUMP ANIMATION
===================================================== */

.confirm-text{
    opacity:0;
    transform:translateY(80px) scale(.7);
}

.confirm-text.animate{
    animation:jumpIn .75s cubic-bezier(.175,.885,.32,1.275) forwards;
}

.confirm-text:nth-child(1){
    animation-delay:.05s
}

.confirm-text:nth-child(2){
    animation-delay:.25s
}

.confirm-text:nth-child(3){
    animation-delay:.45s
}

.confirm-text:nth-child(4){
    animation-delay:.65s
}

.confirm-text:nth-child(5){
    animation-delay:.85s
}

@keyframes jumpIn{

    0%{
        opacity:0;
        transform:translateY(80px) scale(.65) rotate(-5deg);
    }

    55%{
        opacity:1;
        transform:translateY(-14px) scale(1.08) rotate(2deg);
    }

    75%{
        transform:translateY(5px) scale(.98);
    }

    100%{
        opacity:1;
        transform:translateY(0) scale(1) rotate(0);
    }
}

.confirm-title{
    font-family:'Cormorant Garamond',serif;
    font-size:48px;
    margin:10px 0;
}

/* =====================================================
   FINAL REVEAL
===================================================== */

.final-box{
    padding:30px 15px;
}

.final-emoji{
    font-size:75px;
    animation:finalBounce 1.2s infinite;
}

@keyframes finalBounce{

    0%,100%{
        transform:translateY(0)
    }

    50%{
        transform:translateY(-15px) rotate(5deg)
    }
}

.reveal-line{
    opacity:0;
    transform:translateY(40px);
}

.reveal-line.show{
    animation:revealLine .7s ease forwards;
}

@keyframes revealLine{

    to{
        opacity:1;
        transform:translateY(0);
    }
}

/* =====================================================
   FUTURE YES / NO BUTTONS
===================================================== */

.future-buttons{
    margin-top:25px;
    opacity:0;
    transform:translateY(35px);
}

.future-buttons.show{
    animation:futureButtonsIn .8s cubic-bezier(.175,.885,.32,1.275) forwards;
}

@keyframes futureButtonsIn{

    0%{
        opacity:0;
        transform:translateY(35px) scale(.8);
    }

    70%{
        opacity:1;
        transform:translateY(-6px) scale(1.04);
    }

    100%{
        opacity:1;
        transform:translateY(0) scale(1);
    }
}

.future-yes{
    background:linear-gradient(135deg,#e889a5,#d9688b) !important;
}

.future-no{
    background:#fff !important;
    color:#a6536d !important;
    border:2px solid #e3a0b3 !important;
}

.response-message{
    margin-top:20px;
    font-family:'Pacifico',cursive;
    font-size:20px;
    opacity:0;
}

.response-message.show{
    animation:responsePop .7s ease forwards;
}

@keyframes responsePop{

    0%{
        opacity:0;
        transform:scale(.5);
    }

    70%{
        opacity:1;
        transform:scale(1.1);
    }

    100%{
        opacity:1;
        transform:scale(1);
    }
}

/* =====================================================
   MUSIC BUTTON
===================================================== */

.music-control{
    position:fixed;
    top:18px;
    right:18px;
    z-index:100;
    width:45px;
    height:45px;
    border-radius:50%;
    background:rgba(255,255,255,.9);
    box-shadow:0 5px 20px rgba(0,0,0,.12);
    font-size:20px;
}

/* =====================================================
   FLOATING HEARTS
===================================================== */

.heart{
    position:fixed;
    pointer-events:none;
    animation:heartFloat linear forwards;
    z-index:1;
}

@keyframes heartFloat{

    from{
        transform:translateY(0) rotate(0);
        opacity:1;
    }

    to{
        transform:translateY(-110vh) rotate(360deg);
        opacity:0;
    }
}

/* =====================================================
   CONFETTI
===================================================== */

.confetti{
    position:fixed;
    width:9px;
    height:13px;
    pointer-events:none;
    z-index:999;
    animation:confettiFall 2.5s ease-out forwards;
}

@keyframes confettiFall{

    0%{
        transform:translate(0,0) rotate(0);
        opacity:1;
    }

    100%{
        transform:translate(var(--x),var(--y)) rotate(720deg);
        opacity:0;
    }
}

/* =====================================================
   SPARKLES
===================================================== */

.sparkle{
    position:fixed;
    pointer-events:none;
    z-index:999;
    font-size:20px;
    animation:sparkle .9s ease-out forwards;
}

@keyframes sparkle{

    from{
        opacity:1;
        transform:scale(.3);
    }

    to{
        opacity:0;
        transform:translate(var(--sx),var(--sy)) scale(1.5) rotate(180deg);
    }
}

/* =====================================================
   RESPONSIVE
===================================================== */

@media(max-width:600px){

    .card{
        min-height:0;
        padding:28px 18px;
        border-radius:25px;
    }

    .options{
        grid-template-columns:1fr 1fr;
        gap:10px;
    }

    .option{
        padding:15px 8px;
    }

    .hero{
        width:150px;
        height:150px;
        font-size:65px;
    }

    .confirm-title{
        font-size:38px;
    }

    p{
        font-size:15px;
    }

    .future-buttons{
        display:flex;
        flex-direction:column;
        align-items:center;
    }

}

</style>
</head>


<body class="theme-bts">

<!-- =====================================================
     MUSIC
===================================================== -->

<audio id="bgm1" loop preload="auto">
    <source src="bgm1.mp3" type="audio/mpeg">
</audio>

<audio id="bgm2" loop preload="auto">
    <source src="bgm2.mp3" type="audio/mpeg">
</audio>

<button class="music-control" onclick="toggleMusic()" id="musicBtn">
    🔊
</button>


<div class="page">
<div class="card">


<!-- =====================================================
     STEP 1
===================================================== -->

<section class="step active" id="step1">

    <div class="bts-label">
        A LITTLE BTS-INSPIRED QUESTION 💜
    </div>

    <div class="hero">
        💜
    </div>

    <h1>
        🌸 Will you go on a<br>
        BTS date with me? 🌸
    </h1>

    <p class="subtitle">
        Maybe a little food, a little music,<br>
        and a lot of good memories? 👀
    </p>

    <div class="question-area">

        <button
            class="primary-btn"
            onclick="acceptDate()">
            YES 💜
        </button>

        <button
            class="primary-btn no-btn"
            id="noBtn"
            onmouseover="dodgeNoButton()"
            onclick="dodgeNoButton()">
            NO 😭
        </button>

    </div>

</section>


<!-- =====================================================
     STEP 2
===================================================== -->

<section class="step" id="step2">

    <div class="hero">
        🥹
    </div>

    <h2>
        WAIT...
    </h2>

    <h1>
        YOU ACTUALLY SAID YES?! 😭
    </h1>

    <p class="subtitle">
        I was fully prepared for the NO button
        to destroy my confidence. 😂
    </p>

    <p class="script">
        Okay... let's plan this properly. 💕
    </p>

    <button
        class="primary-btn"
        onclick="nextStep()">
        Let's plan it ✨
    </button>

</section>


<!-- =====================================================
     STEP 3
===================================================== -->

<section class="step" id="step3">

    <h2>
        First things first 🌷
    </h2>

    <p class="subtitle">
        When should our little adventure happen?
    </p>

    <div class="field">

        <label>
            📅 Pick a date
        </label>

        <input
            type="date"
            id="dateInput">

    </div>

    <div class="field">

        <label>
            ⏰ Pick a time
        </label>

        <select id="timeInput">

            <option value="">
                Choose a time...
            </option>

            <option>11:00 AM</option>
            <option>12:00 PM</option>
            <option>1:00 PM</option>
            <option>2:00 PM</option>
            <option>3:00 PM</option>
            <option>4:00 PM</option>
            <option>5:00 PM</option>
            <option>6:00 PM</option>
            <option>7:00 PM</option>
            <option>8:00 PM</option>

        </select>

    </div>

    <button
        class="primary-btn"
        onclick="saveDateTime()">
        Continue 🌸
    </button>

</section>


<!-- =====================================================
     STEP 4
===================================================== -->

<section class="step" id="step4">

    <h2>
        What are we eating? 🍜
    </h2>

    <p class="subtitle">
        Important question. Very important.
    </p>

    <div class="options">

        <div
            class="option"
            onclick="selectFood(this,'Pizza 🍕')">

            <span class="emoji">
                🍕
            </span>

            Pizza

        </div>


        <div
            class="option"
            onclick="selectFood(this,'Pasta 🍝')">

            <span class="emoji">
                🍝
            </span>

            Pasta

        </div>


        <div
            class="option"
            onclick="selectFood(this,'Korean Food 🇰🇷')">

            <span class="emoji">
                🍜
            </span>

            Korean Food

        </div>


        <div
            class="option"
            onclick="selectFood(this,'Dessert & Coffee ☕')">

            <span class="emoji">
                🍰
            </span>

            Dessert & Coffee

        </div>


        <div
            class="option"
            onclick="selectFood(this,'Anything You Want 💕')">

            <span class="emoji">
                💗
            </span>

            Anything You Want

        </div>


        <div
            class="option"
            onclick="selectFood(this,'Surprise Me 👀')">

            <span class="emoji">
                🎁
            </span>

            Surprise Me

        </div>

    </div>

    <button
        class="primary-btn"
        onclick="goCafe()">

        Next ✨

    </button>

</section>


<!-- =====================================================
     STEP 5
===================================================== -->

<section class="step" id="step5">

    <h2>
        Where should we go? ☕
    </h2>

    <p class="subtitle">
        Pick a café for our little date.
    </p>

    <div class="cafes">


        <div class="cafe">

            <h3>
                🌹 La Vie En Rose Cafe & Bistro
            </h3>

            <p>
                Romantic café vibes ✨
            </p>

            <div class="cafe-actions">

                <a
                    class="map-btn"
                    target="_blank"
                    href="https://www.google.com/maps/search/?api=1&query=La+Vie+En+Rose+Cafe+and+Bistro+Kothapet+Hyderabad">

                    📍 Google Maps

                </a>

                <button
                    class="choose-btn"
                    onclick="selectCafe(this,'La Vie En Rose Cafe & Bistro')">

                    Choose

                </button>

            </div>

        </div>


        <div class="cafe">

            <h3>
                ☕ Cafe Maxibrew
            </h3>

            <p>
                Cozy & chill atmosphere
            </p>

            <div class="cafe-actions">

                <a
                    class="map-btn"
                    target="_blank"
                    href="https://www.google.com/maps/search/?api=1&query=Cafe+Maxibrew+Kothapet+Hyderabad">

                    📍 Google Maps

                </a>

                <button
                    class="choose-btn"
                    onclick="selectCafe(this,'Cafe Maxibrew')">

                    Choose

                </button>

            </div>

        </div>


        <div class="cafe">

            <h3>
                🌸 Siri Lit Café
            </h3>

            <p>
                Cute café date energy
            </p>

            <div class="cafe-actions">

                <a
                    class="map-btn"
                    target="_blank"
                    href="https://www.google.com/maps/search/?api=1&query=Siri+Lit+Cafe+Kothapet+Hyderabad">

                    📍 Google Maps

                </a>

                <button
                    class="choose-btn"
                    onclick="selectCafe(this,'Siri Lit Café')">

                    Choose

                </button>

            </div>

        </div>


        <div class="cafe">

            <h3>
                🌳 The Tree Stories
            </h3>

            <p>
                Relaxed café & restaurant
            </p>

            <div class="cafe-actions">

                <a
                    class="map-btn"
                    target="_blank"
                    href="https://www.google.com/maps/search/?api=1&query=The+Tree+Stories+LB+Nagar+Hyderabad">

                    📍 Google Maps

                </a>

                <button
                    class="choose-btn"
                    onclick="selectCafe(this,'The Tree Stories')">

                    Choose

                </button>

            </div>

        </div>


        <div class="cafe">

            <h3>
                🎮 Cosmos Cafe & Gaming
            </h3>

            <p>
                Café + games + fun
            </p>

            <div class="cafe-actions">

                <a
                    class="map-btn"
                    target="_blank"
                    href="https://www.google.com/maps/search/?api=1&query=Cosmos+Cafe+Gaming+Kothapet+Hyderabad">

                    📍 Google Maps

                </a>

                <button
                    class="choose-btn"
                    onclick="selectCafe(this,'Cosmos Cafe & Gaming')">

                    Choose

                </button>

            </div>

        </div>

    </div>


    <button
        class="primary-btn"
        onclick="goSongs()">

        Continue 💕

    </button>

</section>


<!-- =====================================================
     STEP 6
===================================================== -->

<section class="step" id="step6">

    <h2>
        And obviously... 🎧
    </h2>

    <p class="subtitle">
        We need a song for the date.
    </p>

    <div class="options">


        <div
            class="option"
            onclick="selectSong(this,'Spring Day 🌸')">

            <span class="emoji">
                🌸
            </span>

            Spring Day

        </div>


        <div
            class="option"
            onclick="selectSong(this,'Euphoria 💜')">

            <span class="emoji">
                💜
            </span>

            Euphoria

        </div>


        <div
            class="option"
            onclick="selectSong(this,'Dynamite ✨')">

            <span class="emoji">
                ✨
            </span>

            Dynamite

        </div>


        <div
            class="option"
            onclick="selectSong(this,'Boy With Luv 💕')">

            <span class="emoji">
                💕
            </span>

            Boy With Luv

        </div>


        <div
            class="option"
            onclick="selectSong(this,'Still With You 🌙')">

            <span class="emoji">
                🌙
            </span>

            Still With You

        </div>


        <div
            class="option"
            onclick="selectSong(this,'Your Choice 👀')">

            <span class="emoji">
                🎶
            </span>

            Your Choice

        </div>

    </div>


    <button
        class="primary-btn"
        onclick="showSummary()">

        Confirm Everything 💜

    </button>

</section>


<!-- =====================================================
     STEP 7 - CONFIRMATION
===================================================== -->

<section class="step" id="step7">

    <div id="confirmationContent">


        <div class="confirm-text">

            <div class="final-emoji">
                🥹
            </div>

        </div>


        <div class="confirm-text">

            <div class="confirm-title">
                WAIT...
            </div>

        </div>


        <div class="confirm-text">

            <h1>
                YOU ACTUALLY<br>
                DID ALL THAT?! 😭
            </h1>

        </div>


        <div class="confirm-text">

            <p>
                You chose the date.<br>
                You chose the food.<br>
                You chose the café.<br>
                You even chose the song. 😂
            </p>

        </div>


        <div class="confirm-text">

            <p class="script">
                Okay... I respect the commitment. 💕
            </p>

        </div>

    </div>


    <button
        class="primary-btn"
        id="revealButton"
        style="opacity:0;transform:translateY(30px)"
        onclick="finalReveal()">

        Continue 👀

    </button>

</section>


<!-- =====================================================
     STEP 8 - FINAL REVEAL
===================================================== -->

<section class="step" id="step8">

    <div class="final-box">

        <div class="final-emoji">
            😂💜
        </div>


        <h1 class="reveal-line">
            JUST KIDDING 😂
        </h1>


        <p class="reveal-line">
            There is no date agreement.
        </p>


        <p class="reveal-line">
            No payment.
        </p>


        <p class="reveal-line">
            No pressure.
        </p>


        <br>


        <p class="reveal-line">
            But hey...
        </p>


        <h2 class="reveal-line">
            Be ready for the future 👀💕
        </h2>


        <!-- NEW YES / NO SECTION -->

        <div
            class="future-buttons"
            id="futureButtons">

            <button
                class="primary-btn future-yes"
                onclick="futureResponse('YES')">

                YES 💜

            </button>


            <button
                class="primary-btn future-no"
                onclick="futureResponse('NO')">

                NO 😭

            </button>

        </div>


        <div
            class="response-message"
            id="responseMessage">

        </div>

    </div>

</section>


</div>
</div>


<script>

/* =====================================================
   GOOGLE APPS SCRIPT URL
===================================================== */

const GOOGLE_SCRIPT_URL =
    "https://script.google.com/macros/s/AKfycbzfS_tJN5Fn_yZfewa31H8S-vaWEWDmJiIBapJB-oKUtkIsUM64OS-NX4ve9H4dOcI1vA/exec";


/* =====================================================
   VARIABLES
===================================================== */

let currentStep = 1;

let selectedDate = "";
let selectedTime = "";
let selectedFoodValue = "";
let selectedCafeValue = "";
let selectedSongValue = "";

let finalResponse = "";

const bgm1 =
    document.getElementById("bgm1");

const bgm2 =
    document.getElementById("bgm2");

const musicBtn =
    document.getElementById("musicBtn");

let musicPlaying = false;


/* =====================================================
   SET MIN DATE
===================================================== */

const dateInput =
    document.getElementById("dateInput");

const today =
    new Date();

const yyyy =
    today.getFullYear();

const mm =
    String(today.getMonth()+1)
    .padStart(2,"0");

const dd =
    String(today.getDate())
    .padStart(2,"0");

dateInput.min =
    `${yyyy}-${mm}-${dd}`;


/* =====================================================
   PAGE THEME
===================================================== */

function updateTheme(){

    if(currentStep === 1){

        document.body.classList.remove(
            "theme-romantic"
        );

        document.body.classList.add(
            "theme-bts"
        );

    }else{

        document.body.classList.remove(
            "theme-bts"
        );

        document.body.classList.add(
            "theme-romantic"
        );

    }
}


/* =====================================================
   CHANGE PAGE
===================================================== */

function changeStep(number){

    const oldStep =
        document.getElementById(
            `step${currentStep}`
        );

    oldStep.classList.remove("active");

    currentStep = number;

    updateTheme();

    const newStep =
        document.getElementById(
            `step${currentStep}`
        );

    setTimeout(()=>{

        newStep.classList.add("active");

        sparkleBurst();

    },100);
}


/* =====================================================
   NEXT
===================================================== */

function nextStep(){

    if(currentStep < 8){

        changeStep(
            currentStep + 1
        );

    }
}


/* =====================================================
   YES BUTTON - PAGE 1
===================================================== */

function acceptDate(){

    playBGM1();

    massiveConfetti();

    createHearts();

    changeStep(2);
}


/* =====================================================
   BGM 1
===================================================== */

function playBGM1(){

    bgm2.pause();

    bgm2.currentTime = 0;

    bgm1.volume = 0.75;

    bgm1.play()
        .then(()=>{

            musicPlaying = true;

            musicBtn.textContent = "🔊";

        })
        .catch(()=>{

            console.log(
                "Browser blocked autoplay."
            );

        });
}


/* =====================================================
   BGM 2
===================================================== */

function playBGM2(){

    bgm1.pause();

    bgm1.currentTime = 0;

    bgm2.volume = 0.75;

    bgm2.play()
        .then(()=>{

            musicPlaying = true;

            musicBtn.textContent = "🔊";

        })
        .catch(()=>{

            console.log(
                "BGM 2 could not autoplay."
            );

        });
}


/* =====================================================
   MUSIC TOGGLE
===================================================== */

function toggleMusic(){

    if(currentStep >= 7){

        if(bgm2.paused){

            bgm2.play();

            musicBtn.textContent = "🔊";

            musicPlaying = true;

        }else{

            bgm2.pause();

            musicBtn.textContent = "🔇";

            musicPlaying = false;

        }

    }else{

        if(bgm1.paused){

            bgm1.play();

            musicBtn.textContent = "🔊";

            musicPlaying = true;

        }else{

            bgm1.pause();

            musicBtn.textContent = "🔇";

            musicPlaying = false;

        }

    }
}


/* =====================================================
   DODGE NO BUTTON
===================================================== */

function dodgeNoButton(){

    const btn =
        document.getElementById("noBtn");

    const maxX =
        Math.min(
            180,
            window.innerWidth / 2
        );

    const maxY = 100;

    const x =
        (Math.random()*2-1) * maxX;

    const y =
        (Math.random()*2-1) * maxY;

    btn.style.transform =
        `translate(${x}px,${y}px)
         rotate(${Math.random()*20-10}deg)`;
}


/* =====================================================
   SAVE DATE/TIME
===================================================== */

function saveDateTime(){

    selectedDate =
        dateInput.value;

    selectedTime =
        document.getElementById(
            "timeInput"
        ).value;

    if(!selectedDate || !selectedTime){

        alert(
            "Choose a date and time first 💕"
        );

        return;
    }

    sparkleBurst();

    changeStep(4);
}


/* =====================================================
   FOOD
===================================================== */

function selectFood(
    element,
    value
){

    document
        .querySelectorAll(
            "#step4 .option"
        )
        .forEach(el =>
            el.classList.remove(
                "selected"
            )
        );

    element.classList.add(
        "selected"
    );

    selectedFoodValue =
        value;

    sparkleBurst();
}


/* =====================================================
   GO CAFE
===================================================== */

function goCafe(){

    if(!selectedFoodValue){

        alert(
            "You have to choose food first 😭🍜"
        );

        return;
    }

    changeStep(5);
}


/* =====================================================
   SELECT CAFE
===================================================== */

function selectCafe(
    button,
    value
){

    selectedCafeValue =
        value;

    document
        .querySelectorAll(".cafe")
        .forEach(cafe => {

            cafe.style.outline =
                "none";

        });

    const selectedCafe =
        button.closest(".cafe");

    if(selectedCafe){

        selectedCafe.style.outline =
            "3px solid #e39ab0";

    }

    sparkleBurst();
}


/* =====================================================
   GO SONGS
===================================================== */

function goSongs(){

    if(!selectedCafeValue){

        alert(
            "Pick a café first ☕💕"
        );

        return;
    }

    changeStep(6);
}


/* =====================================================
   SONG
===================================================== */

function selectSong(
    element,
    value
){

    document
        .querySelectorAll(
            "#step6 .option"
        )
        .forEach(el =>
            el.classList.remove(
                "selected"
            )
        );

    element.classList.add(
        "selected"
    );

    selectedSongValue =
        value;

    sparkleBurst();
}


/* =====================================================
   SEND RESPONSE TO GOOGLE SHEETS
===================================================== */

async function sendResponseToGoogleSheets(){

    if(
        !GOOGLE_SCRIPT_URL ||
        GOOGLE_SCRIPT_URL.includes(
            "PASTE_YOUR_GOOGLE_SCRIPT"
        )
    ){

        console.warn(
            "Google Apps Script URL has not been added."
        );

        return;
    }


    const responseData = {

        date:
            selectedDate,

        time:
            selectedTime,

        food:
            selectedFoodValue,

        cafe:
            selectedCafeValue,

        song:
            selectedSongValue,

        response:
            finalResponse

    };


    try{

        await fetch(

            GOOGLE_SCRIPT_URL,

            {

                method:"POST",

                mode:"no-cors",

                headers:{

                    "Content-Type":
                        "text/plain;charset=utf-8"

                },

                body:
                    JSON.stringify(
                        responseData
                    )

            }

        );

        console.log(
            "Response sent to Google Sheets."
        );

    }

    catch(error){

        console.error(
            "Could not send response:",
            error
        );

    }

}


/* =====================================================
   CONFIRM EVERYTHING
===================================================== */

async function showSummary(){

    if(!selectedSongValue){

        alert(
            "Pick a song first 🎧💜"
        );

        return;
    }


    /* BGM 2 */

    playBGM2();

    massiveConfetti();

    createHearts();


    /* Move to confirmation page first */

    changeStep(7);


    /* Animate confirmation text */

    setTimeout(()=>{

        const items =
            document.querySelectorAll(
                ".confirm-text"
            );

        items.forEach(item=>{

            item.classList.remove(
                "animate"
            );

        });


        setTimeout(()=>{

            items.forEach(item=>{

                item.classList.add(
                    "animate"
                );

            });

        },100);


        const revealButton =
            document.getElementById(
                "revealButton"
            );


        revealButton.style.opacity =
            "1";

        revealButton.style.transform =
            "translateY(0)";

        revealButton.style.transition =
            "all .8s cubic-bezier(.175,.885,.32,1.275)";

    },700);

}


/* =====================================================
   FINAL REVEAL
===================================================== */

function finalReveal(){

    massiveConfetti();

    createHearts();

    sparkleBurst();

    changeStep(8);


    setTimeout(()=>{

        const lines =
            document.querySelectorAll(
                "#step8 .reveal-line"
            );


        lines.forEach(
            (line,index)=>{

                setTimeout(()=>{

                    line.classList.add(
                        "show"
                    );

                },index*350);

            }
        );


        /* Show YES / NO after text */

        setTimeout(()=>{

            const buttons =
                document.getElementById(
                    "futureButtons"
                );

            buttons.classList.add(
                "show"
            );

        },2800);

    },700);

}


/* =====================================================
   FINAL YES / NO RESPONSE
===================================================== */

async function futureResponse(answer){

    finalResponse =
        answer;


    /* Save YES or NO to Google Sheets */

    await sendResponseToGoogleSheets();


    /* Hide buttons */

    const buttons =
        document.getElementById(
            "futureButtons"
        );

    buttons.style.display =
        "none";


    /* Show response message */

    const message =
        document.getElementById(
            "responseMessage"
        );


    if(answer === "YES"){

        message.innerHTML =
            "I knew it 😌💜✨";

    }else{

        message.innerHTML =
            "Okay... I'll pretend I didn't see that 😭😂";

    }


    message.classList.add(
        "show"
    );


    massiveConfetti();

    sparkleBurst();

    createHearts();

}


/* =====================================================
   FLOATING HEARTS
===================================================== */

function createHearts(){

    const hearts = [

        "💜",
        "💕",
        "💗",
        "💖",
        "🌸",
        "✨"

    ];


    for(let i=0;i<18;i++){

        const heart =
            document.createElement(
                "div"
            );

        heart.className =
            "heart";

        heart.textContent =
            hearts[
                Math.floor(
                    Math.random() *
                    hearts.length
                )
            ];

        heart.style.left =
            Math.random()*100 +
            "vw";

        heart.style.bottom =
            "-30px";

        heart.style.fontSize =
            (14 + Math.random()*22) +
            "px";

        heart.style.animationDuration =
            (4 + Math.random()*4) +
            "s";

        document.body.appendChild(
            heart
        );


        setTimeout(()=>{

            heart.remove();

        },8000);

    }

}


/* =====================================================
   CONFETTI
===================================================== */

function massiveConfetti(){

    const symbols = [

        "💜",
        "💕",
        "✨",
        "🌸",
        "💗",
        "⭐"

    ];


    for(let i=0;i<70;i++){

        const piece =
            document.createElement(
                "div"
            );

        piece.className =
            "confetti";

        piece.textContent =
            symbols[
                Math.floor(
                    Math.random() *
                    symbols.length
                )
            ];

        piece.style.left =
            "50vw";

        piece.style.top =
            "45vh";


        piece.style.setProperty(

            "--x",

            (
                (Math.random()*2-1) *
                window.innerWidth

            ) + "px"

        );


        piece.style.setProperty(

            "--y",

            (
                (Math.random()*2-1) *
                window.innerHeight

            ) + "px"

        );


        piece.style.fontSize =
            (10 + Math.random()*15) +
            "px";


        document.body.appendChild(
            piece
        );


        setTimeout(()=>{

            piece.remove();

        },3000);

    }

}


/* =====================================================
   SPARKLE BURST
===================================================== */

function sparkleBurst(){

    const symbols = [

        "✦",
        "✧",
        "✨",
        "💫"

    ];


    for(let i=0;i<15;i++){

        const sparkle =
            document.createElement(
                "div"
            );

        sparkle.className =
            "sparkle";

        sparkle.textContent =
            symbols[
                Math.floor(
                    Math.random() *
                    symbols.length
                )
            ];


        sparkle.style.left =
            (35 + Math.random()*30) +
            "vw";


        sparkle.style.top =
            (35 + Math.random()*30) +
            "vh";


        sparkle.style.setProperty(

            "--sx",

            (
                (Math.random()*2-1) *
                180

            ) + "px"

        );


        sparkle.style.setProperty(

            "--sy",

            (
                (Math.random()*2-1) *
                180

            ) + "px"

        );


        document.body.appendChild(
            sparkle
        );


        setTimeout(()=>{

            sparkle.remove();

        },1000);

    }

}


/* =====================================================
   START HEARTS PERIODICALLY
===================================================== */

setInterval(()=>{

    if(
        document.visibilityState ===
        "visible"
    ){

        const heart =
            document.createElement(
                "div"
            );

        heart.className =
            "heart";

        heart.textContent =
            Math.random() > .5
            ? "♡"
            : "✦";


        heart.style.left =
            Math.random()*100 +
            "vw";


        heart.style.bottom =
            "-20px";


        heart.style.fontSize =
            (12 + Math.random()*15) +
            "px";


        heart.style.animationDuration =
            (7 + Math.random()*4) +
            "s";


        document.body.appendChild(
            heart
        );


        setTimeout(()=>{

            heart.remove();

        },11000);

    }

},1800);


/* =====================================================
   INITIAL THEME
===================================================== */

updateTheme();

</script>

</body>
</html>
