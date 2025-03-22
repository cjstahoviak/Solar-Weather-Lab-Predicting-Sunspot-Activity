# Solar Weather Lab: Predicting Sunspot Activity
University of New Mexico course, ST: Advanced Machine Learning, Lab 1

## Introduction
Have you ever wondered how the Sun's activity influences space weather and even life on Earth? Sunspots — dark, cooler regions on the Sun’s surface - are closely tied to solar storms that can disrupt satellites, GPS, and even power grids. Understanding and predicting sunspot activity is crucial for space weather forecasting.

In this lab, you’ll experiment with sequence modeling using some of the techniques we have covered in class to predict sunspot numbers. We'll use real NASA data and train various sequence models, including Recurrent Neural Networks (RNNs), Gated Recurrent Units (GRUs), Long Short-Term Memory (LSTM) networks, and the state-of-the-art Mamba model. You will fine-tune these models and optimize hyperparameters to improve RMSE accuracy. By the end, you’ll gain hands-on experience with time series forecasting and sequence learning, all while unraveling the mysteries of our star!

## Objectives
- Fetch and preprocess real-world NASA Sunspot data.
- Apply sequence modeling techniques for time series forecasting.
- Implement and train RNN, GRU, LSTM, and Mamba models using PyTorch.
- Tune hyperparameters and optimize models for improved RMSE accuracy.
- Evaluate model performance and visualize predictions.

## Prerequisites
Before starting, ensure you have:
- Basic knowledge of Python and PyTorch.
- Familiarity with neural networks and sequence modeling (RNNs, GRUs, LSTMs, Mamba).
- Experience with data preprocessing and time series analysis.

## Dataset
We will use NASA’s **Sunspot & Solar Weather Data**, fetched from:
[NOAA Solar Cycle Sunspots JSON](https://services.swpc.noaa.gov/json/solar-cycle/sunspots.json)
This dataset includes historical sunspot counts and solar flux data, essential for understanding solar activity cycles.

---

## Lab Steps

### Preprocessing
   - Retrieve the NASA’s **Sunspot & Solar Weather Data**.  
   - Normalize the data and handle missing values (minmax scaler is provided).  
   - Convert the dataset into sequences (48 past time steps are provided)


### Implement Sequence Models

You will implement and compare the following models:

- **Simple RNN**
 - Implement a single-layer RNN to process seismic time-series data.
 - Train and evaluate performance.

- **Long Short-Term Memory (LSTM) - this is provided**
 - Implement an LSTM-based model to capture long-range dependencies.
 - Compare results with the simple RNN model.

- **Gated Recurrent Unit (GRU)**
 - Implement a GRU model and analyze its efficiency in training and generalization.


### Evaluation and insights
- **Compare Model Performance**  
   - Train all models using the same dataset split.  
   - Evaluate using RMSE.
   - Evaluate performance in terms of training time vs inference time.
   - Visualize loss curves and performance metrics.
   - Compare how different architectures handle sequence modeling.
   - Discuss challenges such as overfitting and vanishing gradients.


---

### **Deliverables**
- Notebook with code and explanations. See `notesbooks/predicting_subspot_activity.ipynb`
- Report summarizing findings and insights, include visualizations comparing model predictions. See `reports/Solar_Weather_Lab__Predicting_Sunspot_Activity.pdf`

### **Setup**
Please use the conda environment defined in `./environment.yml` when running all scripts.