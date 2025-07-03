🛠️ Corrosion Detection using YOLOv5 🚧

This project is part of my Summer Research Internship and aims to develop a deep learning-based system for detecting corrosion on metal surfaces using the YOLOv5 object detection model.

🚀 Project Overview
Goal:
To build an AI tool that can automatically detect corrosion in industrial images to assist in preventive maintenance and inspection.

Technique Used:
YOLOv5 (You Only Look Once) object detection algorithm, fine-tuned on a labeled corrosion dataset.

Application:
Industrial inspection, infrastructure monitoring, non-destructive testing, preventive maintenance.

🔍 How It Works
YOLOv5 takes an image as input and outputs bounding boxes around detected corrosion spots.
The model has been trained to detect corrosion based on features like color patterns, texture, and surface damage.
Non-Max Suppression (NMS) is used to eliminate overlapping predictions for clean and accurate results.
The model was trained and tested on a public corrosion detection dataset available on Roboflow.

💾 Dataset Used
Name: Corrosion Instance Segmentation
Source: Roboflow Dataset
Size: 1000+ annotated images in COCO format with bounding boxes for corrosion areas.
Classes: Corrosion

💻 How I Did It
Used YOLOv5 for object detection (PyTorch-based implementation).
Trained and tested the model on Google Colab using a custom corrosion dataset.
Converted the model to TorchScript format (best.torchscript) for cross-platform compatibility and deployment.
Final project tested on local system using Visual Studio Code + Python virtual environment.

▶️ How To Run The Project (Windows)
Step 1: Open Terminal and Set Up Environment
cd corrosion_yolov5\yolov5
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt

Step 2: Run Detection
python detect.py --weights best.torchscript --img 640 --conf 0.3 --source Corrosion-Instance-Segmentation-1/test/images

Output images with bounding boxes will be saved in the runs/detect/exp/ folder.

📸 Example Use Cases
Detect corrosion in real-time from drone footage or inspection cameras.
Automate defect tracking in oil, gas, marine, or industrial assets.
Help maintenance teams prioritize inspections using AI.