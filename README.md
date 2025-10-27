<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Autenticación</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            text-align: center;
            padding: 20px;
        }
        .container {
            margin: auto;
            padding: 20px;
            max-width: 400px;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            background-color: #ffffff;
        }
        input[type="text"], input[type="password"] {
            padding: 10px;
            width: 100%;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ddd;
        }
        button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Autenticación</h1>
        <label for="username">Nombre de usuario</label>
        <input type="text" id="username" placeholder="Ingresa tu usuario">

        <label for="password" class="hidden">Contraseña</label>
        <input type="password" id="password" placeholder="Ingresa tu contraseña" class="hidden">

        <button id="auth-button">Enviar</button>

        <div id="question-section" class="hidden">
            <p>¿Lia Thais es la super influencer?</p>
            <button id="yes-button">Sí</button>
            <button id="no-button">No</button>
        </div>

        <div id="final-section" class="hidden">
            <p>¡Muy bien! 🎉</p>
        </div>
    </div>

    <script>
        const usernameInput = document.getElementById('username');
        const passwordInput = document.getElementById('password');
        const authButton = document.getElementById('auth-button');
        const questionSection = document.getElementById('question-section');
        const finalSection = document.getElementById('final-section');
        const yesButton = document.getElementById('yes-button');
        const noButton = document.getElementById('no-button');

        let usernameValidated = false;

        authButton.addEventListener('click', () => {
            const username = usernameInput.value.trim().toLowerCase();

            if (!usernameValidated) {
                if (username === 'la lisa') {
                    usernameValidated = true;
                    passwordInput.classList.remove('hidden');
                    document.querySelector('label[for="password"]').classList.remove('hidden');
                    alert('Nombre de usuario correcto. Ahora ingresa tu contraseña.');
                } else {
                    alert('Nombre de usuario incorrecto.');
                }
            } else {
                const password = passwordInput.value.trim().toLowerCase();
                if (password === 'blackpink') {
                    document.querySelector('.container').querySelectorAll('input, button, label').forEach(el => el.classList.add('hidden'));
                    questionSection.classList.remove('hidden');
                } else {
                    alert('Contraseña incorrecta.');
                }
            }
        });

        yesButton.addEventListener('click', () => {
            questionSection.classList.add('hidden');
            finalSection.classList.remove('hidden');
            setTimeout(() => {
                window.open('https://youtube.com/@andreagonzales-oj2je?si=YrxPfNwthAPFcY1x', '_blank');
            }, 2000);
        });

        noButton.addEventListener('click', () => {
            alert('¡Claro que lo eres! 😄');
        });
    </script>
</body>
</html>