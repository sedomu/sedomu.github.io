---
layout: post
title:  "Installer Jekyll sur MacOS"
date:   2023-07-26 11:00:00 +0200
last_modified_at:
#categories: jekyll update
author: 'sedomu'
---

## La doc

La [documentation officielle de Jekyll][jekyll-doc_macos]{:target="_blank"} montre pas à pas comment faire une fresh install. Par rapport à l'installation sur Windows, je la trouve un peu plus simple.

## L'install de Ruby via Homebrew

Dans le terminal:
1. Installer Homebrew: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
2. Suivre les explications d'Homebrew directement dans le terminal pour ajouter Homebrew au PATH.
2. Installer _chruby_ et _ruby-install_: `brew install chruby ruby-install xz`
3. Installer la dernière version stable de Ruby avec _ruby-install_: `ruby-install ruby 3.1.3`
4. Configurer le zshell pour utiliser automatiquement _chruby_ (3 lignes de commandes):
    * `echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc`
    * `echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc`
    * `echo "chruby ruby-3.1.3" >> ~/.zshrc`
5. Quitter le terminal et le réouvrir, puis contrôler la version de ruby: `ruby -v`

## L'install de Jekyll

Simplement exécuter la commande `gem install jekyll` dans le terminal.

_Voir la suite de la création d'un site Jekyll sur GitHub pages dans [ce post][yo-jekyll_github]. [Tout à la fin, car je n'ai pas trouvé de moyen de créer une ancre de lien dans un post Jekyll]_


[jekyll-doc_macos]: https://jekyllrb.com/docs/installation/macos/
[yo-jekyll_github]:{% post_url 2023-05-26-comment-creer-un-site-sur-github-avec-jekyll %}