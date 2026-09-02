<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cookie Clicker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f8f1e4;
        }
        h1 {
            color: #5a3e2b;
        }
        #cookie {
            width: 200px;
            cursor: pointer;
            transition: transform 0.1s;
        }
        #cookie:active {
            transform: scale(0.95);
        }
        #score {
            font-size: 24px;
            margin-top: 20px;
            color: #5a3e2b;
        }
        button {
            margin-top: 20px;
            padding: 10px 20px;
            font-size: 16px;
            background-color: #d2691e;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #a0522d;
        }
    </style>
</head>
<body>

    <h1>🍪 Cookie Clicker 🍪</h1>
    <img id="cookie" src="https://upload.wikimedia.org/wikipedia/commons/6/69/Chocolate_Chip_Cookie.png" alt="Cookie">
    <div id="score">Cookies: 0</div>
    <button id="resetBtn">Reset</button>

    <script>
        let score = 0;

        const cookie = document.getElementById('cookie');
        const scoreDisplay = document.getElementById('score');
        const resetBtn = document.getElementById('resetBtn');

        // Increase score when cookie is clicked
        cookie.addEventListener('click', () => {
            score++;
            scoreDisplay.textContent = `Cookies: ${score}`;
        });

        // Reset score
        resetBtn.addEventListener('click', () => {
            score = 0;
            scoreDisplay.textContent = `Cookies: ${score}`;
        });
    </script>

</body>
</html>
