# Labo-TDZ-Final01
2ème partie du laboratoire évalué

Les classes fournies proviennent de la solution possible à la première partie

Acteur.cs

Ce labo comporte 1 nouvelle classe à développer

Niveau.cs

Et une classe fournie

Position2D.cs


La classe Niveau

- Elle contient les attributs pour définir la carte et la position des éléments essentiels
- Elle utilise la classe Position2D pour gérer les positions: joueur, ennemi et sorite
- Carte : un tableau 2D de string. Les murs sont des #, le joueur est un J et la sortie est un S. On n'affiche pas l'ennemi pour que ce soit une surprise!​
- PosJoueur : une instance de la classe Position2D qui contient les coordonnées du joueur​
- PosEnnemi : une instance de la classe Position2D qui contient les coordonnées de l'ennemi​
- PosSortie: une instance de la classe Position2D qui contient les coordonnées de la sortie​

Le constructeur ne reçoit aucun paramètre. Cependant, il initialise la carte du niveau avec ses murs. Ensuite, il place le joueur en haut à gauche et la sortie en bas à droite. Puis, il utilise la méthode privée PlacerEnnemi() pour déterminer la position de l'antagoniste.


La méthode PlacerEnnemi​

- Aucun paramètre​
- Générer une position aléatoire pour l'ennemi​
- L'ennemi ne peut pas être dans les murs, ni à la même position que la sortie. Il ne peut pas non plus être à la position d'entrée du joueur​
- La position générée est assignée à l'attribut PosEnnemi​
​

La méthode AfficherCarte​

- Aucun paramètre​
- Affiche la carte à la console​
- Les murs sont des #, la position du joueur est un J, la position de la sortie est un S​
- Affiche une ligne supplémentaire pour indiquer quelles touches peuvent être utilisées pour se déplacer​
- Cette méthode ne fais pas la gestion du déplacement, elle affiche la carte (le tableau 2D) à la console et c'est tout​

​
La méthode DeplacerJoueur​

- Reçoit en paramètre un string qui indique dans quelle direction déplacer le joueur​
- Elle vérifie d'abord si le déplacement est possible, on ne peut pas envoyer le joueur dans un mur ou en dehors de la carte​
- Vous pouvez utiliser des méthodes privées pour gérer chacune des directions ou tout faire dans cette méthode, à votre choix


La méthode DetruireEnnemi​

- Aucun paramètre​
- Sert après le combat, avant que le joueur n'atteigne la sortie​
- Déplace l'ennemi à la position -1, -1. De cette façon, on ne peut pas tomber sur l'ennemi de nouveau puisqu'il est en dehors de la carte​
​

La méthode estSotrie​

- Aucun paramètre​
- Retourne un booléen (true ou false)​
- Si le joueur est à la même position que la sortie, on retourne true sinon on retourne false​


La méthode estCombat​

- Aucun paramètre​
- Retourne un booléen (true ou false)​
- Si le joueur est à la même position que l'ennemi, on retourne true sinon on retourne false​