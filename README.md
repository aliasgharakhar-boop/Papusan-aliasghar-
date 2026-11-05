# Papusan-aliasghar-
Official web application for Heyat Pabousan Hazrat Ali Asghar - Weekly Noha &amp; Posters
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>هیئت پابوسان حضرت علی اصغر</title>
    <style>
        /* ایمپورت فونت زیبای فارسی */
        @import url('https://fonts.googleapis.com/css2?family=Vazirmatn:wght@400;700;900&display=swap');

        /* متغیرهای رنگ برای تغییر تم (سفید / سیاه) */
        :root {
            --bg-color: #ffffff;
            --text-color: #1a1a1a;
            --card-bg: #f8f9fa;
            --gold-color: #d4af37; /* رنگ طلایی هماهنگ با لوگو */
            --border-color: #e0e0e0;
        }

        /* تم تاریک (مشکی) */
        body.dark-mode {
            --bg-color: #0d0d0d;
            --text-color: #f0f0f0;
            --card-bg: #1a1a1a;
            --gold-color: #e6c200; /* طلایی روشن‌تر برای پس‌زمینه تیره */
            --border-color: #333333;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Vazirmatn', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            transition: background-color 0.3s, color 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        /* هدر برنامه (لوگو و اسم) */
        .header {
            text-align: center;
            margin-bottom: 30px;
            width: 100%;
            max-width: 500px;
        }

        .logo {
            width: 180px;
            height: auto;
            border-radius: 15px;
            margin-bottom: 15px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .header h1 {
            font-size: 22px;
            color: var(--gold-color);
            margin-bottom: 5px;
        }

        /* بخش جمله امام حسین (ع) */
        .quote-box {
            background-color: var(--card-bg);
            border: 2px dashed var(--gold-color);
            border-radius: 15px;
            padding: 25px 20px;
            text-align: center;
            width: 100%;
            max-width: 500px;
            margin-bottom: 40px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
        }

        .quote-box p {
            font-size: 20px;
            font-weight: 700;
            line-height: 1.6;
            color: var(--text-color);
        }

        .quote-box span {
            display: block;
            font-size: 14px;
            color: var(--gold-color);
            margin-top: 10px;
            font-weight: 400;
        }

        /* دکمه‌های منو */
        .menu {
            display: flex;
            flex-direction: column;
            gap: 15px;
            width: 100%;
            max-width: 500px;
        }

        .menu-btn {
            background-color: var(--card-bg);
            color: var(--text-color);
            border: 1px solid var(--border-color);
            padding: 18px;
            border-radius: 12px;
            font-size: 18px;
            font-family: 'Vazirmatn', sans-serif;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.2s;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }

        .menu-btn:hover {
            border-color: var(--gold-color);
            transform: translateY(-2px);
        }

        .menu-btn .icon {
            font-size: 24px;
        }

        /* دکمه تغییر تم */
        .theme-toggle {
            position: fixed;
            top: 20px;
            left: 20px;
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            color: var(--text-color);
            width: 45px;
            height: 45px;
            border-radius: 50%;
            cursor: pointer;
            font-size: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            z-index: 100;
        }

        /* تنظیمات برای گوشی‌های کوچک */
        @media (max-width: 400px) {
            .header h1 { font-size: 18px; }
            .quote-box p { font-size: 16px; }
            .menu-btn { font-size: 16px; padding: 15px; }
        }
    </style>
</head>
<body>

    <!-- دکمه تغییر تم (سفید/مشکی) -->
    <button class="theme-toggle" onclick="toggleTheme()" id="themeBtn" title="تغییر حالت شب و روز">
        🌙
    </button>

    <!-- بخش هدر (لوگو و نام هیئت) -->
    <div class="header">
        <!-- توجه: عکسی که فرستادی را در کنار این فایل با نام logo.jpg ذخیره کن -->
        <img src="logo.jpg" alt="لوگوی هیئت پابوسان حضرت علی اصغر" class="logo">
        <h1>هیئت پابوسان حضرت علی اصغر</h1>
    </div>

    <!-- بخش جمله امام حسین (ع) -->
    <div class="quote-box">
        <p>«امام حسین دلیل آرامش دل هاست»</p>
        <span>التماس دعا</span>
    </div>

    <!-- دکمه‌های برنامه -->
    <div class="menu">
        <button class="menu-btn" onclick="alert('بخش نوحه‌های هفتگی به زودی...')">
            <span>🎵 نوحه‌های هفتگی</span>
            <span class="icon">➔</span>
        </button>
        
        <button class="menu-btn" onclick="alert('بخش پوسترهای هفتگی به زودی...')">
            <span>🖼️ پوسترهای هفتگی</span>
            <span class="icon">➔</span>
        </button>

        <button class="menu-btn" onclick="alert('بخش اشتراک ماهانه به زودی...')">
            <span>💳 اشتراک ماهانه</span>
            <span class="icon">➔</span>
        </button>

        <button class="menu-btn" onclick="alert('تنظیمات برنامه...')">
            <span>⚙️ تنظیمات</span>
            <span class="icon">➔</span>
        </button>
    </div>

    <!-- کدهای جاوا اسکریپت برای تغییر تم -->
    <script>
        const body = document.body;
        const themeBtn = document.getElementById('themeBtn');

        // بررسی اینکه آیا کاربر قبلاً تمی انتخاب کرده است یا خیر
        const currentTheme = localStorage.getItem('theme');
        if (currentTheme === 'dark') {
            body.classList.add('dark-mode');
            themeBtn.innerHTML = '☀️';
        }

        function toggleTheme() {
            body.classList.toggle('dark-mode');
            
            if (body.classList.contains('dark-mode')) {
                themeBtn.innerHTML = '☀️'; // اگر شب بود، خورشید نشان بده
                localStorage.setItem('theme', 'dark');
            } else {
                themeBtn.innerHTML = '🌙'; // اگر روز بود، ماه نشان بده
                localStorage.setItem('theme', 'light');
            }
        }
    </script>

</body>
</html>
