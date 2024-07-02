# Student-Schedule-Manager

Université de Montréal
Département d’informatique et de recherche opérationnelle
Devoir 1
Les étudiants doivent fournir un projet java (code source + documentation en javadoc), dont le sujet est présenté dans la suite du document.

I. Informations générales :
  Session

Date de début Date de remise

Été 2024
25/06/2024
14/07/2024 avant minuit
    

Directives

• Il y aura une pénalité de 10% par jour de retard (maximum 3 jours de retard).
• Les contestations des notes seront acceptées pendant les deux semaines suivantes l’affichage de celles-là sur le StudiUM
II. Objectifs du devoir :

Valider les compétences de la première partie du cours par l’écriture d’un programme en manipulant les différentes notions vues en cours et en travaux pratiques.

III. Organisation :

Le travail doit se faire en binôme.

IV. Ce qu'il faut rendre :

1. Le code source complet bien commenté (le projet au complet).
2. Un rapport présentant le travail effectué (en .pdf au maximum 3
pages).

V.

a) Dégager toutes les classes.
b) Dégager les constructeurs nécessaires dans chaque classe.
c) Dégager les membres de chaque classe.
d) Expliquer le mode d’emploi du programme.
e) Bilan qualitatif du travail, difficultés rencontrées, critiques et
suggestions.
Évaluation du projet : 
❖ Les critères d’évaluation sont :
1. Le programme source :
• Respect de l’énoncé – 5%
2. Qualité de conception/technique :
• Définitions appropriées des classes (variables de l’instance, méthodes, constructeurs), encapsulation des données ; découpage en fonctions, instructions, algorithmes, efficacité – 30%
• Code compilable et exécutable, fonction main avec les tests – 35%
3. Présentation du programme :
Indentation, commentaires (JavaDoc) et nommage (conventions d’identificateur) – 10%
4. Documentation fournie (rapport) – 20% :
a. Organisation du programme et son mode d’emploi. b. Bilan.
Présentation du devoir :

VI.

Vous devrez réaliser un programme permettant de gérer un horaire d’étudiant.

VII. Description du devoir :
Le modèle à mettre contiendra les classes, dont les champs contiennent au minimum les informations suivantes.

Cours: numéro, matière (par exemple IFT pour les cours d’informatique), horaire d’un cours (les dates des cours théoriques, pratiques, les dates et l’horaire des examens, etc.), nombre de crédits. Votre programme devra proposer un menu comme celui-ci :
1. Gestion des cours.
2. Ajouter, modifier ou supprimer un ensemble des cours candidats
(maximum 10 cours) pour un horaire d’étudiant.
On demande de permettre à l'usager de modifier la liste des cours disponibles, pas nécessairement ceux auxquels l'étudiant est inscrit. Imaginez que votre programme est utilisé par la TGDE, qui doit créer la liste des cours qui sont disponibles à l'inscription. L'usager de votre programme créera donc des cours, puis inscrira l'étudiant à ces cours. Il n'est pas demandé que votre programme travaille avec un répertoire de cours prédéfinis.
a) Créer un horaire personnalisé en prenant en considération les conflits des cours (l’horaire superposé, les dates d’examens superposées ou trop proches, etc.). Les deux conditions pour faire le choix des cours sont :
• Le nombre de crédits spécifié pour la session
• Minimum de conflits d’horaire entre les différents cours
choisis
3. Afficher l’horaire créé ou les messages des conflits, si on n’arrive
pas satisfaire des contraintes.
4. Utiliser dans votre design les classes de l’API Java, c'est-à-dire les
classes fournies par la librairie standard (ArrayList, Calendar, Date, LocalTime, etc.). Je vous suggère de mettre cette page de documentation dans vos favoris, elle vous sera souvent utile: https://docs.oracle.com/en/java/javase/20/docs/api/java.base/ module-summary.html

Référez-vous-y lorsque vous voulez regarder comment utiliser une certaine classe ; toutes les méthodes y sont très bien documentées. Utilisez la barre de recherche en haut à droite. Évitez de recréer des fonctionnalités déjà offertes par l'API de Java. Par exemple : si vous avez besoin d'une liste chaînée, plutôt que de créer vous- mêmes une classe contenant une liste, puis une classe représentant un nœud, utilisez plutôt la classe LinkedList déjà offerte. Pour représenter une date, au lieu de créer vous-mêmes une classe contenant les informations d'une date (jour, mois, année), vous pouvez utiliser Calendar, ou bien les classes du package java.time telles que LocalTime et LocalDate. (Il y a aussi un type enum pour les jours de la semaine, si vous vous sentez à l'aise avec les énumérations).
5. Pour valider les entrées et gérer les erreurs, utilisez les exceptions.
6. Utilisez les structures de données (bibliothèques Java) appropriées favorisantes les traitements demandés pour stocker les données.
L'énoncé de ce TP est écrit de façon très générale, et c'est voulu. Vous avez la liberté de décider (dans la limite du raisonnable) du fonctionnement de votre programme quant à ce qui n'est pas mentionné explicitement dans l'énoncé. Par exemple, comment afficher l'horaire : sous forme d'une liste ou sous forme tabulaire ? C'est votre choix. Comment stocker l'horaire en mémoire ? Réponse : c'est vous qui devez décider comment vous concevez le design à cet effet. Voici quelques idées, libre à vous de les adapter à votre convenance :

• Pour chaque cours, une date de début, une date de fin, et une liste de séances par semaine (avec le jour de la semaine, les heures, etc.).
• Une liste complète des séances du cours (heure de début et de fin)
• Un tableau à deux dimensions de booléens, où les lignes représentent les jours de la semaine, et les colonnes représentent les heures de la journée (donc un tableau 7 × 24). (Cette idée offre cependant l'inconvénient de n'autoriser que des séances à des heures spécifiques, comme 13h ou 18h, mais pas 18h30 ou 13h15. Mais c'est un choix possible.)
7. Dans le rapport, il devrait y avoir des détails sur les choix que vous avez faits vous-mêmes et qui n'étaient pas explicités dans l'énoncé. Par exemple, des choses pertinentes sur lesquelles écrire seraient :
oLa façon précise dont vous avez choisi d'offrir les fonctionnalités demandées, par exemple quelles informations l'utilisateur peut-il fournir en ce qui concerne un cours ? Comment entre-t-il un horaire (les dates individuelles des séances ? les jours de la semaine et les heures ? etc.)
o Les raisons pour lesquelles vous avez organisé les classes de la façon dont vous l'avez fait. Par exemple, si vous aviez une idée au départ, mais que vous vous êtes rendu compte que ça ne fonctionnait pas et que vous avez réorganisé vos classes d'une autre façon, ce serait une bonne chose à mentionner.
o Tout ce qui est demandé à la section IV.2 de l'énoncé.
