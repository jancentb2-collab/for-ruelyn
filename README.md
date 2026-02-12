<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Pretty Girl</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%);
            font-family: 'Arial', sans-serif;
            text-align: center;
            overflow: hidden;
        }

        .container {
            background: rgba(255, 255, 255, 0.95);
            padding: 40px;
            border-radius: 30px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.1);
            max-width: 500px;
            border: 2px solid #ff4d6d;
        }

        h1 { color: #ff1493; font-size: 2.5rem; margin-bottom: 20px; line-height: 1.2; }
        
        .heart {
            font-size: 50px;
            display: inline-block;
            animation: heartBeat 1.2s infinite;
            margin-bottom: 10px;
        }

        @keyframes heartBeat {
            0% { transform: scale(1); }
            14% { transform: scale(1.3); }
            28% { transform: scale(1); }
            42% { transform: scale(1.3); }
            70% { transform: scale(1); }
        }

        .buttons { 
            margin-top: 30px; 
            display: flex; 
            justify-content: center; 
            align-items: center;
            gap: 20px;
            min-height: 100px;
        }

        button {
            padding: 15px 35px;
            font-size: 1.2rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.2s ease;
            font-weight: bold;
        }

        #yesBtn { background-color: #ff4d6d; color: white; z-index: 999; }
        #noBtn { background-color: #999; color: white; position: relative; }

        .final-message {
            font-size: 1.8rem;
            color: #ff4d6d;
            font-weight: bold;
            margin-top: 20px;
        }

        .thank-you {
            font-size: 1.2rem;
            color: #d02090;
            margin-top: 20px;
            font-style: italic;
        }
    </style>
</head>
<body>

    <div class="container" id="cardContainer">
        <div class="heart">❤️</div>
        <h1>WILL YOU BE MY VALENTINE MY RUELYN?</h1>
        
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">YES!</button>
            <button id="noBtn" onmouseover="moveBtn()">No</button>
        </div>
    </div>

    <script>
        let scale = 1;

        function moveBtn() {
            const noBtn = document.getElementById('noBtn');
            const yesBtn = document.getElementById('yesBtn');
            
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
            noBtn.style.position = 'absolute';
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';

            scale += 0.5;
            yesBtn.style.transform = `scale(${scale})`;
        }

        function celebrate() {
            document.getElementById('cardContainer').innerHTML = `
                <div class="heart" style="font-size: 80px;">💖</div>
                <h1 style="font-size: 3rem;">YAY! 🥰</h1>
                <div class="final-message">
                    I LOVE YOU BIG TIME MY BEAUTIFUL BABY GIRL!
                </div>
                <div class="thank-you">
                    Thank you for being the best girlfriend ever!
                </div>
            `;
            document.body.style.background = "#ff4d6d";
        }
    </script>
</body>
</html>
