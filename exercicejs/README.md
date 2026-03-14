# TD n°1 — Introduction à JavaScript
**École Normale Supérieure de l'Enseignement Technique de Mohammedia**  
**Master SDIA — Technologies du Web & Web Sémantique**

---

## Objectifs

Ce TD a pour but d'expérimenter les constructions de base du langage JavaScript :
- Types simples et déclarations de variables
- Instructions de contrôle (`if / else`)
- Itérations (`while`, `for`)

La syntaxe utilisée est très proche de celle du langage C.

---

## Exercices

### Exercice 1 — Conversion de températures (`ex1.html`)
**Fonction :** `degreC()`

Convertit une température en degrés Fahrenheit vers des degrés Celsius à l'aide de la formule :

```
tempC = (5 / 9) × (tempF − 32)
```

**Exemple :**
```
Une température en Fahrenheit : 60.0
→ Cette température équivaut à 15.6 degrés Celsius
```

---

### Exercice 2 — Conversion de durées (`ex2.html`)
**Fonction :** `hjms()`

Prend un nombre de secondes et le convertit en jours, heures, minutes et secondes.

**Exemple :**
```
Une durée en secondes : 235789
→ Cette durée équivaut à 2 jours 17 heures 29 minutes 49 secondes
```

**Exercice 2-bis (amélioration incluse) :**
- Les unités nulles ne sont pas affichées.
- Les unités égales à 1 sont affichées au singulier (sans "s").

```
Une durée en secondes : 3621
→ Cette durée équivaut à 1 heure 21 secondes
```

---

### Exercice 3 — Classer 3 nombres (`ex3.html`)
**Fonction :** `troisNombres()`

Demande 3 nombres à l'utilisateur et les affiche dans l'ordre croissant, en utilisant des échanges conditionnels (méthode des comparaisons successives).

**Exemple :**
```
1er nombre : 14
2ème nombre : 10
3ème nombre : 17
→ Les nombres dans l'ordre croissant : 10 14 17
```

---

### Exercice 4 — Motif en escalier (`ex4.html`)
Affiche un triangle rectangle d'astérisques dont la taille est choisie par l'utilisateur.

**Exemple (taille = 6) :**
```
*
**
***
****
*****
******
```

Deux versions implémentées :
- **`triangle1()`** — avec des boucles `while` uniquement
- **`triangle2()`** — avec des boucles `for` uniquement (voir `ex5.html`)

---

### Exercice 4-bis — Motif en pyramide (`ex5.html`)
Affiche une pyramide centrée d'astérisques.

**Exemple (taille = 7) :**
```
      *
     ***
    *****
   *******
  *********
 ***********
*************
```

---

### Exercice 5 — Nombre premier (`ex6.html`)
Teste si un entier positif saisi par l'utilisateur est un nombre premier. Si non, affiche le premier diviseur trouvé.

**Exemples :**
```
Un entier positif : 7
→ 7 est un nombre premier

Un entier positif : 25
→ 25 n'est pas un nombre premier, il est divisible par 5
```

---

### Exercice 6 — Suite de Fibonacci (`ex7.html` & `ex8.html`)
La suite de Fibonacci est définie par :
```
u₀ = 0,  u₁ = 1,  uₙ₊₁ = uₙ + uₙ₋₁
```

**a) `Fibo1` (`ex7.html`)** — Calcule le n-ième terme de la suite pour un rang `n` donné par l'utilisateur.

```
Entrez n : 10
→ Le terme de rang 10 est : 55
```

**b) `Fibo2` (`ex8.html`)** — Trouve le premier terme de la suite qui dépasse une valeur seuil donnée, et indique son rang.

```
Entrez une valeur limite : 100
→ Le premier terme supérieur à 100 est 144 (il est au rang 12)
```

---

### Exercice 7 — Racine carrée par la méthode de Héron (`ex9.html`)
**Fonction :** `Raca1()`

Calcule une valeur approchée de √A pour un réel A ∈ [1, 100] en utilisant la suite de Héron (méthode babylonienne) :

```
u₀ = A / 2
uₙ₊₁ = ½ × (uₙ + A / uₙ)
```

L'itération s'arrête dès que `|uₙ² − A| < 10⁻⁵`.

**Exemple :**
```
Pour un nombre A entre 1 et 100 : 19.23
→ Valeur approchée de la racine carrée = 4.385202389856321
```

---

## Structure des fichiers

| Fichier    | Exercice                            |
|------------|-------------------------------------|
| `ex1.html` | Conversion Fahrenheit → Celsius     |
| `ex2.html` | Conversion secondes → j/h/min/s     |
| `ex3.html` | Tri de 3 nombres                    |
| `ex4.html` | Triangle d'astérisques (`while`)    |
| `ex5.html` | Pyramide d'astérisques (`for`)      |
| `ex6.html` | Test de nombre premier              |
| `ex7.html` | Fibonacci — n-ième terme            |
| `ex8.html` | Fibonacci — premier terme > limite  |
| `ex9.html` | Racine carrée (méthode de Héron)    |

---

## Utilisation

Chaque fichier est autonome. Il suffit de l'ouvrir dans un navigateur web :

```bash
# Exemple
open ex1.html
```

Aucune dépendance externe ni serveur requis. Les interactions se font via `prompt()` et `alert()`.

---

## Concepts JavaScript couverts

| Concept | Exercices |
|---|---|
| Fonctions & appels | ex1 |
| Arithmétique & conversion de types | ex1, ex2 |
| Conditions `if / else` | ex2, ex3, ex6, ex7 |
| Boucles `while` | ex4, ex8, ex9 |
| Boucles `for` | ex5, ex6, ex7 |
| Boucles imbriquées | ex4, ex5 |
| Construction de chaînes | ex2, ex4, ex5 |
| Algorithmes itératifs | ex8, ex9 |
| Suite de Fibonacci | ex7, ex8 |