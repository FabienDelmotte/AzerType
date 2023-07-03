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
