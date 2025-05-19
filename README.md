# road-extraction
# 🛰️ Extraction automatique de réseaux routiers à l’aide des CNNs et GNNs

Ce projet est issu d’un mémoire de fin d’études soutenu à l’École de l’Aviation de Borj El Amri, Tunisie, en 2025.  
Il vise à développer un pipeline de segmentation sémantique et de reconstruction topologique des réseaux routiers à partir d’images satellites à très haute résolution, en combinant des modèles CNN, GNN et Foundation Models.

---

## 📁 Contenu du dépôt

| Fichier / Dossier        | Description |
|--------------------------|-------------|
| `unet.ipynb`             | Implémentation du modèle U-Net pour la segmentation des routes. |
| `UnetPlusPlus.ipynb`     | Implémentation du modèle U-Net++ avec backbone ResNet50. |
| `agf-net.ipynb`          | Implémentation du modèle AGF-Net intégrant les modules DCSA, GFFM et MSCM. |
| `sam_road-main.zip`      | Code source complet du modèle SAM-Road (GNN pour reconstruction topologique). |
| `samDINO.zip`            | Version modifiée de SAM-Road intégrant l’encodeur visuel DINOv2 (ViT). |
| `README.md`              | Ce fichier de présentation du projet. |

---

## 🧠 Modèles testés

### 🟦 CNNs :
- `U-Net`
- `U-Net++`
- `AGF-Net`

### 🟩 GNNs :
- `SAM-Road`
- `DINO-Road` (SAM-Road + DINOv2)

---

## 🧪 Jeux de données utilisés

- **DeepGlobe Road Extraction Dataset** (masques binaires)
- **Cityscale Dataset** (annotations topologiques vectorielles)
- **Images satellites haute résolution de la ville de Sfax (Tunisie)**

---

## 📊 Évaluation des performances

Les modèles ont été évalués selon :

- **Métriques géométriques** : IoU, F1-score, Precision, Recall
- **Métriques topologiques** : TOPO, APLS

> Les meilleurs résultats ont été obtenus par `AGF-Net` (segmentation fine) et `DINO-Road` (connectivité topologique).

---

## 💡 Objectifs du projet

- Comparer des modèles CNN et GNN pour la détection de routes.
- Intégrer un foundation model (DINOv2) pour enrichir la représentation visuelle.
- Évaluer les modèles sur des images réelles tunisiennes.
- Proposer un pipeline hybride pour la reconstruction fidèle de graphes routiers.

---

## 🛠️ Technologies utilisées

- Python, PyTorch
- Segmentation Models PyTorch
- OpenCV, Albumentations
- Jupyter Notebooks
- Kaggle GPU Notebooks

---

## 🖼️ Résultats visuels

Des exemples de masques prédits, graphes reconstruits et overlays d’images satellites sont disponibles dans le rapport officiel (voir annexe).


---

## 📣 Auteur

**Chawki RIAHI**  


---

## 📜 Licence

Ce projet est librement consultable à des fins académiques et de recherche. Toute utilisation commerciale est interdite sans autorisation préalable.

