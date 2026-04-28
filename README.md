<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Ghizlane Elouakili · software universe</title>
    <!-- Google Fonts: Luxurious Cinematic Blend -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600&family=Cormorant+Garamond:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0A0908;
            font-family: 'Inter', sans-serif;
            color: #E2DDD4;
            line-height: 1.5;
            padding: 2rem 1.5rem;
        }

        /* refined container – cinematic breath */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            background: rgba(13, 12, 10, 0.65);
            backdrop-filter: blur(2px);
            border-radius: 48px;
            padding: 2rem 2rem 2.5rem;
            box-shadow: 0 25px 45px -12px rgba(0,0,0,0.6), inset 0 1px 0 rgba(255,255,255,0.02);
            border: 0.5px solid rgba(196, 167, 160, 0.2);
        }

        /* typography luxury */
        h1, h2, h3, .serif {
            font-family: 'Cormorant Garamond', serif;
            font-weight: 400;
            letter-spacing: -0.01em;
        }

        h1 {
            font-size: 3.8rem;
            font-weight: 400;
            background: linear-gradient(135deg, #F2EBE1, #C7A99F);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            letter-spacing: -0.02em;
            margin-bottom: 0.2rem;
        }

        .badge-sub {
            font-size: 0.7rem;
            letter-spacing: 0.3rem;
            text-transform: uppercase;
            color: #C4A7A0;
            font-weight: 300;
        }

        .divider-elegant {
            height: 1px;
            background: linear-gradient(90deg, transparent, #C4A7A0, #C4A7A0, transparent);
            width: 50%;
            margin: 1.5rem auto;
            opacity: 0.5;
        }

        .section-title {
            font-size: 1.7rem;
            font-weight: 400;
            border-left: 3px solid #C4A7A0;
            padding-left: 1rem;
            color: #F2EBE1;
            margin: 2rem 0 1rem 0;
            letter-spacing: -0.3px;
        }

        /* skill cards — with logos & glassmorphism */
        .skills-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1.5rem;
            justify-content: center;
        }

        .skill-card {
            background: rgba(23, 21, 19, 0.7);
            backdrop-filter: blur(4px);
            border: 0.6px solid rgba(196, 167, 160, 0.25);
            border-radius: 60px;
            padding: 0.5rem 1.2rem 0.5rem 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: all 0.25s ease;
            box-shadow: 0 2px 6px rgba(0,0,0,0.2);
        }

        .skill-card:hover {
            border-color: #C4A7A0;
            transform: translateY(-3px);
            background: rgba(33, 29, 26, 0.8);
            box-shadow: 0 8px 18px rgba(0,0,0,0.3);
        }

        .skill-icon {
            width: 28px;
            height: 28px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
        }

        .skill-icon img, .skill-icon svg {
            width: 100%;
            height: auto;
            max-height: 24px;
            object-fit: contain;
        }

        .skill-name {
            font-size: 0.85rem;
            font-weight: 500;
            color: #DDD2C6;
            letter-spacing: 0.2px;
        }

        /* custom network icon style (SVG) */
        .network-icon-svg {
            width: 24px;
            height: 24px;
        }

        /* mission card update */
        .mission-card {
            background: linear-gradient(145deg, #13110E, #0D0C0A);
            border-radius: 32px;
            padding: 1.5rem;
            border: 0.5px solid rgba(196, 167, 160, 0.2);
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: space-between;
            align-items: center;
            margin: 1.2rem 0;
        }

        .mission-text {
            flex: 3;
        }

        .mission-icon {
            flex: 1;
            text-align: center;
            font-size: 3rem;
            background: #1F1C19;
            border-radius: 80px;
            padding: 0.8rem;
            width: 80px;
            height: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto;
            border: 0.5px solid #C4A7A0;
        }

        /* stats wrapper */
        .stats-wrapper {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1rem;
            margin-top: 1.2rem;
        }

        .stats-wrapper img {
            border-radius: 20px;
            background: #0D0C0A;
            border: 0.5px solid #2E2A26;
            transition: transform 0.2s;
        }

        .stats-wrapper img:hover {
            transform: scale(0.98);
        }

        /* quote & signature */
        .quote-silent {
            text-align: center;
            font-style: italic;
            font-size: 1rem;
            color: #CFC3B6;
            margin: 2rem 0 0.5rem;
            font-family: 'Cormorant Garamond', serif;
        }

        .signature {
            text-align: center;
            font-size: 0.7rem;
            color: #A18E7E;
            letter-spacing: 1px;
            margin-top: 0.8rem;
        }

        hr.glow {
            margin: 2rem auto 0;
            width: 120px;
            border: none;
            height: 2px;
            background: linear-gradient(90deg, transparent, #C4A7A0, transparent);
        }

        @media (max-width: 680px) {
            .container {
                padding: 1.5rem;
            }
            h1 {
                font-size: 2.6rem;
            }
            .skill-card {
                padding: 0.35rem 1rem 0.35rem 0.8rem;
            }
            .skill-name {
                font-size: 0.75rem;
            }
        }
    </style>
</head>
<body>
<div class="container">

    <!-- header: silent royalty -->
    <div align="center">
        <h1>Ghizlane Elouakili</h1>
        <div class="badge-sub">✦ SOFTWARE ENGINEER IN PROGRESS ✦</div>
        <div style="margin: 0.9rem 0 0.4rem;">
            <span style="background: #1A1815; padding: 0.3rem 1.2rem; border-radius: 40px; font-size: 0.7rem; letter-spacing: 0.2rem; color: #C4A7A0;">MOROCCO  ·  🇲🇦</span>
        </div>
        <div class="divider-elegant"></div>
        <div class="quote-silent" style="max-width: 500px; margin: 0 auto;">
            “I don’t write code… I translate silence into logic.”
        </div>
    </div>

    <!-- identity / quiet storm (enhanced) -->
    <div align="center" style="max-width: 680px; margin: 2rem auto; text-align: center;">
        <span style="font-size: 1.5rem; color: #C4A7A0;">✦</span>
        <p style="color: #C9BCAE; font-size: 0.98rem; line-height: 1.7; margin-top: 0.5rem;">
            I am the contradiction that intrigues me.<br>
            A builder who prefers shadows over spotlights.<br>
            My mind is a library where logic and poetry argue at midnight.<br>
            The storm is real. It just doesn't need to shout.
        </p>
    </div>

    <!-- CURRENT MISSION refined -->
    <div class="section-title">／ current mission</div>
    <div class="mission-card">
        <div class="mission-text">
            <h3 style="font-weight: 400; font-size: 1.7rem; color: #E8DDD2;">Mind Library</h3>
            <p style="color: #BCAF9F; margin-top: 0.3rem;">
                A digital sanctuary where books breathe conversation — not isolated reading, but <em>belonging</em>.<br>
                Intellectual social fabric: upload, annotate, resonate. For minds that refuse to be islands.
            </p>
            <p style="font-size: 0.7rem; color: #9B8879; margin-top: 0.6rem; letter-spacing: 0.3px;">⚡ status: building the first chapter — upload, comment, resonate.</p>
        </div>
        <div class="mission-icon">
            🧠
        </div>
    </div>

    <!-- TECH ARSENAL — MASTERED + LOGOS (complete list: HTML, CSS, JS, C, Java, Express, UI/UX, PHP, Git, GitHub, Shell, Réseau) -->
    <div class="section-title">／ mastered arsenal</div>
    <div style="margin: -0.5rem 0 0.5rem 0; font-size: 0.75rem; color: #B39F8E; letter-spacing: 0.2px;">⟡ every tool, a verse in my logic library</div>

    <div class="skills-grid">
        <!-- HTML5 -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/html5/E34F26" alt="HTML5" width="22" height="22"></div><span class="skill-name">HTML5</span></div>
        <!-- CSS3 -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/css3/1572B6" alt="CSS3" width="22" height="22"></div><span class="skill-name">CSS3</span></div>
        <!-- JavaScript (ES6+) -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/javascript/F7DF1E" alt="JavaScript" width="22" height="22"></div><span class="skill-name">JavaScript (ES6+)</span></div>
        <!-- C -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/c/A8B9CC" alt="C" width="22" height="22"></div><span class="skill-name">C</span></div>
        <!-- Java -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/java/007396" alt="Java" width="22" height="22"></div><span class="skill-name">Java</span></div>
        <!-- Express.js -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/express/000000" alt="Express.js" width="22" height="22" style="filter: invert(0.9);"></div><span class="skill-name">Express.js</span></div>
        <!-- UI/UX (Figma + design) -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/figma/F24E1E" alt="Figma" width="20" height="20"></div><span class="skill-name">UI/UX (Figma)</span></div>
        <!-- PHP -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/php/777BB4" alt="PHP" width="22" height="22"></div><span class="skill-name">PHP</span></div>
        <!-- Git -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/git/F05032" alt="Git" width="22" height="22"></div><span class="skill-name">Git</span></div>
        <!-- GitHub -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/github/181717" alt="GitHub" width="22" height="22" style="filter: brightness(0) invert(1);"></div><span class="skill-name">GitHub</span></div>
        <!-- Shell / Bash -->
        <div class="skill-card"><div class="skill-icon"><img src="https://cdn.simpleicons.org/gnubash/4EAA25" alt="Shell" width="22" height="22"></div><span class="skill-name">Shell / Bash</span></div>
        <!-- Réseau (Networking) custom elegant SVG logo -->
        <div class="skill-card"><div class="skill-icon"><svg class="network-icon-svg" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 4c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2zm0 13c-2.33 0-4.31-1.46-5.11-3.5h10.22c-.8 2.04-2.78 3.5-5.11 3.5z" fill="#C4A7A0"/></svg></div><span class="skill-name">Réseau / Networking</span></div>
    </div>
    
    <!-- additional in progress stack + exploring (modern) -->
    <div style="margin-top: 1rem; display: flex; flex-wrap: wrap; gap: 0.6rem; justify-content: center;">
        <span style="background: #1D1A17; padding: 0.2rem 0.9rem; border-radius: 30px; font-size: 0.7rem; border-left: 2px solid #C4A7A0;">⟡ React (learning)</span>
        <span style="background: #1D1A17; padding: 0.2rem 0.9rem; border-radius: 30px; font-size: 0.7rem; border-left: 2px solid #C4A7A0;">⟡ Node.js (deepening)</span>
        <span style="background: #1D1A17; padding: 0.2rem 0.9rem; border-radius: 30px; font-size: 0.7rem; border-left: 2px solid #C4A7A0;">⟡ MongoDB & PostgreSQL</span>
    </div>

    <!-- full stack & network knowledge description subtle -->
    <div style="margin: 1.8rem 0 0 0; font-size: 0.8rem; text-align: center; background: #13110E; padding: 0.7rem; border-radius: 80px; width: fit-content; margin-left: auto; margin-right: auto;">
        <span style="color:#C4A7A0;">//</span> OSI, TCP/IP, DNS, secure architecture <span style="color:#C4A7A0;">//</span> clean code, CLI automation
    </div>

    <!-- DIGITAL FOOTPRINT stats (improved spacing) -->
    <div class="section-title" style="margin-top: 2.2rem;">／ digital footprint</div>
    <div class="stats-wrapper">
        <img src="https://github-readme-stats.vercel.app/api?username=GHIZLANE-ELOUAKILI&show_icons=true&hide_title=true&bg_color=0D0C0A&title_color=C4A7A0&icon_color=C4A7A0&text_color=A89F91&border_radius=16&border_color=2E2A26&hide_border=false&ring_color=C4A7A0" alt="GitHub Stats" width="48%">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=GHIZLANE-ELOUAKILI&layout=compact&bg_color=0D0C0A&title_color=C4A7A0&text_color=A89F91&border_radius=16&border_color=2E2A26&hide_border=false" alt="Top Languages" width="48%">
    </div>

    <!-- hidden poetry: deeper philosophy (additional emotion) + current learning path -->
    <div style="margin: 2.2rem 0 0.5rem 0; padding: 1rem 1.2rem; background: rgba(20, 18, 16, 0.6); border-radius: 28px; border-left: 2px solid #C4A7A0;">
        <p style="font-size: 0.85rem; font-style: normal; color: #D9CEC1; display: flex; align-items: center; gap: 8px;">
            <span style="font-size: 1.6rem;">🌙</span> 
            <span><strong style="font-family: 'Cormorant Garamond'; font-weight: 500;">currently architecting</strong> — Express.js backends, Java OOP fluency, bash automation, and networking protocols that whisper. Every line, an elegy.</span>
        </p>
    </div>

    <!-- final signature / closing (cinematic) -->
    <div align="center" style="margin-top: 2.5rem;">
        <div style="width: 50px; height: 1px; background: #C4A7A0; margin: 0 auto 1rem;"></div>
        <p class="quote-silent" style="font-size: 0.9rem;">“The loudest storms are the ones you never see coming.”</p>
        <div class="signature">
            Ghizlane — always building, quietly.
        </div>
        <hr class="glow">
    </div>
    <div style="height: 5px;"></div>
</div>
<!-- small whisper: note for observer: full mastery in HTML/CSS/JS/C/Java/Express/UI-UX/PHP/Git/GitHub/Shell/Reseau -->
</body>
</html>
