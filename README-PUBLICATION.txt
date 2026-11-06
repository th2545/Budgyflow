BUDGYFLOW — MISE EN LIGNE
========================

Contenu du dossier
------------------
- index.html                  Application web (point d’entrée à publier)
- budgy.v10.html              Copie de travail/source conservée
- manifest.webmanifest        Métadonnées de l’application installable
- sw.js                       Cache de l’interface et ouverture hors ligne après une première visite
- app-icon.svg                Icône vectorielle
- app-icon-180.png            Icône pour l’écran d’accueil iOS
- app-icon-192.png            Icône PWA
- app-icon-512.png            Icône PWA haute résolution
- app-icon-maskable-512.png   Icône adaptée aux masques Android
- privacy.html                Politique de confidentialité à vérifier
- legal.html                  Mentions légales à compléter impérativement
- robots.txt                  Autorise l’indexation publique

L’application comprend maintenant un onglet « Bons plans » : conseils généraux, recherches
de lieux par ville/quartier sur Google Maps et liens vers des plateformes de réductions
étudiantes. Les explications de chaque rubrique et de « À savoir » sont accessibles via
l’astérisque placé à droite du titre. Les offres et prix ne sont pas récupérés en temps réel ;
l’écran le précise.

L’interface utilise une identité visuelle futuriste bleu nuit, cyan et violet, avec les
polices Space Grotesk et DM Sans. La police web est chargée depuis Google Fonts ; une police
système prend le relais si le service n’est pas accessible. Le thème Nuit néon est activé
par défaut ; le thème choisi dans les réglages est enregistré localement pour les prochaines
visites.

Avant la mise en ligne
----------------------
1. Compléter tous les champs [ENTRE CROCHETS] de legal.html avec les informations
   publiques exactes : éditeur, adresse à publier, contact, directeur de publication,
   hébergeur et URL publique.
2. Relire privacy.html après avoir choisi l’hébergeur. Elle décrit le comportement
   actuel du code : budget conservé localement, pas de compte ni d’envoi automatique
   du budget, polices DM Sans et Space Grotesk chargées en ligne, et partage/export seulement
   sur demande.
3. Vérifier les obligations légales applicables au pays et au statut de l’éditeur.
4. Publier l’intégralité de ce dossier à la racine d’un hébergement de site statique.
   Ne pas publier uniquement index.html : les icônes, le manifeste et sw.js sont requis.

Publication choisie : GitHub Pages
----------------------------------
1. Créer un dépôt GitHub pour Budgyflow. Avec GitHub Free, un dépôt public est nécessaire
   pour publier un site Pages.
2. Ajouter à la racine de la branche publiée tous les fichiers de ce dossier, notamment
   index.html, sw.js, manifest.webmanifest, les icônes et les deux pages légales.
3. Dans le dépôt, ouvrir Settings > Pages.
4. Dans Build and deployment, choisir Deploy from a branch, puis sélectionner la branche
   et le dossier / (root), et enregistrer.
5. Attendre la fin du déploiement indiqué dans l’onglet Actions, puis ouvrir l’URL affichée
   dans Settings > Pages. Pour un dépôt de projet, elle ressemble généralement à
   https://<compte>.github.io/<nom-du-depot>/ ; pour un dépôt de site utilisateur,
   https://<compte>.github.io/.
6. Reporter l’URL définitive dans legal.html, vérifier toutes les pages et ressources, puis
   publier à nouveau le dossier complet.

Les sites GitHub Pages sont accessibles publiquement sur Internet. Vérifier le contenu de
tous les fichiers avant de pousser le dépôt. La source budgy.v10.html est conservée à côté
de index.html ; elle ne contient pas les données personnelles des utilisateurs.

Exigences de publication
------------------------
- Utiliser l’URL HTTPS fournie par l’hébergeur (les Service Workers exigent HTTPS,
  sauf sur localhost). Ne pas tester le mode hors ligne en ouvrant index.html directement.
- Après déploiement, ouvrir le site en ligne, vérifier les pages privacy.html et legal.html
  dans le même chemin que index.html,
  puis installer l’application depuis le navigateur.
- Vérifier le chargement du manifeste et de toutes les icônes dans les outils développeur.
- Tester une première visite en ligne, puis l’ouverture hors ligne après installation.
- Tester aussi sur un vrai iPhone/Safari et un téléphone Android si ces plateformes sont visées.
- Ne pas annoncer une synchronisation : les données du budget restent dans le stockage local
  du navigateur et ne suivent pas l’utilisateur sur un autre appareil.

Mise à jour
-----------
Téléverser de nouveau l’intégralité du dossier après toute modification. Pour publier une
nouvelle version du cache hors ligne, incrémenter CACHE_NAME dans sw.js (par exemple v9 vers
v10). Toujours tester l’application et ses pages légales après chaque déploiement.

Ce dossier prépare une application web installable. Il ne contient pas les inscriptions
nécessaires pour publier une application native dans l’App Store ou Google Play.
