# econ3916-lab06-sampling

# Sampling for Machine Learning — Train-Test Splits

## Objective

In this lab, I explored how sampling methods, train-test splits, and data leakage affect the accuracy and reliability of machine learning results.

## Methodology

- **Titanic Dataset:** I explored data from 891 Titanic passengers, using survival as the target variable.
- **Train-Test Splits:** I compared naive random splitting with stratified splitting and examined how well each method preserved the overall survival rate.
- **Data Leakage:** I identified and fixed data leakage in StandardScaler and SimpleImputer by fitting them only on the training data.
- **Custom Function:** I wrote a `split_by_share()` function to divide a dataset into training and test sets using a test share and random seed. I also checked its results against the lab's original split.
- **Literary Digest Simulation:** I simulated the 1936 presidential election polling failure using a population of 10 million voters.
- **Data Defect Correlation:** I calculated Meng's data defect correlation to understand how sampling bias affects estimation accuracy.
- **Repeated Simulations:** I ran 100 replications to compare the estimation errors of biased and random samples.

## Key Findings

- Stratified splitting kept the survival rate close to 40.6% in both the training and test sets, while naive splitting produced slightly different rates.
- Data leakage can make model evaluations misleading because information from the test set influences the training process.
- In the election simulation, the biased sample of 4,382,503 responses produced an error of 8.3 percentage points, while the random sample of 50,000 responses was much closer to the true result.
- A data defect correlation of 0.1475 produced an estimation error of 8.3 percentage points.
- Across 100 replications, the biased sample consistently produced estimates farther from the true value, despite having a much larger sample size.

**My main takeaway:** A larger dataset does not always produce better results. Good sampling design and proper separation of training and test data are more important than simply collecting more observations.
