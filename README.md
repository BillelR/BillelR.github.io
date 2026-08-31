# Portfolio — Data Engineer

Site portfolio statique (HTML/CSS/JS, sans dépendance ni build) présentant le parcours
Data Engineer d'OpenClassrooms sous forme de pipeline : 12 projets, leur statut
(validé / en cours / soutenance à planifier), les compétences évaluées et la stack technique.

## Aperçu de la structure

```
.
├── index.html      → contenu de la page (à personnaliser)
├── styles.css       → design (thème sombre "terminal/pipeline")
├── script.js        → menu mobile + filtres par catégorie
└── README.md
```

## Personnalisation avant mise en ligne

Recherchez ces éléments dans `index.html` et remplacez-les par vos informations réelles :

- `votre.email@exemple.com` → votre adresse e-mail
- Les liens `href="#"` (LinkedIn) → votre profil LinkedIn
- `[date de fin]` dans la section contact → date de fin d'alternance
- Les liens `https://github.com/BillelR/` dans chaque carte projet → lien vers le
  repository GitHub spécifique à ce projet, une fois qu'il existe
- La carte "Réalisez votre mission en entreprise" (stage SNCF) → à compléter avec le
  contexte réel, les technologies utilisées et les résultats obtenus

## Déployer sur GitHub Pages

1. Créez un repository sur GitHub (par exemple `portfolio` ou `BillelR.github.io`
   si vous voulez qu'il serve de page de profil principale).
2. Poussez ces trois fichiers (`index.html`, `styles.css`, `script.js`) à la racine du repository :
   ```bash
   git init
   git add index.html styles.css script.js README.md
   git commit -m "Portfolio Data Engineer"
   git branch -M main
   git remote add origin https://github.com/BillelR/NOM-DU-REPO.git
   git push -u origin main
   ```
3. Sur GitHub, allez dans **Settings → Pages**.
4. Dans **Source**, sélectionnez la branche `main` et le dossier `/root`, puis **Save**.
5. Après une à deux minutes, le site est accessible à l'adresse indiquée par GitHub
   (généralement `https://BillelR.github.io/NOM-DU-REPO/`, ou `https://BillelR.github.io/`
   si le repository s'appelle exactement `BillelR.github.io`).

## Ajouter un nouveau projet

Chaque projet est un bloc `<li class="node" data-cat="..." data-status="...">` dans
`index.html`, à l'intérieur de `<ol class="track" id="track">`. Copiez un bloc existant
et adaptez son contenu.

- `data-cat` : une des catégories utilisées par les filtres — `data`, `db`, `cloud`, `orch`, `ai`, `pm`
- `data-status` : `done` (validé), `wip` (en cours), ou `review` (soutenance à planifier)
