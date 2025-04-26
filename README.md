<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Graduation Card</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-image: url('person-of-homage.jpg');
            background-size: cover;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            overflow: hidden;
        }
        .card {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 20px;
            text-align: center;
            max-width: 400px;
            margin: 20px;
            animation: fadeIn 2s ease-in-out;
        }
        .card img {
            width: 100%;
            height: auto;
            border-radius: 8px;
            animation: zoomIn 2s ease-in-out;
        }
        .card h1 {
            font-size: 24px;
            color: #333;
            animation: slideDown 1.5s ease-in-out;
        }
        .card p {
            font-size: 16px;
            color: #555;
            line-height: 1.5;
            animation: fadeIn 2.2s ease-in-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes zoomIn {
            from {
                transform: scale(0.8);
                opacity: 0;
            }
            to {
                transform: scale(1);
                opacity: 1;
            }
        }

        @keyframes slideDown {
            from {
                transform: translateY(-20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
    </style>
</head>
<body>
    <audio id="bgAudio" loop>
        <source src="mild-high-club-homage.mp3" type="audio/mp3">
        Your browser does not support the audio element.
    </audio>
    <div class="card">
        <img src="foto-x.jpg" alt="Foto Wahidatul Millah">
        <h1>Happy Graduation, Wahidatul Millah!</h1>
        <p>
            Congratulation, Millah! So proud of you. :v
        </p>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const audio = document.getElementById('bgAudio');

            // Cek apakah browser mendukung autoplay
            audio.play().then(() => {
                console.log('Audio autoplay berhasil.');
            }).catch(error => {
                console.error('Audio autoplay gagal:', error);
                alert('Audio tidak bisa autoplay. Klik di mana saja pada halaman untuk memulai lagu.');

                // Tunggu interaksi pengguna
                document.body.addEventListener('click', () => {
                    audio.play();
                }, { once: true });
            });
        });
    </script>
</body>
</html>
