# Prédiction des Performances des Élèves

## Introduction

### Contexte:

Ce projet a pour objectif de développer un modèle d'apprentissage automatique afin de prédire la réussite ou l'échec des élèves en fonction de leurs caractéristiques. Les données incluent des informations telles que l'âge, le sexe, le temps d'étude hebdomadaire, les absences, le soutien parental, les activités parascolaires, le sport, la musique, le volontariat, le GPA et la classification des notes (`GradeClass`). Le but est d'utiliser ces informations pour anticiper si un élève réussira ou échouera.

### Objectif du projet:

L'objectif principal est de prédire la réussite scolaire des élèves (`succès` = 1 pour réussite, 0 pour échec) en utilisant des modèles d'apprentissage supervisé tout en explorant différentes techniques de prétraitement des données et de modélisation.

## Description du Dataset

### Source des données:

Le dataset est extrait de [Kaggle - Students Performance Dataset](https://www.kaggle.com/).

### Colonnes du dataset:

* `StudentID`: Identifiant unique de l'élève.
* `Age`: Âge de l'élève.
* `Gender`: Sexe de l'élève (1 = Masculin, 0 = Féminin).
* `Ethnicity`: Groupe ethnique de l'élève.
* `ParentalEducation`: Niveau d'éducation des parents.
* `StudyTimeWeekly`: Temps d'étude hebdomadaire (en heures).
* `Absences`: Nombre d'absences.
* `Tutoring`: Participation au tutorat (1 = Oui, 0 = Non).
* `ParentalSupport`: Niveau de soutien parental (1 à 3).
* `Extracurricular`: Participation à des activités parascolaires (1 = Oui, 0 = Non).
* `Sports`: Participation sportive (1 = Oui, 0 = Non).
* `Music`: Participation musicale (1 = Oui, 0 = Non).
* `Volunteering`: Participation au volontariat (1 = Oui, 0 = Non).
* `GPA`: Moyenne générale des notes.
* `GradeClass`: Classification des notes (1 à 4).
* `succès`: Variable cible binaire créée à partir de `GradeClass` (1 pour réussite si `GradeClass` <= 2, 0 sinon).

## Analyse Exploratoire des Données (EDA)

### Statistiques descriptives:

* Moyennes, médianes et écarts-types des variables numériques.
* Distribution des variables catégorielles (`Gender`, `Ethnicity`, etc.).

### Visualisation des données:

* Histogrammes des variables `StudyTimeWeekly`, `Absences`, `GPA`.
* Boxplot pour `Absences` et `GPA`.
* Heatmap des corrélations entre les variables numériques.

### Observations importantes:

* Les absences sont corrélées négativement avec le GPA.
* Le `GradeClass` est fortement influencé par le `GPA` et le `StudyTimeWeekly`.

## Prétraitement des Données

### Nettoyage des données:

* Vérification des valeurs manquantes et imputation par la moyenne.

### Transformation et normalisation:

* Normalisation des variables numériques (`Age`, `StudyTimeWeekly`, `Absences`, `GPA`).
* Encodage des variables catégorielles (`Gender`).

## Méthodes et Modèles

### Modèles utilisés:

* Régression Logistique : Simple et rapide pour la classification binaire.
* Random Forest : Modèle robuste pour capter des relations complexes.

### Choix des modèles:

* Régression Logistique pour sa simplicité et rapidité.
* Random Forest pour sa capacité à capturer des relations complexes.

## Évaluation des Modèles

### Métriques d'évaluation:

* Précision, Rappel, F1-score et Matrice de confusion.

### Résultats:

* Régression Logistique : Précision = 81%, Rappel = 78%, F1-score = 79%
* Random Forest : Précision = 86%, Rappel = 84%, F1-score = 85%

### Analyse des résultats:

* Le modèle Random Forest offre de meilleures performances en termes de précision et de F1-score.

## Conclusion et Perspectives

### Conclusion:

Le modèle Random Forest a montré les meilleures performances pour la prédiction de la réussite scolaire des élèves. Les variables `GPA`, `StudyTimeWeekly` et `Absences` se sont révélées être des prédicteurs clés.

### Perspectives:

* Ajouter des variables supplémentaires telles que les habitudes de sommeil ou le stress.
* Tester des modèles plus avancés comme les réseaux de neurones pour améliorer les prédictions.
