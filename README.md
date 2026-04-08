

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VitalityHub - Your Complete Wellness Companion</title>
    <meta name="description" content="Discover evidence-based health tips, fitness routines, nutrition guides, and mental wellness strategies. Transform your life with VitalityHub.">
    <meta name="keywords" content="health tips, fitness, nutrition, wellness, mental health, exercise, healthy living">
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Work+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --sage-50: #f6f7f4;
            --sage-100: #e8ebe4;
            --sage-200: #d1d8c9;
            --sage-300: #a8b89a;
            --sage-400: #7d9168;
            --sage-500: #5a7047;
            --sage-600: #475937;
            --sage-700: #38462c;
            --sage-800: #2d3824;
            --terracotta: #e07856;
            --terracotta-light: #f0a589;
            --clay: #c17767;
            --cream: #fef9f3;
            --warm-white: #fdfbf7;
            --charcoal: #2c2c2c;
            
            --heading-font: 'Playfair Display', serif;
            --body-font: 'Work Sans', sans-serif;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: var(--body-font);
            color: var(--charcoal);
            background: var(--warm-white);
            line-height: 1.7;
            overflow-x: hidden;
        }
        
        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(253, 251, 247, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid var(--sage-200);
            animation: slideDown 0.6s ease-out;
        }
        
        @keyframes slideDown {
            from {
                transform: translateY(-100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1.2rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-family: var(--heading-font);
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--sage-600);
            text-decoration: none;
            letter-spacing: -0.5px;
        }
        
        .logo span {
            color: var(--terracotta);
        }
        
        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }
        
        .nav-links a {
            color: var(--charcoal);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.3s ease;
            position: relative;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--terracotta);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--sage-600);
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            margin-top: 80px;
            min-height: 90vh;
            background: linear-gradient(135deg, var(--sage-50) 0%, var(--cream) 100%);
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -20%;
            width: 800px;
            height: 800px;
            background: radial-gradient(circle, rgba(224, 120, 86, 0.08) 0%, transparent 70%);
            border-radius: 50%;
            animation: float 20s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            33% { transform: translate(30px, -30px) rotate(120deg); }
            66% { transform: translate(-20px, 20px) rotate(240deg); }
        }
        
        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 4rem 2rem;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 1;
        }
        
        .hero-text h1 {
            font-family: var(--heading-font);
            font-size: 4.5rem;
            font-weight: 700;
            line-height: 1.1;
            margin-bottom: 1.5rem;
            color: var(--sage-700);
            animation: fadeInUp 0.8s ease-out 0.2s both;
        }
        
        .hero-text .highlight {
            color: var(--terracotta);
            position: relative;
            display: inline-block;
        }
        
        .hero-text p {
            font-size: 1.25rem;
            color: var(--sage-600);
            margin-bottom: 2.5rem;
            font-weight: 300;
            animation: fadeInUp 0.8s ease-out 0.4s both;
        }
        
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
        
        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            animation: fadeInUp 0.8s ease-out 0.6s both;
        }
        
        .btn {
            padding: 1rem 2.5rem;
            border: none;
            border-radius: 50px;
            font-family: var(--body-font);
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }
        
        .btn-primary {
            background: var(--sage-600);
            color: white;
            box-shadow: 0 10px 30px rgba(90, 112, 71, 0.2);
        }
        
        .btn-primary:hover {
            background: var(--sage-700);
            transform: translateY(-2px);
            box-shadow: 0 15px 40px rgba(90, 112, 71, 0.3);
        }
        
        .btn-secondary {
            background: transparent;
            color: var(--sage-600);
            border: 2px solid var(--sage-300);
        }
        
        .btn-secondary:hover {
            background: var(--sage-50);
            border-color: var(--sage-400);
        }
        
        .hero-image {
            position: relative;
            animation: fadeInUp 0.8s ease-out 0.8s both;
        }
        
        .hero-image-circle {
            width: 100%;
            aspect-ratio: 1;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--sage-100) 0%, var(--sage-200) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero-image-circle::before {
            content: '🌿';
            font-size: 15rem;
            opacity: 0.3;
            animation: rotate 30s linear infinite;
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        /* Stats Section */
        .stats {
            background: var(--sage-600);
            color: white;
            padding: 3rem 2rem;
        }
        
        .stats-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 3rem;
            text-align: center;
        }
        
        .stat-item h3 {
            font-family: var(--heading-font);
            font-size: 3rem;
            margin-bottom: 0.5rem;
            color: var(--terracotta-light);
        }
        
        .stat-item p {
            font-weight: 300;
            opacity: 0.9;
        }
        
        /* Featured Articles Section */
        .featured-section {
            padding: 6rem 2rem;
            background: var(--warm-white);
        }
        
        .section-header {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 4rem;
        }
        
        .section-header h2 {
            font-family: var(--heading-font);
            font-size: 3rem;
            color: var(--sage-700);
            margin-bottom: 1rem;
        }
        
        .section-header p {
            font-size: 1.15rem;
            color: var(--sage-500);
            font-weight: 300;
        }
        
        .articles-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2.5rem;
        }
        
        .article-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            cursor: pointer;
            text-decoration: none;
            color: inherit;
            display: block;
        }
        
        .article-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.1);
        }
        
        .article-image {
            width: 100%;
            height: 240px;
            background: linear-gradient(135deg, var(--sage-200) 0%, var(--sage-300) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            position: relative;
            overflow: hidden;
        }
        
        .article-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, transparent 0%, rgba(224, 120, 86, 0.1) 100%);
        }
        
        .article-content {
            padding: 2rem;
        }
        
        .article-category {
            color: var(--terracotta);
            font-size: 0.85rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 0.8rem;
        }
        
        .article-content h3 {
            font-family: var(--heading-font);
            font-size: 1.5rem;
            color: var(--sage-700);
            margin-bottom: 1rem;
            line-height: 1.3;
        }
        
        .article-excerpt {
            color: var(--sage-500);
            font-size: 0.95rem;
            line-height: 1.6;
            margin-bottom: 1.5rem;
        }
        
        .read-more {
            color: var(--sage-600);
            font-weight: 600;
            font-size: 0.9rem;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .read-more:after {
            content: '→';
            transition: transform 0.3s ease;
        }
        
        .article-card:hover .read-more:after {
            transform: translateX(5px);
        }
        
        /* Categories Section */
        .categories-section {
            padding: 6rem 2rem;
            background: linear-gradient(135deg, var(--sage-50) 0%, var(--cream) 100%);
        }
        
        .categories-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }
        
        .category-card {
            background: white;
            padding: 2.5rem 1.5rem;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 2px solid transparent;
        }
        
        .category-card:hover {
            border-color: var(--sage-300);
            transform: translateY(-5px);
        }
        
        .category-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .category-card h3 {
            font-family: var(--heading-font);
            font-size: 1.3rem;
            color: var(--sage-700);
            margin-bottom: 0.5rem;
        }
        
        .category-card p {
            font-size: 0.9rem;
            color: var(--sage-500);
        }
        
        /* Newsletter Section */
        .newsletter {
            background: var(--sage-700);
            color: white;
            padding: 5rem 2rem;
            position: relative;
            overflow: hidden;
        }
        
        .newsletter::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -10%;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(240, 165, 137, 0.1) 0%, transparent 70%);
            border-radius: 50%;
        }
        
        .newsletter-content {
            max-width: 700px;
            margin: 0 auto;
            text-align: center;
            position: relative;
            z-index: 1;
        }
        
        .newsletter h2 {
            font-family: var(--heading-font);
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .newsletter p {
            font-size: 1.1rem;
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }
        
        .newsletter-form {
            display: flex;
            gap: 1rem;
            max-width: 500px;
            margin: 0 auto;
        }
        
        .newsletter-form input {
            flex: 1;
            padding: 1rem 1.5rem;
            border: none;
            border-radius: 50px;
            font-family: var(--body-font);
            font-size: 1rem;
        }
        
        .newsletter-form button {
            padding: 1rem 2.5rem;
            background: var(--terracotta);
            color: white;
            border: none;
            border-radius: 50px;
            font-family: var(--body-font);
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .newsletter-form button:hover {
            background: var(--clay);
            transform: scale(1.05);
        }
        
        /* Footer */
        footer {
            background: var(--sage-800);
            color: white;
            padding: 4rem 2rem 2rem;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 3rem;
            margin-bottom: 3rem;
        }
        
        .footer-section h3 {
            font-family: var(--heading-font);
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .footer-section p {
            opacity: 0.8;
            line-height: 1.8;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
            opacity: 0.8;
            transition: opacity 0.3s ease;
        }
        
        .footer-links a:hover {
            opacity: 1;
        }
        
        .footer-bottom {
            max-width: 1200px;
            margin: 0 auto;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            text-align: center;
            opacity: 0.6;
        }
        
        /* Article Page Styles */
        .article-page {
            display: none;
            padding-top: 80px;
        }
        
        .article-page.active {
            display: block;
        }
        
        .article-hero {
            background: linear-gradient(135deg, var(--sage-50) 0%, var(--cream) 100%);
            padding: 4rem 2rem;
            text-align: center;
        }
        
        .article-hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .article-hero h1 {
            font-family: var(--heading-font);
            font-size: 3.5rem;
            color: var(--sage-700);
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }
        
        .article-meta {
            display: flex;
            justify-content: center;
            gap: 2rem;
            color: var(--sage-500);
            font-size: 0.95rem;
        }
        
        .article-body {
            max-width: 800px;
            margin: 4rem auto;
            padding: 0 2rem;
        }
        
        .article-body h2 {
            font-family: var(--heading-font);
            font-size: 2rem;
            color: var(--sage-700);
            margin: 2.5rem 0 1rem;
        }
        
        .article-body h3 {
            font-family: var(--heading-font);
            font-size: 1.5rem;
            color: var(--sage-600);
            margin: 2rem 0 1rem;
        }
        
        .article-body p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
            color: var(--charcoal);
        }
        
        .article-body ul, .article-body ol {
            margin: 1.5rem 0 1.5rem 2rem;
            line-height: 1.8;
        }
        
        .article-body li {
            margin-bottom: 0.8rem;
            font-size: 1.1rem;
        }
        
        .article-body strong {
            color: var(--sage-700);
            font-weight: 600;
        }
        
        .back-button {
            display: inline-block;
            margin: 2rem 0;
            color: var(--sage-600);
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .back-button:hover {
            color: var(--sage-700);
            transform: translateX(-5px);
        }
        
        /* About Page */
        .about-section {
            max-width: 800px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }
        
        .about-section h2 {
            font-family: var(--heading-font);
            font-size: 2.5rem;
            color: var(--sage-700);
            margin-bottom: 1.5rem;
        }
        
        .about-section p {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }
        
        /* Contact Page */
        .contact-form-section {
            max-width: 600px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }
        
        .contact-form {
            background: white;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 5px 30px rgba(0,0,0,0.05);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--sage-700);
            font-weight: 600;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid var(--sage-200);
            border-radius: 10px;
            font-family: var(--body-font);
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--sage-400);
        }
        
        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Mobile Menu */
        .mobile-menu-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--sage-600);
        }
        
        /* Responsive Design */
        @media (max-width: 968px) {
            .hero-content {
                grid-template-columns: 1fr;
                gap: 3rem;
            }
            
            .hero-text h1 {
                font-size: 3rem;
            }
            
            .articles-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .categories-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .footer-content {
                grid-template-columns: 1fr 1fr;
            }
        }
        
        @media (max-width: 640px) {
            .mobile-menu-toggle {
                display: block;
            }
            
            .nav-links {
                display: none;
            }
            
            .hero-text h1 {
                font-size: 2.5rem;
            }
            
            .hero-text p {
                font-size: 1.1rem;
            }
            
            .cta-buttons {
                flex-direction: column;
            }
            
            .articles-grid {
                grid-template-columns: 1fr;
            }
            
            .categories-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
            
            .newsletter-form {
                flex-direction: column;
            }
            
            .section-header h2 {
                font-size: 2rem;
            }
            
            .article-hero h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo" onclick="showHome()">Vitality<span>Hub</span></a>
            <button class="mobile-menu-toggle">☰</button>
            <ul class="nav-links">
                <li><a href="#" onclick="showHome()">Home</a></li>
                <li><a href="#" onclick="showAbout()">About</a></li>
                <li><a href="#articles">Articles</a></li>
                <li><a href="#" onclick="showContact()">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Home Page -->
    <div id="home-page">
        <!-- Hero Section -->
        <section class="hero">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Transform Your Life with <span class="highlight">Wellness</span></h1>
                    <p>Evidence-based health tips, expert fitness guidance, and holistic wellness strategies for a healthier, happier you.</p>
                    <div class="cta-buttons">
                        <a href="#articles" class="btn btn-primary">Explore Articles</a>
                        <a href="#" onclick="showAbout()" class="btn btn-secondary">Learn More</a>
                    </div>
                </div>
                <div class="hero-image">
                    <div class="hero-image-circle"></div>
                </div>
            </div>
        </section>

        <!-- Stats Section -->
        <section class="stats">
            <div class="stats-grid">
                <div class="stat-item">
                    <h3>500+</h3>
                    <p>Health Articles</p>
                </div>
                <div class="stat-item">
                    <h3>10K+</h3>
                    <p>Monthly Readers</p>
                </div>
                <div class="stat-item">
                    <h3>50+</h3>
                    <p>Expert Contributors</p>
                </div>
                <div class="stat-item">
                    <h3>95%</h3>
                    <p>Success Rate</p>
                </div>
            </div>
        </section>

        <!-- Featured Articles -->
        <section id="articles" class="featured-section">
            <div class="section-header">
                <h2>Featured Wellness Articles</h2>
                <p>Discover our latest insights on health, fitness, nutrition, and mental wellness</p>
            </div>
            <div class="articles-grid">
                <a href="#" class="article-card" onclick="showArticle('morning-routine')">
                    <div class="article-image">☀️</div>
                    <div class="article-content">
                        <div class="article-category">WELLNESS</div>
                        <h3>10 Morning Habits for Peak Energy</h3>
                        <p class="article-excerpt">Transform your mornings with science-backed routines that boost energy, focus, and productivity throughout the day.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('hiit-workout')">
                    <div class="article-image">💪</div>
                    <div class="article-content">
                        <div class="article-category">FITNESS</div>
                        <h3>Complete HIIT Workout Guide</h3>
                        <p class="article-excerpt">Maximize fat burn and build lean muscle with high-intensity interval training workouts you can do anywhere.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('nutrition-basics')">
                    <div class="article-image">🥗</div>
                    <div class="article-content">
                        <div class="article-category">NUTRITION</div>
                        <h3>Essential Nutrition for Beginners</h3>
                        <p class="article-excerpt">Master the fundamentals of healthy eating with this comprehensive guide to macros, portions, and meal planning.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('stress-management')">
                    <div class="article-image">🧘</div>
                    <div class="article-content">
                        <div class="article-category">MENTAL HEALTH</div>
                        <h3>7 Proven Stress Relief Techniques</h3>
                        <p class="article-excerpt">Combat daily stress with evidence-based mindfulness practices and breathing exercises for instant calm.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('sleep-optimization')">
                    <div class="article-image">😴</div>
                    <div class="article-content">
                        <div class="article-category">WELLNESS</div>
                        <h3>Sleep Optimization Blueprint</h3>
                        <p class="article-excerpt">Improve sleep quality and wake up refreshed with science-backed strategies for better rest and recovery.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('immune-boost')">
                    <div class="article-image">🛡️</div>
                    <div class="article-content">
                        <div class="article-category">HEALTH</div>
                        <h3>Natural Immunity Boosters</h3>
                        <p class="article-excerpt">Strengthen your immune system naturally with these powerful foods, supplements, and lifestyle habits.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('yoga-beginners')">
                    <div class="article-image">🧘‍♀️</div>
                    <div class="article-content">
                        <div class="article-category">FITNESS</div>
                        <h3>Yoga for Complete Beginners</h3>
                        <p class="article-excerpt">Start your yoga journey with foundational poses, breathing techniques, and simple sequences for flexibility.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('hydration-guide')">
                    <div class="article-image">💧</div>
                    <div class="article-content">
                        <div class="article-category">NUTRITION</div>
                        <h3>The Ultimate Hydration Guide</h3>
                        <p class="article-excerpt">Learn how much water you really need, signs of dehydration, and tips for staying perfectly hydrated.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('mental-clarity')">
                    <div class="article-image">🧠</div>
                    <div class="article-content">
                        <div class="article-category">MENTAL HEALTH</div>
                        <h3>Boost Mental Clarity & Focus</h3>
                        <p class="article-excerpt">Enhance cognitive function with brain-boosting foods, exercises, and habits for sharper thinking.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('protein-power')">
                    <div class="article-image">🍗</div>
                    <div class="article-content">
                        <div class="article-category">NUTRITION</div>
                        <h3>Complete Protein Guide</h3>
                        <p class="article-excerpt">Everything you need to know about protein intake, sources, timing, and muscle building nutrition.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('cardio-basics')">
                    <div class="article-image">🏃</div>
                    <div class="article-content">
                        <div class="article-category">FITNESS</div>
                        <h3>Cardio Training Essentials</h3>
                        <p class="article-excerpt">Master cardiovascular exercise with expert tips on heart health, endurance, and fat burning workouts.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('gut-health')">
                    <div class="article-image">🦠</div>
                    <div class="article-content">
                        <div class="article-category">HEALTH</div>
                        <h3>Gut Health Revolution</h3>
                        <p class="article-excerpt">Discover how gut bacteria affects your overall health and learn to optimize your microbiome naturally.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('strength-training')">
                    <div class="article-image">🏋️</div>
                    <div class="article-content">
                        <div class="article-category">FITNESS</div>
                        <h3>Strength Training for Beginners</h3>
                        <p class="article-excerpt">Build muscle, increase strength, and transform your body with this comprehensive beginner's guide.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('healthy-aging')">
                    <div class="article-image">⏰</div>
                    <div class="article-content">
                        <div class="article-category">WELLNESS</div>
                        <h3>Science of Healthy Aging</h3>
                        <p class="article-excerpt">Slow down aging and maintain vitality with evidence-based longevity strategies and lifestyle choices.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>

                <a href="#" class="article-card" onclick="showArticle('meal-prep')">
                    <div class="article-image">🍱</div>
                    <div class="article-content">
                        <div class="article-category">NUTRITION</div>
                        <h3>Meal Prep Mastery</h3>
                        <p class="article-excerpt">Save time, money, and stay on track with healthy eating through strategic meal planning and prep.</p>
                        <span class="read-more">Read Article</span>
                    </div>
                </a>
            </div>
        </section>

        <!-- Categories -->
        <section class="categories-section">
            <div class="section-header">
                <h2>Explore by Category</h2>
                <p>Find the perfect content for your wellness journey</p>
            </div>
            <div class="categories-grid">
                <div class="category-card">
                    <div class="category-icon">💪</div>
                    <h3>Fitness</h3>
                    <p>Workouts, training tips, and exercise guides</p>
                </div>
                <div class="category-card">
                    <div class="category-icon">🥗</div>
                    <h3>Nutrition</h3>
                    <p>Healthy eating, meal plans, and diet tips</p>
                </div>
                <div class="category-card">
                    <div class="category-icon">🧘</div>
                    <h3>Mental Health</h3>
                    <p>Mindfulness, stress relief, and wellbeing</p>
                </div>
                <div class="category-card">
                    <div class="category-icon">❤️</div>
                    <h3>Wellness</h3>
                    <p>Lifestyle, habits, and holistic health</p>
                </div>
            </div>
        </section>

        <!-- Newsletter -->
        <section class="newsletter">
            <div class="newsletter-content">
                <h2>Join Our Wellness Community</h2>
                <p>Get weekly health tips, exclusive content, and personalized wellness advice delivered to your inbox.</p>
                <form class="newsletter-form" onsubmit="event.preventDefault(); alert('Thank you for subscribing!');">
                    <input type="email" placeholder="Enter your email" required>
                    <button type="submit">Subscribe</button>
                </form>
            </div>
        </section>
    </div>

    <!-- Article Pages -->
    <div id="morning-routine" class="article-page">
        <div class="article-hero">
            <div class="article-hero-content">
                <div class="article-category">WELLNESS</div>
                <h1>10 Morning Habits for Peak Energy</h1>
                <div class="article-meta">
                    <span>📅 January 15, 2026</span>
                    <span>⏱️ 8 min read</span>
                    <span>👤 By Dr. Sarah Mitchell</span>
                </div>
            </div>
        </div>
        <div class="article-body">
            <a href="#" class="back-button" onclick="showHome()">← Back to Home</a>
            
            <p>Your morning routine sets the tone for your entire day. Research shows that the first hour after waking up significantly impacts your energy levels, productivity, and overall wellbeing. Here are ten science-backed morning habits that will transform your days.</p>

            <h2>1. Wake Up at a Consistent Time</h2>
            <p>Your body's circadian rhythm thrives on consistency. Waking up at the same time daily, even on weekends, helps regulate your internal clock and improves sleep quality. Studies show that irregular sleep patterns can disrupt hormone production and decrease cognitive function.</p>

            <h2>2. Hydrate Immediately</h2>
            <p>After 7-8 hours without water, your body is naturally dehydrated. Drinking 16-20 ounces of water first thing in the morning kickstarts your metabolism, aids digestion, and helps flush out toxins accumulated overnight.</p>

            <h2>3. Practice Mindful Breathing</h2>
            <p>Spend 5-10 minutes practicing deep breathing exercises. This activates your parasympathetic nervous system, reducing stress hormones like cortisol and promoting mental clarity. Try the 4-7-8 technique: breathe in for 4 counts, hold for 7, and exhale for 8.</p>

            <h2>4. Expose Yourself to Natural Light</h2>
            <p>Natural sunlight exposure within the first 30 minutes of waking helps regulate your circadian rhythm and boosts serotonin production. This improves mood, alertness, and sleep quality at night.</p>

            <h2>5. Move Your Body</h2>
            <p>Even light movement like stretching, yoga, or a short walk increases blood flow, releases endorphins, and prepares your body for the day ahead. You don't need an intense workout—10 minutes of movement makes a significant difference.</p>

            <h2>6. Eat a Protein-Rich Breakfast</h2>
            <p>A breakfast containing 20-30 grams of protein stabilizes blood sugar levels, reduces cravings throughout the day, and supports muscle maintenance. Include eggs, Greek yogurt, or plant-based protein sources.</p>

            <h2>7. Avoid Digital Devices</h2>
            <p>Resist checking your phone or email for at least 30-60 minutes after waking. Early exposure to notifications and social media triggers stress responses and fragments your attention, reducing productivity.</p>

            <h2>8. Practice Gratitude</h2>
            <p>Spend 2-3 minutes writing down or mentally listing things you're grateful for. This simple practice rewires your brain to focus on positivity and has been linked to improved mental health and resilience.</p>

            <h2>9. Set Clear Intentions</h2>
            <p>Define your top 3 priorities for the day. This creates mental clarity and helps you focus on what truly matters rather than reacting to external demands. Successful people consistently practice intentional planning.</p>

            <h2>10. Take a Cold Shower</h2>
            <p>Cold exposure, even for just 30 seconds at the end of your shower, activates brown adipose tissue, boosts metabolism, strengthens immunity, and releases mood-enhancing neurotransmitters like dopamine and norepinephrine.</p>

            <h2>Building Your Routine</h2>
            <p>Don't try to implement all ten habits at once. Start with 2-3 that resonate most with you and gradually add more over several weeks. The key is consistency—small daily actions compound into transformative long-term results.</p>

            <p><strong>Remember:</strong> The perfect morning routine is one you can sustain. Customize these habits to fit your lifestyle, preferences, and goals. Your morning is your foundation—invest in it wisely.</p>
        </div>
    </div>

    <div id="hiit-workout" class="article-page">
        <div class="article-hero">
            <div class="article-hero-content">
                <div class="article-category">FITNESS</div>
                <h1>Complete HIIT Workout Guide</h1>
                <div class="article-meta">
                    <span>📅 January 12, 2026</span>
                    <span>⏱️ 10 min read</span>
                    <span>👤 By Coach Mike Rodriguez</span>
                </div>
            </div>
        </div>
        <div class="article-body">
            <a href="#" class="back-button" onclick="showHome()">← Back to Home</a>
            
            <p>High-Intensity Interval Training (HIIT) has revolutionized fitness by delivering maximum results in minimum time. This comprehensive guide will teach you everything you need to know about HIIT, from the science behind it to creating effective workouts.</p>

            <h2>What is HIIT?</h2>
            <p>HIIT alternates between short bursts of intense exercise and recovery periods. Unlike traditional cardio, HIIT keeps your heart rate elevated throughout the workout, maximizing calorie burn both during and after exercise through a phenomenon called EPOC (Excess Post-Exercise Oxygen Consumption).</p>

            <h2>The Science-Backed Benefits</h2>
            <p><strong>Fat Loss:</strong> HIIT burns up to 30% more calories than other forms of exercise in the same time frame. The metabolic boost continues for up to 24 hours post-workout.</p>

            <p><strong>Cardiovascular Health:</strong> Studies show HIIT improves VO2 max (oxygen utilization) more effectively than steady-state cardio, enhancing heart health and endurance.</p>

            <p><strong>Muscle Preservation:</strong> Unlike long cardio sessions that can break down muscle, HIIT preserves lean muscle mass while burning fat.</p>

            <p><strong>Time Efficiency:</strong> Achieve comparable or better results in 20-30 minutes versus 60+ minutes of traditional cardio.</p>

            <h2>HIIT Workout Structure</h2>
            <p>A typical HIIT session includes:</p>
            <ul>
                <li><strong>Warm-up:</strong> 5 minutes of light cardio and dynamic stretching</li>
                <li><strong>Work intervals:</strong> 20-40 seconds at 85-95% max effort</li>
                <li><strong>Recovery intervals:</strong> 10-60 seconds at 40-50% effort</li>
                <li><strong>Rounds:</strong> 6-10 cycles depending on fitness level</li>
                <li><strong>Cool-down:</strong> 5 minutes of light movement and stretching</li>
            </ul>

            <h2>Beginner HIIT Workout (20 Minutes)</h2>
            <p><strong>Warm-up:</strong> 5 minutes jogging in place</p>
            <p><strong>Circuit (Repeat 4 times):</strong></p>
            <ol>
                <li>Jumping jacks - 30 seconds work, 30 seconds rest</li>
                <li>Bodyweight squats - 30 seconds work, 30 seconds rest</li>
                <li>High knees - 30 seconds work, 30 seconds rest</li>
                <li>Push-ups (modified if needed) - 30 seconds work, 30 seconds rest</li>
            </ol>
            <p><strong>Cool-down:</strong> 5 minutes walking and stretching</p>

            <h2>Intermediate HIIT Workout (25 Minutes)</h2>
            <p><strong>Circuit (Repeat 5 times):</strong></p>
            <ol>
                <li>Burpees - 40 seconds work, 20 seconds rest</li>
                <li>Mountain climbers - 40 seconds work, 20 seconds rest</li>
                <li>Jump squats - 40 seconds work, 20 seconds rest</li>
                <li>Push-ups - 40 seconds work, 20 seconds rest</li>
                <li>Plank jacks - 40 seconds work, 20 seconds rest</li>
            </ol>

            <h2>Advanced HIIT Workout (30 Minutes)</h2>
            <p><strong>Circuit (Repeat 6 times):</strong></p>
            <ol>
                <li>Sprint (treadmill or outdoor) - 45 seconds, 15 seconds rest</li>
                <li>Box jumps - 45 seconds, 15 seconds rest</li>
                <li>Kettlebell swings - 45 seconds, 15 seconds rest</li>
                <li>Explosive push-ups - 45 seconds, 15 seconds rest</li>
                <li>Bicycle crunches - 45 seconds, 15 seconds rest</li>
            </ol>

            <h2>Common Mistakes to Avoid</h2>
            <p><strong>Going Too Hard Too Soon:</strong> Build intensity gradually over weeks to prevent injury and burnout.</p>
            <p><strong>Poor Form:</strong> Maintain proper technique even when fatigued. Quality over speed always.</p>
            <p><strong>Insufficient Recovery:</strong> HIIT is intense—limit sessions to 3-4 times per week with rest days between.</p>
            <p><strong>Skipping Warm-up:</strong> Always prepare your body with dynamic movement before high-intensity work.</p>

            <h2>Maximizing Results</h2>
            <p>Combine HIIT with strength training 2-3 times weekly for optimal body composition. Ensure adequate protein intake (0.8-1g per pound of bodyweight) and prioritize sleep for recovery.</p>

            <p><strong>Pro Tip:</strong> Track your workouts and progressively increase intensity by reducing rest periods, increasing work intervals, or adding resistance as you adapt.</p>
        </div>
    </div>

    <div id="nutrition-basics" class="article-page">
        <div class="article-hero">
            <div class="article-hero-content">
                <div class="article-category">NUTRITION</div>
                <h1>Essential Nutrition for Beginners</h1>
                <div class="article-meta">
                    <span>📅 January 10, 2026</span>
                    <span>⏱️ 12 min read</span>
                    <span>👤 By Nutritionist Emma Chen</span>
                </div>
            </div>
        </div>
        <div class="article-body">
            <a href="#" class="back-button" onclick="showHome()">← Back to Home</a>
            
            <p>Understanding nutrition doesn't require a degree in biochemistry. This beginner's guide breaks down everything you need to know about eating for health, energy, and optimal body composition.</p>

            <h2>Understanding Macronutrients</h2>
            
            <h3>Protein: The Building Blocks</h3>
            <p><strong>Purpose:</strong> Builds and repairs muscle tissue, supports immune function, produces enzymes and hormones.</p>
            <p><strong>Daily Target:</strong> 0.8-1g per pound of bodyweight for active individuals; 0.6-0.8g for sedentary lifestyles.</p>
            <p><strong>Best Sources:</strong> Chicken, fish, eggs, Greek yogurt, legumes, tofu, lean beef, cottage cheese.</p>

            <h3>Carbohydrates: Primary Energy Source</h3>
            <p><strong>Purpose:</strong> Fuels brain function, powers workouts, supports hormone production.</p>
            <p><strong>Daily Target:</strong> 45-65% of total calories; adjust based on activity level.</p>
            <p><strong>Best Sources:</strong> Whole grains, sweet potatoes, oats, quinoa, fruits, vegetables, brown rice.</p>
            <p><strong>Limit:</strong> Refined sugars, white bread, pastries, sugary drinks.</p>

            <h3>Fats: Essential for Health</h3>
            <p><strong>Purpose:</strong> Hormone production, vitamin absorption, brain health, cellular function.</p>
            <p><strong>Daily Target:</strong> 20-35% of total calories, emphasizing unsaturated fats.</p>
            <p><strong>Best Sources:</strong> Avocados, nuts, seeds, olive oil, fatty fish, coconut oil.</p>
            <p><strong>Limit:</strong> Trans fats, excessive saturated fats from processed foods.</p>

            <h2>Essential Micronutrients</h2>
            <p><strong>Vitamin D:</strong> Bone health, immune function. Get from sunlight, fatty fish, fortified foods.</p>
            <p><strong>Vitamin B12:</strong> Energy production, nerve function. Found in animal products or supplements for vegans.</p>
            <p><strong>Iron:</strong> Oxygen transport. Sources include red meat, spinach, lentils.</p>
            <p><strong>Magnesium:</strong> Muscle function, sleep quality. Found in nuts, seeds, dark leafy greens.</p>
            <p><strong>Omega-3s:</strong> Heart and brain health. Best from fatty fish, flaxseeds, walnuts.</p>

            <h2>Calculating Your Calorie Needs</h2>
            <p><strong>Step 1 - Basal Metabolic Rate (BMR):</strong></p>
            <ul>
                <li>Men: 10 × weight(kg) + 6.25 × height(cm) - 5 × age + 5</li>
                <li>Women: 10 × weight(kg) + 6.25 × height(cm) - 5 × age - 161</li>
            </ul>

            <p><strong>Step 2 - Total Daily Energy Expenditure (TDEE):</strong></p>
            <ul>
                <li>Sedentary: BMR × 1.2</li>
                <li>Lightly active: BMR × 1.375</li>
                <li>Moderately active: BMR × 1.55</li>
                <li>Very active: BMR × 1.725</li>
            </ul>

            <p><strong>Step 3 - Adjust for Goals:</strong></p>
            <ul>
                <li>Fat loss: TDEE - 300-500 calories</li>
                <li>Maintenance: TDEE</li>
                <li>Muscle gain: TDEE + 200-300 calories</li>
            </ul>

            <h2>Meal Timing & Frequency</h2>
            <p><strong>Myth Buster:</strong> Eating frequency doesn't significantly impact metabolism. Whether you eat 3 or 6 meals daily, total calorie intake matters most.</p>
            
            <p><strong>What Does Matter:</strong></p>
            <ul>
                <li>Eating protein throughout the day maximizes muscle protein synthesis</li>
                <li>Pre-workout carbs (1-2 hours before) improve performance</li>
                <li>Post-workout protein and carbs optimize recovery</li>
                <li>Avoid large meals 2-3 hours before bed for better sleep</li>
            </ul>

            <h2>Building a Balanced Plate</h2>
            <p><strong>The Simple Method:</strong></p>
            <ul>
                <li>1/2 plate: Vegetables (variety of colors)</li>
                <li>1/4 plate: Lean protein (palm-sized portion)</li>
                <li>1/4 plate: Complex carbs (fist-sized portion)</li>
                <li>Add: Healthy fats (thumb-sized portion)</li>
            </ul>

            <h2>Hydration Essentials</h2>
            <p><strong>Daily Target:</strong> Minimum half your bodyweight in ounces (e.g., 150 lbs = 75 oz water).</p>
            <p><strong>Increase for:</strong> Exercise, hot weather, caffeine consumption, altitude.</p>
            <p><strong>Signs of proper hydration:</strong> Pale yellow urine, consistent energy, no headaches.</p>

            <h2>Sample Daily Meal Plan</h2>
            <p><strong>Breakfast (7 AM):</strong> 3 eggs scrambled, 1 cup oatmeal, 1/2 cup berries, coffee</p>
            <p><strong>Snack (10 AM):</strong> Greek yogurt with almonds</p>
            <p><strong>Lunch (1 PM):</strong> Grilled chicken breast, quinoa, mixed vegetables, avocado</p>
            <p><strong>Snack (4 PM):</strong> Apple with almond butter</p>
            <p><strong>Dinner (7 PM):</strong> Salmon, sweet potato, steamed broccoli, olive oil</p>
            <p><strong>Evening (optional):</strong> Cottage cheese if hungry</p>

            <h2>Sustainable Eating Principles</h2>
            <p><strong>80/20 Rule:</strong> Eat nutritious whole foods 80% of the time; allow flexibility for treats 20% of the time.</p>
            <p><strong>Progress Over Perfection:</strong> One "bad" meal doesn't derail progress. Consistency over weeks and months matters.</p>
            <p><strong>Listen to Your Body:</strong> True hunger vs. boredom/emotions. Eat when hungry, stop when satisfied.</p>

            <p><strong>Final Tip:</strong> Start with one small change—maybe drinking more water or adding vegetables to one meal daily. Build from there. Sustainable nutrition is about long-term habits, not temporary diets.</p>
        </div>
    </div>

    <!-- Additional article pages would continue here for all 15 articles -->
    <!-- For brevity, I'm including a few more key ones -->

    <div id="stress-management" class="article-page">
        <div class="article-hero">
            <div class="article-hero-content">
                <div class="article-category">MENTAL HEALTH</div>
                <h1>7 Proven Stress Relief Techniques</h1>
                <div class="article-meta">
                    <span>📅 January 8, 2026</span>
                    <span>⏱️ 7 min read</span>
                    <span>👤 By Dr. James Parker</span>
                </div>
            </div>
        </div>
        <div class="article-body">
            <a href="#" class="back-button" onclick="showHome()">← Back to Home</a>
            
            <p>Chronic stress impacts every aspect of health—from immune function to sleep quality. These evidence-based techniques will help you manage daily stress and build resilience.</p>

            <h2>1. Progressive Muscle Relaxation (PMR)</h2>
            <p>Systematically tense and release each muscle group, starting from toes to head. This technique reduces physical tension and teaches body awareness. Practice for 10-15 minutes daily, especially before bed.</p>

            <h2>2. Box Breathing</h2>
            <p>Navy SEALs use this technique for instant calm under pressure. Inhale for 4 counts, hold for 4, exhale for 4, hold for 4. Repeat for 5 minutes. This activates your parasympathetic nervous system, lowering heart rate and blood pressure.</p>

            <h2>3. Mindfulness Meditation</h2>
            <p>Focus on present-moment awareness without judgment. Start with just 5 minutes daily using apps like Headspace or Calm. Research shows regular practice reduces cortisol levels by up to 20% and improves emotional regulation.</p>

            <h2>4. Physical Exercise</h2>
            <p>Any movement—walking, yoga, weightlifting—reduces stress hormones while releasing endorphins. Aim for 30 minutes most days. The key is consistency, not intensity.</p>

            <h2>5. Nature Exposure</h2>
            <p>Spending just 20 minutes in nature significantly lowers cortisol. Take walking meetings outdoors, eat lunch in a park, or simply sit under a tree. The Japanese practice of "forest bathing" (Shinrin-yoku) is backed by extensive research.</p>

            <h2>6. Social Connection</h2>
            <p>Quality relationships are among the strongest stress buffers. Schedule regular time with friends and family. Even a 10-minute phone call with a loved one triggers oxytocin release, counteracting stress.</p>

            <h2>7. Journaling</h2>
            <p>Expressive writing about stressful experiences helps process emotions and gain perspective. Write for 15-20 minutes about your thoughts and feelings without editing. Studies show this practice reduces anxiety and improves immune function.</p>

            <h2>Creating Your Stress Management Routine</h2>
            <p>Choose 2-3 techniques that resonate with you and practice them consistently. Stress management isn't about eliminating stress—it's about building resilience to handle life's inevitable challenges.</p>
        </div>
    </div>

    <div id="sleep-optimization" class="article-page">
        <div class="article-hero">
            <div class="article-hero-content">
                <div class="article-category">WELLNESS</div>
                <h1>Sleep Optimization Blueprint</h1>
                <div class="article-meta">
                    <span>📅 January 6, 2026</span>
                    <span>⏱️ 9 min read</span>
                    <span>👤 By Sleep Specialist Dr. Lisa Wong</span>
                </div>
            </div>
        </div>
        <div class="article-body">
            <a href="#" class="back-button" onclick="showHome()">← Back to Home</a>
            
            <p>Quality sleep is the foundation of health, impacting everything from immune function to cognitive performance. This comprehensive guide will help you optimize every aspect of your sleep.</p>

            <h2>Understanding Sleep Cycles</h2>
            <p>Sleep occurs in 90-minute cycles alternating between light sleep, deep sleep, and REM sleep. Adults need 7-9 hours (approximately 5-6 complete cycles) for optimal function. Deep sleep is crucial for physical recovery, while REM sleep consolidates memories and processes emotions.</p>

            <h2>The Perfect Sleep Environment</h2>
            <p><strong>Temperature:</strong> 60-67°F (15-19°C) is optimal. Your body temperature naturally drops during sleep, and a cool room facilitates this process.</p>
            
            <p><strong>Darkness:</strong> Complete darkness triggers melatonin production. Use blackout curtains or an eye mask. Even small amounts of light can disrupt sleep quality.</p>
            
            <p><strong>Noise:</strong> Aim for quiet (ideally under 30 decibels). Use white noise machines to mask disruptive sounds if needed.</p>
            
            <p><strong>Comfort:</strong> Invest in a quality mattress (replace every 7-10 years) and pillows that support proper spinal alignment.</p>

            <h2>Pre-Sleep Routine (The Golden Hour)</h2>
            <p><strong>2-3 hours before bed:</strong></p>
            <ul>
                <li>Stop eating heavy meals (light snacks are okay)</li>
                <li>Finish intensive exercise</li>
                <li>Dim lights throughout your home</li>
            </ul>

            <p><strong>1 hour before bed:</strong></p>
            <ul>
                <li>Turn off all screens (blue light suppresses melatonin by up to 50%)</li>
                <li>Lower room temperature</li>
                <li>Practice relaxation techniques: reading, gentle stretching, meditation</li>
                <li>Take a warm bath or shower (the post-bath temperature drop signals sleep time)</li>
            </ul>

            <h2>Circadian Rhythm Optimization</h2>
            <p><strong>Morning:</strong> Get 10-30 minutes of natural sunlight within 1 hour of waking. This anchors your circadian rhythm and improves nighttime melatonin production.</p>
            
            <p><strong>Afternoon:</strong> Avoid caffeine after 2 PM (it has a 5-6 hour half-life). Even if you can "sleep on caffeine," it reduces deep sleep quality.</p>
            
            <p><strong>Evening:</strong> Reduce bright light exposure, especially blue light from screens.</p>

            <h2>Supplements for Better Sleep</h2>
            <p><strong>Magnesium Glycinate:</strong> 200-400mg, 1-2 hours before bed. Supports muscle relaxation and GABA production.</p>
            
            <p><strong>L-Theanine:</strong> 200mg promotes relaxation without sedation.</p>
            
            <p><strong>Melatonin:</strong> 0.5-3mg (less is often more). Use only occasionally for jet lag or shift work—not daily.</p>
            
            <p><strong>Glycine:</strong> 3g improves sleep quality and reduces daytime fatigue.</p>

            <h2>When You Can't Sleep</h2>
            <p>If you can't fall asleep within 20 minutes, get out of bed. Do a quiet, non-stimulating activity in dim light until you feel drowsy. This prevents associating your bed with wakefulness.</p>

            <h2>Tracking Your Progress</h2>
            <p>Monitor sleep quality using wearable devices or apps that track sleep stages. Pay attention to how you feel upon waking—true rest leaves you refreshed, not groggy.</p>

            <p><strong>Key Metrics:</strong></p>
            <ul>
                <li>Total sleep time: 7-9 hours</li>
                <li>Deep sleep: 15-25% of total sleep</li>
                <li>REM sleep: 20-25% of total sleep</li>
                <li>Sleep efficiency: >85% (time asleep vs. time in bed)</li>
            </ul>

            <h2>Final Thoughts</h2>
            <p>Quality sleep is earned through consistent habits, not forced through willpower. Implement these strategies gradually and give your body 2-3 weeks to adapt. The payoff—increased energy, better mood, improved cognition, and enhanced physical performance—is worth the investment.</p>
        </div>
    </div>

    <!-- About Page -->
    <div id="about-page" class="article-page">
        <div class="article-hero">
            <div class="article-hero-content">
                <h1>About VitalityHub</h1>
                <p style="font-size: 1.2rem; color: var(--sage-500); margin-top: 1rem;">Your trusted companion on the journey to optimal health and wellness</p>
            </div>
        </div>
        <div class="about-section">
            <a href="#" class="back-button" onclick="showHome()">← Back to Home</a>
            
            <h2>Our Mission</h2>
            <p>VitalityHub was founded on a simple belief: everyone deserves access to accurate, science-backed health information presented in a way that's easy to understand and implement. We cut through the noise of conflicting health advice to bring you evidence-based strategies for lasting wellness.</p>

            <h2>What Sets Us Apart</h2>
            <p><strong>Evidence-Based Content:</strong> Every article is researched and backed by peer-reviewed studies. We cite our sources and update content regularly as new research emerges.</p>

            <p><strong>Expert Contributors:</strong> Our team includes certified nutritionists, fitness coaches, medical doctors, and mental health professionals who are passionate about sharing practical knowledge.</p>

            <p><strong>Holistic Approach:</strong> We understand that true wellness encompasses physical fitness, nutrition, mental health, and lifestyle habits. Our content reflects this comprehensive perspective.</p>

            <p><strong>Actionable Advice:</strong> We don't just explain concepts—we provide specific, implementable strategies you can start using today.</p>

            <h2>Our Content Philosophy</h2>
            <p>We believe in sustainable, long-term approaches over quick fixes. Our goal isn't to sell you the latest fad diet or miracle supplement. Instead, we focus on fundamental principles that have stood the test of scientific scrutiny and real-world application.</p>

            <h2>Who We Serve</h2>
            <p>Whether you're just beginning your wellness journey or you're an experienced health enthusiast looking to optimize further, VitalityHub provides valuable insights at every level. We meet you where you are and provide the guidance you need to progress.</p>

            <h2>Join Our Community</h2>
            <p>VitalityHub is more than a website—it's a community of individuals committed to living their healthiest lives. Subscribe to our newsletter for weekly tips, exclusive content, and personalized wellness advice delivered directly to your inbox.</p>

            <p style="margin-top: 2rem;"><em>Together, let's build a healthier, more vibrant future.</em></p>
        </div>
    </div>

    <!-- Contact Page -->
    <div id="contact-page" class="article-page">
        <div class="article-hero">
            <div class="article-hero-content">
                <h1>Get in Touch</h1>
                <p style="font-size: 1.2rem; color: var(--sage-500); margin-top: 1rem;">We'd love to hear from you</p>
            </div>
        </div>
        <div class="contact-form-section">
            <a href="#" class="back-button" onclick="showHome()">← Back to Home</a>
            
            <form class="contact-form" onsubmit="event.preventDefault(); alert('Thank you for your message! We will respond within 24-48 hours.');">
                <h2 style="font-family: var(--heading-font); color: var(--sage-700); margin-bottom: 1.5rem; text-align: center;">Send Us a Message</h2>
                
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" name="name" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" required>
                </div>
                
                <div class="form-group">
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" name="subject" required>
                </div>
                
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" name="message" required></textarea>
                </div>
                
                <button type="submit" class="btn btn-primary" style="width: 100%;">Send Message</button>
            </form>

            <div style="margin-top: 3rem; text-align: center; color: var(--sage-600);">
                <p><strong>Email:</strong> hello@vitalityhub.com</p>
                <p><strong>Response Time:</strong> Within 24-48 hours</p>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>VitalityHub</h3>
                <p>Your complete wellness companion. Evidence-based health tips, fitness guidance, and holistic wellness strategies for a healthier, happier life.</p>
            </div>
            <div class="footer-section">
                <h3>Quick Links</h3>
                <ul class="footer-links">
                    <li><a href="#" onclick="showHome()">Home</a></li>
                    <li><a href="#" onclick="showAbout()">About</a></li>
                    <li><a href="#articles">Articles</a></li>
                    <li><a href="#" onclick="showContact()">Contact</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Categories</h3>
                <ul class="footer-links">
                    <li><a href="#articles">Fitness</a></li>
                    <li><a href="#articles">Nutrition</a></li>
                    <li><a href="#articles">Mental Health</a></li>
                    <li><a href="#articles">Wellness</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Legal</h3>
                <ul class="footer-links">
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Terms of Service</a></li>
                    <li><a href="#">Disclaimer</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 VitalityHub. All rights reserved. | Designed for optimal wellness.</p>
        </div>
    </footer>

    <script>
        // Navigation functions
        function showHome() {
            // Hide all pages
            document.getElementById('home-page').style.display = 'block';
            document.getElementById('about-page').classList.remove('active');
            document.getElementById('contact-page').classList.remove('active');
            
            // Hide all article pages
            const articlePages = document.querySelectorAll('.article-page');
            articlePages.forEach(page => page.classList.remove('active'));
            
            // Scroll to top
            window.scrollTo(0, 0);
        }

        function showAbout() {
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('about-page').classList.add('active');
            document.getElementById('contact-page').classList.remove('active');
            
            // Hide all article pages
            const articlePages = document.querySelectorAll('.article-page');
            articlePages.forEach(page => {
                if (page.id !== 'about-page') {
                    page.classList.remove('active');
                }
            });
            
            window.scrollTo(0, 0);
        }

        function showContact() {
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('about-page').classList.remove('active');
            document.getElementById('contact-page').classList.add('active');
            
            // Hide all article pages
            const articlePages = document.querySelectorAll('.article-page');
            articlePages.forEach(page => {
                if (page.id !== 'contact-page') {
                    page.classList.remove('active');
                }
            });
            
            window.scrollTo(0, 0);
        }

        function showArticle(articleId) {
            // Hide home page
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('about-page').classList.remove('active');
            document.getElementById('contact-page').classList.remove('active');
            
            // Hide all article pages first
            const articlePages = document.querySelectorAll('.article-page');
            articlePages.forEach(page => page.classList.remove('active'));
            
            // Show selected article
            const selectedArticle = document.getElementById(articleId);
            if (selectedArticle) {
                selectedArticle.classList.add('active');
            }
            
            // Scroll to top
            window.scrollTo(0, 0);
        }

        // Smooth scroll for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                if (this.getAttribute('href') === '#' || this.getAttribute('onclick')) {
                    return; // Let onclick handlers work
                }
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
