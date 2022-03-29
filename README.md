# Mask_Detection

---
created: 2022-03-29T11:25:39 (UTC +02:00)
tags: []
source: https://simplonline.co/briefs/2304814f-e468-44f0-bf69-55dcfdb80b17
author: 
---

![](https://simplonline.co/_next/image?url=https%3A%2F%2Fsimplonline-v3-prod.s3.eu-west-3.amazonaws.com%2Fmedia%2Fimage%2Fjpg%2Fe1b41b71-3725-4169-8494-d7b539be3217.jpg&w=1280&q=75)

# Modèle intelligente pour la détection des masques

Transfer learning pour la détection des masques

## Contexte du projet

Ce brief a pour objectif d’appliquer le Transfer Learning sur une base de données.

Dans ce brief, nous appliquons un apprentissage supervisé pour identifier si la personne porte un masque.

NB. Utiliser le Colab pour l'apprentissage du modèle (https://colab.research.google.com/?hl=fr)

## Challenges

- Manipulation des images.
- Analyse, prétraitement et visualisation des images.
- Manipulation et l’exploitation de la Bibliothèque Tensorflow.
- Charger un modèle CNN à partir de Tensorflow.
- Appliquer le Transfer Learning (sur VGG16).
- Faire des tests à partir de la webcam

## Phases de brief

### Partie 1 : Base de données, Analyse et Préparation

Pour aborder cette problématique, il est primordial d’avoir une DataSet. Pour cela, la DataSet se trouve sur : https://drive.google.com/drive/folders/1HOxFk8alSSMshf95ToLEUuYZ1Ki7p90Q?usp=sharing

Par la suite, il faut développer les étapes suivantes :
– Charger les images.
– Penser à redimensionner les images selon le modèle VGG16.
– Splitter les données en données d’apprentissage, validation et test.
– Visualiser les images de la classe `Avec_Masque` et `Sans_Masque`.

### Partie 2 : Architecture CNN sur Tensorflow

Cette deuxième partie est réservée pour développer le modèle CNN sur tensorflow, et lancée par la suite l’apprentissage de CNN.

- Au début, il faut préparer et appliquer la Data Augmentation sur les données d’apprentissage.
- Charger et configurer le modèle VGG16 pour l’application souhaitée.
- Appeler le ModelCheckpoint pour sauvgarder le meilleurs modèle durant l’apprentissage (`from keras.callbacks import ModelCheckpoint`)
- Lancer un apprentissage en utilisant les données d’apprentissage et les données de validation avec un historique.
- Tracer les courbes d’accuracy et d’erreur de train et validation.
- Calculer l’accuracy et la matrice de confusion sur les données de test.

### Partie 3 : Application

Nous cherchons à tester le modèle développé sur des nouvelles images.

Pour un début, cherchez des images sur le net ou prenez photos entre vous et tester le résultat de votre modèle en affichant le message : Avec masque ou Non masque sur l’image. (`cv2.putText(Img, message, (x, y), cv2.FONT_HERSHEY_SIMPLEX, .5, (0,0,0))`)


Par la suite, vous êtes censés à développer un code python qui va activer la Webcam et identifier si la personne qui est devant la Webcam porte un masque en affichant le message : Avec masque ou Non masque sur l’image.

## Modalités pédagogiques

Le deadline pour rendre ce travail est fixé pour le 4 avril.

Le projet est réalisé en groupe de 2 personnes.

## Critères de performance

- Le code doit être bien structuré
- Le bon choix du modèle CNN.
- Le bon fonctionnement de l'Application demandée.

## Modalités d'évaluation

- Un rapport sur le projet réalisé qui explique les différentes étapes du code
- Description des données
- Présentation de l'architecture utilisée
- Conclusion (avantages et inconvénients, concurrents, recommandations…)
- Revue de code avec le formateur.

## Livrables

Un dépôt GitHub avec :
- [ ] Un Notebook bien structuré/organisé qui réalise les différentes étapes de ce projet.
- [ ] Un rapport sur le projet réalisé qui explique les différentes étapes du code (Description des données, présentation de l'architecture utilisée, résultats de l'apprentissage et de test, conclusion, recommandations ...).
- [ ] Le modèle VGG16.h5
- [ ] Un Readme.md pour mettre en avant votre projet.

