# YOLOv5 Custom Object Detection Training

This repository contains a streamlined workflow for training the **YOLOv5** model on custom datasets. It provides a Jupyter Notebook designed to guide users through the process of setting up the environment, preparing data, training the model, and running inference on custom objects.

## 📄 Repository Contents

* `yolov5_custom_training.ipynb`: The main notebook containing the step-by-step code for:
    * Installing dependencies (Ultralytics YOLOv5).
    * Mounting datasets (e.g., from Google Drive or local storage).
    * Configuring model hyperparameters.
    * Training the model.
    * Visualizing results and running inference on new images.

## 🛠️ Prerequisites

To run the notebook locally, you need the following installed:

* [Python 3.8+](https://www.python.org/downloads/)
* [Jupyter Notebook](https://jupyter.org/install) or [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html)
* **PyTorch** (compatible with your hardware, CUDA recommended for faster training)

Alternatively, you can upload the notebook to **Google Colab** for free GPU access.

## 🚀 Usage Guide

### Option A: Running on Google Colab (Recommended)
1.  Download the `yolov5_custom_training.ipynb` file from this repository.
2.  Go to [Google Colab](https://colab.research.google.com/).
3.  Upload the notebook file.
4.  Change the runtime type to GPU (`Runtime` > `Change runtime type` > `T4 GPU`).
5.  Follow the instructions in the notebook cells.

### Option B: Running Locally
1.  **Clone the repository**
    ```bash
    git clone [https://github.com/felixyustian/yolo_v5_test.git](https://github.com/felixyustian/yolo_v5_test.git)
    cd yolo_v5_test
    ```

2.  **Install Dependencies**
    It is recommended to use a virtual environment.
    ```bash
    pip install notebook torch torchvision opencv-python matplotlib
    ```
    *Note: You may need to install the specific requirements for YOLOv5 once you run the notebook.*

3.  **Launch Jupyter**
    ```bash
    jupyter notebook yolov5_custom_training.ipynb
    ```

## 📊 Workflow Overview

The notebook generally follows these steps:

1.  **Setup**: Clone the official Ultralytics YOLOv5 repo and install requirements.
2.  **Dataset Config**: Create a `data.yaml` file pointing to your training and validation images.
3.  **Weights**: Select a pre-trained model (e.g., `yolov5s.pt`, `yolov5m.pt`) to start transfer learning.
4.  **Train**: Run the training loop for a specified number of epochs.
5.  **Detect**: Use the best model weights (`runs/train/exp/weights/best.pt`) to detect objects in test images.

## 📄 License

This project is licensed under the **GPL-3.0 License**. See the `LICENSE` file for details.
