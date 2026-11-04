# Page web personnelle — HTML simple

Aperçu en local : lance `python3 -m http.server` dans ce dossier, puis ouvre http://localhost:8000.

Après avoir ajouté une page, ajoute-la aussi à `sitemap.xml`. Ne supprime pas le fichier `google*.html` (vérification Search Console).

| Je veux changer…                     | Fichier                                    |
|--------------------------------------|--------------------------------------------|
| Version anglaise                     | `index.html`                               |
| Version française                    | `fr/index.html`                            |
| Couleurs, police, mise en page       | `assets/css/style.css`                     |
| Photo                                | `assets/img/` (puis changer `src` du `<img class="photo">`) |

- **Ajouter une publication / un événement** : copie un bloc `<li>…</li>` existant dans la bonne section.
- **Pages vidéo** : à créer plus tard dans `videos/` (une page par langue), avec un lien depuis la publication.
- Le fichier `.nojekyll` dit à GitHub de publier les fichiers tels quels.

## Mise en ligne

1. Dépôt GitHub nommé exactement `GregoireLambrecht.github.io`, en **public**.
2. Dans ce dossier :
   ```bash
   git init && git add . && git commit -m "Initial website"
   git branch -M main
   git remote add origin git@github.com:GregoireLambrecht/GregoireLambrecht.github.io.git
   git push -u origin main
   ```
3. *Settings → Pages → Deploy from a branch → `main` / root*.
   Site en ligne sur `https://gregoirelambrecht.github.io`.
