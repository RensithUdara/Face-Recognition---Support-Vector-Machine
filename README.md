# Face Recognition using Support Vector Machine (SVM)

A facial recognition system that identifies and classifies faces of different individuals using machine learning, specifically Support Vector Machine (SVM) algorithm with Principal Component Analysis (PCA).

## Project Overview

This project demonstrates a complete face recognition pipeline using Support Vector Machine (SVM) with the following features:

- Face detection using Haar Cascade Classifier
- Feature extraction and dimensionality reduction using Principal Component Analysis (PCA)
- Face classification using Support Vector Machine (SVM) with RBF kernel
- Real-time face recognition from images

The system can identify three persons: Barack Obama, Donald Trump, and George W. Bush.

## Repository Structure

```
├── 2.0 Creating the dataset.ipynb     # Notebook for creating face dataset from training images
├── 2.0 SVM demonstration.ipynb        # Simple SVM demonstration on a weather dataset
├── 3.0 Train the SVM.ipynb            # SVM model training with PCA pipeline
├── 4.0 Testing the SVM Model.ipynb    # Testing the trained model on new images
├── data.npy                           # Processed face data (numpy array)
├── target.npy                         # Target labels (numpy array)
├── haarcascade_frontalface_default.xml # Haar cascade classifier for face detection
├── SVM-Face Recognition.sav          # Saved trained model
├── linear-insperable-dataset.csv      # Sample dataset for SVM demonstration
├── test_data/                         # Test images for model evaluation
└── train_data_2/                      # Training images organized by person
    ├── Barack Obama/
    ├── Donald Trump/
    └── George W Bush/
```

## Prerequisites

- Python 3.6+
- Required packages:
  - numpy
  - opencv-python (cv2)
  - scikit-learn
  - matplotlib
  - joblib

You can install the required packages using pip:

```bash
pip install numpy opencv-python scikit-learn matplotlib joblib
```

## Project Workflow

### 1. Dataset Creation

The notebook `2.0 Creating the dataset.ipynb` processes training images to:
- Detect faces using Haar Cascade Classifier
- Crop and resize detected faces to 50x50 pixels
- Create labeled datasets saved as numpy arrays (`data.npy` and `target.npy`)

### 2. Model Training

The notebook `3.0 Train the SVM.ipynb` demonstrates:
- Loading the processed face data
- Creating a pipeline with PCA (150 components) and SVM (RBF kernel)
- Splitting data into training and testing sets
- Training the model and evaluating its accuracy
- Saving the trained model to `SVM-Face Recognition.sav`

### 3. Model Testing

The notebook `4.0 Testing the SVM Model.ipynb` shows how to:
- Load the trained model
- Process test images for face detection
- Classify detected faces
- Display results with bounding boxes and predicted names

## Using the Face Recognition System

### Creating Your Own Dataset

1. Organize your training images in folders named after the person (e.g., `/train_data_2/Person_Name/`)
2. Run the cells in `2.0 Creating the dataset.ipynb` to process these images
3. The script will detect faces, and you can confirm each detection by pressing 'y'

### Training the Model

Run all cells in `3.0 Train the SVM.ipynb` to:
- Load the processed face data
- Train the SVM model with PCA
- Evaluate the model's performance
- Save the trained model

### Testing the Model

1. Place test images in the `test_data` folder
2. Run the cells in `4.0 Testing the SVM Model.ipynb`
3. The system will detect faces in each image and predict their identities

## Performance

The model is evaluated using:
- Accuracy score
- Classification report (precision, recall, f1-score)
- Confusion matrix

## SVM Demonstration

The notebook `2.0 SVM demonstration.ipynb` provides a simple visualization of how SVM works on a weather dataset (temperature and humidity to predict rain). This demonstration helps understand the basic principles of SVM before applying it to the more complex face recognition problem.

## License

[Specify your license here]

## Author

Rensith Udara

## Acknowledgements

- OpenCV for the Haar Cascade Classifier
- Scikit-learn for the SVM implementation
- [Any other acknowledgements]

---
**Note:** This face recognition system is designed for educational purposes. For production applications, consider more robust face recognition approaches like deep learning-based methods.