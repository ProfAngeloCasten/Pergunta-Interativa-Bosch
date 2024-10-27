# Pergunta Interativa Bosch
Pergunta interativa codificada em html exclusivamente para o processo seletivo da empresa Bosch.

Código em html:

    <!DOCTYPE html>
    <html lang="pt-br">
    <head>
        <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Pergunta Interativa</title>
        <style>
            body {
                display: flex;
                align-items: center;
                justify-content: center;
                height: 100vh;
                font-family: 'Roboto', sans-serif;
                background-color: RoyalBlue;
            }
            .container {
                text-align: center;
            }
            h1 {
                font-size: 60px;
                color: white;
                margin-bottom: 10px;
                text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
                font-weight: 500;
                letter-spacing: 1px;
            }
            .btn {
                padding: 12px 24px;
                margin: 10px;
                font-size: 35px;
                cursor: pointer;
                border: none;
                border-radius: 8px;
                background-color: white;
                color: red;
                transition: background-color 0.3s, transform 0.3s;
            }
            .btn:hover {
                background-color: LightSkyBlue;
                transform: scale(1.05);
            }
            #btnNao {
                position: absolute;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <h1>Mereço entrar para a Bosch?</h1>
            <button id="btnSim" class="btn" onclick="mostrarMensagem()">Sim</button>
            <button id="btnNao" class="btn" onmouseover="moverBotao()">Não</button>
            <p id="mensagem"></p>
        </div>
        <script>
            function mostrarMensagem() {
                document.getElementById("mensagem").innerText = "Muito obrigada, agradeço a oportunidade!";
            }
    
            function moverBotao() {
                const botaoNao = document.getElementById("btnNao");
                const larguraTela = window.innerWidth - botaoNao.offsetWidth;
                const alturaTela = window.innerHeight - botaoNao.offsetHeight;
    
                const novaPosX = Math.floor(Math.random() * larguraTela);
                const novaPosY = Math.floor(Math.random() * alturaTela);
    
                botaoNao.style.left = `${novaPosX}px`;
                botaoNao.style.top = `${novaPosY}px`;
            }
        </script>
    </body>
    </html>
