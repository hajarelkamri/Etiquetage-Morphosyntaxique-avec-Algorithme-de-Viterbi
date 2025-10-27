# Étiquetage Morphosyntaxique avec Algorithme de Viterbi

Implémentation d'un système complet d'étiquetage morphosyntaxique (POS tagging) utilisant l'algorithme de Viterbi sur des modèles de Markov cachés (HMM).

##  Description du Projet

Ce projet implémente un étiqueteur morphosyntaxique pour le français qui assigne automatiquement des étiquettes grammaticales (Part-of-Speech tags) à chaque mot d'une phrase. Le système utilise des modèles de Markov cachés entraînés sur le corpus Universal Dependencies (UD) French-GSD.

##  Fonctionnalités

- **Lecture et parsing** des fichiers CONLLU format UD
- **Entraînement de modèles HMM** avec comptage des transitions et émissions
- **Gestion des mots inconnus** via un token `<UNK>`
- **Lissage (smoothing)** pour améliorer la robustesse
- **Algorithme de Viterbi** pour l'inférence optimale
- **Évaluation complète** avec calcul d'accuracy

##  Architecture du Système

### 1. Préparation des Données
- Lecture des fichiers CONLLU
- Extraction des mots et étiquettes POS
- Construction du vocabulaire avec seuil de fréquence

### 2. Modèles Statistiques
- **Matrice de transition A** : Probabilités entre étiquettes
- **Matrice d'émission B** : Probabilités mot|étiquette
- **Lissage de Laplace** pour gérer les données manquantes

### 3. Algorithme de Viterbi
- **Phase forward** : Calcul des probabilités optimales
- **Phase backward** : Reconstruction du chemin optimal

##  Métriques de Performance

Le modèle est évalué sur :
- **Accuracy global** sur l'ensemble de test
- **Accuracy par phrase** pour analyse détaillée
- **Tests manuels** avec phrases personnalisées


