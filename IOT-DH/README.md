Generative AI Acknowledgment:
Portions of the code in this project were generated with assistance from Perplexity Pro Search, an AI tool developed by Perplexity AI.
Reference: Perplexity AI. (2024). Perplexity [Pro Search]. perplexity.ai

# IoT-DH Dataset Analysis

## Overview

The IoT-DH dataset is used to analyze network traffic patterns associated with Internet of Things (IoT) devices. It includes both normal and malicious traffic, making it suitable for developing and evaluating machine learning models for cybersecurity.

## Features

The dataset contains the following primary attributes:

- **dt**: Datetime of the recorded traffic
- **dur**: Duration of the traffic flow
- **dur_nsec**: Nanosecond duration
- **tot_dur**: Total duration
- **pktrate**: Packet rate
- **protocol**: Protocol used in the traffic
- **port_no**: Port number
- **tx_kbps**: Transmission rate in kbps
- **rx_kbps**: Reception rate in kbps
- **tot_kbps**: Total rate in kbps

## Preprocessing Steps

1. **Data Cleaning**: Removed rows with missing labels and filled NaN values.
2. **Feature Selection**: Used `SelectKBest` to choose relevant features.
3. **Class Balancing**: Applied SMOTE to handle class imbalance.
4. **Scaling**: Standardized features using `StandardScaler`.

## Model Training and Evaluation

We trained and evaluated three machine learning models:

1. **Random Forest**
   - Used `class_weight='balanced'` for initial balancing.
   - Applied hyperparameter tuning with RandomizedSearchCV.

2. **KNN (K-Nearest Neighbors)**
   - Tuned hyperparameters using RandomizedSearchCV.

3. **Naive Bayes**
   - Applied hyperparameter tuning for `var_smoothing`.

Each model was evaluated using metrics like accuracy, precision, recall, and F1-score. Learning curves were plotted to assess model performance.

## Visualization

- **Correlation Heatmap**: Visualized correlations between selected features.
- **Confusion Matrix**: Evaluated model predictions against actual labels.

## Conclusion

The IoT-DH dataset provides a valuable resource for researchers aiming to enhance IoT security through data-driven approaches. Our analysis demonstrated the importance of feature selection, class balancing, and hyperparameter tuning in improving model performance.

--- 
