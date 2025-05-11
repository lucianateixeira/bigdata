# 🌒 Big Data Eclipse Classification Project

Welcome to the **Big Data Eclipse Classification** project by [lucianateixeira](https://github.com/lucianateixeira).  
This project showcases how to combine **Apache Spark** for scalable data processing with a **Keras LSTM model** to classify eclipse types using real astronomical data from NASA.

## 🔍 Project Overview

This project involves:
- Loading and exploring a large eclipse dataset using **PySpark**
- **Detecting and removing outliers** based on standard deviation thresholds (3-sigma)
- **Vectorizing and scaling** features with Spark's `VectorAssembler` and `StandardScaler`
- Converting the processed Spark DataFrame to Pandas for modeling
- Training an **LSTM neural network** in TensorFlow/Keras to classify eclipse types (`etype`)

## 📊 Dataset

The dataset used is from NASA and includes:
- Date, time, and location of eclipses
- Gamma and magnitude values
- Saros series and lunar numbers
- Eclipse path width, duration, and astronomical angles

### 🛰️ Data Sources:
- [NASA Solar Eclipse Table](https://umbra.nascom.nasa.gov/eclipse/980226/tables/table_1.html)  
- [NASA Eclipse Predictions (2076)](https://eclipse.gsfc.nasa.gov/SEbeselm/SEbeselm2051/SE2076Jan06Tbeselm.html)

## ⚙️ Technologies Used

- **Apache Spark (PySpark)** – for large-scale data handling and preprocessing  
- **Pandas / NumPy** – for data manipulation  
- **TensorFlow / Keras** – for building and training the neural network  
- **Scikit-learn** – for train/test split  
- **Jupyter Notebook** – for development and interactive analysis  

## 🧠 Model Architecture

- Optimizer: `adam`  
- Loss Function: `sparse_categorical_crossentropy`  
- Output: Classification of eclipse type  
- Evaluation: Accuracy score on 30% test set

## 🧪 Results

- The 3-sigma outlier detection improved model performance
- The LSTM model handled time-like features and multi-dimensional inputs effectively
- Classification accuracy validated on 30% of the test set

## 🚀 How to Run

### 1. Install Dependencies

Make sure you have the following installed:

- **Java 11** (set your `JAVA_HOME`):
  - Install Java 11 from [Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or OpenJDK.
  - Set `JAVA_HOME` on your system:
    - For Windows:
      ```bash
      set JAVA_HOME=C:\Program Files\Java\jdk-11
      ```
    - For Mac/Linux:
      ```bash
      export JAVA_HOME=/path/to/java11
      ```

- **Python Libraries**:
  Install the following Python packages:
  ```bash
  pip install pyspark pandas numpy tensorflow scikit-learn



