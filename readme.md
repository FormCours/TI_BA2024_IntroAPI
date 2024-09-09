# Intro au API
Un API, c'est quoi ?
API -> Acronyme de « Interface de programmation d'application »\
C'est la description des points d'acces pour intérragir avec un élément.

Les différentes API :
 - API de langague _(API du python -> https://docs.python.org/3/py-modindex.html)_
 - API d'un logiciel _(Les fonctionnalités)_
 - Web API _(Les routes d'un serveur)_

# Les Web API
Exposer des données et permettre une interaction de l'exterieur au systeme

## Les types d'API 
- Publique _(Exemple : Banque de donnée)_
- Privé/Interne
- Partenaires _(Externe, mais uniquement disponible avec des credentials)_

## Les protocoles / architectures d'API
### Restfull
Achitecure basé sur le protocole des requetes HTTP (Les méthodes / Les codes de réponse).\
https://developer.mozilla.org/fr/docs/Glossary/REST

Les contraintes de l'archi REST : 
 - Client/Serveur
 - Uniform UI
 - Stateless
 - Cacheable
 - Couche -> Séparation de responsabilité 

Les verbes de l'HTML
 - GET : Récuperation
 - POST : Ajout d'une ressource
 - PUT : Ajout ou mise à jours d'une ressource
 - PATCH : Mise à jours partiel
 - DELETE : Suppression d'une ressource

Quand l'utiliser :
 - Application Web ou Mobile
 - Permet de faire évoluer l'application
 - Facilement consomable via du JavaScript (si format JSON)

### SOAP
Basé sur du XML (Langague balisé) avec un configuration (client et serveur).\
https://developer.mozilla.org/fr/docs/Glossary/SOAP


Quand l'utiliser : 
 - Application complexe
 - Besoin d'une sécurité strict

### RPC
Permet la communication entre processus (Execution de procedure d'un systeme)\
https://en.wikipedia.org/wiki/Remote_procedure_call

Quand l'utiliser : 
 - Mise en place de temps réel entre un client et un serveur (Exemple : Signal R, SocketIO)

### GraphQL
Protocole qui permet au client de demande au serveur ce qui l'a besoin.\
https://graphql.org/learn/

Objectif, éviter le un probleme des API Restfull : 
 - Réponse incomplete -> Necessite plusieur requete.
 - Réponse trop complete -> Surcharge le réseau.

Méthode de fonctionnement :\
 - Le client envoi une requete POST
 - La requete du client contient un objet à populer
 - Le serveur traite la requete et renvoi l'objet completé

Quand l'utiliser : 
Permet de définir les besoins du coté du client et d'adapté facilement les requetes.

## Quelques exemples de Web API public
https://docs.irail.be/ \
https://openweathermap.org/current \
https://nominatim.org/release-docs/latest/api/Overview/ \
https://petstore.swagger.io/

# Utilisation d'un API

## Server Web API de test -> json-server
Ce logiciel permet de tester facilement un API via des fichiers JSON.\
A utiliser pour réaliser un prototype ou une démo.\
https://github.com/typicode/json-server

## Logiciel pour consommer une Web API
- Postman\
https://www.postman.com/
- Insomnia\
https://insomnia.rest/
- Thunder Client (Extension VSC)\
https://github.com/thunderclient/thunder-client-support
- Documentation Swagger (si disponible)

## Exemple de consommer une Web API
[Exemple d'une API](/demo/consommation-webapi.html)

### Documentation
#### Client
https://developer.mozilla.org/fr/docs/Web/API/Fetch_API/Using_Fetch \
https://rtavenar.github.io/poly_python/content/api.html
#### Serveur
https://flask.palletsprojects.com/en/3.0.x/ \
https://www.moesif.com/blog/technical/api-development/Building-RESTful-API-with-Flask/
