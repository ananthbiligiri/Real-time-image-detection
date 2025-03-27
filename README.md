# Real-Time Image Detection using YOLOv8

This project implements **real-time object detection** using the **YOLOv8** model with OpenCV in Python. It includes training a custom dataset and running real-time detection with a webcam.

---

## Features
- Train a **YOLOv8** model on a custom dataset
- Perform real-time object detection using **OpenCV**
- Easy-to-use **Python scripts** for training and detection

---

## Installation
### **1. Clone the Repository**
```bash
git clone https://github.com/yourusername/Real-Time-YOLOv8-Detection.git
cd Real-Time-YOLOv8-Detection
```

### **2. Install Dependencies**
```bash
pip install ultralytics opencv-python numpy
```

---

## Training the Model
### **Prepare Your Dataset**
1. Organize dataset in **YOLO format**:
   ```
   dataset/
   ├── images/
   │   ├── train/
   │   ├── val/
   ├── labels/
   │   ├── train/
   │   ├── val/
   ├── data.yaml
   ```
2. Edit `data.yaml` with the correct dataset paths:
   ```yaml
   train: path/to/your/dataset/images/train
   val: path/to/your/dataset/images/val
   
   nc: 2  # Number of classes
   names: ["class1", "class2"]
   ```

### **Train the Model**
Run the following command to train the YOLOv8 model:
```bash
python train_yolo.py
```
This will train for **50 epochs** using **640x640** images.

---

## Running Real-Time Detection
After training, run the following command to start real-time object detection using your webcam:
```bash
python detect.py
```
Press **'q'** to exit the webcam window.

---

## File Descriptions
- **train_yolo.py** → Script for training the YOLOv8 model
- **detect.py** → Real-time object detection script
- **data.yaml** → Dataset configuration file

---

## Notes
- The trained model will be saved in `runs/train/exp/weights/best.pt`.
- You can use **pre-trained models** (`yolov8n.pt`, `yolov8s.pt`) for better performance.

## Results

Here is an example of real-time image detection using YOLOv8:

![Detection Result](result.jpg)
