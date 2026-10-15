# CONTRIBUTING

Bienvenue sur EcoArt ! Ce guide explique comment contribuer de manière sûre et coordonnée au projet. L'objectif : protéger le code du site (HTML/CSS/ressources) tout en facilitant la collaboration des étudiants YouCode.

## Règles générales
- Ne modifiez pas les fichiers existants du site (HTML, CSS, images, polices) sans en discuter clairement dans une issue et avec l'avis d'un mainteneur.
- N'effectuez jamais de force-push, de réécriture d'historique ou de suppression de branches partagées.
- Ouvrez une issue pour tout changement majeur avant d'implémenter.

## Conventions de nommage des branches
- feature/<nom-court> — nouvelle fonctionnalité ou page (ex. `feature/homepage`).
- fix/<nom-court> — correction de bug (ex. `fix/header-alignment`).
- chore/<nom-court> — tâches non-fonctionnelles (ex. `chore/update-readme`).
- doc/<nom-court> — documentation.
- hotfix/<nom-court> — correctif urgent sur `main` (à éviter sauf cas critique).

Exemples :
- `feature/produits-grid`
- `fix/navigation-mobile`

## Synchroniser votre branche avec la dernière version de main
Avant d'ouvrir une pull request, assurez-vous que votre branche contient les derniers changements de `main`.
Commandes sûres recommandées (fusion locale) :

```bash
# Récupérer les dernières références du dépôt distant
git fetch origin

# Se positionner sur votre branche
git checkout feature/ma-branche

# Fusionner main dans votre branche
git merge origin/main

# Résoudre les conflits localement si nécessaire, tester et pousser
git add <fichiers_conflits_resolus>
git commit
git push origin feature/ma-branche
```

Explication :
- `git fetch origin` récupère les nouvelles références sans toucher vos branches.
- `git merge origin/main` applique les changements récents de `main` sur votre branche (créera un commit de merge si nécessaire).
- Résoudre les conflits localement évite que le maintainer doive modifier votre branche.

Remarque sur rebase :
- Le rebase (`git rebase origin/main`) est acceptable si vous comprenez ses implications, mais il réécrit l'historique. N'utilisez pas `git rebase` si vous devez ensuite forcer un push — nous interdisons les force-pushs sans approbation explicite du maintainer.

## Résolution des conflits sans perdre de travail
1. Lors d'un conflit après `git merge origin/main`, Git marquera les fichiers en conflit. Ouvrez-les, cherchez les délimitations `<<<<<<<`, `=======`, `>>>>>>>`.
2. Conservez les parties du code nécessaires des deux versions ou demandez conseil si vous n'êtes pas sûr.
3. Testez localement le site (ouvrir les pages HTML modifiées dans le navigateur) pour vérifier l'apparence.
4. Après résolution :

```bash
git add <fichiers_resolus>
git commit -m "Résolution de conflits: description courte"
git push origin feature/ma-branche
```

Important : ne supprimez ni n'écrasez le travail d'un autre contributeur sans accord.

## Directives de commits
- Commits petits et atomiques : un changement logique par commit.
- Message de commit : ligne titre courte (50 caractères max) puis description si nécessaire.
- Exemple :

```
Ajout : section "Nos produits"

- Ajout du HTML de la section produits
- Ajout des classes CSS de base (dans artisans.css si applicable)
```

## Pull Requests (PR)
Avant d'ouvrir une PR :
- Assurez-vous que votre branche est synchronisée avec `main` (voir plus haut).
- Testez localement les pages affectées.
- Optimisez les images (taille et résolution) avant d'ajouter des assets.

Dans la PR :
- Expliquez clairement le but du changement.
- Incluez des captures d'écran si l'UI est modifiée.
- Référencez une issue si le changement y est lié.

## Gestion des images et des gros fichiers
- Évitez d'ajouter des fichiers image très volumineux (> 500 KB) ; optimisez (compression, redimensionnement).
- Préférez les formats modernes (WebP, optimisé PNG/JPEG) si possible.
- Si vous devez ajouter un fichier volumineux, ouvrez d'abord une issue et attendez l'accord d'un maintainer.
- Ne stockez pas d'archives ZIP volumineuses dans le dépôt sans discussion.

## Tests locaux simples
- Ouvrez les fichiers HTML modifiés dans un navigateur après vos changements pour vérifier visuellement.
- Vérifiez les consoles de navigateur pour les erreurs JavaScript (si présentes) et les comportements CSS inattendus.

## Questions et support
- Ouvrez une issue en expliquant le problème et la proposition de solution si vous avez un doute.
- Mentionnez @maintainer (ou le nom du responsable) pour attirer l'attention.

Merci de contribuer à EcoArt !