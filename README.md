# MOLO: A Lightweight Object Detection Model with Depth-wise Convolution

## Table of Contents
- [Introduction](#introduction)
- [Project Overview](#project-overview)
- [Methodology](#methodology)
  - [MOLO Architecture](#molo-architecture)
  - [Depth-wise Convolution](#depth-wise-convolution)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction
This repository contains the code and resources for my B.Sc. Thesis on developing a lightweight and efficient object detection model named **MOLO** (MobileNet + YOLO). The objective of this project is to enhance the speed and reduce the computational cost of object detection models by integrating Depth-wise Convolution into the YOLO framework.

This work was conducted as part of my B.Sc. Thesis at the **Deep Learning Lab, Department of Electrical Engineering, Sharif University of Technology**.

## Project Overview
Object detection is a critical task in computer vision with numerous applications, including autonomous driving, video surveillance, and more. Traditional convolutional neural networks (CNNs) often require significant computational resources, making real-time detection challenging on devices with limited processing power.

**MOLO** aims to address this challenge by combining the strengths of the MobileNet architecture with the YOLO object detection framework. Specifically, we leverage Depth-wise Convolution to replace standard convolution layers in YOLO, significantly reducing the number of parameters and computational load.

## Methodology

### MOLO Architecture
MOLO builds upon the YOLO architecture, which is known for its real-time object detection capabilities. YOLO divides the input image into a grid and simultaneously predicts bounding boxes and class probabilities for each grid cell. MOLO enhances YOLO's efficiency by incorporating Depth-wise Convolution, inspired by the MobileNet design.

### Depth-wise Convolution
Depth-wise Convolution is a technique that decomposes a standard convolution operation into two layers: a depth-wise convolution and a point-wise convolution. The depth-wise convolution applies a single convolutional filter per input channel, drastically reducing the number of parameters and the computational cost.

By replacing standard convolutions with Depth-wise Convolutions in the YOLO framework, MOLO achieves a lightweight and faster model, making it suitable for real-time applications on devices with constrained computational resources.

## Results
MOLO has been tested and validated to demonstrate its effectiveness:

- **Parameter Reduction**: Achieved a reduction in the number of parameters by up to 28%.
- **Computational Load**: The computational cost was reduced by 24.4%.
- **Inference Speed**: Improved inference speed by 16.7% compared to the standard YOLO model.

These results affirm the suitability of MOLO for deployment in resource-constrained environments without compromising accuracy.

## Installation
To run the code in this repository, follow these steps:

1. Clone this repository:
   ```bash
   git clone https://github.com/SajjadHm/MOLO-Mobile-Net-YOLO.git
   ```
2. Navigate to the project directory:
   ```bash
   cd MOLO-Mobile-Net-YOLO
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
To run the MOLO object detection model on your images or video streams:

1. Place your input images or videos in the `data/` directory.
2. Run the model using the following command:
   ```bash
   python detect.py --input data/input_image.jpg --output results/
   ```
3. The detection results will be saved in the `results/` directory.

For advanced usage, including hyperparameter adjustments, refer to the `config.yaml` file.

## Contributing
Contributions are welcome! If you find any issues or have ideas for improvements, feel free to open an issue or submit a pull request. Please ensure that your contributions align with the project goals and maintain code quality.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contact
For any questions, suggestions, or collaborations, please contact:

- **Sajjad Hashembeiki**: sajjad.hashembeiki@gmail.com
- **Deep Learning Lab, EE Department, Sharif University of Technology**
