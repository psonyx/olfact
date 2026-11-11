Olfactory V5.4 — dossier complet de l'application PWA

Fichiers à conserver ensemble à la racine du dépôt GitHub :
- index.html : application complète (HTML, CSS et JavaScript intégrés)
- manifest.webmanifest : paramètres d'installation PWA
- sw.js : cache et fonctionnement hors ligne
- icons/icon-192.png : icône PWA 192 px
- icons/icon-512.png : icône PWA 512 px
- icons/apple-touch-icon.png : icône iOS

Correctifs et fonctions inclus :
- Appui long pour déclencher les actions contextuelles définies par clic droit.
- Suppression de la sélection bleue sur les éléments interactifs.
- Champs de saisie adaptés à iOS, grammes en décimales avec virgule ou point.
- Champ actif repositionné au-dessus du clavier quand le viewport visuel change.
- Barre de navigation inférieure fixée à une hauteur constante dans les deux bibliothèques, avec prise en compte de la zone de sécurité iPhone.
- Barre inférieure masquée pendant l’ouverture des fenêtres modales pour ne jamais recouvrir leurs commandes, puis réaffichée à leur fermeture.
- Fenêtres modales adaptées à la hauteur réellement visible de l’écran, y compris lorsque le clavier iOS apparaît ; contenu défilable indépendamment et commandes accessibles.
- Champ actif repositionné dans la fenêtre sans faire défiler toute la page.
- Prévention du zoom par pincement et du double-tap involontaire, sans bloquer la saisie ni le défilement normal.
- Glissement horizontal dans les zones libres des bibliothèques : vers la gauche = formules, vers la droite = matières premières.
- Glissement vers la gauche sur une formule : demande de confirmation avant suppression.
- Glissement vers la gauche sur une matière : demande de confirmation avant suppression, avec avertissement sur les formules qui l'utilisent.
- Appui long sur une formule ouvre son menu contextuel, qui permet notamment d'annuler une fabrication active et de restaurer les stocks lorsque l'historique de fabrication contient les données requises.
- Pourcentage redondant « parfum X % » retiré de l'affichage des lignes.

Installation :
1. Décompresser l'archive.
2. Remplacer les fichiers correspondants à la racine du dépôt GitHub par tout le contenu de ce dossier, en conservant le dossier icons.
3. Publier GitHub Pages.
4. Ouvrir le site en ligne une fois pour charger le nouveau service worker.
5. Fermer puis rouvrir l'application installée sur l'iPhone.

Important : les gestes tactiles, le comportement du clavier et les dimensions des fenêtres doivent encore être confirmés sur un iPhone réel. Les captures et les vérifications de code ne remplacent pas un test sur appareil. Faire une sauvegarde JSON des données avant remplacement. La suppression d'une matière ou d'une formule est définitive dans l'application ; une sauvegarde préalable est recommandée.


VERSION 5.6 — AFFICHAGE DES POURCENTAGES
- En mode pourcentage avec solvant, le TOTAL affiche désormais uniquement la part des matières odorantes dans la formule (la ligne alcool conserve son propre pourcentage).
- En mode pourcentage concentré sans solvant, le TOTAL reste à 100,00 %.
- La cellule de pourcentage de l’alcool reste visuellement vide en mode concentré, mais sa zone entière est tactile/cliquable et permet de passer à l’affichage du prix.
