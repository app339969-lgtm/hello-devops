<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>แนะนำตัว - Adisak Phuangphum</title>
    <style>
        /* ตั้งค่าพื้นฐานและฟอนต์ */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f0f2f5;
            color: #333;
            line-height: 1.6;
        }

        /* ส่วนหัวเว็บไซต์ (Header) */
        header {
            background: linear-gradient(135deg, #1e3c72, #2a5298);
            color: white;
            text-align: center;
            padding: 50px 20px;
        }

        header h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
        }

        header p {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        /* กล่องเนื้อหาหลัก */
        .container {
            max-width: 800px;
            margin: -30px auto 30px;
            padding: 0 20px;
        }

        .card {
            background: white;
            border-radius: 12px;
            padding: 30px;
            margin-bottom: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        .card h2 {
            color: #1e3c72;
            margin-bottom: 15px;
            border-bottom: 2px solid #e0e6ed;
            padding-bottom: 8px;
        }

        /* รายการทักษะ/สิ่งที่สนใจ */
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .badge {
            background-color: #e3f2fd;
            color: #1565c0;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: bold;
        }

        /* ปุ่มลิงก์ไป GitHub */
        .btn {
            display: inline-block;
            background-color: #24292e;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 6px;
            margin-top: 15px;
            font-weight: bold;
            transition: background 0.3s;
        }

        .btn:hover {
            background-color: #444d56;
        }

        /* ส่วนท้ายเว็บไซต์ (Footer) */
        footer {
            text-align: center;
            padding: 20px;
            color: #666;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <header>
        <h1>Adisak Phuangphum</h1>
        <p>นักศึกษาสาขาวิชาเทคโนโลยีสารสนเทศ ปวช.3 | วิทยาลัยเทคนิคนางรอง</p>
    </header>

    <div class="container">
        <div class="card">
            <h2>เกี่ยวกับฉัน (About Me)</h2>
            <p>สวัสดีครับ ยินดีต้อนรับเข้าสู่หน้าเว็บไซต์ส่วนตัวของผม หน้านี้สร้างขึ้นเพื่อฝึกปฏิบัติการพัฒนาเว็บไซต์และการทำงานร่วมกันตามแนวคิด DevOps ครับ</p>
            <a href="https://github.com/app339969-lgtm" target="_blank" class="btn">เยี่ยมชม GitHub ของฉัน</a>
        </div>

        <div class="card">
            <h2>สิ่งที่กำลังเรียนรู้ (Learning)</h2>
            <div class="skills">
                <span class="badge">HTML & CSS</span>
                <span class="badge">Git & GitHub</span>
                <span class="badge">DevOps Concept</span>
                <span class="badge">Web Development</span>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 Adisak Phuangphum. สร้างด้วย HTML5 & CSS3</p>
    </footer>

</body>
</html>
อันนี้คือโค้ดใหม่นะครับ
