<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>שער האריות</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f0f0f0;
        }

        .main-title {
            text-align: center;
            color: #333;
            font-size: 2.5em;
            margin-bottom: 30px;
        }

        .view-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-bottom: 30px;
        }

        .view-button {
            padding: 15px 25px;
            font-size: 1.1em;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .view-button:hover {
            background-color: #45a049;
        }

        .content-section {
            display: none;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            margin: 20px auto;
            max-width: 800px;
            opacity: 0;
            transition: opacity 0.3s ease-in-out;
        }

        .content-section.active {
            display: block;
            opacity: 1;
        }

        .tour-image {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            margin: 15px 0;
        }
    </style>
</head>
<body>
    <h1 class="main-title">שער האריות</h1>

    <div class="view-buttons">
        <button class="view-button" onclick="showContent('front-view')">מבט חזיתי</button>
        <button class="view-button" onclick="showContent('lions')">האריות</button>
        <button class="view-button" onclick="showContent('inside-view')">מבט מבפנים</button>
        <button class="view-button" onclick="showContent('inscriptions')">כתובות היסטוריות</button>
    </div>

    <div id="front-view" class="content-section">
        <img src="images/lions-gate.jpg" alt="מבט חזיתי על שער האריות" class="tour-image">
    </div>

    <div id="lions" class="content-section">
        <img src="images/lions-closeup.jpg" alt="האריות המפורסמים" class="tour-image">
    </div>

    <div id="inside-view" class="content-section">
        <img src="תמונה-3.jpg" alt="מבט מבפנים" class="tour-image">
        <h2>מבט מתוך השער</h2>
        <p>המעבר בשער מוביל ישירות אל הרובע המוסלמי ואל ויה דולורוזה. השער משמש כניסה מרכזית להר הבית ולמסגד אל-אקצא.</p>
    </div>

    <div id="inscriptions" class="content-section">
        <img src="תמונה-4.jpg" alt="הכתובות ההיסטוריות" class="tour-image">
        <h2>הכתובות ההיסטוריות</h2>
        <p>מעל השער ישנן כתובות בערבית המספרות על בנייתו בשנת 1538-1539 בתקופת השלטון העות'מאני.</p>
    </div>

    <script>
        function showContent(sectionId) {
            // הסתר את כל החלקים
            document.querySelectorAll('.content-section').forEach(section => {
                section.classList.remove('active');
            });
            
            // הצג את החלק שנבחר
            document.getElementById(sectionId).classList.add('active');
        }
    </script>
</body>
</html>
