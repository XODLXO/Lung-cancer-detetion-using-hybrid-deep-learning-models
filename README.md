# Lung-cancer-detetion-using-hybrid-deep-learning-models
Project Title
Hybrid VGG16-InceptionV3 Architecture for Lung Cancer Diagnosis from Histopathological Tissue Images

Overview
This project explores a deep learning approach for the multi-class classification of lung cancer subtypes using histopathological tissue images. By integrating the strengths of two proven architectures—VGG16 and InceptionV3—at the feature representation level, the model achieves superior accuracy and interpretability over standalone CNNs. It aims to support clinical diagnostics by offering high precision and transparent visual explanations.

Motivation
Lung cancer is the leading cause of cancer-related deaths globally, and early, reliable detection is crucial. Manual annotation of histopathological images is labor-intensive and subjective. The proposed hybrid model demonstrates that combining CNN architectures can capture both fine-grained textures and complex spatial patterns—critical for robust classification of lung tissue abnormalities.

Literature Insight
Previous works employed architectures like ResNet50, DenseNet, MobileNet, and standalone VGG16 or InceptionV3. While promising, these models struggled with precision, generalizability, or interpretability. This project builds upon existing methodologies by leveraging feature fusion between two networks to improve diagnostic accuracy and address performance inconsistencies noted in prior research.

Dataset
The model was trained on the Lung Cancer Histopathological Images dataset, containing image samples from three classes:

Benign Lung Tissue

Adenocarcinoma

Squamous Cell Carcinoma

Images are resized to 224 × 224 × 3 RGB format and processed with class balancing and data augmentation to ensure robust training performance.

🏗Methodology
The hybrid architecture extracts features simultaneously using:

VGG16 for capturing fine textures

InceptionV3 for multi-scale spatial representation

Feature-level fusion merges the 512-dimensional VGG16 output and 2048-dimensional InceptionV3 output into a 2560-dimensional vector. Dropout layers and dense layers are used for regularization and pattern learning. The final softmax output layer predicts probabilities for the three cancer classes.

Interpretability
Grad-CAM visualizations are employed to produce heatmaps indicating which regions of the image influenced the model’s predictions. This provides clinical interpretability, bridging the gap between AI decisions and human trust.

Results
Performance on the test set includes:

Accuracy: 95.89%

Precision, Recall, F1 Score: 95.88% across all classes

The proposed model outperforms ResNet50 (accuracy: 33.78%, F1: 19.73%) and achieves more balanced metrics than MobileNet, DenseNet, and InceptionV3, which struggle with class-wise performance despite decent overall accuracy.
