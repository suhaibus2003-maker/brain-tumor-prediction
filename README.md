# Brain Tumor Prediction Using Machine Learning

A Convolutional Neural Network (CNN) built with Python and TensorFlow/Keras that
classifies brain MRI images as **tumor** or **no tumor**.

> Educational project - not a medical diagnostic tool.

## Project structure
```
brain-tumor-prediction/
├── data/                 # dataset (sample/ synthetic, real/ from Kaggle)
├── models/               # saved model
├── results/              # training curves
├── src/
│   ├── generate_sample_dataset.py
│   ├── download_dataset.py
│   ├── train.py
│   └── predict.py
├── requirements.txt
└── README.md
```

## Setup
```bash
python -m venv venv
venv\Scripts\activate        # Windows  (Linux/Mac: source venv/bin/activate)
pip install -r requirements.txt
```

## Dataset
**Option A - Real data (recommended):** Kaggle
[Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)
```bash
python src/download_dataset.py     # needs kaggle.json API token
```
**Option B - Synthetic demo data** (quick pipeline test, not real scans):
```bash
python src/generate_sample_dataset.py
```

## Train
```bash
python src/train.py --data data/real
```
Prints a confusion matrix and classification report, saves the model to
`models/` and accuracy/loss curves to `results/training_curves.png`.

## Predict
```bash
python src/predict.py path/to/mri.jpg
```

## Results
Add your own numbers here after training (accuracy, precision, recall, F1).

## Tech stack
Python, TensorFlow/Keras, NumPy, scikit-learn, Matplotlib, Pillow
