# CV Assignment 1 – Image Deblurring and Object Detection

## Overview
This project investigates how image blur affects object detection and whether classical deblurring methods improve downstream performance.

## Dataset
- COCO 2017 validation images
- COCOBlur blurred validation images
- Final subset: 300 images
  - Train: 180
  - Val: 60
  - Test: 60

## Methods
- Gaussian filtering (baseline)
- Wiener deconvolution
- YOLOv8n object detection
- Final YOLO training using a standard YOLO dataset structure

## Key Results
### Deblurring
- Gaussian: PSNR 23.009, SSIM 0.650
- Wiener: PSNR 23.147, SSIM 0.663

### Pretrained detector comparison
- Blurred: 5.0 detections, 0.471 confidence
- Gaussian: 5.0 detections, 0.494 confidence
- Wiener: 4.0 detections, 0.413 confidence

### Final trained model
Replace this section with your final 100-epoch evaluation numbers.

## Structure
- `dataset/processed/` – paired split data
- `dataset/yolo300/` – standard YOLO training structure
- `results/` – figures and saved comparisons
- `runs/.../best.pt` – final trained model

## AI Usage
ChatGPT was used for workflow planning, debugging guidance, and drafting documentation.
All outputs were reviewed, modified, and tested before use.