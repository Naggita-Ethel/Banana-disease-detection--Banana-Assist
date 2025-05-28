

---

```markdown
Banana Disease Detection using YOLOv11m

This project focuses on detecting and classifying banana leaf diseases using the YOLOv11m object detection model. It supports the identification of both healthy leaves and various diseases such as Panama disease, Yellow Sigatoka, and Black Sigatoka, among others using banana leaf images. This model is deployed in the mobile and web version of Banana Assist application for real time detection using a camera and image upload.

Overview

The notebook `banana-disease-detection.ipynb` contains the complete workflow for training and evaluating a YOLOv11m model tailored to banana leaf disease classification. The model can detect multiple disease types in a single image and is optimized for accuracy and efficiency.

Features

- Image annotation and preprocessing
- Custom dataset loading using YOLO format
- YOLOv11m training and validation
- Visualization of predictions
- mAP (mean Average Precision) evaluation metrics
- Export trained model for deployment

Model Architecture

- Model Used: YOLOv11m (Ultralytics)
- Input: Images of banana leaves (healthy and diseased)
- Output: Class labels indicating the type of disease and coonfidences.

Repository Structure

```

📦banana-disease-detection
┣ 📜banana-disease-detection.ipynb
┣ 📂datasets/
┃ ┗ 📜\[train/val/test folders with YOLO format]
┣ 📂runs/
┃ ┗ 📜\[YOLO training logs and weights]
┣ 📜README.md

````

Requirements

Basic dependencies:

* Python 3.8+
* Ultralytics (YOLOv11m)
* OpenCV
* Matplotlib
* Pandas
* NumPy

Training

!yolo task=detect mode=train model=yolov11m.pt data=config.yaml epochs=50 imgsz=640


Make sure your dataset is structured and annotated in YOLO format and the `config.yaml` file is properly defined.

Evaluation

The model's performance is evaluated using:

* mAP\@0.5
* Precision
* Recall

You can visualize results using:

!yolo task=detect mode=val model=runs/detect/train/weights/best.pt data=config.yaml


Sample Predictions

Visual examples of predictions are generated with class labels and confidences.

Use Cases

* Supporting farmers in early detection of banana diseases
* Improving agricultural productivity
* Reducing yield loss due to late diagnosis

Future Work
* Integration with advisory chatbot for treatment recommendations
* Increasing classes of diseases detected and improving model.

Contributors

Naggita Ethel – [GitHub](https://github.com/Naggita-Ethel) | [LinkedIn](https://www.linkedin.com/in/naggita-ethel-b5b066254/)


