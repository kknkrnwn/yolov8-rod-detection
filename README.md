# 🚀 Obstacle Detection Using YOLOv8 on ROD Dataset

A computer vision research project that implements **YOLOv8** for real-time obstacle detection using the **Road Obstacle Detection (ROD) Dataset**. This project was developed as part of an academic research study in Informatics Engineering, focusing on object detection for intelligent transportation and traffic safety systems.

---

## 📸 Project Preview

**Dataset Class Distribution**

<img width="650" alt="distribusi kelas" src="https://github.com/user-attachments/assets/c4b8a97f-11ae-42f2-beaf-81cea43684dc" />

**Confusion Matrix**

<img width="650" alt="confusion matrix" src="https://github.com/user-attachments/assets/285f963c-af5b-469b-a12d-c129c6227708" />

**Training Model**

<img width="650" alt="train" src="https://github.com/user-attachments/assets/5d68577b-7f3b-42ac-bbe9-aa5d1dd83cbc" />

**Prediction Results**

<img width="650" alt="prediksi" src="https://github.com/user-attachments/assets/90c44939-09ac-4cbb-b3a6-5898c1bdd8ac" />

---

## 📚 Dataset Information

The **Road Obstacle Detection (ROD) Dataset** is a large-scale object detection dataset designed for autonomous driving, traffic monitoring, and intelligent transportation system research.

### Dataset Details

* **Source:** Kaggle – Obstacle Detection Dataset
* **Size:** > 2 GB
* **Annotation Format:** YOLO (`.txt`)
* **Task:** Multi-class Object Detection
* **Total Classes:** 25

### Object Categories

#### 🚗 Vehicles

* Bike
* Car
* Motorcycle
* Truck
* Bus

#### 🚸 Road Infrastructure

* Traffic Sign
* Pedestrian Crosswalk
* Traffic Cone
* Traffic Barrel
* Manhole

#### 🌳 Environment & Obstacles

* Person
* Building
* Electrical Pole
* Tree
* Dustbin
* Dog
* Bench
* Plant Pot
* Electrical Box
* Chair
* And other roadside objects

---

## 🛠️ Technology Stack

| Component               | Technology                      |
| ----------------------- | ------------------------------- |
| Programming Language    | Python                          |
| Deep Learning Framework | YOLOv8 (Ultralytics)            |
| Development Platform    | Google Colab / Jupyter Notebook |
| Computer Vision         | OpenCV                          |
| Data Visualization      | Matplotlib                      |
| Data Processing         | Pandas                          |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/yolov8-rod-detection.git
cd yolov8-rod-detection
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the Dataset

The dataset is not included in this repository due to its large size (>1 GB).

Download it manually from Kaggle and place it inside the `dataset/` directory:

```text
dataset/
├── train/
├── valid/
└── test/
```

### 4. Configure Dataset Paths

Update the dataset location in `data.yaml`:

```yaml
path: dataset
train: train/images
val: valid/images
test: test/images

nc: 25

names:
  - Bike
  - Car
  - Motorcycle
  - Truck
  - Bus
  ...
```

### 5. Train the Model

Open the notebook:

```text
notebooks/Obstacle Detection Using YOLOv8 on ROD Dataset.ipynb
```

Run all cells to start training.

Alternatively, train directly from the command line:

```bash
yolo detect train \
    model=yolov8n.pt \
    data=data.yaml \
    epochs=50 \
    imgsz=640
```

---

## 📊 Model Performance

The YOLOv8 model was trained for **50 epochs** and achieved the following performance:

| Metric    | Score |
| --------- | ----- |
| mAP@50    | 0.908 |
| mAP@50-95 | 0.732 |

These results indicate strong detection performance across various road obstacle categories.

---

## 🎯 Research Objectives

This project aims to:

* Detect road obstacles in real-time using deep learning.
* Improve traffic safety through automated object recognition.
* Evaluate YOLOv8 performance on a multi-class road environment dataset.
* Provide a baseline framework for autonomous driving research.

---

## 📦 Requirements

```txt
ultralytics
opencv-python
matplotlib
pandas
numpy
PyYAML
```

Install all requirements using:

```bash
pip install -r requirements.txt
```

---
## 📄 License

This project is intended for educational and research purposes.

---

⭐ If you find this project useful, consider giving it a star on GitHub.
