🌒 Big Data Eclipse Classification Project
Welcome to the Big Data Eclipse Classification project by lucianateixeira. This project demonstrates how to combine Apache Spark for scalable data preprocessing with TensorFlow/Keras LSTM models for time series classification, using real astronomical eclipse data from NASA.

📁 Repository Structure
bash
Copy
Edit
bigdata/
│
├── 2021322_CA.ipynb               # Initial notebook with core implementation
├── 2021322_CA (1).ipynb           # Alternate/backup version
├── 2021322_CA(FINAL).ipynb        # Final cleaned version of the Spark + LSTM project
├── hadoop-apache.ipynb            # Notebook for Hadoop and Apache integration
├── hadoop-apache (FINAL).ipynb    # Final version of Hadoop-Apache work
└── README.md                      # Project documentation
🔍 Project Overview
This project:

Uses PySpark for reading, cleaning, and processing a large dataset of solar and lunar eclipses.

Detects and removes outliers using statistical thresholds (3-sigma rule).

Applies feature engineering (vector assembly and standard scaling).

Converts the Spark DataFrame to Pandas for deep learning.

Trains an LSTM neural network to classify eclipse types based on temporal and geospatial features.

📊 Dataset
The dataset used contains detailed records of solar eclipses, retrieved from NASA sources:

NASA Solar Eclipse Table

NASA Eclipse Data (2076)

Key Features:
Date and time of the eclipse

Geographic coordinates

Saros series and gamma values

Duration, magnitude, and other astronomical parameters

⚙️ Technologies Used
Apache Spark (PySpark) for distributed data processing

Pandas / NumPy for in-memory data manipulation

TensorFlow / Keras for building and training the LSTM model

Scikit-learn for train-test splitting

Jupyter Notebook for development and visualization

🧠 Model Architecture
text
Copy
Edit
Input → LSTM(64) → Dense(64, relu) → Dense(n_classes, softmax)
Loss function: sparse_categorical_crossentropy

Optimizer: adam

Evaluated with accuracy on a 30% test split

🧪 Results
Data cleaning and outlier detection significantly improved model performance.

The LSTM model achieved solid accuracy in predicting eclipse types, indicating the feasibility of time series classification with astronomical data.

🛠 How to Run
Clone the repo:

bash
Copy
Edit
git clone https://github.com/lucianateixeira/bigdata.git
cd bigdata
Install dependencies:

Spark (with Java 11)

Python packages: pyspark, pandas, numpy, tensorflow, scikit-learn

Set your JAVA_HOME:

python
Copy
Edit
os.environ['JAVA_HOME'] = "C:\\Program Files\\Java\\jdk-11"
Run the final notebook:
2021322_CA(FINAL).ipynb
