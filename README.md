
# Object Detection Using YOLOv5

A computer vision project that applies YOLOv5 to detect objects in images and webcam video. The project includes dataset preparation, model training, object detection, and a web-based demo for image uploads.

## Overview

This project explores object detection using YOLOv5, a deep learning model designed for efficient object detection. Experiments were conducted using the COCO128 dataset and custom-labeled image data.

The project also implements a simple web interface that allows users to upload an image and view the processed detection results.

## Features

- **Object Detection:** Detect objects in images using YOLOv5.
- **Custom Dataset Preparation:** Organize image datasets and annotate objects using MakeSense.AI.
- **Model Training:** Train YOLOv5 using custom data and experiment with different training configurations.
- **Web-Based Demo:** Upload images through a web interface and display detection results.
- **Webcam Detection:** Run object detection on a webcam stream.

## Technologies Used

- Python
- PyTorch
- YOLOv5
- OpenCV
- Google Colab
- HTML, CSS, Bootstrap 5
- Flask (for the web application)
- MakeSense.AI (for image annotation)


## Dataset

The project uses two data sources:

- **COCO128:** A sample dataset used to experiment with object detection and model training.
- **Custom Dataset:** Personal images annotated using MakeSense.AI and organized in the YOLOv5 dataset format.

The custom dataset was limited in size due to resource constraints.

## Implementation Workflow

1. **Environment Setup:** Clone the YOLOv5 repository and install the required dependencies in Google Colab.
2. **Dataset Preparation:** Extract the dataset, annotate custom images, and configure the dataset YAML file.
3. **Model Training:** Train the model using YOLOv5 with configurable image size, batch size, number of epochs, and pretrained weights.
4. **Object Detection:** Run inference on sample images and webcam video using trained or pretrained weights.
5. **Web Application:** Build a simple interface for image uploads and display the resulting detection images.

## Model Training

An example training command used in the project:

```bash
python train.py \
  --img 640 \
  --batch 16 \
  --epochs 50 \
  --data data/coco128.yaml \
  --weights yolov5s.pt
```

Training parameters can be adjusted according to the dataset and available computing resources.

## Object Detection

Example command for running detection on images:

```bash
python detect.py \
  --weights yolov5s.pt \
  --img 640 \
  --conf 0.25 \
  --source data/images
```

For webcam detection, the source can be configured to use the webcam device, provided that the execution environment supports camera access.

## Results

The project demonstrates the YOLOv5 object detection workflow, including model training, image inference, webcam detection, and a web-based image upload interface.

Detection outputs can be reviewed visually using the generated bounding boxes and confidence scores.

*Note: Quantitative performance metrics are not included here because verified evaluation results have not yet been documented in this repository.*

## Limitations

- The custom dataset contains a limited number of images.
- Training performance depends on the dataset, training configuration, and available computing resources.
- Detection accuracy may vary depending on object size, image quality, and lighting conditions.
- The web application requires a compatible Python environment and a correctly configured YOLOv5 inference backend.

## Future Improvements

- Expand the custom dataset and improve annotation quality.
- Evaluate the model using precision, recall, mAP, and inference time.
- Compare different YOLOv5 model configurations.
- Improve the web interface and deployment workflow.

## Acknowledgements

- [Ultralytics YOLOv5](https://github.com/ultralytics/yolov5)
- [MakeSense.AI](https://www.makesense.ai/)





