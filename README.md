# Finance – suivi d'achats et de budget

Application web installable (PWA) : onglet **Achat**, onglet **Budget**, formulaire d'ajout.
Fonctionne hors ligne ; avec Firebase, les données se synchronisent dès que la connexion revient.

## Fichiers
`index.html`, `manifest.json`, `sw.js`, `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `firebase-config.js`, `firestore.rules`

## Fonctions
- Achat : liste de tous les achats, bouton +, sélection multiple (icône ✓) pour supprimer
- Budget : budget / reste / total par catégorie pour le mois choisi, crayon bleu pour modifier catégories et budgets
- Menu ☰ : compte de synchronisation (connexion / déconnexion)
- Point de couleur à côté du titre : vert = synchronisé, orange = en attente / hors ligne, gris = pas de synchro

## Mise en place de la synchronisation (Firebase, gratuit)
1. https://console.firebase.google.com → **Ajouter un projet** (désactiver Google Analytics).
2. **Authentication → Commencer → Adresse e-mail/Mot de passe → Activer**.
3. **Firestore Database → Créer une base de données** (mode production, région europe-west).
4. Onglet **Règles** : coller le contenu de `firestore.rules` puis **Publier**.
5. ⚙ **Paramètres du projet → Vos applications → </> (Web)** → enregistrer l'app → copier l'objet `firebaseConfig`.
6. Coller ces valeurs dans `firebase-config.js` (sur GitHub : ouvrir le fichier → crayon → Commit).
7. **Authentication → Paramètres → Domaines autorisés** → ajouter `VOTRE-NOM.github.io`.
8. Ouvrir l'app → ☰ → **Créer le compte** (email + mot de passe), puis **Se connecter** sur le téléphone.

Les règles Firestore garantissent que chaque compte ne voit que ses propres données.

## Installer sur téléphone
Ouvrir l'adresse GitHub Pages dans le navigateur puis :
- **Android (Chrome)** : menu ⋮ → *Installer l'application* / *Ajouter à l'écran d'accueil*
- **iPhone (Safari)** : bouton Partager → *Sur l'écran d'accueil*
