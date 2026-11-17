# AMS Suivi de stock : mise en ligne

L'outil tient dans un seul fichier, `index.html` (accompagné de `logo-ams.png`).
Tant qu'aucune base n'est branchée, il fonctionne en **mode démo** : les données restent dans le navigateur.

## Ce qu'il faut (environ 20 minutes, une seule fois)

1. **Créer un projet Firebase** sur console.firebase.google.com, nommé par exemple `ams-stock`.
2. **Activer la connexion** : Authentication > Méthode de connexion > E-mail/Mot de passe.
3. **Créer la base** : Firestore Database > Créer, région `europe-west9 (Paris)`.
4. **Coller les règles de sécurité** : Firestore > Règles, coller le contenu de `firestore.rules`, puis Publier.
5. **Récupérer la configuration** : Paramètres du projet > Vos applications > Web (`</>`). Copier l'objet `firebaseConfig`.
6. Dans `index.html`, remplacer `const FIREBASE_CONFIG = null;` par cet objet.
7. **Mettre en ligne** sur GitHub Pages (même méthode que le simulateur de devis), puis ajouter l'adresse du site dans Firebase > Authentication > Paramètres > Domaines autorisés.

## Adresse du site

https://mcaudyser.github.io/ams-suivi-stock/ (projet Firebase `ams-stock`, dépôt GitHub `mcaudyser/ams-suivi-stock`).

## Premier compte responsable logistique

1. Ouvrir le site : l'écran « Première mise en route » s'affiche.
2. Choisir un identifiant (ex. `mathis`) et un mot de passe. Ce compte devient administrateur.

## Ajouter un responsable d'agence

1. Onglet **Utilisateurs** > « Créer un accès » : identifiant (ex. `chartres`), mot de passe, agence.
2. Communiquer l'identifiant et le mot de passe à la personne.
3. Mot de passe oublié : bouton « Nouveau mot de passe ». Départ : bouton « Désactiver ».

## Remplir le catalogue

- Onglet **Catalogue** > « Créer les familles de départ ».
- Pour importer en masse : copier les lignes depuis Excel (Code · Famille · Marque · Modèle · Version · Désignation · Fournisseur) et les coller dans la zone d'import.
- Les articles Edström : Code = code Edström, Famille = Meubles Edström, colonnes véhicule vides.
