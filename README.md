# 🏰 Lycée Thibaut de Champagne – Refonte du site

Maquette web statique (HTML / CSS) du site du **lycée Thibaut de Champagne** de Provins, repensée avec une identité visuelle **médiévale** : fond parchemin, cadres dorés, palette bordeaux et typographie à empattements.

> ⚠️ Projet réalisé à titre d'exercice de refonte. Ce n'est pas le site officiel de l'établissement.

---

## 📄 Pages

| Fichier | Contenu |
|---|---|
| `index.html` | Accueil : bandeau d'annonce, présentation, boutons d'accès rapide, derniers articles |
| `lycee.html` | Le lycée : bannière, historique de l'établissement, offre de formation, photo du parc |
| `enseignement.html` | Enseignements : voies générale, technologique, professionnelle, BTS, dispositifs spécifiques, avec sommaire d'ancres |
| `style.css` | Feuille de style unique, commune à toutes les pages |

## 🗂️ Structure du projet

```
.
├── index.html
├── lycee.html
├── enseignement.html
├── style.css
└── assets/
    ├── chateau.svg          # logo du lycée
    ├── rose_provinc.png     # rose de Provins (séparateur)
    ├── parchment.jpg        # texture de fond
    ├── lycee_acceuil.jpg    # photo de la page d'accueil
    ├── imageia.jpg          # bannière de la page « Le lycée »
    ├── parc.jpg             # photo du parc
    ├── book.png             # icône des cartes de formation
    └── Instagram_logo.svg   # logo du pied de page
```

## 🚀 Lancer le projet

Aucune dépendance, aucun outil de build : c'est du HTML/CSS pur.

```bash
git clone <url-du-depot>
cd <nom-du-depot>
```

Puis ouvrez `index.html` dans votre navigateur.
Vous pouvez aussi utiliser un serveur local, par exemple l'extension **Live Server** de VS Code, ou :

```bash
python3 -m http.server 8000
# puis http://localhost:8000
```

> Les polices sont chargées depuis Google Fonts : une connexion internet est nécessaire pour les voir.

## 🎨 Charte graphique

**Couleurs**

| Usage | Code |
|---|---|
| Fond (parchemin) | `#ece2d0` |
| Texte / boutons | `#15181e` |
| Accent bordeaux | `#550a0d` |
| Bordeaux clair (survols) | `#8a2a3b` |
| Fond des cadres | `#fbf6e6` |
| Or (liserés) | `#b08d3c` |
| Or du bandeau d'annonce | `rgb(250, 194, 90)` |

**Typographie**
- Titres des pages « Enseignements » : *Cormorant Garamond* (via Google Fonts)
- Nom du lycée : italique

**Éléments récurrents**
- Séparateur « ligne – rose de Provins – ligne » (`.contain_lignes`)
- Cadres à double bordure bordeaux et or (`.cadre`, `.bloc`)
- En-tête collant (`position: sticky`) avec bouton « Bac STMG 2026 » mis en avant

## 📱 Responsive

La mise en page s'adapte à trois seuils (`@media`) :

- `≤ 1200px` : en-tête sur deux lignes, accueil en colonne
- `≤ 780px` : menu vertical, cartes et articles empilés
- `≤ 600px` : marges réduites sur la page Enseignements

## 🧭 Navigation

Les liens vers **Accueil**, **Le lycée** et **Enseignements** sont fonctionnels.
Les autres entrées du menu (Actualités, Articles, EPS, Contact, Bac STMG 2026) et les liens des articles pointent pour l'instant vers des ancres vides (`#...`) : ces pages restent à créer.

## ✅ Pistes d'amélioration

- [ ] Créer les pages manquantes : Actualités, Articles, EPS, Contact, Bac STMG 2026
- [ ] Harmoniser le menu : « Articles » n'apparaît que sur `index.html`
- [ ] Corriger les `id` en double dans `enseignement.html` (`generale`, `dispositifs`) et supprimer les `<section>` vides qui précèdent le contenu
- [ ] Passer `lang="en"` en `lang="fr"` sur `index.html` et `enseignement.html`
- [ ] Corriger les fautes « Acceuil » (titre, classes CSS)
- [ ] Ajouter un `alt` à l'image `rose_provinc.png` (ou `alt=""` si elle est purement décorative)
- [ ] Nettoyer `style.css` : les classes `.blocs`, `.bloc*`, `.bloc1`, `.tscience` et `.science1 img` ne semblent pas utilisées, et la police est importée pour 7 familles alors qu'une seule est utilisée
- [ ] Remplacer l'image `imageia.jpg` par une vraie photo du lycée
- [ ] Ajouter une favicon et des balises `meta description`

## 🛠️ Technologies

- HTML5
- CSS3 (Flexbox, Grid, media queries)
- Google Fonts

## 📜 Licence

Les textes et le nom de l'établissement appartiennent au lycée Thibaut de Champagne.
