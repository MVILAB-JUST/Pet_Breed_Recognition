A fine-grained image classification project for dog and cat breed recognition using a GCViT-Tiny backbone with a dual-path gated fusion architecture.
This work focuses on improving breed classification performance by combining:
•	Global feature representation
•	Part-aware local feature extraction
•	Adaptive gated feature fusion

Overview
Fine-grained visual classification (FGVC) is challenging because many breeds have very subtle visual differences while showing large intra-class variations.
To address this problem, this project introduces a hybrid architecture built on GCViT-Tiny that extracts both:
•	Global semantic features
•	Local discriminative part features
A gating mechanism dynamically fuses these representations for better breed prediction performance.

Architecture
The proposed architecture consists of:
Input Image
      │
      ▼
Pre-Processing
      │
      ▼
GCViT-Tiny Backbone
      │
      ▼
Feature Token Map
      │
 ┌────┴────┐
 ▼         ▼
Mean Pool  Max Pool
(Global)   (Part)
 │           │
 ▼           ▼
Global      Part
Feature     Feature
 │           │
Global FC   Part FC
 └────┬─────┘
      ▼
Shared Projection Layer
      │
      ▼
Gating Mechanism (α)
      │
      ▼
Gated Fusion
      │
      ▼
Breed Prediction

Key Features
•	GCViT-Tiny transformer backbone
•	Dual-branch feature extraction
•	Global + part-aware representation learning
•	Adaptive gated fusion mechanism
•	Fine-grained breed classification
•	Early stopping support
•	Training visualization
•	Confusion matrix analysis
•	Google Colab compatible

Dataset
This project uses the:
•	Oxford-IIIT Pet Dataset
Dataset Details
•	37 total breeds
•	25 dog breeds
•	12 cat breeds
•	Around 200 images per breed

Technologies Used
•	Python
•	PyTorch
•	timm
•	NumPy
•	Matplotlib
•	Scikit-learn
•	OpenCV
•	Google Colab
Evaluation Metrics
The model is evaluated using:
•	Accuracy
•	Precision
•	Recall
•	F1-score
•	Confusion Matrix
•	Per-class accuracy

Results
Model	Dataset	Accuracy
GCViT-Tiny + Gated Fusion	Oxford-IIIT Pet	94.47

Visualizations
The project includes:
•	Accuracy vs Epoch curves
•	Loss vs Epoch curves
•	Confusion matrices
•	Best & worst classified breeds analysis

Future Work
•	Attention map visualization
•	Grad-CAM explainability
•	Multi-scale feature fusion
•	Ensemble learning
•	Comparison with ViT and Swin Transformer

Acknowledgements
•	GCViT authors
•	Oxford-IIIT Pet Dataset creators
•	PyTorch community
•	timm library contributors
Author
Mowmita Parvin Hera
B.Sc. in Mathematics
Jashore University of Scienc
