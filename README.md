<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Only For U Lolii - Protected</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0c0c2e 0%, #1a1a3e 50%, #2d1b3e 100%);
            color: #fff;
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* Password Screen */
        .password-container {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .password-box {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 50px 40px;
            width: 100%;
            max-width: 500px;
            text-align: center;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .lock-icon {
            font-size: 4rem;
            color: #ff6b9d;
            margin-bottom: 20px;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .password-title {
            font-family: 'Dancing Script', cursive;
            font-size: 3rem;
            color: #ff6b9d;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(255, 107, 157, 0.5);
        }

        .password-subtitle {
            color: #b19cd9;
            margin-bottom: 30px;
            font-size: 1.2rem;
        }

        .password-input {
            width: 100%;
            padding: 15px 20px;
            font-size: 1.2rem;
            border: 2px solid rgba(255, 107, 157, 0.3);
            border-radius: 50px;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            margin-bottom: 20px;
            text-align: center;
            transition: all 0.3s;
        }

        .password-input:focus {
            outline: none;
            border-color = #ff6b9d;
            box-shadow: 0 0 15px rgba(255, 107, 157, 0.5);
        }

        .password-button {
            background: linear-gradient(to right, #ff6b9d, #b19cd9);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1.2rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
            width: 100%;
        }

        .password-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 107, 157, 0.3);
        }

        .password-hint {
            margin-top: 20px;
            color: #b19cd9;
            font-size: 0.9rem;
            font-style: italic;
        }

        .error-message {
            color: #ff6b6b;
            margin-top: 15px;
            min-height: 20px;
            font-weight: 600;
        }

        /* Hidden Main Content */
        .main-content {
            display: none;
            opacity: 0;
            transition: opacity 0.5s;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            padding: 30px 20px;
            position: relative;
        }

        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 4.5rem;
            color: #ff6b9d;
            text-shadow: 0 0 15px rgba(255, 107, 157, 0.5);
            margin-bottom: 10px;
            letter-spacing: 1px;
        }

        .subtitle {
            font-size: 1.3rem;
            color: #b19cd9;
            margin-bottom: 30px;
            font-weight: 300;
        }

        .new-year-card {
            background: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .new-year-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, #ff6b9d, #b19cd9, #6a93ff);
        }

        .year {
            font-size: 8rem;
            font-weight: 700;
            background: linear-gradient(to right, #ff6b9d, #b19cd9, #6a93ff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            line-height: 1;
            margin-bottom: 10px;
        }

        .greeting {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #fff;
            font-weight: 600;
        }

        .girlfriend-name {
            color: #ff6b9d;
            font-weight: 700;
            text-shadow: 0 0 10px rgba(255, 107, 157, 0.5);
        }

        .heart {
            color: #ff6b9d;
            margin: 0 10px;
            animation: heartbeat 1.5s infinite;
        }

        @keyframes heartbeat {
            0% { transform: scale(1); }
            5% { transform: scale(1.3); }
            10% { transform: scale(1.1); }
            15% { transform: scale(1.3); }
            20% { transform: scale(1); }
            100% { transform: scale(1); }
        }

        /* Memories Gallery Section */
        .memories-section {
            margin: 60px 0;
            padding: 40px 20px;
        }

        .memories-title {
            font-family: 'Dancing Script', cursive;
            font-size: 3.5rem;
            text-align: center;
            margin-bottom: 40px;
            color: #ff6b9d;
            text-shadow: 0 0 10px rgba(255, 107, 157, 0.3);
        }

        .gallery-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .memory-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
            cursor: pointer;
        }

        .memory-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(255, 107, 157, 0.2);
            border-color: #ff6b9d;
        }

        .memory-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            display: block;
            transition: transform 0.5s ease;
        }

        .memory-card:hover .memory-img {
            transform: scale(1.05);
        }

        .memory-caption {
            padding: 20px;
            text-align: center;
            font-size: 1.1rem;
            color: #f0e6ff;
            min-height: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(0, 0, 0, 0.3);
        }

        /* Personal Note Section */
        .personal-note-section {
            margin-top: 40px;
        }

        .section-title {
            font-family: 'Dancing Script', cursive;
            font-size: 2.8rem;
            text-align: center;
            margin-bottom: 30px;
            color: #b19cd9;
        }

        .note-container {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            line-height: 1.8;
            font-size: 1.2rem;
            text-align: right;
            border-right: 4px solid #ff6b9d;
            position: relative;
            min-height: 350px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .note-container::before {
            content: '"';
            position: absolute;
            top: 10px;
            left: 20px;
            font-size: 8rem;
            color: rgba(255, 107, 157, 0.2);
            font-family: serif;
            line-height: 1;
        }

        .arabic-text {
            direction: rtl;
            margin-bottom: 20px;
            color: #f0e6ff;
        }

        .english-text {
            color: #d9c9ff;
            margin-bottom: 20px;
            font-style: italic;
        }

        .signature {
            text-align: left;
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            color: #ff6b9d;
            margin-top: 10px;
        }

        .decorations {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }

        .decoration-item {
            font-size: 2rem;
            color: #ff6b9d;
            animation: float 3s ease-in-out infinite;
        }

        .decoration-item:nth-child(2) {
            animation-delay: 0.5s;
            color: #b19cd9;
        }

        .decoration-item:nth-child(3) {
            animation-delay: 1s;
            color: #6a93ff;
        }

        .decoration-item:nth-child(4) {
            animation-delay: 1.5s;
            color: #ffd166;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }

        footer {
            text-align: center;
            padding: 30px 0;
            margin-top: 40px;
            color: #b19cd9;
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .fireworks {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .firework {
            position: absolute;
            width: 4px;
            height: 4px;
            border-radius: 50%;
            box-shadow: 0 0 10px 2px;
            animation: explode 2s infinite;
        }

        @keyframes explode {
            0% { transform: translateY(100vh) scale(0); opacity: 1; }
            100% { transform: translateY(0) scale(1); opacity: 0; }
        }

        /* Countdown Timer */
        .countdown-container {
            margin: 30px 0;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
        }

        .countdown-title {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #b19cd9;
            text-align: center;
        }

        .countdown {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .countdown-item {
            text-align: center;
            min-width: 100px;
        }

        .countdown-number {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(to right, #ff6b9d, #b19cd9);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            line-height: 1;
            margin-bottom: 5px;
        }

        .countdown-label {
            font-size: 0.9rem;
            color: #b19cd9;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .password-title { font-size: 2.5rem; }
            .lock-icon { font-size: 3rem; }
            h1 { font-size: 3.5rem; }
            .year { font-size: 6rem; }
            .greeting { font-size: 2rem; }
            .memories-title { font-size: 2.8rem; }
            .gallery-container { grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); }
            .note-container { padding: 20px; font-size: 1.1rem; }
            .section-title { font-size: 2.2rem; }
        }

        @media (max-width: 480px) {
            .password-box { padding: 30px 20px; }
            .password-title { font-size: 2rem; }
            h1 { font-size: 2.8rem; }
            .year { font-size: 4.5rem; }
            .greeting { font-size: 1.6rem; }
            .memories-title { font-size: 2.2rem; }
            .gallery-container { grid-template-columns: 1fr; }
            .new-year-card { padding: 25px 20px; }
            .note-container { padding: 15px; }
        }
    </style>
</head>
<body>
    <!-- Password Screen -->
    <div class="password-container" id="passwordScreen">
        <div class="password-box">
            <div class="lock-icon">
                <i class="fas fa-lock"></i>
            </div>
            <h1 class="password-title">Only For Lolii</h1>
            <p class="password-subtitle">This message is protected. Enter the special password to continue.</p>
            
            <input type="password" class="password-input" id="passwordInput" placeholder="Enter our special number..." autocomplete="off">
            <button class="password-button" id="submitPassword">Unlock My Message</button>
            
            <div class="error-message" id="errorMessage"></div>
            <p class="password-hint">Hint: It's a number that's special to us</p>
        </div>
    </div>

    <!-- Main Content (Hidden until password is entered) -->
    <div class="main-content" id="mainContent">
        <div class="fireworks" id="fireworks"></div>
        
        <div class="container">
            <header>
                <h1>Only For U Lolii</h1>
                <p class="subtitle">A special New Year wish from the heart • 2026</p>
            </header>
            
            <main>
                <div class="new-year-card">
                    <div class="year">2026</div>
                    <h2 class="greeting">Happy New Year <span class="girlfriend-name">Lolii</span>!</h2>
                    <p>May 2026 bring you endless joy, love, and happiness</p>
                    
                    <div class="countdown-container">
                        <div class="countdown-title">Our First Moments of 2026 Together</div>
                        <div class="countdown">
                            <div class="countdown-item">
                                <div class="countdown-number" id="days">0</div>
                                <div class="countdown-label">Days</div>
                            </div>
                            <div class="countdown-item">
                                <div class="countdown-number" id="hours">0</div>
                                <div class="countdown-label">Hours</div>
                            </div>
                            <div class="countdown-item">
                                <div class="countdown-number" id="minutes">0</div>
                                <div class="countdown-label">Minutes</div>
                            </div>
                            <div class="countdown-item">
                                <div class="countdown-number" id="seconds">0</div>
                                <div class="countdown-label">Seconds</div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="decorations">
                        <div class="decoration-item"><i class="fas fa-heart"></i></div>
                        <div class="decoration-item"><i class="fas fa-star"></i></div>
                        <div class="decoration-item"><i class="fas fa-gem"></i></div>
                        <div class="decoration-item"><i class="fas fa-moon"></i></div>
                    </div>
                </div>
                
                <!-- Personal Note Section -->
                <section class="personal-note-section">
                    <h2 class="section-title">A Personal Note</h2>
                    <div class="note-container">
                        <div class="arabic-text">
                            إحنا الإتنين داخلين على سنة جديدة وإحنا مع بعض🫣❤️
                            <br><br>
                            أنا هاكون ليكي دايماً الأخ والصاحب والحبيب وإن شاء الله الزوج🫣
                            غيرتي فيا كتير في الشهرين اللي فاتوا بس إنتي لسه مش مدركة قد إيه أنا مبسوط بوجودك في حياتي🙈❤️
                            <br><br>
                            إنتي خلاص بقيتي حياتي وعمري وروحي وإن شاء الله في أقرب وقت نقدر عليه تبقى مراتي وأم ولادي كمان🥰❤️
                            <br><br>
                            أنا مش بحبك بس انا بعشقك يا روح قلبي 🥺❤️❤️❤️❤️❤️❤️❤️❤️
                        </div>
                        <div class="english-text">
                            We're entering 2026 together🫣❤️
                            I hope we always stay by each other's side, always honest with each other, and always be best friends, lovers, and soulmates, and everything with each other🥰
                            I'll always be your brother, friend, lover, and hopefully your husband🫣
                            You changed a lot in the previous 2 months but you still don't realize how happy I am with your presence in my life🙈❤️
                            <br><br>
                            You've become my life, my age, my soul, and hopefully in the nearest possible time, you become my wife and the mother of my children too🥰❤️
                            <br><br>
                            Love you so much y Lolo..wla a2olk....
                        </div>
                        <div class="signature">With all my love ❤️</div>
                    </div>
                </section>
                
                <!-- Memories Gallery Section -->
                <section class="memories-section">
                    <h2 class="memories-title">Some of my fav memories🥰</h2>
                    
                    <div class="gallery-container">
                        <!-- Memory 1 -->
                        <div class="memory-card">
                            <img src="https://i.ibb.co/C5phQnDT/IMG-20240527-160331.jpg" 
                                 alt="Romantic sunset" class="memory-img">
                            <div class="memory-caption">
                                That magical sunset when we first held hands ❤️
                            </div>
                        </div>
                        
                        <!-- Memory 2 -->
                        <div class="memory-card">
                            <img src="https://i.ibb.co/4nq3FmWn/IMG-20240527-160134.jpg" 
                                 alt="Beautiful smile" class="memory-img">
                            <div class="memory-caption">
                                Your smile that lights up my whole world ✨
                            </div>
                        </div>
                        
                        <!-- Memory 3 -->
                        <div class="memory-card">
                            <img src="https://i.ibb.co/bRjfFnWh/IMG-20240527-155841.jpg" 
                                 alt="Sudden meeting" class="memory-img">
                            <div class="memory-caption">
                                mn a7la el aw2at ely 2a3dtha mt3aki - I was so nervous but so happy! 🥰
                            </div>
                        </div>
                        
                        <!-- Memory 4 -->
                        <div class="memory-card">
                            <img src="https://i.ibb.co/4RLSNP1k/IMG-20240527-160314.jpg" 
                                 alt="Beach day" class="memory-img">
                            <div class="memory-caption">
                                That amazing beach day with you 🌊
                            </div>
                        </div>
                        
                        <!-- Memory 5 -->
                        <div class="memory-card">
                            <img src="https://i.ibb.co/671ZFb35/IMG-20240527-160226.jpg" 
                                 alt="Our engagement" class="memory-img">
                            <div class="memory-caption">
                                Our engagement 🫣
                            </div>
                        </div>
                        
                        <!-- Memory 6 -->
                        <div class="memory-card">
                            <img src="https://i.ibb.co/FR4PQZP/IMG-20240527-160059.jpg" 
                                 alt="My favorite person" class="memory-img">
                            <div class="memory-caption">
                                Just by looking at you I realise you're my favorite person 🥺❤️❤️❤️❤️
                            </div>
                        </div>
                    </div>
                </section>
            </main>
            
            <footer>
                <p>Made with <i class="fas fa-heart heart"></i> for Lolii | Happy New Year 2026</p>
                <p>Every moment with you is my favorite memory ❤️</p>
            </footer>
        </div>
    </div>

    <script>
        // Password Protection
        const CORRECT_PASSWORD = "16148";
        const passwordInput = document.getElementById('passwordInput');
        const submitButton = document.getElementById('submitPassword');
        const errorMessage = document.getElementById('errorMessage');
        const passwordScreen = document.getElementById('passwordScreen');
        const mainContent = document.getElementById('mainContent');

        // Function to check password
        function checkPassword() {
            const enteredPassword = passwordInput.value.trim();
            
            if (enteredPassword === CORRECT_PASSWORD) {
                // Success - show main content
                passwordScreen.style.display = 'none';
                mainContent.style.display = 'block';
                
                // Fade in effect
                setTimeout(() => {
                    mainContent.style.opacity = '1';
                }, 50);
                
                // Start animations
                startAnimations();
            } else {
                // Error effect
                errorMessage.textContent = "Incorrect password. Try again.";
                passwordInput.style.borderColor = '#ff6b6b';
                passwordInput.style.boxShadow = '0 0 10px rgba(255, 107, 157, 0.5)';
                
                // Shake animation
                passwordInput.classList.add('shake');
                setTimeout(() => {
                    passwordInput.classList.remove('shake');
                }, 500);
                
                // Clear input
                passwordInput.value = '';
                passwordInput.focus();
            }
        }

        // Add shake animation
        const style = document.createElement('style');
        style.textContent = `
            .shake {
                animation: shake 0.5s;
            }
            @keyframes shake {
                0%, 100% { transform: translateX(0); }
                10%, 30%, 50%, 70%, 90% { transform: translateX(-5px); }
                20%, 40%, 60%, 80% { transform: translateX(5px); }
            }
        `;
        document.head.appendChild(style);

        // Event Listeners
        submitButton.addEventListener('click', checkPassword);
        
        passwordInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                checkPassword();
            }
        });

        // Focus on input when page loads
        window.addEventListener('load', () => {
            passwordInput.focus();
        });

        // Main content animations
        function startAnimations() {
            // Create fireworks effect
            function createFireworks() {
                const fireworksContainer = document.getElementById('fireworks');
                const colors = ['#ff6b9d', '#b19cd9', '#6a93ff', '#ffd166', '#ff9e6d'];
                
                for (let i = 0; i < 50; i++) {
                    const firework = document.createElement('div');
                    firework.className = 'firework';
                    
                    // Random position
                    const posX = Math.random() * 100;
                    const posY = Math.random() * 100;
                    
                    // Random color
                    const color = colors[Math.floor(Math.random() * colors.length)];
                    
                    // Random size and animation delay
                    const size = Math.random() * 5 + 2;
                    const delay = Math.random() * 2;
                    
                    firework.style.left = `${posX}%`;
                    firework.style.top = `${posY}%`;
                    firework.style.width = `${size}px`;
                    firework.style.height = `${size}px`;
                    firework.style.backgroundColor = color;
                    firework.style.boxShadow = `0 0 10px 2px ${color}`;
                    firework.style.animationDelay = `${delay}s`;
                    
                    fireworksContainer.appendChild(firework);
                    
                    // Remove firework after animation completes
                    setTimeout(() => {
                        firework.remove();
                    }, 2000);
                }
            }
            
            // Create initial fireworks
            createFireworks();
            
            // Create fireworks periodically
            setInterval(createFireworks, 3000);
            
            // Add heartbeat effect to the girlfriend's name
            const nameElement = document.querySelector('.girlfriend-name');
            setInterval(() => {
                nameElement.style.textShadow = '0 0 15px rgba(255, 107, 157, 0.8)';
                setTimeout(() => {
                    nameElement.style.textShadow = '0 0 10px rgba(255, 107, 157, 0.5)';
                }, 300);
            }, 2000);
            
            // Countdown timer for New Year 2026
            function updateCountdown() {
                const now = new Date();
                const currentYear = now.getFullYear();
                
                // Set target to Jan 1, 2026 (or next year if we're already in 2026)
                let targetYear = 2026;
                if (currentYear >= 2026) {
                    targetYear = currentYear + 1;
                }
                
                const targetDate = new Date(`January 1, ${targetYear} 00:00:00`);
                const timeRemaining = targetDate - now;
                
                // Calculate days, hours, minutes, seconds
                const days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));
                const hours = Math.floor((timeRemaining % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((timeRemaining % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((timeRemaining % (1000 * 60)) / 1000);
                
                // Update display
                document.getElementById('days').textContent = days.toString().padStart(2, '0');
                document.getElementById('hours').textContent = hours.toString().padStart(2, '0');
                document.getElementById('minutes').textContent = minutes.toString().padStart(2, '0');
                document.getElementById('seconds').textContent = seconds.toString().padStart(2, '0');
                
                // If it's already 2026, show a celebration message
                if (currentYear === 2026 && days === 0 && hours === 0 && minutes === 0 && seconds === 0) {
                    document.querySelector('.countdown-title').textContent = "🎉 Happy New Year 2026! We made it! 🎉";
                    document.querySelector('.countdown').style.display = 'none';
                }
            }
            
            // Initialize countdown
            updateCountdown();
            setInterval(updateCountdown, 1000);
            
            // Special message if it's already 2026
            const currentYear = new Date().getFullYear();
            if (currentYear === 2026) {
                document.querySelector('.countdown-title').textContent = "🎉 Celebrating Our 2026 Together! 🎉";
            }
        }
    </script>
</body>
</html>
