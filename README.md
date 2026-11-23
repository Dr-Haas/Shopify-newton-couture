# Newton Couture · Boutique Shopify

Maquette validée de la boutique en ligne Newton Couture (leggings et veste couture), prête à être reprise dans un thème Shopify.

Composition retenue avec la cliente :

| Page | Thème | Ambiance |
|---|---|---|
| Accueil | A · Nuit étoilée | Mise en page éditoriale sur un ciel étoilé fixe, figurines qui flottent |
| Produit | B · Atelier | Fond crème, figurine qui lévite devant son décor de studio figé |
| Panier | B · Atelier | Panier fonctionnel : quantités, suppression, total recalculé, code promo, paiement express |

Police : Poppins (Google Fonts) sur l'ensemble du site. Accroche d'accueil : « Défiez la gravité avec style. », sur une seule ligne en ordinateur.

## Voir la maquette

Ouvrir `maquette/index.html` dans un navigateur. La barre du haut permet de passer d'une page à l'autre (Accueil, Produit, Panier) et entre vue ordinateur et vue mobile. Cette barre sert uniquement à la présentation et ne fait pas partie de la boutique.

## Contenu du dépôt

```
maquette/
  index.html          Maquette complète (HTML, CSS et JavaScript dans un seul fichier)
  img/
    logo.webp         Logo Newton Couture détouré (fond transparent)
    fig_*.webp        Figurines détourées (fond transparent)
    plate_*.webp      Décors de studio sans la figurine (fond figé)
shopify/
  produits_import.csv Les 5 produits au format d'import Shopify, tailles XS à XL, en brouillon
```

### Effet de mouvement sur les visuels

Chaque visuel est composé de deux images superposées : le décor seul (`plate_*`) en dessous, qui reste fixe, et la figurine détourée (`fig_*`) au-dessus, qui flotte, suit la souris et monte au défilement. Sur l'accueil, la figurine est posée directement sur le ciel étoilé, sans décor. Le même procédé pourra être appliqué aux photos du futur shooting.

Les visuels actuels (poupées) sont **provisoires**, en attendant la production et le shooting.

## Catalogue

| N° | Produit | Matière | Prix |
|---|---|---|---|
| 01 | Milano | Coton extensible | 120 € |
| 02 | Vénus | Néoprène anti-transpirant | 150 € |
| 03 | Longchamp | Faux daim | 150 € |
| 04 | Honey Moon | Jersey brillant ivoire | 500 € |
| 05 | Duchesse (veste) | Réversible faux daim et néoprène | 250 € |

Descriptions et points clés : ceux fournis par la cliente, repris dans la maquette et dans `shopify/produits_import.csv`.

## Passage sur Shopify

Base recommandée : la famille de thèmes **Horizon** (thème officiel et gratuit de Shopify, découpé en blocs, avec page produit et panier natifs). Correspondance des sections :

| Maquette | Section Shopify |
|---|---|
| Bandeau d'annonce, en-tête | Announcement bar, Header |
| Hero (accroche, figurine, pastilles) | Section personnalisée (image en deux calques + animation) |
| Bandeau défilant | Marquee / Scrolling text |
| La collection | Featured collection |
| L'élégance est une formule | Section personnalisée (liste des modèles) |
| La ceinture, Une pièce pour chaque moment | Image with text, Multicolumn |
| Citation | Rich text |
| Newsletter, pied de page | Email signup, Footer |
| Page produit | Product information (galerie, variantes Taille, quantité, accordéons) |
| Avis clientes | Application d'avis (Judge.me, Shopify Product Reviews ou équivalent) |
| Panier | Cart page (ou cart drawer) |

Les animations (lévitation, ciel étoilé, transitions de page, ajout au panier) sont à reprendre en sections Liquid et scripts personnalisés. Le code de référence est dans `maquette/index.html`.

Import des produits : Shopify Admin > Produits > Importer > `shopify/produits_import.csv`. Les produits arrivent en brouillon, sans images.

## À compléter avant la mise en ligne

- Confirmer les prix de Honey Moon et de Duchesse.
- Confirmer le guide des tailles (XS à XL est une hypothèse).
- Composition exacte et conseils d'entretien de chaque pièce.
- Délais, frais de livraison et politique de retours.
- Mentions légales et CGV.
- Logo en haute définition (SVG ou PNG détouré) : la version actuelle est reconstituée à partir d'un JPEG sur fond noir.
- Paiement : sur Shopify, l'encaissement passe par Shopify Payments (ou PayPal et prestataires agréés). Un compte Stripe ne se branche pas directement au paiement Shopify.
- Liens réseaux sociaux (Instagram, TikTok).
- Photos du shooting pour remplacer les visuels provisoires.
