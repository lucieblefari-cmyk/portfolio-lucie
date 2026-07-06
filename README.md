# Mon portfolio

Site vitrine simple (HTML/CSS/JS, sans framework, sans installation nécessaire).

## 1. Modifier le contenu

Tout le texte à changer est repéré par le mot **MODIFIER** dans `index.html`.
Ouvrez ce fichier avec un éditeur de texte (Bloc-notes, VS Code, etc.) et remplacez :

- le nom, le métier, l'accroche (section `hero`)
- les 6 blocs de la galerie "Travaux" (dupliquez un bloc `.work-item` si vous avez plus de 6 photos, supprimez-en si vous en avez moins)
- le texte "À propos"
- les 3 services (dupliquez `.service-row` si besoin)
- l'email et les liens de contact

## 2. Ajouter vos photos

1. Mettez vos photos dans le dossier `images/` (formats `.jpg` ou `.png`, idéalement moins de 500 Ko chacune pour un chargement rapide).
2. Dans `index.html`, remplacez `images/travail-1.svg` par le nom exact de votre fichier, ex. `images/mon-projet.jpg`.
3. Faites de même pour `images/profil.svg` (votre photo de profil).
4. Vous pouvez supprimer les fichiers `.svg` une fois remplacés.

## 3. Tester en local

Double-cliquez simplement sur `index.html` pour l'ouvrir dans votre navigateur et voir le résultat.

## 4. Mettre le code sur GitHub

1. Créez un compte sur [github.com](https://github.com) si vous n'en avez pas.
2. Cliquez sur "New repository", nommez-le par exemple `mon-portfolio`, laissez-le public.
3. Sur votre ordinateur, dans le dossier du site, ouvrez un terminal et tapez :
   ```
   git init
   git add .
   git commit -m "Premier envoi du site"
   git branch -M main
   git remote add origin https://github.com/VOTRE-NOM/mon-portfolio.git
   git push -u origin main
   ```
   (remplacez `VOTRE-NOM` par votre nom d'utilisateur GitHub)

   Si vous préférez sans ligne de commande : sur la page du repository GitHub, utilisez le bouton "uploading an existing file" et glissez-déposez tous les fichiers.

## 5. Publier le site gratuitement (GitHub Pages)

1. Dans votre repository GitHub, allez dans **Settings** → **Pages**.
2. Dans "Branch", choisissez `main` et le dossier `/ (root)`, puis **Save**.
3. Après 1-2 minutes, votre site sera visible à l'adresse :
   `https://VOTRE-NOM.github.io/mon-portfolio/`

## 6. Ajouter votre propre nom de domaine (optionnel)

1. Achetez un nom de domaine chez un registrar (ex. OVH, Gandi, Namecheap, Google Domains) — comptez 10-15€/an.
2. Chez le registrar, dans la gestion DNS de votre domaine, ajoutez :
   - 4 enregistrements **A** pointant vers :
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - (si vous utilisez un sous-domaine type `www`) un enregistrement **CNAME** pointant vers `VOTRE-NOM.github.io`
3. Dans le repository GitHub, **Settings** → **Pages** → champ "Custom domain", entrez votre domaine et sauvegardez. GitHub crée alors un fichier `CNAME` automatiquement.
4. Cochez "Enforce HTTPS" une fois le certificat généré (peut prendre jusqu'à 24h).

Propagation DNS : les changements peuvent prendre de quelques minutes à 24-48h selon le registrar.
