# **NeuroCast**
## **Project Proposal**
*Comparative CO2 Forecasting with MLP, MA, and ARIMA on Mauna Lua Data*

## **Objective**

This project aims to evaluate and compare the performance of three forecasting models for predicting monthly CO2 levels at the Mauna Lua observatory:

* **Multi-Layer Perceptron (MLP) :** A neural network architecture capable of learning complex relationships within the data.
* **Moving Average (MA) :** A simple statistical method that averages the past `K` observations to predict the next `T` values.
* **Autoregressive Integrated Moving Average (ARIMA) :** A more advanced statistical model that incorporates both past values and past errors to forecast future observations.

## **Methodology**

1. **Data Acquisition :** Obtain the monthly [Mauna Lua CO2 dataset](https://gml.noaa.gov/webdata/ccgg/trends/co2/co2_mm_mlo.csv).
2. **Data Preprocessing :** Address missing values (if any) and normalize the data for improved model training.
3. **Model Implementation :**
    * **MLP :** Develop an MLP architecture with `K` input neurons representing the past `K` CO2 readings and one output neuron predicting the next `T` value. Training the model using an appropriate optimizer and loss function (e.g., Adam optimizer, Mean Squared Error loss).
    * **MA :** Implementing a rolling window approach to calculate the average of the past `K` observations for each prediction.
    * **ARIMA :** Utilize a library like statsmodels to establish an optimal ARIMA model.
4. **Evaluation :**
    * Split the data into training and testing sets.
    * Train each model on the training set.
    * Generate forecasts for the next `T` values on the testing set using each model.
    * Evaluate the performance of each model using metrics like Mean Squared Error (MSE), Root Mean Squared Error (RMSE)
    * Visualize the actual CO2 values against the predicted values for each model to compare their accuracy.
5. **Results and Discussion :**
    * Analyze the performance metrics and visualizations to identify the most effective forecasting model for this dataset and configuration (`K` and `T`).
    * Discuss the potential reasons for the observed results, considering factors like model complexity (MLP's ability to capture non-linear relationships), seasonality in the data (potential advantage for ARIMA), and the impact of data quality and length on model training.

## **Expected Outcomes**

This project will provide valuable insights into the suitability of different forecasting methods for CO2 prediction on the Mauna Lua dataset. By comparing the performance of MLP, MA, and ARIMA, we can gain a better understanding of the trade-offs between model complexity and accuracy in this specific context.
