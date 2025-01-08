# Car Crash Detection with CNN

A simple PyTorch-based project to detect collisions using dashcam video frames. This repository includes:
- A custom dataset loader that reads labeled frames from CSV.
- A Convolutional Neural Network (CNN) implementation.
- Training scripts for model optimization.
- Fine Tuning script for further model optimization.
- Plots of loss and accuracy over epochs.

## Dataset

Download the dataset from [This Link](https://www.kaggle.com/datasets/asefjamilajwad/car-crash-dataset-ccd).

Frames are extracted and zero-padded for each video (e.g., `C_000001_01.jpg`, `C_000001_02.jpg`, etc.). Adjust the paths for where you have stored your CSV (e.g., `Crash_Table.csv`) and images (e.g., in `CrashBest/`).

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/CarCrashDetection.git
   cd CarCrashDetection
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Update paths** in `train.ipynb` to point to your `Crash_Table.csv` and images directory.
2. **Run the training from the notebook**:
   ```bash
   python train.ipynb
   ```
3. After training, **plots** for loss and accuracy will be generated, and the final model state is saved (e.g., `final_model.pth`).

## Results

Once the model finishes training, you’ll see printed logs like:
```
Epoch 1: Train Loss 0.52, Val Loss 0.48, Train Acc 0.75, Val Acc 0.76
...
```
You can also view the **loss and accuracy charts** for a visual overview of how the model learns over epochs.

![Training Result](/result.png)

## Contributing

Feel free to open issues or submit pull requests if you’d like to help improve this project!