<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quick Question</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f0f2f5;
            overflow: hidden;
        }
        h1 { color: #333; }
        .container { position: relative; width: 100%; height: 300px; text-align: center; }
        
        button {
            padding: 15px 30px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 50px;
            border: none;
            transition: transform 0.2s;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        #yesBtn {
            background-color: #4CAF50;
            color: white;
            box-shadow: 0 4px 15px rgba(76, 175, 80, 0.3);
        }

        #noBtn {
            background-color: #f44336;
            color: white;
            position: absolute;
            transition: 0.1s ease;
            box-shadow: 0 4px 15px rgba(244, 67, 54, 0.3);
        }
    </style>
</head>
<body>

    <h1>Are you happy?</h1>

    <div class="container">
        <button id="yesBtn" onclick="alert('I knew it! ❤️')">
            <span>😊</span> Yes
        </button>
        
        <button id="noBtn" onmouseover="moveButton()" onclick="alert('How did you even click this?!')">
            <span>😢</span> No
        </button>
    </div>

    <script>
        function moveButton() {
            const btn = document.getElementById('noBtn');
            // Calculate random positions within the visible window
            const x = Math.random() * (window.innerWidth - btn.offsetWidth);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight);
            
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }
    </script>

</body>
</html>
