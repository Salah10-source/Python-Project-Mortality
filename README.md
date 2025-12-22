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

## 2) Source des données et mode d’accès

Les données utilisées dans ce projet proviennent de la **Human Mortality Database (HMD)**. Les deux fichiers textes **`Exposures`** et **`Deaths`** ont été téléchargés depuis la plateforme HMD (https://www.mortality.org/) après sélection du pays **France** et soumission d’une adresse e-mail (procédure d’accès standard de la HMD).

Afin d’assurer la **reproductibilité** et de **dissocier le code des données**, ces fichiers ne sont pas versionnés dans le dépôt Git. Ils ont été déposés sur le stockage objet **SSP Cloud (MinIO)**, via le *File Explorer*, dans l’emplacement suivant :

`s3://salaheddine/diffusion/Mortalite_France/`

Ils sont ensuite **importés directement dans le code** à partir de ce répertoire pour exécuter l’ensemble des étapes de construction de la base finale.

## 3) Structure du projet

```text
.
├── main.ipynb          # Notebook principal (analyse complète)
├── requirements.txt    # Dépendances Python nécessaires au projet
└── README.md           # Description du projet
```

## 4) Utilisation

### Pré-requis
- Python (recommandé : **3.9+**)
- `pip`

### Exécution
- pip install -r requirements.txt (Installation des dépendances nécessaire)
- Lancer le notebook demo.ipynb (Run All)

## 5) Résultat général

### Résultat général (bref)
Les modèles de **Machine Learning** se révèlent globalement **plus robustes en prédiction** que les modèles statistiques classiques (ex. **Lee–Carter**), notamment parce qu’ils capturent mieux les **non-linéarités** et les **relations complexes** présentes sur l’ensemble des années.

