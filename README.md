# Data-Pipeline-Automation-and-Analytics-Dashboard
Handling data end-to-end, from acquisition and transformation to visualization.

This project demonstrates the creation of an automated data pipeline to analyze COVID-19 data and visualize trends through an interactive analytics dashboard. The pipeline involves data collection, preprocessing, analysis, and visualization, showcasing fundamental skills in data management, automation, and visualization.

## Table of Contents

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The Automated Data Pipeline and Analytics Dashboard project encompasses the following key components:

- Data Collection: COVID-19 data is sourced from the John Hopkins University COVID-19 dataset, stored in an AWS S3 bucket.
- Data Preprocessing: Data is cleaned, missing values are handled, and additional columns are created for daily cases and rolling averages.
- Automation: Apache Airflow is utilized to schedule and automate the data preprocessing tasks.
- Data Analysis: Exploratory data analysis is performed using pandas to uncover trends and patterns in COVID-19 data.
- Visualization: An interactive analytics dashboard is created using Plotly to visualize key insights and metrics.

## Getting Started

To run this project locally, follow these steps:

1. Clone this repository to your local machine.
2. Set up your environment by installing Python, pandas, NumPy, Docker, and Apache Airflow.
3. Create an AWS account and set up an S3 bucket named "covid-data" for data storage.
4. Configure the Airflow DAG to schedule data preprocessing tasks and specify S3 credentials.
5. Use Docker to build the container image and deploy the Airflow DAG.
6. Access the analytics dashboard to visualize COVID-19 trends and insights.

## Project Structure

The project directory is structured as follows:

Automated-Data-Pipeline-Project/
│ Dockerfile
│ covid_pipeline.py # Apache Airflow DAG
│
└───data/
│ │ covid_data.csv # Raw COVID-19 data
│
└───dashboard/
│ │ index.html # Dashboard HTML
│ │ style.css # Dashboard styling
│ │ script.js # Dashboard JavaScript
│
└───documentation/
│ │ README.md # Project documentation
│
└───outputs/
│ covid_cleaned.csv # Cleaned and preprocessed data


## Usage

1. Clone this repository:

git clone https://github.com/your-username/Automated-Data-Pipeline-Project.git

2. Set up your environment with the required dependencies (Python, pandas, NumPy, Docker, Apache Airflow).

3. Configure the `covid_pipeline.py` Airflow DAG to run data preprocessing tasks and specify your S3 credentials.

4. Build the Docker container and deploy the Airflow DAG:

docker build -t covid-pipeline-image .
docker run -d -p 8080:8080 covid-pipeline-image


5. Access the Airflow UI at `http://localhost:8080` and trigger the DAG to start the data pipeline.

6. Open the analytics dashboard by opening `dashboard/index.html` in a web browser to visualize COVID-19 trends and insights.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1. Fork this repository.
2. Create a new branch for your feature/bug fix.
3. Commit your changes and push them to your fork.
4. Submit a pull request with a detailed description of your changes.



