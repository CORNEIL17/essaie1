<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Conteneurs Pro</title>
    <style>
        /* Styles existants... */

        /* Styles pour la navigation (inchangés) */
        nav {
            background-color: #343a40;
            color: white;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
        }

        nav ul li {
            margin-left: 20px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-size: 1rem;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: #ffcb05;
        }

        body {
            margin-top: 60px;
            font-family: 'Segoe UI', sans-serif;
            background-color: #f8f9fa;
            color: #333;
        }

        header {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 40px 20px 20px 20px;
            background: linear-gradient(135deg, #005b82, #007ea7);
            color: white;
            animation: fadeIn 1s ease-in;
        }

        header h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
        }

        header p {
            font-size: 1.2rem;
            max-width: 700px;
            margin-bottom: 20px;
        }

        .btn {
            background-color: #ffcb05;
            color: #000;
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            font-size: 1rem;
            cursor: pointer;
            transition: background 0.3s ease;
            box-shadow: 0 4px 6px rgba(0,0,0,0.2);
        }

        .btn:hover {
            background-color: #e6b800;
        }

        .images {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
        }

        .images img {
            width: 280px;
            height: 180px;
            object-fit: cover;
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
        }

        /* Styles pour la section "Nos Conteneurs" */
        .container-section {
            padding: 40px 20px;
            text-align: center;
        }

        .container-section h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #005b82;
        }

        .container-types {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .container-type {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            padding: 20px;
            width: 300px;
            text-align: left;
        }

        .container-type h3 {
            font-size: 1.5rem;
            margin-top: 0;
            margin-bottom: 10px;
            color: #007ea7;
        }

        .container-type p {
            font-size: 1rem;
            line-height: 1.6;
            margin-bottom: 15px;
        }

        .container-type .btn-secondary {
            background-color: #007ea7;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .container-type .btn-secondary:hover {
            background-color: #005b82;
        }

        /* Styles pour la section "Contact" */
        .contact-section {
            background-color: #e9ecef;
            padding: 40px 20px;
            text-align: center;
        }

        .contact-section h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #005b82;
        }

        .contact-details {
            max-width: 600px;
            margin: 0 auto;
            text-align: left;
        }

        .contact-details p {
            font-size: 1.1rem;
            line-height: 1.7;
            margin-bottom: 15px;
        }

        .contact-details strong {
            font-weight: bold;
            color: #343a40;
        }

        /* Styles pour la modale (inchangés) */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0; top: 0;
            width: 100%; height: 100%;
            background-color: rgba(0,0,0,0.6);
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: white;
            padding: 30px;
            border-radius: 12px;
            width: 90%;
            max-width: 500px;
            position: relative;
        }

        .modal-content h2 {
            margin-top: 0;
            margin-bottom: 15px;
        }

        .modal-content label {
            display: block;
            margin-top: 10px;
            font-weight: 600;
        }

        .modal-content input,
        .modal-content textarea {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 6px;
            font-size: 1rem;
        }

        .modal-content button {
            margin-top: 20px;
        }

        .close {
            position: absolute;
            top: 10px;
            right: 15px;
            font-size: 24px;
            cursor: pointer;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2rem;
            }

            header p {
                font-size: 1rem;
            }

            .images img {
                width: 90%;
                height: auto;
            }

            .container-types {
                flex-direction: column;
                align-items: center;
            }

            .container-type {
                width: 90%;
            }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">Conteneurs Pro</div>
        <ul>
            <li><a href="#">Accueil</a></li>
            <li><a href="#">Nos Conteneurs</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">À Propos</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <header>
        <h1>Conteneurs Pro</h1>
        <p>Vente et location de conteneurs maritimes partout en France. Qualité garantie, prix imbattables.</p>
        <button class="btn" onclick="openModal()">Demander un devis</button>
        <div class="images">
            <img src="https://cdn.pixabay.com/photo/2016/11/18/18/20/container-1838013_640.jpg" alt="Conteneur Standard" />
            <img src="https://cdn.pixabay.com/photo/2020/11/24/15/48/container-5761286_640.jpg" alt="Conteneur Frigorifique" />
            <img src="https://cdn.pixabay.com/photo/2017/09/22/14/54/container-house-2776231_1280.jpg" alt="Conteneur Maison" />
        </div>
    </header>

    <section class="container-section">
        <h2>Nos Conteneurs</h2>
        <p>Découvrez notre large gamme de conteneurs maritimes adaptés à tous vos besoins.</p>
        <div class="container-types">
            <div class="container-type">
                <h3>Conteneur Standard</h3>
                <p>Idéal pour le stockage sec et le transport de marchandises générales. Disponible en différentes tailles (20', 40', etc.). Robuste et sécurisé.</p>
                <a href="#" class="btn-secondary">En savoir plus</a>
            </div>
            <div class="container-type">
                <h3>Conteneur Frigorifique</h3>
                <p>Solution parfaite pour le transport et le stockage de produits sensibles aux températures. Maintien d'une température contrôlée et constante.</p>
                <a href="#" class="btn-secondary">En savoir plus</a>
            </div>
            <div class="container-type">
                <h3>Conteneur Aménagé</h3>
                <p>Conteneurs transformés pour des usages spécifiques : bureaux, habitations modulaires, ateliers, etc. Personnalisation sur mesure possible.</p>
                <a href="#" class="btn-secondary">En savoir plus</a>
            </div>
        </div>
    </section>

    <section class="contact-section">
        <h2>Contactez-nous</h2>
        <p>Notre équipe est à votre disposition pour répondre à toutes vos questions et vous fournir un devis personnalisé.</p>
        <div class="contact-details">
            <p><strong>Adresse e-mail :</strong> <a href="mailto:contact@conteneurspro.fr">contact@conteneurspro.fr</a></p>
            <p><strong>Téléphone :</strong> <a href="tel:+33123456789">+33 1 23 45 67 89</a></p>
            <p>N'hésitez pas à nous contacter via le formulaire de demande de devis ou par téléphone.</p>
        </div>
    </section>

    <div class="modal" id="quoteModal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h2>Demande de devis</h2>
            <form onsubmit="envoyerDemande(event)">
                <label for="name">Nom complet</label>
                <input type="text" id="name" required>

                <label for="email">Adresse email</label>
                <input type="email" id="email" required>

                <label for="phone">Téléphone</label>
                <input type="tel" id="phone" required>

                <label for="message">Votre demande</label>
                <textarea id="message" rows="4" placeholder="Quel type de conteneur ? Livraison où ?"></textarea>

                <button class="btn" type="submit">Envoyer</button>
            </form>
        </div>
    </div>

    <script>
        /* JavaScript (inchangé) */
        function openModal() {
            document.getElementById('quoteModal').style.display = 'flex';
        }

        function closeModal() {
            document.getElementById('quoteModal').style.display = 'none';
        }

        function envoyerDemande(event) {
            event.preventDefault();
            alert("Merci ! Votre demande a bien été envoyée.");
            closeModal();
        }

        window.addEventListener('keydown', function(e) {
            if (e.key === "Escape") closeModal();
        });

        window.addEventListener('click', function(e) {
            if (e.target === document.getElementById('quoteModal')) closeModal();
        });
    </script>

</body>
</html>
