# [__**Version Française**__](README_FR.md)

### Coding challenge for prospective candidates

## Application Challenge

### Intructions 

1. The objective is to create a runnable native mobile application in accordance to the acceptance criteria below.
1. The data required for each view is contained in the `/data` folder.
1. You are free to use any frameworks or plugins to assist you in the task. If you do so, please provide a brief reason why in the comments.
1. You are given creative freedom to design the UI as you deem fit to display the given data.
1. Provide any instructions required to build and run your application.
1. Instructions to share your code back with us will have been provided via email.

### Acceptance Criteria

**SCENARIO: The user launches your application for the first time.**   
GIVEN the user is on the home screen of their mobile device   
AND the user has never opened the application before    
WHEN the user opens the application    
THEN the user is presented with a landing page with a button labeled "Open".
___

**SCENARIO: The user taps "Open"**   
GIVEN the user is on the landing page   
WHEN the user taps the "Open" button   
THEN the user is taken to a page with a list of their accounts   
AND some data for each account    
AND the page has a "Quit" button in the navigation bar.
___

**SCENARIO: The user launches your application successive times**   
GIVEN the user is on the home screen of their mobile device    
AND the user has previously opened the application before     
AND the user has not clicked "Quit" during their previous session    
WHEN the user opens the application    
THEN the user is taken to a page with a list of their accounts    
AND some data for each account   
AND the page has a "Quit" button in the navigation bar.
___

**SCENARIO: The user wants to view the transactions of a particular account**      
GIVEN the user is viewing a list of accounts    
WHEN the user taps on a specific account    
THEN the user is presented with a view containing a transaction history for said account.
___

**SCENARIO: The user wants to stop viewing a list of accounts**      
GIVEN the user is viewing a list of accounts    
WHEN the user taps the "Quit" button    
THEN the user is presented with a landing page with a button labeled "Open".

## Service Challenge

### Instructions

1. The objective is to create REST services that wraps the JSON files and return them to the client according to the acceptance criteria below.
1. The data required for each service is contained in the `/data` folder.
1. You are free to use any frameworks or plugins to assist you in the task. If you do so, please provide a brief reason why in the comments.
1. Provide any instructions required to build and run your services.
1. Instructions to share your code back with us will have been provided via email.

### Acceptance Criteria

**SCENARIO: The client calls the service**   
GIVEN the client is calling the service   
WHEN the client sends the request   
THEN the data should be read from the JSON file and returned as JSON Payload in the response.
___
 
**SCENARIO: The client calls the service twice**   
GIVEN the client is calling the service for the second time   
AND the client has previously called the service successfully   
WHEN the client sends the request   
THEN the data should come from a cache and not read from file and returned as JSON Payload in the response.
___

**SCENARIO: The client passes a refresh parameter**   
GIVEN the call is made with a `x-refresh:true` header parameter   
AND the client has previously called the service successfully   
WHEN the client sends the request   
THEN the data should be flushed from the cache, retrieved from file and returned as JSON Payload in the response.
___

**SCENARIO: Client ask for the accounts list ("listOfAccounts.json")**   
GIVEN the client is calling the service to retrieve the list of accounts   
WHEN the client sends the request 
THEN the JSON response should contain a field named “total” that contains the sum of each account “balance”.
___

**SCENARIO: Client ask for a specific account ("listOfAccounts.json")**   
GIVEN the call is made with a `id={foo}` request parameter   
WHEN the client sends the request   
THEN the JSON response should only contains the account that has the `{foo}` id.

 ## Bonus - Optional
 Deploy your services in a cloud provider and set-up the app to call the services.
