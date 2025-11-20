# ⚽ Football AI – YOLOv8 Detection Project

This repository contains the **Football AI project**, which focuses on detecting **players, referees, and balls**, as well as identifying **pitch keypoints** using **YOLOv8**.  
The project was trained and deployed using **Google Colab**, **Kaggle GPUs**, and **Roboflow** integration.

---

##  Project Overview

This AI system aims to analyze football videos by:
- Detecting **players**, **referees**, and **balls** in the field.
- Extracting **pitch keypoints** for camera calibration and tactical visualization.
- Enabling future tasks like player tracking, team formation analysis, and event detection.




##  Google Colab Notebook  
To view the full code with outputs, run or edit the notebook directly in Google Colab:

➡️ **Open in Google Colab:**  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1W9c71_TYUJc0-MjhrRP1LymfZNRUZiDW?usp=sharing)




## Models

### 1. Ball, Players, and Referees Detection  
**Model:** YOLOv8 (Kaggle – GPU T4 x2)

- **View Deployment Status:** [Roboflow App Link](https://app.roboflow.com/tonyphamnp/football-players-detection-3zvbc-kerdk/2)  
- **Public Model Page:** [Roboflow Universe](https://universe.roboflow.com/tonyphamnp/football-players-detection-3zvbc-kerdk/model/2)

### 2. Pitch Keypoints Detection  
**Model:** YOLOv8 (Google Colab – GPU T4 x2)

- **View Deployment Status:** [Roboflow App Link](https://app.roboflow.com/tonyphamnp/football-field-detection-f07vi-okdo7/1)  
- **Public Model Page:** [Roboflow Universe](https://universe.roboflow.com/tonyphamnp/football-field-detection-f07vi-okdo7/model/1)


##  Dataset

Both datasets were collected and annotated via **Roboflow**.

| Dataset | Description | Source |
|----------|--------------|--------|
| `football-players-detection` | Includes images with bounding boxes for **players**, **referees**, and **balls** | [![Roboflow Dataset](https://img.shields.io/badge/Roboflow-Dataset-purple?logo=roboflow&logoColor=white)](https://app.roboflow.com/tonyphamnp/football-players-detection-3zvbc)
| `football-field-detection` | Includes images labeled with **keypoints** of the football pitch (lines, corners, center, etc.) | [![Roboflow Dataset](https://img.shields.io/badge/Roboflow-Dataset-purple?logo=roboflow&logoColor=white)](https://app.roboflow.com/tonyphamnp/football-field-detection-f07vi) |

##  Training

The models were trained with:
- **Framework:** Ultralytics YOLOv8
- **Environment:** Google Colab + Kaggle (GPU T4 x2)
- **Training Epochs:** 100
- **Batch Size:** 16
- **Optimizer:** AdamW
- **Image Size:** 640x640

Example command:
```python
!yolo detect train data=data.yaml model=yolov8m.pt epochs=100 imgsz=640 batch=16

