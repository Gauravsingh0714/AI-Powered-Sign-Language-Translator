# AI-Powered Sign Language Translator 🤟🤖

An interactive computer vision application that detects hand gestures in real-time using a webcam and translates them into sign language text/labels. Built using OpenCV, `cvzone` (Hand Tracking), and a pre-trained Keras Deep Learning classification model.

---

## ✨ Features

- **Real-Time Hand Tracking:** Detects and tracks hands with high precision.
- **Dynamic Image Cropping:** Automatically crops the hand region with a specified offset and places it on a standardized white canvas.
- **Keras Classification Model:** Translates hand gestures in real-time to text labels (e.g., "Hello", "I love you", "Thank you", "A").
- **Visual Feedback:** Displays bounding boxes, tracking outputs, and overlay text directly on the camera feed.
- **Data Collection Script:** Included script to capture training images for adding new gestures to the model.

---

## 🛠️ Tech Stack & Dependencies

- **Language:** Python 3.x
- **Computer Vision:** OpenCV (`opencv-python`)
- **Hand Tracking & Utilities:** `cvzone`
- **Numerical Processing:** NumPy
- **Deep Learning / Classification:** TensorFlow / Keras (for loading the pre-trained `.h5` model)

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/AI-Powered-Sign-Language-Translator.git
cd AI-Powered-Sign-Language-Translator
```

### 2. Install Dependencies
Make sure you have python installed, then run:
```bash
pip install opencv-python cvzone tensorflow numpy
```

### 3. Setup Your Pre-trained Model
Ensure you have your pre-trained Keras model (`keras_model.h5`) and classification labels (`labels.txt`) in your local directories, and update their paths in `test.py`:
```python
classifier = Classifier("path/to/keras_model.h5", "path/to/labels.txt")
```

### 4. Run the Application
To start the real-time translator:
```bash
python test.py
```

To run the data collector for training new gestures:
```bash
python datacollection.py
```

---

## 📂 Project Structure

- `test.py`: The main testing and live execution script for real-time translation.
- `datacollection.py`: Utility script to collect and save gesture crop images for training.
- `.gitignore`: Standard rules to keep unnecessary local configurations and caches out of the repository.
- `README.md`: Project documentation.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page or submit pull requests.

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
