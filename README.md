<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>St. Clare Montessori & Science High School</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Other meta tags and title -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.carousel.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.theme.default.min.css">
    <style>
        /* Color Scheme */
        :root {
            --primary-brown: #8B4513;
            --dark-brown: #5D4037;
            --light-brown: #D2B48C;
            --primary-yellow: #FFD700;
            --light-yellow: #FFF9C4;
            --cream: #FFF8E1;
            --white: #FFFFFF;
            --black: #212121;
            --gray: #757575;
        }

        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            line-height: 1.6;
            color: var(--black);
            background-color: var(--cream);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px 0;
        }

        .btn {
            display: inline-block;
            background: var(--primary-yellow);
            color: var(--dark-brown);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            box-shadow: 0 3px 6px rgba(0,0,0,0.1);
        }

        .btn:hover {
            background: #e6c200;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .btn-brown {
            background: var(--primary-brown);
            color: white;
        }

        .btn-brown:hover {
            background: #7a3b10;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: var(--dark-brown);
            position: relative;
            font-size: 2.2rem;
        }

        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--primary-yellow);
            margin: 15px auto 0;
        }

        /* Header */
        .top-bar {
            background: var(--dark-brown);
            color: white;
            padding: 8px 0;
            font-size: 0.9rem;
        }

        .top-bar .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0;
        }

        .announcement-text {
            font-weight: 500;
        }

        .announcement-text span {
            background: var(--primary-yellow);
            color: var(--dark-brown);
            padding: 3px 10px;
            border-radius: 20px;
            font-weight: bold;
            margin-right: 10px;
            font-size: 0.8rem;
        }

        .social-links a {
            color: white;
            margin-left: 15px;
            font-size: 1rem;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--primary-yellow);
        }

        header {
            background: var(--white);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            height: 60px;
            margin-right: 15px;
        }

        .logo-text h1 {
            font-size: 1.5rem;
            color: var(--dark-brown);
            line-height: 1.2;
        }

        .logo-text p {
            font-size: 0.9rem;
            color: var(--gray);
        }

        .nav-links {
            display: flex;
            gap: 25px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark-brown);
            font-weight: 600;
            position: relative;
            padding: 5px 0;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary-brown);
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary-yellow);
            transition: width 0.3s ease;
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .dropdown {
            position: relative;
        }

        .dropdown-content {
            display: none;
            position: absolute;
            background: white;
            min-width: 200px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
            z-index: 1;
            border-radius: 5px;
            top: 100%;
            left: 0;
        }

        .dropdown:hover .dropdown-content {
            display: block;
        }

        .dropdown-content a {
            display: block;
            padding: 10px 15px;
            color: var(--dark-brown);
        }

        .dropdown-content a:hover {
            background: var(--light-yellow);
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--dark-brown);
            cursor: pointer;
        }

        /* Hero Carousel */
        .hero-carousel {
            position: relative;
            height: 80vh;
            overflow: hidden;
        }

        .hero-slide {
            height: 100%;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            position: relative;
        }

        .hero-slide:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.4);
        }

        .hero-content {
            position: relative;
            z-index: 2;
            color: white;
            width: 100%;
            padding: 0 20px;
            text-align: center;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 30px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }

        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .owl-nav {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
            z-index: 3;
        }

        .owl-prev, .owl-next {
            background: rgba(255,255,255,0.3) !important;
            color: white !important;
            width: 50px;
            height: 50px;
            border-radius: 50% !important;
            font-size: 2rem !important;
            display: flex !important;
            align-items: center;
            justify-content: center;
            margin: 0 20px !important;
            transition: all 0.3s ease;
        }

        .owl-prev:hover, .owl-next:hover {
            background: var(--primary-yellow) !important;
            color: var(--dark-brown) !important;
        }

        .owl-dots {
            position: absolute;
            bottom: 30px;
            width: 100%;
            display: flex;
            justify-content: center;
            gap: 10px;
        }

        .owl-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: rgba(255,255,255,0.5) !important;
            transition: all 0.3s ease;
        }

        .owl-dot.active {
            background: var(--primary-yellow) !important;
            transform: scale(1.2);
        }

        /* Quick Links */
        .quick-links {
            padding: 60px 0;
            background: var(--white);
        }

        .links-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .link-card {
            background: var(--cream);
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-top: 4px solid var(--primary-yellow);
        }

        .link-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .link-card i {
            font-size: 2.5rem;
            color: var(--primary-brown);
            margin-bottom: 20px;
        }

        .link-card h3 {
            margin-bottom: 15px;
            color: var(--dark-brown);
        }

        /* About Section */
        .about {
            padding: 80px 0;
            background: var(--light-yellow);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .about-img {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .about-img img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }

        .about-img:hover img {
            transform: scale(1.05);
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--dark-brown);
        }

        .about-text p {
            margin-bottom: 15px;
        }

        .mission-vision {
            margin-top: 30px;
            background: var(--white);
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            border-left: 4px solid var(--primary-brown);
        }

        .mission-vision h4 {
            color: var(--primary-brown);
            margin-bottom: 10px;
        }

        /* Facebook Embed */
        .facebook-embed {
            padding: 80px 0;
            background: var(--white);
        }

        .embed-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .embed-text {
            padding-right: 20px;
        }

        .embed-text h3 {
            font-size: 1.8rem;
            color: var(--dark-brown);
            margin-bottom: 20px;
        }

        .embed-text p {
            margin-bottom: 20px;
        }

        .fb-page {
            background: #f0f2f5;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            min-height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Enrollment CTA */
        .enrollment-cta {
            padding: 100px 0;
            background: linear-gradient(rgba(139, 69, 19, 0.8), rgba(139, 69, 19, 0.8)), url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
        }

        .enrollment-cta h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .enrollment-cta p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 40px;
        }

        /* Highlights Section */
        .highlights {
            padding: 80px 0;
            background: var(--cream);
        }

        .highlight-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .highlight-card {
            background: var(--white);
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border-top: 4px solid var(--primary-yellow);
        }

        .highlight-card h3 {
            color: var(--primary-brown);
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--light-yellow);
            font-size: 1.5rem;
        }

        .alumni-item {
            margin-bottom: 25px;
            padding-bottom: 20px;
            border-bottom: 1px dashed var(--light-brown);
        }

        .alumni-item:last-child {
            margin-bottom: 0;
            padding-bottom: 0;
            border-bottom: none;
        }

        .alumni-item h4 {
            color: var(--dark-brown);
            margin-bottom: 5px;
        }

        .alumni-meta {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 8px;
        }

        .event-item {
            margin-bottom: 20px;
            padding-bottom: 20px;
            border-bottom: 1px dashed var(--light-brown);
        }

        .event-item:last-child {
            margin-bottom: 0;
            padding-bottom: 0;
            border-bottom: none;
        }

        .event-item h4 {
            color: var(--dark-brown);
            margin-bottom: 5px;
        }

        .event-meta {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 5px;
            display: flex;
            align-items: center;
        }

        .event-meta i {
            margin-right: 8px;
            color: var(--primary-brown);
        }

        .achievement-item {
            margin-bottom: 20px;
        }

        .achievement-item h4 {
            color: var(--dark-brown);
            margin-bottom: 8px;
        }

        .view-more {
            display: inline-block;
            margin-top: 20px;
            color: var(--primary-brown);
            font-weight: 600;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .view-more:hover {
            color: var(--primary-yellow);
            text-decoration: underline;
        }

        /* Footer */
        footer {
            background: var(--dark-brown);
            color: white;
            padding: 60px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            color: white;
            margin-bottom: 20px;
            font-size: 1.3rem;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background: var(--primary-yellow);
        }

        .footer-column p {
            margin-bottom: 15px;
            opacity: 0.8;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: white;
            text-decoration: none;
            opacity: 0.8;
            transition: all 0.3s ease;
        }

        .footer-links a:hover {
            opacity: 1;
            color: var(--primary-yellow);
            padding-left: 5px;
        }

        .contact-info {
            list-style: none;
        }

        .contact-info li {
            margin-bottom: 15px;
            display: flex;
            align-items: flex-start;
        }

        .contact-info i {
            margin-right: 10px;
            color: var(--primary-yellow);
        }

        .social-media {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-media a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }

        .social-media a:hover {
            background: var(--primary-yellow);
            color: var(--dark-brown);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            opacity: 0.7;
        }

        /* Responsive Styles */
        @media (max-width: 1200px) {
            .hero-content h1 {
                font-size: 3rem;
            }
        }

        @media (max-width: 992px) {
            .about-content, .embed-container {
                grid-template-columns: 1fr;
            }
            
            .about-img {
                order: -1;
            }
            
            .embed-text {
                padding-right: 0;
                margin-bottom: 30px;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
        }

        @media (max-width: 768px) {
            .top-bar .container {
                flex-direction: column;
                text-align: center;
                gap: 10px;
            }
            
            .social-links {
                margin-top: 5px;
            }
            
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: white;
                flex-direction: column;
                gap: 0;
                box-shadow: 0 5px 10px rgba(0,0,0,0.1);
                padding: 20px 0;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links a {
                padding: 12px 20px;
            }
            
            .dropdown-content {
                position: static;
                box-shadow: none;
                display: none;
                padding-left: 20px;
            }
            
            .dropdown:hover .dropdown-content {
                display: none;
            }
            
            .dropdown.active .dropdown-content {
                display: block;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero-content h1 {
                font-size: 2rem;
            }
            
            .hero-content p {
                font-size: 1rem;
            }
            
            .hero-btns {
                flex-direction: column;
                gap: 15px;
            }
            
            .btn {
                width: 100%;
                max-width: 250px;
                margin: 0 auto;
            }
            
            .hero-carousel {
                height: 70vh;
            }
        }

        @media (max-width: 576px) {
            .section-title {
                font-size: 1.8rem;
            }
            
            .hero-carousel {
                height: 60vh;
            }
            
            .hero-content h1 {
                font-size: 1.8rem;
            }
            
            .enrollment-cta h2 {
                font-size: 2rem;
            }
            
            .enrollment-cta p {
                font-size: 1rem;
            }
        }
		
		/* Hero Carousel */
.hero-carousel {
    position: relative;
    height: 80vh;
    overflow: hidden;
}

.hero-slide {
    height: 100%;
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    position: relative;
}

.hero-slide:before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.4);
}

.hero-content {
    position: relative;
    z-index: 2;
    color: white;
    width: 100%;
    padding: 0 20px;
    text-align: center;
}

.owl-carousel .owl-stage-outer {
    height: 100%;
}

.owl-carousel .owl-item {
    height: 100%;
}

.owl-carousel .owl-stage {
    height: 100%;
}
/* Facebook Embed Styles */
.facebook-embed {
    padding: 80px 0;
    background: var(--white);
}

.embed-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    align-items: center;
}

.embed-text {
    padding-right: 20px;
}

.embed-text h3 {
    font-size: 1.8rem;
    color: var(--dark-brown);
    margin-bottom: 20px;
}

.embed-text p {
    margin-bottom: 20px;
}
    .fb-post-wrapper {
        display: flex;
        justify-content: center;
        margin: 2rem 0;
    }
    
    .fb-post-container {
        width: 100%;
        max-width: 500px;
        overflow: hidden;
        border-radius: 8px;
        box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    
    .fb-post-container iframe {
        min-height: 712px;
        border: none !important;
    }
    
    @media (max-width: 600px) {
        .fb-post-container {
            max-width: 100%;
            margin: 0 10px;
        }
        
        .fb-post-container iframe {
            min-height: 600px;
        }
    }
    </style>
</head>
<body>
<body>
  
 
    <!-- Top Bar -->
    <div class="top-bar">
        <div class="container">
            <div class="announcement-text">
                <span>Free admission test is ongoing!</span> Enrollment for School Year 2025-2026 is now open!
            </div>
        </div>
    </div>
    
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <img src="https://i.ibb.co/pvNz66p6/schools-logo.jpg" alt="St. Clare Schools Logo">
                    <div class="logo-text">
                        <h1>St. Clare Montessori</h1>
						<h1>St. Clare Science High School</h1>
                        <p>Home of the Highfliers and Achievers</p>
                    </div>
                </div>
                
                <div class="nav-links" id="navLinks">
                    <a href="#home">Home</a>
                    <div class="dropdown">
                        <a href="#about">About the School <i class="fas fa-caret-down"></i></a>
                        <div class="dropdown-content">
                            <a href="#history">Our History</a>
                            <a href="#mission">Mission & Vision</a>
                            <a href="#faculty">Faculty</a>
                            <a href="#facilities">Facilities</a>
                        </div>
                    </div>
                    <div class="dropdown">
                        <a href="#admission">Admission <i class="fas fa-caret-down"></i></a>
                        <div class="dropdown-content">
                            <a href="#requirements">Requirements</a>
                            <a href="#process">Process</a>
                            <a href="#tuition">Tuition Fees</a>
                            <a href="#scholarships">Scholarships</a>
                        </div>
                    </div>
                    <a href="#announcements">Announcements</a>
                    <a href="#circulars">School Circulars</a>
                    <a href="#contact">Contact</a>
                </div>
                
                <button class="mobile-menu-btn" id="mobileMenuBtn">
                    <i class="fas fa-bars"></i>
                </button>
            </nav>
        </div>
    </header>
    
    <!-- Hero Carousel -->
    <section class="hero-carousel owl-carousel owl-theme" id="home">
    <div class="hero-slide" style="background-image: url('https://i.ibb.co/hF7y7CtY/background-1.png');">
            <div class="hero-content">
                <h1>Welcome to St. Clare Montessori School <br>and St. Clare Science High School</h1>
                <h2>Home of the Highfliers and Achievers</h2>
                <div class="hero-btns">
                    <a href="#enrollment" class="btn">Enroll Now</a>
                    <a href="#tour" class="btn btn-brown">Virtual Tour</a>
                </div>
            </div>
        </div>
        
        <div class="hero-slide" style="background-image: url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');">
            <div class="hero-content">
                <h1>Excellence in Education</h1>
                <p>Preparing students for success in academics and life through our comprehensive programs</p>
                <div class="hero-btns">
                    <a href="#programs" class="btn">Our Programs</a>
                    <a href="#achievements" class="btn btn-brown">Student Achievements</a>
                </div>
            </div>
        </div>
        
        <div class="hero-slide" style="background-image: url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80');">
            <div class="hero-content">
                <h1>Join Our Community</h1>
                <p>Become part of the highfliers and achievers</p>
                <div class="hero-btns">
                    <a href="#admission" class="btn">Admission Process</a>
                    <a href="#contact" class="btn btn-brown">Contact Us</a>
                </div>
            </div>
        </div>
		  <div class="hero-slide" style="background-image: url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80');">
		 </div>
    </section>
    
    <!-- Quick Links -->
    <section class="quick-links">
        <div class="container">
            <div class="links-grid">
                <div class="link-card">
                    <i class="fas fa-user-graduate"></i>
                    <h3>Enrollment</h3>
                    <p>Ready to join our community? Enroll your child for the upcoming academic year.</p>
                    <a href="#enrollment" class="btn btn-brown" style="margin-top: 15px;">Enroll Now</a>
                </div>
                
                <div class="link-card">
                    <i class="fas fa-calendar-alt"></i>
                    <h3>School Calendar</h3>
                    <p>Stay updated with important dates, events, and academic schedules.</p>
                    <a href="#calendar" class="btn btn-brown" style="margin-top: 15px;">View Calendar</a>
                </div>
                
                <div class="link-card">
                    <i class="fas fa-laptop-house"></i>
                    <h3>Virtual Tour</h3>
                    <p>Explore our campus facilities and learning environments from anywhere.</p>
                    <a href="#tour" class="btn btn-brown" style="margin-top: 15px;">Start Tour</a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">About Our School</h2>
            
            <div class="about-content">
                <div class="about-text">
                    <h3>Our History</h3>
                    <p>St. Clare Montessori School was conceptualized and established by Dr. Remedios G. Aquino, Education  Supervisor of  DepEd,  Rizal, from 1984 to 2002, and OIC-Asst. Schools Division Superintendent/Education  Supervisor-Science of the  Department of  Education,  Antipolo  City, from 2003 to November 2008, and her daughter, Mrs. Evangeline A. Revilla,  a former teacher of Assumption School, Antipolo City, in response to the educational thrust of providing quality education...</p>
                    
                    <div class="mission-vision">
                        <h4>Mission:</h4>
                        <p>To provide good quality and the most enriching educational experiences To bring out the best in each child, his full potential, and humanity.To develop Christian values along with the academic and social skills of the child.</p>
                        
                        <h4>Vision:</h4>
                        <p>  “A community guided by Montessori Philosophy  where  children  are  fully  alive, continue to learn and develop into a complete and well functioning individual and helping himself  to  become,  to  love  and  to  be  a contributing member of the human family and community.“</p>
                    </div>
                    
                    <a href="#" class="btn" style="margin-top: 20px;">Learn More About Us</a>
                </div>
                
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1434030216411-0b793f4b4173?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Students in classroom">
                </div>
            </div>
        </div>
    </section>
    
   <!-- Facebook Embed Section -->
   
<section class="facebook-embed">
    <div class="container">
        <div class="embed-container">
            <div class="embed-text">
                <h3>Connect With Us</h3>
                <p>Stay updated with the latest news, events, and announcements from St. Clare Schools through our official Facebook page.</p>
                <p>See photos from school events, get important updates, and join our growing online community of parents, students, and alumni.</p>
                <a href="https://www.facebook.com/StClareAntipolo" class="btn" target="_blank" style="margin-top: 15px;">Visit Our Facebook Page</a>
            </div>
            
        
    <div class="fb-post-container">
        <iframe 
            src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FStClareAntipolo%2Fposts%2Fpfbid02Q1zZewiYcQdYjcGr3v9BX1qrhaRfQRqhv6iAdA3m4b9nwcFV8zQipinimzBs3qzPl&show_text=true&width=500" 
            style="border:none;overflow:hidden;width:100%;min-height:712px;" 
            scrolling="no" 
            frameborder="0" 
            allowfullscreen="true" 
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share">
        </iframe>
    </div>


</div>

        </div>
    </div>
</section>
    <!-- Enrollment CTA -->
    <section class="enrollment-cta" id="enrollment">
        <div class="container">
            <h2>Ready to Join St. Clare Schools?</h2>
            <p>Give your child the gift of quality education in a nurturing environment that fosters both academic excellence and personal growth.</p>
            <a href="#" class="btn">Enroll Now</a>
            <a href="#" class="btn btn-brown" style="margin-left: 15px;">Schedule a Visit</a>
        </div>
    </section>
    
    <!-- Highlights Section -->
    <section class="highlights">
        <div class="container">
            <h2 class="section-title">School Highlights</h2>
            
            <div class="highlight-grid">
                <div class="highlight-card">
                    <h3>Alumni Spotlight</h3>
                    
                    <div class="alumni-item">
                        <h4>Dr. Maria Santos</h4>
                        <div class="alumni-meta">Class of 2010</div>
                        <p>Now a research scientist at the National Institute of Health, developing breakthrough treatments for rare diseases.</p>
                    </div>
                    
                    <div class="alumni-item">
                        <h4>Engr. James Reyes</h4>
                        <div class="alumni-meta">Class of 2008</div>
                        <p>Award-winning engineer working on sustainable energy solutions at a leading tech company.</p>
                    </div>
                    
                    <a href="#" class="view-more">View more alumni →</a>
                </div>
                
                <div class="highlight-card">
                    <h3>Upcoming Events</h3>
                    
                    <div class="event-item">
                        <h4>Parent-Teacher Conference</h4>
                        <div class="event-meta"><i class="far fa-calendar-alt"></i> June 10-12, 2023 | 8:00 AM - 5:00 PM</div>
                        <div class="event-meta"><i class="fas fa-map-marker-alt"></i> School Auditorium</div>
                    </div>
                    
                    <div class="event-item">
                        <h4>Annual School Festival</h4>
                        <div class="event-meta"><i class="far fa-calendar-alt"></i> July 15, 2023 | 9:00 AM - 4:00 PM</div>
                        <div class="event-meta"><i class="fas fa-map-marker-alt"></i> School Campus</div>
                    </div>
                    
                    <a href="#" class="view-more">View full calendar →</a>
                </div>
                
                <div class="highlight-card">
                    <h3>Recent Achievements</h3>
                    
                    <div class="achievement-item">
                        <h4>National Science Quiz Bee</h4>
                        <p>Our team won 1st place in the National Science Quiz Bee, competing against 50 schools nationwide.</p>
                    </div>
                    
                    <div class="achievement-item">
                        <h4>Robotics Competition</h4>
                        <p>Our robotics team secured 2nd place in the Regional Robotics Competition with their innovative design.</p>
                    </div>
                    
                    <a href="#" class="view-more">View all achievements →</a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>St. Clare Montessori School and St. Clare Science High School</h3>
                    <p>Where Quality Education Begins</p>
                    <div class="social-media">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#programs">
						    <!-- JavaScript Libraries -->
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/owl.carousel.min.js"></script>
    
    <script>
        // Initialize Owl Carousel
        $(document).ready(function(){
            $(".hero-carousel").owlCarousel({
                items: 1,
                loop: true,
                autoplay: true,
                autoplayTimeout: 5000,
                autoplayHoverPause: true,
                nav: true,
                dots: true,
                animateOut: 'fadeOut',
                navText: [
                    '<i class="fas fa-chevron-left"></i>',
                    '<i class="fas fa-chevron-right"></i>'
                ]
            });
            
            // Mobile menu toggle
            $('#mobileMenuBtn').click(function() {
                $('#navLinks').toggleClass('active');
            });
            
            // Dropdown toggle for mobile
            $('.dropdown > a').click(function(e) {
                if ($(window).width() <= 768) {
                    e.preventDefault();
                    $(this).parent().toggleClass('active');
                }
            });
        });
    </script>
	
</body>
</html>
