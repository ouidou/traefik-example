# Traefik exemple

Ce dépôt met à disposition une configuration basique de [Traefik](https://docs.traefik.io/), ainsi que quelques exemples d'utilisations.

## Prérequis

- [docker](https://docs.docker.com/install)
- [docker-compose](https://docs.docker.com/compose/install)

## Traefik

Pour démarrer Traefik, lancer la commande suivante :

```
docker-compose -f ./traefik/docker-compose.yml up -d
```

Vous pouvez ensuite vous rendre sur le [Dashboard](http://localhost/dashboard/#/).

## Exemples

Pour lancer les exemples, lancer la commande suivante :

```
docker-compose -f ./samples/docker-compose.yml up -d
```

Ce docker-compose présente plusieurs cas de figures :

- sample-http : Exemple avec container docker accesible via web.sample.local en HTTP
- sample-https : Exemple avec container docker accesible via secure.sample.local en HTTPS
- sample-multiple : Exemple avec container docker accesible via app1.sample.local et app2.sample.local en HTTP
- sample-tls-redirect : Exemple avec container docker accesible via app3.sample.local en HTTPS et redirge le trafic HTTP vers HTTPS
