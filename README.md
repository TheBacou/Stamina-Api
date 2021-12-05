[![Discord](https://img.shields.io/discord/880133347446247574?color=informational&logo=discord&logoColor=white)](https://discord.gg/rCg6C7YJXJ)
[![NPM](https://img.shields.io/npm/v/stamina-api?color=crimson&logo=npm)](https://www.npmjs.com/package/stamina-api)
[![Download](https://img.shields.io/npm/dt/stamina-api)](https://www.npmjs.com/package/stamina-api)


# Stamina API

Ce paquet Npm fourni une interface pour intéragir avec
[l'API de Stamina](https://discord.gg/rCg6C7YJXJ)

## Installation

Vous pouvez simplement installer la dépendance à votre projet depuis Npm
:

```shell
$ npm install stamina-api
```

## Mise en place

### Importation

```js
const Stamina = require('stamina-api');
```

## Utilisation

### Blague aléatoire

```js
const blague = await Stamina.get("jokes").byType("random")
```

Avec cette méthode, vous pouvez spécifier certains types que vous ne souhaitez pas
recevoir.

```js
const blague = await Stamina.get("jokes").byType("random", {
  disallow: ['dark', 'limit']
});
```

### Blague aléatoire d'une catégorie

```js
const blague = await Stamina.get("jokes").byType('dev');
```

### Blague à partir de son ID

Les blagues sont identifiées par un ID que vous recevez en même tant que chaque
blague.

Spécifiez cet identifiant en paramètre et vous l’obtiendrez à nouveau.

```js
const blague = await Stamina.get("jokes").byID(50);
```

## Valeur retournée

```js
// console.log(blague);

{
  "id": 1,
  "type": "dev",
  "content": {
    "blague": "Question.",
    "reponse": "Réponse."
  }
}
```
