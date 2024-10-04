# Global Terrorism Database (GTD) Analysis

An in-depth analysis of global terrorism incidents using the Global Terrorism Database (GTD). This project encompasses data cleaning, feature engineering, model training with hyperparameter tuning, and the creation of interactive visualizations to understand and predict terrorist activities.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Data](#data)
- [Usage](#usage)
- [Modeling](#modeling)
- [Visualization](#visualization)
- [Git Configuration](#git-configuration)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

The Global Terrorism Database (GTD) provides comprehensive data on terrorist events around the world. This project leverages this dataset to perform data analysis and build predictive models to understand patterns and factors contributing to terrorist activities. By employing machine learning techniques and interactive visualizations, the project aims to offer valuable insights into global terrorism trends.

## Features

- **Data Cleaning:** Handling missing values, correcting data types, and preparing the dataset for analysis.
- **Feature Engineering:** Creating new features to enhance model performance.
- **Model Training:** Utilizing Random Forest classifiers with hyperparameter tuning for accurate predictions.
- **Evaluation Metrics:** Assessing model performance using classification reports and ROC-AUC scores.
- **Interactive Visualization:** Developing heatmaps to visualize terrorist attack distributions globally.
- **Git Hooks:** Implementing custom Git hooks to maintain code quality and repository integrity.

## Installation

Follow these steps to set up the project locally:

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/ramdevmurali/GTD-terrorism.git
    ```

2. **Navigate to the Project Directory:**

    ```bash
    cd GTD-Analysis
    ```

3. **Set Up a Virtual Environment:**

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

4. **Install Dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

5. **Configure Git Hooks:**

    Rename the sample hook scripts to activate them. For example:

    ```bash
    mv GTD.git/hooks/pre-commit.sample GTD.git/hooks/pre-commit
    chmod +x GTD.git/hooks/pre-commit
    ```

    *Repeat for other hooks as needed.*

## Data

### Obtaining the Data

The project utilizes the **Global Terrorism Database May 2022** dataset. Due to its size, the dataset is excluded from version control.

1. **Download the Dataset:**

    Visit [GTD Official Website](https://www.start.umd.edu/gtd/) to download the latest version of the dataset.

2. **Place the Data:**

    Place the downloaded CSV file in the `Data/` directory:

    ```bash
    Data/Global_Terrorism_Database_May_2022.csv
    ```

## Usage

### Running the Jupyter Notebook

The primary analysis is conducted in the `Notebooks/Modelling.ipynb` notebook.

1. **Launch Jupyter Notebook:**

    ```bash
    jupyter notebook
    ```

2. **Open the Notebook:**

    Navigate to `Notebooks/Modelling.ipynb` in the Jupyter interface and execute the cells sequentially.

### Generating the Heatmap Visualization

An interactive heatmap of terrorist attacks is available in the `HTML_Maps/` directory.

- **View the Heatmap:**

    Open the `terrorist_attacks_heatmap.html` file in your web browser to explore the geographic distribution of terrorist activities.

    ```html:HTML_Maps/terrorist_attacks_heatmap.html
    <!DOCTYPE html>
    <html>
    <head>
        <!-- Head content with scripts and styles -->
    </head>
    <body>
        <div id="map"></div>
        <script>
            // Leaflet map initialization and heatmap layer
        </script>
    </body>
    </html>
    ```

## Modeling

The modeling process involves cleaning the data, engineering features, and training a Random Forest classifier with hyperparameter tuning.

### Data Cleaning

Handles missing values and prepares the dataset for modeling.
