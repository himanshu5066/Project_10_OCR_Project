Custom Object Character Recognition (OCR) on AWS:-
This project builds a Custom OCR system by combining YOLOv3 (for object detection) and Tesseract OCR (for text extraction) to read specific contents of lab reports and convert them into editable files.

 Project Overview:-
Train a custom YOLOv3 model on a personal dataset to detect regions of interest in lab reports.
Crop the detected objects using YOLO bounding box coordinates.
Preprocess the cropped images (resize, grayscale, blur, threshold) for better OCR performance.
Use Tesseract OCR to extract text and save the results as CSV files.
Optionally deploy and automate the process using AWS S3 and SageMaker.
Set Up Environment

Mount Google Drive (if using Colab):-
Define folder structure: datasets/, models/, results/.
(Optional) Set up AWS S3 and SageMaker for cloud deployment.

Data Preparation:-
Resize images and create YOLO annotations.
Upload preprocessed data to Google Drive or S3.

Model Training:-
Train YOLOv3 on Colab GPU or SageMaker.

Save weights to models/ folder:-
Validate model and upload results with bounding boxes.

Inference & OCR:-
Run YOLO inference to detect text regions.
Crop images, preprocess (resize → grayscale → blur → threshold → invert).

Run Tesseract OCR on processed images:-

Save extracted text to CSV:-
Evaluation & Optimization

Compare OCR output with ground truth:-
Fine-tune YOLO and preprocessing for better accuracy.

Deployment & Automation:-
Automate pipeline using SageMaker notebooks.
Store outputs in S3 for future processing.

Automate pipeline using SageMaker notebooks.

Store outputs in S3 for future processing.
