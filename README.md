# Gold_Recovery_Analysis_S10

## Project Description

This project focuses on predicting gold recovery efficiency in a mining purification process using machine learning models. The dataset consists of time-series records containing various parameters at different processing stages. The goal was to analyze the data, verify the accuracy of provided recovery values, preprocess missing and inconsistent data, and train models to predict recovery rates with high accuracy. Key aspects of the project included examining metal concentration trends, comparing feed particle size distributions, handling anomalies, and implementing the symmetric Mean Absolute Percentage Error (sMAPE) as the evaluation metric. After training and evaluating multiple models, the best-performing model was selected to provide reliable predictions for gold recovery.

The data was stored in three files:

- **gold_recovery_train.csv** — Training dataset
- **gold_recovery_test.csv** — Test dataset
- **gold_recovery_full.csv** — Source dataset containing both training and test data

The dataset is indexed by the date and time of acquisition, ensuring that adjacent time-stamped data points are often similar. Some features in the training set are absent from the test set due to delayed measurements or calculations. Additionally, the test set does not contain target values. The source dataset includes all features from both the training and test sets.

## Data Preparation

### Data Exploration
- The dataset files were opened and examined.
- The structure and contents of each file were inspected.

**File Paths:**
- `/datasets/gold_recovery_train.csv`
- `/datasets/gold_recovery_test.csv`
- `/datasets/gold_recovery_full.csv`

## Gold Recovery Process:
![image](https://github.com/user-attachments/assets/64c26227-d87c-4853-8363-8d4f853f0504)

### Recovery Calculation Verification
- The `rougher.output.recovery` feature was recalculated using the training set.
- The Mean Absolute Error (MAE) between the calculated values and the provided values was computed.
- Findings were documented regarding the accuracy of the given recovery values.

### Missing Feature Analysis
- Parameters absent from the test set were identified.
- The data types and significance of these missing features were examined.

### Data Preprocessing
- Missing values and inconsistencies were handled.
- Necessary transformations were performed to prepare the data for analysis.

## Data Analysis

### Metal Concentration Trends
- The concentration of **Au (gold), Ag (silver), and Pb (lead)** was analyzed across different purification stages.

### Feed Particle Size Distribution
- The distributions of feed particle sizes in the training and test sets were compared.
- The similarity of these distributions was assessed to ensure reliable model evaluation.

### Total Substance Concentration
- The total concentrations at different processing stages (raw feed, rougher concentrate, and final concentrate) were examined.
- Abnormal values in the distribution were identified and addressed.
- Anomalous values were removed where necessary to improve data quality.

## Recovery Calculation: 
![image](https://github.com/user-attachments/assets/0b6e867a-2e56-4ef4-b153-aed36830368d)
- C — share of gold in the concentrate right after flotation (for finding the rougher concentrate recovery)/after purification (for finding the final concentrate recovery)
- F — share of gold in the feed before flotation (for finding the rougher concentrate recovery)/in the concentrate right after flotation (for finding the final concentrate recovery)
- T — share of gold in the rougher tails right after flotation (for finding the rougher concentrate recovery)/after purification (for finding the final concentrate recovery)

## Model Development

### Implementation of sMAPE Metric
- A function was written to compute the symmetric Mean Absolute Percentage Error (sMAPE).

### Model Training and Evaluation
- Multiple machine learning models were trained and evaluated.
- Cross-validation was used to assess model performance.
- The best-performing model was selected and tested on the test dataset.
- Findings and justifications for the model choice were documented.

## Evaluation metric - symmetric Mean Absolute Percentage Error
- equally takes into account the scale of both the target and the prediction

![image](https://github.com/user-attachments/assets/49246bc0-5a28-4f54-9fa7-8d4eb775b434)

![image](https://github.com/user-attachments/assets/6dcc5b6a-60d2-45c0-9146-25f5b34164c2)








