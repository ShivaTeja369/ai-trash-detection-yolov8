# AI Trash Detection using YOLOv8

This project implements a custom-trained **YOLOv8-based trash detection system** to identify **dry leaves and plastic cups** in real-world outdoor environments.

The goal is to enable intelligent waste monitoring and serve as a foundation for autonomous trash-cleaning robots and smart city applications.

---

## Problem
Manual cleaning of public spaces is inefficient and reactive. Trash such as dry leaves and disposable cups often accumulates before action is taken, leading to unhygienic environments and higher maintenance costs.

---

## Solution
A computer vision–based system **designed for real-time trash detection** using a camera and a deep learning model.

The model is trained on a **self-collected and augmented dataset** and can be deployed for:
- Real-time monitoring
- Edge inference on embedded devices
- Integration with autonomous robots

---

## Dataset
- ~796 images (self-collected)
- Classes: `leaf`, `cup`
- Augmentation: horizontal/vertical flips, brightness adjustment
- Preprocessing: auto-orient, resize to **640×640**
- Managed using **Roboflow**

---

## Model
- Architecture: **YOLOv8s**
- Training platform: Roboflow + Ultralytics
- Input resolution: **640×640**
- Best performing version: **Model v5**

Model versions were iteratively improved by expanding the dataset and retraining to enhance generalization.

---

## Performance (Validation Set – Model v5)
- **mAP@50:** 72.6%
- **Precision:** 72.8%
- **Recall:** 66.3%

Earlier model iterations achieved ~60% mAP; performance improved through dataset expansion and retraining.

---

## Live Demo (Roboflow)
Model inference, metrics, and test samples can be viewed here:  
🔗 https://universe.roboflow.com/robot-project-8w8eb/leaf-and-cup-detection-1/model/5

---

## Sample Predictions
Below are sample predictions from the trained model:

### Leaf Detection
![Leaf Detection](inference/sample_outputs/leaves_detection_img2.jpg)

### Cup Detection
![Cup Detection](inference/sample_outputs/cup_detection.jpg)

---

## Applications
- Autonomous trash-collecting robots
- Smart city cleanliness monitoring
- Campus and park maintenance automation

---

## Future Improvements
- Increase dataset diversity and size
- Add more trash categories
- Deploy on Raspberry Pi / Jetson Nano
- Integrate with robotic vacuum or collection mechanisms
- Optimize for low-cost edge deployment in real-world environments

---

## Tech Stack
- Python
- YOLOv8
- Roboflow
- OpenCV

