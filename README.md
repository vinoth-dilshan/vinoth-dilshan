<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vinoth Dilshan | GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'JetBrains Mono', monospace, -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #0f172a 100%);
            color: #f8fafc;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }

        /* Snow container */
        .snow-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
            overflow: hidden;
        }

        .snow {
            position: absolute;
            top: -10px;
            background: white;
            border-radius: 50%;
            opacity: 0.8;
            animation: snowfall linear infinite;
        }

        @keyframes snowfall {
            0% {
                transform: translateY(-10px) rotate(0deg);
                opacity: 0.8;
            }
            100% {
                transform: translateY(100vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* Main content */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            position: relative;
            z-index: 2;
        }

        /* Header section */
        .header {
            text-align: center;
            padding: 3rem 1rem;
            background: rgba(15, 23, 42, 0.7);
            backdrop-filter: blur(10px);
            border-radius: 24px;
            margin-bottom: 3rem;
            border: 1px solid rgba(56, 189, 248, 0.2);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3),
                        0 0 80px rgba(56, 189, 248, 0.1);
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, 
                #38bdf8 0%, 
                #0ea5e9 25%, 
                #0284c7 50%, 
                #0ea5e9 75%, 
                #38bdf8 100%);
        }

        .typing-text {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            background: linear-gradient(90deg, #38bdf8, #0ea5e9, #7dd3fc);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: textGlow 3s ease-in-out infinite alternate;
        }

        @keyframes textGlow {
            0% { filter: drop-shadow(0 0 5px rgba(56, 189, 248, 0.5)); }
            100% { filter: drop-shadow(0 0 20px rgba(56, 189, 248, 0.8)); }
        }

        .subtitle {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
            color: #cbd5e1;
            font-weight: 300;
        }

        /* Badges */
        .badges {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin: 2rem 0;
        }

        .badge {
            padding: 0.75rem 1.5rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .badge-age {
            background: linear-gradient(135deg, #38bdf8, #0ea5e9);
            color: white;
        }

        .badge-location {
            background: linear-gradient(135deg, #10b981, #059669);
            color: white;
        }

        .badge-lang {
            background: linear-gradient(135deg, #8b5cf6, #7c3aed);
            color: white;
        }

        /* Snow GIF section */
        .snow-gif-section {
            text-align: center;
            margin: 3rem 0;
            padding: 2rem;
            background: rgba(15, 23, 42, 0.5);
            border-radius: 20px;
            border: 1px solid rgba(56, 189, 248, 0.1);
        }

        .snow-gif {
            max-width: 100%;
            border-radius: 16px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4),
                        0 0 60px rgba(56, 189, 248, 0.1);
            transition: transform 0.5s ease;
        }

        .snow-gif:hover {
            transform: scale(1.02);
        }

        /* Holiday message */
        .holiday-message {
            text-align: center;
            padding: 3rem;
            margin: 3rem 0;
            background: linear-gradient(135deg, 
                rgba(230, 57, 70, 0.15) 0%, 
                rgba(56, 189, 248, 0.15) 100%);
            border-radius: 24px;
            border-left: 6px solid #38bdf8;
            border-right: 6px solid #E63946;
            position: relative;
            overflow: hidden;
        }

        .holiday-message h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(90deg, #E63946, #38bdf8);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .holiday-message p {
            font-size: 1.2rem;
            color: #cbd5e1;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
        }

        /* Stats section */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin: 3rem 0;
        }

        .stat-card {
            background: rgba(15, 23, 42, 0.7);
            padding: 2rem;
            border-radius: 16px;
            text-align: center;
            border: 1px solid rgba(56, 189, 248, 0.1);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            border-color: #38bdf8;
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(56, 189, 248, 0.1);
        }

        .stat-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #38bdf8;
        }

        .stat-card p {
            color: #cbd5e1;
            line-height: 1.6;
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            color: #94a3b8;
            font-size: 0.9rem;
            border-top: 1px solid rgba(56, 189, 248, 0.1);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .typing-text {
                font-size: 2.2rem;
            }
            
            .subtitle {
                font-size: 1.4rem;
            }
            
            .holiday-message h2 {
                font-size: 2rem;
            }
            
            .container {
                padding: 1rem;
            }
        }

        @media (max-width: 480px) {
            .typing-text {
                font-size: 1.8rem;
            }
            
            .badges {
                flex-direction: column;
                align-items: center;
            }
            
            .badge {
                width: 100%;
                max-width: 250px;
            }
        }
    </style>
</head>
<body>
    <!-- Snow animation container -->
    <div class="snow-container" id="snowContainer"></div>
    
    <div class="container">
        <!-- Header section -->
        <header class="header">
            <h1 class="typing-text">Welcome to my GitHub Profile!</h1>
            <h2 class="subtitle">I'm Vinoth Dilshan</h2>
            <h2 class="subtitle">From Sri Lanka 🇱🇰</h2>
            <h2 class="subtitle">BIT Undergraduate | Active Learner and Builder</h2>
            
            <div class="badges">
                <div class="badge badge-age">Age: 21</div>
                <div class="badge badge-location">Lives: Sri Lanka</div>
                <div class="badge badge-lang">Languages: English & Sinhala</div>
            </div>
        </header>
        
        <!-- Snow GIF section -->
        <section class="snow-gif-section">
            <img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExdHN2YzduZGNwb3F6a2d3cDB2d284OHM5ZGs3azk3eGthbmQ2c2NlaiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/ok6MAjOB0Rqcd0TAR6/giphy.gif" 
                 alt="Snow GIF" class="snow-gif" />
        </section>
        
        <!-- Holiday message -->
        <section class="holiday-message">
            <h2>❄️✨ Cristmess Season vibes — Code safe, Stay warm! ✨❄️</h2>
            <p>Embracing the festive spirit while building innovative solutions. Wishing you a season filled with bug-free code, efficient algorithms, and warm moments with loved ones.</p>
        </section>
        
        <!-- Stats section -->
        <section class="stats">
            <div class="stat-card">
                <h3>🎓 Education</h3>
                <p>Bachelor of Information Technology (BIT) Undergraduate with focus on software engineering, data structures, and modern web technologies.</p>
            </div>
            
            <div class="stat-card">
                <h3>💻 Tech Stack</h3>
                <p>JavaScript, Python, React, Node.js, Git, SQL, Cloud Computing, and continuously expanding my skills with new technologies.</p>
            </div>
            
            <div class="stat-card">
                <h3>🚀 Projects</h3>
                <p>Building practical applications, contributing to open source, and developing solutions that bridge technology with real-world needs.</p>
            </div>
            
            <div class="stat-card">
                <h3>🌱 Learning</h3>
                <p>Active learner exploring AI/ML, cloud architecture, and full-stack development to create impactful digital experiences.</p>
            </div>
        </section>
        
        <!-- Footer -->
        <footer class="footer">
            <p>© 2023 Vinoth Dilshan | Sri Lanka 🇱🇰 | Connecting technology with purpose</p>
            <p>Made with ❤️ and ☕</p>
        </footer>
    </div>

    <script>
        // Generate snowflakes with pure CSS (no external JS libraries)
        document.addEventListener('DOMContentLoaded', function() {
            const snowContainer = document.getElementById('snowContainer');
            const snowflakeCount = 80;
            
            // Create snowflakes
            for (let i = 0; i < snowflakeCount; i++) {
                const snowflake = document.createElement('div');
                snowflake.classList.add('snow');
                
                // Random size between 2px and 10px
                const size = Math.random() * 8 + 2;
                snowflake.style.width = `${size}px`;
                snowflake.style.height = `${size}px`;
                
                // Random horizontal position
                snowflake.style.left = `${Math.random() * 100}vw`;
                
                // Random animation duration between 5 and 15 seconds
                const duration = Math.random() * 10 + 5;
                snowflake.style.animationDuration = `${duration}s`;
                
                // Random animation delay
                snowflake.style.animationDelay = `${Math.random() * 5}s`;
                
                // Random opacity
                snowflake.style.opacity = Math.random() * 0.7 + 0.3;
                
                snowContainer.appendChild(snowflake);
            }
            
            // Add a simple typing effect for the main title
            const typingText = document.querySelector('.typing-text');
            const originalText = typingText.textContent;
            typingText.textContent = '';
            
            let i = 0;
            function typeWriter() {
                if (i < originalText.length) {
                    typingText.textContent += originalText.charAt(i);
                    i++;
                    setTimeout(typeWriter, 50);
                }
            }
            
            // Start typing effect after a short delay
            setTimeout(typeWriter, 1000);
        });
    </script>
</body>
</html>
