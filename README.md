# Deepfake Detection avec CNN

Projet de détection de deepfakes utilisant des réseaux de neurones convolutifs (CNN) sur le dataset DFD (Deep Fake Detection).

## Dataset

**Source:** Deep Fake Detection DFD Dataset
**Composition:**
- 300 vidéos réelles (DFD_original_sequences)
- 300 vidéos manipulées (DFD_manipulated_sequences)
- Total: 600 vidéos

**Prétraitement:**
- Extraction de 10 frames par vidéo
- Résolution: 128x128 pixels
- Format: RGB
- Total frames générées: 6000 (3000 réelles + 3000 fake)

## Structure du projet
```
forensics-dataset/
├── data extraction
│   └── Extraction frames des vidéos
├── preprocessing
│   └── Normalisation et split train/val/test
└── model training
    └── ResNet50 avec transfer learning
```

## Méthode

**Extraction des frames:**
- 10 frames équidistantes par vidéo
- Resize automatique en 128x128
- Conservation du ratio RGB

**Architecture prévue:**
- Base: ResNet50 pré-entrainée (ImageNet)
- Classification binaire (real vs fake)
- Optimiseur: Adam
- Loss: Binary crossentropy

## Progression

- [x] Import des packages
- [x] Extraction des frames (600 vidéos, 6000 frames)
- [ ] Normalisation des données
- [ ] Split train/validation/test
- [ ] Construction du modèle
- [ ] Entrainement
- [ ] Évaluation
- [ ] Interface de démonstration

## Environnement

**Plateforme:** Kaggle Notebook
**Packages:**
- TensorFlow/Keras
- OpenCV
- NumPy
- scikit-learn
- tqdm

## Prochaines étapes

1. Normaliser les frames (division par 255)
2. Split 70/15/15 (train/val/test)
3. Data augmentation (rotation, flip, brightness)
4. Entrainer ResNet50 avec frozen layers
5. Fine-tuning des dernières couches
6. Évaluation sur test set

## Objectif

Atteindre 85%+ de précision sur la détection de deepfakes avec un modèle déployable.

---

**Date:** Octobre 2025
**Status:** En cours de développement
