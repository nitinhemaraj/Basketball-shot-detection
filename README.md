# AI-basketball-shot-detection
A project with YOLOv8 to detect and analyze basketball shots in real-time. The algorithm tracks the ball's motion, applies data-cleaning techniques, and predicts its trajectory using linear regression to register successful shots when intersecting with the hoop. It enhances playing experience and offers game analytics.

https://github.com/nitinhemaraj/AI-basketball-shot-detection/assets/90787449/2c42261d-0b8b-4a95-a4c1-e67875397c21

## Introduction
This project combines the power of Machine Learning and Computer Vision for the purpose of detecting and analyzing basketball shots in real-time! Built upon the latest YOLOv8 (You Only Look Once) machine learning model and the OpenCV library, the program can process video streams from various sources, such as live webcam feed or pre-recorded videos, providing a tool that can be used for an immersive playing experience and enhanced game analytics.

## Model Training
The training process utilizes the ultralytics YOLO implementation and a custom dataset specified in the 'config.yaml' file. The model undergoes a set number of training epochs, with the resulting weights of the best-performing model saved for subsequent usage in shot detection. Although this model worked for my usage, a different dataset or training method might work better for your specific project.

## Algorithm
The core of this project is an algorithm that uses the trained YOLOv8 model to detect basketballs and hoops in each frame. It then analyzes the motion and position of the basketball relative to the hoop to determine if a shot has been made.

To enhance the accuracy of the shot detection, the algorithm not only tracks the ball's position over time but also applies data-cleaning techniques to both the ball and hoop positions. The algorithm is designed to filter out inaccurate data points, remove points beyond a certain frame limit and prevent jumping from one object to another to maintain the accuracy of the detection.

A linear regression is used to predict the ball's trajectory based on its positions. If the projected trajectory intersects with the hoop, the algorithm registers it as a successful shot.

## How to Use This Code
Clone this repository to your local machine.
Download the dataset specified in 'config.yaml' and adjust the paths in the configuration file to match your local setup.
Follow the instructions in 'main.py' to train the model and prepare for shot detection.
Run 'shot_detector.py' through your webcam or iPhone for real-time shot detection. Or input a video for shot detection analysis.
Please ensure you have the required Python packages installed, including OpenCV, numpy, and ultralytics' YOLO.

### Score Detection Accuracy: 95%
### Shot Detection Accuracy: 97%
