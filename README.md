<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Business - Elliot Mooser | Suisse</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            color: #003366;
            background-color: #f5f5f5;
            line-height: 1.6;
            text-align: center;
            transition: background-color 0.3s, color 0.3s;
        }

        body.dark-mode {
            background-color: #121212;
            color: #e0e0e0;
        }

        header {
            background-color: #004e7c;
            color: white;
            padding: 50px 0;
            font-size: 1.5em;
            border-radius: 12px;
        }

        nav {
            background-color: white;
            padding: 15px 0;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
            border-radius: 12px;
        }

        nav a {
            margin: 0 20px;
            text-decoration: none;
            color: #004e7c;
            font-weight: bold;
            transition: color 0.3s, transform 0.3s;
        }

        nav a:hover {
            color: #007BFF;
            transform: scale(1.1);
        }

        main {
            padding: 60px 20px;
            max-width: 1200px;
            margin: 30px auto;
            background-color: #ffffff;
            border-radius: 16px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            opacity: 1;
            transform: translateY(0);
            transition: opacity 1s ease-out, transform 1s ease-out;
        }

        main.dark-mode {
            background-color: #1e1e1e;
        }

        section {
            margin-bottom: 50px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .service-card {
            background-color: #ffffff;
            padding: 40px;
            border-radius: 16px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            color: #000000;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .service-card.dark-mode {
            background-color: #1e1e1e;
            color: #e0e0e0;
        }

        .button {
            display: inline-block;
            padding: 12px 25px;
            color: white;
            background-color: #00aaff;
            border-radius: 16px;
            text-decoration: none;
            transition: background-color 0.3s, transform 0.3s;
        }

        .button:hover {
            background-color: #0088cc;
            transform: scale(1.05);
        }

        .social-icons {
            margin-top: 20px;
        }

        .social-icons a {
            position: relative;
            display: inline-block;
            margin: 0 15px;
        }

        .social-icons a img {
            width: 40px;
            height: 40px;
            vertical-align: middle;
            transition: transform 0.3s, filter 0.3s;
        }

        .social-icons a img.dark-mode-icon {
            filter: invert(1);
        }

        .social-icons a img:hover {
            transform: rotate(360deg);
        }

        .social-icons a::after {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 10px;
            height: 10px;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.8), transparent);
            border-radius: 50%;
            transform: scale(0);
            transition: transform 0.3s ease-in-out;
        }

        .social-icons a:active::after {
            transform: scale(4);
        }

        .toggle-dark-mode {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #00aaff;
            color: white;
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            font-size: 1.5em;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background-color 0.3s;
        }

        .toggle-dark-mode:hover {
            background-color: #0088cc;
        }

        .toggle-dark-mode::before {
            content: "\26AB"; /* Cercle noir */
            font-size: 1.5em;
        }

        footer {
            background-color: #004e7c;
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 -2px 4px rgba(0, 0, 0, 0.1);
            margin-top: 30px;
            border-radius: 16px;
        }

        .counter {
            font-size: 1.2em;
            margin: 20px 0;
        }

        .social-footer {
            background-color: #121212;
            color: #d0d0d0;
            padding: 30px;
            text-align: center;
            margin-top: 30px;
            border-radius: 16px;
        }

        .social-footer .social-icons a img {
            margin: 0 15px;
        }

        .social-footer p {
            margin-bottom: 15px;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
</head>
<body>

<header>
    <h1>Bienvenue sur Mon Business - Elliot Mooser</h1>
    <p>Votre service local en Suisse</p>
</header>

<nav>
    <a href="#services" onclick="smoothScroll('#services')">Services</a>
    <a href="#apropos" onclick="smoothScroll('#apropos')">À propos</a>
    <a href="#contact" onclick="smoothScroll('#contact')">Contact</a>
    <a href="#cv" onclick="smoothScroll('#cv')">CV</a>
</nav>

<main id="services">
    <h2>Nos Services</h2>
    <div class="grid">
        <div class="service-card">
            <h3>Baby-Sitting</h3>
            <p>Garde d'enfants de confiance pour assurer leur sécurité et leur divertissement.</p>
        </div>
        <div class="service-card">
            <h3>Mécanique</h3>
            <p>Services de réparation et d'entretien pour voitures et deux-roues.</p>
        </div>
        <div class="service-card">
            <h3>Services Divers</h3>
            <p>Des solutions adaptées à vos besoins spécifiques, quelle que soit la tâche.</p>
        </div>
    </div>
</main>

<aside id="apropos">
    <h2>À propos de Elliot Mooser</h2>
    <p>Je suis Elliot Mooser, passionné par la création de services de qualité en Suisse. Mon expérience me permet de fournir des solutions adaptées à vos besoins spécifiques.</p>
</aside>

<aside id="contact">
    <h2>Contactez Elliot Mooser</h2>
    <p>N'hésitez pas à me contacter pour plus d'informations sur mes services en Suisse.</p>
    <form>
        <input type="text" placeholder="Nom" required>
        <input type="email" placeholder="Email" required>
        <textarea placeholder="Message" required></textarea>
        <input type="submit" value="Envoyer">
    </form>
</aside>

<aside id="cv" class="cv">
    <h2>Mon CV</h2>
    <p>Vous pouvez télécharger mon CV ici :</p>
    <a href="cv_elliot_mooser.pdf" target="_blank">Télécharger le CV</a>
</aside>

<div class="social-footer">
    <p>Suivez-moi :</p>
    <div class="social-icons">
        <a href="https://www.instagram.com/elli6.t" target="_blank"><img src="https://img.icons8.com/ios-filled/50/ffffff/instagram-new--v1.png" alt="Instagram"></a>
        <a href="https://open.spotify.com/user/31vwwlxmvdjxynkxe5gmshsijrou" target="_blank"><img src="https://img.icons8.com/ios-filled/50/ffffff/spotify.png" alt="Spotify"></a>
        <a href="https://www.snapchat.com/add/e_mooser" target="_blank"><img src="https://img.icons8.com/ios-filled/50/ffffff/snapchat.png" alt="Snapchat"></a>
        <a href="https://www.facebook.com/MooserElliot" target="_blank"><img src="https://img.icons8.com/ios-filled/50/ffffff/facebook--v1.png" alt="Facebook"></a>
    </div>
</div>

<footer>
    <p>&copy; 2025 Elliot Mooser. Tous droits réservés.</p>
    <p class="counter">Nombre de vues : <span id="viewCount">0</span></p>
</footer>

<button class="toggle-dark-mode" onclick="toggleDarkMode()"></button>

<script>
    function smoothScroll(target) {
        document.querySelector(target).scrollIntoView({ behavior: 'smooth' });
    }

    function toggleDarkMode() {
        document.body.classList.toggle('dark-mode');
        document.querySelectorAll('.social-icons img').forEach(img => {
            img.classList.toggle('dark-mode-icon');
        });
    }

    function handleScroll() {
        document.querySelectorAll('main, aside').forEach(el => {
            const rect = el.getBoundingClientRect();
            if (rect.top < window.innerHeight) {
                el.classList.add('visible');
            }
        });
    }

    function setViewCount() {
        let viewCount = parseInt(localStorage.getItem('viewCount') || '0');
        if (!document.cookie.includes('viewed=true')) {
            viewCount++;
            localStorage.setItem('viewCount', viewCount);
            document.cookie = "viewed=true; max-age=3600";  // 1 heure
        }
        document.getElementById('viewCount').innerText = viewCount;
    }

    document.addEventListener('DOMContentLoaded', () => {
        setViewCount();
        window.addEventListener('scroll', handleScroll);
        handleScroll();  // Initial check to show elements already in view
    });
</script>

</body>
</html>
