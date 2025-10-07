<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tulipanes para mi Kathe</title>
    
    <style>
        /* AJUSTES GLOBALES Y CENTRADO FLEXBOX */
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            background: radial-gradient(circle at bottom, #3a0ca3 10%, #240046 90%);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            font-family: sans-serif;
        }

        /* CONTENEDOR DE TEXTO */
        .love-text-container {
            position: relative;
            z-index: 10; 
            text-align: center;
            margin-bottom: 20px; 
        }

        .love-text {
            font-size: 5vw; 
            font-weight: bold;
            color: #c77dff;
            line-height: 1.25; 
            margin-bottom: 10px; 
            display: block; 
            text-shadow:
                0 0 10px #c77dff,
                0 0 20px #d0a3ff,
                0 0 40px #e0baff,
                0 0 60px #f0d0ff;
            animation: glow 2s ease-in-out infinite alternate;
        }

        /* CONTENEDOR DE FLORES */
        .garden {
            position: relative;
            display: flex;
            gap: 60px;
            margin-top: 20px; 
        }

        /* Tallo */
        .stem {
            width: 6px;
            height: 180px;
            background: linear-gradient(to top, #2e8b57, #3cb371);
            border-radius: 3px;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: flex-end;
        }

        /* Flor (tulipán) */
        .tulip {
            position: absolute;
            bottom: 170px;
            width: 60px;
            height: 70px;
            background: linear-gradient(to top, #ffffff 5%, #c77dff 60%, #7b2cbf 100%);
            border-radius: 60% 60% 0 0;
            box-shadow:
                inset 0 -5px 10px rgba(123, 44, 191, 0.4),
                0 3px 10px rgba(0, 0, 0, 0.4);
            animation: bloom 4s ease-in-out infinite alternate;
        }

        /* Hojas */
        .leaf {
            position: absolute;
            bottom: 40px;
            width: 40px;
            height: 80px;
            background: linear-gradient(to top, #2e8b57, #6fbf73);
            border-radius: 10% 80% 10% 80%;
            transform-origin: bottom center;
            opacity: 0.9;
            box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
        }

        .leaf.left {
            left: -25px;
            transform: rotate(-30deg);
        }

        .leaf.right {
            right: -25px;
            transform: rotate(30deg);
        }

        /* Animaciones */
        @keyframes bloom {
            0% { transform: scale(0.95) translateY(0); }
            50% { transform: scale(1.05) translateY(-5px); }
            100% { transform: scale(0.95) translateY(0); }
        }

        @keyframes glow {
            from {
                text-shadow:
                    0 0 5px #b77bff,
                    0 0 15px #c77dff,
                    0 0 30px #d7b8ff,
                    0 0 50px #e9d1ff;
            }
            to {
                text-shadow:
                    0 0 15px #d0a3ff,
                    0 0 30px #e0baff,
                    0 0 50px #f0d0ff,
                    0 0 70px #ffffff;
            }
        }
    </style>
</head>
<body>
    
    <div class="love-text-container">
        <span class="love-text">Para</span>
        <span class="love-text">mi</span>
        <span class="love-text">Kathe</span>
    </div>
    
    <div class="garden">
        
        <div class="stem">
            <div class="tulip"></div>
            <div class="leaf left"></div>
            <div class="leaf right"></div>
        </div>

        <div class="stem">
            <div class="tulip"></div>
            <div class="leaf left"></div>
            <div class="leaf right"></div>
        </div>

        <div class="stem">
            <div class="tulip"></div>
            <div class="leaf left"></div>
            <div class="leaf right"></div>
        </div>
    </div>
</body>
</html>
