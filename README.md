<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ТЕСТ: НАСКІЛЬКИ ЗДОРОВИМИ Є ВАШІ ХАРЧОВІ ЗВИЧКИ?</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Georgia&family=Arial&display=swap">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-image: url('background_image_url'); /* URL зображення фону */
            background-size: cover;
            background-attachment: fixed;
            margin: 20px;
            color: #333;
        }
        h1 {
            font-family: 'Georgia', serif;
            color: #ee693f; /* Морковь */
            text-align: center;
            font-size: 2.5em;
            font-weight: bold;
            text-transform: uppercase;
        }
        .intro-text {
            font-size: 1.2em;
            font-weight: bold;
            margin-bottom: 20px;
        }
        .question {
            margin-bottom: 20px;
            padding: 15px;
            background-color: rgba(255, 255, 255, 0.8); /* Прозорий білий фон */
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            color: #739F3D;
        }
        .question label {
            color: #333; /* Чорний колір для відповідей */
        }
        .result {
            margin-top: 20px;
            font-weight: bold;
            padding: 15px;
            background-color: rgba(224, 247, 250, 0.8); /* Прозорий синій фон */
            border-radius: 5px;
            display: none;
        }
        button {
            padding: 15px 30px;
            font-size: 18px;
            color: #FFF;
            background-color: #739F3D; /* Грушевый */
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .center {
            text-align: center;
            margin-top: 20px;
        }
        .background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.2; /* Зменшення інтенсивності */
        }
        .heart {
            display: none;
        }
        .heart + label:before {
            content: '♡';
            font-size: 20px;
            color: #ccc;
            padding-right: 10px;
        }
        .heart:checked + label:before {
            content: '❤';
            font-size: 20px;
            color: #45a049;
            padding-right: 10px;
        }
        .highlight-link {
            color: #FFF;
            font-weight: bold;
            background-color: #ee693f;
            padding: 15px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-size: 18px;
            display: inline-block;
        }
        .highlight-link:hover {
            background-color: #d95e3f;
        }
    </style>
</head>
<body>
    <div class="background">
        <img src="background_image_url" alt="Background Image" style="width: 100%; height: 100%;">
    </div>
    <h1>ТЕСТ: НАСКІЛЬКИ ЗДОРОВИМИ Є ВАШІ ХАРЧОВІ ЗВИЧКИ?</h1>
    <p class="intro-text">Привіт! Давай перевіримо, наскільки здоровими є твої харчові звички. Це швидкий тест, який допоможе тобі зрозуміти, як добре ти харчуєшся і чи є щось, що можна покращити. Відповідай чесно, і в кінці отримаєш оцінку своїх звичок. Готовий дізнатися, наскільки здоровий твій раціон? Тоді почнімо!</p>
    
    <form id="quizForm">
        <div class="question">
            <p><strong>1. Як часто ви їсте овочі, фрукти та ягоди?</strong></p>
            <input type="radio" id="q1a" name="q1" value="1" class="heart"><label for="q1a"> Кожен день</label><br>
            <input type="radio" id="q1b" name="q1" value="2" class="heart"><label for="q1b"> Кілька разів на тиждень</label><br>
            <input type="radio" id="q1c" name="q1" value="3" class="heart"><label for="q1c"> Раз на тиждень</label><br>
            <input type="radio" id="q1d" name="q1" value="4" class="heart"><label for="q1d"> Рідше</label>
        </div>
        <div class="question">
            <p><strong>2. Скільки води ви п'єте щодня?</strong></p>
            <input type="radio" id="q2a" name="q2" value="1" class="heart"><label for="q2a"> 8 склянок або більше</label><br>
            <input type="radio" id="q2b" name="q2" value="2" class="heart"><label for="q2b"> 5-7 склянок</label><br>
            <input type="radio" id="q2c" name="q2" value="3" class="heart"><label for="q2c"> 2-4 склянки</label><br>
            <input type="radio" id="q2d" name="q2" value="4" class="heart"><label for="q2d"> Менше 2 склянок</label>
        </div>
        <div class="question">
            <p><strong>3. Як часто ви вживаєте оброблені продукти (наприклад, чіпси, солодощі, фастфуд)?</strong></p>
            <input type="radio" id="q3a" name="q3" value="1" class="heart"><label for="q3a"> Ніколи</label><br>
            <input type="radio" id="q3b" name="q3" value="2" class="heart"><label for="q3b"> Рідко</label><br>
            <input type="radio" id="q3c" name="q3" value="3" class="heart"><label for="q3c"> Кілька разів на тиждень</label><br>
            <input type="radio" id="q3d" name="q3" value="4" class="heart"><label for="q3d"> Щодня</label>
        </div>
        <div class="question">
            <p><strong>4. Як часто ви плануєте своє харчування?</strong></p>
            <input type="radio" id="q4a" name="q4" value="1" class="heart"><label for="q4a"> Завжди</label><br>
            <input type="radio" id="q4b" name="q4" value="2" class="heart"><label for="q4b"> Інколи</label><br>
            <input type="radio" id="q4c" name="q4" value="3" class="heart"><label for="q4c"> Рідко</label><br>
            <input type="radio" id="q4d" name="q4" value="4" class="heart"><label for="q4d"> Ніколи</label>
        </div>
        <div class="question">
            <p><strong>5. Як часто ви пропускаєте сніданок?</strong></p>
            <input type="radio" id="q5a" name="q5" value="1" class="heart"><label for="q5a"> Ніколи</label><br>
            <input type="radio" id="q5b" name="q5" value="2" class="heart"><label for="q5b"> Рідко</label><br>
            <input type="radio" id="q5c" name="q5" value="3" class="heart"><label for="q5c"> Часто</label><br>
            <input type="radio" id="q5d" name="q5" value="4" class="heart"><label for="q5d"> Завжди</label>
        </div>
        <div class="question">
            <p><strong>6. Як часто ви їсте червоне м'ясо?</strong></p>
            <input type="radio" id="q6a" name="q6" value="1" class="heart"><label for="q6a"> Ніколи</label><br>
            <input type="radio" id="q6b" name="q6" value="2" class="heart"><label for="q6b"> Рідко</label><br>
            <input type="radio" id="q6c" name="q6" value="3" class="heart"><label for="q6c"> Кілька разів на тиждень</label><br>
            <input type="radio" id="q6d" name="q6" value="4" class="heart"><label for="q6d"> Щодня</label>
        </div>
        <div class="question">
            <p><strong>7. Як часто ви їсте рибу та морепродукти?</strong></p>
            <input type="radio" id="q7a" name="q7" value="1" class="heart"><label for="q7a"> Кожен день</label><br>
            <input type="radio" id="q7b" name="q7" value="2" class="heart"><label for="q7b"> Кілька разів на тиждень</label><br>
            <input type="radio" id="q7c" name="q7" value="3" class="heart"><label for="q7c"> Раз на тиждень</label><br>
            <input type="radio" id="q7d" name="q7" value="4" class="heart"><label for="q7d"> Рідше</label>
        </div>
        <div class="question">
            <p><strong>8. Чи вживаєте ви цільнозернові продукти (наприклад, цільнозерновий хліб, коричневий рис та інші цільнозернові крупи)?</strong></p>
            <input type="radio" id="q8a" name="q8" value="1" class="heart"><label for="q8a"> Завжди</label><br>
            <input type="radio" id="q8b" name="q8" value="2" class="heart"><label for="q8b"> Інколи</label><br>
            <input type="radio" id="q8c" name="q8" value="3" class="heart"><label for="q8c"> Рідко</label><br>
            <input type="radio" id="q8d" name="q8" value="4" class="heart"><label for="q8d"> Ніколи</label>
        </div>
        <div class="question">
            <p><strong>9. Як часто ви їсте молочні продукти?</strong></p>
            <input type="radio" id="q9a" name="q9" value="1" class="heart"><label for="q9a"> Кожен день</label><br>
            <input type="radio" id="q9b" name="q9" value="2" class="heart"><label for="q9b"> Кілька разів на тиждень</label><br>
            <input type="radio" id="q9c" name="q9" value="3" class="heart"><label for="q9c"> Раз на тиждень</label><br>
            <input type="radio" id="q9d" name="q9" value="4" class="heart"><label for="q9d"> Рідше</label>
        </div>
        <div class="question">
            <p><strong>10. Як часто ви вживаєте солодкі напої та солодощі?</strong></p>
            <input type="radio" id="q10a" name="q10" value="1" class="heart"><label for="q10a"> Ніколи</label><br>
            <input type="radio" id="q10b" name="q10" value="2" class="heart"><label for="q10b"> Рідко</label><br>
            <input type="radio" id="q10c" name="q10" value="3" class="heart"><label for="q10c"> Кілька разів на тиждень</label><br>
            <input type="radio" id="q10d" name="q10" value="4" class="heart"><label for="q10d"> Щодня</label>
        </div>
        <div class="question">
            <p><strong>11. Чи враховуєте ви баланс білків, жирів і вуглеводів у своїй дієті?</strong></p>
            <input type="radio" id="q11a" name="q11" value="1" class="heart"><label for="q11a"> Завжди</label><br>
            <input type="radio" id="q11b" name="q11" value="2" class="heart"><label for="q11b"> Інколи</label><br>
            <input type="radio" id="q11c" name="q11" value="3" class="heart"><label for="q11c"> Рідко</label><br>
            <input type="radio" id="q11d" name="q11" value="4" class="heart"><label for="q11d"> Ніколи</label>
        </div>
        <div class="question">
            <p><strong>12. Чи контролюєте ви розмір порцій під час їжі?</strong></p>
            <input type="radio" id="q12a" name="q12" value="1" class="heart"><label for="q12a"> Завжди</label><br>
            <input type="radio" id="q12b" name="q12" value="2" class="heart"><label for="q12b"> Інколи</label><br>
            <input type="radio" id="q12c" name="q12" value="3" class="heart"><label for="q12c"> Рідко</label><br>
            <input type="radio" id="q12d" name="q12" value="4" class="heart"><label for="q12d"> Ніколи</label>
        </div>
        <div class="question">
            <p><strong>13. Як часто ви їсте на ходу або перед телевізором?</strong></p>
            <input type="radio" id="q13a" name="q13" value="1" class="heart"><label for="q13a"> Ніколи</label><br>
            <input type="radio" id="q13b" name="q13" value="2" class="heart"><label for="q13b"> Рідко</label><br>
            <input type="radio" id="q13c" name="q13" value="3" class="heart"><label for="q13c"> Кілька разів на тиждень</label><br>
            <input type="radio" id="q13d" name="q13" value="4" class="heart"><label for="q13d"> Щодня</label>
        </div>
        <div class="question">
            <p><strong>14. Чи уникаєте ви їжі перед сном (за 2-3 години до сну)?</strong></p>
            <input type="radio" id="q14a" name="q14" value="1" class="heart"><label for="q14a"> Завжди</label><br>
            <input type="radio" id="q14b" name="q14" value="2" class="heart"><label for="q14b"> Інколи</label><br>
            <input type="radio" id="q14c" name="q14" value="3" class="heart"><label for="q14c"> Рідко</label><br>
            <input type="radio" id="q14d" name="q14" value="4" class="heart"><label for="q14d"> Ніколи</label>
        </div>
        <button type="button" onclick="calculateScore()">Отримати результат</button>
    </form>
    
    <div id="result" class="result"></div>
    <div class="center">
        <a href="https://www.instagram.com/karyna_mayer/" class="highlight-link" target="_blank">ЗАПИСАТИСЬ НА КОНСУЛЬТАЦІЮ</a>
    </div>
    
    <script>
        function calculateScore() {
            const form = document.getElementById('quizForm');
            let score = 0;
            const questions = 14; // Кількість питань
            let allAnswered = true;
            for (let i = 1; i <= questions; i++) {
                const answer = form['q' + i].value;
                if (answer) {
                    score += parseInt(answer);
                } else {
                    allAnswered = false;
                }
            }
            if (!allAnswered) {
                alert("Будь ласка, відповідайте на всі питання перед тим, як отримати результат.");
                return;
            }
            let resultText = '';
            if (score <= 22) {
                resultText = 'Вітаю! Твої харчові звички на висоті. Ти обираєш правильні продукти, плануєш прийоми їжі та контролюєш їхній розмір. Щоб ще більше покращити своє здоров\'я, зверни увагу на можливість додати різноманітності у свій раціон, спробуй нові рецепти або продукти. Твій рівень вже високий, але завжди є можливість для вдосконалення!';
            } else if (score <= 36) {
                resultText = 'Твої харчові звички досить здорові, але є кілька аспектів, які можна покращити. Наприклад, можна збільшити споживання свіжих овочів і фруктів або зменшити споживання оброблених продуктів. Можливо, варто звернути увагу на розмір порцій та частоту прийомів їжі. Ти вже на правильному шляху до здорового харчування, і ці кроки допоможуть тобі досягти ще кращих результатів.';
            } else if (score <= 50) {
                resultText = 'Твої харчові звички потребують змін. Ти можеш поліпшити свій раціон, додаючи більше свіжих овочів і фруктів, пити більше води та зменшити споживання оброблених продуктів. Також зверни увагу на регулярність прийомів їжі та намагайся уникати перекусів на ходу. Ці прості кроки допоможуть тобі покращити здоров\'я та самопочуття.';
            } else {
                resultText = 'Твої харчові звички викликають занепокоєння і можуть негативно впливати на твоє здоров\'я. Постарайся зменшити споживання оброблених продуктів і солодощів, збільшити кількість свіжих овочів і фруктів у своєму раціоні, та пити більше води. Зосередься на регулярних прийомах їжі і уникай переїдання. Ці зміни допоможуть тобі покращити свій стан здоров\'я.';
            }
            document.getElementById('result').innerText = resultText;
            document.getElementById('result').style.display = 'block';
        }
    </script>
</body>
</html>
