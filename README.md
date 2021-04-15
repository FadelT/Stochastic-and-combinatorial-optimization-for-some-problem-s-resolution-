# Stochastic-and-combinatorial-optimization-for-some-problem-s-resolution-
Hello, Welcome!
Il s'agit ici de résoudre certains problèmes d'optimisation tels que le Problème du voyageur de commerce et celui de l'emploi du temps. 
La description des problèmes se trouve ici: 

Problème du voyageur de commerce: https://fr.wikipedia.org/wiki/Problème_du_voyageur_de_commerce

Problème de l'emploi du temps:
[[[[
On a K créneaux horaires, m enseignants et n classes d’élèves.

Créneaux : (Lu8,Lu10,…,Ve14,Ve16) - ici: K = 20.
Professeurs : (Dupont, Durand, Duval, …) - par ex: m = 32.
Classes : (6A,6B,…,3D) - par ex: n = 16.
Chaque classe est suivie par 6 professeurs. Chaque professeur est affecté à 3 classes et réalise 3 séances pour chaque classe. Ainsi, chaque professeur réalise un total de 9 séances par semaine, et chaque classe suit 3×6 = 18 séances de cours (à répartir sur 20 créneaux disponibles).

remarque : on vérifie 3m = 6n soit m = 2n

On suppose pour simplifier que les professeurs sont désignés par un numéro unique (de 1 à m) ainsi que les classes (classes 1 à n) et les créneaux (de 1 à K). On suppose qu’est donné au départ le tableau d’affectation (donnant les classes affectées à chaque professeur). Ainsi, pour tout i, A(i) ={A(i,1),…,A(i,6)} est la liste des 6 professeurs affectés à la classe i.

Une solution consiste à définir la semaine de chaque classe sous la forme d’une séquence de K valeurs. Pour tout i, s(i) = (s(i,1), (s(i,2), s(i,3),… ,s(i,20)) qui est une permutation de la liste (A(i,1), A(i,1), A(i,1), A(i,2), A(i,2), A(i,2), …, A(i,6), A(i,6), A(i,6), 0, 0) où les valeurs 0 correspondent aux 2 séances d’”étude”. Une solution prend donc la forme d’une matrice de n lignes et 20 colonnes.

Questions:

Combien ce problème accepte-t-il de solutions?
Comment définiriez-vous le voisin d’une solution s donnée?
En fonction de la définition précédente, combien une solution s possède-t-elle de voisins?
On appelle collision le fait qu’un même professeur apparaisse 2 fois ou plus dans le même créneau (autrement dit une collision est un triplet (i,j,k) tel que (i !=j) et (s(i,k)=s(j,k))). On cherche à proposer un emploi du temps dans lequel il n’y a pas de “collision”.]]]]

Pour les résoudre, j'ai opté pour la construction d'une classe objet dotée de certaines méthodes et attributs qui va permettre d'utiliser facilement les algorithmes d'optimisation une fois ces derniers codés. 
Les algorithmes d'optimisation en question sont: Monte carlo, Gloutton, Gloutton aléatoire, Tabou. 
Certains algorithme s'avèrent plus efficaces que d'autres mais prennent beaucoup de temps. 
