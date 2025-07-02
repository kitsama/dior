<!DOCTYPE html>
<html>
<head>
    <title>Прости меня</title>
    <style>
        body {
            background-color: pink;
            text-align: center;
            font-family: Arial, sans-serif;
            padding-top: 100px;
        }
        h1 {
            color: #ff1493;
            font-size: 40px;
        }
        button {
            padding: 15px 30px;
            font-size: 20px;
            margin: 20px;
            cursor: pointer;
            border: none;
            border-radius: 10px;
            transition: all 0.3s;
        }
        #forgive {
            background-color: #4CAF50;
            color: white;
        }
        #dont-forgive {
            background-color: #f44336;
            color: white;
        }
        #sweet {
            font-size: 50px;
            color: #ff1493;
            display: none;
            margin-top: 30px;
        }
        .firework {
            position: absolute;
            width: 5px;
            height: 5px;
            border-radius: 50%;
            background-color: #ff0000;
            animation: explode 1s ease-out;
            opacity: 0;
        }
        @keyframes explode {
            0% { transform: scale(0); opacity: 1; }
            100% { transform: scale(20); opacity: 0; }
        }
    </style>
</head>
<body>
    <h1>宝贝你能原谅我吗</h1>
    <button id="forgive">原谅</button>
    <button id="dont-forgive">不原谅</button>
    <div id="sweet">你得了甜品!</div>

    <script>
        const forgiveBtn = document.getElementById('forgive');
        const dontForgiveBtn = document.getElementById('dont-forgive');
        const sweetText = document.getElementById('sweet');
        let scale = 1;

        dontForgiveBtn.addEventListener('click', function() {
            scale += 0.3;
            dontForgiveBtn.style.transform = `scale(${scale})`;
        });

        forgiveBtn.addEventListener('click', function() {
            sweetText.style.display = 'block';
            createFireworks();
        });

        function createFireworks() {
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const firework = document.createElement('div');
                    firework.className = 'firework';
                    firework.style.left = Math.random() * window.innerWidth + 'px';
                    firework.style.top = Math.random() * window.innerHeight + 'px';
                    firework.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 50%)`;
                    document.body.appendChild(firework);
                    
                    setTimeout(() => {
                        firework.remove();
                    }, 1000);
                }, i * 100);
            }
        }
    </script>
</body>
</html>

