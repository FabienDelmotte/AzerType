# AzerType

## Écrivez votre premier fichier JavaScript

### Appréhendez la logique de programmation

Créer un fichier index.html et un fichier script.js.

### Contrôlez du code grâce aux conditions

#### Étape 1 : Tester le premier mot

Déclarer une variable listeMots qui est un tableau.
Ce tableau contient trois mots que l’utilisateur devra taper au clavier : “Cachalot”, “Pétunia” et “Serviette”.
Déclarer une deuxième variable score, initialisée à 0, qui contiendra le nombre de mots correctement tapés par l’utilisateur.
À l’aide de l’instruction prompt, demander à l’utilisateur de rentrer le mot contenu dans la première case du tableau.
Écrire une première structure conditionnelle pour savoir si le mot tapé par l’utilisateur est bien celui demandé par l’application.
Si c’est le cas, on augmente la valeur de score de 1.
Vérifier avec des console.log si le score final est correct.

#### Étape 2 : Tester le second mot

Demander à l’utilisateur de rentrer le second mot.
Faire une seconde structure conditionnelle pour vérifier si le second mot tapé par l’utilisateur correspond bien au second mot du tableau.

#### Étape 3 : Tester le troisième mot

Recommencer une troisième fois pour la dernière case du tableau !

### Répétez du code grâce aux boucles

#### Étape 1 : répéter le code avec une boucle

Le tableau listeMots contient 3 mots : “Cachalot”, “Pétunia” et “Serviette”. Pour chacun de ces mots, à l’aide d’une boucle for :

- demander à l’utilisateur de le retaper avec prompt ;
- compter un point par mot correctement tapé ;
- afficher le score à la fin avec un console.log.

#### Étape 2 : proposer deux types de listes de mots

Pour rendre le jeu plus engageant, nous voulons que l’utilisateur puisse avoir le choix entre deux listes de mots différentes : une liste avec des mots et une liste avec des phrases.

- Déclarer un tableau listePhrases qui contient 3 courtes phrases : “Pas de panique !”, “La vie, l’univers et le reste”, “Merci pour le poisson”.
- Demander à l’utilisateur s’il veut la liste de mots ou la liste de phrases. Répéter la question tant que l’utilisateur n’a pas écrit “mots” ou “phrases”.
- Lancer la boucle for, avec la liste que l’utilisateur a choisie.

### Organisez votre code grâce aux fonctions

#### Étape 1 : découper le code en fonctions

Créer les fonctions suivantes :

- afficherResultat : cette fonction prend en paramètre le résultat et le nombre total de mots proposés, et affiche le résultat du joueur ;
- choisirPhrasesOuMots : cette fonction demande à l’utilisateur s’il veut jouer avec des phrases ou des mots ;
- lancerBoucleDeJeu : cette fonction contient la boucle principale de jeu, c'est-à-dire la boucle for qui propose les mots/phrases au joueur, et lui demande de taper ces mots ; Elle prend en paramètre le tableau de mots/phrases qui sera proposé au joueur, et retourne le nombre de mots/phrases correctement tapés ;
- lancerJeu : cette fonction sera la fonction principale, c’est elle qui s’occupe de lancer toutes les autres ; En d’autres termes, c’est elle qui va appeler les fonctions qui viennent d'être écrites.

#### Étape 2 : séparez votre code en plusieurs fichiers

- Séparer le code en plusieurs fichiers.
- Créer un fichier config.js qui contiendra uniquement les deux listes de propositions.
- Créer un fichier main.js qui contiendra uniquement l’appel à la fonction principale lancerJeu.
- Vérifier que tout fonctionne encore.
- Créer un nouveau répertoire appelé “scripts”, et y placer tous les fichiers.
- Vérifier à nouveau le code.

## Faites interagir JavaScript avec une page web

### Récupérez un élément d’une page web

Dans le fichier main.js :

- Sélectionner avec la méthode getElementById :
  - l’input dans lequel le joueur va écrire son texte ;
  - le bouton de validation.
- Sélectionner avec la méthode querySelector :
  - l’endroit où le mot proposé sera affiché ;
  - l’endroit où le score sera affiché.
- Sélectionner avec la méthode querySelectorAll :
  - les boutons radio de choix.

### Créez un nouvel élément dans une page web

Modifier la fonction afficherResultat. Cette fonction ne devra plus afficher le résultat en console, mais directement sur la page HTML sous la forme “score / nbMotsProposes”.

### Interagissez avec un élément d’une page web grâce aux événements

#### Étape 1 : nettoyer le projet

Supprimer les éléments qui seront modifiés dans notre projet :

- mettre en commentaire toutes les méthodes qui utilisent prompt ;
- mettre à jour la fonction lancerJeu pour qu’elle ne fasse plus appel à ces fonctions.

Désactiver temporairement le choix entre la liste des phrases et la liste des mots, de manière à utiliser systématiquement la liste des mots :

- mettre à jour la fonction lancerJeu, et commenter ce qui concerne la variable listePhrases.

#### Étape 2 : gérer le clic sur le bouton “Valider”

À ce stade, le projet n’est plus fonctionnel, il n’est plus possible de jouer. Il faut donc reconstruire ce qui a été commenté à la première étape, en interagissant directement avec la page HTML.
La première étape est de pouvoir réagir au clic sur le bouton “Envoyer” :

- Dans la fonction lancerJeu, récupérer le bouton de validation et écouter l’événement click en utilisant la méthode addEventListener.
- Tester que cela fonctionne avec un console.log(“j’ai cliqué !”).
- Récupérer la balise inputEcriture et la placer dans une variable.
- Dans l’addEventListener, faire un console.log avec la valeur contenue dans cette balise.

Pour accéder à la valeur contenue dans la balise inputEcriture, utiliser la propriété value.

- Tester en écrivant quelque chose dans le champ, et en vérifiant que la valeur apparaît bien lorsqu'on clique sur Envoyer.

#### Étape 3 : afficher les mots que l’utilisateur doit recopier

À ce stade, on sait comment récupérer le mot que l’utilisateur a écrit, mais on n’affiche pas encore le mot qu’il devra recopier. Pour réaliser cette mise à jour du code HTML :

- à l’extérieur du addEventListener, créer une variable i qui servira de compteur. Dans l’addEventListener, ajouter 1 à i à chaque fois que l’utilisateur clique sur le bouton Envoyer ;
- ajouter un console.log qui va afficher le mot numéro i du tableau listeMots ;
- créer une fonction afficherProposition, qui va prendre en paramètre le mot à afficher, et afficher ce mot dans la div zoneProposition ;
- utiliser cette fonction pour afficher les mots à proposer.

Après ces opérations, on doit voir apparaître les mots un par un après avoir réalisé ces opérations. Cependant, on remarquera peut-être que le mot “undefined” s’affiche lorsqu’il n’y a plus de mots disponibles dans le tableau. Pour régler ce problème :

- ajouter un test dans l’addEventListener. Si le mot numéro i du tableau vaut undefined, écrire le message “Le jeu est fini” à la place du mot, et désactiver le bouton de validation. Pour désactiver ce bouton, mettre la propriété disabled de ce bouton à true ;
- à chaque fois que l’utilisateur clique sur Valider, vider le champ inputEcriture.

#### Étape 4 : gérer le score

Il nous reste une dernière étape : gérer le score de l’utilisateur.

- Dans l’addEventListener, comparer ce qu’a écrit l’utilisateur et le mot proposé. Si ces deux mots sont identiques, augmenter le score.
- Dans tous les cas, mettre à jour le score en appelant la fonction de mise à jour du score avec les bons paramètres.

## Créez un formulaire de saisie de données

### Récupérez la valeur d’un champ de formulaire

- Écouter l’événement “change” sur les boutons radio.
- Lorsque cet événement se déclenche, modifier le texte proposé pour le remplacer par une phrase si l’utilisateur a cliqué sur “Phrases”, ou un mot si l’utilisateur a cliqué sur “Mots”. Pour cela :
  - déclarer une nouvelle variable listeProposition initialisée par défaut à listeMots ;
  - utiliser cette nouvelle variable pour le traitement à la place de listeMots ;
  - lorsque le joueur clique sur Phrases, modifier la valeur de listeProposition pour qu’elle corresponde au tableau des phrases. Quand le joueur clique sur Mots, faire de même ;
  - mettre à jour l’affichage.

### Soumettez votre formulaire

Il faut :

- écouter l’événement submit sur ce nouveau formulaire, et empêcher le comportement par défaut de se produire ;
- récupérer les valeurs des champs présents ;
- créer une variable sujet et une variable message, et les afficher dans la console ;
- utiliser la méthode afficherEmail préparée, avec les bons arguments pour afficher l’e-mail à envoyer, prérempli avec les bonnes informations.

### Mettez en place des règles de validation

Il faut :

- Écrire une fonction validerNom qui va prendre le nom à tester en paramètre et retourner true si le nom est valide, false sinon.
  - La fonction doit prendre le nom en paramètre et valider qu’il est correct.
  - La règle est d’avoir un champ avec au moins deux caractères.
- Écrire une fonction validerEmail qui va prendre en paramètre l’e-mail à tester et retourner true si l’e-mail est valide, false sinon.
- Utiliser ces deux fonctions avec l’événement submit du formulaire.
- Si les deux champs sont valides, afficher l’e-mail. Sinon, afficher seulement un message d’erreur dans la console.
