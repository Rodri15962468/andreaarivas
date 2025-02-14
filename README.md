<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para ti, Andrea 🌸</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(45deg, #ff9a9e, #fad0c4);
            color: #5a3e36;
            text-align: center;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 100%;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        h1 {
            color: #e67e22;
            font-size: 2em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }

        .fotos {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin: 20px 0;
            flex-wrap: wrap;
        }

        .fotos img {
            width: 100%;
            max-width: 300px;
            height: auto;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            transition: transform 0.3s;
        }

        .fotos img:hover {
            transform: scale(1.05);
        }

        .mensaje {
            background: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 15px;
            margin: 20px 0;
            position: relative;
        }

        .corazon {
            font-size: 1.5em;
            color: #e74c3c;
            animation: latido 1.2s infinite;
        }

        @keyframes latido {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }

        .quote {
            font-style: italic;
            margin: 20px 0;
            color: #e67e22;
            font-size: 1em;
        }

        footer {
            margin-top: 30px;
            padding: 10px;
            background: rgba(230, 126, 34, 0.1);
            border-radius: 10px;
        }

        .corazones-flotantes {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }

        .corazones-flotantes span {
            position: absolute;
            color: #e74c3c;
            font-size: 24px;
            animation: flotar 5s linear infinite;
        }

        @keyframes flotar {
            0% {
                transform: translateY(100vh) rotate(0deg);
            }
            100% {
                transform: translateY(-10vh) rotate(360deg);
            }
        }

        .niebla-romantica {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.1);
            z-index: 0;
            pointer-events: none;
        }

        @media (max-width: 600px) {
            h1 {
                font-size: 1.8em;
            }
            .fotos img {
                max-width: 100%;
            }
            .mensaje {
                padding: 15px;
            }
            .quote {
                font-size: 0.9em;
            }
        }
    </style>
</head>
<body>
    <div class="corazones-flotantes">
        <span>❤️</span>
        <span>💖</span>
        <span>💕</span>
        <span>🌸</span>
        <span>🌹</span>
    </div>

    <div class="niebla-romantica"></div>

    <div class="container">
        <h1>Para ti, Andrea <span class="corazon">❤️</span></h1>
        
        <div class="fotos">
            <img src="foto1.jpg" alt="Nuestro momento favorito">
        </div>

        <div class="mensaje">
            <p>Querida Andrea,</p>
            
            <p>Hay personas que llegan como el atardecer: despacio, pintando todo de colores que ni sabía que existían. Tú has sido así para mí. Cada conversación, cada risa y hasta esos silencios incómodos, han ido llenando espacios que no sabía que estaban vacíos.</p>

            <p class="quote">"El amor no es mirarse el uno al otro, sino mirar juntos en la misma dirección"</p>

            <p>No quiero apresurar nada, porque lo que siento es demasiado valioso como para convertirlo en una carrera. Prefiero caminar a tu lado, aprender de tus miedos y celebrar tus alegrías, aunque sea desde donde tú me permitas estar.</p>

            <p>Estas fotos son solo instantes de todo lo que me gustaría atesorar contigo. No necesito promesas grandiosas, solo la oportunidad de demostrarte que cuando digo "te quiero", es con paciencia, con respeto y con la tranquilidad de que eres libre de sentir (o no) lo mismo.</p>

            <p>Gracias por existir tal como eres.<br>
            Con todo mi cariño,<br>
            José 💖</p>
        </div>

        <footer>
            <p>Hecho con ❤️ · Cada detalle es para ti, Andrea.</p>
        </footer>
    </div>

    <script>
        const corazonesContainer = document.querySelector('.corazones-flotantes');
        const emoticones = ['❤️', '💖', '💕', '🌸', '🌹'];

        for (let i = 0; i < 50; i++) { 
            const corazon = document.createElement('span');
            corazon.textContent = emoticones[Math.floor(Math.random() * emoticones.length)];
            corazon.style.left = Math.random() * 100 + 'vw';
            corazon.style.animationDuration = Math.random() * 3 + 2 + 's';
            corazon.style.fontSize = Math.random() * 20 + 10 + 'px';
            corazonesContainer.appendChild(corazon);
        }
    </script>
</body>
</html>
