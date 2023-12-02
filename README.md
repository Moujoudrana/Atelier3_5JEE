# Atelier3_5JEE
On souhaite créer une application basée sur une architecture micro-service qui permet de gérer les factures contenant des produits et appartenant à un client.

# Ressources :
   - Partie Backend : https://www.youtube.com/watch?v=hVlEoKQG_2E. et   https://www.youtube.com/watch?v=XEzBA3yIII8
# Travail à faire :
1.Créer le micro-service customer-service qui permet de gérer les client

2.Créer le micro-service inventory-service qui permet de gérer les produits

3. Créer la Gateway Spring cloud Gateway

4. Configuration statique du système de routage

5. Créer l'annuaire Eureka Discrovery Service

6. Faire une configuration dynamique des routes de la gateway

7. Créer le service de facturation Billing-Service en utilisant Open Feign

8. Créer un client Web Angular (Clients, Produits, Factures)

# - Qu'est ce qu'un micro service
Un micro-service fait référence à une architecture logicielle où une application est construite en tant qu'ensemble de petits services indépendants et autonomes. Chaque service, appelé micro-service, est conçu pour effectuer une tâche spécifique de manière autonome. Cette approche est souvent en contraste avec une architecture monolithique, où l'ensemble de l'application est construit en tant qu'unité unique.
# - Qu'est ce qu'une gateway 
 Il s'agit d'un composant qui agit comme un point d'entrée unique pour les clients (applications, utilisateurs) et qui gère divers aspects de la communication avec les micro-services en aval.
 Gateway peut être utilisé pour gérer l'accès aux différents services exposés par les micro-services.

Le rôle principal d'un Gateway dans un environnement de micro-services peut inclure les fonctionnalités suivantes :

-Routage : Diriger les requêtes des clients vers les micro-services appropriés.

-Authentification et autorisation : Gérer les mécanismes d'authentification des clients et d'autorisation pour l'accès aux services.

-Mise en cache : Mettre en cache les réponses des micro-services pour améliorer les performances.

-Monitoring et logging : Fournir des fonctionnalités de suivi et de journalisation pour surveiller les appels aux micro-services.

# - Qu'est ce que c'est Eureka
Spring Cloud Eureka est un composant de la suite Spring Cloud et est utilisé pour la découverte de services dans un environnement de micro-services.

Voici comment Eureka peut être utilisé dans le contexte des micro-services avec une passerelle (gateway) :

Service Discovery avec Eureka : Eureka fournit un mécanisme de découverte de services dans un environnement de micro-services. Chaque micro-service s'enregistre auprès du serveur Eureka lors de son démarrage. Le serveur Eureka maintient un registre des micro-services enregistrés, en associant chaque service à un nom logique (ID) et à une liste d'adresses réseau où il peut être atteint.

Intégration avec la Gateway : Lorsqu'un client souhaite interagir avec un micro-service, il peut d'abord interroger le serveur Eureka pour obtenir l'adresse du micro-service. La gateway peut également utiliser Eureka pour découvrir dynamiquement les micro-services disponibles et configurer son routage en conséquence.
La Gateway, grâce à Eureka, peut fournir un routage dynamique et élastique en dirigeant le trafic vers les instances actuellement disponibles d'un micro-service spécifique. Cela facilite l'évolutivité et la résilience des applications basées sur des micro-services.

![image](https://github.com/Moujoudrana/Atelier3_5JEE/assets/93864104/3cf04a66-7b33-454d-9622-805021717df4)

# - Dépendances utilisés pour la réalisation:
  -h2: Intègre la base de données H2 en tant que base de données embarquée. 

  -lombok: Simplifie le code Java en fournissant des annotations pour générer automatiquement des méthodes telles que les getters, setters, constructeurs, etc. Cela permet de réduire la verbosité du code.

  -Spring DATA JPA : Pour conserver les données dans ‘SQL stores‘ avec Java Persistance API à l’aide de Spring Data et Hibernate. C'est un module qui facilite le ORM basé sur JPA. Il est utilisé avec les bases de données relationnelles.

  -Eureka client: Permet aux applications de s'enregistrer auprès d'un serveur Eureka et d'en tirer parti pour la découverte de services.

  -Spring web:  fournit une configuration de base et des dépendances nécessaires pour gérer les requêtes HTTP, les vues, les erreurs, et d'autres aspects liés au développement web, simplifiant ainsi le processus de création d'applications web robustes et extensibles avec Spring Boot.

  -Spring Boot Actuator: Offre plusieurs fonctionnalités pour aider à surveiller et gérer une application Spring Boot en production. 

  -OpenFeign: Principalement un client HTTP déclaratif qui simplifie l'appel de services web RESTful.

  -HATEOAS: Concept architectural qui vise à rendre les services web RESTful plus évolutifs et découvrables en incluant des liens hypertextes dans les réponses.

  -Gateway

  - Eureka Server: Utilisé pour la découverte et l'enregistrement des services dans un environnement de microservices.

# - Affichage:
