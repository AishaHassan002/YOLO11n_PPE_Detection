# YOLOv11n PPE Detection and Compliance Monitoring Model

This repository contains a YOLOv11n model optimized for real-time personal protective equipment (PPE) detection and a YOLOv8 model for person detection. The project aims to enhance construction site safety by ensuring workers are wearing necessary PPE, such as safety helmets and safety vests, while providing real-time alerts when PPE compliance is not met.

## Model Description

The model is designed for **real-time PPE detection** in dynamic construction environments, leveraging YOLOv11n’s fast inference capabilities. It has been optimized using techniques such as FP16 conversion and batch processing for efficiency. The model uses YOLOv11n for PPE detection, identifying safety helmets and vests, and YOLOv8 for person detection, ensuring monitoring of PPE safety violations. The system processes real-time video footage of construction sites to ensure PPE Compliancy. If a person is detected without PPE, the model sends desktop notifications for immediate attention. To enhance performance, the model utilizes batch processing and FP16 precision to speed up inference, ensuring efficient real-time video analysis without compromising accuracy.

### Model Weights

The model weights (`YOLOv11n_Weight.pt`) for PPE detection and (`Person_Detection_weight.pt`) for person detection are pre-trained and ready for inference. The model was trained on custom datasets, which can be referenced below.

## Datasets

The datasets used to train the model are referenced from **Roboflow Universe**. The model can be applied to similar datasets for PPE detection in construction environments.

You can access and download the dataset from:

- **PPE Detection Classes**: https://universe.roboflow.com/roboflow-universe-projects/safety-vests, https://universe.roboflow.com/universe-datasets/hard-hat-universe-0dy7t
- **Person Detection Class**: https://universe.roboflow.com/yolov8-mn29d/person-hecxr

### Dataset Description:
- The datasets include labeled images of construction workers wearing various types of PPE, captured in real-world construction settings.

## Installation

To use the model, you'll need the following dependencies:

- Python 3.x
- PyTorch (for model loading)
- OpenCV (for video processing)
- NumPy (for tensor operations)
- ptflops (for model complexity analysis)

### Install Dependencies:

```bash
pip install torch opencv-python numpy ptflops
