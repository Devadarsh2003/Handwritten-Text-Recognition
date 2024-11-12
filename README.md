# Handwritten Text Recognition

This project implements a **Handwritten Text Recognition (HTR)** model using the IAM Dataset. The goal is to recognize text from handwritten input images and convert it into a digital format. This repository includes training, inference, and configuration files, along with model storage and dataset directories.

## Table of Contents

- [Project Structure](#project-structure)
- [Installation](#installation)
- [Dataset](#dataset)
- [Training](#training)
- [Inference](#inference)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## Project Structure

```plaintext
Handwritten_Text_Recognition/
├── configs.py                 # Configuration settings for training and inference
├── train.py                   # Script to train the HTR model
├── model.py                   # Model architecture definition
├── inferenceModel.py          # Script for performing inference
├── sample.py                  # Sample script to demonstrate usage
├── requirements.txt
```
## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Devadarsh2003/Handwritten_Text_Recognition.git
    cd Handwritten_Text_Recognition
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Dataset

The project uses the **IAM Handwriting Database**. To download and set up the dataset:

1. Request access to the IAM dataset from [here](http://www.fki.inf.unibe.ch/databases/iam-handwriting-database).
2. Place the images and labels in the `IAM_dataset` directory:
    ```plaintext
    IAM_dataset/
    ├── images/
    └── labels/
    ```

## Training

To train the model:

1. Ensure the dataset is in place under `IAM_dataset/`.
2. Run the `train.py` script:
    ```bash
    python train.py
    ```
3. Training configurations are available in `configs.py`. Adjust parameters like learning rate, batch size, and epochs as needed.

## Inference

To perform inference on new images:

1. Place the model checkpoint in `saved_model/`.
2. Run `inferenceModel.py` with the following command:
    ```bash
    python inferenceModel.py --image_path path/to/image.png
    ```
3. The script will output the predicted text for the input image.

## Configuration

All hyperparameters and settings can be configured in `configs.py`, including paths, training parameters, and model configurations.


## Contributing

Contributions are welcome! Please open an issue or submit a pull request with any improvements.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
