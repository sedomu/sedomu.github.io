---
layout: post
title:  "Comment créer un site sur GitHub avec Jekyll"
date:   2023-05-26 19:35:00 +0200
#categories: jekyll update
author: 'sedomu'
---

## Pour commencer : pourquoi?

Tout MOOC, formation gratuite, ebook, tuto sur YouTube, etc. conseille de compléter son apprentissage en créant un blog parlant de son apprentissage, afin de nourrir l'apprentissage des autres et de mettre en perspective ce que l'on a appris. Sur le papier, ça à l'air top. La restitution est un superbe exercice qui permet d'avoir une autre approche sur les choses que l'on a découvertes, et cela peut prendre plusieurs aspects:
* faire par soi-même: à regarder passivement une vidéo, ou à faire un pas-à-pas en même temps qu'on lit un cours reste réaliser un projet dont généralement, on va pas se mentir, on a pas grand chose à foutre et qui est plus ou moins encadré, laissant beaucoup moins de place à l'erreur (j'explique pas ici le principe d'apprendre de ses erreur, chacun sait que ça marche bien quand même);
* restituer: à se faire expliquer quelque chose, on a l'impression d'avoir appris des trucs. Quand vient le moment, à son tour de l'expliquer, on réalise qu'on y est pas encore (le fameux: "ah ben oui, on pourrait faire ça... mais faut pas... parce que... elle a dit qu'il fallait faire comme ça..." - ah merde, pas sûr d'avoir compris). Et l'exercice d'expliquer est autant formateur que le point précédent. Et amène au point suivant:
* comprendre les briques qui nous manquent: pour t'expliquer le truc, j'ai besoin de savoir dans quel ordre te montrer les choses. C'est un travail de déconstruction qui permet de remettre en perspectives tous les petits bouts que je connais déjà, ou ceux qui vont m'intéresser par la suite. Je pense que cet effet est particulièrement utile lorsque l'on apprend en solo: pendant toute une scolarité, puis tout un parcours académique, on apprend des trucs dans un cadre, un ordre déterminé et on le fait dans un but unique, avoir son diplôme, quand bien même il y a de fortes chances que pour beaucoup de monde, le jour où t'as disséqué une grenouille en 4e ne te serve jamais dans la vie. Et le cadre, l'ordre et le but sont bien trois choses totalement absentes d'un parcours d'apprentissage en solo (c'est ce qui rend le truc pas si facile, en fait);
* enfin, en écrivant à la volée comme ça, le dernier point qui me vient à l'esprit, c'est l'inverse du précédent. En faisant des side-projects, comme par exemple expliquer ce qu'on a appris, on peut se rendre compte qu'on a progressé et que mine de rien, c'était pas si inutile ces heures passées sur ce sujet. Ca rassure, ça fait du bien, et ça contrebalance aussi le sentiment de vertige face à la montagne de trucs que tu souhaite apprendre (car au début, plus t'apprends, plus t'apprends que tu as a apprendre, ce qui cède facilement la place à l'abandon).

Si on se rapproche un peut plus du sujet de base maintenant: on pourrait se dire "pourquoi se faire chier à créer un site avec Jekyll, sur GitHub, qui donne un truc tout moche alors qu'il existe de plus en plus de services, plutôt propres, pour faire de très jolis sites un peu plus dans l'air du temps?" J'irai même un peu plus loin en disant que j'ai déjà fait par le passé plein de petits sites persos: je sais utiliser html, css, php, javascript, et par extension je peux avoir une bonne utilisation de CMS (WordPress, Drupal). Et j'ai ma préférence pour du html en mode débile, tout à la main, en récupérant un petit template css (parce que c'est relou le css). Mais pour se mettre à faire des choses, il peut être très intéressant de chercher à se faciliter quand même au maximum la vie. Si je crée un petit site perso, je vais passer davantage de temps à régler quelques détails qui vont me déplaire sur le css récupéré, polisher le tout à ma sauce, penser et repenser l'organisation du site, etc. que d'écrire des posts. Et puis, pour écrire un post [en html à la main comme un débile], il faudra que je copie-colle un morceau de code, au bon endroit, que j'écrive, que je fitte le tout à mon layout, etc. autant de raisons pour ne pas ajouter un post, qui de toute façon ne sera lu par personne...

Et c'est là ou vient Jekyll. Un compte GitHub? J'en ai déjà un, dont je me sers pour garder mes petits projets web perso. Une petite install sur ma machine et il ne me reste plus qu'à écrire des posts. Envie de poster? Il suffit de créer un nouveau fichier tout vierge, écrire sans penser à aucun instant au layout ou à quelconque code. Un commit directement depuis mon éditeur et c'est en ligne. L'idée là, c'est de se simplifier la vie pour se donner une chance de faire : l'idée de faire est toujours plus séduisant que de s'y mettre vraiment. On se simplifie donc ici la tâche.

## Ensuite : comment?

Toujours partant de l'idée du paragraphe précédent, autant appliquer la méthode KISS: Keep It Simple, Stupid.

Alors oui, on peut faire des trucs super sympa avec Jekyll. Il y a foultitude de gens qui se sortent les doigts pour faire des choses assez poussées. C'est sexy. Mais d'une, j'ai pas envie d'avoir une seule fois le besoin de déboguer un truc que j'ai pas conçu sur ce projet et de deux, par défaut Jekyll est fonctionnel, il répond à mes besoins (qui est je le rappelle d'écrire des posts sans aucune contrainte), et même si j'ai bien envie de trifouiller dedans et d'essayer de faire un truc à mon goût, ce n'est pas ce pourquoi je l'ai créé (qui est je le rappelle d'écrire des posts sans aucune contrainte - la répétition est importante ici).

Encore une fois, tu regardes [la vidéo d'il y a 8 ans de Grafikart][grafikart-jekyll]{:target="_blank"}, il te montre comment faire un truc très drôle, en vitesse x1000 que tu ne peux pas le suivre, sur une vidéo d'une heure, avec Jekyll. C'est une très bonne vidéo: elle donne envie de jouer avec ce programme. Mon install, et ce que je vais montrer ici, c'est comment démarrer le site, comme un débile en suivant la doc, avec les pré-sets et le template par défaut. Ca m'a pris une grosse demi-heure,temps d'install de Ruby compris, sans aucun soucis dans le process.

## Enfin : commençons!

### Ce que j'avais déjà

* Un ordi, avec Windows dessus
* Un compte GitHub
* Une install de VS Code de base avec l'extension GitHub

### Ce que j'ai fait

#### Créer le site:
1. Aller voir la doc de [Jekyll][jekyll-quickstart]{:target="_blank"} et tout faire comme ils disent, pour installer Ruby et Jekyll. Dans l'ordre:
    1. Installer [RubyInstaller][rubyinstaller-home]{:target="_blank"}, avec toutes les options par défaut
    2. A la dernière étape de l'installation, cocher l'exécution de `ridk install`
    3. Choisir l'option `MSYS2 and MINGW development tool chain` dans le prompt, puis fermer (Ruby est installé)
    4. Ouvrir un PowerShell et exécuter la commande `gem install jekyll bundler`, Jekyll est installé
2. Créer un nouveau dépôt GitHub `sedomu.github.io` et le synchroniser.
    1. Pour le coup, j'avais jamais essayé GitHub desktop. Je l'ai fait avec ça. Et je ne pense pas m'en servir à nouveau un jour... Ca sert à rien non?
    2. Créer un dépôt nommé selon la convention `sedomu.github.io` (sedomu, c'est mon blase sur GitHub)
    3. Le synchroniser dans mon dossier de code. En gros, un bon vieux `git init`, ça serait allé plus vite je crois. Je te l'aisse faire comme tu le souhaites.
3. Avec le terminal, aller dans le dossier du dépôt et créer le site
    1. `jekyll new .\ --force` - le "--force", c'est parce que je suis un bourrin, que Jekyll veut un dossier complètement vide, mais il y avait un .gitignore et un README.md...
    2. Il n'y a plus qu'à commit. GitHub reconnaît Jekyll et va le compiler comme un grand. T'attends un peu et le site est en ligne à l'adresse `sedomu.github.io`

#### Pimper le site:
1. Aller voir dans `_config.yml` et changer les trucs utiles (titre, adresse mail, description, etc.)
2. Là, on peut lancer un serveur local pour voir ce que donnent les changements: `jekyll serve`. Ca permet de voir l'avancement en allant sur l'url qu'il te donne (logiquement le port 4000 de ton localhost). Dès que t'écris un truc, ça se met à jour. Ca marche pour tout, sauf quand tu changes `_config.yml` où il faut relancer le serveur.
3. Aller voir dans `about.markdown` et changer le texte.
4. Créer une page pour tester tout ça : forcément, un "[hello world!][yo-helloworld]{:target="_blank"}".
5. Quand t'es content, tu commit, t'attends un peu que ça se build, et tu admires le résultat.

Alors, en effet, je susi allé dans certains détails, mais pas d'autres (fonctionnement de GitHub), mais après tout, c'est mon premier article. Je reste content d'avoir écrit quelque chose et de le publier.

[grafikart-jekyll]: https://grafikart.fr/tutoriels/jekyll-505
[jekyll-quickstart]: https://jekyllrb.com/docs/
[rubyinstaller-home]: (https://rubyinstaller.org/)
[yo-helloworld]:{% post_url 2023-05-25-hello-world %}