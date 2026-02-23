# TP : Prédiction de la Location de Vélos en Libre-Service

## Contexte et Objectif

Ce projet est un travail pratique réalisé dans le cadre du cours **Data Science par l'Application** à l'**Université de Technologie de Troyes (UTT)**.

L'objectif est de **prédire le nombre de vélos loués par heure** pour un système de location de vélos en libre-service (ex: Vélib). Ce modèle permettra à l'organisme de gestion d'optimiser l'organisation de ses équipes de maintenance pour répondre au mieux à la demande de ses clients.

## Objectifs du TP

- Dérouler la méthodologie du **POC** (Proof of Concept) sur une problématique réelle
- Utiliser les grandes familles d'algorithmes de **machine learning** présentés en cours
- Mettre en place les **bonnes pratiques** pour l'entraînement et la validation d'un modèle
- Justifier les choix techniques et interpréter les résultats

## Ensemble de Données

Le dataset contient des relevés horaires avec les variables suivantes :

| Variable | Description |
|----------|-------------|
| `instant` | Index du relevé |
| `dteday` | Date du relevé |
| `season` | Saison (1=Printemps, 2=Été, 3=Automne, 4=Hiver) |
| `mnth` | Mois du relevé (1-12) |
| `hr` | Heure du relevé (0-23) |
| `holiday` | Indicateur de jour de vacances scolaires |
| `weekday` | Jour de la semaine |
| `weather` | Conditions météorologiques (1-4) |
| `temp` | Température en °C |
| `atemp` | Température ressentie en °C |
| `humidity` | Taux d'humidité |
| `windspeed` | Vitesse du vent |
| `casual` | Nombre de locations d'usagers non abonnés |
| `registered` | Nombre de locations d'usagers abonnés |
| `count` | **Nombre total de locations (CIBLE)** |

## Prérequis

- Python 3.7+
- Jupyter Notebook
- Bibliothèques principales :
  - `pandas` - Manipulation de données
  - `numpy` - Calculs numériques
  - `matplotlib` & `seaborn` - Visualisations
  - `scikit-learn` - Algorithmes de machine learning
  - `xgboost`, `lightgbm`, `catboost` - Gradient boosting avancé

## Installation

### 1. Cloner ou télécharger le projet
```bash
cd path/to/project
```

### 2. Créer un environnement virtuel (recommandé)
```bash
python -m venv venv
source venv/bin/activate  # Sur Windows: venv\Scripts\activate
```

### 3. Installer les dépendances
```bash
pip install -r requirements.txt
```

### 4. Lancer Jupyter Notebook
```bash
jupyter notebook
```

Ouvrez ensuite le fichier `TP_velo_sujet.ipynb`

## Structure du Projet

```
notebook/
├── TP_velo_sujet.ipynb          # Notebook principal avec analyses et modèles
├── TP_velo_sujet.html           # Export HTML du notebook (avec résultats)
├── README.md                     # Ce fichier
└── ../data/
    └── input/
        └── velo.csv             # Dataset
```

## Contenu du Notebook

Le notebook est organisé en plusieurs sections :

### 1. **Questions Préalables**
   - Identification de la famille d'algorithmes appropriée (Régression)
   - Sélection de la variable cible (`count`)

### 2. **Extraction et Analyse de la Donnée**
   - Chargement du dataset
   - Exploration des données
   - Vérification de l'intégrité
   - Analyse des valeurs manquantes

### 3. **Analyse Exploratoire (EDA)**
   - Statistiques descriptives
   - Distributions des variables
   - Corrélations et patterns temporels
   - Visualisations des tendances saisonnières

### 4. **Préparation des Données**
   - Recodage des variables catégoriques
   - Normalisation/Standardisation
   - Création de features supplémentaires
   - Séparation train/test

### 5. **Modélisation**
   - Régression Linéaire
   - Régression Ridge/Lasso
   - Arbres de Décision
   - Forêts Aléatoires
   - Gradient Boosting (XGBoost, LightGBM, CatBoost)

### 6. **Évaluation et Comparaison**
   - Métriques de performance (MAE, RMSE, R²)
   - Validation croisée
   - Courbes d'apprentissage
   - Feature importance

### 7. **Conclusions et Recommandations**
   - Synthèse des résultats
   - Choix du meilleur modèle
   - Recommandations opérationnelles

## Utilisation

1. **Ouvrir le notebook** dans Jupyter
2. **Exécuter toutes les cellules** (Kernel → Restart & Run All)
3. **Consulter les résultats** : graphiques, tableaux, métriques
4. **Exporter en HTML** : File → Download as → HTML

## Résultats Attendus

Le projet valide l'approche de machine learning pour ce problème en :
- Comparant plusieurs familles d'algorithmes
- Démontrant l'importance des features
- Fournissant un modèle prédictif robuste
- Offrant des insights exploitables pour l'organisation

## Points Clés d'Apprentissage

- **Méthodologie** : POC, EDA, train/test/validation
- **Algorithmes** : Compréhension comparative des différentes approches
- **Bonnes Pratiques** : Validation croisée, feature engineering, hypertuning
- **Interprétabilité** : Justification des choix techniques au-delà de la performance

## Format du Rendu

- Code Python en format **Jupyter Notebook**
- Contenu mixte : code + texte + graphiques
- Export **HTML** avec toutes les cellules exécutées
- Ensemble cohérent de justifications et d'explications

## Technologies Utilisées

- **Python 3.x**
- **Jupyter Notebook**
- **Pandas** : Manipulation et analyse de données
- **NumPy** : Calculs numériques
- **Scikit-learn** : Machine learning
- **Matplotlib & Seaborn** : Visualisations
- **XGBoost, LightGBM, CatBoost** : Gradient boosting

---

## Auteur

**Jéhovahni SODJINOU**  
Étudiant UTT - Mastère Spécialisé Expert Big Data Engineer

## Licence

Ce projet est réalisé à des fins éducatives pour l'UTT.

---

**Dernière mise à jour :** Février 2026

