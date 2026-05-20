# 🍳 Shopify Theme — Kitchen Gadgets Store

Thème Shopify Online Store 2.0 basé sur Dawn, conçu pour une boutique e-commerce spécialisée dans les **gadgets de cuisine du quotidien** — des produits simples, malins et accessibles, livrés directement chez le client (dropshipping). Refonte complète du header, hero banner animé avec mots rotatifs, section Bestsellers, page catalogue avec filtres en accordéon, et charte graphique cohérente sur l'ensemble du thème.

---

## 🌐 Application déployée

🔗 **[Voir la boutique en ligne](https://your-store.myshopify.com/)** *(à compléter)*

---

## 🛠️ Stack technique

| Technologie | Usage |
|---|---|
| **Shopify Online Store 2.0** | Plateforme e-commerce |
| **Liquid** | Moteur de templating Shopify |
| **HTML5 / CSS3** | Markup sémantique, animations, responsive |
| **JavaScript (Vanilla)** | Mots rotatifs, slideshow, timer |
| **Dawn (base theme)** | Thème Shopify officiel utilisé comme base |

---

## ✨ Fonctionnalités principales

### 📢 Barre d'annonce animée
- 3 messages rotatifs configurables depuis le customizer
- Animation verticale fluide (haut → bas) avec `@keyframes` CSS
- Durée de rotation réglable, sans flèches de navigation

### 🔍 Header personnalisé
- Logo à gauche · barre de recherche inline au centre · compte + panier à droite
- Navigation en 2ème ligne centrée (police **Figtree** depuis Google Fonts)
- Taille et graisse de la police configurables dans le customizer
- Formulaire de recherche custom sans le sélecteur "All" de Dawn

### 🎬 Hero Banner (slideshow)
- 3 slides avec images de fond, 2 boutons par slide
- **Mots rotatifs animés** sur le slide 1 : `simplifient / révolutionnent / transforment / modernisent`
- Contrôles Dawn natifs (points, flèches prev/next) en overlay sur l'image
- Personnalisation complète par slide depuis le customizer : couleur du titre, sous-titre, boutons (fond, texte, contour)
- Mot vert mis en valeur via balise `<em>` stylisée

### 🛒 Section Bestsellers
- Sélection manuelle de **6 produits** via le customizer (blocs individuels)
- Cartes produits sur fond blanc avec padding image, zoom au hover
- Affichage intelligent du prix : **prix barré + prix promo** si remise active
- Bouton **"+ Ajouter au panier"** avec ajout direct (POST `/cart/add`)
- Grille responsive : 6 colonnes → 3 → 2 selon la taille d'écran

### 🗂️ Page Catalogue
- **En-tête** : fil d'Ariane `Home / Catalogue`, titre configurable, sous-titre richtext 3 lignes
- **Layout 2 colonnes** : sidebar filtres sticky à gauche + grille produits à droite
- **5 filtres en accordéon** (chevron animé, texte majuscule + espacement lettres) :
  - Disponibilité (En stock / Rupture de stock) via params natifs Shopify OS 2.0
  - Prix — curseur double avec bouton "Appliquer" (`filter.v.price.gte/lte`)
  - Catégorie — 6 tags (Éplucheurs, Spiraliseurs, Minuteurs, Découpe, Mesure, Rangement)
  - Promotions — filtre tag `sale`
  - Nouveautés — tri `created-descending`
- **Barre de résultats** : nombre de produits + sélecteur de tri natif Shopify
- **Grille 3 colonnes** avec les mêmes cartes que Bestsellers (prix barré, add to cart)
- **Pagination** numérotée, responsive mobile (2 colonnes)

### 🎨 Charte graphique cohérente
| Élément | Couleur |
|---|---|
| Boutons, accents | `#36881f` (vert) |
| Titres | `#2a2a2a` (quasi-noir) |
| Fond section 1 | `#FFFFFF` |
| Fond section 2 | `#FDFDFD` |
| Fond dark (footer, annonce) | `#2a2a2a` |

---

## 🚀 Installation rapide

### Prérequis
- Compte Shopify (boutique de test ou plan Partner)
- [Shopify CLI ≥ 3.x](https://shopify.dev/docs/themes/tools/cli)
- Node.js ≥ 18

### Méthode 1 — Upload ZIP via l'admin Shopify
1. Télécharge le repo : `Code` → `Download ZIP`
2. Dans ton admin : **Boutique en ligne → Thèmes → Ajouter un thème → Téléverser un fichier ZIP**
3. Active le thème

### Méthode 2 — Via Shopify CLI (recommandée pour dev)
```bash
# Cloner le repo
git clone https://github.com/<ton-username>/shopify-kitchen-gadgets-theme.git
cd shopify-kitchen-gadgets-theme

# Lancer le serveur de développement (hot reload)
shopify theme dev --store=ta-boutique.myshopify.com
```

---

## 📁 Structure du projet

```
.
├── sections/
│   ├── announcement-bar.liquid   # Barre d'annonce animée (3 messages rotatifs)
│   ├── header.liquid             # Header custom (search inline, Figtree, flex layout)
│   ├── hero-banner.liquid        # Slideshow hero avec mots rotatifs et couleurs par slide
│   ├── bestsellers.liquid              # Section bestsellers (6 produits manuels + add to cart)
│   ├── main-collection-banner.liquid   # En-tête page catalogue (fil d'Ariane, titre, sous-titre)
│   ├── main-collection-product-grid.liquid  # Grille catalogue (filtres accordéon + 3 colonnes)
│   └── ...                             # Sections Dawn natives conservées
├── snippets/
│   ├── header-dropdown-menu.liquid
│   ├── header-search.liquid
│   └── ...
├── assets/                       # CSS, JS, images, icônes
├── config/
│   ├── settings_data.json        # Charte couleur configurée (schemes 1–5)
│   └── settings_schema.json
├── templates/                    # Templates de pages
├── locales/                      # Fichiers de traduction
└── README.md
```

---

## 📸 Aperçus

> 💡 *Screenshots à venir*

| Desktop | Mobile |
|---|---|
| *(prochainement)* | *(prochainement)* |

---

## 🗺️ Roadmap

- [x] Page collection avec filtres (catégories, prix, disponibilité, promotions, nouveautés)
- [ ] Section "Comment ça marche" (3 étapes illustrées)
- [ ] Section avis clients avec étoiles
- [ ] Bouton pause avec timer animé sur le hero banner
- [ ] Optimisation Lighthouse / Core Web Vitals
- [ ] Mode sombre

---

## 🧰 Compatibilité

- Shopify Online Store 2.0 (sections everywhere)
- Chrome, Firefox, Safari, Edge (versions récentes)
- iOS Safari 14+ · Chrome Android

---

## 📝 Licence

Ce projet est sous licence **MIT**. Voir le fichier `LICENSE` pour plus de détails.
> Le thème Dawn (base) est sous licence MIT par Shopify Inc.

---

## 👤 Auteur

Projet réalisé par **Jayson MOOKEN**
🔗 [LinkedIn](https://www.linkedin.com/in/jayson-mooken/)

---

⭐ Si ce projet t'a été utile, n'hésite pas à laisser une étoile sur le repo !
