<p align="center">
  <a href="https://angular.io/" target="blank"><img src="https://angular.io/assets/images/logos/angular/angular.svg" width="120" alt="Angular Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/angular/angular/main?token=abc123def456
[circleci-url]: https://circleci.com/gh/angular/angular

<p align="center">Un framework moderne et puissant pour construire des applications web scalables côté client.</p>
<p align="center">
<a href="https://www.npmjs.com/package/@angular/core" target="_blank"><img src="https://img.shields.io/npm/v/@angular/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/package/@angular/core" target="_blank"><img src="https://img.shields.io/npm/l/@angular/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/package/@angular/core" target="_blank"><img src="https://img.shields.io/npm/dm/@angular/core.svg" alt="NPM Downloads" /></a>
<a href="https://discord.gg/angular" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://twitter.com/angular" target="_blank"><img src="https://img.shields.io/twitter/follow/angular.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>

## Description

Cette application front-end est conçue pour le dashboard des bots Discord en utilisant le framework Angular.

## Sommaire

- [Normes des Commits et Pull Requests](#normes-pour-les-commits-et-les-pull-requests)
- [Installation](#installation)
- [Configuration et Démarrage](#configuration-et-démarrage)
- [Tests](#tests)

- [Contributeurs](#contributeurs)


# Normes pour les commits et les pull requests ✍️

Afin de maintenir une cohérence et une clarté dans notre travail collaboratif, nous avons mis en place des normes pour les messages de commit et les pull requests.

## Utilisation de GitFlow

Le projet suit le workflow GitFlow pour la gestion des branches. Voici les principales branches à utiliser :

- `main` : Branche de production, contient le code stable
- `develop` : Branche principale de développement
- `feature/*` : Branches pour les nouvelles fonctionnalités
- `hotfix/*` : Branches pour les corrections urgentes
- `release/*` : Branches pour la préparation des versions

Règles importantes :
- Toute nouvelle fonctionnalité doit partir de `develop` et créer une branche `feature/nom-de-la-feature`
- Les corrections urgentes partent de `main` avec une branche `hotfix/nom-du-fix`
- Les branches `feature` sont fusionnées dans `develop`
- Les `hotfix` sont fusionnés dans `main` ET `develop`

## Messages de commit

Les messages de commit doivent suivre ce format :

    type(portée): titre du commit

### Explication :

**_type_** : Le type de modification, par exemple "fix" ou "feat".

**_portée_** : Le dossier concerné (un commit par fichier modifié, supprimé ou ajouté).

**_titre du commit_**: Une description concise du changement apporté. En l'occurence  (en anglais)

### Exemple :

```
  feat(auth): add login button
```

## Body du commit (corps détaillé)

**_Ajouter un body_** : Si le titre du commit n'est pas assez explicite sur la localisation de la modification, le nom du fichier doit être précisé dans le body.

### Exemple :

```
In file "login.component.ts"
```

Cela permet de donner plus d'informations sur les raisons du changement, son impact ou les fichiers modifiés.

## Longueur des commits

**_Bonne pratique_** : Respecter une longueur maximale d'environ 50 caractères pour les titres des commits. Cela permet d'avoir des messages concis, faciles à lire et à comprendre.

## Commits atomiques

**_Commits atomiques_** : Chaque commit doit être atomique, c'est-à-dire qu'il doit se concentrer sur une seule fonctionnalité ou un seul changement.
Cela veut dire un commit par fichier modifié, supprimé ou ajouté au minimum.

Cela garantit une meilleure traçabilité et simplifie la gestion des erreurs.

## Noms des pull requests

**_Nom en anglais_** : Les titres des pull requests doivent être rédigés en anglais pour garantir une compréhension globale de l'équipe.

## Labels sur les pull requests

**_Ajout de labels_** : Chaque pull request doit inclure un ou plusieurs labels pour faciliter la gestion des PRs.

Les labels indiquent le type de changement.

Par exemple :

![Hotfix](https://img.shields.io/badge/Hotfix-ff0000?style=flat)
![Feature](https://img.shields.io/badge/Feature-blue?style=flat)

## Noms de fichiers

**_Nom des fichiers en français_** : Les noms des fichiers dans le projet doivent être en français pour garder une cohérence avec la langue principale du projet.

Utiliser le **kebab-case** : Les noms de fichiers doivent être écrits en kebab-case, c'est-à-dire tout en minuscules, avec des mots séparés par des tirets.

**_Exemple_** :

    gestion-utilisateurs.js
    verifier-email.md

## Suivi des changements dans les pull requests

**_Demandes de changements détaillées par les reviewers_** : Si un reviewer exige des modifications sur une pull request, il doit clairement spécifier dans un commentaire les changements à effectuer.

Le reviewer doit fournir une explication détaillée pour s'assurer que le contributeur comprend bien les modifications demandées. Cela favorise la transparence et permet à tous les membres de l'équipe de suivre l'évolution de la pull request.

## Processus d'approbation et de fusion des pull requests

**_Approbation partagée_** : Une pull request doit être validée par au moins un membre du groupe émetteur de la PR en question.

**_Nombre minimum de reviewers_** : Pour qu'une pull request soit fusionnée, elle doit être approuvée par un minimum de trois reviewers, y compris des membres externes au groupe émetteur, afin de garantir une évaluation complète et de qualité.

**_Validation du Tech Lead_** : Parmi les reviewers, le Tech Lead du groupe émetteur de la pull request doit obligatoirement faire partie des approbateurs. L'approbation finale du Tech Lead est nécessaire pour qu'un membre du groupe puisse procéder à la fusion. Il revient au Tech Lead de donner l'aval définitif, assurant que la pull request est prête à être intégrée dans la base de code principale.

**_Responsabilité lors de la fusion_** : Le tech lead qui approuve le merge d'une pull request est responsable de la fusion de celle-ci. En acceptant de fusionner la pull request, il accepte également de prendre la responsabilité en cas de problèmes futurs liés à cette pull request.

**_Interdiction pour l'émetteur de fusionner sa pull request_** : L'émetteur de la pull request n'est pas autorisé à fusionner sa propre pull request. Cela permet de garantir une validation externe par les autres membres du groupe ou par des reviewers indépendants, pour renforcer la qualité et la fiabilité des modifications apportées.

**_Annulation des approbations de pull requests lorsque de nouveaux commits sont poussés_** : La règle "Dismiss stale pull request approvals when new commits are pushed" doit être activée. Cela signifie que si des commits supplémentaires sont ajoutés à une pull request déjà approuvée, les approbations précédentes seront automatiquement révoquées. Cette règle garantit que les modifications récentes sont également examinées par les reviewers, assurant ainsi que l'évaluation de la pull request reste valide et à jour.

## Installation

```bash
# Installation des dépendances
$ npm install
```

## Configuration et Démarrage

```bash
# mode développement
$ ng serve

# mode développement avec hot reload
$ ng serve --watch

# build pour la production
$ ng build --prod
```

## Tests

```bash
# tests unitaires
$ ng test

# tests end-to-end
$ ng e2e

# lint
$ ng lint
```

## Contributeurs

- [aReynier](https://github.com/aReynier)
- [AyoubLaroussi](https://github.com/ayoub-laroussi)
- [Boris betremieux](https://github.com/BborisB)
- [Martial Floquet](https://github.com/martial59110)
- [EnguerranSGG](https://github.com/EnguerranSGG)
- [Gabriel Luthun](https://github.com/gabrielluthun)
- [Julien Beauchant](https://github.com/julienbeauchant)
- [Messa](https://github.com/MessaKami)
- [YohanF1245](https://github.com/YohanF1245)
- [Justin Didelot](https://github.com/Srekaens)
- [Abdel](https://github.com/UnknOownU)
