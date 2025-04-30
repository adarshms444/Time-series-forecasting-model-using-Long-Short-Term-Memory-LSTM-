
# Air Passenger Forecasting using LSTM - Results

This project involves forecasting the number of monthly international air passengers using an LSTM (Long Short-Term Memory) model. The analysis includes data loading, preprocessing, model building, prediction, and evaluation.

## Contents of the Result File

1. *Raw Dataset Visualization:*
    Displays the trend of monthly air passengers from the dataset.

2. *Normalized and Sequenced Data:*
    Data is scaled using MinMaxScaler and prepared into input-output sequences for the LSTM model.

3. *LSTM Model Training:*
    A two-layer LSTM model is trained using the scaled data with dropout for regularization.

4. *Forecasted vs Actual Graph:*
    A graph comparing the actual and predicted values on the test dataset.

5. *Model Evaluation Metrics:*
    - Mean Squared Error (MSE)
    - Mean Absolute Error (MAE)

 How the Analysis Was Performed

--> Step 1: Importing Libraries
- Imported NumPy, Pandas, Matplotlib for data handling and visualization.
- Imported Keras and Sklearn for model building and evaluation.

--> Step 2: Loading the Dataset
- Read the dataset from "AirPassengers (1).csv" and set the 'Month' column as a DateTime index.

--> Step 3: Visualizing Raw Data
- Used Matplotlib to plot the raw time series data.

--> Step 4: Preprocessing the Data
- Applied MinMaxScaler to normalize passenger numbers.
- Created sequences of data for time series input to LSTM.

--> Step 5: Splitting the Data
- Split the dataset into 80% training and 20% testing data.
- Reshaped the input data to fit LSTM input format.

--> Step 6: Building and Training the LSTM Model
- Constructed a model with:
    - LSTM (128 units) + Dropout (0.4)
    - LSTM (100 units) + Dropout (0.4)
    - Dense output layer
- Trained for 100 epochs with batch size of 8.

--> Step 7: Making Predictions
- Predicted on the test set and inverse-transformed the scaled values back to actual numbers.

--> Step 8: Visualizing Results
- Plotted both actual and predicted passenger values to evaluate model performance visually.

--> Step 9: Evaluating the Model
- Calculated and printed:
    - Mean Squared Error (MSE)
    - Mean Absolute Error (MAE)
