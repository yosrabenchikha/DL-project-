# DL-project_

This project uses an Artificial Neural Network (ANN) built with TensorFlow/Keras to predict the presence of heart disease based on patient medical data.

## 📁 Dataset

The dataset used is `Heart_Disease_Prediction.csv`, which contains medical attributes of patients and a target column indicating whether heart disease is present.

## 🚀 Features

- Data loading and exploratory analysis
- Null value and duplicate row checking
- Label encoding for target variable
- Train-test splitting (75%-25%)
- Feature scaling using `StandardScaler`
- Deep learning model (ANN) with:
  - Multiple dense layers
  - Batch normalization
  - Dropout for regularization
  - He normal kernel initialization
- Early stopping to prevent overfitting
- Performance evaluation using confusion matrix and accuracy score

## 🧠 Model Architecture

| Layer | Units | Activation | Regularization |
|-------|-------|------------|----------------|
| Dense | 128   | ReLU       | BatchNorm + Dropout (0.5) |
| Dense | 64    | ReLU       | BatchNorm + Dropout (0.5) |
| Dense | 32    | ReLU       | BatchNorm + Dropout (0.5) |
| Dense | 16    | ReLU       | BatchNorm + Dropout (0.5) |
| Dense | 8     | ReLU       | BatchNorm + Dropout (0.5) |
| Dense | 1     | Sigmoid    | - |

## ⚙️ Compilation

- **Optimizer**: Adam
- **Loss function**: Binary Crossentropy
- **Metrics**: Accuracy

## 📊 Training

- **Batch size**: 40
- **Epochs**: 200 (with early stopping)
- **Validation split**: 20% of training data
- **Early stopping patience**: 10 epochs

## 📈 Evaluation

The model is evaluated using:

- Confusion matrix
- Accuracy score

## ▶️ How to Run

1. Clone the repository or download the script.
2. Place `Heart_Disease_Prediction.csv` in the `/content/` directory (or update the file path).
3. Run the script in a Python environment with the required libraries installed.

### Required Libraries

- numpy
- pandas
- tensorflow
- scikit-learn
- matplotlib

Install missing libraries using:

```bash
pip install numpy pandas tensorflow scikit-learn matplotlib
