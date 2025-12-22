# Prévision de la mortalité (France, 1816–2023)

Ce dépôt contient un projet de prévision de la mortalité en France sur la période **1816–2023**, avec une comparaison entre **méthodes statistiques classiques** (notamment **Lee–Carter**) et **approches modernes de Machine Learning** (ex. Random Forest, XGBoost, SVM, MLP).

## 1) Contexte et problématique

### Contexte
L’analyse de la mortalité est un enjeu majeur pour :
- les **systèmes de retraite**,
- les **assurances vie**,
- les **politiques publiques de santé**,
- la **planification socio-économique**.

La période 1816–2023 couvre des dynamiques démographiques et sanitaires complexes : vieillissement de la population, progrès médicaux, et chocs (ex. crises sanitaires), ce qui rend la prévision particulièrement exigeante.

### Problématique
**Les approches de Machine Learning permettent-elles d’améliorer la qualité des prévisions de mortalité par rapport aux modèles classiques, en particulier Lee–Carter, en termes de précision, stabilité et robustesse ?**

## 2) Structure du projet

```text
.
├── demo.ipynb          # Notebook principal (analyse complète)
├── requirements.txt    # Dépendances Python nécessaires au projet
└── README.md           # Description du projet
```

## 3) Utilisation

### Pré-requis
- Python (recommandé : **3.9+**)
- `pip`

### Exécution
- pip install -r requirements.txt (Installation des dépendances nécessaire)
- Lancer le notebook demo.ipynb (Run All)

## 4) Résultat général

### Résultat général (bref)
Les modèles de **Machine Learning** se révèlent globalement **plus robustes en prédiction** que les modèles statistiques classiques (ex. **Lee–Carter**), notamment parce qu’ils capturent mieux les **non-linéarités** et les **relations complexes** présentes sur l’ensemble des années.

