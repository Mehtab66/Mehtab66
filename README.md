<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mehtab Ahmed - Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #f0f6fc;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .container {
            background: rgba(13, 17, 23, 0.85);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            border: 1px solid #30363d;
            margin-top: 20px;
        }
        
        header {
            text-align: center;
            padding: 30px 0;
            position: relative;
            overflow: hidden;
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #58a6ff, #8a2be2);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: fadeIn 1.5s ease;
        }
        
        h2 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #58a6ff;
            position: relative;
            display: inline-block;
        }
        
        h2::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, transparent, #58a6ff, transparent);
            bottom: -5px;
            left: 0;
            animation: pulse 2s infinite;
        }
        
        h3 {
            color: #58a6ff;
            margin: 20px 0 15px;
            font-size: 1.5rem;
            border-left: 4px solid #58a6ff;
            padding-left: 10px;
        }
        
        p {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }
        
        .title {
            font-size: 1.4rem;
            color: #8b949e;
            margin-bottom: 30px;
            animation: slideIn 1s ease;
        }
        
        .animated-title {
            font-size: 1.5rem;
            color: #58a6ff;
            position: relative;
            display: inline-block;
            margin: 20px 0;
        }
        
        .animated-title::before {
            content: "Software Engineer at Revive Medical Technologies";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            color: transparent;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #ffd166, #06d6a0);
            -webkit-background-clip: text;
            background-clip: text;
            animation: rainbow 5s infinite;
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin: 20px 0;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            background: rgba(48, 54, 61, 0.5);
            padding: 10px 20px;
            border-radius: 50px;
            transition: transform 0.3s ease;
        }
        
        .contact-item:hover {
            transform: translateY(-5px);
            background: rgba(88, 166, 255, 0.2);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }
        
        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(48, 54, 61, 0.5);
            color: #f0f6fc;
            font-size: 1.5rem;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .social-link:hover {
            background: #58a6ff;
            transform: translateY(-5px) rotate(10deg);
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .skill-category {
            background: rgba(13, 17, 23, 0.7);
            padding: 20px;
            border-radius: 10px;
            border: 1px solid #30363d;
            transition: transform 0.3s ease;
        }
        
        .skill-category:hover {
            transform: translateY(-5px);
            border-color: #58a6ff;
            box-shadow: 0 5px 15px rgba(88, 166, 255, 0.2);
        }
        
        .skill-list {
            list-style-type: none;
        }
        
        .skill-list li {
            padding: 8px 0;
            border-bottom: 1px dashed #30363d;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .skill-list li:last-child {
            border-bottom: none;
        }
        
        .skill-list i {
            color: #58a6ff;
        }
        
        .experience, .projects, .education {
            margin: 30px 0;
        }
        
        .experience-item, .project-item {
            background: rgba(13, 17, 23, 0.7);
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
            border-left: 4px solid #58a6ff;
            transition: transform 0.3s ease;
        }
        
        .experience-item:hover, .project-item:hover {
            transform: translateX(5px);
        }
        
        .company, .project-name {
            color: #58a6ff;
            font-size: 1.3rem;
            margin-bottom: 5px;
        }
        
        .role {
            color: #8b949e;
            font-style: italic;
            margin-bottom: 10px;
        }
        
        .date {
            color: #8b949e;
            font-size: 0.9rem;
            margin-bottom: 10px;
        }
        
        .badge {
            display: inline-block;
            background: rgba(88, 166, 255, 0.2);
            color: #58a6ff;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            margin: 5px 5px 5px 0;
        }
        
        .stats {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 20px;
            margin: 40px 0;
        }
        
        .stat-item {
            text-align: center;
            background: rgba(48, 54, 61, 0.5);
            padding: 20px;
            border-radius: 10px;
            flex: 1;
            min-width: 200px;
            transition: transform 0.3s ease;
        }
        
        .stat-item:hover {
            transform: scale(1.05);
            background: rgba(88, 166, 255, 0.2);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #58a6ff;
            margin-bottom: 10px;
        }
        
        .snake-container {
            text-align: center;
            margin: 40px 0;
            padding: 20px;
            background: rgba(13, 17, 23, 0.7);
            border-radius: 10px;
        }
        
        .snake-animation {
            font-family: monospace;
            font-size: 16px;
            line-height: 1.2;
            color: #58a6ff;
            margin: 20px auto;
            max-width: 500px;
            overflow: hidden;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideIn {
            from { transform: translateY(-20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        @keyframes pulse {
            0% { opacity: 0.5; }
            50% { opacity: 1; }
            100% { opacity: 0.5; }
        }
        
        @keyframes rainbow {
            0% { filter: hue-rotate(0deg); }
            100% { filter: hue-rotate(360deg); }
        }
        
        @keyframes snakeMove {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }
        
        .snake {
            display: inline-block;
            animation: snakeMove 10s linear infinite;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #8b949e;
            font-size: 0.9rem;
            border-top: 1px solid #30363d;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .contact-info {
                flex-direction: column;
                align-items: center;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
            
            .stats {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Mehtab Ahmed</h1>
            <div class="title">Full Stack Developer</div>
            
            <div class="animated-title">Software Engineer at Revive Medical Technologies</div>
            
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>mohamadmehtabahmed@gmail.com</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <span>+92 3430519849</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>Rawalpindi, Pakistan</span>
                </div>
            </div>
            
            <div class="social-links">
                <a href="https://github.com/Mehtab66" class="social-link">
                    <i class="fab fa-github"></i>
                </a>
                <a href="https://linkedin.com/in/mehtab-ahmed58" class="social-link">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="#" class="social-link">
                    <i class="fab fa-twitter"></i>
                </a>
                <a href="#" class="social-link">
                    <i class="fab fa-dev"></i>
                </a>
            </div>
        </header>
        
        <section class="about">
            <h2>About Me</h2>
            <p>Passionate Full Stack Developer with expertise in React.js, Next.js, Node.js, and MongoDB. Experienced in building scalable web applications with REST APIs, WebSockets, and real-time features. Focused on performance, clean UI, and modern development practices.</p>
        </section>
        
        <section class="skills">
            <h2>Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>Frontend</h3>
                    <ul class="skill-list">
                        <li><i class="fab fa-react"></i> React.js</li>
                        <li><i class="fab fa-react"></i> React Native</li>
                        <li><i class="fas fa-code"></i> Next.js</li>
                        <li><i class="fab fa-js-square"></i> JavaScript (ES6+)</li>
                        <li><i class="fas fa-code"></i> TypeScript</li>
                        <li><i class="fab fa-html5"></i> HTML5</li>
                        <li><i class="fab fa-css3-alt"></i> Tailwind CSS</li>
                        <li><i class="fab fa-bootstrap"></i> Bootstrap</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3>Backend</h3>
                    <ul class="skill-list">
                        <li><i class="fab fa-node-js"></i> Node.js</li>
                        <li><i class="fas fa-server"></i> Express.js</li>
                        <li><i class="fas fa-code"></i> RESTful APIs</li>
                        <li><i class="fas fa-bolt"></i> WebSockets</li>
                        <li><i class="fas fa-database"></i> MongoDB</li>
                        <li><i class="fas fa-database"></i> MySQL</li>
                        <li><i class="fas fa-database"></i> Redis</li>
                        <li><i class="fas fa-database"></i> Firebase Firestore</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3>DevOps & Tools</h3>
                    <ul class="skill-list">
                        <li><i class="fab fa-aws"></i> AWS (EC2, S3)</li>
                        <li><i class="fab fa-docker"></i> Docker</li>
                        <li><i class="fab fa-git-alt"></i> Git</li>
                        <li><i class="fas fa-rocket"></i> Vercel</li>
                        <li><i class="fas fa-server"></i> Render</li>
                        <li><i class="fas fa-code-branch"></i> CI/CD</li>
                        <li><i class="fas fa-fire"></i> Firebase Auth</li>
                        <li><i class="fas fa-tasks"></i> BullMQ</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3>Integrations</h3>
                    <ul class="skill-list">
                        <li><i class="fas fa-credit-card"></i> Stripe</li>
                        <li><i class="fas fa-sms"></i> Twilio</li>
                        <li><i class="fas fa-envelope"></i> Nodemailer</li>
                        <li><i class="fas fa-map-marked-alt"></i> Mapbox</li>
                        <li><i class="fas fa-shield-alt"></i> JWT Authentication</li>
                        <li><i class="fas fa-users-cog"></i> Role-Based Access Control</li>
                        <li><i class="fas fa-bell"></i> Real-Time Notifications</li>
                    </ul>
                </div>
            </div>
        </section>
        
        <section class="experience">
            <h2>Work Experience</h2>
            
            <div class="experience-item">
                <div class="company">DevEntia Tech</div>
                <div class="role">Full Stack Developer</div>
                <div class="date">January 2024 - Present</div>
                <p>Contributed to AI-powered, enterprise-grade apps using React.js, Next.js, Node.js, and MongoDB. Built scalable backend services and RESTful APIs optimized for performance and real-time updates.</p>
                <div>
                    <span class="badge">React.js</span>
                    <span class="badge">Next.js</span>
                    <span class="badge">Node.js</span>
                    <span class="badge">MongoDB</span>
                    <span class="badge">Stripe</span>
                    <span class="badge">BullMQ</span>
                    <span class="badge">Firebase</span>
                    <span class="badge">Tailwind CSS</span>
                    <span class="badge">Zustand</span>
                    <span class="badge">AWS EC2</span>
                    <span class="badge">Vercel</span>
                </div>
            </div>
        </section>
        
        <section class="projects">
            <h2>Projects</h2>
            
            <div class="project-item">
                <div class="project-name">Scam Eye – AI-Powered Scam Detection Web App</div>
                <p>Developed an AI-powered web app using Next.js to detect scam messages, featuring a responsive UI with real-time interaction.</p>
                <div>
                    <span class="badge">Next.js</span>
                    <span class="badge">Firebase Auth</span>
                    <span class="badge">BullMQ</span>
                    <span class="badge">Stripe</span>
                    <span class="badge">Zustand</span>
                    <span class="badge">Tailwind CSS</span>
                </div>
            </div>
            
            <div class="project-item">
                <div class="project-name">Falkie – Full Stack Company Management System</div>
                <p>Built a comprehensive platform using the MERN stack for managing projects, clients, employees, and team communication.</p>
                <div>
                    <span class="badge">MongoDB</span>
                    <span class="badge">Express.js</span>
                    <span class="badge">React.js</span>
                    <span class="badge">Node.js</span>
                    <span class="badge">WebSockets</span>
                </div>
            </div>
            
            <div class="project-item">
                <div class="project-name">Social Pro– AI-Powered Social Media Automation</div>
                <p>Developed an AI-driven web app using the MERN stack for streamlined social media content creation, scheduling, and publishing.</p>
                <div>
                    <span class="badge">MERN Stack</span>
                    <span class="badge">GPT Integration</span>
                    <span class="badge">RESTful APIs</span>
                </div>
            </div>
            
            <div class="project-item">
                <div class="project-name">Real Time Chat Application</div>
                <p>Built a real-time announcement web app using the MERN stack with WebSocket integration.</p>
                <div>
                    <span class="badge">WebSockets</span>
                    <span class="badge">MERN Stack</span>
                    <span class="badge">Real-time</span>
                </div>
            </div>
        </section>
        
        <section class="education">
            <h2>Education</h2>
            
            <div class="experience-item">
                <div class="company">COMSATS University, Islamabad</div>
                <div class="role">Bachelors in Software Engineering</div>
            </div>
        </section>
        
        <section class="stats">
            <div class="stat-item">
                <div class="stat-number">10+</div>
                <div>Projects Completed</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">5+</div>
                <div>Technologies</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">100%</div>
                <div>Client Satisfaction</div>
            </div>
        </section>
        
        <section class="snake-container">
            <h2>My Contributions</h2>
            <div class="snake-animation">
                <pre class="snake">
+-+-+-+-+-+-+-+-+
|G|i|t|H|u|b| |C|o|n|t|r|i|b|u|t|i|o|n|s|
+-+-+-+-+-+-+-+-+
                </pre>
            </div>
        </section>
    </div>
    
    <footer>
        <p>© 2023 Mehtab Ahmed. All Rights Reserved.</p>
        <p>Made with ❤️ using HTML, CSS, and JavaScript</p>
    </footer>

    <script>
        // Simple animation for the snake
        document.addEventListener('DOMContentLoaded', function() {
            const snake = document.querySelector('.snake');
            let position = -100;
            
            function animateSnake() {
                position = (position + 2) % 100;
                snake.style.transform = `translateX(${position}%)`;
                requestAnimationFrame(animateSnake);
            }
            
            animateSnake();
        });
    </script>
</body>
</html>
