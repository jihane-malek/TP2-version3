Compte rendu - TP2


1. src/main/java/com.example.tp2version3
Ce répertoire contient le code source principal de l'application, organisé en plusieurs sous-packages pour respecter les bonnes pratiques de structuration des projets Spring Boot.

entities :

Contient les classes qui représentent les entités de l'application.
Exemple : Product représente un produit avec ses attributs (id, nom, prix, etc.).
Ces classes sont mappées à des tables dans la base de données grâce aux annotations JPA (@Entity).

repository :

Contient les interfaces pour interagir avec la base de données.
Exemple : ProductRepository utilise Spring Data JPA pour fournir des méthodes prêtes à l’emploi (comme findAll(), findById(), etc.), réduisant le code nécessaire pour les opérations CRUD.

web :

Contient les contrôleurs REST qui gèrent les requêtes HTTP et fournissent les endpoints pour interagir avec l'application.
Exemple : ProductRestService expose des endpoints comme /products (pour récupérer tous les produits) et /products/{id} (pour récupérer un produit spécifique).

2. src/main/resources
Ce répertoire contient les ressources nécessaires au bon fonctionnement de l'application.

static :

Répertoire prévu pour les fichiers statiques (CSS, JS, images) dans les applications web. Non utilisé ici, car l'application est une API REST.
templates :

Prévu pour les fichiers de template (comme Thymeleaf ou Freemarker). Non utilisé ici car l'application n'a pas d'interface utilisateur.
application.properties :

Fichier de configuration de l'application.
Contient des propriétés comme les informations de connexion à la base de données, le port du serveur, ou d'autres paramètres spécifiques à Spring.

3. src/test/java/com.example.tp2version3
   
Ce dossier contient les tests unitaires et d'intégration pour vérifier le bon fonctionnement des différentes parties de l'application.

Exemple : Tp2Version3ApplicationTests teste le démarrage de l'application et d'autres comportements critiques.
L'utilité de Java dans ce projet
Java est le langage principal utilisé dans ce projet pour les raisons suivantes :

Puissance et performance : Java est optimisé pour développer des applications robustes et performantes.
Écosystème riche : Il offre un large éventail de bibliothèques et de frameworks, comme Spring Boot, pour simplifier le développement.
Portabilité : Grâce à la JVM (Java Virtual Machine), les applications Java peuvent fonctionner sur différentes plateformes.
L'utilité de Spring Boot dans ce projet
Spring Boot est un framework basé sur Spring qui simplifie le développement des applications Java en fournissant :

Configuration automatique : Pas besoin de configurer manuellement des fichiers XML complexes.

Gestion des dépendances : Grâce à Maven, Spring Boot gère toutes les bibliothèques nécessaires.

Création d'API REST rapide :

Annotations comme @RestController et @GetMapping simplifient l'exposition des endpoints.
Exemple : @GetMapping("/products") permet de définir facilement un endpoint pour récupérer tous les produits.

Gestion de la base de données :

Spring Data JPA offre une intégration facile avec les bases de données relationnelles.
Exemple : Méthodes prêtes à l’emploi comme findAll() pour obtenir tous les enregistrements.
