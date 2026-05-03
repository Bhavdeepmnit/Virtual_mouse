# 🖱️ Virtual Mouse via Hand Gestures

A computer vision-based application that allows users to control their computer mouse pointer and perform clicks using simple hand gestures. This project leverages the power of deep learning and computer vision to create a touchless interface.

## ✨ Features

- **Real-Time Hand Tracking**: Uses Google's MediaPipe framework for precise, real-time tracking of hand landmarks.
- **Gesture Recognition**: Employs a trained Support Vector Machine (SVM) classifier to recognize specific gestures.
- **Mouse Control**: Maps hand movements to screen coordinates and translates gestures into mouse clicks using PyAutoGUI.
- **Custom Data Collection**: Includes a pipeline (`project.ipynb`) for collecting your own hand gesture data to train custom models.

## 🛠️ Tech Stack

- **Language**: Python 3
- **Computer Vision**: OpenCV (`cv2`), MediaPipe
- **Machine Learning**: Scikit-learn (SVM/SVC), NumPy
- **Automation**: PyAutoGUI

## 🚀 How It Works

1. **Hand Landmark Detection**: The webcam captures video feed, and MediaPipe extracts 21 3D landmarks for the hand in the frame.
2. **Feature Extraction**: Landmark coordinates are processed and flattened into a feature vector.
3. **Classification**: The pre-trained SVM model classifies the feature vector into a recognized gesture (e.g., Open Palm, Closed Fist, Peace Sign).
4. **Execution**: Based on the recognized gesture and the position of the index finger, PyAutoGUI moves the cursor or performs left/right clicks.

## 📥 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Bhavdeepmnit/Virtual_mouse.git
   cd Virtual_mouse
   ```

2. **Create a Virtual Environment** (Recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install opencv-python mediapipe pyautogui scikit-learn numpy jupyter
   ```

## 💻 Usage

### Running the Application
Execute the main Python script to start the virtual mouse:
```bash
python main.py
```
*(Ensure your webcam is not being used by another application)*

### Training a Custom Model
If you want to train the model on your own hand gestures:
1. Open the Jupyter Notebook: `jupyter notebook project.ipynb`
2. Follow the cells to:
   - Capture frames and save landmark data.
   - Assign labels to your custom gestures.
   - Train the Support Vector Classifier (SVC).
   - Save the trained model (`.pkl` file) for use in the main script.

## 👨‍💻 Author

**Bhavdeep**
- GitHub: [Bhavdeepmnit](https://github.com/Bhavdeepmnit)
- Portfolio: [bhavdeepmnit.vercel.app](https://bhavdeepmnit.vercel.app)