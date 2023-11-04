---
layout: post
title:  "Anaconda m'énerve"
date:   2023-11-04 21:30:00 +0100
last_modified_at:
#categories: python venv
author: 'sedomu'
---

## Anaconda

Anaconda, pour moi, c'était une promesse de gérer ses environnements virtuels avec une grande dose d'abstraction: lancer, créer un environnement, se laisser guider par un choix de paquets, utiles, pour démarrer avec du Python. Au premier abord, ça m'a rappelé les premiers gestionnaires de paquets graphiques sous Ubuntu: c'est pas particulièrement sexy et tu ne te sens pas trop guidé. Bon, j'ai pu faire l'installation, commencer à utiliser `jupiterlab` et tout ça, tout ça. Mais quand je veux y revenir, j'ai bien envie de tout mettre à jour quand je vois le nombre de paquets Updates available (l'habitude du `apt-get update|upgrade` immédiatement après avoir ouvert une session Linux), mais si le `root` se met bien à jour, mon environnement de travail, non...

Et là, il ne démarre même plus sur mon mac...

Je pense que j'aurai une meilleure maîtrise de mes environnements et de comment ça marche `underneath the hood` si je gère moi-même mes environnements virtuels et mes bibliothèques.

## Les mains dans le cambouis

J'ai bien vu des Youtubers utiliser des `venv`, je pense comprendre au-moins de manière abstraite le principe et les avantages (je n'ai pas envie de pourrir mon mac avec des instal douteuses et concurrentes), mais... je ne sais pas comment démarrer. Et je ne me sens pas encore à l'aise avec la doc Python pour ce faire.

On ne va pas faire semblant, et garder un niveau de confort digne d'un débutant: un morceau de cours d'[OpenClassrooms](https://openclassrooms.com/fr/courses/6951236-mettez-en-place-votre-environnement-python/7013854-decouvrez-les-environnements-virtuels){:target="_blank"} répond tout à fait à cette problématique.

C'était extrêment clair et rapide. Facile aussi à mettre en oeuvre. Je me ferai donc juste une cheatsheet ici.

## Python _venv_ cheatsheet

### Prérequis

`venv` n'est disponible qu'à partir de la version 3.3 de Python.
`pip freeze` donne l'ensemble de la configuration.
`pip list` liste les bibliothèques installées.

### Manipuler les environnements virtuels

| Commande | Commentaires |
| -------- | ------------ |
| `python -m venv` _env_ | Crée dans le répertoire actuel l'environnement nommé _env_ |
| `source` _env/bin/activate_ | Activer l'environnement nommé _env (chemin relatif)_ |
| `deactivate` | Désactiver l'environnement actuel indiqué par (_env_) dans le terminal |

Supprimer un environnement virtuel en... supprimant le répertoire _env_.

### Manipuler les _requirements.txt_

| Commande | Commentaires |
| -------- | ------------ |
| `pip freeze > requirements.txt` | Exporter la config dans le répertoire actuel dans **requirements.txt** |
| `pip install -r requirements.txt` | Charger la config de **requirements.txt** |

## A propos d'Anaconda

Du coup, mon `pip freeze` dans l'environnement global, il ressemble à rien aujourd'hui.

731 lignes au total avec des routes (? - plein de @) et des liens vers des fichiers `file:///`, nom d'utilisateur (surement entre autres) = cbousseau. Ca ne me plaît pas beaucoup, ça fait négligé 😅

Je vais suivre la [documentation](https://docs.anaconda.com/free/anaconda/install/uninstall/){:target="_blank"} sur la désinstallation.

Il y en avait partout dans les $PATH... C'est nettoyé.

`pip` n'a plus que 11 paquets (qui doivent provenir de l'installation via homebrew?). Je laisse tout ça, ça paraît mieux.