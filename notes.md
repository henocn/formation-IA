			LES BASES MATHEMATIQUES RAPPEL


### Des vecteurs forment une base
Si c'est une famille libre et generatrcie

Fonction $GELU(x)$ derivable partout et plus fiable que $RELU(x)$
On a les vecteurs :
- vecteur discret (nombres entiers)
- vecteur dense (nombres réels)

$R ^ mXn m $: nombre d'exemples
		n : echantillons
**trace d'une matrice** c'est la somme des elements des diagolanles
Matrice diagonalisable $PDP^-1$
La puissance d'une matrice $PD^kP^-1$ pour une matrice élévée à la puissance k

**SVD** : Singular v=Value Decomposition.



***
			LES BASES MATHEMATIQUES DU DEEP LEARNING

**tenseur** une fonction multilinéaire
**scalaire** : simililarité (-1 mot oposé, 0 orthogonaux, 1 proches)
**softmax** : transformer un vecteur en une distribution de probabilités.

Role models : approximer la distribution.
**hypothese de markov** : cette hypothèse permet de reduire la complexité du modèle
**cont(wt-1, wt)** : le nbr de fois que wt suit wt-1 qui est une probabilité
pour éviter que cette probabilité soit nulle on ajoute un alpha

pour calculer l'incertitude on calcule l'antropie (qui permet de savoir la performance d'un model)
- faible antropie dstribution concentré model est confiant
- faible antropie dstribution model est incertain

**perplexité** : le nombre effectif de mots probables que le model considere 
_perplexité inférieur plus consistant qui permet d'évaluer de manière quantitative_

fonctions d'activation :
- **signoide logistique** $f(x) = \frac{1}{1-e{^-1}}$ probleme de saturation,
- **tangente hyperbolique** centré en 0 probleme de saturation,
- **RELU** neurones morts,
- **GENU**

Quand il n'ya a pas de fonction d'actiation et donc les choses seront linéaires et le model n'apprend pas grand chose. et pour cela on ajout des fonction d'activation non linéaires

Arcitecture transformers
### <u>La fonction de perte </u>
l'ecart entre la prédiction et la réalité. L'object est de minimiser la erte.

La descente de gradient ets une méthode d'optimisation

### <u> Back propagation </u>
Calcul des dérivées partielles de la fonction de perte par rapport aux parametres du model.

### <u> Méthodes d'optimisation </u>
- SGD
- Momentum
- Adam (adaptative Moment Esstimation)

Pour une transformation il faut :
- Sémantique : les mot similaires doivent etre proches en nombres ecludien
- capacité de généralisation.

### <u>La vectorisation c'est aussi d'encoder.</u>
Les différents types d'encodages
- **representation discretes**
  **one-hot** (absence de sémantique, problème de généralisation _ce quil n'as pas vu au cours de l'apprentissage il ne peut pas le faire_)
- **représentation dense** 
  1. **Word2vec**
   Prédire les mots du contexte (probleme : coup computationnel.)
  2. **GloVe (global vector)**
   Apprendre les contextes des mots

### <u>Mesure de la similarité </u>

Quantifier la proximité semantique de deux representation mos
- similatité cosinus (-1 mot oposé, 0 orthogonaux, 1 proches)
- score d'attention (défini deux clefs requete et valeurs)



***
			ARCHITECTURE CLEFS DES TRANSFORMERS

			
### Traitement sequentiel des données
**Objectif** : _modeliser les dépendences entre les différents elements d'une séquence_
#### Les modele
- recurrent neurone (RNN /LSTN)
  - difficile de relier deux mots eloigné
  - cout temporel elevé
  - **dificulté** a cerner le contexte d'un texte assez long

### Structure globale des transformer

**encodeur** encode une séquence
**decodeur** génére la séquence cible.

