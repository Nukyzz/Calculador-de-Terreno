
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Área de Terreno</title>
    <style>
        body {
            font-family: sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f9;
            margin: 0;
        }
        .container {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            width: 300px;
        }
        h2 { color: #333; text-align: center; }
        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        .resultado {
            margin-top: 20px;
            padding: 15px;
            background-color: #e7f3fe;
            border-left: 6px solid #2196F3;
            font-weight: bold;
            text-align: center;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Área do Terreno</h2>
    
    <label for="largura">Largura (metros):</label>
    <input type="number" id="largura" placeholder="Ex: 10" oninput="calcular()">

    <label for="comprimento">Comprimento (metros):</label>
    <input type="number" id="comprimento" placeholder="Ex: 25" oninput="calcular()">

    <div class="resultado" id="display-resultado">
        Área: 0 m²
    </div>
</div>

<script>
    function calcular() {
        // Pega os valores dos inputs
        const largura = document.getElementById('largura').value;
        const comprimento = document.getElementById('comprimento').value;
        const display = document.getElementById('display-resultado');

        // Valida se os campos estão preenchidos
        if (largura > 0 && comprimento > 0) {
            const area = largura * comprimento;
            display.innerHTML = `Área: ${area.toLocaleString('pt-BR')} m²`;
        } else {
            display.innerHTML = "Área: 0 m²";
        }
    }
</script>

</body>
</html>
