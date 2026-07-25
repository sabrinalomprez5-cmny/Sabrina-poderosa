# Site — Sabrina, Accompagnatrice en image

Site statique (HTML / CSS / JS pur, sans framework, sans dépendances à installer).

## Structure

```
.
├── index.html         → Accueil
├── a-propos.html      → À propos
├── prestations.html   → Prestations
├── contact.html       → Contact
├── css/style.css      → Styles
└── js/script.js       → Menu mobile, animations, formulaire de contact
```

## Modifier le contenu

Chaque page est un fichier `.html` indépendant : ouvrez-le avec n'importe
quel éditeur de texte (VS Code, par exemple) et modifiez directement les
textes entre les balises. Les couleurs et polices se règlent en un seul
endroit, en haut de `css/style.css` (variables `:root`).

## Formulaire de contact (Formspree)

Le formulaire envoie déjà les messages directement par email, via le
service gratuit [Formspree](https://formspree.io). Il ne reste qu'une
étape à faire vous-même (2 minutes, gratuit jusqu'à 50 messages/mois) :

1. Allez sur https://formspree.io et créez un compte avec l'adresse email
   où vous voulez recevoir les messages (ex : contact@sabrina-image.fr).
2. Créez un nouveau formulaire ("New Form"). Formspree vous donne une URL
   du type `https://formspree.io/f/abcd1234`.
3. Ouvrez `contact.html`, cherchez cette ligne :
   ```html
   <form id="contact-form" class="reveal" action="https://formspree.io/f/VOTRE_ID_FORMSPREE" method="POST">
   ```
   et remplacez `VOTRE_ID_FORMSPREE` par l'identifiant reçu (ex : `abcd1234`).
4. Sauvegardez, redéployez le site : c'est prêt.

Formspree vous enverra un email de confirmation la première fois qu'un
message est envoyé depuis le site (pour valider le formulaire) — c'est
normal, cliquez sur le lien de confirmation.

Un champ caché (`_gotcha`) est déjà en place pour filtrer les robots
spammeurs, sans imposer de captcha aux visiteuses.

## Déployer le site vous-même

### Option 1 — Vercel (le plus simple, gratuit)
1. Créez un compte sur vercel.com et connectez-le à GitHub.
2. Mettez ce dossier dans un nouveau dépôt GitHub.
3. Sur Vercel : "Add New Project" → sélectionnez le dépôt → Deploy.
   Aucune configuration n'est nécessaire (site 100% statique).

### Option 2 — Netlify
Glissez-déposez simplement ce dossier sur app.netlify.com/drop.

### Option 3 — Un hébergeur classique (OVH, o2switch, etc.)
Uploadez le contenu du dossier via FTP dans le répertoire public de votre
hébergement (souvent `www` ou `public_html`).

## Nom de domaine

Une fois déployé, vous pourrez relier votre propre nom de domaine
(ex : sabrina-image.fr) depuis les réglages du projet, chez Vercel ou
Netlify.
