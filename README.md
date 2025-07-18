<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Beautiful Kushina - A Love Letter</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(135deg, #fdf2f8, #f3e8ff, #fefce8);
            min-height: 100vh;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            background: linear-gradient(135deg, #f43f5e, #a855f7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: #374151;
            font-weight: 500;
            transition: color 0.3s;
            cursor: pointer;
        }

        .nav-links a:hover {
            color: #f43f5e;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            padding-top: 80px;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, #f43f5e, #a855f7, #f59e0b);
            opacity: 0.1;
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 5rem;
            background: linear-gradient(135deg, #f43f5e, #a855f7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease-out;
        }

        .hero-subtitle {
            font-size: 1.5rem;
            color: #374151;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .hero-description {
            font-size: 1.1rem;
            color: #6b7280;
            max-width: 600px;
            margin: 0 auto 3rem;
            line-height: 1.8;
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        .cta-button {
            background: linear-gradient(135deg, #f43f5e, #a855f7);
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            animation: fadeInUp 1s ease-out 0.9s both;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(244, 63, 94, 0.3);
        }

        /* Love Reasons Section */
        .love-section {
            padding: 5rem 0;
            background: rgba(255, 255, 255, 0.5);
        }

        .section-title {
            text-align: center;
            font-size: 3rem;
            background: linear-gradient(135deg, #f43f5e, #a855f7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 3rem;
        }

        .love-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .love-card {
            background: rgba(255, 255, 255, 0.8);
            padding: 2rem;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            opacity: 0;
            transform: translateY(20px);
        }

        .love-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .love-card.animate {
            animation: slideUp 0.8s ease-out forwards;
        }

        .love-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #f43f5e, #a855f7);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1rem;
            font-size: 1.5rem;
            color: white;
        }

        .love-card h3 {
            font-size: 1.3rem;
            color: #374151;
            margin-bottom: 1rem;
        }

        .love-card p {
            color: #6b7280;
            line-height: 1.6;
        }

        /* Photo Gallery */
        .gallery-section {
            padding: 5rem 0;
            background: linear-gradient(135deg, #fdf2f8, #f3e8ff);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 15px;
            height: 250px;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(0, 0, 0, 0.8));
            color: white;
            padding: 1rem;
            transform: translateY(100%);
            transition: transform 0.3s;
        }

        .gallery-item:hover .gallery-overlay {
            transform: translateY(0);
        }

        /* Interactive Section */
        .interactive-section {
            padding: 5rem 0;
            background: rgba(255, 255, 255, 0.7);
        }

        .quote-card {
            background: rgba(255, 255, 255, 0.9);
            padding: 3rem;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            margin-bottom: 3rem;
        }

        .quote-text {
            font-size: 1.5rem;
            font-style: italic;
            color: #374151;
            margin-bottom: 1rem;
            line-height: 1.8;
        }

        .quote-author {
            color: #6b7280;
            font-size: 1rem;
        }

        .promise-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .promise-card {
            background: rgba(255, 255, 255, 0.8);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s;
        }

        .promise-card:hover {
            transform: translateY(-5px);
        }

        .promise-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #f43f5e, #a855f7);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1rem;
            font-size: 1.2rem;
            color: white;
        }

        .love-declaration {
            background: linear-gradient(135deg, #f43f5e, #a855f7);
            color: white;
            padding: 2rem;
            border-radius: 50px;
            text-align: center;
            font-size: 1.3rem;
            font-weight: 600;
            margin-top: 3rem;
            animation: pulse 2s infinite;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, #f43f5e, #a855f7);
            color: white;
            padding: 3rem 0;
            text-align: center;
        }

        .footer-content {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-bottom: 2rem;
        }

        .footer-item {
            text-align: center;
        }

        .footer-icon {
            width: 50px;
            height: 50px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 0.5rem;
            font-size: 1.2rem;
        }

        /* Floating Hearts */
        .floating-hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .heart {
            position: absolute;
            color: #f43f5e;
            opacity: 0.3;
            animation: float 6s ease-in-out infinite;
        }

        .heart:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
        .heart:nth-child(2) { top: 60%; left: 80%; animation-delay: 1s; }
        .heart:nth-child(3) { top: 40%; left: 20%; animation-delay: 2s; }
        .heart:nth-child(4) { top: 80%; left: 70%; animation-delay: 3s; }
        .heart:nth-child(5) { top: 10%; left: 60%; animation-delay: 4s; }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 3rem;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .love-grid {
                grid-template-columns: 1fr;
            }
            
            .gallery-grid {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            }
            
            .footer-content {
                flex-direction: column;
                gap: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Floating Hearts -->
    <div class="floating-hearts">
        <div class="heart">♥</div>
        <div class="heart">♥</div>
        <div class="heart">♥</div>
        <div class="heart">♥</div>
        <div class="heart">♥</div>
    </div>

    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">
                ♥ For Kushina
            </div>
            <ul class="nav-links">
                <li><a onclick="scrollToSection('home')">Home</a></li>
                <li><a onclick="scrollToSection('love')">My Love</a></li>
                <li><a onclick="scrollToSection('memories')">Our Memories</a></li>
                <li><a onclick="scrollToSection('together')">Together</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Kushina</h1>
            <p class="hero-subtitle">My Beautiful, Amazing, Incredible Love</p>
            <p class="hero-description">
                Every moment with you feels like a dream come true. This website is my love letter to you, 
                celebrating the incredible girl you are and the beautiful journey we're on together.
            </p>
            <button class="cta-button" onclick="scrollToSection('love')">
                ♥ Explore My Love
            </button>
        </div>
    </section>

    <!-- Love Reasons Section -->
    <section id="love" class="love-section">
        <div class="container">
            <h2 class="section-title">Why I Love You</h2>
            <p style="text-align: center; font-size: 1.2rem; color: #6b7280;">
                There are countless reasons why you mean everything to me
            </p>
            
            <div class="love-grid">
                <div class="love-card">
                    <div class="love-icon">😊</div>
                    <h3>Your Beautiful Smile</h3>
                    <p>Your smile lights up my entire world. It's the first thing I think about in the morning and the last thing I dream about at night.</p>
                </div>
                
                <div class="love-card">
                    <div class="love-icon">♥</div>
                    <h3>Your Caring Heart</h3>
                    <p>The way you care for everyone around you shows what an incredible person you are. Your compassion inspires me every day.</p>
                </div>
                
                <div class="love-card">
                    <div class="love-icon">⭐</div>
                    <h3>Your Amazing Personality</h3>
                    <p>You're funny, intelligent, kind, and absolutely perfect in every way. Being with you feels like home.</p>
                </div>
                
                <div class="love-card">
                    <div class="love-icon">☀️</div>
                    <h3>You Make Everything Better</h3>
                    <p>Even on the toughest days, just being with you makes everything feel alright. You're my sunshine and my strength.</p>
                </div>
                
                <div class="love-card">
                    <div class="love-icon">∞</div>
                    <h3>Our Future Together</h3>
                    <p>I can't wait to create a lifetime of beautiful memories with you. Every day with you is a new adventure.</p>
                </div>
                
                <div class="love-card">
                    <div class="love-icon">💎</div>
                    <h3>You're Simply Perfect</h3>
                    <p>In every way imaginable, you're perfect for me. I love you more than words can express, my beautiful Kushina.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Photo Gallery -->
    <section id="memories" class="gallery-section">
        <div class="container">
            <h2 class="section-title">Our Beautiful Memories</h2>
            <p style="text-align: center; font-size: 1.2rem; color: #6b7280;">
                Every moment we share together becomes a treasured memory
            </p>
            
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://github.com/grazeweb/images/blob/main/Screenshot%202025-07-13%20153700.png?raw=true" alt="Our First Date">
                    <div class="gallery-overlay">
                        <h4>Our First Date</h4>
                        <p>The day everything changed</p>
                    </div>
                </div>
                
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&h=300" alt="Laughter & Joy">
                    <div class="gallery-overlay">
                        <h4>Laughter & Joy</h4>
                        <p>You make me smile every day</p>
                    </div>
                </div>
                
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1551218808-94e220e084d2?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&h=300" alt="Romantic Dinners">
                    <div class="gallery-overlay">
                        <h4>Romantic Dinners</h4>
                        <p>Special moments together</p>
                    </div>
                </div>
                
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1521737604893-d14cc237f11d?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&h=300" alt="Adventures Together">
                    <div class="gallery-overlay">
                        <h4>Adventures Together</h4>
                        <p>Every journey with you</p>
                    </div>
                </div>
                
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1469474968028-56623f02e42e?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&h=300" alt="Sunset Dreams">
                    <div class="gallery-overlay">
                        <h4>Sunset Dreams</h4>
                        <p>Beautiful endings, new beginnings</p>
                    </div>
                </div>
                
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1518837695005-2083093ee35b?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&h=300" alt="Cozy Moments">
                    <div class="gallery-overlay">
                        <h4>Cozy Moments</h4>
                        <p>Perfect in your arms</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Interactive Section -->
    <section id="together" class="interactive-section">
        <div class="container">
            <h2 class="section-title">Together Forever</h2>
            
            <div class="quote-card">
                <p class="quote-text">
                    "In all the world, there is no heart for me like yours. In all the world, there is no love for you like me hehehe ."
                </p>
                <p class="quote-author">- Grazeweb:)</p>
            </div>
            
            <div class="promise-grid">
                <div class="promise-card">
                    <div class="promise-icon">♥</div>
                    <h3>My Promise</h3>
                    <p>I promise to love you with all my heart, support your dreams, and create beautiful memories together for the rest of our lives.</p>
                </div>
                
                <div class="promise-card">
                    <div class="promise-icon">✓</div>
                    <h3>Our Future</h3>
                    <p>Together we'll build a life filled with love, laughter, adventure, and endless happiness. You're my forever, Kushina.</p>
                </div>
            </div>
            
            <div class="love-declaration">
                ♥ I Love You, Kushina ♥
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-item">
                    <div class="footer-icon">📅</div>
                    <p>Since Our Beginning</p>
                </div>
                
                <div class="footer-item">
                    <div class="footer-icon">♥</div>
                    <p>Forever & Always</p>
                </div>
                
                <div class="footer-item">
                    <div class="footer-icon">∞</div>
                    <p>Endless Love</p>
                </div>
            </div>
            
            <p style="border-top: 1px solid rgba(255,255,255,0.2); padding-top: 2rem; opacity: 0.8;">
                © 2024 Created with endless love for the most amazing woman in the world
            </p>
        </div>
    </footer>

    <script>
        // Smooth scrolling function
        function scrollToSection(sectionId) {
            const element = document.getElementById(sectionId);
            if (element) {
                element.scrollIntoView({ 
                    behavior: 'smooth',
                    block: 'start'
                });
            }
        }

        // Animate love cards on scroll
        function animateOnScroll() {
            const cards = document.querySelectorAll('.love-card');
            
            cards.forEach(card => {
                const rect = card.getBoundingClientRect();
                const windowHeight = window.innerHeight;
                
                if (rect.top < windowHeight - 100) {
                    card.classList.add('animate');
                }
            });
        }

        // Add scroll event listener
        window.addEventListener('scroll', animateOnScroll);

        // Initial animation check
        document.addEventListener('DOMContentLoaded', function() {
            animateOnScroll();
            
            // Add some random movement to hearts
            const hearts = document.querySelectorAll('.heart');
            hearts.forEach((heart, index) => {
                heart.style.animationDelay = `${index * 1.2}s`;
                heart.style.fontSize = `${Math.random() * 10 + 15}px`;
            });
        });

        // Add click effect to CTA button
        document.querySelector('.cta-button').addEventListener('click', function() {
            this.style.transform = 'scale(0.95)';
            setTimeout(() => {
                this.style.transform = 'scale(1)';
            }, 150);
        });

        // Add hover effect to gallery items
        document.querySelectorAll('.gallery-item').forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.transform = 'scale(1.05) rotate(1deg)';
            });
            
            item.addEventListener('mouseleave', function() {
                this.style.transform = 'scale(1) rotate(0deg)';
            });
        });

        // Add pulse animation to love declaration
        setInterval(function() {
            const declaration = document.querySelector('.love-declaration');
            declaration.style.transform = 'scale(1.02)';
            setTimeout(() => {
                declaration.style.transform = 'scale(1)';
            }, 200);
        }, 3000);
    </script>
</body>
</html>
