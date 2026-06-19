# Dakar Rental Price Prediction

Prédiction des loyers résidentiels à Dakar (Sénégal) par apprentissage automatique.

## Prérequis

- Python 3.9+
- Git

## Installation

```bash
git clone https://github.com/<votre-username>/dakar_location_price_modelisation.git
cd dakar_location_price_modelisation

python -m venv venv
source venv/bin/activate        # Windows : venv\Scripts\activate

pip install -r requirements.txt
```

## Jeu de données

Le dataset n'est pas inclus dans ce dépôt. Il est disponible sur Kaggle :

**[Annonces de location résidentielle — Dakar, Sénégal](https://www.kaggle.com/datasets/kassadiallo/annonces-de-location-rsidentielle-dakar-sngal/data)**

Téléchargez `dataset.csv` et placez-le à la racine du projet avant de lancer le notebook.

## Lancer le notebook

```bash
jupyter notebook modelisation.ipynb
```

Exécuter les cellules dans l'ordre — le notebook est auto-suffisant.

## Structure

```
├── dataset.csv          # À télécharger sur Kaggle (voir section ci-dessus)
├── modelisation.ipynb   # Pipeline complet : EDA → modèles → intervalles de confiance
└── requirements.txt     # Dépendances
```

## Contenu du notebook

1. Chargement et feature engineering
2. Analyse exploratoire (EDA)
3. Préprocesseur sans data leakage
4. Baselines : Régression Linéaire, Random Forest, XGBoost
5. Optimisation bayésienne (Optuna) : XGBoost & LightGBM
6. Intervalles de confiance par régression quantile [q10–q50–q90]

## Licence

MIT
