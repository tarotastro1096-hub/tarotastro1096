<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Glitchy Hacker UI</title>
    <style>
        body {
            background-color: black;
            color: #00ff00;
            font-family: monospace;
            overflow: hidden;
        }
        h1 {
            text-align: center;
            font-size: 50px;
            animation: glitch 1s infinite;
        }
        @keyframes glitch {
            0% { text-shadow: 2px 0 red, -2px 0 blue; }
            20% { text-shadow: -2px 0 red, 2px 0 blue; }
            40% { text-shadow: 2px 0 red, -2px 0 blue; }
            60% { text-shadow: -2px 0 red, 2px 0 blue; }
            100% { text-shadow: none; }
        }
        pre {
            font-size: 20px;
            animation: flicker 2s infinite;
        }
        @keyframes flicker {
            0%, 20%, 40%, 60%, 100% { opacity: 1; }
            10%, 30%, 50%, 70%, 90% { opacity: 0; }
        }
    </style>
</head>
<body>
    <h1>WELCOME TO THE HACKER ZONE</h1>
    <pre>
░░▀▄░░░░░░▄▀░░░░░░░░░░░░░░░░░▄░░░░░░░░░░▄▄▀▀▄▄░░░░░░
░░░░█░░▄░░█░░▀▀▀░░░░░░░▄▄░░░░█░░░░░░░▄▀░░░░█░░░░░░
░░░░░░█░░█░░░░░░▄▄█░░░░▄██░░░░▒██████░░░░▀▄░░░░░░░░
░░░░░░█▄░░░█░░▀▄█▒██░░▄███░░░░░░█░░███▄░░░░█░░░░░░░
░░░░░░░░▀▄▄█▄▄▄▄▀▄░░▄▀▀░░█░░░░░░░░░░█░░░▀█▄▄▄░░░░░░
    </pre>
    <script>
        let interval = 100;
        let glitchText = document.getElementsByTagName('pre')[0];
        setInterval(() => {
            glitchText.innerHTML = glitchText.innerHTML.split('').map(c => Math.random() > 0.8 ? '░' : c).join('');
        }, interval);
    </script>
</body>
</html>