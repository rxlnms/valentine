<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <h1>Сабира, есть важный вопрос...</h1>
    <title>Be My Valentine?</title>
    <style>
        body {
            font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
            text-align: center;
            background-color: #ffe6e6;
        }
        h1 {
            color: #ff4d4d;
            margin-top: 50px;
        }
        .buttons {
            margin-top: 30px;
        }
        button {
            font-size: 24px;
            padding: 15px 30px;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
        }
        .yes-btn {
            background-color: #ff4d4d;
            color: white;
        }
        .yes-btn:hover {
            background-color: #ff1a1a;
        }
        .no-btn {
            background-color: #999;
            color: white;
        }
        .heart {
            color: #ff4d4d;
            font-size: 50px;
            animation: float 2s infinite ease-in-out;
            position: absolute;
        }
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }
    </style>
</head>
<body>
    <h1>Ты будешь моей парой на день Святого Валентина?</h1>
    <div class="buttons">
        <button class="yes-btn" id="yes-btn" onclick="alert('УРАААА СПАСИБО!')">Да</button>
        <button class="no-btn" onclick="growYesButton()">Нет</button>
    </div>
    <script>
        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤';
            document.body.appendChild(heart);
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.top = Math.random() * 100 + 'vh';
            setTimeout(() => heart.remove(), 3000);
        }
        setInterval(createHeart, 500);

        function growYesButton() {
            let yesBtn = document.getElementById('yes-btn');
            let currentSize = parseInt(window.getComputedStyle(yesBtn).fontSize);
            yesBtn.style.fontSize = (currentSize + 10) + 'px';
        }
    </script>
</body>
</html>
