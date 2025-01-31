# San-Valentin<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>¿Quieres ser mi San Valentín?</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(45deg, #ff69b4, #ffb6c1);
            font-family: Arial, sans-serif;
            color: #333;
        }
        .container {
            text-align: center;
            background: rgba(255, 255, 255, 0.95);
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            width: 90%;
        }
        .profile-img {
            width: 300px;
            height: 300px;
            border-radius: 15px;
            margin: 20px auto;
            display: block;
            object-fit: cover;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        .message {
            font-size: 1.2rem;
            line-height: 1.6;
            margin: 20px 0;
            padding: 20px;
            background: rgba(255, 105, 180, 0.1);
            border-radius: 10px;
        }
        .buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 30px;
        }
        .btn {
            padding: 15px 40px;
            font-size: 1.2rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .btn-si {
            background: #ff69b4;
            color: white;
        }
        .btn-no {
            background: #666;
            color: white;
        }
        .btn:hover {
            transform: scale(1.1);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        .hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1000;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="/api/placeholder/300/300" alt="Tu foto especial" class="profile-img">
        <div class="message">
            Gracias por iluminar cada uno de mis días con tu presencia,
            por llenar mi vida de sonrisas y momentos inolvidables.
            Tu compañía ha sido el regalo más hermoso que la vida me ha dado.
            Cada momento contigo es especial, cada sonrisa tuya hace que mi corazón lata más fuerte.
            <br><br>
            Después de todo lo que hemos vivido juntos, tengo una pregunta muy especial para ti...
            <br><br>
            ¿Quieres ser mi San Valentín? ❤️
        </div>
        <div class="buttons">
            <button class="btn btn-si" onclick="decirSi()">¡Sí!</button>
            <button class="btn btn-no" onclick="decirNo()">No</button>
        </div>
        <audio id="myAudio" loop>
            <source src="barro-duki.mp3" type="audio/mpeg">
        </audio>
    </div>

    <script>
        function decirSi() {
            const emailBody = "¡Ha dicho que SÍ! 💕";
            sendNotification(emailBody, true);
            createHearts();
        }

        function decirNo() {
            const emailBody = "Ha dicho que NO 💔";
            sendNotification(emailBody, false);
        }

        function createHearts() {
            const heartsContainer = document.createElement('div');
            heartsContainer.className = 'hearts';
            document.body.appendChild(heartsContainer);
            
            for(let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.innerHTML = '❤️';
                    heart.style.position = 'absolute';
                    heart.style.left = Math.random() * 100 + 'vw';
                    heart.style.top = '-20px';
                    heart.style.fontSize = (Math.random() * 20 + 10) + 'px';
                    heart.style.animation = 'fall 4s linear';
                    heartsContainer.appendChild(heart);
                    
                    setTimeout(() => heart.remove(), 4000);
                }, i * 100);
            }
        }

        async function sendNotification(message, response) {
            const email = "johanstivengonzalez.0303@gmail.com";
            const whatsapp = "3125031077";
            
            console.log(`Enviando notificación a ${email} y ${whatsapp}`);
            console.log(`Mensaje: ${message}`);
            
            alert(response ? 
                "¡Gracias por decir que sí! ❤️ Te amo mucho" : 
                "Entiendo tu decisión, gracias por ser sincera ❤️"
            );
        }

        document.body.addEventListener('click', function() {
            const audio = document.getElementById('myAudio');
            audio.play().catch(e => console.log('Error al reproducir audio:', e));
        });
    </style>
    <style>
        @keyframes fall {
            to {
                transform: translateY(100vh);
            }
        }
    </style>
</body>
</html>
