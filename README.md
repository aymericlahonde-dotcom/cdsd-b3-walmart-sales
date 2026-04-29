# Bloc 3 — Walmart Sales (Régression supervisée)

> Projet de la **Certification Jedha — Concepteur Développeur en Science des Données (CDSD)**
> [RNCP35288 — France Compétences](https://www.francecompetences.fr/recherche/rncp/35288/)
> **Bloc 3** : Analyse prédictive de données structurées — Régression supervisée

## Objectif du projet

Le service marketing de Walmart veut un modèle de Machine Learning capable d'**estimer les ventes hebdomadaires** dans leurs magasins, à partir de variables temporelles (date) et économiques (température, prix du carburant, CPI, taux de chômage).

Le projet se découpe en **3 parties** :

1. **Part 1 — EDA + preprocessing**
   - Drop des lignes où la target `Weekly_Sales` est manquante
   - Features depuis `Date` : year, month, day, day of week
   - Drop des outliers en dehors de [μ − 3σ, μ + 3σ] sur les variables numériques
   - Encodage des variables catégorielles (`Store`, `Holiday_Flag`)
   - Standardisation des variables numériques

2. **Part 2 — Régression linéaire baseline**
   - `LinearRegression` de scikit-learn
   - Évaluation train + test (R², RMSE)
   - Analyse des coefficients pour identifier les features importantes

3. **Part 3 — Régularisation**
   - `Ridge` ou `Lasso` pour réduire l'overfitting
   - Bonus : `GridSearchCV` pour tuner la régularization strength

## Données

Le dataset (CSV custom Jedha — modifié depuis la compétition Kaggle Walmart) est à télécharger depuis :
- <https://app.jedha.co/course/projects-supervised-machine-learning-ft/walmart-sales-ft>
- Cliquer sur le lien "Download" et placer le CSV dans `data/walmart_sales.csv`

## Livrable

- Notebook qui couvre les 3 parties
- Visualisations EDA + résidus
- Métriques régression (R², RMSE) train + test pour les 2 modèles
- Interprétation des coefficients

## Structure du projet

```
Bloc_3_Walmart_Sales/
├── notebooks/
│   └── 01_walmart_sales_analysis.ipynb    (notebook complet — livrable)
├── data/
│   └── walmart_sales.csv                  (à télécharger depuis Julie Jedha, gitignored)
├── requirements.txt
└── README.md
```

## Comment rejouer le projet

```bash
cd Bloc_3_Walmart_Sales
pip install -r requirements.txt
# Télécharger walmart_sales.csv depuis Julie Jedha dans data/
```

Puis ouvrir `notebooks/01_walmart_sales_analysis.ipynb` dans Jupyter ou VS Code.

## Auteur

[Aymeric Lahonde](https://github.com/aymericlahonde-dotcom) — promotion Jedha CDSD 2026.
