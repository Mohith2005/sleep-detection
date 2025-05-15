# 💤 Drowsiness Detection System 😴🚗

## 🔍 Project Overview

The **Drowsiness Detection System** is an intelligent, real-time computer vision application designed to monitor driver fatigue and alert them before a potential microsleep episode occurs. Built with Python, OpenCV, Dlib, and SciPy, this solution enhances road safety by analyzing eye behavior to detect signs of drowsiness. When the driver's eyes remain closed beyond a safe threshold, the system triggers an audible alarm using `pygame`.

---

## 🛠️ Key Technologies Used

* 🎥 **OpenCV**: For video capturing and frame processing
* 🧠 **Dlib + shape\_predictor\_68\_face\_landmarks.dat**: For accurate facial landmark detection
* 📐 **SciPy**: To calculate the Eye Aspect Ratio (EAR)
* 🔊 **Pygame Mixer**: For real-time alarm audio playback
* 🧰 **imutils**: For easy image manipulation

---

## 🔬 How It Works

1. **Live Feed Acquisition** 📹: Captures video input from the webcam.
2. **Facial Detection** 🧑‍💻: Dlib detects facial structures.
3. **Eye Aspect Ratio (EAR) Calculation** 👁️: Determines eye openness using six key facial landmarks.
4. **Drowsiness Thresholding** ⚠️: If EAR < 0.25 for 20 consecutive frames, it indicates probable drowsiness.
5. **Alert System** 🚨: Triggers a visual and audible alert to wake up the driver.

---

## 📈 EAR Formula

$$
EAR = \frac{||p_2 - p_6|| + ||p_3 - p_5||}{2 \cdot ||p_1 - p_4||}
$$

Where $p_1$ to $p_6$ are the landmark points around the eye.

---

## 📁 File Structure

```
📂 Drowsiness_Detection/
├── Drowsiness_Detection.py   # Main detection script
├── shape_predictor_68_face_landmarks.dat  # Pre-trained facial landmark model
└── music.wav                 # Alarm sound file
```

---

## 🧪 Prerequisites

* Python 3.x
* `opencv-python`
* `dlib`
* `pygame`
* `imutils`
* `scipy`

Install dependencies:

```bash
pip install opencv-python dlib pygame imutils scipy
```

---

## ▶️ How to Run

1. Ensure `shape_predictor_68_face_landmarks.dat` and `music.wav` are in the same directory.
2. Run the script:

```bash
python Drowsiness_Detection.py
```

3. Press **'q'** to quit the application.

---

## 🚀 Future Enhancements

* Add **head pose estimation** to increase robustness.
* Implement **mobile deployment** using TensorFlow Lite.
* Use **deep learning models** like CNNs for improved accuracy.
* Integrate **cloud alert systems** for fleet safety management.

---

## ⚠️ Disclaimer

This project is intended for **academic and prototype purposes only**. It should not replace certified commercial drowsiness detection systems in critical applications.

