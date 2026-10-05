#  Real-Time Fire Detection System

A deep learning-based computer vision application that detects fire in real-time using a web camera. The project implements transfer learning with **MobileNetV2** for highly efficient, lightweight, and accurate predictions, making it suitable for deployment on edge devices.

---

##  Key Features

*   **Real-Time Detection:** Live webcam feed processing with low-latency predictions.
*   **Deep Learning Backbone:** Built on top of **MobileNetV2** (pre-trained on ImageNet) for rapid and robust feature extraction.
*   **Visual Alert System:** Dynamic UI overlays displaying a red bounding box and warning text when fire is detected, and a green box when safe.
*   **End-to-End Notebook:** Includes `Fire_Detection.ipynb` detailing dataset preprocessing, training history plotting, and detailed evaluation metrics.

---

##  Project Structure

```text
├── Fire_dataset/          # Local dataset containing Fire & Non_Fire images
├── Fire_Detection.ipynb   # Jupyter Notebook for model training & evaluation
├── app.py                 # Main real-time webcam inference script
├── fire_detection_model.h5# Saved TensorFlow model weights
├── requirements.txt       # Python dependencies list
└── README.md              # Project documentation
```

---

##  Tech Stack & Libraries

*   **Deep Learning:** TensorFlow 2.x, Keras
*   **Computer Vision:** OpenCV (for webcam capture and UI overlays)
*   **Data Analysis:** NumPy, Pillow, Scikit-learn
*   **Visualization:** Matplotlib

---

##  Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Eng-younesAsaad/fire-detection-system-main.git
cd fire-detection-system-main
```

### 2. Install Dependencies
Make sure you have Python 3.8+ installed. Install the required Python packages using:
```bash
pip install -r requirements.txt
```

### 3. Run Real-Time Detection
Run the main script to start the webcam feed and begin real-time fire detection:
```bash
python app.py
```
*   **Exit the app:** Press `q` while focused on the video window.

---

##  Model Training & Performance

The model was trained using **Transfer Learning** on the MobileNetV2 architecture to keep it lightweight.

### Dataset Details
*   **Binary Classes:** Fire (1) and Non-Fire (0)
*   **Split:** 80% Training, 10% Validation, 10% Testing
*   **Augmentation:** Horizontal flips, rotation, and width/height shifts to avoid overfitting.

### Metrics & Results
The model achieves high accuracy and recall. The training pipeline computes:
*   **Confusion Matrix**
*   **Precision, Recall (Sensitivity), and F1-Score**
*   **Misclassified Samples Analysis**

To retrain the model or inspect training plots, run all cells in [Fire_Detection.ipynb](Fire_Detection.ipynb).

---

## 🤝 Contributing
Contributions are welcome! If you have suggestions to improve the model accuracy or add new features (such as SMS/Email alerting systems), feel free to open an issue or submit a pull request.
