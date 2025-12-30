# **Automated PCB Component Detection Using OpenCV and YOLOv11**

Overview:
This project automates printed circuit board (PCB) inspection by combining classical
computer vision techniques with deep learning-based object detection. The objective is
to detect and classify PCB components from high-resolution images, reducing the need
for manual inspection in electronics manufacturing.

The project consists of two major components: PCB extraction using OpenCV and
component detection using a fine-tuned YOLOv11 model.

Methodology:
1. PCB Object Masking (OpenCV)
   - Applied image thresholding to separate PCB from background
   - Used edge detection and contour extraction to isolate the motherboard
   - Filtered contours by area to remove noise
   - Extracted the PCB using bitwise masking operations

2. Component Detection (YOLOv11)
   - Fine-tuned a pretrained YOLOv11 nano model using Ultralytics
   - Trained on a labeled PCB component dataset
   - Optimized training parameters including epochs, batch size, and image resolution
   - Used large image sizes to detect small electronic components

3. Model Evaluation
   - Evaluated trained model on unseen PCB images
   - Analyzed detection accuracy, misclassifications, and missed components
   - Reviewed confusion matrix and precision-recall curves

Training Environment:
- Local GPU or Google Colab (T4 GPU recommended)
- Dataset formatted for YOLOv11 compatibility

Technologies Used:
- Python
- OpenCV
- Ultralytics YOLOv11
- PyTorch
- NumPy, Pillow

Key Outcomes:
- Successfully isolated PCBs from complex backgrounds
- Achieved accurate component detection using deep learning
- Demonstrated scalability for real-world manufacturing inspection

Applications:
- Electronics manufacturing quality control
- Automated PCB inspection
- Smart factory and Industry 4.0 systems

