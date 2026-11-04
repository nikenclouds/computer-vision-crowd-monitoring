# Mall Crowd Counting Using Computer Vision

## Project Overview

This project focuses on estimating the number of people in a shopping mall environment using Computer Vision and Deep Learning techniques.

Two approaches are explored and compared:

- **YOLOv8n** — Object detection-based crowd counting.
- **CNN Density Map** — Density map regression-based crowd counting.

The objective is to evaluate and compare the performance of both approaches in estimating crowd size.

## Objectives

- Develop a crowd counting system using Computer Vision.
- Implement CNN-based density map regression.
- Apply YOLOv8n for person detection and counting.
- Evaluate model performance using MAE and RMSE.
- Compare the prediction results of both approaches.

## Methodology

The project follows these main stages:

1. Dataset preparation and preprocessing.
2. Density map preparation.
3. CNN model development and training.
4. CNN training optimization using Early Stopping.
5. YOLOv8n implementation and evaluation.
6. Crowd count prediction.
7. Performance comparison using MAE and RMSE.

## Experimental Results

| Model | Mean Error | MAE | RMSE |
|---|---:|---:|---:|
| YOLOv8n | -14.505 | 14.505 | 14.916 |
| CNN Density Map | -32.395 | 32.395 | 32.862 |

YOLOv8n achieved lower error values than CNN Density Map in the reported evaluation.

The relative error reductions compared with CNN Density Map were:

- MAE reduction: 55.22%
- RMSE reduction: 54.61%

*Note: These results should be interpreted in the context of the evaluation data and protocol used in this experiment.*

## Evaluation Metrics

- **Mean Error:** Measures the average signed difference between predicted and actual crowd counts.
- **MAE (Mean Absolute Error):** Measures the average absolute prediction error.
- **RMSE (Root Mean Squared Error):** Measures prediction error while penalizing larger errors more heavily.

## Project Structure

```text
mall-crowd-counting/
│
├── mall_crowd_counting.ipynb
├── requirements.txt
├── README.md
├── .gitignore
│
├── Results/
│   ├── yolo_evaluation_results.csv
│   ├── yolo_cnn_validation_metrics.csv
│   ├── yolo_cnn_validation_comparison.csv
│   └── ...
│
└── processed/
    └── mall_crowd_cnn.pth
```

## Installation

Clone this repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd mall-crowd-counting
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on macOS/Linux:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## How to Run

Open the notebook:

```bash
jupyter notebook mall_crowd_counting.ipynb
```

Run the notebook cells sequentially after preparing the required dataset.

## Limitations

- Prediction performance may be affected by image quality, lighting, camera angle, and crowd density.
- Object detection and density map regression use different estimation approaches.
- Further evaluation on independent datasets is needed to assess generalization.

## Future Development

- Hyperparameter optimization.
- Evaluation on more diverse crowd datasets.
- Real-time crowd counting.
- Integration with a crowd monitoring dashboard.

## Technologies

Python | PyTorch | YOLOv8 | OpenCV | NumPy | Pandas | Matplotlib | Scikit-learn | Jupyter Notebook

---

**Project Category:** Computer Vision / Deep Learning  
**Task:** Crowd Counting  
**Models:** YOLOv8n and CNN Density Map