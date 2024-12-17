# PracticalML
# Practical Machine Learning Course Project

This project is part of the Coursera Practical Machine Learning course. The goal is to apply machine learning techniques to predict how well experimental subjects perform a specific weightlifting exercise, the "biceps curl", based on sensor data. The data consists of measurements from sensors worn on the body and attached to the dumbbell. The project involves data preprocessing, model training, and evaluation.

## Project Overview

- **Dataset**: The dataset consists of 160 data points obtained from five male subjects performing a one-handed dumbbell "biceps curl" in five different ways (A - correct, B - E - deviations).
- **Data Source**: The dataset was provided as CSV files: [Training Dataset](https://d396qusza40orc.cloudfront.net/predmachlearn/pml-training.csv) and [Test Dataset](https://d396qusza40orc.cloudfront.net/predmachlearn/pml-testing.csv).
- **Machine Learning Task**: We apply a classification algorithm to predict the type of exercise ("classe") performed by the subjects, based on sensor data.

## Project Steps

1. **Loading Necessary Packages**
   - Used the `caret`, `kernlab`, `dplyr`, and `RANN` packages to perform machine learning tasks.

2. **Loading and Splitting the Data**
   - Downloaded the training and test data and split the training data into training and validation sets (75% training, 25% validation).

3. **Exploratory Data Analysis (EDA)**
   - Examined the distribution of several variables and performed log transformations on skewed variables for better distribution.

4. **Data Preprocessing**
   - Imputed missing values using k-nearest neighbors (KNN) method to prepare the data for training.
   - Identified and selected important features based on random forest analysis.

5. **Model Training**
   - Trained a random forest model on a subset of the data (5%) to identify important features.
   - Used the full dataset to train the final model and performed cross-validation to estimate out-of-sample error.

6. **Model Evaluation**
   - Evaluated the model accuracy on the validation set.
   - Tested the model on unseen test data and predicted the exercise "classe" for each row in the test set.

7. **Results**
   - The final model achieved high accuracy, and predictions on the test data were evaluated using Coursera’s grading system, yielding a score of 20/20.

## Files

- `pml-training.csv`: The training dataset containing sensor data.
- `pml-testing.csv`: The test dataset containing sensor data with missing `classe` values.
- `Practical_Machine_Learning_Project.Rmd`: The R Markdown file containing the analysis and steps for building the model.

## How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/Practical-Machine-Learning.git
    ```

2. Install the required R packages:
    ```r
    install.packages(c("caret", "kernlab", "dplyr", "RANN"))
    ```

3. Open the R Markdown file `Practical_Machine_Learning_Project.Rmd` in RStudio and run the analysis.

## Dependencies

- **R version**: 4.x.x
- **Required Packages**: `caret`, `kernlab`, `dplyr`, `RANN`

## Conclusion

This project demonstrates the application of machine learning techniques to classify exercises based on sensor data. The steps covered include data loading, preprocessing, exploratory analysis, model training, and evaluation using a random forest classifier. The model performs well and is able to predict the exercise type with high accuracy.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
