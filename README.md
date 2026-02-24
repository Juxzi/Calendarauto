# Planning Builder FR

Webapp statique (fichier HTML unique) prête pour un déploiement sur **GitHub Pages** via **GitHub Actions**.

## Structure

```text
/
├─ index.html
├─ README.md
├─ .gitignore
└─ .github/
   └─ workflows/
      └─ deploy-pages.yml
```

## Lancer en local

Depuis la racine du projet, utilisez un serveur statique simple.

### Option 1 — Node.js

```bash
npx serve .
```

### Option 2 — Python

```bash
python -m http.server 8000
```

Ensuite ouvrez l'URL affichée (souvent `http://localhost:3000` pour `serve` ou `http://localhost:8000` pour Python).

## Déploiement GitHub Pages

Le dépôt contient un workflow **Deploy to GitHub Pages** qui publie automatiquement à chaque push sur `main`.

### Réglage GitHub (une fois)

Dans le dépôt GitHub :

1. `Settings` → `Pages`
2. `Build and deployment` → `Source`
3. Choisir **GitHub Actions**

Si c'est déjà configuré, vérifiez juste que la source est bien **GitHub Actions**.

## URL du site

Après le premier déploiement réussi, l'URL est visible :

- dans `Settings` → `Pages`
- ou dans l'onglet `Actions`, job `deploy`, section environnement `github-pages`

Format habituel : `https://<owner>.github.io/<repo>/`.
