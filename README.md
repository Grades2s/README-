<!DOCTYPE html>
<html>
<head>
    <style>
        /* Temel stil */
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }

        /* Animasyon efekti */
        @keyframes moveButton {
            from {
                transform: translate(0, 0);
            }
            to {
                transform: translate(
                    calc(100% - 100px),
                    calc(100vh - 150px)
                );
            }
        }

        /* Düğme stil */
        #myButton {
            width: 100px;
            height: 50px;
            background-color: #3498db;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            animation: moveButton 2s ease infinite;
        }
    </style>
</head>
<body>
    <h1>Grade Interpide</h1>
    <button id="myButton">Butona Tıkla</button>

    <script>
        // Düğme tıklanınca
        document.getElementById('myButton').addEventListener('click', function() {
            // Düğmeyi rastgele bir konuma taşı
            const button = document.getElementById('myButton');
            const maxX = window.innerWidth - button.clientWidth;
            const maxY = window.innerHeight - button.clientHeight;

            const randomX = Math.random() * maxX;
            const randomY = Math.random() * maxY;

            button.style.transform = `translate(${randomX}px, ${randomY}px)`;
        });
    </script>
</body>
</html>
