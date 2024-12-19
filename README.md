# Final Project 1
# Uber and Lyft Cab Price Prediction

This repository contains the implementation of a data analysis and predictive modeling project aimed at estimating the price of cab services (Uber and Lyft) using a Linear Regression model. The project combines data preprocessing, machine learning, and web application deployment to create a user-friendly cab price prediction tool.

## Key Features
- **Machine Learning Model**: A Linear Regression model trained to predict cab prices based on relevant features.
- **Data Preprocessing**: Cleaned and prepared dataset to ensure reliable predictions.
- **Web Application**: Flask-based app for user interaction, allowing users to input ride details and get predictions in real-time.
- **Deployment Ready**: Configured for deployment on platforms like Heroku using `Procfile` and `gunicorn`.

## Repository Structure
```
.
├── model
│   └── linear_regression.pkl   # Trained Linear Regression model.
├── static
│   ├── css
│   │   ├── legends.png         # Legend image for the app.
│   │   └── style.css           # CSS file for styling the front end.
├── templates
│   └── main.html               # Front-end HTML file for user interaction.
├── Procfile                    # Configuration file for deployment.
├── app.py                      # Flask application script.
└── README.md                   # Project documentation (this file).
```

## How It Works
1. **Input Features**:
   - `cab_type`: Indicates the type of cab (0 for Lyft, 1 for Uber).
   - `distance`: The distance of the ride (e.g., in miles).
   - `surge_multiplier`: Surge pricing factor (e.g., 1, 1.25, etc.).
   - `name`: Name of the cab type (e.g., UberX, LyftXL).
   - `source` and `destination`: Start and end locations.

2. **Model Prediction**:
   - The trained Linear Regression model predicts the cab price based on the input features.

3. **Output**:
   - Displays the predicted price in the web interface.

## Installation and Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/safrip2/FinalProject1_PYTN.git
   cd FinalProject1_PYTN
   ```
2. Install required Python packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Flask application:
   ```bash
   python app.py
   ```
4. Access the app at `http://127.0.0.1:5000/` in your web browser.

## Deployment
To deploy the app on platforms like Heroku:
1. Ensure `Procfile` and all dependencies are properly configured.
2. Deploy using the Heroku CLI:
   ```bash
   heroku create
   git push heroku main
   ```

## Example Usage
1. Open the web application.
2. Fill in the form with details like cab type, distance, surge multiplier, etc.
3. Click "Predict" to get the estimated cab price.

## Future Improvements
- Add support for additional machine learning models to compare predictions.
- Integrate more features for improved accuracy (e.g., weather conditions, traffic data).
- Enhance the UI/UX for better user experience.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---
## Dataset: https://www.kaggle.com/datasets/brllrb/uber-and-lyft-dataset-boston-ma/download?datasetVersionNumber=2
