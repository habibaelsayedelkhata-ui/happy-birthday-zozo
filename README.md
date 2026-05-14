<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>رحلة العمر - زوزو</title>
    <style>
        body {
            background-color: #001f3f; /* كحلي ملكي مطفي */
            color: #FFD700; /* ذهبي ساطع */
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-align: center;
            margin: 0;
            overflow-x: hidden;
        }
        .container { padding: 50px 20px; }
        .level {
            margin-bottom: 80px;
            cursor: pointer;
            animation: fadeIn 1.5s ease-in;
        }
        .icon {
            font-size: 70px;
            text-shadow: 0 0 15px #FFD700;
            margin-bottom: 10px;
            transition: 0.3s;
        }
        .level:hover .icon { transform: scale(1.2); text-shadow: 0 0 30px #FFD700; }
        .date { font-weight: bold; font-size: 1.3em; margin-bottom: 10px; }
        .message {
            display: none;
            background: rgba(255, 215, 0, 0.05);
            border: 1px solid #FFD700;
            padding: 25px;
            border-radius: 20px;
            margin: 20px auto;
            line-height: 1.8;
            max-width: 85%;
            font-size: 1.1em;
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
        }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    </style>
</head>
<body>

<div class="container">
    <!-- المرحلة الأولى: النجمة -->
    <div class="level" onclick="showMsg('m1')">
        <div class="icon">★</div>
        <div class="date">6/3/2002</div>
        <div id="m1" class="message">
            6/3/2002 ممتنه لليوم اللي اتولدت فيه عشان بقي عندي اجمل واحن راجل في الدنيا، بحبك.
        </div>
    </div>

    <!-- المرحلة الثانية: القلب -->
    <div class="level" onclick="showMsg('m2')">
        <div class="icon">❤</div>
        <div class="date">9/9/2020</div>
        <div id="m2" class="message">
            من 9/9/2020 والقلب ده ملوش اتجاه غيرك.. أنت الاختيار اللي كل يوم بكتشف إني صح فيه، بحبك.
        </div>
    </div>

    <!-- المرحلة الثالثة: الخاتم -->
    <div class="level" onclick="showMsg('m3')">
        <div class="icon">💍</div>
        <div class="date">1/10/2025</div>
        <div id="m3" class="message">
            1/10/2025 اليوم اللي لبست فيه دبلتك وبقيت رسمي ملكك. عارفة إن الجيش وتعب الأيام دي ضغط عليك، بس رغم كل ده أنت بتثبت لي إنك الراجل الصح. ممتنة لكل تعب بتتعبه عشاننا، وفخورة بيك وبقوتك فوق ما تتخيل. بحبك.
        </div>
    </div>

    <!-- المرحلة الرابعة: البيت -->
    <div class="level" onclick="showMsg('m4')">
        <div class="icon">🏠</div>
        <div class="date">المستقبل القريب</div>
        <div id="m4" class="message">
            السنة دي بنحتفل وإحنا بنعد الأيام، والسنة الجاية بإذن الله هنحتفل في بيتنا.. بحبك يا أغلى بطل.
        </div>
    </div>
</div>

<script>
    function showMsg(id) {
        var allMsgs = document.getElementsByClassName('message');
        for (var i = 0; i < allMsgs.length; i++) {
            if (allMsgs[i].id !== id) allMsgs[i].style.display = 'none';
        }
        var msg = document.getElementById(id);
        msg.style.display = (msg.style.display === 'block') ? 'none' : 'block';
        msg.scrollIntoView({ behavior: 'smooth', block: 'center' });
    }
</script>

</body>
</html>
