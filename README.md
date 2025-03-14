# Fire.Bitch
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Горящий сайт</title>
    <style>
        body {
            text-align: center;
            padding: 50px;
            font-family: Arial, sans-serif;
            overflow: hidden; /* Скрывает прокрутку при видео */
        }
        .button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }
        .error {
            display: none;
            color: red;
            font-size: 24px;
            margin-top: 20px;
        }
        #fireVideo {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: none; /* Скрываем видео изначально */
        }
    </style>
</head>
<body>

<h1>Нажмите кнопку, чтобы "зажечь" сайт!</h1>
<button class="button" onclick="ignite()">Зажечь!</button>
<div class="error" id="error">Ошибка: Сайт загорелся!</div>
<video id="fireVideo" autoplay muted>
    <source src="" type="video/mp4">
    Ваш браузер не поддерживает видео.
</video>

<script>
    function ignite() {
        document.getElementById('fireVideo').style.display = 'block'; // Показываем видео
        document.getElementById('fireVideo').play(); // Запускаем видео

        setTimeout(() => {
            document.getElementById('fireVideo').style.display = 'none'; // Скрываем видео через 5 секунд
            document.getElementById('error').style.display = 'block'; // Показываем сообщение об ошибке
        }, 5000); // Через 5 секунд
    }
</script>

</body>
</html>
