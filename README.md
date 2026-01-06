# Blood_detecton_YOLO3

# White Blood Cell Detection using YOLOv3

This repository contains a YOLOv3-based object detection model for detecting **White Blood Cells (WBC)** in microscopic blood cell images.

The project uses a **custom YOLOv3 configuration** and annotated dataset for training and testing.

---

## 📂 Repository Structure

```
WBC-YOLOv3/
│
├── annotations/              # Annotation files (bounding boxes)
├── annotations_df.xlsx       # Annotation data in Excel format
├── Bloodcells.ipynb          # Jupyter notebook for data analysis
│
├── train.txt                 # Training image paths
├── test.txt                  # Testing image paths
│
├── WBC-obj.data              # YOLO data file
├── WBC.names                 # Class names
│
├── yolo_custom.cfg           # Custom YOLOv3 configuration
├── yolov3.cfg                # Original YOLOv3 configuration
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## 🧠 Model Details

- **Model:** YOLOv3
- **Framework:** Darknet
- **Task:** Object Detection
- **Classes:** White Blood Cells (WBC)

---

## 🏷️ Classes

The class names are defined in:

#### WBC.names

classes:
  - WBC
path: ./dataset
train: train/images
val: val/images

nc: 1
names:
  - WBC
🏷️ Classes

```yaml
classes:
  - WBC


---

## ⚙️ Configuration Files

- `yolov3.cfg` – Original YOLOv3 configuration
- `yolo_custom.cfg` – Modified YOLOv3 config for WBC detection
- `WBC-obj.data` – Contains class count, train/test paths, and names file

---

## 🏋️ Training

1. Prepare training and testing image paths in:
   - `train.txt`
   - `test.txt`

2. Update paths inside:
WBC-obj.data

powershell
Copy code

3. Start training using Darknet:

darknet detector train WBC-obj.data yolo_custom.cfg darknet53.conv.74
# 🔍 Testing

darknet detector test WBC-obj.data yolo_custom.cfg yolov3.weights test_image.jpg
# 📊 Dataset
Microscopic blood cell images

Bounding box annotations

Annotation files stored in annotations/

# 📜 License
This project is licensed under the terms of the MIT License.

# ✨ Author
Developed *Jagdamba* academic and research purposes in medical image analysis.
