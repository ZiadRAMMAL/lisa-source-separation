# Séparation de Sources pour la Mission LISA (Deep Learning & Traitement du Signal)

Ce dépôt contient le code développé dans le cadre de mon stage de Master 1 EEA (parcours SIA2) à l'Université de Toulouse, portant sur la **séparation de sources pour la mission spatiale LISA** (Laser Interferometer Space Antenna).

---

## 🎯 Contexte du Projet

La mission spatiale **LISA** de l'Agence Spatiale Européenne (ESA) a pour objectif de détecter les ondes gravitationnelles depuis l'espace. Les données enregistrées par les interféromètres contiennent un mélange complexe de signaux astrophysiques superposés, notamment :
* Les **MBHB** (Massive Black Hole Binaries)
* Les **GBs** (Galactic Binaries)

L'objectif de ce projet est de concevoir et d'entraîner des modèles de Deep Learning (architectures de type U-Net, approches par classification/régression et masques complexes) afin de séparer et d'extraire efficacement ces différentes composantes fréquentielles et temporelles à partir des données simulées.

---

## 🛠️ Stack Technique & Bibliothèques

Le projet repose sur les technologies suivantes :
* **Langage :** Python 3.11
* **Deep Learning :** PyTorch, TensorFlow
* **Traitement du Signal & Manipulation :** NumPy, SciPy, Pandas, H5Py (`.h5`)
* **Visualisation :** Matplotlib, Seaborn

---

## ⚙️ Installation et Environnement

Pour garantir la reproductibilité des résultats, un fichier de configuration Conda est fourni.

1. Cloner le dépôt :
   ```bash
   git clone [https://github.com/ZiadRAMMAL/lisa-source-separation.git](https://github.com/ZiadRAMMAL/lisa-source-separation.git)
   cd lisa-source-separation

2. Créer l'environnement Conda à l'aide du fichier environment.yml :
    ```bash
    conda env create -f environment.yml

3. Activer l'environnement :
    ```bash
    conda activate ml_gpu

---

## 📦 Gestion des Données et Modèles

En raison de leur taille importante, les jeux de données d'entraînement (fichiers `.h5`) et les poids des modèles entraînés (fichiers `.pth`) ne sont pas stockés directement sur ce dépôt Git.

- **Jeux de données (`lisa_dataset_2k.h5`)** et **Poids des modèles** : Téléchargeables depuis l'espace de stockage dédié (Google Drive du projet). 
- Veille à placer les fichiers de données dans un dossier `data/` local avant d'exécuter les scripts d'entraînement ou d'inférence.

---

## 🚀 Structure du Projet

    ```text
    lisa-source-separation/
    │
    ├── environment.yml         # Configuration de l'environnement Conda
    ├── .gitignore              # Fichiers ignorés par Git (données, poids, caches)
    ├── README.md               # Documentation du projet
    ├── main.py                 # Script principal (ou notebooks d'entraînement)
    └── utils/                  # Fonctions utilitaires (chargement H5, métriques, etc.)

---

## 👤 Auteur

- **Ziad RAMMAL**
- Master 2 EEA - Spécialité Signal, Image et Machine Learning (SIA2) — Université de Toulouse
- Stage de fin M1 / Projets en Deep Learning