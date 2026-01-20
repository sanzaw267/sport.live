# sport.live
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Live Website</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body{
      margin:0;
      font-family: Arial, Helvetica, sans-serif;
      background:#0f172a;
      color:#fff;
      text-align:center;
    }
    header{
      background:#020617;
      padding:16px;
      font-size:22px;
      font-weight:bold;
    }
    .container{
      max-width:900px;
      margin:20px auto;
      padding:10px;
    }
    .live{
      display:inline-block;
      background:red;
      padding:4px 12px;
      border-radius:20px;
      margin-bottom:10px;
      font-size:14px;
    }
    iframe{
      width:100%;
      height:480px;
      border-radius:12px;
      border:none;
    }
    footer{
      margin-top:20px;
      font-size:13px;
      color:#94a3b8;
    }
  </style>
</head>
<body><header>🔴 My Live Streaming Website</header><div class="container">
  <div class="live">LIVE</div>  <!-- YouTube Live Embed -->  <iframe 
    src="https://www.youtube.com/embed/YOUR_VIDEO_ID?autoplay=1&mute=1"
    allow="autoplay; encrypted-media"
    allowfullscreen>
  </iframe>  <!-- YouTube Live Chat -->  <iframe
    src="https://www.youtube.com/live_chat?v=YOUR_VIDEO_ID&embed_domain=YOUR_DOMAIN"
    style="width:100%; height:350px; margin-top:15px; border:none; border-radius:12px;"
    allowfullscreen>
  </iframe>  <h3>Live Description</h3>
  <p>
    ဒီ Website က Server မလိုဘဲ YouTube Live ကို
    ကိုယ်ပိုင် Website မှာ တိုက်ရိုက်ပြနိုင်ဖို့ရေးထားတာပါ။
  </p>
</div><footer>
  © 2026 My Live Website
</footer></body>
</html>
