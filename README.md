# Muzak API - Postman Collection

Ce dépôt contient une collection Postman pour interagir avec l'API de l'application Muzak. Cette collection regroupe des requêtes permettant de tester différentes fonctionnalités de l'API, telles que l'authentification, la gestion des utilisateurs, des groupes, des genres, des instruments, des adresses et des réservations.

## Table des matières

- [Installation](#installation)
- [Utilisation](#utilisation)
- [Variables](#variables)
- [Collections](#collections)
- [Licence](#licence)

## Installation

1. Clonez ce dépôt ou téléchargez-le directement depuis GitHub.
2. Installez [Postman](https://www.postman.com/downloads/) si ce n'est pas déjà fait.
3. Importez le fichier `Muzak.postman_collection.json` dans Postman :
   - Cliquez sur **Import** dans Postman.
   - Sélectionnez le fichier `Muzak.postman_collection.json`.

## Utilisation

### Variables

Avant d'utiliser la collection, configurez les variables nécessaires dans votre environnement Postman. Voici une liste des variables incluses dans ce fichier d'export :

- `base_url` : URL de base de l'API (par défaut : `http://localhost:3000/api`).
- `token` : Jeton d'accès pour les endpoints nécessitant une authentification.
- `user` et `password` : Informations de connexion pour tester les endpoints.

### Collections

La collection inclut les endpoints suivants :

#### 1. **Auth**
- **Login** : `POST /v1/auth/login` - Authentification de l'utilisateur.
- **Register** : `POST /v1/auth/register` - Inscription d'un nouvel utilisateur.

#### 2. **Users**
- **Me** : `GET /v1/users/me` - Récupérer les informations de l'utilisateur authentifié.
- **User by ID** : `GET /v1/users/:id` - Récupérer les informations d'un utilisateur via son ID.
- **Update User** : `PATCH /v1/users/:id` - Mettre à jour les informations d'un utilisateur.
- **Get All Users** : `GET /v1/users` - Liste tous les utilisateurs.

#### 3. **Groups**
- **All Groups** : `GET /v1/groups` - Liste tous les groupes.
- **Group by ID** : `GET /v1/groups/:id` - Récupérer les informations d'un groupe via son ID.
- **Create Group** : `POST /v1/groups` - Créer un nouveau groupe.

#### 4. **Genres**
- **All Genres** : `GET /v1/genres` - Liste tous les genres.

#### 5. **Instruments**
- **All Instruments** : `GET /v1/instruments` - Liste tous les instruments.

#### 6. **Address**
- **Create Address** : `POST /v1/addresses` - Ajouter une nouvelle adresse.
- **Get Addresses** : `GET /v1/addresses` - Liste toutes les adresses.

#### 7. **Reservation**
- **Create Reservation** : `POST /v1/reservations` - Créer une réservation.
- **Confirm Reservation** : `PATCH /v1/reservations/:id/confirm` - Confirmer une réservation.
- **Cancel Reservation** : `PATCH /v1/reservations/:id/cancel` - Annuler une réservation.

#### 8. **UserGroups**
- **Update User in Group** : `POST /v1/user-groups` - Ajouter un utilisateur à un groupe.

### Scripts intégrés

Certains endpoints incluent des scripts Postman pour gérer les jetons d'authentification automatiquement en cas d'expiration.

## Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus d'informations.
