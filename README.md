
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="LIFE SHIFT - あなたの人生を変える瞬間。プロフェッショナルなライフコンサルティングサービス">
    <title>LIFE SHIFT - あなたの人生を変える瞬間</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300;400;700&family=Poppins:wght@300;400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary-color: #1a237e;
            --secondary-color: #3f51b5;
            --accent-color: #ff4081;
            --background-color: #f5f5f5;
            --text-color: #212121;
            --light-text-color: #ffffff;
            --dark-background-color: #121212;
            --dark-text-color: #e0e0e0;
        }

        @media (prefers-color-scheme: dark) {
            :root {
                --background-color: var(--dark-background-color);
                --text-color: var(--dark-text-color);
            }
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Noto Sans JP', sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.6;
            font-size: 16px;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        nav {
            background-color: rgba(255, 255, 255, 0.95);
            position: fixed;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        nav ul {
            display: flex;
            justify-content: flex-end;
            list-style-type: none;
            padding: 20px 0;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: bold;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: var(--accent-color);
        }

        header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: var(--light-text-color);
            padding: 150px 0 100px;
            text-align: center;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
        }

        h1, h2, h3 {
            font-family: 'Poppins', sans-serif;
            line-height: 1.2;
        }

        h1 {
            font-size: clamp(2.5em, 5vw, 4em);
            margin-bottom: 20px;
            letter-spacing: 2px;
        }

        .subtitle {
            font-size: clamp(1.2em, 3vw, 1.5em);
            font-weight: 300;
            margin-bottom: 40px;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--accent-color);
            color: var(--light-text-color);
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .cta-button:hover {
            background-color: #f50057;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        .section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            font-size: clamp(2em, 4vw, 2.5em);
            margin-bottom: 50px;
            color: var(--primary-color);
        }

        .benefit-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .benefit-item {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            text-align: center;
        }

        .benefit-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }

        .benefit-item i {
            font-size: 3em;
            color: var(--secondary-color);
            margin-bottom: 20px;
        }

        .testimonial-section {
            background: linear-gradient(135deg, var(--secondary-color), var(--primary-color));
            color: var(--light-text-color);
            padding: 100px 0;
            clip-path: polygon(0 15%, 100% 0, 100% 85%, 0 100%);
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .testimonial {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }

        .consultant-profile {
            display: flex;
            align-items: center;
            margin-bottom: 30px;
        }

        .consultant-image {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            margin-right: 20px;
            object-fit: cover;
        }

        #contact {
            background-color: white;
        }

        form {
            display: grid;
            gap: 20px;
            max-width: 600px;
            margin: 0 auto;
        }

        input, textarea {
            width: 100%;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }

        textarea {
            height: 150px;
        }

        footer {
            background-color: var(--primary-color);
            color: var(--light-text-color);
            text-align: center;
            padding: 20px 0;
        }

        @media (max-width: 768px) {
            .section {
                padding: 60px 0;
            }

            .benefit-grid, .testimonial-grid {
                grid-template-columns: 1fr;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
            }

            nav ul li {
                margin: 10px 0;
            }
        }

        .parallax {
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
        }

        .cookie-consent {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
            padding: 15px;
            text-align: center;
            z-index: 9999;
        }

        .cookie-consent button {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 10px 20px;
            margin-left: 10px;
            cursor: pointer;
        }

        .visually-hidden {
            position: absolute;
            width: 1px;
            height: 1px;
            padding: 0;
            margin: -1px;
            overflow: hidden;
            clip: rect(0, 0, 0, 0);
            white-space: nowrap;
            border: 0;
        }
    </style>
</head>
<body>
    <nav>
        <div class="container">
            <ul>
                <li><a href="#intro">ホーム</a></li>
                <li><a href="#benefits">特徴</a></li>
                <li><a href="#testimonials">成功事例</a></li>
                <li><a href="#consultants">コンサルタント</a></li>
                <li><a href="#contact">お問い合わせ</a></li>
            </ul>
        </div>
    </nav>

    <header class="parallax">
        <div class="container">
            <h1>LIFE SHIFT</h1>
            <p class="subtitle">あなたの人生を変える瞬間</p>
            <a href="#contact" class="cta-button">無料相談を予約する</a>
        </div>
    </header>

    <main>
        <section class="section" id="intro">
            <div class="container">
                <h2 class="section-title">人生を変える、それは今</h2>
                <p>LIFE SHIFTは、あなたの潜在能力を最大限に引き出し、夢を現実にするためのプレミアムコンサルティングサービスです。経験豊富な専門家があなたの側に立ち、人生の転換点を共に作り上げます。</p>
            </div>
        </section>

        <section class="section" id="benefits">
            <div class="container">
                <h2 class="section-title">あなたの人生にもたらす価値</h2>
                <div class="benefit-grid">
                    <div class="benefit-item">
                        <i class="fas fa-bullseye" aria-hidden="true"></i>
                        <h3>明確なビジョン</h3>
                        <p>あなたの真の目標を見出し、それを達成するための具体的な道筋を描きます。</p>
                    </div>
                    <div class="benefit-item">
                        <i class="fas fa-rocket" aria-hidden="true"></i>
                        <h3>生産性の飛躍的向上</h3>
                        <p>時間管理と集中力強化のテクニックを習得し、効率的に目標達成を目指します。</p>
                    </div>
                    <div class="benefit-item">
                        <i class="fas fa-crown" aria-hidden="true"></i>
                        <h3>自信とリーダーシップ</h3>
                        <p>自己肯定感を高め、周囲に好影響を与えるリーダーシップスキルを培います。</p>
                    </div>
                    <div class="benefit-item">
                        <i class="fas fa-balance-scale" aria-hidden="true"></i>
                        <h3>ワークライフバランス</h3>
                        <p>キャリアの成功と充実したプライベートライフの両立を実現します。</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="section testimonial-section parallax" id="testimonials">
            <div class="container">
                <h2 class="section-title">成功事例</h2>
                <div class="testimonial-grid">
                    <div class="testimonial">
                        <p>"LIFE SHIFTのコンサルティングを受けて、私の人生は180度変わりました。起業への不安が自信に変わり、今では自分の会社を経営しています。"</p>
                        <p><strong>田中 健太郎</strong> - 32歳、起業家</p>
                    </div>
                    <div class="testimonial">
                        <p>"キャリアの停滞感に悩んでいましたが、LIFE SHIFTのサポートで新たな可能性を見出すことができました。今は、より充実した毎日を送っています。"</p>
                        <p><strong>鈴木 美香</strong> - 28歳、マーケティング専門家</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="section" id="consultants">
            <div class="container">
                <h2 class="section-title">あなたを成功に導くエキスパート</h2>
                <div class="consultant-profile">
                    <img src="consultant1.jpg" alt="佐藤 美咲" class="consultant-image" loading="lazy">
                    <div>
                        <h3>佐藤 美咲</h3>
                        <p>キャリアコンサルタント。Fortune 500企業でのHR経験を活かし、クライアントのキャリア戦略を支援。</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="section" id="contact">
            <div class="container">
                <h2 class="section-title">人生の変革は、ここから始まる</h2>
                <form id="contact-form">
                    <label for="name" class="visually-hidden">お名前</label>
                    <input type="text" id="name" name="name" placeholder="お名前" required>
                    <label for="email" class="visually-hidden">メールアドレス</label>
                    <input type="email" id="email" name<img width="160" alt="スクリーンショット 2024-06-24 4 13 12" src="https://github.com/Yuuuuuuuki712/Togeggee/assets/173628829/c74da858-562c-41b8-a0f3-168b7335f05c">
