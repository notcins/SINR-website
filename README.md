<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SINR - Where Rebellion Meets Luxury</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700;900&family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
            background: linear-gradient(135deg, #ff6b9d, #c44569, #f8b500, #3742fa);
            background-size: 400% 400%;
            animation: gradientShift 15s ease infinite;
        }
        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        /* Navigation */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 15px 0;
            transition: all 0.3s ease;
            border-bottom: 3px solid #ff6b9d;
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
        }
        
        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            font-weight: 700;
            background: linear-gradient(45deg, #ff6b9d, #c44569, #f8b500);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: 2px;
        }
        
        .nav-menu {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        .nav-link {
            text-decoration: none;
            color: #ff6b9d;
            font-weight: 600;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
        }
        
        .nav-link:hover {
            color: #c44569;
            transform: translateY(-2px);
        }
        
        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(45deg, #ff6b9d, #c44569);
            transition: width 0.3s ease;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #ff6b9d, #c44569, #f8b500, #3742fa);
            background-size: 400% 400%;
            animation: gradientShift 10s ease infinite;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.2);
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: 0 20px;
        }
        
        .hero-title {
            font-family: 'Playfair Display', serif;
            font-size: 4.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            letter-spacing: 4px;
        }
        
        .hero-subtitle {
            font-size: 1.5rem;
            margin-bottom: 15px;
            opacity: 0.9;
        }
        
        .hero-tagline {
            font-size: 1rem;
            opacity: 0.8;
            letter-spacing: 2px;
            margin-bottom: 40px;
        }
        
        .cta-button {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            border: 2px solid white;
            padding: 15px 40px;
            font-size: 1rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            border-radius: 25px;
            backdrop-filter: blur(10px);
        }
        
        .cta-button:hover {
            background: white;
            color: #ff6b9d;
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 15px 30px rgba(255, 255, 255, 0.3);
        }
        
        /* Sections */
        .section {
            padding: 100px 0;
            display: none;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            margin: 20px;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }
        
        .section.active {
            display: block;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 60px;
            background: linear-gradient(45deg, #ff6b9d, #c44569, #f8b500);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        /* Collection Grid */
        .collection-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }
        
        .sin-card {
            background: linear-gradient(135deg, rgba(255, 107, 157, 0.1), rgba(196, 69, 105, 0.1), rgba(248, 181, 0, 0.1));
            border-radius: 20px;
            padding: 40px 30px;
            text-align: center;
            transition: all 0.3s ease;
            border: 2px solid transparent;
            background-clip: padding-box;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }
        
        .sin-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, #ff6b9d, #c44569, #f8b500);
            border-radius: 20px;
            padding: 2px;
            mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
            mask-composite: exclude;
            z-index: -1;
        }
        
        .sin-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 40px rgba(255, 107, 157, 0.3);
            background: linear-gradient(135deg, rgba(255, 107, 157, 0.2), rgba(196, 69, 105, 0.2), rgba(248, 181, 0, 0.2));
        }
        
        .sin-emoji {
            font-size: 4rem;
            margin-bottom: 20px;
            filter: drop-shadow(0 4px 8px rgba(255, 107, 157, 0.3));
        }
        
        .sin-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(45deg, #ff6b9d, #c44569);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 15px;
        }
        
        .sin-description {
            color: #666;
            font-size: 1rem;
            line-height: 1.6;
        }
        
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }
        
        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #666;
        }
        
        .about-text h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            background: linear-gradient(45deg, #ff6b9d, #c44569);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
        }
        
        .brand-story {
            background: linear-gradient(135deg, #ff6b9d, #c44569, #f8b500);
            color: white;
            padding: 40px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 15px 30px rgba(255, 107, 157, 0.3);
        }
        
        .brand-evolution {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            font-weight: 700;
            letter-spacing: 3px;
            margin-bottom: 20px;
        }
        
        /* Contact Section */
        .contact-content {
            max-width: 600px;
            margin: 0 auto;
            text-align: center;
        }
        
        .contact-form {
            display: grid;
            gap: 20px;
            margin-top: 40px;
        }
        
        .form-group {
            display: grid;
            gap: 8px;
        }
        
        .form-label {
            font-weight: 600;
            background: linear-gradient(45deg, #ff6b9d, #c44569);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-align: left;
        }
        
        .form-input,
        .form-textarea {
            padding: 15px;
            border: 2px solid #ff6b9d;
            border-radius: 10px;
            font-family: 'Inter', sans-serif;
            font-size: 1rem;
            transition: all 0.3s ease;
            background: rgba(255, 255, 255, 0.9);
        }
        
        .form-input:focus,
        .form-textarea:focus {
            outline: none;
            border-color: #c44569;
            box-shadow: 0 0 20px rgba(255, 107, 157, 0.3);
            transform: translateY(-2px);
        }
        
        .form-textarea {
            resize: vertical;
            min-height: 120px;
        }
        
        .submit-btn {
            background: linear-gradient(45deg, #ff6b9d, #c44569, #f8b500);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.3s ease;
            border-radius: 25px;
            box-shadow: 0 10px 20px rgba(255, 107, 157, 0.3);
        }
        
        .submit-btn:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 15px 30px rgba(255, 107, 157, 0.4);
        }
        
        /* Footer */
        .footer {
            background: linear-gradient(135deg, #ff6b9d, #c44569, #f8b500);
            color: white;
            text-align: center;
            padding: 40px 0;
            margin: 20px;
            border-radius: 20px;
            box-shadow: 0 15px 30px rgba(255, 107, 157, 0.3);
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .social-link {
            color: white;
            font-size: 1.5rem;
            transition: opacity 0.3s ease;
        }
        
        .social-link:hover {
            opacity: 0.7;
        }
        
        /* Mobile Menu */
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: #2c3e50;
            cursor: pointer;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            .nav-menu {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: white;
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            }
            
            .nav-menu.active {
                display: flex;
            }
            
            .hero-title {
                font-size: 3rem;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
            }
            
            .section-title {
                font-size: 2.5rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }
            
            .collection-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">SINR</div>
            <ul class="nav-menu" id="navMenu">
                <li><a href="#" class="nav-link" onclick="showSection('home')">Home</a></li>
                <li><a href="#" class="nav-link" onclick="showSection('collection')">Collection</a></li>
                <li><a href="#" class="nav-link" onclick="showSection('about')">About</a></li>
                <li><a href="#" class="nav-link" onclick="showSection('contact')">Contact</a></li>
            </ul>
            <button class="mobile-menu-btn" onclick="toggleMobileMenu()">☰</button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1 class="hero-title">SINR</h1>
            <p class="hero-subtitle">Where Rebellion Meets Luxury</p>
            <p class="hero-tagline">CINDY → CINS → SINR</p>
            <a href="#" class="cta-button" onclick="showSection('collection')">Explore Collection</a>
        </div>
    </section>

    <!-- Collection Section -->
    <section class="section" id="collection">
        <div class="container">
            <h2 class="section-title">The 7 Sins Collection</h2>
            <p style="text-align: center; font-size: 1.2rem; color: #666; margin-bottom: 60px;">
                Euro Summer meets Bratz energy. Mini skirts, crop tops, and capri pants designed for the unapologetically bold.
            </p>
            
            <div class="collection-grid">
                <div class="sin-card" onclick="showSinDetail('pride')">
                    <div class="sin-emoji">😈</div>
                    <h3 class="sin-title">Pride</h3>
                    <p class="sin-description">Confidence that commands attention. Bold silhouettes for those who own their power.</p>
                </div>
                
                <div class="sin-card" onclick="showSinDetail('lust')">
                    <div class="sin-emoji">💋</div>
                    <h3 class="sin-title">Lust</h3>
                    <p class="sin-description">Seductive elegance meets rebellious spirit. Pieces that whisper and shout simultaneously.</p>
                </div>
                
                <div class="sin-card" onclick="showSinDetail('wrath')">
                    <div class="sin-emoji">🔥</div>
                    <h3 class="sin-title">Wrath</h3>
                    <p class="sin-description">Fierce fashion for fierce souls. Channel your inner fire with statement pieces.</p>
                </div>
                
                <div class="sin-card" onclick="showSinDetail('greed')">
                    <div class="sin-emoji">💎</div>
                    <h3 class="sin-title">Greed</h3>
                    <p class="sin-description">Luxury you can't resist. Indulgent textures and premium details worth coveting.</p>
                </div>
                
                <div class="sin-card" onclick="showSinDetail('gluttony')">
                    <div class="sin-emoji">🍑</div>
                    <h3 class="sin-title">Gluttony</h3>
                    <p class="sin-description">More is more. Excessive beauty in every stitch, for those who refuse to settle.</p>
                </div>
                
                <div class="sin-card" onclick="showSinDetail('envy')">
                    <div class="sin-emoji">💚</div>
                    <h3 class="sin-title">Envy</h3>
                    <p class="sin-description">Be the one they envy. Pieces designed to turn heads and steal hearts.</p>
                </div>
                
                <div class="sin-card" onclick="showSinDetail('sloth')">
                    <div class="sin-emoji">😴</div>
                    <h3 class="sin-title">Sloth</h3>
                    <p class="sin-description">Effortless luxury. Looking flawless should never feel like work.</p>
                </div>
            </div>
            
            <div style="text-align: center;">
                <p style="font-size: 1.1rem; color: #666; margin-bottom: 30px;">Coming Soon: 7 pieces. 7 sins. Infinite attitude.</p>
                <div style="display: flex; justify-content: center; gap: 15px; flex-wrap: wrap;">
                    <span style="background: linear-gradient(45deg, #ff6b9d, #c44569); color: white; padding: 8px 16px; border-radius: 20px; font-size: 0.9rem; box-shadow: 0 5px 15px rgba(255, 107, 157, 0.3);">#SINR</span>
                    <span style="background: linear-gradient(45deg, #c44569, #f8b500); color: white; padding: 8px 16px; border-radius: 20px; font-size: 0.9rem; box-shadow: 0 5px 15px rgba(196, 69, 105, 0.3);">#7Sins</span>
                    <span style="background: linear-gradient(45deg, #f8b500, #3742fa); color: white; padding: 8px 16px; border-radius: 20px; font-size: 0.9rem; box-shadow: 0 5px 15px rgba(248, 181, 0, 0.3);">#EuroSummer</span>
                    <span style="background: linear-gradient(45deg, #3742fa, #ff6b9d); color: white; padding: 8px 16px; border-radius: 20px; font-size: 0.9rem; box-shadow: 0 5px 15px rgba(55, 66, 250, 0.3);">#BratzEnergy</span>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title">About SINR</h2>
            
            <div class="about-content">
                <div class="about-text">
                    <h3>The Story Behind the Name</h3>
                    <p>SINR began as Cindy – a name that evolved through rebellion and reinvention. From Cindy to Cins to SINR, each transformation represented a shedding of expectations and an embrace of authentic self-expression.</p>
                    
                    <p>We believe fashion should be fearless. Our pieces are designed for those who refuse to apologize for taking up space, for being seen, for being unapologetically themselves.</p>
                    
                    <p>Euro summer sophistication meets Bratz-inspired confidence. Every piece in our collection tells a story of rebellion, luxury, and the beautiful complexity of modern femininity.</p>
                </div>
                
                <div class="brand-story">
                    <div class="brand-evolution">CINDY → CINS → SINR</div>
                    <p>Evolution through rebellion.<br>Luxury through authenticity.<br>Fashion through fearlessness.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section" id="contact">
        <div class="container">
            <h2 class="section-title">Get in Touch</h2>
            
            <div class="contact-content">
                <p style="font-size: 1.1rem; color: #666; margin-bottom: 20px;">
                    Ready to embrace your sins? Have questions about our collection? We'd love to hear from you.
                </p>
                
                <form class="contact-form" onsubmit="handleSubmit(event)">
                    <div class="form-group">
                        <label class="form-label">Name</label>
                        <input type="text" class="form-input" required>
                    </div>
                    
                    <div class="form-group">
                        <label class="form-label">Email</label>
                        <input type="email" class="form-input" required>
                    </div>
                    
                    <div class="form-group">
                        <label class="form-label">Subject</label>
                        <input type="text" class="form-input" required>
                    </div>
                    
                    <div class="form-group">
                        <label class="form-label">Message</label>
                        <textarea class="form-textarea" required></textarea>
                    </div>
                    
                    <button type="submit" class="submit-btn">Send Message</button>
                </form>
                
                <p style="margin-top: 30px; color: #666; font-size: 0.9rem;">
                    <strong>Note:</strong> This is a demo contact form. In a live website, this would connect to a backend service to send emails.
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-content">
            <div class="social-links">
                <a href="#" class="social-link">📱</a>
                <a href="#" class="social-link">📧</a>
                <a href="#" class="social-link">🌐</a>
            </div>
            <p>&copy; 2024 SINR. Where rebellion meets luxury.</p>
        </div>
    </footer>

    <script>
        // Navigation functionality
        function showSection(sectionId) {
            // Hide all sections
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => section.classList.remove('active'));
            
            // Hide hero
            const hero = document.getElementById('home');
            hero.style.display = 'none';
            
            // Show selected section
            if (sectionId === 'home') {
                hero.style.display = 'flex';
            } else {
                const targetSection = document.getElementById(sectionId);
                if (targetSection) {
                    targetSection.classList.add('active');
                }
            }
            
            // Close mobile menu
            const navMenu = document.getElementById('navMenu');
            navMenu.classList.remove('active');
        }
        
        function toggleMobileMenu() {
            const navMenu = document.getElementById('navMenu');
            navMenu.classList.toggle('active');
        }
        
        function showSinDetail(sinName) {
            alert(`${sinName.charAt(0).toUpperCase() + sinName.slice(1)} collection coming soon! Stay tuned for the full reveal.`);
        }
        
        function handleSubmit(event) {
            event.preventDefault();
            alert('Thank you for your message! This is a demo form. In a live website, your message would be sent to SINR.');
        }
        
        // Smooth scrolling and navbar background
        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.style.background = 'rgba(255, 255, 255, 0.98)';
            } else {
                navbar.style.background = 'rgba(255, 255, 255, 0.95)';
            }
        });
        
        // Initialize - show home by default
        document.addEventListener('DOMContentLoaded', function() {
            showSection('home');
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'96bb6ab4954e45b7',t:'MTc1NDYxODM5Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
