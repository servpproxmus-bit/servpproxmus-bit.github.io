<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Mon Site – Accueil</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      color: #222;
      background: #f5f5f5;
    }
    header {
      background: #222;
      color: #fff;
      padding: 15px 20px;
      position: sticky;
      top: 0;
      z-index: 10;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    header h1 { font-size: 1.1rem; }
    nav a {
      color: #fff;
      text-decoration: none;
      margin-left: 15px;
      font-size: 0.95rem;
    }
    nav a:hover { text-decoration: underline; }

    .hero {
      padding: 60px 20px;
      text-align: center;
      background: #ffffff;
    }
    .hero h2 {
      font-size: 2rem;
      margin-bottom: 10px;
    }
    .hero p {
      max-width: 600px;
      margin: 10px auto 25px;
    }
    .btn-primary {
      display: inline-block;
      padding: 10px 20px;
      border-radius: 4px;
      border: none;
      cursor: pointer;
      text-decoration: none;
      background: #222;
      color: #fff;
      font-weight: bold;
      font-size: 0.95rem;
    }

    section {
      padding: 40px 20px;
      max-width: 900px;
      margin: 0 auto;
      background: #fff;
      margin-top: 15px;
      border-radius: 6px;
    }
    section h3 {
      margin-bottom: 15px;
      font-size: 1.4rem;
    }
    section p {
      margin-bottom: 10px;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 15px;
      margin-top: 15px;
    }
    .service-card {
      border: 1px solid #ddd;
      border-radius: 6px;
      padding: 15px;
      background: #fafafa;
    }
    .service-card h4 {
      margin-bottom: 8px;
      font-size: 1.1rem;
    }

    form {
      display: grid;
      gap: 10px;
      max-width: 500px;
    }
    label {
      font-weight: bold;
      font-size: 0.95rem;
    }
    input, textarea {
      padding: 8px;
      border-radius: 4px;
      border: 1px solid #ccc;
      font-size: 0.95rem;
      width: 100%;
    }
    textarea { min-height: 100px; resize: vertical; }

    footer {
      text-align: center;
      font-size: 0.85rem;
      color: #666;
      padding: 15px 10px 25px;
    }

    @media (max-width: 600px) {
      header {
        flex-direction: column;
        align-items: flex-start;
      }
      nav {
        margin-top: 8px;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Mon Site Professionnel</h1>
    <nav>
      <a href="#accueil">Accueil</a>
      <a href="#apropos">À propos</a>
      <a href="#services">Services</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main>
    <section id="accueil" class="hero">
      <h2>Bienvenue, je suis [Ton Nom]</h2>
      <p>
        J'aide les personnes et les organisations grâce à mes compétences en [ton activité principale].
        Sur ce site, tu trouveras qui je suis, ce que je propose et comment me contacter.
      </p>
      <a href="#contact" class="btn-primary">Me contacter</a>
    </section>

    <section id="apropos">
      <h3>À propos</h3>
      <p>
        Je m'appelle [Ton Nom] et je suis [ton métier / activité principale].
        J'ai une expérience de [X] ans dans les domaines de [domaine 1, domaine 2].
      </p>
      <p>
        Ma manière de travailler est basée sur l'écoute, la clarté et la confiance.
        Mon objectif : t'aider à obtenir des résultats concrets rapidement, sans prise de tête.
      </p>
    </section>

    <section id="services">
      <h3>Services</h3>
      <p>Voici quelques exemples de ce que je peux te proposer :</p>

      <div class="services-grid">
        <div class="service-card">
          <h4>Service 1</h4>
          <p>
            Description courte de ton premier service. Explique en quelques lignes le bénéfice pour ton client.
          </p>
        </div>
        <div class="service-card">
          <h4>Service 2</h4>
          <p>
            Description courte de ton deuxième service. Essaie de rester simple et concret.
          </p>
        </div>
        <div class="service-card">
          <h4>Service 3</h4>
          <p>
            Autre service ou accompagnement que tu proposes, en précisant pour qui c'est utile.
          </p>
        </div>
      </div>
    </section>

    <section id="contact">
      <h3>Contact</h3>
      <p>
        Tu peux me contacter directement par e-mail à l'adresse :
        <strong>[ton.email@example.com]</strong><br>
        ou en utilisant le formulaire ci-dessous :
      </p>

      <form>
        <div>
          <label for="nom">Nom</label>
          <input type="text" id="nom" name="nom" placeholder="Ton nom">
        </div>
        <div>
          <label for="email">E-mail</label>
          <input type="email" id="email" name="email" placeholder="ton.email@example.com">
        </div>
        <div>
          <label for="message">Message</label>
          <textarea id="message" name="message" placeholder="Écris ton message ici..."></textarea>
        </div>
        <button type="submit" class="btn-primary">Envoyer</button>
      </form>
      <p style="margin-top:10px; font-size:0.85rem; color:#666;">
        (Pour que le formulaire envoie réellement des e-mails, il faudra ajouter un petit service externe plus tard.)
      </p>
    </section>
  </main>

  <footer>
    &copy; <span id="year"></span> [Ton Nom] – Tous droits réservés.
  </footer>

  <script>
    // Met l'année automatique dans le footer
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
