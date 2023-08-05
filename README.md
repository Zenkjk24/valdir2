<!DOCTYPE html>
<html>

<head>
    <title>Botão Sim e Não</title>
    <style>
        body {
            position: relative;
        }

        #naoBtn {
            position: absolute;
        }

        #imagemAleatoria {
            display: none;
            position: absolute;
        }
    </style>
</head>

<body>
    <h1>Botão Sim e Não</h1>
    <button onclick="responderSim()" id="simBtn">Sim</button>
    <button onclick="moverNao()" id="naoBtn">Não</button>

    <img src="meci.jpg" id="imagemAleatoria">

    <script>
        function moverNao() {
            var naoBtn = document.getElementById("naoBtn");
            var imagemAleatoria = document.getElementById("imagemAleatoria");
            var screenWidth = window.innerWidth;
            var screenHeight = window.innerHeight;

            var randomX = Math.floor(Math.random() * (screenWidth - naoBtn.clientWidth));
            var randomY = Math.floor(Math.random() * (screenHeight - naoBtn.clientHeight));

            naoBtn.style.left = randomX + "px";
            naoBtn.style.top = randomY + "px";

            imagemAleatoria.style.left = randomX + "px";
            imagemAleatoria.style.top = randomY + "px";
            imagemAleatoria.style.display = "block";
        }

        function responderSim() {
            var simBtn = document.getElementById("simBtn");
            simBtn.style.display = "none";
        }
    </script>
</body>

</html>
