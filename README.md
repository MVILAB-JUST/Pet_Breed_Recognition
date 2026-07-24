# DP-GCViT: Dual-Path Global Context Vision Transformer for Fine-Grained Pet Breed Recognition

A fine-grained visual classification (FGVC) framework for dog and cat breed recognition based on a **Global Context Vision Transformer (GCViT-Tiny)** with a **Dual-Path architecture** and a **parameter-free adaptive confidence-based fusion mechanism**.

The proposed **DP-GCViT** enhances breed recognition by combining complementary global and local visual representations through confidence-based prediction fusion while maintaining a lightweight architecture without auxiliary localization networks or saliency detection modules.

---

# Overview

Fine-grained visual classification (FGVC) is a challenging computer vision task because different breeds often exhibit subtle inter-class differences while simultaneously presenting large intra-class variations caused by pose, illumination, occlusion, background clutter, and appearance diversity.

To address these challenges, **DP-GCViT** extends the GCViT-Tiny backbone by introducing two complementary prediction branches:

- **Global Path**, capturing holistic semantic information using Global Average Pooling.
- **Local Salient Path**, emphasizing highly discriminative local regions through Global Max Pooling.

Instead of relying on explicit part localization, saliency estimation, or attention-guided cropping, the proposed framework employs a **parameter-free adaptive confidence-based fusion mechanism**, which dynamically combines the predictions of the two branches according to their confidence scores.

---

# Architecture

```text
                    Input Image
                         │
                         ▼
                  Image Pre-processing
                         │
                         ▼
                GCViT-Tiny Backbone
                         │
                         ▼
                Shared Feature Map
                  ┌──────────────┐
                  │              │
                  ▼              ▼
         Global Average Pool   Global Max Pool
          (Global Path)      (Local Salient Path)
                  │              │
                  ▼              ▼
           Global Feature    Local Feature
                  │              │
                  ▼              ▼
          Global Classifier  Local Classifier
                  │              │
                  └──────┬───────┘
                         ▼
           Adaptive Confidence Computation
                         │
                         ▼
      Parameter-Free Confidence-Based Fusion
                         │
                         ▼
                Final Breed Prediction
```

---

# Key Features

- GCViT-Tiny transformer backbone
- Dual-path feature learning
- Global semantic representation
- Local salient feature representation
- Parameter-free adaptive confidence-based fusion
- End-to-end fine-grained breed classification
- Lightweight architecture without auxiliary localization networks
- Extensive evaluation on multiple FGVC benchmarks
- Grad-CAM visualization for model interpretability
- Fully reproducible PyTorch implementation

---

# Datasets

## Oxford-IIIT Pet Dataset

- **37** pet breeds
- **25** dog breeds
- **12** cat breeds
- **7,349** RGB images

## Stanford Dogs Dataset

- **120** dog breeds
- **20,580** RGB images

---

# Technologies Used

- Python
- PyTorch
- timm
- torchvision
- NumPy
- OpenCV
- Matplotlib
- Scikit-learn
- Google Colab

---

# Evaluation Metrics

The proposed model is evaluated using:

- Top-1 Accuracy
- Top-5 Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curve
- Area Under the Curve (AUC)
- Per-class Performance Analysis

---

# Experimental Results

| Model | Dataset | Test Accuracy |
|-------|---------|--------------:|
| **DP-GCViT** | Oxford-IIIT Pet | **95.26%** |
| **DP-GCViT** | Stanford Dogs | **93.25%** |

The proposed **DP-GCViT** achieves state-of-the-art performance while maintaining a lightweight architecture without requiring explicit part localization, saliency detection, multi-view cropping, or auxiliary attention modules.

---

# Visualizations

The repository includes:

- Training and validation accuracy curves
- Training and validation loss curves
- Confusion matrices
- ROC curves
- Grad-CAM visualizations
- Best and worst classified breed analysis
- Comparative model performance analysis

---

# Future Work

Future research directions include:

- Controllable generative AI for attribute-aware data augmentation
- Privacy-preserving edge deployment through model quantization and pruning
- Multi-scale feature learning
- Lightweight model compression
- Real-time mobile deployment
- Extension to broader fine-grained visual recognition tasks

---

# Citation

If you use this work, please cite:

```bibtex
@article{hera2026dpgcvit,
  title={DP-GCViT: Dual-Path Global Context Vision Transformer for Fine-Grained Pet Breed Recognition},
  author={Mowmita Parvin Hera and others},
  journal={Under Review},
  year={2026}
}
```

---

# Acknowledgements

We gratefully acknowledge:

- GCViT authors
- Oxford-IIIT Pet Dataset creators
- Stanford Dogs Dataset creators
- PyTorch community
- timm library contributors

---

# Author

**Mowmita Parvin Hera**

B.Sc. in Mathematics  
Jashore University of Science and Technology (JUST)

**Research Interests**

- Computer Vision
- Deep Learning
- Fine-Grained Visual Classification
- Vision Transformers
- Explainable AI
