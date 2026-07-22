# 🍀 Trèfle.Minotaure — Convention de fichiers (v2)

## Règle fixe (obligatoire pour CHAQUE dossier de chanson)

Chaque dossier `NNN nom-de-la-chanson/` doit contenir exactement ces 6 fichiers :

```
index.html
chanter.html
pedagogique.html
tablatures_fr.html
tablatures_en.html
tablatures_es.html
```

Si une tablature n'est pas disponible (stems non exploitables), on n'omet PAS le fichier : on y met une copie de `tablatures-indisponible_fr.html` / `_en.html` / `_es.html`, renommée selon la langue. Comme ça, le fichier existe toujours au même endroit et le `catalogue.json` n'a plus besoin de savoir si une tablature manque.

Grâce à cette convention, **`catalogue.json` ne stocke plus les noms de fichiers** — seulement le champ `dossier`. Le fichier `index.html` principal reconstruit tous les liens automatiquement (`dossier/chanter.html`, `dossier/pedagogique.html`, etc.).

## Renommages à faire sur vos 4 dossiers existants

Vos dossiers 000, 006, 007, 009 utilisaient des noms de fichiers différents. Voici exactement quoi renommer :

**`000 9-11 survivor - remember us/`**
- `pédagogique.html` → renommer en `pedagogique.html` (enlever l'accent)
- ajouter `index.html` (page d'accueil de la chanson — à créer si elle n'existe pas encore)
- ajouter `tablatures_fr.html`, `tablatures_en.html`, `tablatures_es.html` (ou copier les pages "indisponible" si pas de tablature pour ce titre)

**`006 le dernier voyage/`**
- `tablatures.html` → renommer en `tablatures_fr.html`
- créer `tablatures_en.html` et `tablatures_es.html` (contenu réel ou page "indisponible")
- ajouter `index.html` si absent

**`007 berceuse noire/`**
- `tablatures.html` → renommer en `tablatures_fr.html`
- créer `tablatures_en.html` et `tablatures_es.html`
- ajouter `index.html` si absent

**`009 les fantomes de la tolérances/`**
- déjà `tablatures_fr.html` ✓ (rien à changer ici)
- créer `tablatures_en.html` et `tablatures_es.html`
- ajouter `index.html` si absent

## Pour les 9 chansons restantes (001 à 005, 008, 010 à 012)

Simplement respecter la convention dès le départ : les 6 fichiers, dans chaque dossier, dès leur création.

## Ajouter une nouvelle chanson (013, 014...)

1. Créer le dossier `NNN nom-de-la-chanson/`
2. Y mettre les 6 fichiers de la convention
3. Ajouter un bloc dans `catalogue.json` (copier un bloc existant, changer `id`, `titre`, `dossier`, et les métadonnées)
4. C'est tout — pas besoin de toucher à `index.html` principal

## Déploiement GitHub Pages

1. Dépôt `trefleminotaure` (compte `duboisstephan5-lgtm`)
2. Settings → Pages → Source : branche `main`, dossier `/` (root)
3. URL publique : `https://duboisstephan5-lgtm.github.io/trefleminotaure/`
