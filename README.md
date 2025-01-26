
# Flower Detection using Convolutional Neural Networks (CNN)

## Overview
This project focuses on detecting and classifying flowers using a Convolutional Neural Network (CNN). It leverages deep learning techniques to accurately predict the category of a flower based on its image.

---

## Table of Contents
1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Installation](#installation)
4. [Dataset Structure](#dataset-structure)
5. [Model Architecture](#model-architecture)
6. [Usage](#usage)
7. [Results](#results)
8. [Contributing](#contributing)
9. [License](#license)

---

## Features
- Detects and classifies flowers into multiple categories.
- Trained using a CNN model for high accuracy.
- Supports real-time image predictions.
- Easily extendable for additional flower categories.

---

## Technologies Used
- Python
- TensorFlow/Keras (for model creation and training)
- NumPy (for numerical operations)
- OpenCV or PIL (for image preprocessing)
- Matplotlib (for visualizing results)

---

## Installation
1. Clone this repository:
    ```bash
    git clone https://github.com/your-username/flower-detection-cnn.git
    cd flower-detection-cnn
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

---

## Dataset Structure
The project dataset is organized as follows:

```
images/
├── daisy/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
├── rose/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
├── sunflower/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
├── dandelion/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
├── tulip/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...

sample/
├── example_image1.jpg
└── example_image2.jpg
```

- **images/**: Contains subfolders for each flower category (daisy, rose, sunflower, dandelion, tulip) with their respective images.
- **sample/**: Contains sample images for testing and demonstration.

---

## Model Architecture
The CNN model is designed as follows:
1. **Input Layer:** Processes images of size 128x128.
2. **Convolutional Layers:** Extract spatial features from the images.
3. **Pooling Layers:** Reduce spatial dimensions and prevent overfitting.
4. **Fully Connected Layers:** Map features to flower categories.
5. **Output Layer:** Outputs the predicted category using softmax activation.

### Example Model Summary:
```plaintext
Layer (type)                 Output Shape              Param #
================================================================
Conv2D                      (128, 128, 32)             896
MaxPooling2D                (64, 64, 32)               0
Conv2D                      (64, 64, 64)               18496
MaxPooling2D                (32, 32, 64)               0
Flatten                     (None, 65536)             0
Dense                       (None, 128)               8388864
Dense                       (None, num_categories)    16512
================================================================
Total params: ~8.4M
Trainable params: ~8.4M
Non-trainable params: 0
```

---

## Usage
1. Train the model:
    ```bash
    python train.py
    ```

2. Test the model:
    ```bash
    python test.py --image path/to/image.jpg
    ```

3. Visualize training performance:
    ```bash
    python plot_metrics.py
    ```

4. Perform predictions:
    ```bash
    python predict.py --image path/to/flower.jpg
    ```

---

## Results
The model achieved the following accuracy metrics:
- **Training Accuracy:** 95%
- **Validation Accuracy:** 90%

### Sample Predictions:
| Image                     | Predicted Label | Confidence |
|---------------------------|-----------------|------------|
| ![flower1](examples/img1.jpg) | Rose            | 96%        |
| ![flower2](examples/img2.jpg) | Daisy           | 92%        |

---

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and push to your fork.
4. Submit a pull request with a detailed explanation of your changes.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
