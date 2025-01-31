<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi San Valentín?</title>
    <style>
        body {
            margin: 0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(45deg, #ff69b4, #ffb6c1);
            font-family: Arial, sans-serif;
            color: #333;
            padding: 20px;
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
            white-space: pre-line;
        }
        
        .buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 30px;
            flex-wrap: wrap;
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
        
        @keyframes fall {
            to {
                transform: translateY(100vh) rotate(360deg);
            }
        }
        
        .heart {
            position: absolute;
            font-size: 20px;
            animation: fall 4s linear;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/4gHYSUNDX1BST0ZJTEUAAQEAAAHIAAAAAAQwAABtbnRyUkdCIFhZWiAH4AABAAEAAAAAAABhY3NwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQAA9tYAAQAAAADTLQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAlkZXNjAAAA8AAAACRyWFlaAAABFAAAABRnWFlaAAABKAAAABRiWFlaAAABPAAAABR3dHB0AAABUAAAABRyVFJDAAABZAAAAChnVFJDAAABZAAAAChiVFJDAAABZAAAAChjcHJ0AAABjAAAADxtbHVjAAAAAAAAAAEAAAAMZW5VUwAAAAgAAAAcAHMAUgBHAEJYWVogAAAAAAAAb6IAADj1AAADkFhZWiAAAAAAAABimQAAt4UAA
