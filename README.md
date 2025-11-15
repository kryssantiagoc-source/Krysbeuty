<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Krys Santiago Coiffeur</title>

    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: #fff8f8;
            margin: 0;
            padding: 0;
            color: #333;
        }

        header {
            text-align: center;
            padding: 40px 20px;
            background: #ffe6ef;
            border-bottom: 2px solid #f7c8d8;
        }

        header h1 {
            margin: 0;
            font-size: 28px;
            letter-spacing: 2px;
        }

        header h2 {
            margin: 5px 0 0;
            font-size: 18px;
            font-weight: 300;
        }

        .container {
            max-width: 500px;
            margin: 40px auto;
            background: #ffffff;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
        }

        label {
            font-weight: bold;
            display: block;
            margin-bottom: 6px;
        }

        input, textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: 1px solid #e6b8c6;
            border-radius: 8px;
            background: #fff5f7;
        }

        button {
            width: 100%;
            padding: 14px;
            background: #ffb6c9;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        button:hover {
            background: #f79ab2;
        }

        .comanda-box {
            margin-top: 25px;
            padding: 20px;
            background: #fff1f4;
            border: 1px solid #f7c8d8;
            border-radius: 10px;
        }
    </style>
</head>

<body>

    <header>
        <h1>KRYS SANTIAGO COIFFEUR</h1>
        <h2>Consulta de Comanda</h2>
    </header>

    <div class="container">
        <label for="nome">Nome da Cliente:</label>
        <input type="text" id="nome" placeholder="Ex: Ana Paula">

        <label for="valor">Valor Total:</label>
        <input type="text" id="valor" placeholder="Ex: R$ 250,00">

        <label for="detalhes">Procedimentos Realizados:</label>
        <textarea id="detalhes" rows="4" placeholder="Ex: Luzes, hidratação, tonalização"></textarea>

        <button onclick="gerarComanda()">Gerar Comanda</button>

        <div id="resultado"></div>
    </div>

    <script>
        function gerarComanda() {
            let nome = document.getElementById('nome').value;
            let valor = document.getElementById('valor').value;
            let detalhes = document.getElementById('detalhes').value;

            let box = `
                <div class='comanda-box'>
                    <h3>Comanda de ${nome}</h3>
                    <p><strong>Valor total:</strong> ${valor}</p>
                    <p><strong>Procedimentos:</strong><br>${detalhes.replace(/\n/g,'<br>')}</p>
                </div>
            `;

            document.getElementById('resultado').innerHTML = box;
        }
    </script>

</body>
</html>
