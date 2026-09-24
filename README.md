# OrthoLens AI — Bone X-ray Analysis

OrthoLens AI is a computer-vision project for exploring bone X-ray analysis through object detection, image visualization, and a browser-based interface.

The project connects a trained YOLO model with a FastAPI backend and a lightweight frontend to create an end-to-end X-ray analysis workflow.

> **Purpose:** Research, education, experimentation, and project demonstration.  
> OrthoLens AI is not a clinical diagnostic system.

## Live Demo

**https://ortholensai-bone-x-ray-analysis.onrender.com**

## What the project does

OrthoLens AI allows a user to:

- Upload a JPG or PNG bone X-ray
- Send the image to a FastAPI backend
- Run the trained YOLO detection model
- View detected regions and confidence values
- Compare the original X-ray with the model's annotated output
- Inspect a heatmap-style visual explanation when detections are available

## Current model classes

The current trained model exposes these labels:

- Elbow positive
- Fingers positive
- Forearm fracture
- Humerus
- Humerus fracture
- Shoulder fracture
- Wrist positive

## Project workflow

```text
X-ray Image
     ↓
Browser Upload
     ↓
FastAPI Backend
     ↓
YOLO Model Inference
     ↓
Detected Regions
     ↓
Confidence + Bounding Boxes
     ↓
Annotated Result
     ↓
Visual Explanation

```
##
## Technology Stack

## Machine Learning
Python,
PyTorch,
Ultralytics YOLO

## Backend
FastAPI,
Uvicorn,
Python Multipart,
Pillow,
OpenCV,
NumPy,
Matplotlib

## Frontend
HTML5,
CSS3,
JavaScript,
Font Awesome,
Google Fonts

## Deployment
Render

## Project Structure

```text
OrthoLensAI-Bone-X-ray-Analysis/
│
├── backend/
│   ├── app.py
│   └── models/
│       └── model.pt
│
├── frontend/
│   ├── index.html
│   ├── about.html
│   ├── features.html
│   ├── detect.html
│   ├── detect-script.js
│   ├── gradcam.html
│   ├── project.html
│   ├── nav-template.html
│   ├── nav-handler.js
│   ├── footer-template.html
│   ├── footer-handler.js
│   ├── footer-styles.css
│   ├── styles.css
│   └── images/
│
├── .python-version
├── .gitignore
├── LICENSE
├── requirements.txt
└── README.md
```

# Important limitations

## Dataset-dependent performance

The model was trained on a specific X-ray dataset, so performance can vary when images differ substantially from the training data in anatomy, positioning, image quality, or acquisition style.

## Not a medical diagnostic tool

Model predictions are provided for research, education, and demonstration purposes. They should not be used as a substitute for professional medical interpretation.

## Visual explanation

The current project includes a heatmap-style visual explanation generated from detected regions. It should not be described as a verified gradient-based Grad-CAM implementation.

# Future development

## Potential improvements include:

Evaluation across additional X-ray datasets
More structured model validation and performance metrics
Improved generalization to different image distributions
Better explainability methods
More robust deployment architecture
Expanded experimentation with fracture detection models

# Project

OrthoLens AI was developed as an exploration of how machine learning, computer vision, backend APIs, and web interfaces can be combined into a single working application.

## The project focuses on making the complete workflow understandable:

image → inference → detection → visualization → user interface

# Disclaimer

OrthoLens AI is an educational and research-oriented software project. Its outputs are not intended for clinical diagnosis, treatment decisions, or emergency medical use.
