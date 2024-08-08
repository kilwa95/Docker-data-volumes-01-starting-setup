# Data Volume Example

Ce projet est un exemple simple d'application Node.js utilisant des volumes Docker pour gérer des données persistantes. 

## Prérequis

Avant de commencer, assurez-vous d'avoir installé les éléments suivants :

- [Docker](https://www.docker.com/get-started)

## Installation

 Clonez ce dépôt ou téléchargez les fichiers.



### Construire l'image Docker

Avant de pouvoir exécuter l'application, vous devez construire l'image Docker :

```bash
docker build -t feedback-node .
```
## Exécuter le conteneur

```bash
docker run -p 3001:80 -d --name feedback-app-volumes -v feedback:/app/feedback feedback-node:volumes
```

## supprimer un volume

```bash
docker volume rm feedback
```
OU
```bash
docker volume prun
```