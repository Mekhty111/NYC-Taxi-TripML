# NYC Taxi Trip Duration Prediction

## Project Overview

**Goal:** Automate business processes by building a **machine learning** pipeline that predicts the total duration of a New York City taxi trip. This enables accurate fare estimation based on US taxi pricing rules (fixed fees plus time- and distance-based tariffs).

## Table of Contents

- [Project Overview](#project-overview)
- [Business Context](#business-context)
- [Project Objectives](#project-objectives)
- [Repository Structure](#repository-structure)
- [Data Sources](#data-sources)
- [Getting Started](#getting-started)
- [Main Workflow](#main-workflow)
- [Results & Insights](#results--insights)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Business Context

Taxi and ride-hailing services need reliable trip duration forecasts for route planning, pricing transparency, and customer satisfaction. By predicting ride time from features such as pickup/dropoff locations, time of day, and weather, our model helps optimize both business operations and end-user experience.

## Project Objectives

- **Build unified dataset:** Integrate trips with weather and geospatial data.
- **Feature Engineering:** Design new predictors and select the strongest features.
- **EDA & Visualization:** Reveal key insights and patterns in the data.
- **Modeling:** Evaluate multiple regression algorithms for prediction.
- **Deployment Workflow:** Automate end-to-end prediction for new rides.
- **Kaggle Submission:** Showcase results in a live data science competition.

## File Descriptions

- **train.csv** - The training set (contains 1,458,644 trip records)  
- **test.csv** - The testing set (contains 625,134 trip records)  
- **sample_submission.csv** - A sample submission file in the correct format  

## Data Fields

- **id** - A unique identifier for each trip  
- **vendor_id** - A code indicating the provider associated with the trip record  
- **pickup_datetime** - Date and time when the meter was engaged  
- **dropoff_datetime** - Date and time when the meter was disengaged  
- **passenger_count** - The number of passengers in the vehicle (driver entered value)  
- **pickup_longitude** - The longitude where the meter was engaged  
- **pickup_latitude** - The latitude where the meter was engaged  
- **dropoff_longitude** - The longitude where the meter was disengaged  
- **dropoff_latitude** - The latitude where the meter was disengaged  
- **store_and_fwd_flag** - Indicates whether the trip record was held in vehicle memory before sending to the vendor because the vehicle did not have a connection to the server.  
  - *Y* = store and forward  
  - *N* = not a store and forward trip  
- **trip_duration** - Duration of the trip in seconds (target variable)  


## Repository Structure
```
├── data/ # Raw and processed datasets
├── notebooks/ # Jupyter notebooks for development & analysis
├── src/
│ ├── data/ # Data prep scripts
│ ├── features/ # Feature engineering
│ ├── models/ # ML pipelines, metrics, training logic
│ └── utils/ # Helper functions
├── requirements.txt # Dependency list
└── README.md # Project overview (this file)

```

## Data Sources

- NYC taxi ride datasets (pickup/dropoff, timestamp, trip length)
- Open weather datasets
- Geospatial info

## Getting Started

Clone the repo:
git clone https://github.com/Mekhty111/NYC-Taxi-TripML.git
cd NYC-Taxi-TripML


Install dependencies:
pip install -r requirements.txt


Download all datasets (see `data/README.md` for sources) and use the provided notebooks for analysis and experiments.

## Main Workflow

- **Data merging & cleaning**
- **Feature engineering:** Compute distances, time intervals, join weather info, extract temporal features
- **Exploration:** Analyze trends, outliers, and correlations
- **Modeling:** Train and compare regression models (e.g., linear, ensemble, boosting)
- **Evaluation:** Use RMSE, MAE for model selection

## Results & Insights

Our best model achieves robust accuracy on public test sets (metrics and feature importances available in the `notebooks/results` section). Top features include route length, pickup time, and weather factors.

## Contributing

Please feel free to open an Issue or Pull Request with ideas, bug reports, or improvements!

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

Data provided by NYC Open Data, Kaggle, and thanks to the open-source and data science community.
