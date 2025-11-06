# 🧠 Travaux Pratiques — Vision & Machines Intelligentes (VMI)
**Auteur :** Wassim CHIKHI  
**Année :** 2025  
**Master 2 — Parcours Vision et Machines Intelligentes (VMI)**

---

## 🎯 Objectif du dépôt
Ce dépôt centralise **l’organisation des Travaux Pratiques** du Master 2 VMI :  
Deep Learning, Reconnaissance de Formes Avancée, Imagerie Biomédicale et Imagerie 3D.

🧩 **Tout le travail s’effectue sur Google Colab**  
➡️ Les notebooks présents ici ne sont que des *squelettes structurés* destinés à être ouverts et complétés sur Colab.  


---

## 🗂️ Organisation générale
```
tp-vmi-wassim/
├─ reco-forme-avancee/
│  └─ tp1-fuzzy-cmeans/
│     ├─ notebooks/   → Notebook principal (à ouvrir sur Colab)
│     ├─ data/        → Liens Drive / URL des jeux de données
│     └─ rapport/     → Figures + rapport LaTeX → PDF final
│
├─ deep-learning/
│  ├─ tp1-mlp-mnist/
│  └─ tp2-cnn-transfer-learning/
│
├─ imagerie-biomed/
│  └─ tp1-seg-medicale/
│
├─ 3d/
│  └─ tp1-bases/
│
└─ docs/templates/
```

---

## 🔑 Principes de travail
- 📘 **1 TP = 1 dossier** (structure identique à reproduire sur Colab).  
- 📂 **Données** : uniquement *liens Drive/URL*, pas de fichiers lourds dans le repo.  
- 🧾 **Rapport** : rédigé en **LaTeX** et exporté en PDF (dans `rapport/`).  
- 🚀 **Badge Colab** dans chaque `README.md` pour ouverture directe du notebook.  
- 🧠 **Versioning GitHub** : “Save a copy to GitHub” depuis Colab à chaque étape clé.

---

## 🧩 Priorités de développement
| Ordre | UE | TP | Thème principal |
|:--:|:--|:--|:--|
| 1️⃣ | Reconnaissance de Formes Avancée | TP1 | Segmentation par **Fuzzy C-Means** |
| 2️⃣ | Deep Learning | TP1 | **MLP sur MNIST** |
| 3️⃣ | Deep Learning | TP2 | **CNN + Transfer Learning (ResNet18)** |
| 4️⃣ | Imagerie Biomédicale | TP1 | Segmentation médicale (SimpleITK) |
| 5️⃣ | 3D | TP1 | Visualisation et traitement de nuages de points |

---

## 🧭 Workflow Colab recommandé
1️⃣ **Ouvrir** le notebook via le badge “Open in Colab”.  
2️⃣ **Monter Drive** :  
```python
from google.colab import drive
drive.mount('/content/drive')
```
3️⃣ **Charger les données** depuis Drive ou une URL.  
4️⃣ **Exécuter / documenter / sauvegarder** ton travail sur Colab.  
5️⃣ **Exporter** les résultats importants vers `rapport/`.  
6️⃣ **Rédiger le rapport LaTeX** et générer le PDF final.

---

## 🗃️ Dossiers utiles
- `docs/templates/README_TP.md` → Modèle de README par TP  
- `docs/templates/rapport_template.tex` → Modèle LaTeX pour les rapports  
- `docs/templates/COLAB_header.md` → En-tête standard à coller dans ton premier bloc Colab

---

## ⚖️ Licence
Projet académique — **Licence MIT**  
© 2025 — *Wassim CHIKHI*
