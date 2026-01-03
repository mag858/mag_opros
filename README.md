
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="author" content="Glushnev Mikhail Alekseevich">
    <meta name="description" content="MAG Industries – опрос по электронным наручным часам">
    <meta name="keywords" content="MAG industries, опрос, электронные часы, смарт-часы, гаджеты, стартап">
    <title>MAG Industries | Опрос по электронным часам</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Roboto:wght@300;400&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary: #F3A000;
            --red: #FF0000;
            --bg: #CCE1FE;
            --text: #222;
            --shadow: 0 4px 15px rgba(0,0,0,0.1);
            --card-bg: rgba(255,255,255,0.9);
        }
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.6;
            animation: fadeIn 1.5s ease-out;
        }
        
        .back-btn {
            position: fixed;
            top: 15px;
            left: 15px;
            padding: 10px 18px;
            background: rgba(255,255,255,0.9);
            color: var(--text);
            text-decoration: none;
            font-weight: 600;
            font-size: 0.95rem;
            border-radius: 30px;
            box-shadow: var(--shadow);
            transition: all 0.3s ease;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }
        
        .back-btn:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-3px);
        }
        
        .hero {
            text-align: center;
            padding: 80px 20px 40px;
        }
        
        .logo {
            max-width: 320px;
            border-radius: 20px;
            box-shadow: var(--shadow);
            margin-bottom: 20px;
            transition: transform 0.5s ease;
            animation: slideUp 1s ease-out;
        }
        
        .logo:hover { transform: scale(1.05); }
        
        h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 3rem;
            color: var(--primary);
            margin: 0 0 10px 0;
        }
        
        .subtitle {
            font-size: 1.6rem;
            color: #333;
            font-weight: 500;
            margin-bottom: 50px;
        }
        
        .survey {
            max-width: 900px;
            margin: 0 auto 80px;
            padding: 40px;
            background: var(--card-bg);
            border-radius: 20px;
            box-shadow: var(--shadow);
            animation: fadeInUp 1.5s ease-out;
        }
        
        .survey h3 {
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            font-size: 2.4rem;
            color: var(--primary);
            margin-bottom: 40px;
        }
        
        .user-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 50px;
            padding: 20px;
            background: rgba(255,255,255,0.6);
            border-radius: 15px;
        }
        
        .user-info input {
            width: 100%;
            padding: 14px;
            border: 2px solid #ddd;
            border-radius: 12px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .user-info input:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 15px rgba(243,160,0,0.3);
        }
        
        .question {
            margin-bottom: 50px;
            padding: 25px;
            background: rgba(255,255,255,0.6);
            border-radius: 15px;
            opacity: 0;
            animation: fadeInUp 1s ease-out forwards;
        }
        
        .question b {
            font-size: 1.3rem;
            display: block;
            margin-bottom: 25px;
            color: var(--text);
        }
        
        .options {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .option-item {
            position: relative;
        }
        
        .option-item input[type="checkbox"] {
            position: absolute;
            opacity: 0;
            cursor: pointer;
            width: 100%;
            height: 100%;
            z-index: 2;
        }
        
        .option-btn {
            display: block;
            padding: 14px 24px;
            background: white;
            border: 3px solid var(--primary);
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            min-width: 160px;
            box-shadow: var(--shadow);
            text-align: center;
            cursor: pointer;
        }
        
        .option-btn:hover {
            background: rgba(243,160,0,0.1);
            transform: translateY(-3px);
        }
        
        /* Полное заливание оранжевым при выборе */
        .option-item input[type="checkbox"]:checked ~ .option-btn {
            background: var(--primary) !important;
            color: white;
            border-color: var(--primary);
        }
        
        .text-input {
            width: 100%;
            max-width: 600px;
            margin: 20px auto 0;
            padding: 14px;
            border: 2px solid #ddd;
            border-radius: 12px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .text-input:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 15px rgba(243,160,0,0.3);
        }
        
        .buttons {
            text-align: center;
            margin: 60px 0 20px;
        }
        
        input[type="submit"], input[type="reset"] {
            padding: 16px 40px;
            margin: 0 15px;
            font-size: 1.2rem;
            font-weight: 600;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.4s ease;
            box-shadow: var(--shadow);
        }
        
        input[type="submit"] {
            background: var(--primary);
            color: white;
        }
        
        input[type="submit"]:hover {
            background: var(--red);
            transform: translateY(-5px) scale(1.05);
        }
        
        input[type="reset"] {
            background: #ccc;
            color: var(--text);
        }
        
        input[type="reset"]:hover {
            background: #999;
            color: white;
        }
        
        .privacy {
            text-align: center;
            font-size: 0.9rem;
            color: #666;
            margin-top: 40px;
        }
        
        footer {
            text-align: center;
            padding: 40px;
            background: var(--card-bg);
            font-size: 0.9rem;
            color: #666;
        }
        
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @keyframes slideUp { from { opacity: 0; transform: translateY(50px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
        
        .question:nth-child(1) { animation-delay: 0.2s; }
        .question:nth-child(2) { animation-delay: 0.4s; }
        .question:nth-child(3) { animation-delay: 0.6s; }
        .question:nth-child(4) { animation-delay: 0.8s; }
        .question:nth-child(5) { animation-delay: 1.0s; }
        .question:nth-child(6) { animation-delay: 1.2s; }
        .question:nth-child(7) { animation-delay: 1.4s; }
        
        @media (max-width: 768px) {
            .back-btn { top: 10px; left: 10px; padding: 8px 14px; font-size: 0.9rem; }
            .hero { padding-top: 70px; }
            h1 { font-size: 2.4rem; }
            .subtitle { font-size: 1.4rem; }
            .survey { margin: 20px; padding: 25px; }
            .survey h3 { font-size: 2rem; }
            .option-btn { min-width: 140px; padding: 12px 16px; font-size: 1rem; }
            .logo { max-width: 280px; }
        }
    </style>
</head>
<body>

    <a href="https://mag858.github.io/MAG-industries/" class="back-btn">← На главную</a>

    <section class="hero">
        <img src="sait/logo_2.jpeg" alt="Логотип MAG Industries" class="logo">
        <h1>future - right now</h1>
        <div class="subtitle">(будущее - прямо сейчас)</div>
    </section>

    <section class="survey">
        <h3>Опрос по электронным наручным часам</h3>
        
        <div class="user-info">
            <input type="text" name="имя" placeholder="Ваше Имя" required>
            <input type="number" name="возраст" placeholder="Сколько вам лет" min="1" max="120">
            <input type="email" name="email" placeholder="Ваш email" required>
        </div>

        <form action="https://api.web3forms.com/submit" method="POST">
            <input type="hidden" name="access_key" value="cabd165b-582a-434a-8aec-d05523b4c7f7">

            <div class="question">
                <b>1) Какой тип дисплея вы предпочитаете?</b>
                <div class="options">
                    <div class="option-item">
                        <input type="checkbox" name="1. AMOLED" id="amoled">
                        <label for="amoled" class="option-btn">AMOLED / OLED</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="1. LCD" id="lcd">
                        <label for="lcd" class="option-btn">LCD / IPS</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="1. E-Ink" id="eink">
                        <label for="eink" class="option-btn">E-Ink (как в Kindle)</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="1. всегда включен" id="aod">
                        <label for="aod" class="option-btn">Always On Display</label>
                    </div>
                </div>
            </div>

            <div class="question">
                <b>2) Какие функции для вас важны?</b>
                <div class="options">
                    <div class="option-item">
                        <input type="checkbox" name="2. уведомления" id="notify">
                        <label for="notify" class="option-btn">Уведомления</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="2. фитнес" id="fitness">
                        <label for="fitness" class="option-btn">Шагомер / Фитнес</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="2. пульс" id="pulse">
                        <label for="pulse" class="option-btn">Пульс / Давление</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="2. GPS" id="gps">
                        <label for="gps" class="option-btn">Встроенный GPS</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="2. музыка" id="music">
                        <label for="music" class="option-btn">Хранение музыки</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="2. звонки" id="calls">
                        <label for="calls" class="option-btn">Звонки по Bluetooth</label>
                    </div>
                </div>
                <input type="text" name="2. свои функции" class="text-input" placeholder="Другие функции, которые вы хотите видеть...">
            </div>

            <div class="question">
                <b>3) Какой дизайн корпуса нравится?</b>
                <div class="options">
                    <div class="option-item">
                        <input type="checkbox" name="3. круглый" id="round">
                        <label for="round" class="option-btn">Круглый</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="3. квадратный" id="square">
                        <label for="square" class="option-btn">Квадратный / Прямоугольный</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="3. минимализм" id="minimal">
                        <label for="minimal" class="option-btn">Минималистичный</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="3. спортивный" id="sport">
                        <label for="sport" class="option-btn">Спортивный / Защитный</label>
                    </div>
                </div>
            </div>

            <div class="question">
                <b>4) Как долго должна работать батарея?</b>
                <div class="options">
                    <div class="option-item">
                        <input type="checkbox" name="4. 1 день" id="day1">
                        <label for="day1" class="option-btn">1 день</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="4. 3-5 дней" id="days35">
                        <label for="days35" class="option-btn">3–5 дней</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="4. неделя" id="week">
                        <label for="week" class="option-btn">Неделя</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="4. более недели" id="moreweek">
                        <label for="moreweek" class="option-btn">Более недели</label>
                    </div>
                </div>
            </div>

            <div class="question">
                <b>5) Какой размер корпуса часов оптимален?</b>
                <input type="text" name="5. размер корпуса" class="text-input" placeholder="Например: 35x25x14 мм">
            </div>

            <div class="question">
                <b>6) Какой материал корпуса вы предпочитаете?</b>
                <div class="options">
                    <div class="option-item">
                        <input type="checkbox" name="6. пластик" id="plastic">
                        <label for="plastic" class="option-btn">Пластик</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="6. алюминий" id="aluminum">
                        <label for="aluminum" class="option-btn">Алюминий</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="6. сталь" id="steel">
                        <label for="steel" class="option-btn">Нержавеющая сталь</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="6. титан" id="titan">
                        <label for="titan" class="option-btn">Титан</label>
                    </div>
                </div>
                <input type="text" name="6. свой материал" class="text-input" placeholder="Другой материал или пожелания...">
            </div>

            <div class="question">
                <b>7) Сколько вы готовы заплатить за электронные часы?</b>
                <div class="options">
                    <div class="option-item">
                        <input type="checkbox" name="7. до 50$" id="under50">
                        <label for="under50" class="option-btn">До 50 $</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="7. 50-150$" id="50-150">
                        <label for="50-150" class="option-btn">50–150 $</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="7. 150-300$" id="150-300">
                        <label for="150-300" class="option-btn">150–300 $</label>
                    </div>
                    <div class="option-item">
                        <input type="checkbox" name="7. более 300$" id="over300">
                        <label for="over300" class="option-btn">Более 300 $</label>
                    </div>
                </div>
            </div>

            <div class="question">
                <b>8) Ваши дополнительные пожелания (дизайн, функции и т.д.)</b>
                <input type="text" name="8. пожелания" class="text-input" placeholder="Напишите свои идеи...">
            </div>

            <div class="buttons">
                <input type="submit" value="Отправить">
                <input type="reset" value="Сброс">
            </div>
        </form>

        <div class="privacy">
            Все ваши ответы строго конфиденциальны и не передаются третьим лицам.
        </div>
    </section>

    <footer>
        обновление 3.1 &emsp; январь 2026 г.
    </footer>

</body>
</html>
