# Breast Cancer Wisconsin (Diagnostic) Data Set

Hello and welcome to this project repository! In this project, we use the Breast Cancer Wisconsin (Diagnostic) dataset to build predictive models that determine whether a given tumor is **benign** or **malignant**. This README will give you an overview of the dataset, the structure of the project, and how to get started.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Description](#dataset-description)
3. [Features and Attributes](#features-and-attributes)
4. [Project Structure](#project-structure)
5. [Modeling Approaches](#modeling-approaches)
6. [Results and Evaluation](#results-and-evaluation)

---

## Introduction
Breast cancer is one of the most common cancers among women worldwide. Early and accurate detection is crucial for effective treatment. In this project, we explore the **Breast Cancer Wisconsin (Diagnostic) Data Set**, which contains features computed from digitized images of fine needle aspirates (FNA) of breast masses. 

Using a variety of classification algorithms, we aim to predict whether a given tumor is malignant (M) or benign (B). The project compares multiple classification methods for performance, so you can get a sense of which models work best for this specific dataset.

---

## Dataset Description
The dataset originally comes from the UCI Machine Learning Repository and can be found in multiple sources (including FTP servers at the University of Wisconsin).

- **Total Instances**: 569
- **Missing Values**: None
- **Class Distribution**: 357 Benign (B), 212 Malignant (M)
- **File**: `data.csv` (in this repository)

### Brief Summary of What’s Inside
- **ID number** – A unique identifier for each patient.
- **Diagnosis** – M (malignant) or B (benign).
- **30 Features** – These include the mean, standard error, and “worst” (or largest) values for each of the following:
  1. Radius
  2. Texture
  3. Perimeter
  4. Area
  5. Smoothness
  6. Compactness
  7. Concavity
  8. Concave points
  9. Symmetry
  10. Fractal dimension
  
The features are computed from the geometry and characteristics of cell nuclei in the FNA images.

---

## Features and Attributes
For each cell nucleus, the dataset records:

1. **Radius**: Mean of distances from center to points on the perimeter.
2. **Texture**: Standard deviation of gray-scale values.
3. **Perimeter**: Measured perimeter of the cell nucleus.
4. **Area**: Measured area of the cell nucleus.
5. **Smoothness**: Local variation in radius lengths.
6. **Compactness**: (Perimeter^2 / Area) - 1.0.
7. **Concavity**: Severity of concave portions of the contour.
8. **Concave points**: Number of concave portions of the contour.
9. **Symmetry**: Symmetry factor of the cell nucleus.
10. **Fractal dimension**: "Coastline approximation" - 1.

For each of these, the dataset contains:
- **Mean value**
- **Standard error (SE)**
- **Worst value** (mean of the three largest values)

That’s how the total of 30 features is formed (10 features × 3 different measurements per feature).

---

## Project Structure
Below is an overview of the main files in this repository along with their creation details:
1. **CancerPrediction_DicisionTreeClassification.ipynb**  
2. **CancerPrediction_KNN.ipynb**  
3. **CancerPrediction_KernalSVM.ipynb**  
4. **CancerPrediction_LogisticRegression.ipynb**  
5. **CancerPrediction_NaiveBayes.ipynb**  
6. **CancerPrediction_RandomTreeClassification.ipynb**  
7. **CancerPrediction_SVM.ipynb**  
8. **data.csv**  
9. **readme.md**  

---
## Modeling Approaches

In this project, we experiment with various classification algorithms to predict tumor type (benign or malignant):

1. **Logistic Regression**
2. **K-Nearest Neighbors (KNN)**
3. **Support Vector Machine (SVM)**
4. **Kernel SVM**
5. **Naive Bayes**
6. **Decision Tree Classifier**
7. **Random Forest Classifier**

### Steps for Each Model

1. **Data Splitting**  
   The dataset is split into training and test sets (e.g., 80% training, 20% testing).
   
2. **Feature Scaling**  
   Important for models like KNN, SVM, and logistic regression.

3. **Model Training**  
   Fit the chosen algorithm to the training set.

4. **Prediction**  
   Predict tumor type on the test set.

5. **Evaluation**  
   - **Accuracy**

---

## Results and Evaluation

Each model’s performance is measured on the test set. Generally, most well-tuned models achieve very high accuracy (around 90–98%) on this dataset. Below is a simple example of how you might display the results:

| Model                     | Accuracy | 
|---------------------------|----------|
| Logistic Regression       | 96.0%    | 
| K-Nearest Neighbors       | 95.0%    | 
| SVM                       | 95.0%    | 
| Kernel SVM                | 97.0%    | 
| Naive Bayes               | 94.0%    |
| Decision Tree Classifier  | 94.0%    |
| Random Forest Classifier  | 98.0%    |

### Best Model
Based on **accuracy** alone, the **Random Forest Classifier** performed the best, achieving **98.0% accuracy**. If you are seeking a model that balances ease of interpretability and strong performance, consider also evaluating other metrics such as **precision**, **recall**, **F1-score**, and **ROC-AUC** to find a model that best fits the specific needs of your project.

