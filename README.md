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
