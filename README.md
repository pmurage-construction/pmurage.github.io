# pmurage.github.io
Professional Construction Portfolio - Estimator &amp; Project Coordinator
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Construction Professional Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Work+Sans:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #FF6B35;
            --secondary: #004E89;
            --dark: #1A1A1D;
            --light: #F7F7F7;
            --accent: #FFD23F;
            --concrete: #C5C3C6;
        }

        body {
            font-family: 'Work Sans', sans-serif;
            background: var(--dark);
            color: var(--light);
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(26, 26, 29, 0.95);
            backdrop-filter: blur(10px);
            padding: 20px 0;
            z-index: 1000;
            border-bottom: 3px solid var(--primary);
        }

        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav .logo {
            font-family: 'Bebas Neue', cursive;
            font-size: 32px;
            color: var(--primary);
            letter-spacing: 2px;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 40px;
        }

        nav a {
            color: var(--light);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--accent);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--dark) 0%, var(--secondary) 100%);
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
            background: 
                repeating-linear-gradient(
                    45deg,
                    transparent,
                    transparent 10px,
                    rgba(255, 107, 53, 0.03) 10px,
                    rgba(255, 107, 53, 0.03) 20px
                );
            animation: slide 20s linear infinite;
        }

        @keyframes slide {
            0% { transform: translateX(-100px) translateY(-100px); }
            100% { transform: translateX(0) translateY(0); }
        }

        .hero-content {
            text-align: center;
            z-index: 1;
            animation: fadeInUp 1s ease;
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

        .hero h1 {
            font-family: 'Bebas Neue', cursive;
            font-size: 80px;
            color: var(--accent);
            letter-spacing: 4px;
            margin-bottom: 20px;
            text-shadow: 4px 4px 0 var(--primary);
        }

        .hero .tagline {
            font-size: 24px;
            font-weight: 300;
            margin-bottom: 15px;
            color: var(--concrete);
        }

        .hero .experience {
            font-size: 20px;
            color: var(--primary);
            font-weight: 700;
            margin-bottom: 40px;
        }

        .cta-button {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 18px 45px;
            text-decoration: none;
            font-weight: 700;
            border-radius: 0;
            border: 3px solid var(--primary);
            transition: all 0.3s;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .cta-button:hover {
            background: transparent;
            color: var(--primary);
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(255, 107, 53, 0.3);
        }

        /* Section Styles */
        section {
            padding: 100px 40px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-family: 'Bebas Neue', cursive;
            font-size: 60px;
            color: var(--accent);
            margin-bottom: 50px;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100px;
            height: 4px;
            background: var(--primary);
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-text h3 {
            font-size: 28px;
            margin-bottom: 20px;
            color: var(--accent);
        }

        .about-text p {
            line-height: 1.8;
            margin-bottom: 20px;
            color: var(--concrete);
        }

        .about-image {
            background: var(--concrete);
            height: 400px;
            border: 5px solid var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            color: var(--dark);
            font-weight: 600;
            position: relative;
            overflow: hidden;
        }

        .about-image::before {
            content: '📸 YOUR PROFESSIONAL PHOTO';
            position: absolute;
            font-size: 16px;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .skill-card {
            background: var(--secondary);
            padding: 30px;
            border-left: 5px solid var(--primary);
            transition: transform 0.3s;
        }

        .skill-card:hover {
            transform: translateX(10px);
            background: rgba(0, 78, 137, 0.8);
        }

        .skill-card h4 {
            font-size: 20px;
            margin-bottom: 15px;
            color: var(--accent);
            font-weight: 700;
        }

        .skill-card ul {
            list-style: none;
        }

        .skill-card li {
            padding: 8px 0;
            color: var(--concrete);
            position: relative;
            padding-left: 25px;
        }

        .skill-card li::before {
            content: '▸';
            position: absolute;
            left: 0;
            color: var(--primary);
            font-weight: bold;
        }

        /* Projects Gallery */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            margin-top: 40px;
        }

        .project-card {
            background: var(--secondary);
            overflow: hidden;
            transition: transform 0.3s;
            border: 3px solid transparent;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary);
        }

        .project-image {
            height: 250px;
            background: var(--concrete);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--dark);
            font-weight: 600;
            position: relative;
            overflow: hidden;
        }

        .project-image::before {
            content: '📷 PROJECT IMAGE';
            position: absolute;
        }

        .project-info {
            padding: 25px;
        }

        .project-info h3 {
            font-size: 24px;
            margin-bottom: 10px;
            color: var(--accent);
        }

        .project-meta {
            display: flex;
            gap: 20px;
            margin-bottom: 15px;
            font-size: 14px;
            color: var(--concrete);
        }

        .project-meta span {
            background: var(--dark);
            padding: 5px 15px;
        }

        .project-info p {
            color: var(--concrete);
            line-height: 1.6;
        }

        /* Experience Timeline */
        .timeline {
            position: relative;
            padding-left: 50px;
            margin-top: 40px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 4px;
            background: var(--primary);
        }

        .timeline-item {
            position: relative;
            margin-bottom: 50px;
            padding-left: 40px;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -54px;
            top: 0;
            width: 16px;
            height: 16px;
            background: var(--accent);
            border: 4px solid var(--primary);
            border-radius: 50%;
        }

        .timeline-item h3 {
            font-size: 24px;
            color: var(--accent);
            margin-bottom: 5px;
        }

        .timeline-item .date {
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 10px;
        }

        .timeline-item p {
            color: var(--concrete);
            line-height: 1.8;
        }

        .timeline-item ul {
            margin-top: 15px;
            list-style: none;
        }

        .timeline-item li {
            padding: 5px 0;
            padding-left: 25px;
            position: relative;
            color: var(--concrete);
        }

        .timeline-item li::before {
            content: '▸';
            position: absolute;
            left: 0;
            color: var(--primary);
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            margin-top: 40px;
        }

        .contact-info h3 {
            font-size: 28px;
            color: var(--accent);
            margin-bottom: 30px;
        }

        .contact-item {
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .contact-item .icon {
            font-size: 24px;
            color: var(--primary);
        }

        .contact-item p {
            color: var(--concrete);
            font-size: 16px;
        }

        .contact-item a {
            color: var(--accent);
            text-decoration: none;
        }

        .contact-item a:hover {
            color: var(--primary);
        }

        .social-links {
            display: flex;
            gap: 20px;
            margin-top: 30px;
        }

        .social-links a {
            width: 50px;
            height: 50px;
            background: var(--secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: var(--accent);
            text-decoration: none;
            transition: all 0.3s;
            border: 2px solid transparent;
        }

        .social-links a:hover {
            background: var(--primary);
            border-color: var(--accent);
            transform: scale(1.1);
        }

        /* Footer */
        footer {
            background: var(--dark);
            padding: 40px;
            text-align: center;
            border-top: 3px solid var(--primary);
        }

        footer p {
            color: var(--concrete);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 50px;
            }

            .about-content,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            nav ul {
                display: none;
            }

            section {
                padding: 60px 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="logo">YOUR NAME</div>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>CONSTRUCTION PROFESSIONAL</h1>
            <p class="tagline">Estimator | Project Coordinator | Virtual Assistant</p>
            <p class="experience">3+ Years of Construction Experience</p>
            <a href="#contact" class="cta-button">Let's Build Together</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2 class="section-title">About Me</h2>
        <div class="about-content">
            <div class="about-text">
                <h3>Turning Blueprints Into Reality</h3>
                <p>
                    I'm a construction professional with 3 years of hands-on experience in estimating, 
                    project coordination, and construction management. My expertise spans from reading 
                    complex blueprints to delivering accurate cost estimates that help projects succeed.
                </p>
                <p>
                    I specialize in combining technical construction knowledge with modern digital tools 
                    to streamline workflows, improve accuracy, and deliver results. Whether it's a 
                    residential build or commercial project, I bring dedication and precision to every task.
                </p>
                <p>
                    Currently seeking remote opportunities where I can leverage my construction expertise 
                    to support teams from anywhere in the world.
                </p>
            </div>
            <div class="about-image">
                <!-- Replace with your actual photo -->
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <h2 class="section-title">Skills & Expertise</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <h4>Construction Estimating</h4>
                <ul>
                    <li>Blueprint Reading & Interpretation</li>
                    <li>Material Quantity Takeoffs</li>
                    <li>Cost Analysis & Budgeting</li>
                    <li>Vendor Coordination</li>
                    <li>Bid Preparation</li>
                </ul>
            </div>
            <div class="skill-card">
                <h4>Software & Tools</h4>
                <ul>
                    <li>PlanSwift (Learning)</li>
                    <li>Microsoft Excel (Advanced)</li>
                    <li>AutoCAD (Basic)</li>
                    <li>Bluebeam Revu</li>
                    <li>Google Workspace</li>
                </ul>
            </div>
            <div class="skill-card">
                <h4>Project Management</h4>
                <ul>
                    <li>Schedule Coordination</li>
                    <li>Document Management</li>
                    <li>Vendor Communication</li>
                    <li>Progress Tracking</li>
                    <li>Quality Control</li>
                </ul>
            </div>
            <div class="skill-card">
                <h4>Administrative Support</h4>
                <ul>
                    <li>Invoice Processing</li>
                    <li>Meeting Scheduling</li>
                    <li>Email Management</li>
                    <li>Report Generation</li>
                    <li>Data Entry</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2 class="section-title">Featured Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-image">
                    <!-- Add your project image here -->
                </div>
                <div class="project-info">
                    <h3>Commercial Building Renovation</h3>
                    <div class="project-meta">
                        <span>📍 Location</span>
                        <span>💰 $500K Budget</span>
                    </div>
                    <p>
                        Led cost estimation for 10,000 sq ft commercial renovation. Managed material 
                        takeoffs, coordinated with subcontractors, and delivered detailed bid packages 
                        that helped secure the project.
                    </p>
                </div>
            </div>

            <div class="project-card">
                <div class="project-image">
                    <!-- Add your project image here -->
                </div>
                <div class="project-info">
                    <h3>Residential Development</h3>
                    <div class="project-meta">
                        <span>📍 Location</span>
                        <span>🏘️ 15 Units</span>
                    </div>
                    <p>
                        Assisted in estimating costs for multi-unit residential development. Created 
                        comprehensive material lists, tracked project progress, and maintained 
                        documentation throughout construction phases.
                    </p>
                </div>
            </div>

            <div class="project-card">
                <div class="project-image">
                    <!-- Add your project image here -->
                </div>
                <div class="project-info">
                    <h3>Infrastructure Project</h3>
                    <div class="project-meta">
                        <span>📍 Location</span>
                        <span>⏱️ 12 Months</span>
                    </div>
                    <p>
                        Provided administrative support for large-scale infrastructure project. 
                        Coordinated schedules, processed invoices, and maintained communication 
                        between stakeholders and field teams.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
        <h2 class="section-title">Work Experience</h2>
        <div class="timeline">
            <div class="timeline-item">
                <h3>Construction Estimator / Coordinator</h3>
                <p class="date">2022 - Present | Company Name</p>
                <p>
                    Currently working as a construction estimator and project coordinator, handling 
                    multiple projects simultaneously and delivering accurate cost estimates.
                </p>
                <ul>
                    <li>Prepared detailed cost estimates for 20+ projects totaling $5M+</li>
                    <li>Reduced estimation errors by 15% through improved processes</li>
                    <li>Coordinated with 10+ subcontractors and vendors weekly</li>
                    <li>Managed project documentation and schedule tracking</li>
                </ul>
            </div>

            <div class="timeline-item">
                <h3>Junior Estimator</h3>
                <p class="date">2021 - 2022 | Company Name</p>
                <p>
                    Started career as junior estimator, learning blueprint reading, material takeoffs, 
                    and construction cost analysis.
                </p>
                <ul>
                    <li>Assisted senior estimators with 30+ residential projects</li>
                    <li>Performed material quantity takeoffs from blueprints</li>
                    <li>Created bid comparison spreadsheets and reports</li>
                    <li>Maintained vendor pricing databases</li>
                </ul>
            </div>

            <div class="timeline-item">
                <h3>Construction Assistant</h3>
                <p class="date">2020 - 2021 | Company Name</p>
                <p>
                    Gained foundational construction knowledge through hands-on site experience 
                    and administrative support roles.
                </p>
                <ul>
                    <li>Supported project managers with daily operations</li>
                    <li>Learned to read construction drawings and specifications</li>
                    <li>Assisted with material ordering and delivery coordination</li>
                    <li>Maintained project filing systems and documentation</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2 class="section-title">Let's Connect</h2>
        <div class="contact-grid">
            <div class="contact-info">
                <h3>Get In Touch</h3>
                <div class="contact-item">
                    <span class="icon">📧</span>
                    <p><a href="/cdn-cgi/l/email-protection#255c4a50570b4048444c4965405d44485549400b464a48"><span class="__cf_email__" data-cfemail="70091f05025e151d11191c301508111d001c155e131f1d">[email&#160;protected]</span></a></p>
                </div>
                <div class="contact-item">
                    <span class="icon">📱</span>
                    <p>+1 (555) 123-4567</p>
                </div>
                <div class="contact-item">
                    <span class="icon">📍</span>
                    <p>City, Country</p>
                </div>
                <div class="contact-item">
                    <span class="icon">💼</span>
                    <p><a href="https://linkedin.com/in/yourprofile" target="_blank">LinkedIn Profile</a></p>
                </div>

                <div class="social-links">
                    <a href="#" title="LinkedIn">🔗</a>
                    <a href="#" title="GitHub">💻</a>
                    <a href="#" title="Portfolio">📁</a>
                </div>
            </div>

            <div class="contact-info">
                <h3>Available For</h3>
                <ul style="list-style: none; line-height: 2.5;">
                    <li style="color: var(--concrete);">✓ Remote Construction Estimating</li>
                    <li style="color: var(--concrete);">✓ Virtual Construction Assistant Roles</li>
                    <li style="color: var(--concrete);">✓ Project Coordination Support</li>
                    <li style="color: var(--concrete);">✓ Freelance Estimating Projects</li>
                    <li style="color: var(--concrete);">✓ Consulting & Advisory</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Your Name - Construction Professional Portfolio</p>
        <p style="margin-top: 10px; font-size: 14px;">Built with dedication to quality and precision</p>
    </footer>

    <script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
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

        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all major sections
        document.querySelectorAll('.project-card, .skill-card,
