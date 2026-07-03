index.html
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>陳若濋 Rosy | AI 產業鏈顧問</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@500;600&family=Noto+Serif+TC:wght@400;500;600&display=swap');
        body { font-family: 'Noto Serif TC', serif; }
        .script-font { font-family: 'Dancing Script', cursive; }
    </style>
</head>
<body class="bg- text- ">

    <div class="max-w-2xl mx-auto pt-14 px-6 text-center">
        <div class="text- font-medium">陳若濋 <span class="script-font text- text- ">Rosy</span></div>
        <div class="text-2xl text- mt-1">RUO CHU, CHEN</div>
        <div class="text-xl text- mt-6">AI 產業鏈顧問 | AI Industry Chain Consultant</div>
    </div>

    <div class="max-w-md mx-auto mt-16 px-6">
        <div onclick="showResume()" class="bg-white border border- rounded-3xl p-8 text-center cursor-pointer">
            <i class="fa-solid fa-file-lines text-4xl text- mb-4"></i>
            <div class="text-2xl font-medium">專業履歷</div>
            <div class="text- ">Professional Standard Resume</div>
        </div>
    </div>

    <div class="max-w-md mx-auto mt-20 px-6">
        <div class="text-center text-xl font-medium mb-8">聯絡我</div>
        
        <div class="space-y-4">
            <div class="bg-white border border- rounded-2xl p-5">
                iOS 請優先傳 I message（最快速聯繫方式）<br>
                <span class="text- ">violet58889999@icloud.com</span>
            </div>
            
            <a href="mailto:rosychuchu999@duck.com" class="block bg-white border border- rounded-2xl p-5">📧 Email <span class="float-right text- ">點我</span></a>
            <a href="https://www.linkedin.com/in/999rosy0825" target="_blank" class="block bg-white border border- rounded-2xl p-5">💼 LinkedIn <span class="float-right text- ">點我</span></a>
            <a href="https://wa.me/886909999999" target="_blank" class="block bg-white border border- rounded-2xl p-5">📱 WhatsApp <span class="float-right text- ">點我</span></a>
            <a href="https://line.me/ti/p/9brhY8e-jP" target="_blank" class="block bg-white border border- rounded-2xl p-5">💚 Line <span class="float-right text- ">點我</span></a>
            
            <div onclick="showQR('wechat')" class="bg-white border border- rounded-2xl p-5 cursor-pointer">📱 WeChat 掃碼</div>
            <div onclick="showQR('telegram')" class="bg-white border border- rounded-2xl p-5 cursor-pointer">📱 Telegram 掃碼</div>
        </div>
    </div>

    <button onclick="toggleMusic()" class="fixed bottom-6 right-6 w-12 h-12 bg- text-white rounded-full flex items-center justify-center shadow-lg text-2xl">
        <i class="fa-solid fa-pause" id="musicIcon"></i>
    </button>

    <div id="player" style="display:none;"></div>

    <script src="https://www.youtube.com/iframe_api"></script>
    <script>
        let player, isPlaying = true;

        function onYouTubeIframeAPIReady() {
            player = new YT.Player('player', {
                height: '0', width: '0',
                videoId: 'jFksEU-cJPs',
                playerVars: { 'autoplay': 1, 'controls': 0 },
                events: { 'onReady': e => e.target.playVideo() }
            });
        }

        function toggleMusic() {
            if (!player) return;
            const icon = document.getElementById('musicIcon');
            isPlaying ? player.pauseVideo() : player.playVideo();
            icon.classList.toggle('fa-pause', !isPlaying);
            icon.classList.toggle('fa-seedling', isPlaying);
            isPlaying = !isPlaying;
        }

        function showResume() {
            alert("請把你的4張履歷圖片上傳到這個 GitHub 倉庫");
        }

        function showQR(type) {
            alert(type === 'wechat' ? "請上傳 WeChat QR Code" : "請上傳 Telegram QR Code");
        }
    </script>
</body>
</html>
