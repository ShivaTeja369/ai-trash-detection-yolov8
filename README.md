# AI Trash Detection using YOLOv8

This project implements an AI-based trash detection system using a custom-trained YOLOv8 model to detect **leaves and plastic cups** in real-world outdoor environments.

## Problem
Manual cleaning of public spaces is inefficient and reactive. Trash like dry leaves and disposable cups often accumulates before action is taken.

## Solution
A computer vision–based system that detects trash in real time using a camera and a deep learning model, enabling autonomous or assisted cleanup.

## Dataset
- Manually collected ~300 images
- Classes: `leaf`, `cup`
- Augmented using Roboflow (flips, brightness)
- Auto-orient and resized to 640×640

## Model
- Architecture: YOLOv8
- Training platform: Roboflow + Ultralytics
- Input size: 640×640

## Performance (Validation Set)
- **mAP@50:** 72.6%
- **Precision:** 72.8%
- **Recall:** 66.3%

## Sample Predictions
*(Add sample prediction images here)*

## Applications
- Autonomous trash-collecting robots
- Smart city cleanliness monitoring
- Campus and park maintenance automation

## Future Improvements
- Increase dataset diversity
- Add more trash categories
- Deploy on Raspberry Pi / Jetson Nano
- Integrate with robotic vacuum system

## Tech Stack
- Python
- YOLOv8
- Roboflow
- OpenCV
