# 🧪 TP1 — Imagerie Photonique : Modalités et principe de la fluorescence

**Auteur :** Wassim Chikhi  
**Année :** 2025–2026  
**Formation :** Master 2 Vision & Machine Intelligente — UE Bio-Imagerie Médicale  
**Université :** Université Paris Cité  

---

## 🎯 Objectifs
Ce premier TP vise à illustrer les **principales modalités de microscopie photonique** :
- Microscopie en **champ clair** (transmission)
- Microscopie à **contraste de phase**
- Microscopie à **fluorescence (champ large)**
- Microscopie **confocale à balayage**

Chaque configuration est représentée par un **schéma optique en TikZ**, construit selon les principes physiques vus en cours.

---

## 📂 Structure du projet
```
TP1_BioImg/
├── figures/                   # Schémas TikZ des quatre microscopes
│   ├── 01_microscope_champ_clair.tex
│   ├── 02_microscope_contraste_phase.tex
│   ├── 03_microscope_fluorescence.tex
│   └── 04_microscope_confocal.tex
├── images/                    # Graphiques et images de résultats
│   └── mean_intensity_plot.png
├── Universite_Paris-Cite-logo.jpeg
├── rapport.tex                # Rapport principal en LaTeX
└── TP_1_BioImg.pdf            # Rapport compilé final
```

---

## ⚙️ Compilation du rapport
### En local
```bash
pdflatex -shell-escape rapport.tex
```
⚠️ Le flag `-shell-escape` est indispensable pour que les figures **standalone** soient automatiquement compilées.

### En ligne (Overleaf)
- Importer le dossier complet  
- Vérifier que le mode de compilation est `LaTeX ➜ PDF`  
- Activer **Shell Escape** dans les paramètres du projet  

---

## 📊 Analyse d'image
Une séquence temporelle (`cell2D_timelapse.tif`) est utilisée pour illustrer le **photoblanchiment** :
- Calcul de l’intensité moyenne par image :  
  \[
  I_{moy}(t) = \frac{1}{N}\sum_{i=1}^{N} I_i(t)
  \]
- Résultat : décroissance progressive de la fluorescence.

---

## 📈 Résultats
- **Figures principales :**
  - `01_microscope_champ_clair.pdf`
  - `02_microscope_contraste_phase.pdf`
  - `03_microscope_fluorescence.pdf`
  - `04_microscope_confocal.pdf`
- **Graphique d’intensité moyenne :**
  - `mean_intensity_plot.png`

---

## 📝 Rapport final
Le rapport complet est disponible ici :  
📄 **[`TP_1_BioImg.pdf`](TP_1_BioImg.pdf)**  

---

## 🧩 Remarques
- Tous les schémas TikZ utilisent un jeu de couleurs standardisé :
  - Vert `exc` pour l’excitation
  - Rouge `emi` pour l’émission
  - Gris `opticgray` pour les éléments optiques neutres  
- Compatible avec `tau-class` pour la mise en page normalisée des TPs du M2 VMI.
