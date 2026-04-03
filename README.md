<!DOCTYPE html>
<html lang="my">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WiFi Promo</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Pyidaungsu:wght@400;700&display=swap');

        body {
            font-family: 'Pyidaungsu', sans-serif;
            background-color: #0d0d1a;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        #star-canvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
        }

        .promo-card {
            position: relative;
            z-index: 2;
            width: 90%;
            max-width: 450px;
            background: rgba(0, 0, 0, 0.7);
            border: 2px solid rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 25px;
            text-align: center;
            box-sizing: border-box; /* padding ကြောင့် အပြင်မထွက်အောင် */
        }

        /* ရောင်စုံလင်းတဲ့ Animation */
        @keyframes rainbowGlow {
            0% { color: #ff0000; text-shadow: 0 0 10px #ff0000; }
            25% { color: #00ff00; text-shadow: 0 0 10px #00ff00; }
            50% { color: #00ffff; text-shadow: 0 0 10px #00ffff; }
            75% { color: #ffff00; text-shadow: 0 0 10px #ffff00; }
            100% { color: #ff00ff; text-shadow: 0 0 10px #ff00ff; }
        }

        .rainbow-text {
            animation: rainbowGlow 5s infinite linear;
            font-weight: bold;
            font-size: 1.6rem;
            line-height: 1.6;
            margin: 10px 0;
        }

        .plain-text {
            color: #ffffff;
            font-size: 1.1rem;
            margin: 10px 0;
            line-height: 1.5;
        }

        .price {
            font-size: 2.2rem;
            color: #ffeb3b;
            font-weight: bold;
            text-shadow: 0 0 15px #ffeb3b;
            margin: 15px 0;
            display: block;
        }

        .footer {
            color: #ff4757;
            font-size: 1rem;
            margin-top: 15px;
            font-weight: bold;
        }

        /* စာသားတွေအကုန်လုံး Card ထဲမှာပဲ ရှိနေစေဖို့ */
        p, div {
            word-wrap: break-word;
            overflow-wrap: break-word;
        }
    </style>
</head>
<body>

    <canvas id="star-canvas"></canvas>

    <div class="promo-card">
        <div class="rainbow-text">
            တစ်သက်မှာ တခါပဲဆုံတဲ့ <br>
            မျိုးထက် ဝိုင်ဖိုင်လေးအဝသုံးသွားကြနော်
        </div>

        <div class="plain-text">
            အရင်လို Ooredoo. MPT တို့လို ဈေးမကြီးပါဘူး
        </div>

        <div class="plain-text">
            မင်းကြိုက်တဲ့ချိန်လာသုံး
        </div>

        <div class="price">
            ငွေ ၁၀၀၀ သာယူခဲ့
        </div>

        <div class="rainbow-text">
            တနေ့တာပင်ပန်မှူတွေ <br>
            ပြေပျောက်စေရမယ်
        </div>

        <div class="footer">
            ဟာသမဟုတ်ဘူးနော် တကယ်ပြောတာ 😊
        </div>
    </div>

    <script>
        const canvas = document.getElementById('star-canvas');
        const ctx = canvas.getContext('2d');
        let stars = [];

        function init() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
            stars = [];
            for (let i = 0; i < 80; i++) {
                stars.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    size: Math.random() * 2,
                    speed: Math.random() * 1 + 0.2
                });
            }
        }

        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = "white";
            stars.forEach(s => {
                ctx.beginPath();
                ctx.arc(s.x, s.y, s.size, 0, Math.PI * 2);
                ctx.fill();
                s.y += s.speed;
                if (s.y > canvas.height) s.y = -5;
            });
            requestAnimationFrame(draw);
        }

        window.addEventListener('resize', init);
        init();
        draw();
    </script>
</body>
</html>
