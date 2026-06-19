<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Daftuar Associate - Professional Legal & Tax Advisory</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.75;
            color: #e2e8f0;
            background: radial-gradient(circle at top, rgba(7, 16, 39, 0.96), #0a1120 55%);
            letter-spacing: 0.01em;
        }

        body::before {
            content: '';
            position: fixed;
            inset: 0;
            background: radial-gradient(circle at 20% 10%, rgba(252, 163, 17, 0.12), transparent 22%),
                        radial-gradient(circle at 80% 15%, rgba(255, 255, 255, 0.08), transparent 18%),
                        linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0));
            pointer-events: none;
            z-index: -1;
        }

        header {
            background: rgba(4, 14, 35, 0.95);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1240px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .logo {
            font-size: 1.9rem;
            font-weight: 800;
            letter-spacing: 0.2em;
            text-transform: uppercase;
            color: #f8fafc;
            display: inline-flex;
            flex-direction: column;
            align-items: flex-start;
            gap: 4px;
        }

        .advocate-name {
            font-size: 0.78rem;
            font-weight: 700;
            letter-spacing: 0.04em;
            text-transform: uppercase;
            margin-top: 0;
            color: #ffd88c;
            display: block;
        }

        nav a {
            color: rgba(248, 250, 252, 0.8);
            text-decoration: none;
            transition: color 0.2s ease, transform 0.2s ease;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.88rem;
        }

        nav a:hover {
            color: #fca311;
            transform: translateY(-2px);
        }

        .nav-group {
            display: flex;
            align-items: center;
            gap: 32px;
            flex: 1;
        }

        .nav-links-group {
            display: flex;
            gap: 28px;
            align-items: center;
        }

        .nav-links-group a {
            padding: 8px 12px;
            border-radius: 8px;
            transition: background-color 0.2s ease, color 0.2s ease, transform 0.2s ease;
        }

        .nav-links-group a:hover {
            background-color: rgba(252, 163, 17, 0.1);
        }

        nav ul {
            display: flex;
            gap: 32px;
            list-style: none;
            padding: 0;
            margin: 0;
        }

        nav li {
            display: list-item;
        }

        .hero {
            background: linear-gradient(180deg, rgba(12, 25, 52, 0.96) 0%, #08101f 100%);
            color: white;
            padding: 120px 20px 100px;
            text-align: center;
            min-height: 620px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            max-width: 720px;
            width: 100%;
        }

        .hero-text {
            text-align: center;
        }

        .hero::before,
        .hero::after {
            content: '';
            position: absolute;
            border-radius: 50%;
            filter: blur(80px);
            opacity: 0.55;
        }

        .hero::before {
            width: 620px;
            height: 620px;
            top: -140px;
            left: -100px;
            background: rgba(252, 163, 17, 0.18);
        }

        .hero::after {
            width: 400px;
            height: 400px;
            bottom: -120px;
            right: -70px;
            background: rgba(102, 126, 234, 0.18);
        }

        .hero h1 {
            font-family: 'Poppins', 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            font-size: clamp(3rem, 6vw, 5.2rem);
            font-weight: 800;
            max-width: 900px;
            margin-bottom: 24px;
            line-height: 1.02;
            letter-spacing: -0.06em;
            z-index: 1;
        }

        .hero p {
            font-size: 1.15rem;
            max-width: 680px;
            margin-bottom: 38px;
            opacity: 0.95;
            z-index: 1;
            letter-spacing: 0.01em;
        }

        .cta-button {
            background: linear-gradient(135deg, #f8b500, #fca311);
            color: #08101f;
            padding: 18px 48px;
            border: none;
            border-radius: 999px;
            font-size: 1rem;
            font-weight: 700;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            box-shadow: 0 20px 45px rgba(252, 163, 17, 0.24);
        }

        .cta-button:hover {
            transform: translateY(-4px);
            box-shadow: 0 24px 55px rgba(252, 163, 17, 0.3);
        }

        .nav-button {
            background: #fca311;
            color: #08101f;
            padding: 12px 26px;
            border-radius: 999px;
            font-weight: 700;
            transition: transform 0.25s ease, box-shadow 0.25s ease;
        }

        .nav-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 18px 30px rgba(252, 163, 17, 0.22);
        }

        .highlight-section,
        .about,
        .process,
        .services,
        .team,
        .testimonials,
        .contact {
            padding: 80px 20px;
        }

        section {
            max-width: 1240px;
            margin: 0 auto;
        }

        h2 {
            font-size: clamp(2.2rem, 3vw, 3rem);
            margin-bottom: 20px;
            text-align: center;
            color: #f8fafc;
        }

        .section-intro {
            max-width: 720px;
            margin: 0 auto 50px;
            color: #d2dce8;
            text-align: center;
            font-size: 1rem;
            line-height: 1.85;
        }

        .highlight-section {
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 32px;
            box-shadow: 0 30px 70px rgba(2, 9, 28, 0.35);
        }

        .highlight-grid {
            display: grid;
            gap: 24px;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
        }

        .highlight-card {
            background: rgba(255,255,255,0.06);
            border-radius: 28px;
            padding: 32px;
            box-shadow: 0 18px 45px rgba(15, 23, 42, 0.14);
            border: 1px solid rgba(255, 255, 255, 0.08);
            transition: transform 0.35s ease, box-shadow 0.35s ease;
            backdrop-filter: blur(10px);
        }

        .highlight-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 28px 70px rgba(15, 23, 42, 0.18);
        }

        .highlight-card span {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 56px;
            height: 56px;
            border-radius: 18px;
            background: rgba(252, 163, 17, 0.14);
            font-size: 1.45rem;
            margin-bottom: 18px;
        }

        .highlight-card h3 {
            font-size: 1.25rem;
            margin-bottom: 14px;
            color: #f8fafc;
            font-weight: 700;
        }

        .highlight-card p {
            color: #d2dce8;
            line-height: 1.9;
            letter-spacing: 0.01em;
        }

        .about {
            background: transparent;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 42px;
            align-items: center;
        }

        .about-text h3,
        .about-content h3 {
            font-size: 1.75rem;
            margin-bottom: 18px;
            color: #ffffff;
        }

        .about-text p,
        .about-content p {
            margin-top: 1rem;
            color: #d2dce8;
        }

        .about-card,
        .process-card,
        .service-card,
        .testimonial-card,
        .team-member,
        .contact-card,
        .form-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 28px;
            padding: 32px;
            box-shadow: 0 24px 70px rgba(2, 9, 28, 0.18);
            border: 1px solid rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(14px);
        }

        .process {
            background: transparent;
        }

        .process-grid {
            display: grid;
            gap: 24px;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
        }

        .process-card {
            text-align: left;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .process-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 34px 90px rgba(2, 9, 28, 0.22);
        }

        .process-step {
            font-size: 0.95rem;
            font-weight: 700;
            color: #fca311;
            margin-bottom: 18px;
            letter-spacing: 0.08em;
            text-transform: uppercase;
        }

        .process-card h3 {
            margin-bottom: 14px;
            color: #ffffff;
            font-weight: 700;
            letter-spacing: 0.01em;
        }

        .process-card p {
            color: #d2dce8;
            line-height: 1.85;
        }

        .testimonials {
            background: transparent;
        }

        .testimonials-grid {
            display: grid;
            gap: 24px;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        }

        .testimonial-card {
            transition: transform 0.25s ease;
        }

        .testimonial-card:hover {
            transform: translateY(-6px);
        }

        .testimonial-card p {
            margin-bottom: 20px;
            line-height: 1.9;
            color: rgba(248, 250, 252, 0.9);
        }

        .testimonial-card strong {
            color: #f8fafc;
            display: block;
            margin-top: 10px;
        }

        .services {
            background: transparent;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 28px;
        }

        .service-card {
            text-align: left;
            transition: transform 0.35s ease, box-shadow 0.35s ease;
        }

        .service-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 34px 90px rgba(2, 9, 28, 0.22);
        }

        .service-card h3 {
            font-size: 1.35rem;
            margin-bottom: 14px;
            color: #ffffff;
        }

        .service-card p {
            color: #d2dce8;
            line-height: 1.9;
        }

        .team {
            background: transparent;
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 28px;
        }

        .team-member {
            padding-bottom: 28px;
            transition: transform 0.3s ease;
        }

        .team-member:hover {
            transform: translateY(-6px);
        }

        .member-avatar {
            background: linear-gradient(135deg, #fca311 0%, #d97706 100%);
            height: 150px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.4rem;
            color: white;
        }

        .member-info {
            padding: 26px 24px 0;
        }

        .member-info h3 {
            margin-bottom: 8px;
            color: #f8fafc;
        }

        .member-info p {
            color: #cbd5e1;
            font-size: 0.95rem;
        }

        .contact {
            background: transparent;
        }

        .contact h2 {
            color: #f8fafc;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 32px;
        }

        .contact-card,
        .form-card {
            padding: 34px;
        }

        .contact-card h3,
        .form-card h3 {
            margin-bottom: 24px;
            color: #f8fafc;
        }

        .contact-item strong {
            color: #f8fafc;
        }

        .contact-item span,
        .contact-item a {
            color: #d2dce8;
        }

        .form-group label {
            color: #d2dce8;
            font-weight: 600;
            letter-spacing: 0.02em;
        }

        .form-group input,
        .form-group textarea {
            background: rgba(255,255,255,0.08);
            border: 1px solid rgba(255,255,255,0.12);
            color: #f8fafc;
            font-size: 0.98rem;
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: rgba(248,250,252,0.55);
        }

        .submit-btn {
            background: #fca311;
            color: #08101f;
            padding: 16px 40px;
            border-radius: 999px;
            font-size: 1rem;
            font-weight: 700;
            box-shadow: 0 24px 50px rgba(252, 163, 17, 0.22);
        }

        footer {
            background: transparent;
            color: #94a3b8;
            text-align: center;
            padding: 40px 20px;
            margin-top: 40px;
            border-top: 1px solid rgba(255,255,255,0.08);
        }

        footer p + p {
            margin-top: 10px;
        }

        .whatsapp-float {
            position: fixed;
            right: 24px;
            bottom: 24px;
            width: 68px;
            height: 68px;
            border-radius: 50%;
            background: #25d366;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 18px 40px rgba(37, 211, 102, 0.28);
            transition: transform 0.25s ease, box-shadow 0.25s ease;
            z-index: 1001;
        }

        .whatsapp-float:hover {
            transform: translateY(-4px);
            box-shadow: 0 22px 46px rgba(37, 211, 102, 0.32);
        }

        .whatsapp-float svg {
            width: 32px;
            height: 32px;
            fill: white;
        }

        .whatsapp-footer {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            color: #25d366;
            text-decoration: none;
            font-weight: 700;
            margin-top: 10px;
        }

        .whatsapp-footer:hover {
            color: #22c75a;
        }

        @media (max-width: 980px) {
            .about-content,
            .contact-content,
            .process-grid,
            .services-grid,
            .testimonials-grid,
            .team-grid {
                grid-template-columns: 1fr;
            }

            nav ul {
                justify-content: center;
            }
        }

        @media (max-width: 720px) {
            header {
                padding: 0.8rem 0;
            }

            .hero {
                min-height: 520px;
                padding: 90px 20px 70px;
            }

            .hero h1 {
                font-size: 2.85rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .contact-content {
                gap: 24px;
            }

            .contact-card,
            .form-card {
                padding: 26px;
            }
        }
        /* Entrance animations for headings and other elements */
        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(18px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .animate-on-scroll {
            opacity: 0;
            transform: translateY(18px);
            will-change: transform, opacity;
        }

        .animate-on-scroll.in-view {
            animation: fadeUp 640ms cubic-bezier(.2,.9,.2,1) both;
        }
    </style>
</head>
<body>
    <!-- Header/Navigation -->
    <header>
        <nav>
            <div class="logo">Daftuar Associate <span class="advocate-name">MR. ASHUTOSH KUMAR DAFTUAR</span></div>
            <div class="nav-group">
                <div class="nav-links-group">
                    <a href="#home">Home</a>
                    <a href="#about">About</a>
                </div>
                <ul>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#team">Team</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            <a href="#contact" class="nav-button">Hire Us</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <div class="hero-text">
                <h1>Welcome to Daftuar Associate</h1>
                <p>Professional legal and tax advisory tailored to protect and grow your business</p>
            </div>
            <a href="#contact" class="cta-button">Get Started</a>
        </div>
    </section>

    <!-- Process Section -->
    <section class="process" id="process">
        <h2>How We Work</h2>
        <div class="section-intro">From discovery to delivery, our process is built for clarity, speed, and meaningful impact across every phase.</div>
        <div class="process-grid">
            <div class="process-card">
                <div class="process-step">01</div>
                <h3>Discover</h3>
                <p>We begin with careful analysis of your business, goals, and market, then create a roadmap aligned to your needs.</p>
            </div>
            <div class="process-card">
                <div class="process-step">02</div>
                <h3>Design</h3>
                <p>We design practical, results-driven solutions that are both innovative and easy to implement.</p>
            </div>
            <div class="process-card">
                <div class="process-step">03</div>
                <h3>Deliver</h3>
                <p>We execute quickly, monitor performance, and refine the plan until your targets are met.</p>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials">
        <h2>Client Feedback</h2>
        <div class="section-intro">Trusted by clients for practical advice, strong delivery, and supportive collaboration.</div>
        <div class="testimonials-grid">
            <div class="testimonial-card">
                <p>"Daftuar Associate helped us reshape our strategy and gave us the confidence to move forward faster than expected."</p>
                <strong>— SHUBHAM SINHA </strong>
            </div>
            <div class="testimonial-card">
                <p>"Their team is responsive, professional, and deeply knowledgeable — a true partner in our growth."</p>
                <strong>— PRIYA SINHA </strong>
            </div>
            <div class="testimonial-card">
                <p>"Exceptional service and attention to detail. They handled our complex legal matters with professionalism and expertise."</p>
                <strong>— RAJESH KUMAR </strong>
            </div>
            <div class="testimonial-card">
                <p>"Best decision we made for our business. Their tax advisory strategies saved us significant costs while ensuring compliance."</p>
                <strong>— AMIT PATEL </strong>
            </div>
        </div>
    </section>

    <!-- Highlights Section -->
    <section class="highlight-section">
        <h2>Why Clients Choose Us</h2>
        <div class="section-intro">Daftuar Associate combines deep industry experience, smart planning, and operational excellence to deliver solutions that work today and grow stronger tomorrow.</div>
        <div class="highlight-grid">
            <div class="highlight-card">
                <span>✓</span>
                <h3>Result-Oriented Strategy</h3>
                <p>We create plans with measurable outcomes so your business can move forward with confidence.</p>
            </div>
            <div class="highlight-card">
                <span>💡</span>
                <h3>Practical Leadership</h3>
                <p>Our guidance blends real-world experience with modern practices to support your teams and operations.</p>
            </div>
            <div class="highlight-card">
                <span>⚡</span>
                <h3>Efficient Execution</h3>
                <p>Timely implementation and continuous improvement keep your projects on budget and on schedule.</p>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <h2>About Us</h2>
        <div class="about-content">
            <div class="about-text">
                <h3>Who We Are</h3>
                <p>Daftuar Associate is a professional legal and tax advisory firm led by Advocate Ashutosh Kumar Daftuar. We provide specialist legal counsel, tax planning, compliance advice and representation for businesses and individuals.</p>
                <p style="margin-top: 15px;">Our approach combines deep legal expertise, pragmatic tax strategy, and client-centred service to deliver clear, defensible outcomes.</p>
            </div>
            <div>
                <h3>Our Mission</h3>
                <p>To empower businesses through strategic consulting and innovative solutions that create lasting value and sustainable growth.</p>
                <h3 style="margin-top: 30px;">Our Vision</h3>
                <p>To be the trusted partner of choice for organizations seeking transformative business solutions and strategic guidance in an ever-changing market.</p>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <h2>Our Services</h2>
        <div class="services-grid">
            <div class="service-card">
                <h3>⚖️ Corporate & Commercial Law</h3>
                <p>Advising on company formation, commercial contracts, corporate compliance and board governance.</p>
            </div>
            <div class="service-card">
                <h3>🧾 Tax Advisory & Planning</h3>
                <p>Practical tax planning, optimisation and representation for corporate and individual tax matters.</p>
            </div>
            <div class="service-card">
                <h3>✅ Regulatory Compliance</h3>
                <p>Assistance with statutory compliance, licensing, filings and regulator interactions.</p>
            </div>
            <div class="service-card">
                <h3>🛡️ Litigation & Dispute Resolution</h3>
                <p>Representation in civil and commercial disputes, mediation and court proceedings.</p>
            </div>
            <div class="service-card">
                <h3>✒️ Contracts & Documentation</h3>
                <p>Drafting, reviewing and negotiating commercial agreements, employment and transaction documents.</p>
            </div>
            <div class="service-card">
                <h3>🔍 Due Diligence & Risk Review</h3>
                <p>Pre-transaction due diligence, risk assessments and compliance audits to support informed decisions.</p>
             <div class="service-card">
                <h3>GST Advice </h3>
                <p>Comprehensive GST advisory services, including compliance, planning, and representation for businesses.</p>
             </div>

                </h3>
        <div>

    </section>

    <!-- Team Section -->
    <section class="team" id="team">
        <h2>Our Team</h2>
        <div class="team-grid">
            <div class="team-member">
                <div class="member-avatar">👤</div>
                <div class="member-info">
                    <h3>Mayank Sharma</h3>
                    <p>Senior Consultant</p>
                </div>
            </div>
            <div class="team-member">
                <div class="member-avatar">👤</div>
                <div class="member-info">
                    <h3>Priya Patel</h3>
                    <p>Strategy Advisor</p>
                </div>
            </div>
            <div class="team-member">
                <div class="member-avatar">👤</div>
                <div class="member-info">
                    <h3>Rajesh Kumar</h3>
                    <p>Financial Analyst</p>
                </div>
            </div>
            <div class="team-member">
                <div class="member-avatar">👤</div>
                <div class="member-info">
                    <h3>Neha Gupta</h3>
                    <p>Business Development</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <h2>Get In Touch</h2>
        <div class="section-intro">Reach out for a free consultation and discover how Daftuar Associate can support your legal, compliance, and tax needs.</div>
        <div class="contact-content">
            <div class="contact-card">
                <h3>Contact Information</h3>
                <div class="contact-info">
                    <div class="contact-item">
                        <strong>📍 Address:</strong>
                        <span>Chamber No: 135, Red Building Civil Court<br>Gayaji Bihar</span>
                    </div>
                    <div class="contact-item">
                        <strong>📞 Phone:</strong>
                        <span>9709470964</span>
                    </div>
                    <div class="contact-item">
                        <strong>💬 WhatsApp:</strong>
                        <a href="https://wa.me/919709470964" target="_blank" rel="noopener">Send a message</a>
                    </div>
                    <div class="contact-item">
                        <strong>✉️ Email:</strong>
                        <span>ashutosh_daftuar@rediff.com</span>
                    </div>
                    <div class="contact-item">
                        <strong>⏰ Hours:</strong>
                        <span>Mon - Fri: 9:00 AM - 6:00 PM<br>Sat & Sun: Closed</span>
                    </div>
                </div>
            </div>
            <div class="form-card">
                <h3>Send us a Message</h3>
                <p style="margin-bottom: 18px; color: #cbd5e1;">Your message will open in WhatsApp for Advocate Ashutosh Kumar Daftuar.</p>
                <form id="contact-form">
                    <div class="form-group">
                        <label for="name">Your Name</label>
                        <input type="text" id="name" name="name" placeholder="Your full name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email Address</label>
                        <input type="email" id="email" name="email" placeholder="you@example.com" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Mobile Number</label>
                        <input type="tel" id="phone" name="phone" placeholder="Mobile number" required>
                    </div>
                    <div class="form-group">
                        <label for="preferred-date">Preferred Date</label>
                        <input type="date" id="preferred-date" name="preferred-date" required>
                    </div>
                    <div class="form-group">
                        <label for="address">Address</label>
                        <input type="text" id="address" name="address" placeholder="Your address" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" placeholder="How can we help you?" required></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Daftuar Associate. All rights reserved.</p>
        <p>Professional Legal & Tax Advisory | Legal & Tax Solutions</p>
        <a class="whatsapp-footer" href="https://wa.me/919709470964?text=hello%20DAFTUAR%20ASSOCIATE" target="_blank" rel="noopener">
            <span>📱</span>
            <span>Send Hello on WhatsApp</span>
        </a>
    </footer>
    <a class="whatsapp-float" href="https://wa.me/919709470964?text=hello%20DAFTUAR%20ASSOCIATE" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" aria-hidden="true">
            <path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.945.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.247 2.248 3.488 5.235 3.486 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.491-5.688-1.423l-6.305 1.654zm6.597-3.807c1.676.995 3.497 1.522 5.393 1.523 5.448 0 9.886-4.431 9.889-9.885.002-2.644-1.03-5.123-2.894-6.987-1.864-1.864-4.346-2.896-6.99-2.894-5.449 0-9.887 4.431-9.889 9.885-.001 1.956.592 3.864 1.711 5.417l-.999 3.648 3.608-.944zm11.387-5.464c-.297-.149-1.758-.867-2.03-.967-.273-.099-.472-.148-.672.149-.197.297-.761.967-.933 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.52.149-.173.198-.297.298-.495.099-.198.05-.372-.025-.521-.074-.149-.672-1.611-.92-2.207-.242-.579-.487-.5-.672-.51l-.573-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.262.489 1.693.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414-.074-.124-.272-.198-.57-.347z"/>
        </svg>
    </a>
    <script>
        document.addEventListener('DOMContentLoaded', function () {
            var form = document.getElementById('contact-form');
            form.addEventListener('submit', function (event) {
                event.preventDefault();
                var name = document.getElementById('name').value.trim();
                var email = document.getElementById('email').value.trim();
                var message = document.getElementById('message').value.trim();
                var phone = '919709470964';
                var text = 'Hello Advocate Ashutosh Kumar Daftuar,%0A%0A';
                text += '*Name:* ' + encodeURIComponent(name) + '%0A';
                text += '*Email:* ' + encodeURIComponent(email) + '%0A%0A';
                text += '*Message:* ' + encodeURIComponent(message) + '%0A%0A';
                text += 'Kindly respond to this request.';
                var url = 'https://wa.me/' + phone + '?text=' + text;
                window.open(url, '_blank');
            });

            // Entrance animations: observe headings and key cards
            var observerOptions = { root: null, rootMargin: '0px 0px -8% 0px', threshold: 0.12 };
            var observer = new IntersectionObserver(function(entries){
                entries.forEach(function(entry){
                    if (entry.isIntersecting) {
                        entry.target.classList.add('in-view');
                        observer.unobserve(entry.target);
                    }
                });
            }, observerOptions);

            var animatedItems = document.querySelectorAll('h1, h2, .highlight-card, .service-card, .team-member');
            animatedItems.forEach(function(el, i){
                el.classList.add('animate-on-scroll');
                // small stagger
                el.style.transitionDelay = (i * 70) + 'ms';
                observer.observe(el);
            });
        });
    </script>
</body>
</html>

