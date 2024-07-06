# Lab Mise en Pratique des Notions sur les Assertions dans Dataform

## Objectif du Lab
Ce lab a pour objectif de mettre en pratique les notions apprises sur les assertions en créant et en vérifiant des assertions sur des tables dimensionnelles afin de garantir la qualité et l'intégrité des données.

## Contexte
Afin de garantir la qualité et l'intégrité des données tout au long du pipeline de transformation et pour détecter les erreurs de manière précoce, nous allons définir des assertions sur les tables utilisées dans notre plateforme de données.

## Contraintes
Implémenter les contraintes suivantes :
* Les IDs ne doivent pas être null.
* Les IDs des produits dans la table `transactions` doivent exister dans la table `products`.
* La quantité des produits dans la table `transactions` doit être > 0.
* Les IDs de customer et de produit doivent être uniques.

## Dependences
* rendre les tables `dim` et `fct`dependante de la assertions des tables sources