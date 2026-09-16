# Vitrine GitHub Pages pour plusieurs aperçus

Ce dossier est prêt à être copié dans **un seul dépôt GitHub** nommé par exemple `vitrine-sites`. Chaque aperçu possède son dossier et son `index.html` de redirection. L'adresse de Thaïland'erne sera `https://VOTRE-PSEUDO.github.io/vitrine-sites/thailanderne/`.

## Une seule fois

1. Créer le dépôt GitHub `vitrine-sites` et copier à sa racine `index.html` et le dossier `thailanderne/` de ce dossier.
2. Dans le dépôt, ouvrir **Settings → Pages → Build and deployment**.
3. Choisir **Deploy from a branch**, puis la branche `main`, le dossier `/(root)` et enregistrer.
4. La page d'accueil `https://VOTRE-PSEUDO.github.io/vitrine-sites/` liste les aperçus. Chaque lien de site garde son adresse, même si le tunnel change.

## Quand le tunnel Thaïland'erne change

1. Lancer `start-secure-preview.ps1` et copier le lien `https://...trycloudflare.com` affiché.
2. Sur GitHub, ouvrir `thailanderne/index.html`, cliquer sur le crayon, puis modifier uniquement cette ligne :

   ```js
   const TUNNEL_URL = "https://nouveau-tunnel.trycloudflare.com";
   ```

3. Cliquer sur **Commit changes**. La même adresse GitHub Pages redirigera vers le nouveau tunnel après publication.

## Pour ajouter un autre aperçu

Créer un autre dossier, par exemple `autre-site/`, y copier `thailanderne/index.html`, puis changer le titre et la ligne `TUNNEL_URL`. Ajouter un lien vers `./autre-site/` dans le fichier `index.html` à la racine.

Le dépôt reste accessible même si le tunnel est arrêté. Pour ouvrir l'aperçu, l'ordinateur, les conteneurs et le tunnel doivent être en marche. La redirection se fait dans le navigateur et nécessite JavaScript.

Documentation : [créer un site GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site), [publier depuis une branche](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).
