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
