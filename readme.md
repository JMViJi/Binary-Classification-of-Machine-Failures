# Binary Classification of Machine Failures

## Introduction
The Machine Failure Prediction project aims to accurately predict if a machine will fail based on its operating conditions. This prediction plays a crucial role in predictive maintenance where preventing machine downtime is vital to ensure optimal resource utilization. The problem is framed as a classification problem, tackled using comprehensive exploratory data analysis, feature engineering, and robust classification modeling.

## Dataset
The dataset contains observations of machine operations, each providing multiple operating attributes. These attributes include Rotational speed [rpm], Torque [Nm], Tool wear [min], and Machine failure. The data is clean with no missing or mismatched values.

## Dataset Features
The dataset for this competition consists of multiple sensor readings and conditions that are essential to predicting machine failure. Both the training and test datasets are generated from a deep learning model that was initially trained on Machine Failure Predictions. However, it's important to note that while the distributions of the features are similar, they are not identical to the original data. This adds an extra layer of complexity and challenge to the competition.

The dataset comprises of the following features:

- ID: This is a unique identifier assigned to each record in the dataset. It helps in indexing and referencing each individual record.

- Product Id: Combination of Type variable followed by a identifier number

- Type: This refers to the type of machine for which the readings are recorded. Understanding the type of machine can provide insight into the kind of operations it performs, which can in turn be linked to the probability of failure.

- Air temperature [K]: This is the ambient temperature around the machine, measured in Kelvin. It could be an important factor as machines might behave differently under different ambient temperatures.

- Process temperature [K]: This represents the temperature of the process in which the machine is engaged, also measured in Kelvin. Certain processes might cause the machine to heat up and thus increase the chances of failure.

- Rotational speed [rpm]: This is the speed at which the machine operates. It is measured in rotations per minute (rpm). Higher speeds could potentially lead to increased wear and tear.

- Torque [Nm]: This is a measure of the force that causes the machine to rotate. High torque might indicate high load on the machine, which could increase the likelihood of failure.

- Tool wear [min]: This feature indicates the degree of wear and tear the machine has undergone. This is measured in minutes and high tool wear might indicate that the machine is due for maintenance.

- Machine failure: This is the target variable, a binary indicator specifying whether the machine failed (1) or not (0).

In addition to these, there are other failure modes captured in the dataset:

- TWF: Tool wear failure. This indicates whether the machine failed due to tool wear.
- HDF: Heat dissipation failure. This indicates whether the machine failed due to an inability to dissipate heat.
- PWF: Power failure. This indicates whether the machine failed due to a power problem.
- OSF: Overstrain failure. This indicates whether the machine failed due to being overstrained.
- RNF: Random failure. This indicates whether the machine failed due to a random, unspecified issue.

These additional failure modes can provide more context to the machine failure and could be crucial in developing a comprehensive predictive model. Understanding the causes of failure can be instrumental in devising preventative measures and maintenance schedules in real-world scenarios.

The provided train.csv file contains the training data with the target variable 'Machine failure', while the test.csv file contains test data for which participants need to predict the probability of machine failure. A sample_submission.csv file is also provided to guide participants on how to format their predictions for submission.


## Methodology
The following stages were employed in this project:

- Exploratory Data Analysis (EDA): Understand the distribution of data, correlations between different features, and detection of potential outliers or anomalies.

- Feature Engineering: Generate new features that might improve the model's accuracy using combinations of existing features or transformations.

- Model Building: Build various classification models like Logistic Regression, Decision Trees, Random Forests, SVM, etc., to predict the machine failure.

- Model Evaluation: Evaluate the model using appropriate metrics and error analysis.

- Model Tuning: Tune hyperparameters and apply techniques like cross-validation to avoid overfitting.

## Usage
The project is structured as a Jupyter notebook, which provides a detailed walk-through of the code, methodology, and analysis. To use the notebook, clone the repository and run it on a Jupyter notebook environment. The required dependencies can be installed using pip:

```bash
pip install -r requirements.txt
```

## Contact
For any questions, comments, or feedback, feel free to reach out to me at josevillalbajimenez@gmail.com

## Acknowledgments
This project would not have been possible without the dataset provided for this competition. I would like to thank Kaggle for hosting this competition and providing an excellent platform for data science enthusiasts to learn and grow.
