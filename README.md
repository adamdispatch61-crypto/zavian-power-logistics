<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Zavian Power Logistics - Professional freight dispatch and trucking load management services in Houston, TX. Powering your loads with precision.">
    <meta name="keywords" content="freight dispatch, trucking dispatch, load management, logistics, Houston TX">
    <meta name="author" content="Zavian Power Logistics">
    <title>Zavian Power Logistics | Freight Dispatch & Load Management</title>
    
    <!-- Favicon -->
    <link rel="icon" type="image/x-icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' fill='%231a1a1a'/><text y='.9em' font-size='90' fill='%23D4AF37'>ZPL</text></svg>">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-black: #1a1a1a;
            --secondary-black: #0d0d0d;
            --accent-gold: #D4AF37;
            --accent-blue: #00bfff;
            --text-light: #ffffff;
            --text-muted: #b0b0b0;
            --shadow: 0 20px 40px rgba(0,0,0,0.3);
            --shadow-gold: 0 20px 40px rgba(212, 175, 55, 0.3);
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-light);
            background: var(--primary-black);
            overflow-x: hidden;
        }

        /* Sticky Navigation */
        nav {
            position: sticky;
            top: 0;
            width: 100%;
            background: rgba(13, 13, 13, 0.98);
            backdrop-filter: blur(20px);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }

        nav.scrolled {
            background: rgba(13, 13, 13, 0.99);
            padding: 0.7rem 0;
            box-shadow: var(--shadow);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(45deg, var(--accent-gold), var(--accent-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: linear-gradient(45deg, var(--accent-gold), var(--accent-blue));
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--accent-gold);
        }

        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 4px;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: var(--text-light);
            transition: 0.3s;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, var(--secondary-black) 0%, var(--primary-black) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23D4AF37' fill-opacity='0.03'%3E%3Ccircle cx='30' cy='30' r='2'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hero-content h1 {
            font-size: clamp(3rem, 8vw, 6rem);
            margin-bottom: 1rem;
            background: linear-gradient(45deg, var(--accent-gold), var(--accent-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInUp 1s ease;
        }

        .hero-content .tagline {
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            margin-bottom: 2rem;
            color: var(--text-muted);
            animation: fadeInUp 1s ease 0.2s both;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, var(--accent-gold), var(--accent-blue));
            color: var(--primary-black);
            padding: 1rem 2.5rem;
            font-size: 1.1rem;
            font-weight: bold;
            text-decoration: none;
            border-radius: 50px;
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease 0.4s both;
            box-shadow: var(--shadow-gold);
        }

        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 25px 50px rgba(212, 175, 55, 0.4);
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

        /* Sections */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding-left: 2rem;
            padding-right: 2rem;
        }

        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            font-size: clamp(2rem, 5vw, 3.5rem);
            margin-bottom: 4rem;
            background: linear-gradient(45deg, var(--accent-gold), var(--accent-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* About */
        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
            font-size: 1.2rem;
            line-height: 1.8;
        }

        /* Services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .service-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 2.5rem;
            border-radius: 20px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(212, 175, 55, 0.2);
            backdrop-filter: blur(10px);
        }

        .service-card:hover {
            transform: translateY(-10px);
            background: rgba(212, 175, 55, 0.1);
            border-color: var(--accent-gold);
            box-shadow: var(--shadow-gold);
        }

        .service-icon {
            font-size: 3rem;
            background: linear-gradient(45deg, var(--accent-gold), var(--accent-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
        }

        /* Why Choose Us */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
        }

        .feature-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(45deg, var(--accent-gold), var(--accent-blue));
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            flex-shrink: 0;
        }

        /* Contact */
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            max-width: 1000px;
            margin: 0 auto;
        }

        .contact-info h3 {
            color: var(--accent-gold);
            margin-bottom: 2rem;
            font-size: 1.5rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
            gap: 1rem;
        }

        .contact-item .icon {
            width: 50px;
            height: 50px;
            background: rgba(212, 175, 55, 0.2);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent-gold);
            font-size: 1.2rem;
        }

        .map-container {
            margin-top: 2rem;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow-gold);
            height: 300px;
        }

        .contact-form {
            background: rgba(255, 255, 255, 0.05);
            padding: 2.5rem;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212, 175, 55, 0.2);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--text-muted);
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            color: var(--text-light);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--accent-gold);
            box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.1);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .submit-btn {
            width: 100%;
            background: linear-gradient(45deg, var(--accent-gold), var(--accent-blue));
            color: var(--primary-black);
            padding: 1rem;
            border: none;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: var(--shadow-gold);
        }

        .success-message,
        .error-message {
            padding: 1rem;
            border-radius: 10px;
            margin-bottom: 1rem;
            display: none;
            text-align: center;
        }

        .success-message {
            background: rgba(0, 255, 0, 0.2);
            color: #90ee90;
            border: 1px solid rgba(0, 255, 0, 0.3);
        }

        .error-message {
            background: rgba(255, 0, 0, 0.2);
            color: #ff6b6b;
            border: 1px solid rgba(255, 0, 0, 0.3);
        }

        /* Footer */
        footer {
            background: var(--secondary-black);
            padding: 2rem;
            text-align: center;
            border-top: 1px solid rgba(212, 175, 55, 0.2);
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .footer-info {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .footer-logo {
            font-size: 1.5rem;
            font-weight: bold;
            background: linear-gradient(45deg, var(--accent-gold), var(--accent-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }

            .nav-links {
                display: none;
            }

            .contact-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            section {
                padding: 80px 0;
            }

            .container {
                padding-left: 1.5rem;
                padding-right: 1.5rem;
            }

            .hero {
                padding: 0 1rem;
            }

            .map-container {
                height: 250px;
            }
        }

        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <!-- Sticky Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">Zavian Power Logistics</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#why-us">Why Us</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Zavian Power Logistics</h1>
            <p class="tagline">Powering Your Loads, Delivering Precision</p>
            <a href="#contact" class="cta-button">Get a Quote</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">About Zavian Power Logistics</h2>
            <div class="about-content">
                <p>Based in Houston, TX, Zavian Power Logistics is your trusted partner for professional freight dispatch and load management services. We specialize in connecting shippers with reliable carriers, negotiating competitive rates, and ensuring seamless load execution from pickup to delivery.</p>
                <p>With our cutting-edge technology and industry expertise, we power your logistics operations with unmatched precision and efficiency.</p>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" style="background: rgba(0,0,0,0.3);">
        <div class="container">
            <h2 class="section-title">Our Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">🚚</div>
                    <h3>Freight Dispatch</h3>
                    <p>Expert dispatch services connecting shippers with vetted carriers. We handle the coordination so you can focus on your business.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">📍</div>
                    <h3>Load Tracking</h3>
                    <p>Real-time GPS tracking and load monitoring with instant updates and ETAs for complete visibility.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">💰</div>
                    <h3>Rate Negotiation</h3>
                    <p>Market-leading rate negotiation securing you the best possible pricing on every load.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">✅</div>
                    <h3>Carrier Onboarding</h3>
                    <p>Comprehensive carrier vetting, insurance verification, and onboarding for reliable partnerships.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Choose Us -->
    <section id="why-us">
        <div class="container">
            <h2 class="section-title">Why Choose Zavian?</h2>
            <div class="features">
                <div class="feature">
                    <div class="feature-icon">⚡</div>
                    <div>
                        <h3>Lightning Fast Dispatch</h3>
                        <p>Loads posted and carriers secured within hours, not days.</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">🎯</div>
                    <div>
                        <h3>Precision Execution</h3>
                        <p>99.8% on-time pickup and delivery performance.</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">💎</div>
                    <div>
                        <h3>Premium Service</h3>
                        <p>24/7 support with dedicated account managers.</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">📈</div>
                    <div>
                        <h3>Market Expertise</h3>
                        <p>Deep knowledge of freight rates and carrier capacity nationwide.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" style="background: rgba(0,0,0,0.3);">
        <div class="container">
            <h2 class="section-title">Contact Us</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Ready to Power Your Loads?</h3>
                    <p style="margin-bottom: 2rem; color: var(--text-muted);">Get in touch for a free rate quote or consultation.</p>
                    
                    <div class="contact-item">
                        <div class="icon">📍</div>
                        <div>
                            <strong>1113 Vine Street</strong><br>
                            Houston, TX 77002<br>
                            United States
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="icon">✉️</div>
                        <div>
                            <strong>zavianlogistics@gmail.com</strong>
                        </div>
                    </div>

                    <!-- Google Maps iframe for 1113 Vine Street, Houston, TX -->
                    <div class="map-container">
                        <iframe 
                            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3468.057845614614!2d-95.37038968502668!3d29.756308982115!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8640c1f4b4b4b4b4%3A0x4b4b4b4b4b4b4b4b!2s1113%20Vine%20St%2C%20Houston%2C%20TX%2077002!5e0!3m2!1sen!2sus!4v1700000000000!5m2!1sen!2sus" 
                            width="100%" 
                            height="100%" 
                            style="border:0;" 
                            allowfullscreen="" 
                            loading="lazy" 
                            referrerpolicy="no-referrer-when-downgrade">
                        </iframe>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" name="message" required placeholder="Tell us about your logistics needs..."></textarea>
                        </div>
                        <div id="successMessage" class="success-message">Thank you! Your message has been sent. We'll respond within 24 hours.</div>
                        <div id="errorMessage" class="error-message">Please fill out all fields correctly.</div>
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-info">
                <div class="footer-logo">Zavian Power Logistics</div>
                <p>&copy; 2024 Zavian Power Logistics. All rights reserved.</p>
                <p>1113 Vine Street, Houston, TX 77002 | zavianlogistics@gmail.com</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
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

        // Navbar scroll effect (enhanced for sticky nav)
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if (window.scrollY > 50) {
                nav.classList.add('scrolled');
            } else {
                nav.classList.remove('scrolled');
            }
        });

        // Form validation and submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();
            
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            
            if (!name || !email || !message) {
                showError();
                return;
            }
            
            if (!emailRegex.test(email)) {
                showError('Please enter a valid email address.');
                return;
            }
            
            // Simulate form submission
            showSuccess();
            
            // Here you would typically send the data to your server
            console.log('Form submitted:', { name, email, message });
            
            // Reset form
            this.reset();
        });

        function showSuccess() {
            document.getElementById('successMessage').style.display = 'block';
            document.getElementById('errorMessage').style.display = 'none';
            setTimeout(() => {
                document.getElementById('successMessage').style.display = 'none';
            }, 5000);
        }

        function showError(message = 'Please fill out all fields correctly.') {
            const errorEl = document.getElementById('errorMessage');
            errorEl.textContent = message;
            errorEl.style.display = 'block';
            document.getElementById('successMessage').style.display = 'none';
        }

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe service cards and features
        document.querySelectorAll('.service-card, .feature').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'all 0.6s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>
