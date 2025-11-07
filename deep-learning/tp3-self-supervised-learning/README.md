# 🧠 TP3 — Apprentissage Auto-Supervisé (SSL)
**Auteur : Wassim CHIKHI — M2 VMI 2025**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vvazzim/Tp-VMI-Wassim/blob/main/deep-learning/tp3-self-supervised-learning/notebooks/Self_Supervised_Learning_Demos_final.ipynb)

---

## 🎯 Objectif
Comparer différentes **tâches prétextes** en apprentissage auto-supervisé (SSL) sur les datasets **CIFAR-10** et **STL-10**, afin d’évaluer leur capacité à apprendre des représentations utiles pour la classification.

---

## ⚙️ Configuration
- **Encodeur** : ResNet-18 (ou CNN simple)
- **Optimiseur** : Adam, *lr = 0.001*
- **Datasets** : CIFAR-10 (32×32), STL-10 (96×96)
- **Entraînement** : 20 epochs (prétexte) + 5 epochs (linear probe)
- **Plateforme** : Google Colab (GPU T4)

---

## 🧪 Méthodologie
- Implémentation de la tâche prétexte **Relative Patch Location** (Doersch et al., 2015).
- Comparaison avec **Rotation Prediction**, **Inpainting**, et **SimCLR**.
- Évaluation linéaire (classifieur gelé) sur les représentations apprises.

---

## 📊 Résultats (linear probe)
| Tâche prétexte | CIFAR-10 | STL-10 |
|----------------|-----------|---------|
| Relative Patch | **22.6 %** | **14.2 %** |
| Rotation | **68.5 %** | **49.3 %** |
| Inpainting | **74.3 %** | — |
| SimCLR | **81.0 %** | — |

**Analyse :**
- La tâche **Relative Patch** apprend des structures locales mais peu transférables.  
- **Rotation** et **SimCLR** capturent de meilleures représentations globales.  
- **STL-10** est plus complexe → les limites des approches locales sont plus visibles.

---

## 🧩 Conclusion
Les tâches **globales ou contrastives** (SimCLR, Rotation) sont les plus efficaces pour le transfert.  
Relative Patch reste utile en complément, notamment pour des approches **multi-prétexte** ou **géométriques**.

**Perspectives :**
- Entraînement plus long (epochs ↑)  
- Fine-tuning complet  
- Architectures plus profondes

---

## 🔗 Liens utiles
- Notebook Colab : badge ci-dessus ☝️  
- Rapport PDF : [`rapport/CHIKHI_Wassim_TP_SSL_VMI2025.pdf`](./rapport/CHIKHI_Wassim_TP_SSL_VMI2025.pdf)

---

## 📚 Références
- [1] Doersch, M. et al. *Unsupervised visual representation learning by context prediction* (ICCV 2015).  
- [2] Gidaris, S. et al. *Unsupervised representation learning by predicting image rotations* (arXiv 2018).  
- [3] Chen, T. et al. *SimCLR: A Simple Framework for Contrastive Learning* (arXiv 2020).  
- [4] Pathak, D. et al. *Context Encoders: Feature Learning by Inpainting* (CVPR 2016).  
