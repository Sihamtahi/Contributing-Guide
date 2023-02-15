# Clean Code

Voici un résumé des principales idées du livre « [Clean Code: A Handbook of Agile Software Craftsmanship](https://www.decitre.fr/livres/clean-code-9780132350884.html) » de Robert C. Martin (Uncle Bob). La plupart des sites / organisation reprennent ces principes de la même façon exposé dans ce document.

On parle d'un code propre (clean) s'il s'agit d'un code qui peut être compris facilement - par chaque personne de l'équipe. Un code propre (Clean code) peut être lu et amélioré par un·e développeur·se autre que la personne qui l'a écrit. Avec la compréhensibilité vient la lisibilité, la facilité à changer, l'extensibilité et la maintenabilité.

---

## Règles générales

1. Suivre les règles connu.
2. Keep it simple stupid. Plus simple est toujours mieux. Réduire autant que possibe.
3. Règle"Boy scout". Laissez le camping plus propre que vous ne l'avez trouvé.
4. Chercher et trouver la cause racine lors de résolution d'un problème.
5. DRY (Don't repeat yoursel) : Ne vous répétez pas

## Règles de design

1. Gardez les données configurables (par exemple les constantes) à hauts niveaux. Elles devraient être faciles à changer.
2. Préférez le polymorphisme aux if/else ou switch/case.
3. Separate multi-threading code.
4. Évitez la sur-configurabilité.
5. Utilisez [dependency injection](https://fr.wikipedia.org/wiki/Injection_de_d%C3%A9pendances) (l'injection de dépendances) :
6. Suivez la loi de [Déméter] ( Principe de connaissance minimale) : une classe ne devrait connaître que ses dépendances directes.

## Tips pour la compréhensibilité

1. Soyez cohérent. Si vous faites quelque chose d'une certaines manière, toutes les choses similaires devraient être faites de la même manière.
2. Utilisez des noms de variables explicites.
3. Encapsulez les conditions limites : elles sont compliquées à suivre. Il vaut mieux les isoler à un endroit.
4. Préférez des value objects spécifiques plutôt que des types primitifs : un pricipe utilisé dans le DDD (Domain Driven Design).
5. Évitez les dépendances logiques : n'écrivez pas de méthodes qui dépendent d'autre chose dans la même classe.
6. Évitez les conditions négatives.

## Règles de nommages

1. Choisissez des noms descriptifs et sans ambiguïté..
2. Faites des distinctions qui ont du sens.
3. Utilisez des noms prononçables.
4. Utilisez des noms qu'on peut chercher.
5. Remplacez les nombres magiques par des constantes bien nommées..
6. Évitez d'ajouter des préfixes ou des informations sur les types.

## Règles relatives aux fonctions

1. Courtes.
2. Ne fait qu'une chose et la fait bien.
3. Utilisez des noms descriptifs.
4. Préférez les avec le moins d'arguments possibles, idéalement pas plus de 3.
5. Sans effets de bord.

## Règles relatives aux commentaires

1. Essayez d'écrire du code expressif ne nécessitant pas de commentaire. Si c'est impossible, prenez le temps d'écrire un bon commentaire.
2. Ne soyez pas redondant (par exemple : i++; // increment i).
3. N'ajoutez pas de bruit évident.
4. N'utilisez pas les commentaires de fermeture de bloc (par exemple : } // end of function).
<!-- 5. Don't comment out code. Just remove. -->
5. Utilisez des commentaires pour expliquer l'intention.
6. Utilisez des commentaires pour avertir des conséquences.

## Structure du code source

1. Séparez les concepts verticalement.
2. Le code lié devrait apparaître dense verticalement.
3. Déclarez les variables à proximité de leurs usages.
4. Les fonctions dépendantes les unes des autres devraient être à proximité.
5. Les fonctions similaires devraient être à proximité les unes des autres.
6. Placez les fonctions dans la direction descendante.
7. Gardez les lignes courtes.
8. N'alignez rien horizontalement.
9. Utilisez des espaces pour associer des choses liées et dissocier des choses liées faiblement.
10. Ne cassez pas l'indentation.

## Les Objects et la structure des données

1. Cachez les structures internes.
   2Devraient être petits.
2. Devraient être petits.
3. Ne font qu'une chose.
4. Possèdent un petit nombre de variables d'instance. Si votre classe a trop de variables d'instance, il est probable.
5. que votre objet fasse plus qu'une chose.
6. Une classe de base ne devrait rien connaître de ses classes dérivées.
7. Il vaut mieux avoir plusieurs fonctions que de passer du code à une fonction pour qu'elle choisisse un 8. comportement.
   9.Préférez des méthodes non statiques

## Tests

1. Un concept par test.
2. Rapides.
3. Indépendants.
4. Répétables.
5. Auto validants.
6. Utiles.
7. Lisibles.
8. Faciles à lancer.
9. Utilisez un outil de génération de couverture de code.
