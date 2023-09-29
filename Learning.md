# Docker

### Construire une image d'application
```bash
docker build -t image-name .
```
La commande `docker build` Permet de créer une image en se basant dur le fichier Docker (Dockerfile). 

Chaque image créer par Docker possède un ID(long et difficile à mémoriser). Pour éviter de saisir à chaque fois cet ID, on utilise un nom pour représenter l'image. le drapeau `-t` permet nommer notre image. Il sera utile lorsqu'on voudras executer notre container.

Le `.` à la fin de la commande permet de spécifier à Docker dans quel dossier il doit chercher le fichier de configuration (Dockerfile). Dans notre cas il s'agit du dossier courant.


### Démarer un container d'application

```bash
docker run -dp 127.0.0.1:3000:3000 getting-starded
```

`docker run` permet de d'exécuter l'application dans  un container

Le drapeau `-d` (version courte de `--detach`) permet d'exécuter le container en arrière plan 

Le drapeau `-p` (version courte de `--publish`) permet de créer une liaison entre l'adresse de la machine(hôte ou HOST) et le port du container sur lequel l'image se situe. cette commande s'écrit généralement sous la forme `host:containerPort`. Ceci permet d'acceder à l'application (dans le container) depuis l'hôte(notre machine).


### Gestion des container 

```bash
docker ps
```
Permet de lister tous les container disponible.


```bash
docker stop <the-container-ID>
```
Permet de stopper un container


```bash
docker rm <the-container-ID>
```
Permet de supprimer un container