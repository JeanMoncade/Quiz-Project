# Quiz

## Elaboration d'un quiz sur python

J'ai réalisé un quiz simplifié pour m'entrainer sur les boucles python.

Pour commencer ce quiz, l'utilisateur doit au préalable insérer un mot de passe pour activer le quiz :

```
mdp = input("quel est le mot de passe ?")

while mdp != "jedha":
    print("Ceci n'est pas le mot de passe")
    mdp = input("quel est le mot de passe")
    break
```

Grâce à cette boucle le code va demander le mot de passe pour lancer le quiz.
Si le bon mot de passe, jedha, est rendu en réponse alors l'utilisateur pourra accéder au quiz.

De plus, on souhaite donner 3 chances au joueur du quiz.

Pour cela on va donc définir la variable nb_de_chances pour ensuite l'insérer dans nos boucles et ainsi limiter
le nombre de chance totale à 3 sur l'ensemble des questions.

'''
nb_de_chances = 3
print("Voici notre quiz, tu as trois chances !")
'''

Puis on ajoute ensuite nos questions grâce à des boucles python.

Lorsque l'utilisateur se trompe sur la réponse d'une question alors le code vérifie si le joueur a encore des chances.

Si l'utilisateur n'a plus de chances alors il a perdu le jeu, si il a encore des chances et qu'il fait une erreur
alors on va lui supprimer une chance et relancer la boucle :

'''
Question1= input("Combien de fois la France a gagné la coupe du monde ?")
while Question1 != "2":
    if nb_de_chances == 0:
        print("Oh non ! Tu as perdu le jeu...")
        break
    else: nb_de_chances -=1
    print("Dommage ! Il te reste {} chance".format(nb_de_chances))
    question1 = input("Combien de fois la France a gagné la coupe du monde ?")
'''

Les questions s'enchainent à la suite de la même façon. Avant chaque question on vérifie qu'il reste des chances au joueur :

'''
if nb_de_chances != 0 :
'''

Enfin, on finalise le quiz à la fin de la boucle de la question 3 en imprimant un message de félicitation pour les gagnants :

'''
if question3 == "elon musk":
    print("Bravo ! Tu as gagné le quiz !")
'''
