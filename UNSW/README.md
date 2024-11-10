Generative Al Acknowledgment: Portions of the code in this project were generated with assistance from ChatGPT, an Al tool developed by OpenAl.
Reference: OpenAl. (2024). ChatGPT [Large language model].
openai.com/chatgpt

# UNSW Dataset
## Dataset Overview

The raw network packets of the UNSW-NB 15 dataset was created by the IXIA PerfectStorm tool in the Cyber Range Lab of UNSW Canberra for generating a hybrid of real modern normal activities and synthetic contemporary attack behaviours. The tcpdump tool was utilised to capture 100 GB of the raw traffic (e.g., Pcap files).


## Features

The dataset consists of 49 features that was genereated with the help of over 12 algorithms. These features are described in the UNSW-NB15_features.csv file.  Some of the features are mentioned below.

- **srcip** - Source IP address
- **sport** - Source port number
- **dstip** - Destination IP address
- **dsport** - Destination port number
- **proto** - Transaction protocol
- **dur** - Record total duration
- **sbytes** - Source to destination transaction bytes 
- **dbytes** - Destination to source transaction bytes
- **sttl** - Source to destination time to live value 
- **dttl** - Destination to source time to live value
- **sloss** - Source packets retransmitted or dropped 
- **attack_cat** - Fuzzers, Analysis, Backdoors, DoS Exploits, Generic, Reconnaissance, Shellcode and Worms

## Preprocessing

- Removing Duplicates: Duplicate records were identified and removed to ensure data quality and avoid introducing bias in the model.
- Handling Missing Values: Any missing data was addressed by removing rows with significant missing information, ensuring that the dataset was complete for model training.
- Dropping Irrelevant Columns: Columns deemed irrelevant to the analysis, such as identifiers or time-based columns, were dropped to reduce noise and improve model focus.

## Model Training and Evaluation
We trained and evaluated Random Forest, K-Nearest Neighbors(KNN) and Naive Bayes machine learning models

Each model was evaluated using metrics like accuracy, precision, recall, and F1-score. Learning curves were plotted to assess model performance.

## Visualization

Correlation Heatmap: Visualized correlations between selected features.
Confusion Matrix: Evaluated model predictions against actual labels.

## Conclusion
The USNW dataset offers a valuable resource for researchers focused on strengthening IoT security using data-driven methods. Our findings highlight the significance of feature selection, class balancing, and hyperparameter optimization in boosting model performance.
