# les bases de la programmation

[le cours en PDF](pdf/bases_programmation.pdf)

## les langages

### les différentes familles
### quelques langages
## Les bases du langage Python
### Les variables
#### Usage
Une variable sert à représenter une valeur par un nom. Quelques différences avec la notion de variable en mathématiques :
> - En informatique, une variable est toujours connue, car elle est associée à une case mémoire qui contient sa valeur. Le concept d'inconnue n'existe pas.
> - En informatique, une variable évolue, sa valeur change au cours du temps suivant les actions effectuées durant l'exécution du programme. 
> - Lorsque l'on modifie une variable : la nouvelle valeur écrase la précédente et l'ancienne valeur est oubliée.
#### Nommage
Une des consignes les plus importantes de la vie d'un développeur : ==le choix du nom d'une variable==. Les mathématiciens ou les physiciens ont pour usage de choisir des noms d'inconnus les plus courts possible. Ainsi on peut voir des x, y, $\alpha$, $\Sigma$ ...

On a, bien souvent, des lettres associés à un concept : par usage R désigne une résistance, I une intensité, x une abscisse... Les exercices les plus compliqués ne nécessitent que quelques inconnues

Dans le monde informatique il en est autrement : une petite application fait dans les 1000 à 10 000 lignes de code, une application moyenne 100 000 lignes, la priorité devient tout autre : ==lisibilité et organisation==.

Prenons ces 2 lignes de code, écrites avec des instructions identiques, mais dans 2 styles complétement différents :
```python
p = a * (1 + t)
```
ou
```pyhton
prix_TTC = prix_HT * (1 + tva)
```
Vous serez sûrement tenté par le 1er choix par facilité ou habitude. 
Les raisons du débutant semblent légitimes :

- Programme court : une dizaine de lignes
- Echelle de temps de conception courte : une heure, un jour, max une semaine
- Conception solitaire : peu de travail en équipe
  
Malheureusement ces raisons ne tiennent pas dans le cadre d'un véritable projet informatique, et c'est là que commence les problèmes, il est donc essentiel de faire bien tout de suite. Prendre l'habitude de nommer correctement et explicitement ces variables est essentiel.

Le dernier argument du débutant, celui de la perte de temps, ne tient pas non plus, les éditeurs modernes proposent tous la saisie prédictive (je rentre une 1ère fois, puis l'éditeur propose après saisie des premières lettres)

!!! conclu "Le choix d’un nom de variable doit obéir à plusieurs règles"

> - le nom doit être significatif
> - Le nom est une suite de caractères accolés **sans espace**.
> - les caractères à utiliser sont :
>        - les lettres **non accentuées**
>        - les chiffres
>        - le caractère _ (underscore)
>- le premier caractère ne peut pas être un chiffre, ni une majuscule
>- le nom ne peut pas être un mot clé du langage (ou le nom d’une fonction)
>- quand on utilise plusieurs mots, on peut les séparer par le signe _ ou mettre une majuscule indiquant le début du 2nd mot, voire du 3ème, du... Ex : ma_variable ou maVariable

#### Affecter une variable

c’est lui attribuer une valeur. Le contenu précédent, s’il y en avait un, est effacé. L’affectation d’une variable permet de remplir l’emplacement mémoire.  Sans affectation, cet emplacement reste vide.

|Algorithmique|Python|Signification|
|--|--|--|
|x <- 5|x = 5|<ul><li>On crée la variable x si elle n’existait pas et on lui affecte la valeur 5.</li><li>x est alors une variable de type entier</li></ul>|
|mot <- "Hello"| mot = "Hello"|<ul><li>la variable mot contient la valeur "Hello".</li><li>Le mot est alors une variable de type chaîne de caractères (str)</li></ul>|
|<ul><li>c <- 3,2</li><li> c <- c + 5,4</li></ul>|<ul><li>c = 3.2</li><li> c = c + 5.4</li></ul>|<ul><li>La première instruction : la variable c reçoit la valeur 3,2.</li><li> La deuxième instruction entraîne le calcul du contenu de c additionné à 5,4 dont le résultat est 8,6.</li><li> Ce nouveau nombre est alors affecté à c. Si on utilise à nouveau la variable c, elle contient 8.6.</li><li> c est une variable de type flottant (float)</li></ul>|

!!! conclu "L'affectation"
> - **une valeur** : comme le nombre 12 ou la chaîne de caractères "Bonjour"
> - **une autre variable** : on va lire la valeur à laquelle cette variable est associée
> - **une expression** : une succession de calculs fournissant un résultat, les calculs peuvent intégrer la variable elle-même. Ex : a = a + 3

!!! warning "Remarque"
> A tort ou à raison, le symbole = a été choisi pour représenter l'affectation. Mais il est inadéquat, car en mathématiques on peut écrire aussi bien a = b que b = a. Dans l'ensemble des langages informatiques, le symbole = se lit de droite à gauche. On évalue d'abord l'expression à droite et on l'associe au nom de la variable se trouvant à gauche. Le symbole flèche gauche <- aurait été plus judicieux.

je crée mes premières variables

Le terminal ci-dessous vous permet de créer et tester vos premières variables
{{ terminal () }}

#### Les types des variables

Durant l'affectation, le type des variables est choisi automatiquement en fonction de ce qui se trouve à droite du symbole =. Pour connaître le type de la variable nous pouvons utiliser la fonction Python ```type()```
la fonction ```print()``` permet d'afficher le résultat à l'écran

```py
a = 1
print(type(a))
a = 1.0
print(type(a))
a = 'Bonjour'
print(type(a))

>> <class 'int'>
>> <class 'float'>
>> <class 'str'>
```

A vous de jouer
{{ terminal () }}

##### les opérations entre des types différents

- Vous pouvez additionner un nombre entier et un réel, le résultat sera automatiquement un réel. 
- Vous pouvez multiplier un nombre et une chaîne de caractères
- Vous pouvez "additionner" 2 chaînes de caractères
- La division de 2 entiers donne automatiquement un réel
    - Pour avoir un entier, il faut utiliser la division euclidienne avec le symbole //
    - Le symbole % vous donnera le reste de cette division

##### Convertir un type en un autre

Pour cela il faut utiliser la fonction de conversion adéquate :

- ```int()``` pour obtenir un entier
- ```float()``` pour un réel
- ```str()``` pour une chaîne de caractères

#### Les opérations sur les chaînes de caractères

De base nous avons :

```py
a = 'Bonjour'
b = 'toi'
```

- Concaténer 2 chaînes de caractères : ```a + ' ' + b``` qui nous donne ```'Bonjour toi'``` 
- Connaître la longueur d'une chaîne de caractères : ```len(a)``` qui nous donne ```6```
- Accéder à un caractère ou un ensemble de caractères :
  ```py
  print(a[0:2])
  print(a[2:-2])
  print(a[3:])
  print(a[:3])

  >> Bo
  >> njo
  >> jour
  >> Bon
  ```
- Transformer une chaîne en majuscules/minuscules, avec les fonctions ```a.upper()``` et ```a.lower()```
- Rechercher ou remplacer une chaîne avec ```a.find('Bon')``` et ```a.replace('Bon', 'Abat-')```

!!! warning "Remarque"
> Ces 4 dernières fonctions ne modifient pas la chaîne en cours, elles retournent une nouvelle chaîne
> 
```py
a = 'Bonjour'
b = a.replace('Bon', 'Abat-')
print(a)
print(b)

>> Bonjour
>> Abat-jour
```

{{ terminal () }}

### Instruction d'affichage



### Instructions de saisie



### La structure conditionnelle
### La notion de boucle
### Les fonctions

{{ IDEv('../scripts/essai/moyenne', MAX = 5, SANS = 'min, max') }}

```python linenums="1" hl_lines="2 3"
def tri_bulles(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```
