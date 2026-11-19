<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio | Adisak Phuangphum</title>
    <!-- นำเข้าฟอนต์ภาษาไทยสวยๆ จาก Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Prompt:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-dark: #090d16;
            --card-bg: rgba(255, 255, 255, 0.05);
            --card-border: rgba(255, 255, 255, 0.12);
            --neon-blue: #00f2fe;
            --neon-purple: #4facfe;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Prompt', sans-serif;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }

        /* วงกลมแสงเรืองรองด้านหลัง (Background Glow) */
        .glow-circle-1 {
            position: fixed;
            top: -100px;
            left: -100px;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(79, 172, 254, 0.25) 0%, rgba(0,0,0,0) 70%);
            border-radius: 50%;
            z-index: -1;
            animation: float 8s ease-in-out infinite;
        }

        .glow-circle-2 {
            position: fixed;
            bottom: -150px;
            right: -100px;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(0, 242, 254, 0.2) 0%, rgba(0,0,0,0) 70%);
            border-radius: 50%;
            z-index: -1;
            animation: float 10s ease-in-out infinite reverse;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(30px); }
        }

        /* แถบเมนูด้านบน (Navbar) */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1000px;
            margin: 0 auto;
            padding: 25px 20px;
        }

        .logo {
            font-size: 1.4rem;
            font-weight: 700;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 1px;
        }

        .nav-status {
            background: rgba(16, 185, 129, 0.15);
            color: #34d399;
            border: 1px solid rgba(52, 211, 153, 0.3);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.85rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .dot {
            width: 8px;
            height: 8px;
            background-color: #34d399;
            border-radius: 50%;
            box-shadow: 0 0 8px #34d399;
        }

        /* ส่วนต้อนรับ (Hero Section) */
        .hero {
            text-align: center;
            padding: 50px 20px 40px;
            max-width: 800px;
            margin: 0 auto;
        }

        .avatar-ring {
            width: 120px;
            height: 120px;
            margin: 0 auto 20px;
            border-radius: 50%;
            padding: 4px;
            background: linear-gradient(135deg, var(--neon-blue), #a855f7);
            box-shadow: 0 0 25px rgba(0, 242, 254, 0.4);
        }

        .avatar-inner {
            width: 100%;
            height: 100%;
            background-color: #1e293b;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--neon-blue);
        }

        .hero h1 {
            font-size: 2.8rem;
            font-weight: 700;
            margin-bottom: 10px;
            letter-spacing: -0.5px;
        }

        .typing-box {
            font-size: 1.2rem;
            color: var(--neon-blue);
            min-height: 32px;
            margin-bottom: 20px;
            font-weight: 400;
        }

        .hero p {
            color: var(--text-muted);
            max-width: 600px;
            margin: 0 auto 30px;
            font-size: 1rem;
        }

        /* ปุ่มกดเรืองแสง */
        .btn-group {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn-primary {
            background: linear-gradient(90deg, var(--neon-purple), var(--neon-blue));
            color: #090d16;
            text-decoration: none;
            padding: 12px 28px;
            border-radius: 30px;
            font-weight: 700;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 0 20px rgba(0, 242, 254, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 30px rgba(0, 242, 254, 0.6);
        }

        .btn-outline {
            background: transparent;
            color: var(--text-main);
            border: 1px solid var(--card-border);
            text-decoration: none;
            padding: 12px 28px;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s;
        }

        .btn-outline:hover {
            border-color: var(--neon-blue);
            background: rgba(0, 242, 254, 0.1);
        }

        /* กล่องเนื้อหาแบบ Glassmorphism */
        .container {
            max-width: 1000px;
            margin: 20px auto 60px;
            padding: 0 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }

        .glass-card {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-radius: 16px;
            padding: 30px;
            transition: transform 0.3s, border-color 0.3s;
        }

        .glass-card:hover {
            transform: translateY(-6px);
            border-color: rgba(0, 242, 254, 0.5);
        }

        .card-icon {
            font-size: 2rem;
            margin-bottom: 15px;
        }

        .glass-card h3 {
            font-size: 1.3rem;
            margin-bottom: 12px;
            color: #fff;
        }

        .glass-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            line-height: 1.7;
        }

        /* แถบป้ายทักษะ */
        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
        }

        .tag {
            background: rgba(79, 172, 254, 0.15);
            color: var(--neon-blue);
            border: 1px solid rgba(79, 172, 254, 0.3);
            padding: 5px 12px;
            border-radius: 8px;
            font-size: 0.85rem;
        }

        footer {
            text-align: center;
            padding: 30px 20px;
            border-top: 1px solid var(--card-border);
            color: var(--text-muted);
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <div class="glow-circle-1"></div>
    <div class="glow-circle-2"></div>

    <!-- แถบด้านบน -->
    <nav>
        <div class="logo">&lt;ADISAK.DEV /&gt;</div>
        <div class="nav-status">
            <span class="dot"></span> พร้อมเรียนรู้ DevOps
        </div>
    </nav>

    <!-- ส่วนหัวต้อนรับ -->
    <section class="hero">
        <div class="avatar-ring">
            <div class="avatar-inner">AP</div>
        </div>
        <h1>Adisak Phuangphum</h1>
        <div class="typing-box" id="typing-text"></div>
        <p>นักศึกษาสาขาวิชาเทคโนโลยีสารสนเทศ ปวช.3 วิทยาลัยเทคนิคนางรอง มุ่งมั่นพัฒนาทักษะด้านการเขียนโปรแกรม การทำงานร่วมกันเป็นทีมด้วย Git & GitHub และเทคโนโลยีคลาวด์</p>
        
        <div class="btn-group">
            <a href="https://github.com/app339969-lgtm" target="_blank" class="btn-primary">🚀 ดูผลงานบน GitHub</a>
            <a href="https://github.com/app339969-lgtm/hello-devops" target="_blank" class="btn-outline">📂 โปรเจกต์ hello-devops</a>
        </div>
    </section>

    <!-- การ์ด 3 คอลัมน์ -->
    <div class="container">
        <div class="glass-card">
            <div class="card-icon">💻</div>
            <h3>การพัฒนาเว็บไซต์</h3>
            <p>ออกแบบและสร้างโครงสร้างหน้าเว็บไซต์สมัยใหม่ด้วย HTML5 และ CSS3 พร้อมปรับแต่งให้รองรับการแสดงผลทุกหน้าจอ</p>
            <div class="tags">
                <span class="tag">HTML5</span>
                <span class="tag">CSS3</span>
                <span class="tag">Responsive</span>
            </div>
        </div>

        <div class="glass-card">
            <div class="card-icon">🔄</div>
            <h3>แนวคิด DevOps</h3>
            <p>เรียนรู้กระบวนการทำงานร่วมกันระหว่างทีมพัฒนาและทีมดูแลระบบ เพื่อส่งมอบซอฟต์แวร์ได้รวดเร็วและมีคุณภาพสูง</p>
            <div class="tags">
                <span class="tag">Git</span>
                <span class="tag">GitHub</span>
                <span class="tag">Teamwork</span>
            </div>
        </div>

        <div class="glass-card">
            <div class="card-icon">🎯</div>
            <h3>เป้าหมายในรายวิชา</h3>
            <p>สามารถใช้งานระบบควบคุมเวอร์ชันได้อย่างคล่องแคล่ว จัดการโค้ดร่วมกับเพื่อนในทีมได้โดยไม่ทับกัน และสร้างโปรเจกต์จริงได้สำเร็จ</p>
            <div class="tags">
                <span class="tag">21901-2012</span>
                <span class="tag">ปวช.3 IT</span>
            </div>
        </div>
    </div>

    <footer>
        <p>ออกแบบและพัฒนาโดย <strong>Adisak Phuangphum</strong> | รายวิชาการพัฒนาระบบร่วมกันด้วยแพลตฟอร์ม (2026)</p>
    </footer>

    <!-- สคริปต์สร้างเอฟเฟกต์พิมพ์ข้อความอัตโนมัติ -->
    <script>
        const texts = [
            "IT Student @ NRTECH",
            "DevOps & GitHub Beginner",
            "Web Developer in Training"
        ];
        let count = 0;
        let index = 0;
        let currentText = "";
        let letter = "";

        (function type() {
            if (count === texts.length) {
                count = 0;
            }
            currentText = texts[count];
            letter = currentText.slice(0, ++index);

            document.getElementById("typing-text").textContent = letter + "|";
            if (letter.length === currentText.length) {
                setTimeout(() => {
                    count++;
                    index = 0;
                    type();
                }, 2000);
            } else {
                setTimeout(type, 100);
            }
        })();
    </script>

</body>
</html>
อันนี้เวอร์ชั่นใหม่นะ
