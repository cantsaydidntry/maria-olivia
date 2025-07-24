<html lang="pt-br">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Lucas + Maria Olivia</title>
    <style>
        html, body {
            margin: 0; padding: 0;
            background-color: black;
            color: red;
            font-family: Arial, sans-serif;
            text-align: center;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            overflow-x: hidden;
        }

        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 1s ease, transform 1s ease;
        }

        .show {
            opacity: 1;
            transform: translateY(0);
        }

        .top {
            margin-top: 5vh;
            font-size: 6vw;
            font-weight: bold;
            text-shadow: 0 0 10px red;
        }

        .middle {
            margin-top: 3vh;
            font-size: 5vw;
            text-shadow: 0 0 8px red;
        }

        .bottom {
            margin-bottom: 3vh;
            font-size: 4vw;
            text-shadow: 0 0 5px red;
        }

        .heart {
    width: 15vw;
    height: 15vw;
    background: red;
    position: relative;
    margin: 5vh auto 0 auto;
    transform: rotate(-45deg);
    animation: pulse 1s infinite;
    box-shadow: 0 0 20px red;
}

.heart::before,
.heart::after {
    content: "";
    width: 15vw;
    height: 15vw;
    background: red;
    border-radius: 50%;
    position: absolute;
}

.heart::before {
    top: -7.5vw;
    left: 0;
}

.heart::after {
    top: 0;
    left: 7.5vw;
}


        @keyframes pulse {
            0% { transform: scale(1) rotate(-45deg); }
            50% { transform: scale(1.1) rotate(-45deg); }
            100% { transform: scale(1) rotate(-45deg); }
        }
    </style>
</head>
<body>

    <div class="top fade-in">LUCAS + MARIA OLIVIA</div>

    <div class="heart fade-in" style="animation-delay: 0.2s;"></div>

    <div class="middle fade-in">maria olivia livs meu amor</div>

    <div class="bottom fade-in">#UsemDrogas</div>

    <script>
        window.addEventListener("load", () => {
            const elements = document.querySelectorAll(".fade-in");
            elements.forEach((el, index) => {
                setTimeout(() => {
                    el.classList.add("show");
                }, index * 300);
            });
        });
    </script>
</body>
</html>
