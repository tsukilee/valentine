# valentine
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Sweetheart 💕</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            text-align: center;
            background-color: #ffe6f2;
            color: #ff4d6d;
            position: relative;
            overflow: hidden;
        }
        .container {
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            border-radius: 10px;
            background-color: white;
            box-shadow: 2px 2px 10px rgba(255, 0, 0, 0.3);
            animation: fadeIn 1s ease-in-out;
        }
        button {
            background-color: #ff4d6d;
            color: white;
            border: none;
            padding: 10px 20px;
            margin-top: 10px;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
            transition: transform 0.2s;
        }
        button:hover {
            transform: scale(1.1);
        }
        .hidden {
            display: none;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>
    <div class="container" id="letter-container">
        <h2>For My Sweetheart 💕</h2>
        <p id="letter-text">Dear Love,</p>
        <button onclick="nextLetter()">Next</button>
    </div>
    <div class="container hidden" id="valentine-container">
        <h2>Now the big question... 💖</h2>
        <h1>Will you be my Valentine? 💘</h1>
        <button onclick="alert('Yay! 💖')">YES</button>
        <button onclick="alert('Double Yay! 💕')">YES</button>
    </div>
    <script>
        const letters = [
            "Dear Love,", 
            "From the moment I met you, my world became brighter.",
            "Every day with you is a new adventure, and I cherish each moment.",
            "You make me laugh, smile, and feel truly special.",
            "I just want you to know how much I adore you."
        ];
        let currentLetter = 0;
        const letterText = document.getElementById("letter-text");
        const letterContainer = document.getElementById("letter-container");
        const valentineContainer = document.getElementById("valentine-container");

        function nextLetter() {
            currentLetter++;
            if (currentLetter < letters.length) {
                letterText.innerText = letters[currentLetter];
            } else {
                letterContainer.classList.add("hidden");
                valentineContainer.classList.remove("hidden");
            }
        }
    </script>
</body>
</html>
