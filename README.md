<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            background-color: #ffdde1;
            color: #d10056;
            overflow: hidden;
        }
        #container {
            position: relative;
            margin-top: 50px;
        }
        img {
            width: 60%;
            border-radius: 15px;
            box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.2);
        }
        #buttons {
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
            position: relative;
        }
        #yesBtn {
            background-color: #ff4081;
            color: white;
        }
        #noBtn {
            background-color: #cccccc;
        }
        #lyrics {
            position: fixed;
            bottom: 10px;
            right: 10px;
            background: white;
            padding: 10px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
        }
        #finalMessage {
            display: none;
        }
    </style>
</head>
<body>

    <script>
        const password = "marwanisthebest";
        let userInput = prompt("Enter the secret password to access:");
        if (userInput !== password) {
            document.body.innerHTML = "<h1>Access Denied ❌</h1>";
            throw new Error("Access Denied");
        }
    </script>

    <div id="container">
        <h1>Will you be my Valentine? 💖</h1>
        <img src="first-image.jpg" id="mainImage">
        <div id="buttons">
            <button id="yesBtn" onclick="acceptLove()">Yes 💕</button>
            <button id="noBtn" onmousemove="avoidNo()">No 😢</button>
        </div>
    </div>

    <div id="finalMessage">
        <h1>LETS GO FROM GETTING REJECTED TO BEING UR VALENTINE I LOVE YOU 💖</h1>
        <img src="second-image.jpg">
    </div>

    <audio autoplay loop>
        <source src="romantic-killer.mp3" type="audio/mp3">
    </audio>

    <div id="lyrics">
        <iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/7s5VQqrjBtrBgZL4pEa46S?utm_source=generator" width="300" height="80" frameBorder="0" allowfullscreen allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
    </div>

    <script>
        function acceptLove() {
            document.getElementById('container').style.display = 'none';
            document.getElementById('finalMessage').style.display = 'block';
        }

        function avoidNo() {
            let noBtn = document.getElementById("noBtn");
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            noBtn.style.position = "absolute";
            noBtn.style.left = `${x}px`;
            noBtn.style.top = `${y}px`;
        }
    </script>

</body>
</html>
