# u-really-suck
u just suck
<!DOCTYPE html>
<html lang="no">
<head>
    <meta charset="UTF-8">
    <title>welcome sucker</title>
    <style>
        body {
            background-color: #00f;
            color: #fff;
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            text-align: center;
            overflow: hidden;
        }

        h1 { font-size: 3rem; margin-bottom: 10px; }
        p { font-size: 1.5rem; color: #FF0; }

        #run-away-btn {
            padding: 15px 30px;
            font-size: 1.2rem;
            background: #fff;
            border: none;
            cursor: pointer;
            position: absolute;
            transition: 0.1s;
        }
    </style>
</head>
<body>

    <h1>u suck!</h1>
    <p id="insult">you suck <br> 0 funnet.</p>

    <button id="run-away-btn" onmouseover="flykt()">click here if ur smart smart</button>

    <script>
        const fornærmelser = [
            "u smel like feet.",
            "u look very human.",
            "ur hair is not very good loking",
            "u look like u eat banana bread."
        ];

        // Bytter fornærmelse hvert 3. sekund
        setInterval(() => {
            const random = Math.floor(Math.random() * fornærmelser.length);
            document.getElementById('insult').innerText = fornærmelser[random];
        }, 3000);

        // Gjør det umulig å klikke på knappen
        function flykt() {
            const btn = document.getElementById('run-away-btn');
            const x = Math.random() * (window.innerWidth - btn.clientWidth);
            const y = Math.random() * (window.innerHeight - btn.clientHeight);
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }
    </script>
</body>
</html>
