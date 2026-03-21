# u-really-suck
u just suck
            
  <title>Velkommen tapere</title>
    <style>
        body {
            background-color: #000;
            color: #0f0;
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
        p { font-size: 1.5rem; color: #ff00ea; }

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

    <h1>Systemfeil: Bruker er for teit</h1>
    <p id="insult">Leter etter hjerneceller... <br> 0 funnet.</p>

    <button id="run-away-btn" onmouseover="flykt()">Klikk her hvis du er smart</button>

    <script>
        const fornærmelser = [
            "Du ser ut som noen som bruker sokker i sandaler.",
            "Jeg har sett brødristere med høyere IQ enn deg.",
            "Var det meningen at du skulle se sånn ut i dag?",
            "Du er grunnen til at vi har advarsler på sjampoflasker."
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
