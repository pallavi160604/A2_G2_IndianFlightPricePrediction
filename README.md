# A2_GRP2


# Flight Price Prediction using Machine Learning

## Project Title and Objective

**Title:** Flight Price Prediction using Machine Learning
**Objective:**
The objective of this project is to develop a regression model that predicts airline ticket prices based on factors such as airline, route, journey date, duration, and number of stops. The project builds a complete preprocessing and modeling pipeline in Google Colab and allows users to input flight details to obtain price predictions.

---

## Dataset Details

The dataset contains historical flight pricing information with columns such as:

* Airline
* Source
* Destination
* Date_of_Journey
* Dep_Time
* Arrival_Time
* Duration
* Total_Stops
* Additional_Info
* Price (target variable)

Key preprocessing steps performed:

* Handling missing values
* Extracting journey day and month
* Converting time columns into hour and minute
* Parsing duration into numerical values
* Encoding categorical features using OneHotEncoder
* Applying log transformation on the Price column to reduce skewness

---

## Algorithm / Model Used

The model is built using the following components:

* **ColumnTransformer** for preprocessing
* **OneHotEncoder** for categorical variables
* **StandardScaler** for numerical features
* **GradientBoostingRegressor** as the final regression model
* **Log-Transformation:** `np.log1p` applied on target values
* **Inverse Transformation:** `np.expm1` applied on predictions

All steps are combined into a scikit-learn pipeline.

---

## Results

The model was evaluated using standard regression metrics. Key results include:

* **R² Score:** Indicates how well the model explains price variance
* **RMSE:** Measures prediction error in the original price scale
* **MAE:** Average absolute difference between actual and predicted prices
* **MAPE:** Percentage error between actual and predicted values
* **Explained Variance Score:** Measures proportion of variability explained

The model demonstrates strong performance after log transformation and boosting-based regression.

---

## Conclusion

The project successfully demonstrates a complete machine learning workflow for flight price prediction. The Gradient Boosting model, combined with proper preprocessing and log transformation, provides reliable predictions. Users can directly enter flight details in the Colab notebook and obtain expected price estimates. This model highlights the importance of feature engineering and end-to-end automation in price prediction tasks.

---

## Future Scope

* Hyperparameter tuning for improved accuracy
* Comparison with additional models such as Random Forest, XGBoost, or Neural Networks
* Increasing dataset size for better generalization
* Deployment using Flask, FastAPI, or Streamlit
* Integration with a graphical interface such as Gradio

---

## References

* Scikit-learn Documentation
* Pandas Documentation
* NumPy Documentation
* Public Flight Price Dataset (Kaggle)

