<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do you love me?</title>
    <style>
        body {
            text-align: center;
            background-color: #FFDCE0;
            font-family: 'Arial', sans-serif;
        }
        #container {
            margin-top: 50px;
        }
        #questionContainer {
            position: relative;
            width: 300px;
            height: 100px;
            margin: auto;
        }
        #question {
            font-size: 24px;
            font-weight: bold;
            margin-top: 10px;
            color: #333;
        }
        #noBtn, #yesBtn {
            position: absolute;
            padding: 10px 20px;
            border: none;
            border-radius: 20px;
            font-size: 16px;
            cursor: pointer;
            color: white;
        }
        #noBtn {
            background-color: #FF4D6D;
            left: 200px;
            top: 60px;
        }
        #yesBtn {
            background-color: #FF69B4;
            left: 50px;
            top: 60px;
        }
        #resultContainer {
            display: none;
            margin-top: 20px;
        }
        #resultText {
            font-size: 22px;
            color: #FF4D6D;
        }
    </style>
</head>
<body>
    <div id="container">
        <!-- Ảnh gấu dễ thương -->
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3Bp65rlePz5vd15G_xkAGZjs2mlyIPsWuKQ&s">
        <p id="question">Do you love me?</p>
        <div id="questionContainer">
            <button id="yesBtn">Yes</button>
            <button id="noBtn">No</button>
        </div>
    </div>
    
    <div id="resultContainer">
        <p id="resultText">💖 Yay! I love you too! 💖</p>
        <!-- Ảnh meme cute -->
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTxDdfnyxGbxkcW_M9UZkKkLcjJj2GDQqJyBQ&s">
    </div>

    <script>
        const questionContainer = document.getElementById("questionContainer");
        const noBtn = document.getElementById("noBtn");
        const yesBtn = document.getElementById("yesBtn");
        const resultContainer = document.getElementById("resultContainer");

        noBtn.addEventListener("mouseover", () => {
            const maxX = questionContainer.offsetWidth - noBtn.offsetWidth;
            const maxY = questionContainer.offsetHeight - noBtn.offsetHeight;
            const newX = Math.floor(Math.random() * maxX);
            const newY = Math.floor(Math.random() * maxY);
            noBtn.style.left = `${newX}px`;
            noBtn.style.top = `${newY}px`;
        });

        yesBtn.addEventListener("click", () => {
            questionContainer.style.display = "none";
            resultContainer.style.display = "block";
        });
    </script>
</body>
</html>
