# DockerProjet

## Projet docker installé:
- wordpress
- heimdall
- projet perso vuejs
- phpmyadmin
- mysql
- mariadb
- postgres
- pgadmin
- gitea
- plik
- portainer
- phpldpadmin
- nextcloud
- bookstack
- openLdap

## Pour faire fonctionner le docker compose:

Etape 1: pull le projet

```sh
git clone https://github.com/doninj/DockerProjet.git
```

Etape 2: DuckDns
- Aller sur Ducker DNS et créer son adresse
- modifier dans le docker compose pour swag et dans les url pour mettre votre url 

Etape 3: Lancer le docker-compose

```sh
docker-compose up -d
```
Aprèe le docker-compose, il va falloir faire des modifications sur pour que le swag marche pour les redirections.

- Modifier tous les fichiers trouvable dans le dossier "configToAdd" dans "config/nginx/proxy-confs"
- Modifier dans /config/nginx/site-confs/default et commenter le bloc  location / { }

Ensuite redemarrer le container swag:
```
docker restart swag
```
Ensuite vous pouvez allez sur les pages correspondante:
- nextcloud
- portainer
- heimdall (page d'accueil)
- pgadmin
- phpmyadmin
- gitea
- phpladpadmin
- bookstack

### Lancer le projet personnel
Aller dans le dossier vue-docker

- Ensuite lancer le docker-compose
```sh
docker-compose up -d
```
puis allez sur le 
```sh
localhost:8080
```
vous pouvez tester de modifier le projet en hard reload

