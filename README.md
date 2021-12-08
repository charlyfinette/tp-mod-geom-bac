# TP Modélisation géométrique avec Alexandra Bac 

## TP1: Courbures discrètes

### Exercice de Base

Pour contrôler le nombre de voisins, j'ai rajouté une condition à l'ajout du 2-ring de voisins.
```c++
    if(neigh.size() < 5)
    {
        neigh.insert(neigh.end(), neigh2.begin(), neigh2.end());
    }
```
C'est quoi un maillage "sparse" ? 

Implémentation des matrices A et B: La principale cause de mon retard c'est parce que je n'avais pas effectué le changement de base pour les éléments de la matrice B.

```c++
// B :
    B(i) = pi_e[2];  // z_i
// A :
    A(i,0) = pi_e[0] * pi_e[0]; // (x_i)**2
    A(i,1) = pi_e[0] * pi_e[1]; // (x_i)*(y_i)
    A(i,2) = pi_e[1] * pi_e[1]; // (y_i)**2
    A(i,3) =           pi_e[0]; // x_i
    A(i,4) =           pi_e[1]; // y_i
```

1. Pourquoi on peut utiliser l'approximation ?
2. Courbures pour H et K


#### Courbure gausienne sur kitten.obj
![Courbure gausienne sur kitten.obj](https://github.com/charlyfinette/tp-mod-geom-bac/blob/master/Images/KittenCourbureK..png) 

#### Courbure moyenne sur kitten.obj  
![Courbure moyenne sur kitten.obj](https://github.com/charlyfinette/tp-mod-geom-bac/blob/master/Images/KittenCourbureH..png)

### Visualisation 

## TP2: Réparation de maillage par surfaces implicites
