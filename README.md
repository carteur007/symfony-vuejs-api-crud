# Projet de gestion des opérations crud avec Symfony,Vuejs,QuoraJs

> Vous pouvez outre-passer ces étapes et cloner le repository directement avec l'une des commandes suivantes:
> HTTPS `https://github.com/carteur007/symfony-vuejs-api-crud.git`
> SSH `git@github.com:carteur007/symfony-vuejs-api-crud.git`
> GitHub CLI `gh repo clone carteur007/symfony-vuejs-api-crud`

## Mise en place du projet

1. Créer le repository git
2. Créer le projet symfony avec l'une des commandes commandes suivante:
   2.1. Commande `symfony`

```sh
symfony new symfony-vuejs-api-crud
```

    2.2. Commande `composer`

```sh
composer create-project symfony/skeleton symfony-vuejs-api-crud  --no-interaction
```

> Ajouter le fifchier README.md

```sh
cd symfony-vuejs-api-crud
touch README.md
git commit -am "Initialisation de la structure du projet symfony"
```

## Liaison du projet au repository github

```sh
git remote add origin https://github.com/carteur007/symfony-vuejs-api-crud.git
git branch -M master
git push -u origin master
```

## Installation des outils

1. Outils de developpement
   1.1. Packet permettant de gerer le débogage

```sh
cd symfony-vuejs-api-crud
composer req --dev debug
```

2. Outils gestion de la base de donnée à partir de `PHP`
   2.1. Installation de `ORM`,`twig` et `maker-bundle`

    > Nous utilisation `sqlite3`

```sh
composer req symfony/orm-pack
composer req --dev symfony/maker-bundle
#Modifier le fichier .env et decommenter la ligne suivante
DATABASE_URL="sqlite:///%kernel.project_dir%/var/app.db"
```

3. Outils gestion des templates
   3.1. Template `Twig`

```sh
composer req twig/twig
composer req twig/extra-bundle
composer req symfony/twig-bundle
# Ou simplement
composer req twig
```

    3.2. Template `HTML` et `CSS`
