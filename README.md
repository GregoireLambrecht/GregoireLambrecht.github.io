# Page web personnelle (GitHub Pages + Jekyll)

GitHub Pages compile Jekyll automatiquement : il suffit de pousser les fichiers, aucune installation n'est nécessaire.

## Où modifier quoi

| Je veux changer…                       | Fichier                                   |
|----------------------------------------|-------------------------------------------|
| Nom, lien LinkedIn, e-mail, photo      | `_config.yml`                             |
| Ma présentation (anglais / français)   | `index.md` / `fr/index.md`                |
| Publications (à la une ou non)         | `_data/publications.yml`                  |
| Conférences et événements              | `_data/events.yml`                        |
| Titres des rubriques, poste, université| `_data/i18n.yml`                          |
| Pages vidéo des articles               | `_videos/<nom>.md` (une par langue)       |
| Couleurs, police, mise en page         | `assets/css/style.css`                    |

- **Photo** : dépose `assets/img/photo.jpg` puis mets `photo: /assets/img/photo.jpg` dans `_config.yml`.
- **Contenu différent selon la langue** : ajoute `lang: [fr]` (ou `[en]`) à une publication ou un événement.
- **Nouvelle page vidéo** : copie `_videos/example-paper.md`, change `title`, `youtube` (l'ID après `v=`)
  ou `video_file`, puis ajoute `video_en: /videos/<nom>/` à la publication correspondante.

## Mise en ligne

1. Crée sur GitHub un dépôt nommé exactement `GregoireLambrecht.github.io`.
2. Dans ce dossier :
   ```bash
   git init && git add . && git commit -m "Initial website"
   git branch -M main
   git remote add origin git@github.com:GregoireLambrecht/GregoireLambrecht.github.io.git
   git push -u origin main
   ```
3. Sur GitHub : *Settings → Pages → Source : Deploy from a branch → `main` / root*.
   Le site est en ligne sur `https://GregoireLambrecht.github.io` après une minute.

## Aperçu en local (optionnel)

```bash
gem install --user-install jekyll
jekyll serve      # puis ouvrir http://localhost:4000
```
