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

## Configuration

1. **Configuration Azure Functions :** Assurez-vous d'avoir une instance Azure Functions configurée et prête à l'emploi.
