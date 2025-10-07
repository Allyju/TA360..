<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tech Alliance 360 - Complete Cybersecurity Solutions</title>
    <style>
        /* CSS IMPROVEMENTS AND ENHANCEMENTS */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary-blue: #19366D;
            --secondary-blue: #4A90E2;
            --accent-blue: #2A5BA7;
            --light-bg: #F5F5F5;
            --white: #FFFFFF;
            --text-dark: #333333;
            --text-light: #6c757d;
            --success: #28a745;
            --warning: #ffc107;
            --danger: #dc3545;
        }

        body {
            background-color: var(--light-bg);
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* Header - Enhanced with better navigation */
        header {
            background-color: var(--primary-blue);
            padding: 15px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px rgba(0,0,0,0.15);
            transition: all 0.3s ease;
        }

        header.scrolled {
            padding: 10px 0;
            background-color: rgba(25, 54, 109, 0.95);
            backdrop-filter: blur(10px);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo h1 {
            color: var(--white);
            font-size: 1.8rem;
            font-weight: 700;
        }

        .logo span {
            color: var(--secondary-blue);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 25px;
            position: relative;
        }

        nav ul li a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            padding: 5px 0;
            position: relative;
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: var(--secondary-blue);
            transition: width 0.3s ease;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        nav ul li a:hover {
            color: var(--secondary-blue);
        }

        .mobile-menu {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section - Enhanced with animation */
        .hero {
            background: linear-gradient(135deg, var(--primary-blue), var(--accent-blue));
            color: var(--white);
            padding: 180px 0 120px;
            text-align: center;
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
            background: url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiPjxkZWZzPjxwYXR0ZXJuIGlkPSJwYXR0ZXJuIiB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIHBhdHRlcm5Vbml0cz0idXNlclNwYWNlT25Vc2UiIHBhdHRlcm5UcmFuc2Zvcm09InJvdGF0ZSg0NSkiPjxyZWN0IHdpZHRoPSIyMCIgaGVpZ2h0PSIyMCIgZmlsbD0icmdiYSgyNTUsIDI1NSwgMjU1LCAwLjAzKSIvPjwvcGF0dGVybj48L2RlZnM+PHJlY3QgZmlsbD0idXJsKCNwYXR0ZXJuKSIgd2lkdGg9IjEwMCUiIGhlaWdodD0iMTAwJSIvPjwvc3ZnPg==');
            opacity: 0.3;
        }

        .hero h2 {
            font-size: 3.2rem;
            margin-bottom: 20px;
            font-weight: 700;
            position: relative;
            animation: fadeInDown 1s ease;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 30px;
            opacity: 0.9;
            position: relative;
            animation: fadeInUp 1s ease 0.3s both;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--white);
            color: var(--primary-blue);
            padding: 14px 35px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s;
            border: 2px solid transparent;
            position: relative;
            animation: fadeIn 1s ease 0.6s both;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .cta-button:hover {
            background-color: transparent;
            color: var(--white);
            border: 2px solid var(--white);
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
        }

        /* About Section */
        .about {
            padding: 100px 0;
            background-color: var(--white);
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
            color: var(--primary-blue);
            font-size: 2.5rem;
            position: relative;
            font-weight: 700;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: var(--secondary-blue);
            margin: 20px auto;
            border-radius: 2px;
        }

        .about-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 30px;
        }

        .about-item {
            flex: 1;
            min-width: 300px;
            padding: 40px 30px;
            background-color: var(--light-bg);
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
            overflow: hidden;
        }

        .about-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background-color: var(--secondary-blue);
            transition: width 0.3s;
        }

        .about-item:hover::before {
            width: 8px;
        }

        .about-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }

        .about-item h3 {
            color: var(--secondary-blue);
            margin-bottom: 20px;
            font-size: 1.5rem;
            font-weight: 600;
        }

        /* Services Section */
        .services {
            padding: 100px 0;
            background-color: var(--light-bg);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background-color: var(--white);
            padding: 40px 30px;
            border-radius: 8px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s;
            border-top: 4px solid var(--secondary-blue);
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 0;
            background: linear-gradient(to bottom, var(--secondary-blue), transparent);
            opacity: 0.1;
            transition: height 0.3s;
        }

        .service-card:hover::before {
            height: 100%;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }

        .service-icon {
            font-size: 3rem;
            color: var(--secondary-blue);
            margin-bottom: 20px;
            display: inline-block;
            transition: transform 0.3s;
        }

        .service-card:hover .service-icon {
            transform: scale(1.1);
        }

        .service-card h3 {
            color: var(--primary-blue);
            margin-bottom: 15px;
            font-size: 1.5rem;
            font-weight: 600;
        }

        /* Contact Section */
        .contact {
            padding: 100px 0;
            background-color: var(--white);
        }

        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
        }

        .contact-info {
            flex: 1;
            min-width: 300px;
        }

        .contact-info h3 {
            color: var(--primary-blue);
            margin-bottom: 20px;
            font-size: 1.5rem;
            font-weight: 600;
        }

        .contact-details {
            margin-top: 30px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
            padding: 15px;
            border-radius: 8px;
            transition: background-color 0.3s;
        }

        .contact-item:hover {
            background-color: rgba(74, 144, 226, 0.05);
        }

        .contact-icon {
            background-color: var(--secondary-blue);
            color: var(--white);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            flex-shrink: 0;
            font-size: 1.2rem;
        }

        .contact-form {
            flex: 1;
            min-width: 300px;
            background-color: var(--light-bg);
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--primary-blue);
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 14px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border 0.3s, box-shadow 0.3s;
        }

        .form-control:focus {
            border-color: var(--secondary-blue);
            box-shadow: 0 0 0 3px rgba(74, 144, 226, 0.2);
            outline: none;
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        .submit-btn {
            background-color: var(--secondary-blue);
            color: var(--white);
            border: none;
            padding: 14px 35px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 500;
            transition: background-color 0.3s, transform 0.3s;
            width: 100%;
        }

        .submit-btn:hover {
            background-color: var(--primary-blue);
            transform: translateY(-2px);
        }

        /* Footer */
        footer {
            background-color: var(--primary-blue);
            color: var(--white);
            padding: 60px 0 20px;
        }

        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 30px;
            margin-bottom: 40px;
        }

        .footer-column {
            flex: 1;
            min-width: 200px;
        }

        .footer-column h3 {
            color: var(--secondary-blue);
            margin-bottom: 20px;
            font-size: 1.3rem;
            font-weight: 600;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: var(--white);
            text-decoration: none;
            transition: color 0.3s;
            position: relative;
            padding-left: 0;
            transition: padding-left 0.3s;
        }

        .footer-links a:hover {
            color: var(--secondary-blue);
            padding-left: 8px;
        }

        .footer-links a::before {
            content: '›';
            position: absolute;
            left: -10px;
            opacity: 0;
            transition: opacity 0.3s, left 0.3s;
        }

        .footer-links a:hover::before {
            opacity: 1;
            left: 0;
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: rgba(255,255,255,0.7);
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
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

        /* Mobile Responsive */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2.8rem;
            }
            
            .section-title {
                font-size: 2.2rem;
            }
        }

        @media (max-width: 768px) {
            .header-container {
                flex-direction: row;
                text-align: left;
            }

            nav {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--primary-blue);
                padding: 20px;
                box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            }

            nav.active {
                display: block;
            }

            nav ul {
                flex-direction: column;
                margin-top: 0;
            }

            nav ul li {
                margin: 0 0 15px;
            }

            .mobile-menu {
                display: block;
            }

            .hero {
                padding: 150px 0 100px;
            }

            .hero h2 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .section-title {
                font-size: 1.8rem;
            }
        }

        @media (max-width: 480px) {
            .hero {
                padding: 130px 0 80px;
            }

            .hero h2 {
                font-size: 1.8rem;
            }

            .about-item, .service-card {
                min-width: 100%;
            }
            
            .contact-form {
                padding: 25px;
            }
        }
    </style>
</head>
<body>
    <!-- Website Header -->
    <header id="header">
        <div class="container header-container">
            <div class="logo">
                <h1>Tech<span>Alliance</span>360</h1>
            </div>
            <nav id="nav">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <button class="mobile-menu" id="mobileMenu">☰</button>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <h2>Tech Alliance 360</h2>
            <p>Empowering Businesses with Complete Cyber Protection</p>
            <p>We provide comprehensive cybersecurity solutions for businesses in Tanzania and beyond</p>
            <a href="#contact" class="cta-button">Get Expert Assistance</a>
        </div>
    </section>

    <!-- About Us -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About Us</h2>
            <div class="about-content">
                <div class="about-item">
                    <h3>Our Mission</h3>
                    <p>To deliver comprehensive cybersecurity solutions that protect businesses against digital threats. We focus on providing cutting-edge, premium services to our clients.</p>
                </div>
                <div class="about-item">
                    <h3>Our Vision</h3>
                    <p>To become the leading trusted cybersecurity service provider for businesses worldwide. We aim to be the first choice for all businesses in Tanzania.</p>
                </div>
                <div class="about-item">
                    <h3>Our Values</h3>
                    <p>Integrity, innovation, and dedication in everything we do. Our clients are always our top priority, and we're committed to their security and success.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Services -->
    <section id="services" class="services">
        <div class="container">
            <h2 class="section-title">Our Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">🔒</div>
                    <h3>Security Audits</h3>
                    <p>We examine your technological systems and provide protection recommendations. Use cutting-edge technology to detect security vulnerabilities.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">📚</div>
                    <h3>Security Training</h3>
                    <p>Provide training to your employees on cybersecurity. Your employees are the first line of defense against cyber threats.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🛡️</div>
                    <h3>Threat Management</h3>
                    <p>Detect and respond to cyber threats in real-time. Ensure your business remains secure at all times.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">💼</div>
                    <h3>Security Planning</h3>
                    <p>We help you prepare emergency plans and risk management strategies. Prepare your business for all challenges.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🔍</div>
                    <h3>Incident Investigation</h3>
                    <p>Conduct in-depth investigations following security incidents. Identify the source of problems and prevent recurrence.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🌐</div>
                    <h3>Web Security</h3>
                    <p>Protect your website and applications against cyber attacks. Ensure your system continues to function optimally.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Us -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Contact Us</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Let's Talk</h3>
                    <p>Call us, send us an email, or use the form here to leave us a message. We're happy to listen and help you.</p>
                    
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">✉️</div>
                            <div>
                                <strong>Email</strong><br>
                                <a href="mailto:info@techalliance360.co.tz">info@techalliance360.co.tz</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">📞</div>
                            <div>
                                <strong>Phone</strong><br>
                                +255 695![file_00000000f3f0622fa7c9df6e7488291c](https://github.com/user-attachments/assets/f41edb41-258e-4825-896f-8a39d9f9177a)
 096 807
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">📍</div>
                            <div>
                                <strong>Location</strong><br>
                                Dar es Salaam, Tanzania
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Full Name</label>
                            <input type="text" id="name" class="form-control" placeholder="Enter your full name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" class="form-control" placeholder="your@email.com" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" class="form-control" placeholder="Subject of your message" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" placeholder="Write your message here..." required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Tech Alliance 360</h3>
                    <p>Empowering Businesses with Complete Cyber Protection. We provide premium cybersecurity services in Tanzania.</p>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Our Services</h3>
                    <ul class="footer-links">
                        <li><a href="#">Security Audits</a></li>
                        <li><a href="#">Security Training</a></li>
                        <li><a href="#">Threat Management</a></li>
                        <li><a href="#">Web Security</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 Tech Alliance 360. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Enhanced JavaScript for better functionality
        document.addEventListener('DOMContentLoaded', function() {
            // Mobile menu toggle
            const mobileMenu = document.getElementById('mobileMenu');
            const nav = document.getElementById('nav');
            
            mobileMenu.addEventListener('click', function() {
                nav.classList.toggle('active');
            });
            
            // Header scroll effect
            const header = document.getElementById('header');
            
            window.addEventListener('scroll', function() {
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }
            });
            
            // Smooth scrolling for anchor links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        // Close mobile menu if open
                        nav.classList.remove('active');
                        
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
            
            // Contact form handling
            document.getElementById('contactForm').addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Get form data
                const name = document.getElementById('name').value;
                const email = document.getElementById('email').value;
                const subject = document.getElementById('subject').value;
                const message = document.getElementById('message').value;
                
                // Simple validation
                if (!name || !email || !subject || !message) {
                    alert('Please fill in all fields before submitting.');
                    return;
                }
                
                // Show success message
                alert(`Thank you for your message, ${name}! We will contact you soon at ${email}.`);
                
                // Reset form
                this.reset();
            });
        });
    </script>
</body>
</html>
