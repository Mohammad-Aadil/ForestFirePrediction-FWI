## Forest Fire Prediction using FWI

This is a Flask web application that predicts the Fire Weather Index (FWI) based on user-provided input. The FWI is a numerical rating that represents the fire potential of the forest. The application uses machine learning models to make predictions.

Dataset Information

The dataset used for training the machine learning model includes weather data observations from two regions of Algeria: the Bejaia region located in the northeast and the Sidi Bel-abbes region located in the northwest. The dataset contains 244 instances with 11 attributes and 1 output attribute (Classes) that classifies instances into "fire" and "not fire" classes.

Attribute Information

Date: Day, month (June to September), year (2012).
Temperature: Temperature at noon (maximum temperature) in Celsius degrees (range: 22 to 42).
RH (Relative Humidity): Relative Humidity in percentage (range: 21 to 90).
Ws (Wind Speed): Wind speed in km/h (range: 6 to 29).
Rain: Total day rain in mm (range: 0 to 16.8).
FFMC (Fine Fuel Moisture Code): Index from the FWI system (range: 28.6 to 92.5).
DMC (Duff Moisture Code): Index from the FWI system (range: 1.1 to 65.9).
ISI (Initial Spread Index): Index from the FWI system (range: 0 to 18.5).
Classes: Two classes, "fire" and "not fire".
Region: Represents the region of Algeria (0 for Bejaia Region, 1 for Sidi-Bel Abbes Region).

Installation and Setup
1. Clone the repository to your local machine:
bash
Copy code
git clone [repository_url.git]

2. Install the required dependencies by running:
bash
Copy code
pip install -r requirements.txt

3. Run the Flask application:
bash
Copy code
python app.py
Access the application in your web browser at http://127.0.0.1:5000/.

Usage
1. Open the web application in your web browser.
2. Enter the required input data for the FWI prediction: Temperature, RH, Ws, Rain, FFMC, DMC, ISI, Classes (fire or not fire), and Region (0 for Bejaia Region, 1 for Sidi-Bel Abbes Region).
3. Click the "Predict" button.
4. The application will predict the FWI based on the provided input and display the result.

## Model Information
The Flask application uses machine learning models to make FWI predictions. The Ridge Regression model was trained on the Algerian Forest Fires Dataset. The model was saved using pickle and is loaded during runtime for making predictions.

## Data Cleaning and Preprocessing
The dataset was cleaned and preprocessed to remove missing values, fix column names, and convert the required columns to the appropriate data types.

## Exploratory Data Analysis (EDA)
EDA was performed to gain insights into the dataset. Visualizations such as histograms, density plots, pie charts, and box plots were used to analyze the data.

## Feature Selection and Scaling
Correlation analysis was performed to identify multicollinearity. Features with correlation coefficients greater than 0.85 were dropped to prevent collinearity issues. The data was then standardized using StandardScaler to ensure all features are on the same scale for better model performance.

## Machine Learning Models

The following machine learning models were trained and evaluated:

- Linear Regression
- Lasso Regression
- Ridge Regression
- ElasticNet Regression
- The Ridge Regression model showed the best performance, and it was used for the FWI prediction in the web application.

## Contact
For any questions or inquiries, please contact:

Your Name: Mohammad Aadil
Email: shaikhaadil8855@gmail.com