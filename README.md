<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Amatech Eagle Global Enterprises</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #1a5276;
            --secondary: #f39c12;
            --accent: #2e86c1;
            --light: #f8f9fa;
            --dark: #2c3e50;
            --gray: #7f8c8d;
            --success: #27ae60;
            --error: #e74c3c;
        }

        body {
            line-height: 1.6;
            color: #333;
            background-color: var(--light);
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        section {
            padding: 60px 0;
        }

        h1, h2, h3, h4 {
            margin-bottom: 15px;
            color: var(--dark);
        }

        h1 {
            font-size: 2.5rem;
            line-height: 1.2;
        }

        h2 {
            font-size: 2rem;
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }

        h2:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--secondary);
            margin: 10px auto;
        }

        p {
            margin-bottom: 15px;
        }

        .btn {
            display: inline-block;
            padding: 12px 25px;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .btn:hover {
            background: var(--accent);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .btn-secondary {
            background: var(--secondary);
        }

        .btn-secondary:hover {
            background: #e67e22;
        }

        /* Header Styles */
        header {
            background: var(--primary);
            color: white;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
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
            font-size: 1.8rem;
            color: white;
            margin-bottom: 0;
        }

        .logo span {
            color: var(--secondary);
        }

        .logo i {
            font-size: 2rem;
            margin-right: 10px;
            color: var(--secondary);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 25px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            padding: 5px 0;
            position: relative;
        }

        nav ul li a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: var(--secondary);
            transition: width 0.3s;
        }

        nav ul li a:hover:after {
            width: 100%;
        }

        nav ul li a:hover {
            color: var(--secondary);
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1504307651254-35680f356dfd?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 120px 0;
        }

        .hero h1 {
            font-size: 3rem;
            color: white;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }

        /* Services Section */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
            height: 100%;
            display: flex;
            flex-direction: column;
        }

        .service-card:hover {
            transform: translateY(-10px);
        }

        .service-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }

        .service-content {
            padding: 20px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .service-content h3 {
            color: var(--primary);
            margin-bottom: 10px;
        }

        .service-content p {
            flex-grow: 1;
        }

        /* About Section */
        .about {
            background: var(--dark);
            color: white;
        }

        .about h2 {
            color: white;
        }

        .about h2:after {
            background: var(--secondary);
        }

        .about-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
        }

        .about-image {
            flex: 1;
            min-width: 300px;
            height: 400px;
            background: url('https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        /* Contact Section */
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
            margin-bottom: 20px;
            color: var(--primary);
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            padding: 15px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .contact-item:hover {
            transform: translateX(5px);
        }

        .contact-item i {
            width: 50px;
            height: 50px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.2rem;
        }

        .contact-form {
            flex: 1;
            min-width: 300px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border 0.3s;
        }

        .form-control:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 2px rgba(26, 82, 118, 0.2);
        }

        textarea.form-control {
            height: 150px;
            resize: vertical;
        }

        .form-message {
            padding: 10px;
            border-radius: 5px;
            margin-top: 15px;
            display: none;
        }

        .form-message.success {
            background-color: rgba(39, 174, 96, 0.1);
            color: var(--success);
            border: 1px solid var(--success);
            display: block;
        }

        .form-message.error {
            background-color: rgba(231, 76, 60, 0.1);
            color: var(--error);
            border: 1px solid var(--error);
            display: block;
        }

        /* Deployment Guide Section */
        .deployment-guide {
            background: #f9f9f9;
            padding: 60px 0;
        }

        .deployment-steps {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }

        .deployment-step {
            flex: 1;
            min-width: 250px;
            background: white;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }

        .deployment-step h3 {
            color: var(--primary);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .deployment-step h3 i {
            color: var(--secondary);
        }

        .deployment-step ol {
            padding-left: 20px;
        }

        .deployment-step li {
            margin-bottom: 10px;
        }

        .deployment-links {
            display: flex;
            gap: 10px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 40px 0 20px;
        }

        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 30px;
            margin-bottom: 30px;
        }

        .footer-column {
            flex: 1;
            min-width: 250px;
        }

        .footer-column h3 {
            color: var(--secondary);
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-column ul li a:hover {
            color: var(--secondary);
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            text-decoration: none;
            transition: all 0.3s;
        }

        .social-links a:hover {
            background: var(--secondary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            color: #aaa;
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 80%;
                height: calc(100vh - 70px);
                background: var(--dark);
                transition: all 0.3s;
                z-index: 999;
                padding-top: 30px;
            }
            
            nav.active {
                left: 0;
            }
            
            nav ul {
                flex-direction: column;
                padding: 20px;
            }
            
            nav ul li {
                margin: 0 0 20px 0;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .hero-buttons .btn {
                width: 80%;
                max-width: 250px;
            }
        }

        @media (max-width: 576px) {
            section {
                padding: 40px 0;
            }
            
            .hero {
                padding: 80px 0;
            }
            
            .hero h1 {
                font-size: 1.8rem;
            }
            
            h2 {
                font-size: 1.6rem;
            }
            
            .about-content, .contact-container {
                flex-direction: column;
            }
            
            .about-image {
                height: 250px;
            }
            
            .deployment-links {
                flex-direction: column;
            }
            
            .deployment-links .btn {
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-building"></i>
                <h1>Amatech <span>Eagle</span> Global</h1>
            </div>
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#deploy">Go Live</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Amatech Eagle Global Enterprises</h1>
            <p>Your trusted partner for high-quality construction materials and contracting services</p>
            <div class="hero-buttons">
                <a href="#services" class="btn btn-secondary">Our Services</a>
                <a href="#contact" class="btn">Get In Touch</a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <div class="container">
            <h2>Our Products & Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="service-content">
                        <h3>High Quality Aluminum</h3>
                        <p>Premium aluminum products for construction, industrial and domestic applications. Durable, corrosion-resistant and aesthetically pleasing.</p>
                        <a href="#contact" class="btn" style="margin-top: auto; align-self: flex-start;">Inquire Now</a>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1586023492125-27b2c045efd7?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="service-content">
                        <h3>Stone Coated Tiles</h3>
                        <p>Beautiful and durable stone-coated roofing tiles that combine the elegance of natural stone with modern manufacturing technology.</p>
                        <a href="#contact" class="btn" style="margin-top: auto; align-self: flex-start;">Inquire Now</a>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1616046229478-9901c5536a45?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="service-content">
                        <h3>PVC Pipes & Gutters</h3>
                        <p>High-quality PVC pipes and gutter systems for efficient water management in residential and commercial buildings.</p>
                        <a href="#contact" class="btn" style="margin-top: auto; align-self: flex-start;">Inquire Now</a>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1504307651254-35680f356dfd?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80');"></div>
                    <div class="service-content">
                        <h3>General Contracting</h3>
                        <p>Complete construction and contracting services from design to execution, ensuring quality and timely project delivery.</p>
                        <a href="#contact" class="btn" style="margin-top: auto; align-self: flex-start;">Inquire Now</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2>About Us</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Amatech Eagle Global Enterprises is a leading provider of high-quality construction materials and contracting services. With years of experience in the industry, we have built a reputation for excellence, reliability, and customer satisfaction.</p>
                    <p>Our product range includes premium aluminum products, durable stone-coated tiles, and high-quality PVC pipes and gutters. We also offer comprehensive general contracting services for residential and commercial projects.</p>
                    <p>At Amatech Eagle Global, we are committed to delivering superior quality products and services that meet the highest standards. Our team of experienced professionals ensures that every project is completed with precision and attention to detail.</p>
                    <a href="#contact" class="btn">Contact Us Today</a>
                </div>
                <div class="about-image"></div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2>Contact Us</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Get In Touch</h3>
                    <div class="contact-item">
                        <i class="fas fa-phon