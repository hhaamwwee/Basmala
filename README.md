# Basmala
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="keyword" content="abdullha&basmala">
    <title>مكاننا الخاص ❤️</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #fce4ec;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
        }

        /* تنسيق صندوق كلمة السر */
        #login-screen {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            text-align: center;
            z-index: 10;
        }

        input {
            padding: 10px;
            border: 2px solid #f06292;
            border-radius: 10px;
            outline: none;
            width: 80%;
            margin-bottom: 15px;
            text-align: center;
        }

        button {
            background-color: #f06292;
            color: white;
            border: none;
            padding: 10px 25px;
            border-radius: 10px;
            cursor: pointer;
            transition: 0.3s;
        }

        button:hover { background-color: #d81b60; }

        /* تنسيق المحتوى السري (مخفي في البداية) */
        #secret-content {
            display: none;
            text-align: center;
            animation: fadeIn 1.5s;
        }

        h1 { color: #d81b60; }
        .heart { color: red; font-size: 50px; animation: beat 1s infinite; }

        @keyframes beat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
</head>
<body>

    <div id="login-screen">
        <h3>أدخل كلمة السر لفتح ذكرياتنا ❤️</h3>
        <input type="password" id="passInput" placeholder="اكتب الكلمة هنا...">
        <br>
        <button onclick="checkPass()">دخول</button>
        <p id="error" style="color: red; display: none; margin-top: 10px;">كلمة السر غلط يا جميل! حاول تاني.</p>
    </div>

    <div id="secret-content">
        <div class="heart">❤️</div>
        <h1>كل سنة وأنتِ طيبة!</h1>
        <p>هنا ممكن تحط صوركم، رسايلكم، أو أي فيديو خاص بيكم.</p>
        <img src="https://via.placeholder.com/300" alt="صورة لينا" style="border-radius: 15px; max-width: 90%;">
    </div>

    <script>
        function checkPass() {
            const pass = document.getElementById('passInput').value;
            // غير كلمة '1234' لأي كلمة سر تحبها
            if (pass === "1234") {
                document.getElementById('login-screen').style.display = 'none';
                document.getElementById('secret-content').style.display = 'block';
                document.body.style.backgroundColor = "#fff0f3";
            } else {
                document.getElementById('error').style.display = 'block';
            }
        }
    </script>
</body>
</html>
