# Brain_Tumor_Detection
# 🧠 Brain Tumor Detection Using CNN

This project uses a Convolutional Neural Network (CNN) to detect brain tumors from MRI scan images.

---

## 📂 Dataset

The dataset is structured into folders:

- All images are resized to *240x240* pixels.
- Labels:
  - 0 → No tumor
  - 1 → Tumor present

---

## 🔄 Image Preprocessing

- Image resizing to (240, 240, 3)
- Normalization to [0, 1]
- Label encoding
- Dataset split: *80% train, **20% test*

---

## 🧠 Model Architecture

Built using TensorFlow/Keras. The CNN consists of:

- 3 Convolutional + MaxPooling2D layers
- 1 Flatten layer
- 1 Dense layer with Dropout
- 1 Output Dense layer (sigmoid activation)

### Model Summary


---

## ⚙ Training

- Optimizer: adam
- Loss: binary_crossentropy
- Metrics: accuracy
- Epochs: 15
- Validation split: 20%

---

## ✅ Evaluation

After training, the model is evaluated using:

- ✅ Accuracy
- 📊 Classification Report (Precision, Recall, F1-score)
- 📉 Confusion Matrix

---

## 💾 Model Saving/Loading

```python
# Save the trained model
model.save("brain_tumor_model.h5")

# Load the model later
from tensorflow.keras.models import load_model
model = load_model("brain_tumor_model.h5")

pip install tensorflow numpy matplotlib scikit-learn opencv-python
