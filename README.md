# 🍀 Trèfle.Minotaure — Site de ressources

Paroles, guides pédagogiques et tablatures trilingues (FR · ES · EN).

## Structure des dossiers

```
trefleminotaure.github.io/
│
├── index.html              ← Page d'accueil (auto-générée depuis catalogue.json)
├── catalogue.json          ← SEUL FICHIER À MODIFIER pour ajouter une chanson
├── README.md
│
├── 000-survivors-remember-us/
│   ├── chanter.html
│   └── pedagogique.html
│
├── 001-ghosts-of-tolerance/
│   ├── chanter.html
│   ├── pedagogique.html
│   └── tablatures.html
│
├── 002-le-dernier-voyage/
│   ├── chanter.html
│   ├── pedagogique.html
│   └── tablatures.html
│
└── 003-berceuse-noire/
    ├── chanter.html
    ├── pedagogique.html
    └── tablatures.html
```

## Pour ajouter une nouvelle chanson

1. Créer un dossier `NNN-nom-de-la-chanson/`
2. Y déposer les fichiers HTML (chanter.html, pedagogique.html, tablatures.html)
3. Ouvrir `catalogue.json` et ajouter un bloc dans le tableau `chansons`
4. C'est tout — la page d'accueil se met à jour automatiquement

## Déploiement GitHub Pages

1. Dépôt nommé exactement `trefleminotaure.github.io`
2. Settings → Pages → Source : `main` branch, dossier `/` (root)
3. URL publique : `https://trefleminotaure.github.io`
