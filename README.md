Participer à notre blog
===================

Bienvenue sur le blog d'[ElevenLabs](http://blog.eleven-labs.com), il s'agit d'un site en Jekyll sur lequel **tout le monde** peut participer.

----------

Installer le blog
-------------

Le blog s'installe comme un projet classique.

**Prérequis**

Avoir [ruby](https://www.ruby-lang.org/fr/) d'installer sur sa machine dernière version.

**1 - Cloner le projet**
```bash
git clone git@github.com:eleven-labs/eleven-labs.github.io.git
```

**2 - Installer Jekyll**
```bash
gem install jekyll bundler
```
**3 - Lancer le blog**
```bash
cd eleven-labs.github.io && bundle exec jekyll serve
```
Vous devriez avoir le blog qui s'affiche dans votre navigateur préféré à l'adresse suivante http://localhost:4000

--------------------------------------------------------------------

Créer votre page auteur
-------------------------
**1 - Ajoutez votre page**

Dans le dossier `_authors` ajouter votre page.
```bash
cd _authors && touch login.md
```
**2 - Remplissez votre fiche**

Veuillez utiliser le template d'auteur suivant, vous pouvez copier template disponible dans le fichier `_authors/template-autor.md`

```md
---
layout: author
login: votre_login
name: Prénom Nom
twitter: Compte twitter
---
Votre Bio
```

**3 - Faite votre pull request**

Vous pouvez créer votre branche, avec le naming suivant.
```bash
git checkout -b feat/add-author-login
```

Il ne vous reste plus qu'a faire votre pull request, en mettant le TAG `publication`.

-------------------------

Créer votre article
----------------------------

**1 - Ajoutez votre article**

Dans le dossier `_drafts` ajoutez un fichier pour votre article avec le naming suivant.

```bash
AAAA-MM-DD-titre.md
```

**2 - Remplissez le template d'article**

Veuillez utiliser le template d'article suivant, vous pouvez copier template disponible dans le fichier `_drafts/template-article.md`

```md
---
layout: post
title: TITRE
excerpt: DESCRIPTION (VISIBLE SUR LA HOME)
author: LOGIN
permalink: /LANGUE (fr/en)/TITRE SANS ESPACES/
categories:
    - CATEGORIE 1
    - CATEGORIE 2
    - ...
tags:
    - TAG 1
    - TAG 2
    - ...
image:
  path: URL D'IMAGE DE HOME
  height: HAUTEUR DE L'IMAGE
  width: LARGEUR DE L'IMAGE
---

VOTRE ARTICLE EN MARKDOWN
```

**3 - Ecrivez votre article**

Votre article doit être écrit en [markdown](https://guides.github.com/features/mastering-markdown/) , il existe de nombreuses solution online pour écrire en markdown comme par exemple:

 - https://stackedit.io
 - http://dillinger.io

 Si vous avez besoin de mettre des images dans votre article il faut d'abord les ajouter dans le dossier suivant `assets` puis de les insérer dans votre article.

```md
![DESCRIPTION](/assets/MON IMAGE)
```

**4 - Demandez une la publication**

Une fois votre article terminer il faut déplacer le fichier de l'article du dossier `_drafts`au dossier `_posts`

```sh
cp _drafts/AAAA-MM-DD-NOUVEL-ARTICLE.md _posts/AAAA-MM-DD-NOUVEL-ARTICLE.md
```

Il vous suffit de faire une pull request avec le nom de branche suivante.

```bash
git checkout -b feat/add-article-TITRE
```

N'oubliez le tag  `publication`.

--------------------------------

Mettre en ligne un article
-----------

**1 - Validation d'un article**

Tout le monde peut commenter une pull request de `publication`, une fois approuvé elle est mergé dans master.

**ATTENTION**: Seulement quelques personnes ont le droit de merger les pulls requests

**2 - On partage**

L'article est ligne !!! Vous n'avez plus qu'a le partager.
