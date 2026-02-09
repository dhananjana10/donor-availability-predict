# 🩸 Donor Availability Predictor

A machine learning-powered web application that predicts blood donor availability using logistic regression and advanced feature engineering.


## 🎯 Features

- **ML-Powered Predictions**: Logistic regression model with enhanced feature engineering
- **Interactive Web App**: Streamlit-based user interface
- **User Authentication**: Secure sign-in/sign-up system
- **PDF Reports**: Generate detailed prediction reports
- **Multi-City Support**: Predictions for multiple Australian cities
- **Blood Type Analysis**: Support for all major blood groups

## 🏗️ Project Structure

```
donor_app_full/
├── app/                          # Streamlit web application
│   ├── app.py                   # Main application file
│   ├── requirements.txt         # Python dependencies
│   ├── users.json              # User authentication data
│   └── pages/                  # Multi-page app structure
│       ├── Sign_In.py          # Login page
│       └── Sign_Up.py          # Registration page
├── data/                        # Dataset files
│   ├── Blood_Donor_updated.csv # Original dataset
│   └── clean_donor.csv         # Processed dataset
├── models/                      # Trained ML models
│   ├── final_model.pkl         # Enhanced accuracy model
│   ├── simple_model.pkl        # Basic compatibility model
│   ├── metrics.json            # Model performance metrics
│   └── simple_metrics.json     # Basic model metrics
├── Donor_Availability_Predictor.ipynb  # ML training notebook
└── README.md                   # This file
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- pip package manager

### Installations

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd donor_app_full
   ```

2. **Install dependencies:**
   ```bash
   cd app
   pip install -r requirements.txt
   ```

3. **Run the application:**
   ```bash
   streamlit run app.py
   ```

4. **Access the app:**
   Open your browser and navigate to `http://localhost:8501`

## 📊 Model Performance

### Enhanced Model
- **Accuracy**: 100% (with enhanced features)
- **F1-macro**: 1.0
- **ROC-AUC**: 1.0

### Simple Model (App Compatible)
- **Accuracy**: 51.96%
- **F1-macro**: 51.95%
- **ROC-AUC**: 51.87%

## 🔧 Usage

1. **Sign Up/Sign In**: Create an account or log in to existing account
2. **Enter Donor Information**:
   - Select city from dropdown
   - Choose blood group
   - Enter donation history (months, count, pints)
   - Set created date
3. **Get Prediction**: Click "Predict" to get availability probability
4. **Download Report**: Generate PDF report with prediction details

## 🛠️ Development

### Training New Models

Open and run the Jupyter notebook:
```bash
jupyter notebook Donor_Availability_Predictor.ipynb
```

The notebook includes:
- Data loading and preprocessing
- Feature engineering
- Model comparison and selection
- Model saving and evaluation

### App Structure

- **app.py**: Main Streamlit application with prediction logic
- **pages/**: Authentication pages for multi-page app
- **Authentication**: File-based user management with password hashing

## 📈 Features Engineering

The model uses various engineered features:
- **Basic Features**: City, blood group, donation history
- **Time Features**: Year, month, day components
- **Enhanced Features**: Donation frequency, commitment scores, availability indicators

## 🔐 Security

- Password hashing using PBKDF2
- Session-based authentication
- File-based user storage (not for production)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built with Streamlit for the web interface
- Uses scikit-learn for machine learning
- ReportLab for PDF generation