# Digital_Banking_Projet
Ce compte rendu présente une étude de l'application de gestion des opérations pour les banques 
en utilisant les frameworks Spring Boot et Angular.
L'objectif principal de cette application est gérer les client a partir d'une platforme, 
leurs comptes et leurs opérations bancaires, telles que les dépôts, les retraits, les transferts.
L'application repose sur deux technologies : Spring Boot c'est un framework Java populaire pour le développement d'applications d'entreprise, 
et Angular, un framework JavaScript utilisé pour la création d'interfaces utilisateur.

# Spring Boot

![spting-boot](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/cf0a4e23-918f-4a53-97f9-3440838d8dc7)


Spring Boot est un framework open-source basé sur Spring, qui facilite le développement d'applications Java. Il fournit une approche simplifiée pour créer rapidement des applications autonomes, prêtes à être exécutées, avec des configurations par défaut intelligentes et des fonctionnalités intégrées.

Voici quelques caractéristiques clés de Spring Boot :

1. Configuration automatique : Spring Boot propose une configuration automatique basée sur les conventions. Il détecte les dépendances dans votre projet et configure automatiquement les composants nécessaires sans nécessiter de configurations explicites. Cela permet de réduire la quantité de code de configuration boilerplate.

2. Serveur intégré : Spring Boot intègre un serveur d'applications intégré (Tomcat, Jetty ou Undertow) afin que vous puissiez exécuter votre application directement, sans avoir à déployer un fichier WAR ou EAR dans un conteneur d'application externe.

3. Dépendances simplifiées : Spring Boot simplifie la gestion des dépendances en fournissant des starters préconfigurés. Les starters incluent les dépendances nécessaires pour développer des fonctionnalités spécifiques (par exemple, les starters pour les applications web, les bases de données, la sécurité, etc.), ce qui facilite leur intégration dans votre projet.

4. Actuateur : Spring Boot fournit l'Actuateur (Actuator), une fonctionnalité qui permet de surveiller et de gérer facilement votre application en exposant des endpoints (points d'accès) pour obtenir des informations sur la santé, les métriques, les journaux, etc.

5. Flexibilité et extensibilité : Bien que Spring Boot propose des configurations par défaut, il reste flexible et extensible. Vous pouvez personnaliser et ajuster la configuration en fonction de vos besoins spécifiques à l'aide de propriétés, de fichiers de configuration ou de classes de configuration personnalisées.

 # Angular 


![0_wuNf24urnMp7ypDp](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/7a17916b-2ced-40ed-922d-cd6dff814835)

Angular est un framework de développement d'applications web open-source basé sur TypeScript. Il est largement utilisé pour créer des applications web riches et interactives, des applications mobiles et même des applications de bureau. Angular est développé et maintenu par Google.

Voici quelques caractéristiques clés d'Angular :

1- Architecture orientée composants : Angular suit une architecture orientée composants où les fonctionnalités de l'application sont organisées en composants réutilisables. Les composants sont des éléments autonomes qui encapsulent la logique, les données et les vues.

2- Binding de données : Angular propose une liaison de données bidirectionnelle, ce qui signifie que les modifications dans les données du modèle (backend) sont automatiquement reflétées dans la vue (frontend), et vice versa. Cela permet de synchroniser facilement les données et l'interface utilisateur.

3- Gestion de l'état : Angular facilite la gestion de l'état de l'application en utilisant un concept appelé "services". Les services sont des classes qui permettent de centraliser et de partager des données et de la logique entre les différents composants de l'application.

4- Routage : Angular fournit un système de routage qui permet de créer des applications à pages multiples avec des routes définies. Cela permet de naviguer entre les différentes vues de l'application sans rechargement de page.

5- Testing : Angular met l'accent sur les tests unitaires et fournit des outils intégrés pour faciliter les tests unitaires et les tests d'intégration. Cela permet de garantir la qualité et la fiabilité de l'application.

6- Écosystème riche : Angular bénéficie d'un écosystème riche comprenant de nombreuses bibliothèques tierces, des outils de développement, une vaste documentation et une communauté active. Cela facilite le développement, la maintenance et l'évolution des applications Angular.

Angular est souvent utilisé en combinaison avec d'autres technologies, telles que TypeScript, HTML, CSS, RxJS, et différentes bibliothèques comme Angular Material pour créer des interfaces utilisateur modernes et réactives.

 # interaction entre le frontend et le backend
 ![spring-boot-upload-single-file](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/5bc4e154-576c-4463-b2a3-85914580d494)

 
 La communication entre Spring Boot et Angular dans une application typique suit généralement une architecture client-serveur. 
 Voici comment l'interaction entre le frontend et le backend peut se dérouler :

--> Le frontend Angular envoie une requête HTTP au backend en utilisant le module HttpClient d'Angular. La requête peut être GET, POST, PUT, DELETE, etc., en fonction de l'action requise.

--> Le backend Spring Boot reçoit la requête HTTP et la traite en fonction de l'endpoint spécifié. Il peut valider les données, effectuer des opérations, accéder à la base de données ou à d'autres sources de données, etc.

--> Le backend effectue les opérations nécessaires et renvoie une réponse HTTP au frontend. La réponse peut inclure les données demandées, des informations de statut (succès, échec, etc.) ou d'autres informations pertinentes.

--> Le frontend Angular reçoit la réponse du backend et met à jour l'interface utilisateur en conséquence. Il peut afficher les données reçues, afficher des messages d'erreur ou de succès, ou effectuer d'autres actions en fonction de la réponse du backend.

Cette interaction entre le frontend Angular et le backend Spring Boot se fait via des requêtes HTTP et des réponses, suivant les principes de l'architecture client-serveur. Les deux parties communiquent en utilisant des formats de données standard, tels que JSON, pour faciliter l'échange de données de manière structurée et cohérente.

--> Communication entre Spring Boot et MySQL :

Spring Boot utilise le module Spring Data JPA pour interagir avec la base de données MySQL de manière simplifiée.
Les entités Java sont définies pour représenter les tables de la base de données MySQL. Ces entités sont annotées avec des annotations telles que @Entity, @Table, etc., pour établir la correspondance entre les objets Java et les tables de la base de données.

#Architecture de l'application digitalBanking : 

![Capture d'écran 2023-06-25 213113](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/33c04484-d44c-483c-a7c8-98c76241e081)

# 1 - Backend 

![Capture d'écran 2023-06-25 213312](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/d7fbe3fc-c53f-4e36-98f5-064eedc94614)

--> les dependecies utilisée au niveau du fichier (pom.xml)

. Spring Data JPA : est un projet de Spring Framework qui simplifie l'interaction avec les bases de données relationnelles en utilisant la norme Java Persistence API (JPA)


![Capture d'écran 2023-06-25 213550](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/93bfa202-bc66-4d98-8e5a-ce122091ab66)


. Spring Web : Spring Web est un module du framework Spring qui facilite le développement d'applications web en utilisant Java. Il fournit des fonctionnalités et des composants pour la création de services web RESTful, le traitement des requêtes HTTP et la gestion des vues.
  
![Capture d'écran 2023-06-25 213752](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/0e7763c0-a829-4314-8d2c-75852b804420)

. H2 database : H2 Database est un système de gestion de base de données relationnelle écrit en Java. Il est léger, rapide et open source, et il est souvent utilisé pour le développement d'applications et les tests unitaires en raison de sa simplicité et de sa facilité d'intégration.


![Capture d'écran 2023-06-25 214220](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/d9b7ec87-0bbf-453e-bb75-f6db2ac052c9)

. MySQL est un système de gestion de base de données relationnelle populaire et largement utilisé. Il est open source, ce qui signifie qu'il est gratuit et dispose d'une vaste communauté de développeurs qui le soutiennent et le maintiennent.


![Capture d'écran 2023-06-25 214343](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/ec2983dd-fb0f-4189-b612-0296745697a4)

.Lombok : est une bibliothèque Java open source qui simplifie le développement en réduisant la quantité de code boilerplate (code répétitif) nécessaire pour les classes POJO (Plain Old Java Objects).


![Capture d'écran 2023-06-25 214501](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/fa9fb580-8eb6-45fc-b796-5804ca08d1a6)

. Springdoc-openapi-starter-webmvc-ui : est une bibliothèque open source pour la génération et la documentation automatique des API RESTful dans les projets Spring Boot. 


![Capture d'écran 2023-06-25 214640](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/f16e22ac-8718-422e-8381-1ee13313ae8c)


# Le fichier "application.properties" :


![Capture d'écran 2023-06-25 215054](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/39b7e433-355b-478e-9d98-b5ded24802a3)


-------->>>>  Tous les détails pour la couche DAO , la couche métier , la couche web vous allez avoir dans le projet 

# 2 - Frontend 
On commence par un nouveau projet de la technologie Angular avec la commande : ng new frontend.

![Capture d'écran 2023-06-25 215630](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/9ad76e3a-e918-40dc-b74b-bef079210e03)

. Les dependences utilisés dans le fichier "package.json":

1- Bootstrap et Bootstrap Icons sont deux outils populaires utilisés dans le développement web pour créer des interfaces utilisateur réactives et attrayantes.


![Capture d'écran 2023-06-25 215921](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/7d14c816-94a3-49fc-91ba-8cdc8100a86f)


2- Les modèles :
les modèles font référence aux structures  pour représenter et manipuler les données dans l'application. ils sont généralement des classes pour le langages TypeScript qui définissent la structure des objets de données et les fonctionnalités associées.


![Capture d'écran 2023-06-25 220105](https://github.com/othmanetozy/Digital_Banking_Projet/assets/92949683/d0b1a579-da7f-4529-a5f0-834e5a465d93)


 3- Les composants :
Un composant du Angular est généralement constitué de quatre parties principales : le template, la classe du composant, les styles associés et le fichier de test :

Le template définit la structure HTML de la vue du composant,

La classe du composant contient la logique 

Les styles 

Le fichier de test est utilisé pour écrire des tests unitaires pour le composant afin de vérifier son comportement et sa fonctionnalité attendus,

---->>>> Création d'un composant : ng g c componant-name.


#Conclustion

En conclusion, grâce à la combinaison de Spring Boot et d'Angular, l'application Digital Banking offre une solution complète et performante pour répondre aux besoins de gestion bancaire. Les technologies utilisées ont permis de développer une application robuste, sécurisée et conviviale, offrant aux utilisateurs une expérience bancaire agréable et efficace.















 
