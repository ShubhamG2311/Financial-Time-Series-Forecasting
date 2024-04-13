# Financial Time Series Forecasting using Deep Learning

This project explores the application of deep learning techniques for financial time series forecasting, specifically for predicting stock prices. The main objective is to develop accurate models for forecasting future values in time series data by leveraging various deep learning architectures and innovative approaches.

## Problem Statement

The project delves into the real-world problem of time series forecasting, examining various techniques alongside the well-established Long Short-Term Memory (LSTM) methods. Furthermore, it explores innovative approaches such as encoding time series data as images and utilizing Convolutional Neural Networks (CNNs), ResNets, and LSTMs for prediction. The premise lies in CNN's adeptness at learning from 2-dimensional image data, potentially enhancing forecasting accuracy by capturing intricate spatial patterns, while retaining comprehensive information from the financial data.

## Dataset

The project utilizes the hourly AAPL stock price data from Yahoo Finance (Uploaded on Kaggle). The dataset contains opening, high, low, and closing prices for each hour from 2022-05-11 to 2024-04-10.

## Approaches

The following models (or sequential combinations of models) have been implemented and compared:

1. **Simple LSTM**: A baseline approach using a simple LSTM model on the time series data.
2. **CNN on GADF Images**: Generating Gramian Angular Difference Field (GADF) images from the time series data and training a CNN model to predict the 'close price' directly.
3. **LSTM on GADF Images**: Utilizing a sequence of GADF images as input to an LSTM model, with the 'close_price' as the target variable.
4. **CNN Feature Extraction and LSTM Forecasting**: A two-stage model where a pre-trained CNN (e.g., ResNet-50) is employed as a feature extractor to obtain embeddings from the GADF-encoded images, which are then fed into an LSTM network for forecasting future stock prices using a sliding window approach.

## Results

### 1. Using Simple LSTM on the time series data: 
![image](https://github.com/ShubhamG2311/Financial-Time-Series-Forecasting/assets/76262127/2fd54c13-689c-49da-a7af-5fef189ccf0e)

### 2. Using CNN on the GADF generated images: 
![image](https://github.com/ShubhamG2311/Financial-Time-Series-Forecasting/assets/76262127/1ee2f202-4e60-4d0d-8742-cf6349e84130)

### 3. Using LSTM on the GADF generated images (LSTM Image Model):
![image](https://github.com/ShubhamG2311/Financial-Time-Series-Forecasting/assets/76262127/8db7ab79-0434-4803-b021-4ca619769ccf)

### 4. Using ResNet-18 to encode images and passing embeddings to LSTM With Encoded Input:
![image](https://github.com/ShubhamG2311/Financial-Time-Series-Forecasting/assets/76262127/ec3c82a5-b336-402c-a081-3c32ac7c03b9)


The project demonstrates that the approach of using a pre-trained ResNet as a feature extractor, followed by an LSTM for forecasting, yields the most promising results, effectively capturing both spatial patterns in GADF images and temporal dependencies in time series data.

## Code

The code for this project can be found in the provided Colab notebook. The notebook includes data preprocessing, model implementation, training, and evaluation steps for the different approaches explored.

To run the code, you can open the Colab notebook and execute the cells sequentially. Alternatively, you can download the notebook and run it locally with the required dependencies installed.

## Future Scope

The project highlights the potential for further improvement in time series prediction performance by exploring better time-series-specific image generation techniques and fine-tuning the proposed architectures. Future work could focus on optimizing the models for specific financial applications, such as high-frequency trading or medical time series prediction.

## References

The report includes relevant references used in the project, such as research papers and online resources.
