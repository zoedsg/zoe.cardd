<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Card de Preço</title>
    <style>
        /* Fundo rosa */
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(to bottom, #ffb6c1, #ff69b4);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        /* Nuvens animadas */
        .clouds {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://www.transparenttextures.com/patterns/clouds.png');
            opacity: 0.3;
            animation: moveClouds 20s linear infinite;
        }

        @keyframes moveClouds {
            from {
                background-position: 0 0;
            }
            to {
                background-position: 1000px 500px;
            }
        }

        /* Card de Preço */
        .pricing-card {
            background: white;
            width: 300px;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
            transform: scale(0);
            opacity: 0;
            transition: opacity 1.5s ease-out, transform 1.5s ease-out;
            position: relative;
            z-index: 10;
        }

        .pricing-card h3 {
            font-size: 22px;
            color: #333;
        }

        .price {
            font-size: 28px;
            font-weight: bold;
            color: #ff69b4;
            margin: 10px 0;
        }

        .pricing-card ul {
            list-style: none;
            padding: 0;
        }

        .pricing-card ul li {
            padding: 8px 0;
            border-bottom: 1px solid #eee;
        }

        .pricing-card ul li:last-child {
            border-bottom: none;
        }

        .pricing-card button {
            background-color: #ff69b4;
            color: white;
            border: none;
            padding: 12px;
            width: 100%;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 15px;
            font-size: 16px;
        }

        .pricing-card button:hover {
            background-color: #d94d8c;
        }

    </style>
</head>
<body>

    <div class="clouds"></div>

    <div class="pricing-card" id="card">
        <h3>Plano Premium</h3>
        <p class="price">R$49,90/mês</p>
        <ul>
            <li>✔ Acesso ilimitado</li>
            <li>✔ Suporte 24/7</li>
            <li>✔ Sem anúncios</li>
            <li>✔ Conteúdo exclusivo</li>
        </ul>
        <button>Assinar agora</button>
    </div>

    <script>
        // Espera 2 segundos antes de mostrar o card suavemente
        window.onload = function() {
            setTimeout(() => {
                let card = document.getElementById("card");
                card.style.opacity = "1";
                card.style.transform = "scale(1)";
            }, 2000);
        };
    </script>

</body>
</html>