# ❤️ Heart Disease Prediction Application

A machine learning application that predicts the probability of heart disease based on patient health data. This project implements a complete MLOps workflow including data preprocessing, model training, and a user-friendly Streamlit interface.

## 📋 Features

- **Individual Patient Prediction**: Enter patient details and get an instant prediction
- **Batch Prediction**: Upload CSV files for processing multiple patient records
- **Model Explanation**: Understand feature importance and how predictions are made
- **Comprehensive Logging**: Track all operations for auditability
- **Production-ready Architecture**: Modular, maintainable codebase following MLOps best practices

## 🏗 Project Structure

```
heart-disease-prediction/
├── app.py                              # Streamlit interface
├── main.py                             # Application logic control
├── data_processing.py                  # Data preprocessing pipeline
├── ml_functions.py                     # Model training and prediction
├── helper_functions.py                 # Logging and utility functions
├── data/                               # Data directory
│   ├── raw/                           # Raw input data
│   ├── processed/                     # Processed data
│   └── output/                        # Prediction outputs
├── artifacts/                          # Model artifacts
│   ├── heart_disease_model.pkl        # Trained model
│   └── data_processing_pipeline.pkl   # Preprocessing pipeline
├── logs/                               # Application logs
└── .env                               # Environment variables
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- pip or conda for package management

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/heart-disease-prediction.git
   cd heart-disease-prediction
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Create a `.env` file in the project root with the following variables:**
   ```env
   DATA_DIR=data
   ARTIFACTS_DIR=artifacts
   LOGS_DIR=logs
   ```

### Running the Application

1. **Train the model (if not already trained):**
   ```bash
   python main.py
   ```

2. **Launch the Streamlit application:**
   ```bash
   streamlit run app.py
   ```

3. **Open your browser and navigate to** `http://localhost:8501`

## 💻 Usage

### Single Patient Prediction

1. Navigate to "Single Prediction" in the sidebar
2. Enter patient details including age, sex, chest pain type, etc.
3. Click "Predict" to see the heart disease risk assessment

### Batch Prediction

1. Navigate to "Batch Prediction" in the sidebar
2. Prepare a CSV file with the required columns (see format in the app)
3. Upload the CSV file and click "Run Batch Prediction"
4. Download the results with predictions added

### Model Explanation

1. Navigate to "Model Explanation" in the sidebar
2. View feature importance chart and medical interpretation

## 🔧 Technical Details

### Model Information

- **Algorithm**: Random Forest Classifier
- **Features**: Age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, ECG results, max heart rate, exercise-induced angina, ST depression, ST slope
- **Preprocessing**: Standardization for numerical features, one-hot encoding for categorical features
- **Metrics**: Accuracy, precision, recall, F1-score, ROC AUC

### Data Format

The application expects heart disease data with the following features:

| Feature | Description | Type |
|---------|-------------|------|
| `age` | Age in years | Numerical |
| `sex` | Sex (1 = male, 0 = female) | Binary |
| `cp` | Chest pain type (0-3) | Categorical |
| `trestbps` | Resting blood pressure in mm Hg | Numerical |
| `chol` | Serum cholesterol in mg/dl | Numerical |
| `fbs` | Fasting blood sugar > 120 mg/dl (1 = true, 0 = false) | Binary |
| `restecg` | Resting ECG results (0-2) | Categorical |
| `thalach` | Maximum heart rate achieved | Numerical |
| `exang` | Exercise induced angina (1 = yes, 0 = no) | Binary |
| `oldpeak` | ST depression induced by exercise | Numerical |
| `slope` | Slope of the peak exercise ST segment (0-2) | Categorical |
| `target` | Heart disease diagnosis (1 = present, 0 = absent) | Binary |

## 📊 Model Performance

- **Accuracy**: ~85% (varies with dataset)
- **Precision**: ~84%
- **Recall**: ~86%
- **F1 Score**: ~85%
- **ROC AUC**: ~0.90

## 🔬 Future Improvements

- Add more advanced explainability with SHAP and LIME
- Implement model monitoring for drift detection
- Add cross-validation for more robust model evaluation
- Enhance the UI with interactive visualizations
- Add user authentication for clinical settings

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- [UCI Heart Disease Dataset](https://archive.ics.uci.edu/ml/datasets/heart+disease)
- [Streamlit](https://streamlit.io/) for the user interface framework
- [scikit-learn](https://scikit-learn.org/) for machine learning tools

## 📞 Contact

For questions or feedback, please open an issue on the GitHub repository or contact the maintainer at your-email@example.com.

---

**Note**: This application is for educational and research purposes only. It should not be used as a substitute for professional medical advice, diagnosis, or treatment.
