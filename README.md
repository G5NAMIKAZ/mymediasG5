# <!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minhas Redes Sociais</title>
    <style>
        :root {
            --bg-color: #f5f5f5;
            --card-color: white;
            --text-color: #333;
            --secondary-text: #666;
            --shadow: rgba(0, 0, 0, 0.1);
        }

        @media (prefers-color-scheme: dark) {
            :root {
                --bg-color: #121212;
                --card-color: #1e1e1e;
                --text-color: #f0f0f0;
                --secondary-text: #aaa;
                --shadow: rgba(0, 0, 0, 0.3);
            }
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            color: var(--text-color);
            transition: background-color 0.5s ease;
        }
        
        .container {
            background-color: var(--card-color);
            border-radius: 15px;
            box-shadow: 0 10px 30px var(--shadow);
            padding: 40px;
            width: 90%;
            max-width: 500px;
            text-align: center;
            transition: all 0.5s ease;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .container::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                45deg,
                #ff9a9e 0%,
                #fad0c4 10%,
                #fbc2eb 20%,
                #a6c1ee 30%,
                #84fab0 40%,
                #8fd3f4 50%,
                #ff9a9e 60%,
                #fad0c4 70%,
                #fbc2eb 80%,
                #a6c1ee 90%,
                #84fab0 100%
            );
            background-size: 200% 200%;
            animation: gradientBG 15s ease infinite;
            opacity: 0.1;
            z-index: -1;
            transition: opacity 0.5s ease;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .profile {
            margin-bottom: 30px;
            position: relative;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid;
            border-image: linear-gradient(45deg, #4a6fa5, #84fab0) 1;
            margin-bottom: 15px;
            transition: all 0.3s ease;
        }

        .profile-img:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
        }
        
        h1 {
            margin: 0;
            background: linear-gradient(45deg, #4a6fa5, #84fab0);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-size: 2rem;
        }
        
        p {
            color: var(--secondary-text);
            margin-bottom: 30px;
            transition: color 0.5s ease;
        }
        
        .social-links {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 12px 20px;
            border-radius: 8px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .social-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(255,255,255,0.1), rgba(255,255,255,0.3));
            z-index: -1;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .social-link:hover::before {
            opacity: 1;
        }
        
        .social-link i {
            margin-right: 10px;
            font-size: 20px;
        }
        
        .youtube { background: linear-gradient(45deg, #FF0000, #cc0000); }
        .tiktok { background: linear-gradient(45deg, #010101, #69C9D0); }
        .twitter { background: linear-gradient(45deg, #1DA1F2, #1d8cf2); }
        .twitch { background: linear-gradient(45deg, #9146FF, #6441a5); }
        .discord { background: linear-gradient(45deg, #5865F2, #404EED); }
        
        .social-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        footer {
            margin-top: 30px;
            font-size: 14px;
            color: var(--secondary-text);
            transition: color 0.5s ease;
        }

        .theme-toggle {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(0,0,0,0.1);
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            color: var(--text-color);
            transition: all 0.3s ease;
        }

        .theme-toggle:hover {
            background: rgba(0,0,0,0.2);
            transform: rotate(30deg);
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <div class="container">
        <button class="theme-toggle" id="themeToggle">
            <i class="fas fa-moon"></i>
        </button>

        <div class="profile">
            <!-- Substitua pela URL da sua foto -->
            <img src="https://cdn.discordapp.com/attachments/858724180795326497/1395450027370873044/ryder.jpeg?ex=687a7d9c&is=68792c1c&hm=2d706872b7d315dec369d25e7cbf923b8b633f3189719b508496293520452d94&" alt="Minha Foto" class="profile-img">
            <h1>G5</h1>
            <p>Me siga!</p>
        </div>
        
        <div class="social-links">
            <!-- Substitua os links pelos seus -->
            <a href="https://www.youtube.com/@G5NAMIKAZ" class="social-link youtube">
                <i class="fab fa-youtube"></i> YouTube
            </a>
            
            <a href="https://www.tiktok.com/@g5namikaz?lang=pt-BR" class="social-link tiktok">
                <i class="fab fa-tiktok"></i> TikTok
            </a>
            
            <a href="https://x.com/G5NAMIKAZ" class="social-link twitter">
                <i class="fab fa-twitter"></i> Twitter
            </a>
            
            <a href="https://www.twitch.tv/g5namikaz" class="social-link twitch">
                <i class="fab fa-twitch"></i> Twitch
            </a>
            
            <a href="https://discord.gg/CJqAp2JW" class="social-link discord">
                <i class="fab fa-discord"></i> Discord
            </a>
        </div>
        
        <footer>
            ©2025 Henrique - Todos os direitos reservados
        </footer>
    </div>

    <script>
        // Botão de alternar tema
        const themeToggle = document.getElementById('themeToggle');
        const html = document.documentElement;
        
        themeToggle.addEventListener('click', () => {
            html.classList.toggle('dark-mode');
            
            // Alterna entre ícone de lua e sol
            const icon = themeToggle.querySelector('i');
            if (html.classList.contains('dark-mode')) {
                icon.classList.replace('fa-moon', 'fa-sun');
            } else {
                icon.classList.replace('fa-sun', 'fa-moon');
            }
        });
    </script>
</body>
</html>
