# ⚡ Building Energy Prediction API

## 🎯 Contexte

La ville de Seattle souhaite atteindre la neutralité carbone d’ici 2050.  
Dans ce cadre, elle cherche à mieux anticiper la consommation énergétique des bâtiments non résidentiels.

Les relevés énergétiques étant coûteux à réaliser, l’objectif du projet est de prédire la consommation d’énergie à partir des caractéristiques structurelles des bâtiments.

---

## 🧩 Problématique

Comment construire un modèle de Machine Learning capable de prédire la consommation énergétique d’un bâtiment, puis l’exposer via une API utilisable en temps réel ?

---

## 🏗️ Pipeline du projet

1. Analyse exploratoire des données
2. Nettoyage et filtrage des bâtiments pertinents
3. Traitement des valeurs manquantes et outliers
4. Feature engineering
5. Préparation des variables pour la modélisation
6. Comparaison de plusieurs modèles supervisés
7. Optimisation du meilleur modèle avec `GridSearchCV`
8. Analyse des features importantes
9. Création d’une API d’inférence avec BentoML
10. Déploiement cloud du modèle

---

## 🛠️ Stack technique

- Python
- Pandas
- Scikit-learn
- BentoML
- Pydantic
- Docker
- Cloud deployment
- Jupyter Notebook

---

## 📊 Analyse exploratoire

L’analyse exploratoire a permis de :

- filtrer les bâtiments non résidentiels pertinents ;
- identifier et traiter les valeurs aberrantes ;
- analyser les variables structurelles des bâtiments ;
- éviter le data leakage en excluant les variables directement liées à la consommation réelle.

---

## 🤖 Modélisation

Plusieurs modèles de régression ont été testés et comparés.

Les performances ont été évaluées avec :

- R²
- RMSE

Le meilleur modèle a été optimisé avec `GridSearchCV`.

---

## 🔍 Interprétation du modèle

L’analyse des features importantes a permis d’identifier les variables ayant le plus d’impact sur la prédiction de consommation énergétique.

Cette étape permet de rendre le modèle plus explicable et plus utile dans un contexte décisionnel.

---

## 🌐 API d’inférence

Le modèle est exposé via une API BentoML.

L’API permet d’envoyer les caractéristiques d’un bâtiment et de recevoir une prédiction de consommation énergétique.

Une validation des données d’entrée est mise en place avec Pydantic afin d’éviter les valeurs incohérentes.

---

## 🚀 Déploiement

Le projet inclut un fichier `bentofile.yaml` permettant de packager le modèle, son service API et ses dépendances.

L’API peut être servie localement avec :

```bash
bentoml serve service.py
```
Puis packagée et déployée sous forme d’image Docker.

---

## 💡 Compétences démontrées

- Analyse exploratoire de données  
- Nettoyage et préparation de données  
- Feature engineering  
- Prévention du data leakage  
- Entraînement de modèles supervisés  
- Validation croisée  
- Optimisation d’hyperparamètres  
- Interprétation de modèle  
- Création d’API ML  
- Validation des entrées API  
- Déploiement cloud  

---

## 📁 Livrables

- Notebook d’analyse et de modélisation  
- Support de présentation  
- Scripts Python pour l’API  
- Fichier `bentofile.yaml`  
- Modèle sauvegardé via BentoML  

---

## 🚧 Axes d’amélioration

- Analyser plus finement la distribution des erreurs du modèle  
- Identifier les segments de bâtiments où le modèle sous-performe  
- Supprimer les features peu explicatives  
- Ajouter un monitoring des prédictions  
- Industrialiser le pipeline d’entraînement et de déploiement  

---

## 🏙️ Objectif métier

Ce projet permet à la ville de Seattle de disposer d’un prototype capable d’estimer la consommation énergétique de bâtiments sans relevé terrain immédiat.

Il s’inscrit dans une logique d’aide à la décision pour la planification énergétique et environnementale.
