
# Flower Image Classification Using CNN

## 1. Project Overview

This project implements a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify flower images into five categories. It demonstrates the complete deep learning workflow, including dataset loading, image preprocessing, data splitting, CNN model development, training, evaluation, prediction, and performance analysis.

The project is developed as part of **Assignment 9 – CNN Model for Image Classification**.

## 2. Objectives

- Load and preprocess a flower image dataset.
- Split the dataset into training, validation, and testing sets.
- Build a CNN model for multi-class image classification.
- Train the model and monitor its performance.
- Evaluate the model using test accuracy, test loss, and classification metrics.
- Visualize training and validation performance.
- Identify possible improvements to the model.

## 3. Dataset

The project uses the TensorFlow Flower Photos dataset, which contains images from five flower categories:

- Daisy
- Dandelion
- Roses
- Sunflowers
- Tulips

**Dataset source:** [TensorFlow Flower Photos Dataset](https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz)

### Dataset preprocessing

- Images are resized to **96 × 96 pixels**.
- Images are processed as RGB images.
- A maximum of 100 images per class is selected for this experiment.
- The dataset is split into:
  - 70% training data
  - 15% validation data
  - 15% testing data
- Stratified splitting is used to maintain class proportions.

The notebook downloads and extracts the dataset automatically when needed. The downloaded archive is also tracked in this repository using Git Large File Storage (Git LFS).

## 4. Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- Git and Git LFS

## 5. Project Workflow

### Task 1: Load and Preprocess the Dataset

The flower dataset is loaded using TensorFlow's image dataset utilities. Images are resized, class labels are collected, and the data is split into training, validation, and testing sets. Sample images are visualized to understand the dataset.

### Task 2: Build the CNN Model

A Sequential CNN architecture is developed using the following layers:

- Rescaling layer for pixel normalization
- Convolutional layers with 16, 32, and 64 filters
- Max pooling layers
- Global average pooling layer
- Dense layer with 64 neurons
- Dropout layer with a rate of 0.3
- Softmax output layer for five-class classification

### Task 3: Compile and Train the Model

The model is compiled using:

- **Optimizer:** Adam
- **Loss function:** Sparse categorical cross-entropy
- **Evaluation metric:** Accuracy
- **Training epochs:** 15
- **Batch size:** 16

Training and validation performance are monitored during training.

### Task 4: Evaluate the Model

The trained CNN is evaluated using the test dataset. The notebook reports test loss, test accuracy, and a classification report containing precision, recall, and F1-score for each flower class.

A sample test image is also used to compare the actual flower category with the predicted category and display the model's confidence.

### Task 5: Performance Analysis and Improvements

Training and validation accuracy and loss curves are plotted to understand the model's learning behavior and identify possible overfitting.

Potential improvements include:

1. Increasing the number of training images per class.
2. Applying image augmentation, such as random flips and rotations.
3. Tuning the number of filters, learning rate, and training epochs.
4. Experimenting with a pretrained model such as MobileNetV2.
5. Reviewing misclassified images and comparing different model configurations.

## 6. Model Evaluation

The notebook calculates test accuracy and test loss after training. It also generates a classification report for each flower category.

| Evaluation Metric | Result |
|---|---|
| Test Accuracy | 66.67% |
| Test Loss | 1.0788 |

*Note: These values represent a recorded run. Results may vary depending on the execution environment and training configuration. Refer to the latest notebook output for the results of your current run.*

## 7. Visualizations and Outputs

The project generates:

- Sample images from the dataset
- Training and validation accuracy curves
- Training and validation loss curves
- Actual versus predicted flower classification for a sample image
- Classification report
- Saved trained model files

The training and validation plots are saved in the `output_images/` directory.

## 8. Project Structure

```text
Assignment-9---CNN-Model-for-Image-Classification/
│
├── dataset/
│   └── flower_photos.tgz
│
├── model/
│
├── notebook/
│   └── Assignment 9 CNN Model for Image Classification.ipynb
│
├── output_images/
│   └── training_validation_curves.png
│
├── .gitattributes
├── .gitignore
├── requirements.txt
└── README.md
```

The exact files inside `model/`, `notebook/`, and `output_images/` may vary depending on the files saved during execution.

## 9. Installation and Execution

### Step 1: Clone the repository

```bash
git clone https://github.com/dvsan10/Assignment-9---CNN-Model-for-Image-Classification.git
cd Assignment-9---CNN-Model-for-Image-Classification
```

### Step 2: Install Git LFS

Install Git LFS from [git-lfs.com](https://git-lfs.com/) if it is not already installed.

Initialize Git LFS:

```bash
git lfs install
```

Download the LFS-managed files:

```bash
git lfs pull
```

### Step 3: Create a virtual environment (optional)

```bash
python -m venv venv
```

On Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### Step 4: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 5: Run the notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook in the `notebook/` directory and run all cells in order.

The notebook may download the dataset automatically if it is not already available in the expected location.

## 10. Future Enhancements

- Apply data augmentation to improve generalization.
- Experiment with different CNN architectures and hyperparameters.
- Use transfer learning with MobileNetV2.
- Add a confusion matrix to analyze class-wise misclassification.
- Build a simple interface for predicting flower categories from uploaded images.

## 11. Conclusion

This project demonstrates the implementation of a CNN-based image classification system using TensorFlow and Keras. The workflow covers data preparation, model development, training, evaluation, prediction, and performance analysis. The evaluation results provide a baseline for further experimentation, while image augmentation, hyperparameter tuning, and transfer learning offer opportunities to improve classification performance.

## Author

**Dharun Vikash**

GitHub: [@dvsan10](https://github.com/dvsan10)
