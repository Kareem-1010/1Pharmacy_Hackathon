# 1Pharmacy QR Code Detection Hackathon

## Overview
This repository contains a QR code detection solution developed for the 1Pharmacy Hackathon using YOLOv8 models. The project implements computer vision techniques to accurately detect and locate QR codes in pharmaceutical images.

## Project Structure
```
1Pharmacy_Hackathon/
├── 1pharmacy (1).ipynb          # Main Jupyter notebook with implementation
├── data.yaml                    # YOLO dataset configuration
├── results.csv                  # Training/validation results
├── yolov8s.pt                   # YOLOv8 small pre-trained model
├── yolov8x.pt                   # YOLOv8 extra-large pre-trained model
├── QR_Dataset/                  # Dataset directory
│   ├── sample_submission_1.json # Sample submission format
│   ├── sample_submission_2.json # Sample submission format
│   ├── train_images/           # Training images (img001-img200)
│   ├── train_label/            # Training labels in YOLO format
│   ├── test_images/            # Test images (img201-img250)
│   ├── test_label/             # Test labels for validation
│   └── yolo_dataset/           # Processed YOLO dataset
└── qr_detection_max_accuracy/   # Trained models
    ├── qr_yolov8s_best_accuracy/  # Best YOLOv8s model results
    │   ├── weights/               # Model weights (.pt files)
    │   ├── args.yaml             # Training arguments
    │   ├── results.csv           # Training metrics
    │   └── train_batch*.jpg      # Training visualization
    └── qr_yolov8x_best_accuracy/  # Best YOLOv8x model results
```

## Features
- **QR Code Detection**: Accurate detection of QR codes in pharmaceutical images
- **YOLOv8 Implementation**: Utilizes both YOLOv8s and YOLOv8x models for optimal performance
- **Comprehensive Dataset**: 250 images with proper train/test split (200/50)
- **Model Comparison**: Multiple model variants with performance metrics

## Models
### YOLOv8s Best Accuracy Model
- **Location**: `qr_detection_max_accuracy/qr_yolov8s_best_accuracy/`
- **Weights Available**: 
  - `best.pt` - Best performing checkpoint
  - `last.pt` - Final training checkpoint
  - Training epoch checkpoints (0, 20, 40, 60, 80, 100)

### YOLOv8x Best Accuracy Model
- **Location**: `qr_detection_max_accuracy/qr_yolov8x_best_accuracy/`
- **Features**: Enhanced accuracy with larger model architecture

## Dataset Information
- **Training Images**: 200 images (img001.jpg - img200.jpg)
- **Test Images**: 50 images (img201.jpg - img250.jpg)
- **Label Format**: YOLO format with bounding box coordinates
- **Classes**: QR code detection (single class)

## Getting Started
1. **Clone the repository**
   ```bash
   git clone https://github.com/Kareem-1010/1Pharmacy_Hackathon.git
   cd 1Pharmacy_Hackathon
   ```

2. **Install dependencies**
   ```bash
   pip install ultralytics opencv-python matplotlib pandas
   ```

3. **Run the main notebook**
   ```bash
   jupyter notebook "1pharmacy (1).ipynb"
   ```

## Usage
The main implementation is in `1pharmacy (1).ipynb` which includes:
- Data preprocessing and augmentation
- Model training with YOLOv8
- Performance evaluation and metrics
- Inference on test images
- Result visualization

## Results
Training results and performance metrics are available in:
- `results.csv` - Overall project results
- `qr_detection_max_accuracy/qr_yolov8s_best_accuracy/results.csv` - Detailed model metrics

## Submission Format
Sample submission formats are provided in:
- `QR_Dataset/sample_submission_1.json`
- `QR_Dataset/sample_submission_2.json`

## Technologies Used
- **Deep Learning Framework**: Ultralytics YOLOv8
- **Programming Language**: Python
- **Libraries**: OpenCV, matplotlib, pandas, numpy
- **Model Architecture**: YOLO (You Only Look Once) v8

## Contributing
This project was developed for the 1Pharmacy Hackathon. Contributions and improvements are welcome.

## License
This project is part of the 1Pharmacy Hackathon competition.

---
*Developed for 1Pharmacy Hackathon - QR Code Detection Challenge*
