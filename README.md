# Hand-Writing Detection

A machine learning project that uses TensorFlow and Keras to recognize handwritten digits using the MNIST dataset.

## Overview

This project implements a neural network model capable of recognizing handwritten digits (0-9). The model is trained on the famous MNIST dataset and can predict digits from custom images.

## Features

- Neural network training using TensorFlow/Keras
- MNIST dataset integration
- Custom digit image prediction
- Model evaluation and accuracy reporting
- Visualization of predictions with matplotlib

## Requirements

```
tensorflow
opencv-python
numpy
matplotlib
```

## Installation

1. Clone this repository:
```bash
git clone <your-repo-url>
cd Hand-Writing-Detection-2
```

2. Install required dependencies:
```bash
pip install tensorflow opencv-python numpy matplotlib
```

## Usage

### Training and Testing

Run the main script to train the model and test it on sample images:

```bash
python ML.py
```

The script will:
1. Load and preprocess the MNIST dataset
2. Create a neural network with 2 hidden layers (128 neurons each)
3. Train the model for 20 epochs
4. Save the trained model as `handwritten.h5`
5. Evaluate the model's accuracy on test data
6. Process all digit images in the `digits/` folder and display predictions

### Model Architecture

- **Input Layer**: Flattened 28x28 pixel images
- **Hidden Layer 1**: 128 neurons with ReLU activation
- **Hidden Layer 2**: 128 neurons with ReLU activation  
- **Output Layer**: 10 neurons with softmax activation (for digits 0-9)

### Adding Custom Images

To test the model with your own handwritten digits:

1. Add your digit images to the `digits/` folder
2. Name them following the pattern: `digit{number}.png` (e.g., `digit21.png`, `digit22.png`)
3. Ensure images are in PNG format
4. Run the script - it will automatically detect and process new images

## Sample Data

The project includes 20 sample digit images (`digit1.png` to `digit20.png`) in the `digits/` folder for testing purposes.

## Model Performance

The model typically achieves high accuracy on the MNIST test dataset. Training and test accuracy will be displayed when running the script.

## Files Structure

```
Hand-Writing-Detection-2/
├── ML.py                 # Main script
├── digits/              # Sample digit images
│   ├── digit1.png
│   ├── digit2.png
│   └── ...
├── handwritten.h5       # Trained model (generated after first run)
└── README.md           # This file
```

## How It Works

1. **Data Preprocessing**: MNIST images are normalized to improve training efficiency
2. **Model Training**: A sequential neural network learns to classify digits
3. **Image Processing**: Custom images are loaded, inverted (to match MNIST format), and fed to the model
4. **Prediction**: The model outputs probabilities for each digit (0-9), and the highest probability determines the prediction

## Contributing

Feel free to fork this project and submit pull requests for improvements such as:
- Enhanced model architectures
- Better image preprocessing
- Additional evaluation metrics
- UI improvements

## License

This project is open source and available under the MIT License.