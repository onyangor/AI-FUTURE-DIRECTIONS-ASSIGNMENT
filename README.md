# ♻️ Edge AI Prototype: Waste Classifier (TFLite)

This project trains a lightweight image classifier using TensorFlow and MobileNetV2, fine-tuned on the Garbage Classification dataset from Kaggle. The model is then converted to TensorFlow Lite for edge deployment.

##  Tools & Frameworks
- TensorFlow 2.x
- TensorFlow Hub
- TensorFlow Lite
- Kaggle API
- Google Colab

##  Dataset
**[Garbage Classification (Kaggle)](https://www.kaggle.com/datasets/asdasdasasdas/garbage-classification)**

Download steps:
1. Go to https://www.kaggle.com/account
2. Create a new API Token
3. Upload `kaggle.json` to Colab
4. Run notebook cells to download and unzip the dataset

##  Model Architecture
- **Base Model**: MobileNetV2 (pretrained on ImageNet, via TensorFlow Hub)
- **Custom Head**: Dense softmax layer for classification
- **Loss**: Sparse Categorical Crossentropy
- **Optimizer**: Adam

##  Edge AI Workflow
1. Load and preprocess dataset
2. Train MobileNetV2 classifier
3. Convert to `.tflite` using `TFLiteConverter`
4. Download the `.tflite` model for deployment

##  Performance
- Trained for 5 epochs
- Validation accuracy: ~80% (depends on hardware and split)

##  Output
- `edge_model.tflite`: Portable TFLite model for mobile or microcontroller deployment

##  Deployment Options
- Raspberry Pi (with TensorFlow Lite runtime)
- Android apps (via TFLite Interpreter)
- Coral Edge TPU devices

---

##  Use Case
Smart recycling bins can use this classifier on low-power devices to automatically detect recyclable materials in real-time — enhancing waste management efficiency at the edge without sending data to the cloud.

---


