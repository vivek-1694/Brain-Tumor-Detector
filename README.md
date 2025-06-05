# Brain-Tumor-Detector
MobileNetV2-based Brain Tumor Detection Model

This project is a deep learning model that detects brain tumors from MRI images using MobileNetV2.


## Files in this project

"mobilenet_BT_model.keras": Trained MobileNetV2 model
"label_encoder.pkl" : Label encoder for tumor classes
"train_model.ipynb" : Jupyter notebook with full training code
"README.md" : Project info (this file)


## Dataset

The model was trained on a dataset of MRI brain scan images(from kaggle) labeled as:
Tumor
No Tumor
(The dataset is not included in this repository due to its large size.)


## How to Use

1. Clone the repository:
git clone https://github.com/vivek-1694/Brain-Tumor-Detector.git

2. Install required packages:
pip install -r requirements.txt


3. Load the model and encoder in Python:

from tensorflow.keras.models import load_model
import pickle
model = load_model('mobilenet_BT_model.keras')
with open('label_encoder.pkl', 'rb') as f:
    label_encoder = pickle.load(f)


4. To Retrain the Model:

Open the .ipynb file to:
Load your dataset
Train the model
Save the .keras and .pkl files