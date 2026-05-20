# 🍳 Shopify Theme — LD Global (Kitchen Gadgets Store)

Thème Shopify Online Store 2.0 basé sur **Dawn**, conçu pour une boutique e-commerce spécialisée dans les **gadgets de cuisine du quotidien** — produits simples, malins et accessibles, livrés directement chez le client (dropshipping). Refonte complète du thème : header custom, hero banner animé, pages personnalisées (Accueil, Catalogue, Produit, À propos, FAQ, Contact), charte graphique cohérente et full responsive.

🔗 **[Voir la boutique en ligne](https://ldglobalco.myshopify.com/)**

---

## 🛠️ Stack technique

| Technologie | Usage |
|---|---|
| **Shopify Online Store 2.0** | Plateforme e-commerce |
| **Liquid** | Moteur de templating Shopify |
| **HTML5 / CSS3** | Markup sémantique, animations, responsive |
| **JavaScript (Vanilla)** | Cart drawer, carousel, filtres prix, mots rotatifs |
| **Dawn (base theme)** | Thème Shopify officiel utilisé comme base |
| **Figtree** | Police principale (Google Fonts) |

---

## ✨ Fonctionnalités principales

### 📢 Barre d'annonce animée
- 3 messages rotatifs configurables depuis le customizer
- Animation verticale fluide (haut → bas) avec `@keyframes` CSS
- Durée de rotation réglable, sans flèches de navigation

### 🔍 Header personnalisé
- Logo à gauche · barre de recherche inline au centre · compte + panier à droite
- Navigation en 2ème ligne centrée (police **Figtree**)
- Soulignement du lien actif et au hover en vert `#36881f` (3px, offset 1rem)
- Formulaire de recherche custom sans le sélecteur "All" de Dawn
- Fix z-index sticky pour éviter le chevauchement avec le slideshow

### 🎬 Hero Banner (slideshow)
- Slides avec images de fond desktop + mobile indépendantes
- **Mots rotatifs animés** sur le titre (animation fade-in/out CSS)
- Contrôles slideshow (prev/next + dots) masqués sur mobile et tablette
- Bouton autoplay caché (présent dans le DOM pour le JS Dawn) — fix bug d'autoplay
- Personnalisation complète par slide : couleur titre, sous-titre, boutons (fond, texte, contour)
- Mot en évidence via balise `<em>` stylisée en vert

### 🏠 Page d'accueil — sections custom

#### Hero Home (`hero-home.liquid`)
- Titre animé avec `clamp()` pour fluidité typographique
- Grille de catégories (3 colonnes mobile, flex desktop) avec cercles image
- CTA vert `#74B734` configurable depuis le customizer
- Full responsive : tablette (cercles 88%) + mobile (padding, titre réduit)

#### Vitrine Collections (`collection-showcase.liquid`)
- Mosaïque asymétrique 5 blocs (grille CSS 12 colonnes)
- Effet zoom image au hover (`scale(1.05)`)
- **Taille de titre et sous-titre réglables par bloc** depuis le customizer
- Responsive : 2 colonnes tablette → 2 colonnes empilées mobile

#### Mur Social (`social-wall.liquid`)
- Grille mosaic 6 blocs avec `grid-template-areas`
- Titre section blanc `clamp(2rem, 4vw, 6rem)` / sous-titre blanc 2rem
- Overlay au hover, zoom image
- Responsive : 2 colonnes tablette, 2 colonnes mobile

#### Section Bestsellers (`bestsellers.liquid`)
- 6 produits sélectionnés manuellement
- Bouton "+ Ajouter au panier" → ouvre le cart drawer automatiquement
- Grille responsive : 6 → 3 → 2 colonnes

#### Avis & Confiance (`reviews-trust.liquid`)
- Carousel scroll horizontal avec dots de navigation
- **Dots intelligents** : nombre calculé selon les cartes visibles (desktop 3/vue → 2 dots)
- Flèches prev/next masquées sur mobile
- Stats configurables (chiffre + couleur + libellé)

#### Split Image CTA (`split-image-cta.liquid`)
- Section 2 colonnes image/texte avec CTA

### 🗂️ Page Catalogue (`main-collection-product-grid.liquid`)
- En-tête : fil d'Ariane + titre + sous-titre richtext
- **Layout sidebar filtres** (sticky desktop) + grille produits
- **5 filtres en accordéon** :
  - Disponibilité · Prix (curseur 0–200€) · Catégorie · Promotions · Nouveautés
- **Toolbar** : bouton "Filtres" à gauche (tablette/mobile) + sélecteur tri à droite
- Bouton filtres avec chevron animé et état actif en vert
- Grille 3 colonnes desktop → 3 tablette → 2 mobile
- Pagination numérotée

### 📦 Page Produit (`main-product.liquid`)
- Galerie image principale + miniatures
- Sélecteur de variante, quantité, bouton ajout panier → cart drawer
- Section suggestions produits similaires avec add to cart
- Full responsive tablette et mobile

### 🛒 Cart Drawer custom (`cart-drawer.liquid`)
- Stepper quantité custom (▲/▼)
- Section upsell "Vous aimerez aussi"
- Checkbox conditions générales
- **Fix bug panier vide** : suppression de la classe `is-empty` sur `<cart-drawer>` avant `renderContents()` pour éviter l'affichage de l'état vide lors du premier ajout
- Auto-ouverture du drawer sur tous les boutons "Ajouter au panier" (sections customs) via intercepteur global dans `theme.liquid`

### 📖 Page À propos (`page-about.liquid`)
- Hero banner pleine largeur avec overlay
- 3 sections split image/texte (avec effet de chevauchement de carte)
- Stats sombres (fond configurable, 2 colonnes)
- Grille avis clients 2 colonnes
- Full responsive tablette et mobile

### ❓ Page FAQ (`page-faq.liquid`)
- Hero bannière configurable
- Layout 2 colonnes : sidebar sticky + panel accordéon
- **Recherche en temps réel** par question (filtrage JS)
- Catégories avec icônes PNG uploadables depuis le customizer
- Icône sidebar et icône aide en `image_picker` (dimensions recommandées affichées)
- Sidebar non-sticky sur tablette/mobile (défile normalement)
- Bannière CTA en bas (couleur, texte, lien configurables)

### 📩 Page Contact (`contact-form.liquid`)
- Formulaire avec champs Nom, Email, Sujet (select), Message
- Colonne droite : support client, email direct, engagements (3 icônes PNG uploadables)
- Textes des engagements éditables dans le customizer
- Bannière CTA identique à la FAQ
- Textes de la colonne info augmentés pour meilleure lisibilité

---

## 🎨 Charte graphique

| Élément | Valeur |
|---|---|
| **Vert principal** | `#74B734` |
| **Vert foncé / hover** | `#36881f` / `#5a9228` |
| **Quasi-noir titres** | `#2a2a2a` |
| **Texte corps** | `#444` / `#555` |
| **Fond clair** | `#faf7f4` / `#fdfdfd` |
| **Fond sombre** | `#2a2a2a` |
| **Page width** | `1400px` |
| **Police** | Figtree (Google Fonts) |

---

## 🚀 Installation

### Prérequis
- Compte Shopify (boutique de test ou plan Partner)
- [Shopify CLI ≥ 3.x](https://shopify.dev/docs/themes/tools/cli)
- Node.js ≥ 18

### Méthode 1 — Upload ZIP via l'admin Shopify
1. Télécharge le repo : `Code` → `Download ZIP`
2. Dans l'admin : **Boutique en ligne → Thèmes → Ajouter un thème → Téléverser un fichier ZIP**
3. Active le thème

### Méthode 2 — Via Shopify CLI (recommandée)
```bash
git clone https://github.com/YamiUtsukushi/shopify-kitchen-gadgets-theme.git
cd shopify-kitchen-gadgets-theme

# Serveur de développement avec hot reload
shopify theme dev --store=ldglobalco.myshopify.com

# Pousser vers la boutique
shopify theme push
```

---

## 📁 Structure du projet

```
.
├── assets/                             # CSS, JS, icônes SVG
│   ├── base.css                        # Styles globaux Dawn
│   ├── cart-drawer.js                  # Logique cart drawer Dawn
│   └── component-slideshow.css         # Styles slideshow
├── config/
│   ├── settings_data.json              # Charte couleur + page_width 1400px
│   └── settings_schema.json
├── layout/
│   └── theme.liquid                    # Layout principal + intercepteur cart global
├── sections/
│   ├── announcement-bar.liquid         # Barre d'annonce animée
│   ├── header.liquid                   # Header custom (search, Figtree, soulignement vert)
│   ├── hero-banner.liquid              # Slideshow hero (mots rotatifs, autoplay fix)
│   ├── hero-home.liquid                # Hero page d'accueil (catégories, CTA vert)
│   ├── bestsellers.liquid              # Bestsellers (6 produits, cart drawer)
│   ├── collection-showcase.liquid      # Vitrine mosaïque 5 blocs (zoom hover, tailles custom)
│   ├── social-wall.liquid              # Mur social grille mosaic 6 blocs
│   ├── reviews-trust.liquid            # Avis carousel (dots intelligents, stats)
│   ├── split-image-cta.liquid          # Section split image/texte CTA
│   ├── main-collection-banner.liquid   # En-tête page catalogue
│   ├── main-collection-product-grid.liquid  # Catalogue (filtres, tri, 3 col, toolbar)
│   ├── main-product.liquid             # Page produit (galerie, variantes, suggestions)
│   ├── cart-drawer.liquid              # (Section) Appel du snippet cart-drawer
│   ├── page-about.liquid               # Page À propos (hero, splits, stats, avis)
│   ├── page-faq.liquid                 # Page FAQ (accordéon, recherche, icônes PNG)
│   └── contact-form.liquid             # Page Contact (formulaire, infos, CTA)
├── snippets/
│   ├── cart-drawer.liquid              # Cart drawer custom (stepper, upsell, CGV)
│   └── ...
├── templates/
│   ├── index.json
│   ├── page.about.json
│   ├── page.faq.json
│   ├── page.contact.json
│   └── ...
└── locales/
```

---


## 🗺️ Roadmap

- [x] Header custom avec recherche inline
- [x] Hero banner avec mots rotatifs et slideshow
- [x] Page catalogue avec filtres et tri
- [x] Cart drawer auto-open sur tous les boutons
- [x] Responsive complet tablette + mobile
- [x] Pages personnalisées : À propos, FAQ, Contact
- [x] Nouvelles sections : Vitrine, Mur Social, Avis, Split CTA
- [ ] Optimisation Lighthouse / Core Web Vitals
- [ ] Mode sombre
- [ ] Timer animé sur le hero banner
- [ ] Section "Comment ça marche"

---

## 🧰 Compatibilité

- Shopify Online Store 2.0 (sections everywhere)
- Chrome, Firefox, Safari, Edge (versions récentes)
- iOS Safari 14+ · Chrome Android

---

## 📝 Licence

Ce projet est sous licence **MIT**.
> Le thème Dawn (base) est sous licence MIT par Shopify Inc.

---

## 👤 Auteur

Projet réalisé par **Jayson MOOKEN**
🔗 [LinkedIn](https://www.linkedin.com/in/jayson-mooken/)

---

⭐ Si ce projet t'a été utile, n'hésite pas à laisser une étoile sur le repo !
