# Vehicle Plate Detection & Recognition using CRNN and YOLOv11  

This project implements a robust pipeline for **vehicle license plate detection** and **text recognition** using YOLOv11 for object detection and CRNN (Convolutional Recurrent Neural Network) for Optical Character Recognition (OCR).  

## Table of Contents  
- [Overview](#overview)  
- [Features](#features)  
- [Installation](#installation)  
- [Usage](#usage)  
- [File Structure](#file-structure)  
- [Model Details](#model-details)  
- [Results](#results)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Overview  
Vehicle plate detection and recognition are crucial for applications like traffic monitoring, automated toll collection, and law enforcement. This project provides a deep learning-based solution to detect license plates and extract text from them using state-of-the-art YOLOv11 and CRNN models.  

---

## Features  
- High-accuracy license plate detection using **YOLOv11**.  
- Robust text recognition for various fonts and plate styles using **CRNN**.  
- Easy-to-use pipeline for processing images or video streams.  
- Modular and scalable design for integration into larger systems.  

---

## Installation  
1. Clone the repository:  
   ```bash  
   git clone [https://github.com/your-username/Vehicle-Plate-Detection-Recognition-using-CRNN-and-YOLOV11.git 
   cd Vehicle-Plate-Detection-Recognition-using-CRNN-and-YOLOV11
   ```
2. Install required dependencies:
  ```bash
  pip install -r requirements.txt  
  ```

---

## Usage
1. To process an image:
  ```bash
  python detect_and_recognize.py --input path/to/image.jpg  
  ```
2. To process a video:
  ```bash
  python detect_and_recognize.py --input path/to/video.mp4 --mode video  
  ```
Output files will be saved in the outputs/ directory.

---

## File Structure
  ```plaintext
  Vehicle-Plate-Detection-Recognition-using-CRNN-and-YOLOV11/
  ├── dataset/
  │   ├── Detection/
  │   │   ├── images/
  │   │   ├── labels/
  │   │   ├── Licplatesdetection_train.csv
  │   ├── detection_splits/
  │   │   ├── train/
  │   │   ├── val/
  │   ├── Recognition/
  │   │   ├── images/
  │   │   ├── Licplatesrecognition_train.csv
  │   ├── runs/
  │   │   ├── detect/
  │   │   │   ├── train/
  │   │   │   ├── train2/
  │   │   │   ├── train3/
  │   │   │   ├── train32/
  │   ├── test/
  │   │   ├── test/
  │   ├── license_plate_recognition_model.h5
  ├── Car_Number_Plate_Detection_and_Recognition.ipynb
  ```

---

## Model Details

1. YOLOv11
* A cutting-edge object detection model used for detecting vehicle plates with high accuracy and speed.
2. CRNN
* Combines CNN for feature extraction and RNN for sequential text recognition, making it ideal for license plate text extraction.

---

## Results
1. YOLOv11:
- Precision (P): 0.991
- Recall (R): 1
- mAP50 (Mean Average Precision at IoU threshold 50%): 0.995
- mAP50-95 (Mean Average Precision at IoU thresholds from 50% to 95%): 0.778

2. CRNN:
- Accuracy: 0.7221
- Loss: 1.2978
- Validation Loss: 1.2603590488433838
- Validation Accuracy: 0.7298611402511597

Processed 30 FPS on a GPU-enabled environment.

---

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request for improvements and bug fixes.

---
