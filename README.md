# Étiquetage Morphosyntaxique avec HMM et Viterbi

Implémentation complète d'un système d'étiquetage grammatical (Part-of-Speech Tagging) utilisant les Modèles de Markov Cachés (HMM) et l'algorithme de Viterbi.

##  Description

Ce projet développe un étiqueteur morphosyntaxique pour le français qui assigne automatiquement des étiquettes grammaticales à chaque mot d'un texte. Le système est entraîné sur le corpus Universal Dependencies French-GSD et utilise des techniques avancées de traitement automatique des langues.

##  Objectifs

- **Étiquetage automatique** : Assigner la catégorie grammaticale correcte à chaque mot
- **Apprentissage statistique** : Utiliser des HMM pour modéliser les séquences linguistiques
- **Décodage optimal** : Appliquer l'algorithme de Viterbi pour trouver la séquence d'étiquettes la plus probable
- **Évaluation de performance** : Mesurer l'accuracy du modèle sur des données de test

##  Architecture du Système

### 1. Préparation des Données
- **Lecture CONLL-U** : Parsing du format standard Universal Dependencies
- **Extraction des features** : Mots et étiquettes POS
- **Construction du vocabulaire** : Gestion des mots fréquents et rares

### 2. Modèles de Markov Cachés
- **Matrice de transition (A)** : Probabilités entre étiquettes (`P(tag|tag_prev)`)
- **Matrice d'émission (B)** : Probabilités d'émission (`P(mot|tag)`)
- **Lissage de Laplace** : Prévention des probabilités nulles

### 3. Algorithme de Viterbi
- **Phase Forward** : Calcul des probabilités cumulées optimales
- **Phase Backward** : Reconstruction du chemin d'étiquettes optimal

##  Performance

Le modèle atteint une précision de **91.23%** sur le corpus de test, démontrant son efficacité pour l'étiquetage du français.

 ## Résultats
  Haute précision (91.23%) sur données de test
  
  Robustesse grâce au lissage de Laplace
  
  Efficacité sur des phrases de longueur variable
  
  Gestion des mots inconnus via le vocabulaire filtré
