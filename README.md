# Netflix EDA PySpark

This project involves performing **Exploratory Data Analysis (EDA)** on Netflix datasets using PySpark. It is a part of the **CE408 - Cloud Computing Assignment** by **Muhammad Ahmad**.

---

## Overview

The project showcases how PySpark can be utilized for conducting data preprocessing and analysis on the Netflix dataset. It provides valuable insights and visualizations based on various attributes like genres, release years, and more.

### Key Features:
- Efficient data preprocessing with PySpark.
- Analysis of Netflix titles based on multiple attributes such as genre, release year, duration, and ratings.
- Interactive visualizations to present insights.

---

## Dataset

The dataset used in this analysis is publicly available on [Kaggle](https://www.kaggle.com/datasets/shivamb/amazon-prime-movies-and-tv-shows?resource=download). It contains essential information about Netflix titles, including:
- **Title**: Name of the movie or TV show.
- **Genre**: Category or type of content (e.g., Drama, Comedy, etc.).
- **Release Year**: The year the title was released.
- **Country**: The country where the content was produced.
- **Duration**: Runtime of the movie or number of seasons for a TV show.
- **Ratings**: Audience ratings and reviews.

The dataset is stored locally and mounted into the Docker container for processing during analysis.

---

## Requirements

### Software Prerequisites:
- **Docker** and **Docker Compose**: To set up and manage the Spark cluster.
- **Python 3.x**: Optional, for local testing and debugging purposes.

---

## Setup Instructions

### Using Docker
1. **Clone the Repository**:
   Clone the project repository to your local machine:
   ```bash
   git clone https://github.com/ahmad9022032/Netflix_EDA_PySpark.git
   cd Netflix_EDA_PySpark
  ```

2. Start the Spark cluster:
   ```bash
   docker-compose up -d
   ```

3. Verify that the services are running:
   - Spark Master: [http://localhost:9090](http://localhost:9090)

### Running the Script
1. Copy the python script to the `spark-master` container:
   ```bash
   docker cp -L netflix_titles_eda.py spark-master:/opt/bitnami/spark/amazonPrime_eda.py
   ```

2. Submit the PySpark job:
   ```bash
   docker exec spark-master spark-submit --master spark://spark-master:7077 /opt/bitnami/spark/amazonPrime_eda.py
   ```

3. Check the console output for analysis results and visualizations.



## Project Files

### Repository Structure:
```
Netflix_EDA_PySpark/
|
├── data/
│   └── netflix_titles.csv            # Netflix dataset
│
├── netflix_titles_eda.py            # PySpark script for EDA
├── docker-compose.yaml              # Docker Compose configuration
├── Dockerfile                       # Custom Spark image with dependencies
└── README.md                        # Project documentation
```


## Results
All the results are attached in the screen record video in the repository named CE408


