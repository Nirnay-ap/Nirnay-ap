<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nirnay Anidil Pathikkaran | Electronics Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: #0a0a0a;
            color: #e0e0e0;
            line-height: 1.6;
            overflow-x: hidden;
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1.5rem 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: #fff;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: #e0e0e0;
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }

        .nav-links a:hover {
            color: #10b981;
        }

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem;
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
            background: #0a0a0a;
            overflow: hidden;
        }

        .stars {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: white;
            border-radius: 50%;
            animation: shoot linear forwards;
        }

        @keyframes shoot {
            0% {
                transform: translateX(0) translateY(0);
                opacity: 1;
            }
            100% {
                transform: translateX(1000px) translateY(1000px);
                opacity: 0;
            }
        }

        .hero-content {
            max-width: 1200px;
            text-align: center;
            z-index: 1;
        }

        h1 {
            font-size: 5rem;
            font-weight: 900;
            margin-bottom: 2rem;
            color: #fff;
            font-style: italic;
            letter-spacing: -2px;
        }

        .cursor {
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }

        .subtitle {
            font-size: 1.8rem;
            color: #a0a0a0;
            margin-bottom: 3rem;
            font-style: italic;
            display: flex;
            gap: 2rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .subtitle span {
            position: relative;
        }

        .subtitle span::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: #10b981;
            transition: width 0.3s;
        }

        .subtitle span:hover::after {
            width: 100%;
        }

        .contact-info {
            font-size: 1rem;
            color: #808080;
            margin-bottom: 2rem;
        }

        .contact-info a {
            color: #10b981;
            text-decoration: none;
            margin: 0 0.5rem;
        }

        .contact-info a:hover {
            text-decoration: underline;
        }

        .skills {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 2rem;
        }

        .skill-tag {
            background: rgba(16, 185, 129, 0.1);
            border: 1px solid rgba(16, 185, 129, 0.3);
            padding: 0.75rem 1.5rem;
            border-radius: 50px;
            color: #10b981;
            font-weight: 600;
            transition: all 0.3s;
        }

        .skill-tag:hover {
            background: rgba(16, 185, 129, 0.2);
            transform: translateY(-2px);
        }

        .tech-stack {
            margin-top: 3rem;
            padding: 0;
            background: transparent;
            border-radius: 0;
            border: none;
        }

        .tech-stack h3 {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            color: #fff;
            font-weight: 600;
        }

        .tech-grid {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .tech-item {
            display: inline-flex;
            align-items: center;
            gap: 0.75rem;
            padding: 1rem 1.5rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 50px;
            transition: all 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-decoration: none;
            color: #e0e0e0;
            cursor: pointer;
            position: relative;
            z-index: 1;
        }

        .tech-item:visited {
            color: #e0e0e0;
        }

        .tech-item:hover {
            background: rgba(16, 185, 129, 0.1);
            transform: translateY(-5px);
            border-color: rgba(16, 185, 129, 0.3);
            box-shadow: 0 10px 30px rgba(16, 185, 129, 0.2);
        }

        .tech-item span {
            pointer-events: none;
        }

        .tech-item .tech-icon {
            pointer-events: none;
        }

        .tech-icon {
            width: 24px;
            height: 24px;
            background: transparent;
            border-radius: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #10b981;
            font-size: 1.2rem;
        }

        section {
            max-width: 1200px;
            margin: 0 auto;
            padding: 6rem 2rem;
        }

        h2 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 3rem;
            color: #fff;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 1rem;
            padding: 2rem;
            transition: all 0.3s;
            cursor: pointer;
            text-decoration: none;
            color: inherit;
            display: block;
        }

        .project-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.05);
            border-color: rgba(16, 185, 129, 0.5);
            box-shadow: 0 15px 40px rgba(16, 185, 129, 0.2);
        }

        .project-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #10b981, #3b82f6);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .project-header {
            display: flex;
            justify-content: space-between;
            align-items: start;
            margin-bottom: 1rem;
        }

        .project-title {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: #fff;
        }

        .project-date {
            color: #10b981;
            font-size: 0.9rem;
            font-weight: 600;
        }

        .project-description {
            color: #a0a0a0;
            margin-bottom: 1rem;
            line-height: 1.8;
        }

        .project-highlights {
            margin-top: 1rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #808080;
        }

        .project-highlights strong {
            color: #10b981;
        }

        .experience-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 1rem;
            padding: 2rem;
            margin-bottom: 2rem;
        }

        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: start;
            margin-bottom: 1.5rem;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .experience-title {
            flex: 1;
        }

        .company-name {
            font-size: 1.8rem;
            font-weight: 700;
            color: #fff;
            margin-bottom: 0.5rem;
        }

        .role-name {
            font-size: 1.2rem;
            color: #10b981;
            font-weight: 600;
        }

        .experience-period {
            text-align: right;
            color: #808080;
            font-size: 0.9rem;
        }

        .experience-description {
            list-style: none;
            padding: 0;
        }

        .experience-description li {
            color: #a0a0a0;
            padding-left: 1.5rem;
            position: relative;
            margin-bottom: 0.75rem;
            line-height: 1.8;
        }

        .experience-description li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: #10b981;
            font-weight: bold;
        }

        .carousel {
            position: relative;
            margin-top: 3rem;
            overflow: hidden;
            border-radius: 1rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            background: rgba(255, 255, 255, 0.02);
        }

        .carousel-track {
            display: flex;
            transition: transform 0.5s ease;
        }

        .carousel-item {
            min-width: 100%;
            aspect-ratio: 16/9;
            background: linear-gradient(135deg, rgba(16, 185, 129, 0.1) 0%, rgba(59, 130, 246, 0.1) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #606060;
            font-size: 1.2rem;
        }

        .carousel-controls {
            position: absolute;
            bottom: 1rem;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 0.5rem;
        }

        .carousel-dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.3);
            cursor: pointer;
            transition: all 0.3s;
        }

        .carousel-dot.active {
            background: #10b981;
            width: 30px;
            border-radius: 5px;
        }

        .education-section {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 1rem;
            padding: 2rem;
        }

        .education-header {
            display: flex;
            justify-content: space-between;
            align-items: start;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .university-name {
            font-size: 1.5rem;
            font-weight: 700;
            color: #fff;
        }

        .degree-info {
            color: #a0a0a0;
            margin-top: 0.5rem;
        }

        .gpa {
            color: #10b981;
            font-weight: 600;
            font-size: 1.1rem;
        }

        footer {
            text-align: center;
            padding: 3rem 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #606060;
        }

        footer a {
            color: #10b981;
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        .cert-badge {
            display: inline-block;
            background: rgba(16, 185, 129, 0.1);
            border: 1px solid rgba(16, 185, 129, 0.3);
            padding: 0.5rem 1rem;
            border-radius: 8px;
            color: #10b981;
            font-size: 0.9rem;
            margin-top: 1rem;
        }

        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            h2 { font-size: 2rem; }
            .subtitle { font-size: 1.2rem; }
            .project-grid { grid-template-columns: 1fr; }
            .nav-links { gap: 1rem; font-size: 0.9rem; }
            .experience-header { flex-direction: column; }
            .experience-period { text-align: left; }
        }
    </style>
</head>
<body>
    <nav>
        <div class="container">
            <a href="#" class="logo">Nirnay</a>
            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <section class="hero">
        <div class="stars" id="starsContainer"></div>
        <div class="hero-content">
            <h1>Hello, I'm Nirnay_</h1>
            <div class="subtitle">
                <span>Embedded Software Engineering</span>
                <span>PCB Design</span>
                <span>Firmware Development</span>
            </div>
            <div class="contact-info">
                <a href="https://github.com/Nirnay-ap" target="_blank">GitHub</a> |
                <a href="https://linkedin.com/in/nirnay-pathikkaran" target="_blank">LinkedIn</a>
            </div>
            
            <div class="tech-stack">
                <h3>Engineering with</h3>
                <div class="tech-grid">
                    <a href="https://oshwa.org/" target="_blank" class="tech-item">
                        <div class="tech-icon">🔧</div>
                        <span>Open-Source Hardware</span>
                    </a>
                    <a href="https://opensource.org/" target="_blank" class="tech-item">
                        <div class="tech-icon">💚</div>
                        <span>Open-Source Software</span>
                    </a>
                    <a href="https://www.altium.com/" target="_blank" class="tech-item">
                        <div class="tech-icon">⚡</div>
                        <span>Altium Designer</span>
                    </a>
                    <a href="https://www.microchip.com/mplab/mplab-x-ide" target="_blank" class="tech-item">
                        <div class="tech-icon">💻</div>
                        <span>MPLAB X IDE</span>
                    </a>
                    <a href="https://www.st.com/en/development-tools/stm32cubeide.html" target="_blank" class="tech-item">
                        <div class="tech-icon">🎯</div>
                        <span>STM32CubeIDE</span>
                    </a>
                    <a href="https://en.cppreference.com/" target="_blank" class="tech-item">
                        <div class="tech-icon">📟</div>
                        <span>C/Python</span>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <section id="about">
        <h2>ABOUT ME</h2>
        <div class="experience-card">
            <p style="color: #a0a0a0; line-height: 1.8; font-size: 1.1rem;">
                I'm an Electronics & Communication Engineering student with a passion for embedded systems and hardware design. My expertise lies in developing efficient firmware solutions, designing PCBs, and creating innovative IoT applications. I thrive on solving complex technical challenges and transforming ideas into functional, real-world solutions.
            </p>
            <p style="color: #a0a0a0; line-height: 1.8; font-size: 1.1rem; margin-top: 1rem;">
                With hands-on experience in industry-standard tools like Altium Designer, MPLAB X IDE, and STM32CubeIDE, I focus on building reliable, power-efficient systems. Whether it's optimizing communication protocols or designing complete hardware solutions, I'm committed to delivering quality engineering work that makes an impact.
            </p>
        </div>
    </section>

    <section id="experience">
        <h2>PROFESSIONAL EXPERIENCE</h2>
        <div class="experience-card">
            <div class="experience-header">
                <div class="experience-title">
                    <div class="company-name">MICROCHIP TECHNOLOGY</div>
                    <div class="role-name">Embedded Software Engineering Intern</div>
                </div>
                <div class="experience-period">
                    July 2025 – October 2025<br>
                    <span style="color: #10b981;">4 months</span>
                </div>
            </div>
            <ul class="experience-description">
                <li>Developed low-power SPI communication system for dual AVR microcontrollers with master-slave architecture, focusing on low-power embedded system design for battery-operated applications</li>
                <li>Implemented interrupt-driven data transfer mechanism to minimize CPU active time, achieving significant power savings through optimized sleep mode implementation</li>
                <li>Gained hands-on experience with MPLAB X IDE, debugging tools, and industry-standard development workflows for embedded systems</li>
                <li>Configured bidirectional communication with error detection and data validation protocols to ensure reliable data transmission</li>
            </ul>
        </div>

        <div class="experience-card">
            <div class="experience-header">
                <div class="experience-title">
                    <div class="company-name">TAKSHAK TECH FEST - MACE</div>
                    <div class="role-name">Head of Events (Infrastructure & Sponsorship)</div>
                </div>
                <div class="experience-period">
                    July 2024 – September 2024<br>
                    <span style="color: #10b981;">Ernakulam, Kerala</span>
                </div>
            </div>
            <ul class="experience-description">
                <li>Orchestrated complete infrastructure setup for India's largest tech fest with 20+ events across 3 days, managing budget of ₹5 lakhs for equipment and logistics</li>
                <li>Streamlined vendor management for sound, lighting, and staging equipment, negotiating contracts that saved 25% compared to previous year</li>
                <li>Secured corporate sponsorships by prospecting and pitching to a pipeline of 20+ companies, successfully converting 5 into key partners</li>
                <li>Collaborated with a 20-member marketing team to develop sponsorship packages and outreach strategies, contributing to overall fundraising goals</li>
            </ul>
        </div>
    </section>

    <section id="projects">
        <h2>FEATURED PROJECTS</h2>
        <div class="project-grid">
            <div class="project-card">
                <div class="project-icon">📡</div>
                <div class="project-header">
                    <div>
                        <div class="project-title">GHz/THz RF Designs and Simulations</div>
                    </div>
                    <div class="project-date">Ongoing</div>
                </div>
                <div class="project-description">
                    Currently working on high-frequency RF circuit design and electromagnetic simulations spanning GHz to THz range. Focus on signal integrity analysis, impedance matching, and electromagnetic compatibility for next-generation wireless communication systems.
                </div>
                <div class="project-highlights">
                    <strong>Highlights:</strong> RF circuit design, EM simulations, S-parameter analysis, antenna design, impedance matching networks, signal integrity optimization
                </div>
            </div>

            <div class="project-card">
                <div class="project-icon">⚡</div>
                <div class="project-header">
                    <div>
                        <div class="project-title">High-Speed Signaling Interfaces</div>
                    </div>
                    <div class="project-date">Ongoing</div>
                </div>
                <div class="project-description">
                    Designing and implementing high-speed digital communication interfaces including PCIe 4.0, USB 3.2, and Gigabit Ethernet. Focus on signal integrity, differential pair routing, impedance control, and EMI/EMC compliance for multi-Gbps data transmission.
                </div>
                <div class="project-highlights">
                    <strong>Highlights:</strong> PCIe 4.0 (16 GT/s), USB 3.2 (20 Gbps), Gigabit Ethernet, differential signaling, controlled impedance routing, eye diagram analysis, jitter optimization
                </div>
            </div>

            <a href="https://github.com/Nirnay-ap/Low-Power-SPI-Communication-for-Dual-AVR-MCUs" target="_blank" class="project-card">
                <div class="project-icon">⚡</div>
                <div class="project-header">
                    <div>
                        <div class="project-title">Low-Power SPI Communication System</div>
                    </div>
                    <div class="project-date">Oct 2025</div>
                </div>
                <div class="project-description">
                    Designed and implemented an interrupt-driven SPI communication architecture for dual AVR microcontrollers, optimized for battery-operated applications. The system minimizes CPU active time through efficient power management and sleep mode implementation.
                </div>
                <div class="project-highlights">
                    <strong>Highlights:</strong> Interrupt-driven architecture, bidirectional master-slave communication, error detection and validation, optimized power consumption, low-power mode implementation
                </div>
            </a>

            <a href="https://github.com/Nirnay-ap/24V_6Ah_Battery_Management_System" target="_blank" class="project-card">
                <div class="project-icon">🔋</div>
                <div class="project-header">
                    <div>
                        <div class="project-title">Battery Management System (BMS)</div>
                    </div>
                    <div class="project-date">May 2025</div>
                </div>
                <div class="project-description">
                    Developed a complete BMS solution for LFP battery packs featuring custom C firmware and I2C communication. Designed PCB schematic and layout using Altium Designer with focus on cost optimization while maintaining performance standards.
                </div>
                <div class="project-highlights">
                    <strong>Highlights:</strong> Voltage monitoring, temperature sensing, state-of-charge estimation algorithms, Altium Designer PCB design, I2C communication, optimized BOM cost reduction
                </div>
            </a>
        </div>
    </section>

    <section id="education">
        <h2>EDUCATION</h2>
        <div class="education-section">
            <div class="education-header">
                <div>
                    <div class="university-name">Mar Athanasius College of Engineering</div>
                    <div class="degree-info">Bachelor of Technology in Electronics & Communication Engineering</div>
                </div>
                <div class="experience-period">
                    Ernakulam, Kerala<br>
                    <span style="color: #10b981;">Expected 2025</span>
                </div>
            </div>
            <div class="cert-badge">🏆 Microsoft Azure AI Fundamentals (AI-900) Certified</div>
        </div>
    </section>

    <footer id="contact">
        <p>© 2025 Nirnay | 
            <a href="https://github.com/Nirnay-ap" target="_blank">GitHub</a> | 
            <a href="https://linkedin.com/in/nirnay-pathikkaran" target="_blank">LinkedIn</a>
        </p>
        <p style="margin-top: 1rem;">Passionate about Embedded Systems & Hardware Design • Open to Opportunities</p>
    </footer>

    <script>
        // Create shooting stars animation
        const starsContainer = document.getElementById('starsContainer');
        
        function createStar() {
            const star = document.createElement('div');
            star.className = 'star';
            
            // Random starting position
            const startX = Math.random() * window.innerWidth;
            const startY = Math.random() * window.innerHeight;
            
            star.style.left = startX + 'px';
            star.style.top = startY + 'px';
            
            // Random duration between 1-3 seconds
            const duration = Math.random() * 2 + 1;
            star.style.animationDuration = duration + 's';
            
            // Random size
            const size = Math.random() * 2 + 1;
            star.style.width = size + 'px';
            star.style.height = size + 'px';
            
            starsContainer.appendChild(star);
            
            // Remove star after animation
            setTimeout(() => {
                star.remove();
            }, duration * 1000);
        }
        
        // Create stars periodically
        setInterval(createStar, 100);
        
        // Smooth scroll for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', e => {
                e.preventDefault();
                const target = document.querySelector(anchor.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });
    </script>
</body>
</html>
