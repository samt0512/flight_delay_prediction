# Flight Delay Prediction

A machine learning project that predicts whether a U.S. domestic flight will be delayed 
by 15 or more minutes using 2015 flight data.

## Project Overview

This project was completed as a final project for an Intro to Machine Learning course. 
We build a full machine learning pipeline including data exploration, preprocessing, 
model training, and evaluation. Two classification models are compared: Logistic 
Regression and Gaussian Naive Bayes.

## Dataset

**Source:** [2015 Flight Delays and Cancellations](https://www.kaggle.com/datasets/usdot/flight-delays) — Kaggle  
**Files needed:** `flights.csv`, `airports.csv`, `airlines.csv`

The dataset contains approximately 5.8 million domestic flights from 2015 with 31 
features including airline, origin/destination airport, scheduled times, and delay 
information.

> Note: The dataset files are not included in this repository due to their size. 
> Please download them from Kaggle and place them in the same directory as the notebook.

## Requirements
pandas
numpy
matplotlib
seaborn
scikit-learn

Install with:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## How to Run

1. Clone this repository
2. Download the dataset from Kaggle and place `flights.csv`, `airports.csv`, and 
   `airlines.csv` in the same folder as the notebook
3. Open `flight_delay_prediction.ipynb` in Jupyter Notebook or VS Code
4. Run all cells in order

## Results Summary

| Model | Accuracy | Recall (Delayed) |
|-------|----------|-----------------|
| Logistic Regression (initial) | 81.4% | 0% |
| Logistic Regression (balanced) | 58.0% | 60% |
| Naive Bayes (initial) | 81.3% | 0% |
| Naive Bayes (balanced) | 55.8% | 64% |

Both models initially suffered from the majority class problem. After applying class 
balancing techniques, both models achieved meaningful recall for delayed flights.

## Acknowledgements

Dataset provided by the U.S. Department of Transportation via Kaggle.  
Project completed with guidance from Claude (Anthropic) for code structure and debugging.
