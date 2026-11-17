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

## Premier compte responsable logistique

1. Dans Authentication > Utilisateurs, créer son compte (e-mail et mot de passe).
2. Se connecter une fois sur l'outil : le compte apparaît « en attente ».
3. Dans Firestore > `users` > ce compte, remplacer `role: "attente"` par `role: "admin"`.
4. Recharger la page. La suite (familles de départ, articles, comptes des agences) se fait depuis l'outil.

## Ajouter un responsable d'agence

1. Créer son compte dans Firebase > Authentication.
2. Il se connecte une fois, puis le responsable logistique choisit son rôle et son agence dans l'onglet **Utilisateurs**.

## Remplir le catalogue

- Onglet **Catalogue** > « Créer les familles de départ ».
- Pour importer en masse : copier les lignes depuis Excel (Code · Famille · Marque · Modèle · Version · Désignation · Fournisseur) et les coller dans la zone d'import.
- Les articles Edström : Code = code Edström, Famille = Meubles Edström, colonnes véhicule vides.
