# Adaptive Gradient Dimension Splitting for Robust and Heterogeneous Federated Intrusion Detection

This repository provides the code of Neurips Workshop 2024

## Requirements
To install requirements:
```setup
pip install -r requirements.txt

# conda environment
conda env create -f environment.yml
conda activate agas
```

## Training
To train the model(s) in the IDS setting, make adaptions in the config part, and run this command:
```train
python main.py
```
Run the code under baseline settings(cifar10 and mnist):
```train
cd baselines
python cifar10.py
python mnist.py
```

## Results
Detection accuracy of Baselines under different Byzantine attacks and datasets:
| Dataset | Method      | LIE   | BitFlip | Min-Sum | IPM   |
|---------|-------------|-------|---------|---------|-------|
| **MNIST** | Bulyan      | 97.44 | 97.36   | 96.93   | 97.28 |
|         | GAS         | 97.33 | 98.63   | 98.49   | **98.83** |
|         | AGDS NS     | 97.19 | 98.70   | 98.55   | 98.81 |
|         | AGDS PCA    | **98.88** | **98.82** | 98.86   | 98.79 |
|         | AGDS Kmeans | 98.39 | 98.75   | **99.00** | 98.69 |
| **CIFAR10** | Bulyan    | 70.73 | 68.45   | 69.65   | 70.06 |
|         | GAS         | 70.33 | 70.05   | 70.26   | 70.03 |
|         | AGDS NS     | 71.42 | **71.05** | 69.88   | **70.97** |
|         | AGDS PCA    | **71.83** | 70.38   | 70.13   | 70.55 |
|         | AGDS Kmeans | 71.28 | 69.31   | **70.75** | 70.87 |

Detection Accuracy of IDS under Different Byzantine Attacks and Datasets:
| Dataset      | Method      | LIE   | BitFlip | Min-Sum | IPM   |
|--------------|-------------|-------|---------|---------|-------|
| **CICIOT2023** | Bulyan      | 86.22 | 86.66   | 86.36   | 85.83 |
|              | GAS         | 87.62 | 87.58   | 87.63   | 87.27 |
|              | AGDS NS     | 87.68 | 87.62   | 87.52   | **87.67** |
|              | AGDS PCA    | 87.81 | **87.64** | **87.68** | **87.67** |
|              | AGDS Kmeans | **88.74** | 87.62   | 87.67   | 87.65 |
| **Edge-IIoT** | Bulyan     | 68.69 | 71.05   | 72.55   | 72.40 |
|              | GAS         | 73.64 | 71.22   | 75.17   | 74.79 |
|              | AGDS NS     | 73.78 | 75.26   | 75.68   | 75.97 |
|              | AGDS PCA    | **76.15** | 75.57   | **76.28** | 75.44 |
|              | AGDS Kmeans | 75.88 | **75.61** | 75.30   | **76.16** |


## Contributing
This project builds upon the work from [YuchenLiu-a/byzantine-gas](https://github.com/YuchenLiu-a/byzantine-gas).

It is licensed under the MIT License, so feel free to submit issues, fork the repository, and open pull requests to contribute to the project.



