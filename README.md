# customer-segmentation

This repository contains a revised and modular version of my final project for IST 418: Big Data Analytics at Syracuse University. Originally implemented as a single notebook, the codebase has now been refactored into multiple notebooks for improved readability and modularity.

The project focuses on segmenting retail customers using demographic and behavioral data to enhance marketing strategies through clustering and recommendation systems. By leveraging PySpark, K-Means Clustering, FP-Growth, and a hybrid recommendation algorithm, this project transforms raw customer data into actionable insights for personalized marketing and inventory management.

---

## Project Structure

- `Code/`
    - `customer_segmentation.ipynb`: final pipeline- clustering + recommendations
    - `EDA.ipynb`: exploratory data analysis and visualizations
    - `preprocessing.ipynb`: data cleaning and feature engineering
    - `artifacts/`
        - Saved Spark model artifacts
- `Data/`
    - `marketing_campaign.csv` (original dataset)
    - `preprocessed_segmenting_data_csv/` (output CSVs from PySpark)

- `requirements.txt`: Packages needed to run code

--- 

## Project Goals:

- Segment customers based on demographic and behavioral traits using **K-Means clustering**

- Visualize and interpret clusters using **PCA**

- Develop recommendation systems to:

    - Suggest products to customers based on personal and group behavior

    - Recommend deals tailored to cluster characteristics

    - Highlight high-demand items using FP-Growth

- Provide actionable marketing and inventory insights

---

## Dataset

The dataset was sourced from Kaggle, originally published by Dr. Omar Romero-Hernandez. It contains customer information from a Portuguese retail campaign, with 2,240 observations and 29 features, including:

- Demographic: Age, Marital Status, Education, Income

- Behavioral: Purchase history by product category, deal acceptance, customer loyalty

- Engagement: Days since last purchase, enrollment date

[Link to Kaggle Dataset](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)

---

## Running The Project

> This project was developed using Python 3.11.0

1. Clone the Repository
    - Run the following commands in your terminal:
    - git clone https://github.com/your-username/customer-segmentation.git
    - cd customer-segmentation

2. Set Up Your Environment
    - Install required Python packages:
    - `pip install -r requirements.txt`

3. Configure Java and PySpark
    - PySpark requires Java 17+ and Apache Spark.

    - Install Java 17 using Homebrew: `brew install openjdk@17`

    - Add the following lines to your shell config file (`~/.zshrc` or `~/.bash_profile`):
        - `export JAVA_HOME="/opt/homebrew/opt/openjdk@17"`
        - `export PATH="$JAVA_HOME/bin:$PATH"`

    - Install Apache Spark: `brew install apache-spark`

    - Add Spark to your shell config file (`~/.zshrc` or `~/.bash_profile`):
        - `export SPARK_HOME="/opt/homebrew/Cellar/apache-spark/4.0.0/libexec"`
        - `export PATH="$SPARK_HOME/bin:$PATH"`

    - Apply changes: `source ~/.zshrc` or `source ~/.bash_profile`

    - Verify installation: `spark-submit --version`

---

## Notebook Overview's

- `preprocessing.ipynb`: Cleans and transforms the raw data, performs feature engineering, and exports preprocessed data.

- `EDA.ipynb`: Generates visualizations and summary statistics to explore customer patterns.

- `customer_segmentation.ipynb`: Runs K-Means clustering, evaluates models with PCA and silhouette scores, and implements three recommendation algorithms.

---

## Key Insights

- Customers were segmented into three groups based on behavior and demographics:

    - Balanced Mid-Spenders

    - Budget-Conscious Deal Seekers

    - Affluent Digital Loyalists

- Association Rule Mining highlighted that wine and meat are core product drivers.

- Cluster-based and hybrid recommendations allow for personalized marketing strategies.

- Tailored deal recommendations can enhance customer engagement and loyalty.

---

## Packages Used

- pyspark
- matplotlib
- pandas
- seaborn

---

## Author

Tyler Katz

B.S. in Applied Data Analytics, Class of 2026
Syracuse University

[GitHub Profile](https://github.com/tkatz123) • [LinkedIn](https://www.linkedin.com/in/tylerkatz1/)

---

## License

This projest is licensed under the MIT Licesne. See the LICESNE for details.