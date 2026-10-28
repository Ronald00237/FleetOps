# FleetOps — Fleet Management Backend

Backend de gestion de flotte développé avec Java et Spring Boot.

FleetOps permet de gérer les véhicules, les conducteurs et leurs
affectations. Le projet met l'accent sur la séparation des responsabilités,
la maintenabilité et les tests automatisés.

## Fonctionnalités

- Gestion des véhicules et de leur cycle de vie
- Gestion des conducteurs
- Affectation d'un conducteur à un véhicule
- Historique des affectations
- Validation des règles métier
- API REST avec gestion des erreurs
- Persistance PostgreSQL

## Technologies

- Java 25
- Spring Boot 4.1
- PostgreSQL
- Spring Data JPA
- Flyway
- Maven
- Docker
- Testcontainers

## Architecture

Le projet sépare la logique métier, les services applicatifs et
l'infrastructure.

Les services dépendent d'interfaces de repository plutôt que directement
de la persistance PostgreSQL. Des implémentations en mémoire sont également
utilisées pour certains tests.

## API

Exemples d'endpoints disponibles :

POST  /api/v1/vehicles
GET   /api/v1/vehicles
GET   /api/v1/vehicles/{id}
PUT   /api/v1/vehicles/{id}

## Tests

Le projet contient des tests unitaires et des tests d'intégration couvrant
le domaine, les services, l'API REST et la persistance.

Les tests PostgreSQL utilisent Testcontainers.

## Exécution

Depuis le dossier `backend` :

docker compose up -d
.\mvnw.cmd spring-boot:run

Pour lancer les tests :

.\mvnw.cmd test

## Statut

Projet en développement actif.

**FleetOps — projet personnel de développement backend et d'architecture logicielle.**
