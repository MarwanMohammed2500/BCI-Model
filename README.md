# Brain–Computer Interface (BCI) Project
## Overview

This project explores non-invasive Brain–Computer Interfaces (BCIs) through EEG signal classification. The focus lies on two key paradigms — **SSVEP (Steady-State Visual Evoked Potentials)** and **MI (Motor Imagery)** — to understand and compare how neural signals can be translated into machine-interpretable commands.

The implementation builds on classical machine learning and deep learning methods, emphasizing reproducibility and clarity rather than black-box automation.

---
## Objectives

* Decode brain signals for real-time intent recognition.
* Compare **SSVEP** and **MI** paradigms in classification accuracy and signal robustness.
* Evaluate classical ML vs. deep learning pipelines under the same data and preprocessing conditions.

---
## Key Components

### EEG Paradigms

* **SSVEP** — frequency-tagged visual stimuli to classify directional intent.
* **MI** — imagination of motor movements (left/right hand) for intent inference.

### Pipeline

1. **Preprocessing**: band-pass filtering (7–30 Hz), artifact removal, normalization.
2. **Feature Extraction**: Power Spectral Density (Welch) and optionally FBCCA.
3. **Modeling**:

   * Classical ML — Random Forest, XGBoost.
   * Deep Learning — PyTorch CNN-based model (custom, device-agnostic).
4. **Evaluation**: per-subject accuracy, confusion matrices, comparative plots.

---
## Results (Highlights)
* Classical ML performed competitively on smaller samples due to reduced variance.
* Deep learning showed higher stability with longer trial durations and richer frequency content.
* SSVEP yielded consistently better signal-to-noise ratios compared to MI.

*(See the notebook for plots and per-trial metrics.)*

---
## Future Work

* Incorporate **FBCCA** for enhanced SSVEP feature extraction.
* Extend MI classification with **Riemannian geometry-based features**.
* Explore real-time streaming for external device control.
