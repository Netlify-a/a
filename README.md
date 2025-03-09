<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>المسرحية المرعبة</title>
    <style>
        body {
            background: url('https://source.unsplash.com/1600x900/?haunted,mansion') no-repeat center center fixed;
            background-size: cover;
            color: white;
            font-family: 'Arial', sans-serif;
            text-align: center;
            overflow: hidden;
        }
        .container {
            margin-top: 10%;
        }
        h1 {
            font-size: 3em;
            text-shadow: 4px 4px 10px black;
        }
        p {
            font-size: 1.5em;
            background: rgba(0, 0, 0, 0.6);
            padding: 20px;
            border-radius: 10px;
            display: inline-block;
        }
        .qr-code {
            margin-top: 20px;
        }
        .ghost {
            position: absolute;
            width: 100px;
            height: 100px;
            background: url('https://cdn-icons-png.flaticon.com/512/1970/1970977.png') no-repeat center;
            background-size: contain;
            opacity: 0.7;
            animation: float 3s infinite;
        }
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>مرحبًا بكم في قصر الظلام</h1>
        <p>اكتشفوا أسرار القصر المسكون وواجهوا الأشباح ومصاصي الدماء في هذه المغامرة الشيقة.</p>
        <div class="qr-code">
            <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://yourwebsite.com" alt="QR Code">
        </div>
    </div>
    <script>
        document.addEventListener('mousemove', function(e) {
            let ghost = document.createElement('div');
            ghost.classList.add('ghost');
            ghost.style.left = `${e.pageX}px`;
            ghost.style.top = `${e.pageY}px`;
            document.body.appendChild(ghost);
            setTimeout(() => ghost.remove(), 1000);
        });
    </script>
</body>
</html>
