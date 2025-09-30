<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tharindu Piyumal - Software Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #fff;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .container::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);
            transform: rotate(45deg);
            animation: shine 8s infinite linear;
        }
        
        @keyframes shine {
            0% {
                transform: rotate(45deg) translateX(-100%);
            }
            100% {
                transform: rotate(45deg) translateX(100%);
            }
        }
        
        .content {
            position: relative;
            z-index: 1;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .greeting {
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: #4fc3f7;
            text-shadow: 0 0 10px rgba(79, 195, 247, 0.5);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
            100% {
                transform: scale(1);
            }
        }
        
        .name {
            font-size: 2.8rem;
            font-weight: 700;
            margin-bottom: 20px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4, #45b7d1, #96ceb4, #ffeaa7);
            background-size: 400% 100%;
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: gradient 8s ease infinite;
        }
        
        @keyframes gradient {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }
        
        .intro {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: #e0e0e0;
        }
        
        .portfolio-section {
            text-align: center;
            margin: 30px 0;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            transition: all 0.3s ease;
        }
        
        .portfolio-section:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .portfolio-text {
            font-size: 1.2rem;
            margin-bottom: 15px;
        }
        
        .portfolio-link {
            display: inline-block;
            background: linear-gradient(45deg, #4fc3f7, #01579b);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .portfolio-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: 0.5s;
        }
        
        .portfolio-link:hover::before {
            left: 100%;
        }
        
        .portfolio-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }
        
        .signature {
            text-align: center;
            margin-top: 30px;
            font-size: 1.3rem;
            color: #81c784;
            font-style: italic;
        }
        
        .emojis {
            text-align: center;
            margin-top: 20px;
            font-size: 2.5rem;
        }
        
        .emoji {
            display: inline-block;
            margin: 0 10px;
            animation: float 3s ease-in-out infinite;
        }
        
        .emoji:nth-child(2) {
            animation-delay: 0.5s;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-15px);
            }
            100% {
                transform: translateY(0);
            }
        }
        
        .tech-icons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }
        
        .tech-icon {
            font-size: 2.5rem;
            transition: all 0.3s ease;
        }
        
        .tech-icon:hover {
            transform: scale(1.3) rotate(10deg);
        }
        
        .fa-js {
            color: #f7df1e;
        }
        
        .fa-react {
            color: #61dafb;
        }
        
        .fa-python {
            color: #3776ab;
        }
        
        .fa-node-js {
            color: #68a063;
        }
        
        .fa-git-alt {
            color: #f05032;
        }
        
        .fa-database {
            color: #336791;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 25px;
            }
            
            .name {
                font-size: 2.2rem;
            }
            
            .greeting {
                font-size: 1.5rem;
            }
            
            .intro {
                font-size: 1.1rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="content">
            <div class="header">
                <h1 class="greeting">Hi there 👋</h1>
                <h2 class="name">I'm Tharindu Piyumal </h2>
            </div>
            
            <div class="intro">
                <p>Software Engineer passionate about creating innovative solutions.</p>
            </div>
            
            <div class="portfolio-section">
                <p class="portfolio-text">Do you want to know about me? 🙃</p>
                <p class="portfolio-text">Just visit my Portfolio 👇</p>
                <a href="https://piyumalt.ct.ws/" class="portfolio-link" target="_blank">
                    <i class="fas fa-external-link-alt"></i> Explore My Portfolio
                </a>
            </div>
            
            <div class="tech-icons">
                <i class="fab fa-js tech-icon"></i>
                <i class="fab fa-react tech-icon"></i>
                <i class="fab fa-python tech-icon"></i>
                <i class="fab fa-node-js tech-icon"></i>
                <i class="fab fa-git-alt tech-icon"></i>
                <i class="fas fa-database tech-icon"></i>
            </div>
            
            <div class="signature">
                <p>Happy coding!</p>
            </div>
            
            <div class="emojis">
                <span class="emoji">👨‍💻</span>
                <span class="emoji">👩‍💻</span>
            </div>
        </div>
    </div>

    <script>
        // Add some interactive effects
        document.addEventListener('DOMContentLoaded', function() {
            const container = document.querySelector('.container');
            
            // Add mousemove effect
            document.addEventListener('mousemove', (e) => {
                const xAxis = (window.innerWidth / 2 - e.pageX) / 25;
                const yAxis = (window.innerHeight / 2 - e.pageY) / 25;
                container.style.transform = `rotateY(${xAxis}deg) rotateX(${yAxis}deg)`;
            });
            
            // Reset transform when mouse leaves
            document.addEventListener('mouseleave', () => {
                container.style.transform = 'rotateY(0deg) rotateX(0deg)';
            });
            
            // Add click effect
            container.addEventListener('click', function() {
                this.style.transform = 'scale(0.98)';
                setTimeout(() => {
                    this.style.transform = 'scale(1)';
                }, 150);
            });
        });
    </script>
</body>
</html>
