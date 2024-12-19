# TP Individuel MERN Paris - Application "Le Bon Coin"

## Contexte

Ce projet consiste à créer une application web MERN (MongoDB, Express, React, Node.js) inspirée de "Le Bon Coin", une plateforme de petites annonces. L'objectif est de mettre en pratique vos connaissances sur la stack MERN en créant un système complet avec gestion des utilisateurs et des annonces.

## Objectifs

- Implémenter un système d'authentification sécurisé avec JWT et bcrypt.
- Permettre la gestion (CRUD) des utilisateurs et des annonces.
- Lors de la création d'une annonce, le backend doit automatiquement récupérer l'ID de l'auteur via le token JWT.
- Utiliser des states locaux pour gérer l'état de l'application côté frontend.

## Spécifications Techniques

### 1. Système d'authentification

Implémenter un système d’inscription et de connexion sécurisé :

- **Inscription** : Hachage des mots de passe avec bcrypt.
- **Connexion** : Génération d’un token JWT pour sécuriser l’accès aux pages protégées.
- Les pages protégées (CRUD utilisateurs et annonces) doivent nécessiter un token valide.

### 2. Pages obligatoires

#### Page d'inscription (Register)

- Permet à un utilisateur de créer un compte en renseignant :
  - Nom d’utilisateur (unique).
  - Email.
  - Mot de passe.
- Vérification des champs côté serveur et client.

#### Page de connexion (Login)

- Permet à un utilisateur de se connecter avec son email et son mot de passe.
- Si les informations sont correctes, un token JWT est généré et stocké côté client.

#### CRUD sur les annonces

- Une page où les utilisateurs peuvent :
  - Voir toutes les annonces.
  - Ajouter, modifier ou supprimer des annonces.
- Lors de la création d’une annonce, le backend doit automatiquement associer l’annonce à l’utilisateur connecté en récupérant son ID via le token JWT.

### 3. Fonctionnalités supplémentaires

#### Filtrage par catégorie (Bonus)

- Ajoutez un champ "catégorie" dans les annonces (exemple : Immobilier, Véhicules, Électronique, etc.).
- Permettez à l’utilisateur de filtrer les annonces par catégorie via un menu déroulant ou des boutons.

#### Détails d’une annonce (Bonus)

- Lorsque l’utilisateur clique sur "Voir l'annonce" dans la liste, affichez une page dédiée :
  - Titre, description, catégorie, prix.
  - Nom de l’utilisateur ayant posté l’annonce.

## Contraintes

- Lors de la création d'une annonce, l'ID de l'utilisateur connecté doit être automatiquement ajouté dans le champ `author` côté backend.
- Le CRUD (création, modification, suppression) sur les annonces n’est pas restreint aux auteurs des annonces.

## Stack Technique

### 1. Backend (Node.js/Express)

- Créez des routes sécurisées pour les fonctionnalités d'authentification et les CRUD.
- Utilisez **MongoDB** pour la base de données.
- Implémentez la récupération de l’ID de l’auteur via le token JWT dans le middleware backend.

### 2. Frontend (React)

- Gérez l’état de l’application uniquement avec des **states locaux**.
- Proposez une interface utilisateur simple et fonctionnelle.
- Gérez les tokens JWT avec **localStorage** ou **Cookies** pour les pages protégées.

## Plan de développement

### Initialisation

1. Créez les dossiers backend et frontend.
2. Installez les dépendances principales :
   - **Backend** : express, mongoose, bcrypt, jsonwebtoken, dotenv, etc.
   - **Frontend** : react, react-router-dom, etc.

### Backend

1. Configurez le serveur Express avec MongoDB.
2. Implémentez les routes pour :
   - Inscription / Connexion.
   - CRUD utilisateurs et annonces.
   - Middleware d’authentification.

### Frontend

1. Implémentez les pages principales (Register, Login, Annonces).
2. Ajoutez les formulaires avec validation des champs.
3. Gérez l’authentification avec JWT.

### Tests et Debugging

1. Testez toutes les routes backend avec Postman.
2. Validez le bon fonctionnement des pages frontend.

### Fonctionnalités Bonus

1. Ajoutez le filtrage par catégorie.
2. Implémentez les pages de détails des annonces.

## Livrables

1. **Code source complet** : Déposez-le sur GitHub.
2. **Documentation du projet (README.md)** :
   - Description du projet.
   - Instructions pour exécuter le projet.
   - Liste des fonctionnalités implémentées.
   - Screenshots des pages principales.

## Instructions pour exécuter le projet

### Prérequis

- Node.js
- MongoDB

### Backend

1. Clonez le repository :
   ```bash
   git clone <URL_DU_REPOSITORY>
   cd backend
