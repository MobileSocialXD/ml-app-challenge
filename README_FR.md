### Défi de programmation pour les candidats potentiels
## Défi d'application
### Instructions
1. L'objectif est de créer une application mobile native exécutable répondant aux critères d'acceptation ci-dessous.
2. Les données requises pour chaque vue sont contenues dans le dossier `/data`.
3. Vous êtes libre d'utiliser des frameworks ou des plugins pour vous aider dans cette tâche. Si vous le faites, veuillez expliquer pourquoi dans les commentaires.
4. Vous disposez d'une liberté de création pour concevoir l'interface utilisateur à votre convenance pour afficher les données.
5. Indiquez toutes les instructions nécessaires pour créer et exécuter votre application.
6. Les instructions pour partager votre code avec nous auront été fournies par courriel.

### Critères d'acceptation
**SCÉNARIO: L'utilisateur lance votre application pour la première fois.**   
LORSQUE l'utilisateur est sur l'écran d'accueil de son appareil mobile   
ET l'utilisateur n'a jamais ouvert l'application auparavant   
QUAND l'utilisateur ouvre l'application   
ALORS l'utilisateur se voit alors proposer une page de destination avec un bouton intitulé « Ouvrir ».
___

**SCÉNARIO: L'utilisateur tape sur « Ouvrir »**       
LORSQUE l'utilisateur est sur la page d’accueil de l’application   
QUAND l'utilisateur appuie sur le bouton « Ouvrir »    
ALORS l'utilisateur est amené à une page avec une liste de ses comptes   
ET quelques données pour chaque compte   
ET la page a un bouton « Quitter » dans la barre de navigation.
___

**SCÉNARIO: L'utilisateur lance votre application plusieurs fois successivement**       
LORSQUE l'utilisateur est sur l'écran d'accueil de son appareil mobile      
ET l'utilisateur a déjà ouvert l'application auparavant     
ET l'utilisateur n'a pas tapé sur le bouton « Quitter » lors de sa session précédente     
QUAND l'utilisateur ouvre l'application     
ALORS l'utilisateur est amené à une page avec une liste de ses comptes  
ET quelques données pour chaque compte  
ET la page a un bouton « Quitter » dans la barre de navigation.   
___

**SCÉNARIO: L'utilisateur veut voir les transactions d'un compte particulier**  
LORSQUE l'utilisateur visualise une liste de comptes    
QUAND l'utilisateur tape sur un compte spécifique   
ALORS L'utilisateur est alors présenté une vue contenant un historique des transactions pour ledit compte.
___

**SCÉNARIO: L'utilisateur veut arrêter de visualiser une liste de comptes**     
LORSQUE l'utilisateur visualise une liste de comptes    
QUAND l'utilisateur appuie sur le bouton « Quitter »  
ALORS L'utilisateur se voit rediriger vers la page d’accueil de l’application avec un bouton intitulé « Ouvrir ». 

## Défi de service
### Instructions
1. L'objectif est de créer des services REST répondant aux critères d'acceptation ci-dessous.
1. Les données requises pour chaque service sont contenues dans le dossier `/data`.
1. Vous êtes libre d'utiliser des « frameworks » ou des plugins pour vous aider dans cette tâche. Si vous le faites, veuillez expliquer pourquoi dans les commentaires.
1. Indiquez toutes les instructions nécessaires pour créer et exécuter votre application.
1. Les instructions pour partager votre code avec nous auront été fournies par courriel.

### Critères d'acceptation
**SCÉNARIO: Le client appelle un service.**   
LORSQUE le client appelle le service   
QUAND le client envoie la requête   
ALORS les données devraient être lu du fichier JSON et retourné au client en format JSON.
___

**SCÉNARIO: Le client appelle un service une deuxième fois.**   
LORSQUE le client appelle le service une seconde fois   
QUAND le client envoie la requête   
ALORS les données devraient provenir d’une « cache », ne pas être lu du fichier et retournées au client en format JSON.
___

**SCÉNARIO: Le client utilise un paramètre « refresh »**   
LORSQUE le client appelle le service avec le paramètre « header »  suivant: `x-refresh:true`   
QUAND le client envoie la requête   
ALORS les données devraient être vidées de la cache, devraient être lu du fichier JSON et retournées au client en format JSON.
___

**SCÉNARIO: Le client demande la liste de comptes (« listOfAccounts.json »)**   
LORSQUE le client appelle le service pour avoir la liste de comptes   
QUAND le client envoie la requête    
ALORS la réponse JSON retourné au client devrait contenir un champ « total » qui est la somme des champs « balance » de chaque compte. 
 
**SCENARIO: Le client demande un compte spécifique (« listOfAccounts.json »)**   
LORSQUE le client appelle le service avec un paramètre de requête `id={foo}`   
QUAND le client envoie la requête  
ALORS la réponse JSON retourné au client devrait contenir seulement le compte qui possède un id `{foo}`.
 
 ## Boni - Optionnel
 Déployer vos services sur un « cloud provider » et configurer votre application pour appeler vos services.
