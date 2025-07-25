Keratoconus Detection using Deep Learning (ResNet50)
This repository contains the implementation of a deep learning-based classification model for detecting Keratoconus, Suspect, and Normal cases from corneal topography maps using a ResNet50 architecture. The project was developed as part of the coursework for COS7053-B: Advanced Topics in AI and Digital Healthcare at the University of Bradford.

📌 Project Overview
Keratoconus is an eye disease that affects the shape of the cornea and degrades vision quality. Traditional diagnosis is time-consuming and requires expert ophthalmologists. This project proposes an automated, AI-powered solution using corneal images and a transfer-learning approach to classify eyes into:

Keratoconus

Suspect (Borderline)

Normal

🧠 Model Summary
Base Model: ResNet50 (pretrained on ImageNet)

Architecture Modifications:

Frozen early layers

Fine-tuned last 50 layers

Added regularization (L1/L2), dropout, and batch normalization

Training Details:

Image size: 224×224

Batch size: 32

Early stopping and model checkpointing

Augmentation applied especially to underrepresented “Suspect” class

🗂️ Dataset
Source: Kaggle - Keratoconus Detection Dataset

Classes: Keratoconus, Suspect, Normal

Distribution:

Train: 2,115 images (balanced using augmentation)

Validation: 885 images

Test: 1,050 images

📊 Results
Metric	Training Set	Validation Set	Test Set
Accuracy	81.66%	78.55%	59.05%


Confusion Matrix (Validation Set)
The model performs best on Keratoconus and Normal classes, with more confusion on Suspect due to overlapping features.

ROC Curve
Plotted using one-vs-rest approach; the Keratoconus class had the highest area under the curve (AUC).

📈 Training Curves
(if available)

🔁 Data Augmentation
To handle class imbalance for the Suspect class:

Horizontal flips

Random rotations

Zoom and shift

🧪 Evaluation
Metrics: Accuracy, F1-score, Confusion Matrix, ROC-AUC

Tools: TensorFlow, Keras, NumPy, Matplotlib

🔍 Key Insights
The model successfully classifies Keratoconus cases with high accuracy.

Suspect class remains challenging due to its visual overlap with Normal/Keratoconus.

Shows strong potential for aiding early diagnosis in clinical settings.

🛠️ Future Work
Incorporate explainable AI tools (e.g., Grad-CAM)

Enhance data diversity, especially for suspect cases

Experiment with attention mechanisms and ensemble models

Deploy a prototype in a clinical decision support system (CDSS)

📚 References
Dataset: Kaggle - Keratoconus Detection

Chen et al., 2021: BMJ Open Ophthalmology

Lavric and Valentin, 2019: KeratoDetect

Lin et al., 2019: Review of ML Techniques

👤 Author
Abdul Rafay Hussain


