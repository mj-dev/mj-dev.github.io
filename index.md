# Pokedex API  - Install

[![pipeline status](https://gitlab.com/Elioz/pokedex-api/badges/master/pipeline.svg)](https://gitlab.com/Elioz/pokedex-api/commits/master)
[![coverage report](https://gitlab.com/Elioz/pokedex-api/badges/master/coverage.svg)](https://gitlab.com/Elioz/pokedex-api/commits/master)
    

An API to get info on the Pokemons written in NodeJs/Express and Vue.js with Vue-Router and Vuex.

### Collection Postman dans le fichier "collectionPostman.json"

## Screnshots

<img src="https://github.com/victorgarciaesgi/Pokedex-Api/blob/master/captures/acceuil.png?raw=true">

<img src="https://github.com/victorgarciaesgi/Pokedex-Api/blob/master/captures/mypokemons.png?raw=true">
<img src="https://github.com/victorgarciaesgi/Pokedex-Api/blob/master/captures/pokemon.png?raw=true">


## Install MongoDB and launch it

```bash
mongod
```

## Import pokemon data

```bash
mongoimport --db Pokemondb --collection pokemons --file pokemon-data.json --jsonArray
```

## Install and start Node Server

```bash
yarn 
```
or
```bash
npm install
```


```bash
npm start
```

The api start on port http://localhost:3000

## Install and start Vue.js web pack server

```bash
cd ./Front
```

```bash
yarn 
```
or
```bash
npm install
```


```bash
npm run dev
```




The api start on port http://localhost:8080


# Workflow mis en place

* Une branche master qui correspond à l'environnement de PRODUCTION

* Une branche preprod qui correspond à l'environnement de PREPROD

* Chaques nouvelles demandes clients abouties à la création d'un ticket sur notre support

* Chaque création de branche est lié à un ticket

* Les devs doivent respecter la nomenclature de commit suivant : #numero_du_ticket : commentaire de commit

* Un template de MR a été créé pour les branches qui nécessitent de la review

* Le template assigne la MR au lead developer, ajoute le label pending-review, et met en copie le chef de projet

* Pour chaque push sur la branche master, des scripts de test sont exécutés et un deploiement sur heroku est lancé

* Nous utilisons JS Hint qui permet de valider le code JS pour la version ES6
