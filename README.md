# YOLO Object Detection and Tracking

A YOLO-based workflow for images and videos, structured detection outputs, person counting, basic object tracking, dataset splitting, model training and evaluation.

**Status: source implementations included.** Notebooks may need local input data and configuration to run.

## What this covers

- Image and video object detection with bounding boxes
- Confidence filtering, category labels and non-max suppression in YOLO inference
- Person/car counting and frame-by-frame tracking
- IoU matching and dataset training/evaluation

## Processing pipeline

~~~mermaid
flowchart LR
    A[Image or video frames] --> B[YOLO inference]
    B --> C[Boxes, classes, scores]
    C --> D[Filter and annotate]
    D --> E[Track and count]
    E --> F[Evaluate detections]
~~~

## Technical explanation

For two bounding boxes A and B: **IoU(A,B) = area(A ∩ B) / area(A ∪ B)**. Predictions are represented by class, bounding box and confidence.

## Contents

- `notebooks/yolo-object-detection.ipynb` — from `week06_frequency_domain/lab06/lab06_yolo.ipynb`

## Getting started

Use Python 3.10+ in a virtual environment:

~~~bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
~~~

On Windows, activate with `.venv\Scripts\activate` instead. Install `jupyterlab` if it is not installed already. Open a notebook under `notebooks/`. Dataset/model paths in the original examples may need updating.

## Important limitations

Model weights, videos, Kaggle datasets and training runs are not republished. The notebook uses path configuration and optional downloads; adjust paths and inspect model/dataset terms before executing.

Input assets, lecture handouts, PDFs, trained models, cached results and third-party datasets have intentionally not been republished. Notebook code and explanatory cells are retained, while saved cell outputs are removed. No performance claims or additional experiments have been invented.

## Provenance

Adapted from the publicly available [ComputerVision source collection](https://github.com/dbxdrgsl/ComputerVision). Source-to-destination file mappings appear above. Each repository is organized by technical subject rather than course numbering.
