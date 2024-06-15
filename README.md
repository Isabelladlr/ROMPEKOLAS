<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pregunta</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            flex-direction: column;
        }
        .container {
            text-align: center;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        .buttons {
            margin-top: 20px;
            position: relative;
            height: 50px; /* Asegúrate de que haya suficiente espacio para mover el botón "No" */
        }
        button {
            padding: 10px 20px;
            margin: 0 10px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .yes {
            background-color: #4CAF50;
            color: white;
        }
        .no {
            background-color: #f44336;
            color: white;
            position: absolute;
        }
        .message {
            margin-top: 30px;
            font-size: 18px;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Walid, ¿me amarías si fuese un gusanito? 🥹👉🏼👈🏼</h1>
        <div class="buttons">
            <button class="yes" onclick="alert('¡Gracias!')">Sí</button>
            <button class="no" onmouseover="moveButton()">No</button>
        </div>
        <div class="message">Te amo Walid</div>
    </div>

    <script>
        function moveButton() {
            const noButton = document.querySelector('.no');
            const container = document.querySelector('.container');
            const containerRect = container.getBoundingClientRect();
            const noButtonRect = noButton.getBoundingClientRect();

            let newTop = Math.random() * (containerRect.height - noButtonRect.height);
            let newLeft = Math.random() * (containerRect.width - noButtonRect.width);

            noButton.style.top = ${newTop}px;
            noButton.style.left = ${newLeft}px;
        }
    </script>
</body>
</html>
