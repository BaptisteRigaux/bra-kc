# Bra-KC

Bra-KC est une application web développé dans le cadre de l'UE Gestion de projet en M1 MIAGE à Amiens.  
L'application permet de référencer des points d'intérêts sportifs dans la ville d'Amiens.

## Exigences

L'application nécessite l'installation de [docker](https://www.docker.com/get-started).

## Installation

Cloner le projet:
```
git clone git@github.com:Medd410/bra-kc.git
```

Construire et lancer les conteneurs:
```
docker-compose build
docker-compose up -d
```

Exécuter le conteneur et le serveur symfony:
```
docker exec -it php8-sf6 bash
cd bra-kc
composer install
symfony server:start -d
```

L'accès à l'application se fait depuis le navigateur à l'adresse : **127.0.0.1:9000**.  
Les fichiers sources du projet se trouvent dans le dossier **project**, ce dossier est un volume partagé avec le dossier **/var/www/html** se trouvant dans le conteneur **php8-sf6**.