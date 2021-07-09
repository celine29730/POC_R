# POC_R

## **Objectif**

L'objectif de notre étude est de découvrir le langage R à travers un jeu de données concernant les prix de l'immobilier sur Paris.
On va utiliser R afin de créer un modèle prédictif. La visualisation des prédictions se fera par le biais d'une application réalisée gràce à la bibliothèque shiny.

Ce projet nous permettra également de comparer avec un autre langage utilisé en modélisation statistiques, Python.

## Analyse des données

Notre dataset comporte 17 variables numériques et ne possède pas de valeurs manquantes.

La variable que l'on souhaite expliquée (Target) est la variable "price" et c'est sur cette variable que nous allons réaliser notre modèle de prédiction.
On peut visualiser cette variable de prix à l'aide de l'histogramme suivant:

![histo](https://github.com/celine29730/POC_R/blob/main/images/Histogramme_evol_prix.jpg)

On va ensuite construire une matrice de corrélation afin de voir quelles sont les variables qui peuvent influencer le prix.

![corrélation](https://github.com/celine29730/POC_R/blob/main/images/Matrice_Corr%C3%A9lation.jpg)

On constate que seule la variable sqaureMeters (surface) est corrélée avec la variable price. Nous obtenons un coefficient de corrélation de 99%.
Si on observe la relation existant entre ces deux variables, nous pouvons dire qu'il s'agit d'une relation parfaitement linéaire.

![visu](https://github.com/celine29730/POC_R/blob/main/images/visu_price_squareMeters.jpg)

L'équation de notre modèle est Y = aX + b + e.

Y (Target) est la variable "price" 
X est la variable explicative "squareMeters"
e est le risque d'erreur du modèle.

Nous allons donc utiliser un modèle de régression linéaire simple pour effectuer nos prédictions de prix.

Le modèle est obtenu gràce au code suivant:

![model](https://github.com/celine29730/POC_R/blob/main/images/model.jpg)

## Visualisation des prédictions gràce à l'interface shiny

On lance l'application à l'ade du fichier app_house2bis.R

le fichier comporte un bloc **ui** pour la partie mise en forme de la page et une partie **server** pour la partie plus importante des calculs (ici le calcul des prédictions de prix).

![app1](https://github.com/celine29730/POC_R/blob/main/images/app1.jpg)

Dans le premier onglet de l'interface graphique figurent les prédictions que l'on peut faire varier en fonction du curseur de surface.
Dans le second onglet, on trouve la visualisation du dataset.

![app2](https://github.com/celine29730/POC_R/blob/main/images/app2.jpg)

il est possible d'appliquer un filtre sur le nombre d'enregistrement (show entries) et sur les valeurs du dataset (search).

# Conclusion

Si on veut établir un comparatif entre le langage R et Python, nous pouvons dire que:

* **R est plus fonctionnel, Python est plus orienté objet**
* **R a plus de fonction ‘built-in’ pour analyser des données, Python s’appuie sur des librairies.**
* **Python a des packages “principaux” pour les tâches d’analyse de données, R a un plus grand écosystème de petits packages.**
* **R est meilleur pour les statistiques de façon générale.**
* **Il est généralement plus simple de faire des tâches non statistiques en Python.**
* **Néanmoins,il existe de nombreux parallèles dans l’analyse de données des 2 langages.La syntaxe et les approches sont similaires pour de nombreuses tâches courantes dans les deux langages.









