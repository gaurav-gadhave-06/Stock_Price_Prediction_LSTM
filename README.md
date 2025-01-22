# Stock Price Prediction Using LSTM Neural Network

This project utilizes a Long Short-Term Memory (LSTM) neural network to predict stock prices. It involves data preprocessing, model training, validation, and forecasting future stock prices, with a focus on interpreting performance metrics and generating visual insights.

---

## 📌 Project Motivation

Stock price prediction is a challenging problem due to the complexity and randomness of financial markets. The goal of this project is to:

1. **Analyze historical stock data** to identify trends and patterns.
2. **Train a predictive model** to forecast future prices using an LSTM neural network.
3. **Validate model accuracy** using metrics such as RMSE and R² Score.
4. **Generate actionable insights** by visualizing predictions alongside actual stock prices.

---

## 🧠 Methodology

### 1. **Data Preprocessing**
- Loaded historical stock price data (e.g., CSV format).
- Extracted the `CLOSE` price for analysis.
- Split the data into training and validation datasets.
- Normalized the data using MinMaxScaler for faster convergence during training.

### 2. **Model Architecture**
- **LSTM Layers**: Used to capture temporal dependencies in sequential data.
  - First LSTM layer with 128 units and `tanh` activation.
  - Second LSTM layer with 64 units.
- **Dropout Layers**: Added to prevent overfitting.
- **Dense Layers**: Final layers for regression to predict the next price.
- **Optimizer**: Adam optimizer for adaptive learning rates.
- **Loss Function**: Mean Squared Error (MSE).

### 3. **Model Training**
- Trained the model on 80% of the dataset.
- Used 20% of the training data for validation.
- Batch size: 32
- Epochs: 20 (adjusted for optimal performance).

### 4. **Validation and Metrics**
- Evaluated model performance on unseen validation data using:
  - **Root Mean Squared Error (RMSE)**: Measures prediction error magnitude.
  - **R² Score**: Determines how well the model explains variance in the data.
  
### 5. **Future Predictions**
- Forecasted the next 30 days of stock prices using the last 60 days of data as input.
- Visualized predictions alongside historical trends.

---

## 🚀 How to Run the Project

### Prerequisites
- Python 3.7+
- TensorFlow/Keras
- Pandas
- NumPy
- Matplotlib
- scikit-learn

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name/stock-price-prediction
   cd stock-price-prediction
