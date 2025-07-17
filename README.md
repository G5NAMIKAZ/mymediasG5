<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>G5 - Redes Sociais</title>
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
            padding: 20px;
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
            max-width: 600px;  /* Aumentei o tamanho máximo */
            text-align: center;
            transition: all 0.5s ease;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .profile {
            margin-bottom: 30px;
            position: relative;
        }
        
        .profile-img {
            width: 180px;  /* Aumentei o tamanho da foto */
            height: 180px;
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
            font-size: 2.5rem;  /* Aumentei o tamanho do título */
            background: linear-gradient(45deg, #4a6fa5, #84fab0);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        p {
            color: var(--secondary-text);
            margin-bottom: 30px;
            font-size: 1.2rem;  /* Aumentei o tamanho do texto */
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
            padding: 15px 25px;  /* Aumentei o padding dos botões */
            border-radius: 8px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            font-size: 1.1rem;  /* Aumentei o tamanho do texto dos botões */
            transition: all 0.3s ease;
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
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <div class="container">
        <div class="profile">
            <!-- Foto corrigida - removi os parâmetros extras da URL -->
            <img src="https://cdn.discordapp.com/attachments/858724180795326497/1395450027370873044/ryder.jpeg" alt="Foto do G5" class="profile-img">
            <h1>G5</h1>
            <p>Me siga nas redes sociais!</p>
        </div>
        
        <div class="social-links">
            <a href="https://www.youtube.com/@G5NAMIKAZ" target="_blank" rel="noopener noreferrer" class="social-link youtube">
                <i class="fab fa-youtube"></i> YouTube
            </a>
            
            <a href="https://www.tiktok.com/@g5namikaz?lang=pt-BR" target="_blank" rel="noopener noreferrer" class="social-link tiktok">
                <i class="fab fa-tiktok"></i> TikTok
            </a>
            
            <a href="https://x.com/G5NAMIKAZ" target="_blank" rel="noopener noreferrer" class="social-link twitter">
                <i class="fab fa-twitter"></i> Twitter
            </a>
            
            <a href="https://www.twitch.tv/g5namikaz" target="_blank" rel="noopener noreferrer" class="social-link twitch">
                <i class="fab fa-twitch"></i> Twitch
            </a>
            
            <a href="https://discord.gg/CJqAp2JW" target="_blank" rel="noopener noreferrer" class="social-link discord">
                <i class="fab fa-discord"></i> Discord
            </a>
        </div>
        
        <footer>
            ©2025 G5 - Todos os direitos reservados
        </footer>
    </div>
</body>
</html>
