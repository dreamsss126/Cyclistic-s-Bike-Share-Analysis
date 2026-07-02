# Google Data Analytics Capstone Project
## Cyclistic's Bike Share Analysis 🏍️ 
### Chicago Based Bike Share Company - End-to-End Analysis & Recommendations

![Project Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Tools](https://img.shields.io/badge/Tools-Python%20%7C%20Pandas%20%7C%20NumPy%20%7C%20Tableau-blue)
![Records](https://img.shields.io/badge/Records-791K%2B-orange)
![Period](https://img.shields.io/badge/Period-Q1%202019%20%26%202020-lightgrey)


## 📌 Project Overview
This project analyzes Cyclistic bike-share data from the first quarter of 2019 and the first quarter of 2020 to understand behavioral differences between annual members and casual riders. The analysis follows the Google Data Analytics Case Study framework and uses Python for data cleaning and analysis, with Tableau for data visualization and presentation.



## 🎯 Project Objective
The objective is to generate actionable insights that can help Cyclistic increase annual membership subscriptions by understanding how different customer segments use the bike-sharing service.



## ❓ Business Problem
Cyclistic's marketing team aims to increase the number of annual members because annual memberships generate more consistent revenue and contribute to long-term business growth.

### Key Business Question:
How do annual members and casual riders use Cyclistic bikes differently, and how can these insights help convert casual riders into annual members?



## 🗂️ Project Structure
```
Bike-share-analysis/
│
├── data/
│   ├── Q1 2019 Divvy Tripps.csv Q1 2020 Divvy Tripps.csv         # Raw dataset (with quality issues)
│   └── Divvy_Tripps_dataset_cleaned.csv                          # Cleaned dataset
│
├── docs/
│   ├── bike_share_analysis_guide.docx                            # Data cleanings steps, Analysis processes, Python guide
│   └── bike_share_cleaning.pdf                                   # Data cleaning process documentation
│
├── python-jupyter notebooks/
│   └── bike_share_analysis.ipynb                                 # All code in notebook
│
├── dashboard/
│   └── bike_share_visualization.tableau                          #Tableau dashboard file
│
└── README.md
```

---


## 🛠️ Tools & Technologies
| Tool | Purpose |
|---|---|
| **Python (pandas, numpy)** | Data cleaning & Analysis 
| **Tableau Public** | Interactive dashboard generation |
| **Microsoft Powerpoint** | Presentation of project to stakeholders |

---


## 📊 Dataset Overview
| Attribute | Detail |
|---|---|
| Total Records | 791K (Before cleaning) |
| Columns | 25 |
| Geographic Coverage | Chicago |
| Customer type | Casual vs Members |
| Reporting Period | Q1 2019 & Q1 2020 |

### Columns
Q1 2019: 12 Columns — trip_id, start_time, end_time, bikeid, tripduration, from_station_id, from_station_name, to_station_id, to_station_name, usertype, gender, birthyear



Q1 2020: 13 columns — ride_id, rideable_type, started_at, ended_at, start_station_name, start_station_id, end_station_name, end_station_id, start_lat, start_lng, end_lat, end_lng, member_casual

Link to dataset: https://divvy-tripdata.s3.amazonaws.com/index.html 


Cyclistic historical trip data provided for the Google Data Analytics Professional Certificate Capstone Project.

The datasets meets ROCCC in that the datasets is:

Reliable Original Comprehensive Current Cited

---



# METHODOLOGY 
Google Data Analytics 6 - step framework

ASK ➩ PREPARE ➩ PROCESS ➩ ANALYZE ➩ SHARE ➩ ACT



## 🧹 Data Cleaning
The raw dataset contained at least **5 issues that rendered it unclean for analysis**:

| Issue | Detail | Resolution |
|---|---|---|
| Inconsitent fields | Different column names in both datasets | Standardized with `q1_2019.rename(columns={})` |
| Customer labels categorization | Recorded as subscriber & customer | Standardized to casual & member using `all_trips['member_casual'].replace({})` |
| Ride ID | Needed to be converted as strings | Converted to strings using `q1_2019['ride_id'].astype(str)`|
| Create necessary fields | Missing fields needed for analysis that had to be derived from the dataset | Add date, dayof_week, month, year fields using `all_trips['started_at'].dt.date` |
|Dropped column names | Not needed for analysis | Drop columns using `all_trips.drop(columns=[])`|
    

> Full cleaning decisions and justifications documented in `(https://www.kaggle.com/code/emmanuelbkorankye/bike-share-analysis-capstone-project)`

---


## 🔍 Python Analysis
Conducted a descriptive data analysis ranging from beginner codes to intermediate codes

- **Beginner:** Compare members and casual, see average ride time by each day for member vs casual
- **Intermediate:** see ride time for member vs casual by month, analyze ridership data by type and weekday


### Key Findings

| Finding | Result |
|---|---|
| Compare members and casual| Members rode longer on weekdays and casuals rode longer on weekends|
| See average ride time by each day for member vs casual | Members ride longer each day compared to casual riders |
| see ride time for member vs casual by month | 77% of all year trips came from members while casual riders accounted for 23% |
| Analyze ridership data by type and weekday | ~52 mins for members and ~22 mins ride per day for casual riders |

---


### Exported the cleaned dataset to tableau public for visualization

## 📈 Tableau Public Dashboard
<a href="https://public.tableau.com/app/profile/emmanuel.korankye/viz/GoogleDataAnalyticsCapstoneCyclisticbikeshareanalysis/BikeShareDashboard">
  <img width="969" height="548" alt="Cyclistic Bike Share Dashboard" src="https://raw.githubusercontent.com/dreamsss126/Bike-Share-Analysis/main/Bike%20Share%20Dashboard%20(1).png" />
</a>

## 💡 Key Insights & Recommendations
- Weekend membership campaigns.

- Target casual riders during peak weekend usage periods with membership promotions.

- Membership trial programs.

- Offer discounted trial memberships to encourage adoption.

- Commuter incentive programs.

- Promote membership benefits to casual riders who ride frequently.

- Loyalty and reward programs.

- Provide incentives for repeat casual riders who demonstrate consistent usage patterns.

- Personalized marketing.

- Develop campaigns tailored to the specific behaviors of casual riders.
  

## 👨🏿‍💻 About
**Korankye Emmanuel Boadi** - Data Analyst

Linkdin: www.linkedin.com/in/emmanuel-korankye 
  
