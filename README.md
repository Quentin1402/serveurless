# Mise en Place d'un Système de Gestion des Tâches Collaboratif

Le problème identifié concerne la gestion des tâches collaboratif. Nous fournirons un service minimaliste en serverless pour mettre en place un système de gestion des tâches collaboratif qui permettra aux équipes de planifier, d'attribuer, de suivre les tâches et d'améliorer la communication interne en utilisant Azure Functions et Azure Cosmos DB.

## Conception de l'architecture de solution

Stockage des données :

Utilisation d'Azure Cosmos DB pour stocker les données.
Pour créer une instance Cosmos DB avec l'interface Azure :
   Connectez-vous à votre compte Azure : Rendez-vous sur le portail Azure et connectez-vous à votre compte Azure.
   Créez une ressource Cosmos DB :    
     - Dans la barre de recherche, tapez "Azure Cosmos DB" et sélectionnez la suggestion qui apparaît.
     - Cliquez sur le bouton "Créer" pour démarrer le processus de création d'une ressource Azure Cosmos DB.
       ![image](https://github.com/Quentin1402/serveurless/assets/113422793/7ec8ee27-3c04-447e-87a8-9faabae5d3ef)
     - Cliquez sur MongoDB :
       ![image](https://github.com/Quentin1402/serveurless/assets/113422793/c780a055-afe0-4163-8d6a-5c4af44fba74)
     - Configurez la ressource Cosmos DB :   
        Choisissez un groupe de ressources existant ou créez-en un nouveau. Les groupes de ressources permettent de regrouper des ressources Azure pour une gestion simplifiée.
        Dans la section "Nom du compte", donnez un nom à votre base de données Cosmos DB.   
        Créez la ressource : Cliquez sur le bouton "Vérifier + créer" pour vérifier vos paramètres. Une fois que tout est correct, cliquez sur "Créer" pour créer la ressource Cosmos DB. Le déploiement peut prendre quelques minutes.
        Accédez à votre base de données Cosmos DB : Une fois le déploiement terminé, vous pouvez accéder à votre base de données Cosmos DB à partir du portail Azure. Dans le tableau de bord de la ressource Cosmos DB, vous trouverez des informations sur la base de données, les clés d'accès, les chaînes de connexion, etc.
        Une fois sur votre base de données cliquez sur Ajouter une collection
        ![image](https://github.com/Quentin1402/serveurless/assets/113422793/990150f0-4034-4653-8c3b-66d8b0a544ef)
        Entrez un nom de base de données et un nom de collection et cliquez sur ok.
   Votre base de données est maintenant créé.

Traitement des données :

Utilisation d'Azure Functions pour traiter les données stockées dans Azure Cosmos DB.
Connectez-vous à votre compte Azure : Rendez-vous sur le portail Azure et connectez-vous à votre compte Azure.
   Créez une ressource Azure Function : 
     - Dans la barre de recherche, tapez "Application de fonction" et sélectionnez la suggestion qui apparaît.
     - Cliquez sur le bouton "Créer" pour démarrer le processus de création d'une ressource Azure Function.
       ![image](https://github.com/Quentin1402/serveurless/assets/113422793/29941512-4cca-456a-a5a5-9e5573315a56)
     - Configurez la ressource Azure Function :   
        Choisissez un groupe de ressources existant ou créez-en un nouveau. Les groupes de ressources permettent de regrouper des ressources Azure pour une gestion simplifiée.
        Dans la section "Nom de l'application", donnez un nom à votre Azure Function. 
        Sélectionnez le déployement par code puis choisissiez votre langage et sa version dans cette exemple nous prendrons node.js 18 ensuite choisissez serverless comme hebergement
        ![image](https://github.com/Quentin1402/serveurless/assets/113422793/d503248a-9189-40f0-80cc-a15849c27b9e)
        Créez la ressource : Cliquez sur le bouton "Vérifier + créer" pour vérifier vos paramètres. Une fois que tout est correct, cliquez sur "Créer" pour créer la ressource Azure Function. Le déploiement peut prendre quelques minutes.
        Accédez à votre Azure Fonction : Une fois le déploiement terminé, vous pouvez accéder à votre fonction à partir du portail Azure.
        Une fois sur votre Azure Fonction cliquez sur "Créer"
        ![image](https://github.com/Quentin1402/serveurless/assets/113422793/3236fb8b-4834-4b61-900d-74c3f18bd588)
        Choisissez comment créer votre function ici avec le portail Azure, choissisez HTTP trigger et cliquez sur "Créer".
        ![image](https://github.com/Quentin1402/serveurless/assets/113422793/f04fd0a8-86df-4e90-8c58-80a6e549fd88)
        Allez sur votre fonction.
        ![image](https://github.com/Quentin1402/serveurless/assets/113422793/7b66be4d-113e-4fc1-b773-414a0a508de5)
        Cliquez sur code + test.
        ![image](https://github.com/Quentin1402/serveurless/assets/113422793/f723297d-4d75-4f25-927f-9858daa602f9)
        Ensuite mettez le code du fichier function à la place du code en exemple en vous assurant de remplacer 'username', "password", "your-cosmosdb-uri", "your-database-name", et "your-collection-name" par les informations spécifiques à votre instance Cosmos DB.
   Votre fonction est maintenant créé.

