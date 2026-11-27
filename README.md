# Perle Bubble Tea

Site vitrine et commande en ligne pour un bar à bubble tea.

- Héro animé (gobelets détourés, perles en 3D, changement de couleur par boisson)
- Carte des boissons avec tailles M / L et prix en FCFA
- Panier : livraison, sur place ou à emporter
- Commande envoyée sur WhatsApp avec position GPS et lien d'itinéraire
- Paiement : espèces, T-Money, Flooz
- Badge Ouvert / Fermé selon les horaires
- Version française et anglaise

## Mettre en ligne

Le site est statique : `index.html` et le dossier `img/`.

- **GitHub Pages** : Settings → Pages → Branch `main` / dossier racine.
- **Netlify** : glisser le dossier sur https://app.netlify.com/drop.

La position GPS ne fonctionne qu'en https.

## Modifier

Dans `index.html` :
- numéro WhatsApp : `WHATSAPP_NUMBER`
- boissons et prix : tableau `DRINKS`
- horaires : `SCHEDULE` (et le texte `hours` dans `STR`)

## Sécurité

- Site statique : pas de serveur, pas de base de données, aucun paiement en ligne.
- Les bibliothèques (GSAP, three.js, Leaflet) sont hébergées dans `vendor/`, sans dépendre d'un CDN externe.
- `_headers` : en-têtes de sécurité appliqués par Netlify (CSP, anti-iframe, HSTS, position autorisée seulement pour ce site).
- Les textes saisis par les clients sont échappés avant affichage.
- Le prénom, le nom et le téléphone du client sont mémorisés uniquement dans son propre navigateur pour la prochaine commande ; la position n'est jamais enregistrée.
