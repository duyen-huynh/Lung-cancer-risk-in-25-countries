![Project Portfolio](Project%20porfolio.png)


# Lung-cancer-risk-in-25-countries

This dataset contains information on lung cancer risk factors across various countries, focusing on demographic details, smoking behaviors, and family history.
## Project Overview

This project utilizes the Lung Cancer Risk in 25 Countries dataset from Kaggle, applying data cleaning, feature engineering, and data visualization techniques to analyze how risk factors, demographics, and regional variations influence lung cancer diagnosis and patient mortality.
## Purpose of analysis

- **Risk Factor Analysis**: Analyze how smoking habits, exposure to secondhand smoke, and family history correlate with lung cancer risk.  
- **Demographic Insights**: Explore how age and gender impact the prevalence of lung cancer risk factors.
- **Regional variatons**: Compare lung cancer risk factors across different countries and regions.    
- **Public Health Research**: Identify populations with high-risk behaviors and suggest interventions or preventive measures.

## Data Dictionary

| Column Name                      | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| `ID`                             | Unique identifier for each record                                           |
| `Country`                        | Name of the country                                                         |
| `Population_Size`               | Total population size of the country (in millions)                         |
| `Age`                            | Age of the individual (in years)                                            |
| `Gender`                         | Gender of the individual (`Male` / `Female`)                                |
| `Smoker`                         | Whether the individual is a smoker (`Yes` / `No`)                           |
| `Years_of_Smoking`              | Number of years the individual has been smoking                             |
| `Cigarettes_per_Day`           | Average number of cigarettes smoked per day                                 |
| `Passive_Smoker`                | Whether the individual is regularly exposed to secondhand smoke             |
| `Family_History`                | Whether there is a family history of lung cancer (`Yes` / `No`)             |
| `Chronic_Lung_Disease`         | Presence of pre-existing chronic lung conditions (`Yes` / `No`)             |
| `Genetic_Mutation`             | Whether the individual has genetic mutations linked to cancer risk (`Yes` / `No`) |
| `Radiation_Exposure`           | Exposure to radiation (`Yes` / `No`)                                        |
| `Air_Pollution_Exposure`       | Level of exposure to air pollution (`Low` / `Medium` / `High`)              |
| `Occupational_Exposure`        | Whether the person is exposed to carcinogens at work (`Yes` / `No`)         |
| `Indoor_Pollution`             | Whether the individual is exposed to indoor pollutants (`Yes` / `No`)       |
| `Healthcare_Access`            | Quality of healthcare access (`Good` / `Moderate` / `Poor`)                 |
| `Early_Detection`              | Whether lung cancer was detected early (`Yes` / `No`)                       |
| `Treatment_Type`               | Type of treatment received (`None`, `Surgery`, `Radiation`, etc.)           |
| `Developed_or_Developing`      | Economic status of the country (`Developed` / `Developing`)                 |
| `Annual_Lung_Cancer_Deaths`    | Number of deaths from lung cancer per year in the country                   |
| `Lung_Cancer_Prevalence_Rate` | Percentage of population diagnosed with lung cancer                         |
| `Mortality_Rate`               | Mortality rate due to lung cancer (possibly normalized or % value)          |

## Table of Contents

- [Import Packages of Dataset](#dataset)
- [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Exploratory Data Analysis/Visualization](#exploratory-data-analysis/Visualization)

## Import Packages of Dataset

The dataset is sourced from [Kaggle’s Lung-cancer-risk-in-25-countries dataset](https://www.kaggle.com/datasets/aizahzeeshan/lung-cancer-risk-in-25-countries/data![image](https://github.com/user-attachments/assets/5898967e-162e-48fc-a34e-b63b50b1bea1)).

## Data cleaning and preprocessing

- **Handling Missing Values**: The dataset was scanned for missing values, no need for imputing missing values except for 'Cancer Stage' and 'Treatment type' nan were filled with 'No info'
- **Checking for duplicates**: The dataset was scanned for fully and partially duplicated rows using data exploration techniques. This included checking for duplicates on Index (ID) columns to prevent repeating patient information
- **Cleaning columns**: Medical datasets often include categorical columns with binary values such as "Yes"/"No" responses, which are not directly suitable for numerical analysis or machine learning model, these columns were converted to numerical format of 0/1
- **Incorrect data entry**: Some records indicated that the number of years a patient had smoked exceeded their reported age — a clear indication of incorrect data entry. By addressing these issues early in the pipeline, we notice it when analyzing the dataset

## Feature engineering

Key features for this analysis include:

- **Lung_Cancer_Death_rate_in_population** : Create new column of annual lung cancer deaths by population size
- **Smoker type (`smoker-type`)**: Classifies smokers based on years of smoking and the amount of cigarretes per day:
  - **Longterm and Heavy Smoker**: Years of smoking above mean of years of smoking and the amount of cigarretes per day above mean of cigarretes per day
  - **Longterm Smoker**: Only years of smoking above mean of years of smoking 
  - **Heavy Smoker**: Only amount of cigarretes per day above mean of cigarretes per day
  - **Light Smoker**: Years of smoking below mean of years of smoking and the amount of cigarretes per day below mean of cigarretes per day

## Exploratory data analysis/visualization

1. **Lung Cancer Diagnosis & Correlations of numeric value**
2. **Lung cancer diagnosis breakdown by gender/ smoker/ smoker types**
3. **Lung Cancer Diagnosis by Family History, passive smoker, adenocarcinoma type**
4. **Lung cancer patients categorised by smoker type for each air pollution exposure split on genders**
5. **Regional Variations in Lung cancer diagnosis**:
   - Lung cancer death rate in population of each country
   - Lung cancer prevalence rate against Developed or Developing Country
   - Pairplot country numeric columns in dataset
   - Mortality rate vs. Lung cancer death rate in population by Country
   - Average mortality rate by countries
   - Top countries of Average mortality rate
   - Lung cancer cases in Ethiopia
   - Lung cancer cases in Nigeria    









   
