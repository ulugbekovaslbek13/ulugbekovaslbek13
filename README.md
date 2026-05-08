<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ulug'bekovvv_3 | Professional Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500&family=Plus+Jakarta+Sans:wght@400;500;700;800&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-main: #0b0f17;
            --bg-card: rgba(17, 24, 39, 0.7);
            --border-neon: rgba(56, 189, 248, 0.2);
            --primary: #38bdf8;
            --green-neon: #10b981;
            --purple-neon: #a855f7;
            --text-main: #f3f4f6;
            --text-dim: #9ca3af;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        body {
            background-color: var(--bg-main);
            color: var(--text-main);
            min-height: 100vh;
            padding: 40px 5%;
            overflow-x: hidden;
            background-image: radial-gradient(circle at 10% 20%, rgba(56, 189, 248, 0.05) 0%, transparent 40%),
                              radial-gradient(circle at 90% 80%, rgba(168, 85, 247, 0.05) 0%, transparent 40%);
        }

        /* HEADER */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 40px;
            padding-bottom: 20px;
            border-bottom: 1px solid var(--border-neon);
        }
        .header-logo {
            font-size: 24px;
            font-weight: 800;
            letter-spacing: 2px;
            color: var(--text-main);
        }
        .header-logo span { color: var(--primary); }

        /* PORTFOLIO GRID STRUKTURASI */
        .portfolio-container {
            display: grid;
            grid-template-columns: 1.1fr 1.9fr;
            gap: 30px;
            max-width: 1500px;
            margin: 0 auto;
        }

        /* CARD STYLE */
        .glass-card {
            background: var(--bg-card);
            border: 1px solid var(--border-neon);
            border-radius: 24px;
            padding: 30px;
            backdrop-filter: blur(12px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            transition: all 0.3s ease;
        }
        .glass-card:hover {
            border-color: rgba(56, 189, 248, 0.4);
            box-shadow: 0 15px 35px rgba(56, 189, 248, 0.08);
        }

        /* LEFT COLUMN */
        .left-column {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        /* PROFILE CARD */
        .profile-card {
            text-align: center;
            position: relative;
        }
        .profile-img-container {
            position: relative;
            width: 180px;
            height: 180px;
            margin: 0 auto 20px;
        }
        .profile-img-container img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--primary);
            box-shadow: 0 0 30px rgba(56, 189, 248, 0.3);
        }
        .status-dot {
            width: 18px;
            height: 18px;
            background-color: var(--green-neon);
            border-radius: 50%;
            position: absolute;
            bottom: 12px;
            right: 12px;
            border: 3px solid #0b0f17;
            box-shadow: 0 0 10px var(--green-neon);
        }
        .profile-card h2 {
            font-size: 28px;
            font-weight: 800;
            margin-bottom: 5px;
            letter-spacing: 1px;
        }
        .profile-card h2 span { color: var(--primary); }
        .profile-subtitle {
            color: var(--text-dim);
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 20px;
        }
        .profile-badge-list {
            display: flex;
            flex-direction: column;
            gap: 12px;
            text-align: left;
            margin-top: 15px;
        }
        .badge-item {
            display: flex;
            align-items: center;
            gap: 12px;
            background: rgba(255, 255, 255, 0.03);
            padding: 12px 18px;
            border-radius: 12px;
            border-left: 3px solid var(--primary);
        }
        .badge-item i {
            font-size: 18px;
            color: var(--primary);
        }
        .badge-item span {
            font-size: 14px;
            font-weight: 600;
        }

        /* REPOSITORIES SECTION */
        .repos-section h3 {
            font-size: 20px;
            margin-bottom: 20px;
            border-left: 4px solid var(--primary);
            padding-left: 10px;
        }
        .repo-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        .repo-card {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 16px;
            transition: 0.3s;
            text-decoration: none;
            color: white;
        }
        .repo-card:hover {
            border-color: var(--primary);
            background: rgba(56, 189, 248, 0.05);
            transform: translateX(5px);
        }
        .repo-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 8px;
        }
        .repo-title {
            font-weight: 700;
            font-size: 16px;
            color: var(--text-main);
        }
        .repo-stats {
            display: flex;
            gap: 12px;
            font-size: 12px;
            color: var(--text-dim);
        }
        .repo-tags {
            display: flex;
            gap: 8px;
            margin-top: 10px;
        }
        .tag {
            font-size: 11px;
            padding: 3px 8px;
            border-radius: 6px;
            font-weight: bold;
        }
        .tag.java { background: rgba(239, 68, 68, 0.15); color: #ef4444; }
        .tag.js { background: rgba(245, 158, 11, 0.15); color: #f59e0b; }
        .tag.python { background: rgba(59, 130, 246, 0.15); color: #3b82f6; }

        /* RIGHT COLUMN */
        .right-column {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        /* HEADER BANNER */
        .hero-banner {
            background: linear-gradient(135deg, rgba(56, 189, 248, 0.1) 0%, rgba(168, 85, 247, 0.1) 100%);
            border: 1px solid rgba(168, 85, 247, 0.2);
            padding: 25px;
            border-radius: 20px;
            text-align: center;
        }
        .hero-banner p {
            font-size: 15px;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 5px;
        }
        .hero-banner h3 {
            font-size: 22px;
            font-weight: 800;
            background: linear-gradient(to right, var(--primary), var(--purple-neon));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* GITHUB STATS CHART */
        .stats-header-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }
        .stats-title {
            font-size: 20px;
            font-weight: 700;
        }
        .stats-number {
            font-size: 32px;
            font-weight: 900;
            color: var(--green-neon);
            text-shadow: 0 0 15px rgba(16, 185, 129, 0.4);
        }
        .stats-number span {
            font-size: 14px;
            color: var(--text-dim);
            font-weight: normal;
            display: block;
        }

        /* CHART GRAPHIC Placeholder */
        .mock-chart {
            height: 180px;
            width: 100%;
            position: relative;
            margin-bottom: 25px;
            border-bottom: 2px solid rgba(255, 255, 255, 0.1);
        }
        .chart-svg {
            width: 100%;
            height: 100%;
        }

        /* GITHUB CONTRIBUTION GRID */
        .contrib-title {
            font-size: 16px;
            color: var(--text-dim);
            margin-bottom: 12px;
        }
        .contrib-grid {
            display: grid;
            grid-template-columns: repeat(28, 1fr);
            gap: 4px;
        }
        .contrib-box {
            aspect-ratio: 1;
            border-radius: 3px;
            background: rgba(255, 255, 255, 0.05);
        }
        .contrib-box.lvl-1 { background-color: #0e4429; }
        .contrib-box.lvl-2 { background-color: #006d32; }
        .contrib-box.lvl-3 { background-color: #26a641; }
        .contrib-box.lvl-4 { background-color: #39d353; }

        /* TERMINAL / CODE DEMO */
        .terminal-card {
            background: #05070c;
            border: 1px solid rgba(168, 85, 247, 0.3);
            border-radius: 20px;
            padding: 25px;
            font-family: 'Fira Code', monospace;
            box-shadow: 0 10px 40px rgba(168, 85, 247, 0.05);
        }
        .terminal-header {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 20px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            padding-bottom: 12px;
        }
        .term-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        .term-dot.red { background-color: #ef4444; }
        .term-dot.yellow { background-color: #f59e0b; }
        .term-dot.green { background-color: #10b981; }
        .terminal-header span {
            margin-left: 10px;
            font-size: 13px;
            color: var(--text-dim);
        }
        .code-line {
            font-size: 14px;
            line-height: 1.8;
            color: #a78bfa;
        }
        .code-line span.keyword { color: #f472b6; }
        .code-line span.type { color: #60a5fa; }
        .code-line span.string { color: #34d399; }
        .code-line span.comment { color: #6b7280; }

        /* CONTACTS & QR GRID */
        .contacts-wrapper {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        .qr-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }
        .qr-card {
            background: rgba(255, 255, 255, 0.01);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 20px;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
            transition: 0.3s;
        }
        .qr-card.telegram:hover { border-color: var(--primary); box-shadow: 0 0 20px rgba(56, 189, 248, 0.15); }
        .qr-card.instagram:hover { border-color: var(--purple-neon); box-shadow: 0 0 20px rgba(168, 85, 247, 0.15); }
        .qr-card.gmail:hover { border-color: var(--green-neon); box-shadow: 0 0 20px rgba(16, 185, 129, 0.15); }

        .qr-placeholder {
            width: 110px;
            height: 110px;
            background: #fff;
            padding: 5px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .qr-placeholder img {
            width: 100%;
            height: 100%;
        }
        .qr-btn {
            padding: 8px 16px;
            border-radius: 10px;
            font-size: 12px;
            font-weight: bold;
            text-decoration: none;
            color: white;
            width: 100%;
        }
        .qr-btn.telegram { background: linear-gradient(135deg, #0088cc 0%, #38bdf8 100%); }
        .qr-btn.instagram { background: linear-gradient(135deg, #f09433 0%, #bc1888 100%); }
        .qr-btn.gmail { background: linear-gradient(135deg, #10b981 0%, #059669 100%); }

        @media (max-width: 1024px) {
            .portfolio-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-logo">ASLBEK<span>.DEV</span></div>
    </header>

    <main class="portfolio-container">
        
        <div class="left-column">
            
            <div class="glass-card profile-card">
                <div class="profile-img-container">
                    <img src="img/foto.jpg" alt="Aslbek">
                    <div class="status-dot"></div>
                </div>
                <h2>ULUG'BEKOVVV_3</h2>
                <p class="profile-subtitle">Full-Stack Developer</p>
                
                <div class="profile-badge-list">
                    <div class="badge-item">
                        <i class="fas fa-graduation-cap"></i>
                        <span>IT Park Al-Xorazmiy Loyihasi</span>
                    </div>
                    <div class="badge-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <span>Xorazm, Xonqa, O'zbekiston</span>
                    </div>
                    <div class="badge-item">
                        <i class="fas fa-code-branch"></i>
                        <span>7-sinf o'quvchisi</span>
                    </div>
                </div>
            </div>

            <div class="glass-card repos-section">
                <h3>Popular Repositories</h3>
                <div class="repo-list">
                    <a href="https://github.com/tojibayevlutfulla-rgb" target="_blank" class="repo-card">
                        <div class="repo-header">
                            <span class="repo-title">ALGORITM PRO</span>
                            <div class="repo-stats">
                                <span><i class="fas fa-star"></i> 49.5k</span>
                                <span><i class="fas fa-code-branch"></i> 582</span>
                            </div>
                        </div>
                        <div class="repo-tags">
                            <span class="tag java">Java</span>
                            <span class="tag js">JS</span>
                            <span class="tag python">Python</span>
                        </div>
                    </a>
                    <a href="https://github.com/tojibayevlutfulla-rgb" target="_blank" class="repo-card">
                        <div class="repo-header">
                            <span class="repo-title">JAVA BACKEND FRAMEWORK</span>
                            <div class="repo-stats">
                                <span><i class="fas fa-star"></i> 73.6k</span>
                                <span><i class="fas fa-code-branch"></i> 29</span>
                            </div>
                        </div>
                        <div class="repo-tags">
                            <span class="tag java">Java</span>
                            <span class="tag python">Python</span>
                        </div>
                    </a>
                </div>
            </div>

        </div>

        <div class="right-column">
            
            <div class="hero-banner">
                <p>BUILDING THE DIGITAL FUTURE</p>
                <h3>AL-XORAZMIY LOYIHASI BI'TIRUVCHISI | CERTIFIED JAVA DEVELOPER</h3>
            </div>

            <div class="glass-card">
                <div class="stats-header-row">
                    <div class="stats-title">My GitHub Activity</div>
                    <div class="stats-number">345+<span>COMMITS (LAST YEAR)</span></div>
                </div>
                
                <div class="mock-chart">
                    <svg class="chart-svg" viewBox="0 0 500 100" preserveAspectRatio="none">
                        <defs>
                            <linearGradient id="neonGrad" x1="0" y1="0" x2="0" y2="1">
                                <stop offset="0%" stop-color="#38bdf8" stop-opacity="0.4"/>
                                <stop offset="100%" stop-color="#38bdf8" stop-opacity="0"/>
                            </linearGradient>
                        </defs>
                        <path d="M0,80 Q50,40 100,70 T200,30 T300,50 T400,20 T500,10" fill="none" stroke="#38bdf8" stroke-width="4" filter="drop-shadow(0px 0px 8px #38bdf8)" />
                        <path d="M0,80 Q50,40 100,70 T200,30 T300,50 T400,20 T500,10 L500,100 L0,100 Z" fill="url(#neonGrad)" />
                    </svg>
                </div>

                <div class="contrib-title">Contribution Grid</div>
                <div class="contrib-grid">
                    <div class="contrib-box lvl-1"></div><div class="contrib-box lvl-3"></div><div class="contrib-box"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-4"></div><div class="contrib-box"></div><div class="contrib-box lvl-1"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-3"></div><div class="contrib-box lvl-4"></div><div class="contrib-box"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-1"></div><div class="contrib-box lvl-4"></div><div class="contrib-box"></div><div class="contrib-box lvl-3"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-4"></div><div class="contrib-box"></div><div class="contrib-box lvl-1"></div><div class="contrib-box lvl-3"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-4"></div><div class="contrib-box lvl-1"></div><div class="contrib-box"></div><div class="contrib-box lvl-3"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-4"></div>
                    <div class="contrib-box"></div><div class="contrib-box lvl-1"></div><div class="contrib-box lvl-4"></div><div class="contrib-box lvl-3"></div><div class="contrib-box"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-1"></div><div class="contrib-box lvl-3"></div><div class="contrib-box lvl-4"></div><div class="contrib-box"></div><div class="contrib-box lvl-1"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-3"></div><div class="contrib-box lvl-4"></div><div class="contrib-box"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-1"></div><div class="contrib-box lvl-4"></div><div class="contrib-box"></div><div class="contrib-box lvl-3"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-4"></div><div class="contrib-box"></div><div class="contrib-box lvl-1"></div><div class="contrib-box lvl-3"></div><div class="contrib-box lvl-2"></div><div class="contrib-box lvl-4"></div><div class="contrib-box lvl-1"></div>
                </div>
            </div>

            <div class="terminal-card">
                <div class="terminal-header">
                    <div class="term-dot red"></div>
                    <div class="term-dot yellow"></div>
                    <div class="term-dot green"></div>
                    <span>main.java - Live Coding Demo</span>
                </div>
                <div class="code-line"><span class="keyword">package</span> com.spring.boot;</div>
                <div class="code-line"><span class="keyword">public class</span> <span class="type">SpringApp</span> {</div>
                <div class="code-line">&nbsp;&nbsp;&nbsp;&nbsp;<span class="keyword">public static void</span> <span class="type">main</span>(String[] args) {</div>
                <div class="code-line">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="type">System</span>.out.println(<span class="string">"Aloqa o'rnatildi. IT Park Al-Xorazmiy!"</span>);</div>
                <div class="code-line">&nbsp;&nbsp;&nbsp;&nbsp;}</div>
                <div class="code-line">}</div>
            </div>

            <div class="contacts-wrapper">
                <div class="qr-grid">
                    <div class="qr-card telegram">
                        <div class="qr-placeholder">
                            <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://t.me/ulugbekovvv_3" alt="TG QR">
                        </div>
                        <a href="https://t.me/ulugbekovvv_3" target="_blank" class="qr-btn telegram">Telegram</a>
                    </div>
                    <div class="qr-card instagram">
                        <div class="qr-placeholder">
                            <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://instagram.com/_u1ugbekovvvx71_" alt="Insta QR">
                        </div>
                        <a href="https://instagram.com/_u1ugbekovvvx71_" target="_blank" class="qr-btn instagram">Instagram</a>
                    </div>
                    <div class="qr-card gmail">
                        <div class="qr-placeholder">
                            <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=mailto:tojibayevlutfulla@gmail.com" alt="Gmail QR">
                        </div>
                        <a href="mailto:tojibayevlutfulla@gmail.com" class="qr-btn gmail">Gmail</a>
                    </div>
                </div>
            </div>

        </div>

    </main>

</body>
</html>
