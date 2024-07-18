# Lab Mise en Pratique des Notions sur les Assertions dans Dataform
L'objectif principal de ce laboratoire pratique est de mettre en application les concepts appris sur les assertions en les utilisant pour créer et vérifier des règles de qualité et d'intégrité des données au sein de nos tables dimensionnelles. Ces assertions joueront un rôle crucial dans la détection précoce des erreurs et des incohérences potentielles tout au long du pipeline de transformation des données.

## Objectif du Lab
Ce lab vise à :

1. **Garantir la Qualité des Données** : En définissant des assertions, nous nous assurerons que les données respectent des règles spécifiques définies, telles que l'existence des IDs, la validité des relations entre les tables, et la cohérence des valeurs.

2. **Assurer l'Intégrité des Données** : Les assertions serviront à vérifier que les données sont complètes, correctes et conformes aux attentes, ce qui est essentiel pour maintenir la fiabilité de nos analyses et rapports.

## Contexte
Dans le cadre de notre plateforme de données, où plusieurs systèmes alimentent et modifient les données en continu, il est essentiel d'implémenter des contrôles robustes pour éviter les erreurs. Par exemple, nous devons nous assurer que :

* Les IDs ne sont jamais nuls, car ils sont essentiels pour l'identification et la relation entre les données.
* Les IDs des produits mentionnés dans la table des transactions doivent correspondre à des IDs valides dans la table des produits, assurant ainsi l'intégrité des relations.
* La quantité des produits dans les transactions doit toujours être supérieure à zéro pour garantir des données cohérentes et valides.
* Les IDs des clients et des produits doivent être uniques pour éviter toute ambiguïté ou doublon dans les données.
## Contraintes
Implémenter les contraintes suivantes :
* Les IDs ne doivent pas être null.
* Les IDs des produits dans la table `transactions` doivent exister dans la table `products`.
* La quantité des produits dans la table `transactions` doit être > 0.
* Les IDs des tables doivent être uniques.
* les Ids des customers et products dans la table `stg_transactions` doivent exister dans les tables `stg_customers`et `stg_products`
* les méthodes de payments dans la table `stg_transactions` doit être l'une des ses valeurs : Credit card ou cash
* le status des commandes dans la table `stg_transactions` doit être l'une des ses valeurs : completed, pending ou canceled,

## Dependences
* rendre les tables `dim` et `fct`dependante de la assertions des tables sources
