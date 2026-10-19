# EcoArt

**Le design qui donne une seconde vie aux matières.**

EcoArt est un site vitrine consacré à l’upcycling et à l’artisanat local. Il met en valeur des objets créés à partir de matières revalorisées, les artisans qui les façonnent et les ateliers qui transmettent leur savoir-faire.

## Découvrir le site

| Page | Présentation |
| --- | --- |
| [Accueil](index.html) | Découvrir l’approche EcoArt et ses engagements |
| [Catalogue](produits.html) | Explorer des créations artisanales upcyclées |
| [Ateliers & Services](services.html) | En savoir plus sur les ateliers et les expériences proposées |
| [Nos Artisans](artisans.html) | Rencontrer le collectif et ses savoir-faire |
| [Impact & Contact](impact.html) | Découvrir la démarche et contacter EcoArt |

## Aperçu du projet

- Site multipage réalisé en HTML et CSS, sans framework ni étape de compilation.
- Mise en page responsive et navigation adaptée aux petits écrans.
- Styles partagés et styles propres aux différentes pages.
- Visuels et identité graphique dédiés au projet.

## Lancer le site en local

Aucune installation de dépendances n’est nécessaire. Depuis le dossier du projet, lancez un serveur HTTP local :

```bash
python3 -m http.server 8000
```

Ouvrez ensuite [http://localhost:8000](http://localhost:8000) dans votre navigateur. Pour arrêter le serveur, utilisez `Ctrl+C` dans le terminal.

Vous pouvez aussi ouvrir `index.html` directement dans un navigateur, mais le serveur local est préférable pour tester le site dans des conditions proches d’un hébergement web.

## Structure

```text
.
├── index.html
├── produits.html
├── services.html
├── artisans.html
├── impact.html
├── css/
│   ├── variables.css
│   ├── style.css
│   ├── responsive.css
│   ├── navbar.css
│   └── styles propres aux pages
├── assets/
│   └── images/
└── charte-graphic/
```

## Technologies

- HTML5
- CSS3
- Google Fonts (Space Grotesk)

---

*EcoArt — création artisanale, matières réemployées, impact positif.*
