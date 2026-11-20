# Traffic Sign Recognition Using Deep Learning

The project uses the German Traffic Sign Recognition Benchmark (GTSRB) to study two approaches:

- **CNN:** classifies cropped traffic-sign images into 43 categories.
- **YOLOv8n:** detects traffic signs and predicts their locations using bounding boxes.

## Dataset

GTSRB contains 39,209 training images and 12,630 official test images across 43 classes. The training data are split into training and validation subsets by traffic sign track ID to reduce data leakage. The official test set is kept separate.

## Results

| Model | Evaluation set | Main results |
|---|---|---|
| Baseline CNN | Official test set | 98.27% accuracy; 98.24% weighted F1-score |
| YOLOv8n | Validation set (5,610 images; 41 classes) | 98.40% precision; 98.90% recall; 99.40% mAP@50; 94.60% mAP@50-95 |


## Running the Project

Open DLPROJECT_Group5 (1).ipynb in Google Colab and run the cells in order. A GPU runtime is required for the YOLO training section. The CNN optimization section also requires the baseline model and training-history files saved to Google Drive by the earlier notebook cells.

## Tools

Python, TensorFlow/Keras, PyTorch, Ultralytics YOLO, scikit-learn, NumPy, pandas, and Google Colab.

## Limitation

The experiments use cropped traffic-sign images rather than full road scenes. Further testing on road-scene images and videos, and quantitative YOLO evaluation across all 43 classes, are needed.
