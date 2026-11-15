# Finance – suivi d'achats et de budget

Petite application web (PWA) sans dépendances : onglet **Achat**, onglet **Budget**, formulaire d'ajout.

## Confidentialité
- Les données sont stockées **uniquement dans le navigateur** (localStorage). Rien n'est envoyé sur un serveur.
- Le dépôt GitHub ne contient que le code, jamais vos achats. Gardez-le en **Private**.
- Utilisez le menu ☰ → *Exporter une sauvegarde* régulièrement (les données sont liées à l'appareil/navigateur).

## Utilisation locale
Ouvrez `index.html` dans un navigateur, ou lancez `python3 -m http.server` puis allez sur http://localhost:8000.

## Installer sur téléphone
Il faut servir le site en HTTPS (service worker). Options :
- **GitHub Pages** (dépôt privé = plan GitHub payant ; sinon dépôt public, le code seul est visible, pas vos données) ;
- **Cloudflare Pages / Netlify** connectés à un dépôt privé (gratuit) ;
- puis « Ajouter à l'écran d'accueil ».

## Fonctions
- Ajouter / modifier / supprimer un achat (catégorie, prix, date, note)
- Filtre par mois, recherche, sélection multiple (icône ✓) pour supprimer
- Budget par catégorie : budget, reste, total ; rouge si dépassé
- Crayon bleu : modifier les catégories, icônes, couleurs et budgets mensuels
- Export/Import JSON, export CSV, devise configurable
