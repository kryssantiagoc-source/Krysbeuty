<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Krys Santiago Coiffeur - Comandas</title>

    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: #f8f2f5;
            margin: 0;
            padding: 0;
            text-align: center;
            color: #3a2a2a;
        }

        header {
            padding: 30px;
            background: #ffffff;
            border-bottom: 2px solid #f1d7dd;
        }

        h1 {
            font-size: 26px;
            margin: 0;
            letter-spacing: 2px;
        }

        .logo-flor {
            width: 80px;
            margin-top: 10px;
        }

        .container {
            margin-top: 30px;
            max-width: 400px;
            margin-left: auto;
            margin-right: auto;
            background: #ffffff;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 0 10px rgba(0,0,0,0.05);
        }

        label {
            font-weight: 600;
            font-size: 14px;
        }

        input {
            width: 100%;
            padding: 12px;
            margin-top: 8px;
            margin-bottom: 20px;
            border: 1px solid #e2c1c9;
            border-radius: 8px;
            font-size: 16px;
        }

        button {
            width: 100%;
            padding: 14px;
            border: none;
            background: #e8a4b3;
            color: white;
            font-size: 16px;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
        }

        button:hover {
            background: #d98b9e;
        }

        .resultado {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
            color: #8a4d60;
        }
    </style>
</head>

<body>

<header>
    <h1>KRYS SANTIAGO COIFFEUR</h1>
    <p>Consulta de Comandas</p>
</header>

<div class="container">
    <label for="nome">Digite o nome da cliente:</label>
    <input type="text" id="nome" placeholder="Ex: Ana Souza">

    <button onclick="buscarComanda()">Ver Comanda</button>

    <p class="resultado" id="resultado"></p>
</div>

<script>
    const comandas = {
        "ana souza": "R$ 250 — Luzes + Hidratação",
        "maria fernanda": "R$ 180 — Escova + Nutrição",
        "clara mendes": "R$ 350 — Loiro Global",
        "lais costa": "R$ 90 — Sobrancelha + Hidratação"
    };

    function buscarComanda() {
        let nome = document.getElementById("nome").value.trim().toLowerCase();
        let resultado = document.getElementById("resultado");

        if (comandas[nome]) {
            resultado.innerHTML = "Total da comanda: " + comandas[nome];
        } else {
            resultado.innerHTML = "Cliente não encontrada. Verifique o nome.";
        }
    }
</script>

</body>
</html>
