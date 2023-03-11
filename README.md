# Counterterrorism Wars: Drone Strikes Analysis in Pakistan

![U.S Drone](/assets/MQ-9_Afghanistan_takeoff_1_Oct_07.jpeg)

Source: By U.S. Air Force - This image was released by the United States Air Force with the ID [070931-M-5827M-020](https://www.174attackwing.ang.af.mil/News/Photos/igphoto/2000442364/) [(next)](https://commons.wikimedia.org/w/index.php?title=Category:Files_created_by_the_United_States_Air_Force_with_known_IDs&filefrom=070931-M-5827M-020#mw-category-media). This tag does not indicate the copyright status of the attached work. A normal [copyright tag](https://commons.wikimedia.org/wiki/Commons:Copyright_tags) is still required. See [Commons:Licensing](https://commons.wikimedia.org/wiki/Commons:Licensing)

[![Python version](https://img.shields.io/badge/Python-v3.9.16-blue)](https://www.python.org/downloads/release/python-3916/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-yellowgreen.svg)](https://github.com/yourusername/yourrepositoryname)
![License](https://img.shields.io/badge/License-MIT-green)

## Table of Contents

1. [Objective](#objective)
2. [Overview](#overview)
3. [Data Source](#data-source)
4. [Methods](#methods)
   1. [Data Wrangling](#data-wrangling)
   2. [Data Analysis and Visualization](#data-analysis-and-visualization)
   3. [Geospatial Analysis](#geospatial-analysis)
5. [Tools and Libraries](#tools-and-libraries)
6. [Findings](#findings)
7. [Explore the notebooks](#explore-the-notebook)
8. [Repository Structure](#repository-structure)
9. [Contribution](#contribution)
10. [License](#license)

## Objective

The objective of this study is to analyze and visualize the drone strikes that took place in Pakistan between 2004 and 2018, using geospatial analysis techniques. The aim is to gain insights into the patterns and trends of the drone strikes, and to identify any correlations between the strikes and other factors such as time, location, and the type of target. The study also aims to create interactive maps that display the geographical distribution of the drone strikes and provide a more intuitive understanding of their impact on the region.

## Overview

This repository contains the code and data for analyzing the drone strikes that took place in Pakistan as part of the "War on Terror" campaign. The project uses various Python libraries such as pandas, numpy, matplotlib, and seaborn to perform data wrangling, visualization, and analysis, as well as geospatial analysis using folium.

## Data Source

The data used in this project was gathered from publicly available sources.

- [ Counterterrorism Wars – Pakistan PUBLIC DATA - Google Sheets](https://docs.google.com/spreadsheets/d/1nHZopMQpvDO1ETpMVP6ZJ22wk3fHRgB00sekIvqXB_c/edit#gid=1682788061)

## Methods

The methods used in this project can be categorized into the following sections:

### 1. Data Wrangling

The data wrangling process for this project involved the following steps:

- **Exploring Data:** The first step was to explore the dataset and identify any potential issues, such as missing or inconsistent data.

- **Dealing with Missing Values:** The dataset used in this project contained several columns with missing values. To handle missing values, different strategies were employed depending on the context in which the data was missing.

  - For cases where data was missing due to non-recording, an appropriate value was filled by manually observing the data.

    For example, in the **province** column, an appropriate value was filled by comparing values in **region** column.

  - Conversely, for instances where data was absent due to its non-existence, a specific value was assigned based on the contextual relevance of the column.

    For example, in the **leaders-killed** column, the value "0" was assigned to the field as no leader was killed in that specific strike.

These strategies were utilized to maintain the integrity and quality of the data and ensure its suitability for analysis.

- **Data Formatting:** To ensure consistency and accuracy in the analysis, the following data formatting steps were performed:

  - **Converting strings to lower case:** All strings were converted to lower case to ensure consistency in the data.

  - **Renaming columns:** Some columns were renamed to make the column names more descriptive and easier to understand.

  - **Parsing dates:** Dates were parsed and converted to a consistent format to ensure consistency in the analysis.

  - **Changing data types:** The data types of some columns were changed to have the most appropriate data type, such as changing strings to integers or floats where appropriate.

- **Dealing with Inconsistent Data:** Any inconsistent data was identified and cleaned to ensure accuracy in the analysis.

  For example, some entries had inconsistent spellings of location names, which were standardized to ensure consistency across the dataset.

Overall, the data wrangling process was a critical step in preparing the dataset for analysis and ensuring the accuracy and consistency of the results.

### 2. Data Visualization and Analysis

The data visualization and analysis of the drone strikes in Pakistan was performed to gain insights into the patterns and trends of drone strikes. The libraries used for visualization and analysis are seaborn and matplotlib.

- **Casualties by Category:**
  We visualized the distribution of casualties across different categories, including leaders, militants, civilian casualties, and unknown, using a donut chart created with matplotlib.

- **Casualties by Region:**
  The distribution of casualties across categories, including leaders, militants, civilian casualties, and unknown, was visualized using a donut chart created with matplotlib.

- **Casualties by Year:**
  A line plot created with matplotlib was used to investigate the changes in the number of casualties over time.

- **Target Organization:**
  A bar chart using seaborn was created to identify which organizations were most targeted.

- **Strikes in Most Targeted Region:**
  The distribution of drone strikes in the most targeted region, FATA, was examined using a pie chart created with matplotlib.

- **Strikes by Year**
  Changes in the number of drone strikes over time were explored using a histogram created with seaborn.

These visualizations provide useful insights into the patterns and trends of drone strikes in Pakistan. The findings are discussed in detail in the next section.

### 3. Geospatial Analysis

Geospatial analysis was performed to create interactive maps that display the geographical distribution of the drone strikes. The folium library was used to create the maps, which include markers for each drone strike location. The markers provide information on the date, location, target type, and number of fatalities. Clusters were also created for those markers that were located in close proximity to each other.

The geospatial analysis section includes the following:

- **Interactive Maps:**
  Interactive maps were created using folium to display the geographical distribution of drone strikes in Pakistan.

- **Markers:**
  Markers were added for each drone strike location with pop-up that provide information on date, location, target organization, and number of fatalities.

- **Clusters:**
  Clusters were created for markers located in close proximity to each other to allow for a more comprehensive understanding of the geographical distribution of drone strikes.

**Overall**, this project provides a comprehensive analysis of US drone strikes in Pakistan using a variety of Python libraries and techniques, including data wrangling, statistical analysis, data visualization, and geospatial analysis.

## Tools and Libraries

- Pandas (data manipulation library)
- NumPy (scientific computing package)
- Matplotlib (plotting library)
- Seaborn (statistical graphics library)
- Folium (interactive map library)

## Findings

The analysis of US drone strikes in Pakistan reveals several insights into the patterns and trends of the strikes. Here are the findings:

1. The majority of the drone strikes in Pakistan targeted leaders and militants, with civilian and unknown casualties accounting for a relatively small percentage.

Donut chart to show casualties by category:

![Pie chart showing the percentages of drone strike casualties in each category](/assets/casualties_by_category_pie.png)

2. The most targeted regions were North Waziristan and South Waziristan, which belong to present-day Khyber Pakhtunkhwa (previously, North Waziristan and South Waziristan were part of FATA).

Bar chart to show casualties by each region:

![Bar chart showing the regions with most casualties](/assets/most_casualties_by_regions_bar.png)

Pie chart to show percentage of strikes by each region:

![Pie chart showing the most targeted regions](/assets/most_targeted_regions_pie.png)

3. The number of drone strikes and fatalities increased sharply from 2009 to 2010, reaching a peak in 2010, before gradually declining until 2016.

Line chart to show average casualties by year:

![Line graph showing the number of casualtes per year from 2004 to 2018](/assets/casualties_by_year_line.png)

Histogram to show strikes by year:

![Line graph showing the number of casualtes per year from 2004 to 2018](/assets/strikes_by_year_hist.png)

4. The most targeted organization was the Taliban, followed by Al-Qaeda and Haqqani Network.

Bar chart to show casualties by organization:

![Bar graph showing the number of casualties of each organization](/assets/casualties_by_organization_bar.png)

5. The geographical distribution of drone strikes is highly concentrated in certain regions, with clusters of strikes occurring in specific areas.

![Interactive map showing the concentration of drone strikes in specific regions](/assets/interactive_map.gif)

These findings provide important insights into the impact of US drone strikes in Pakistan, highlighting the areas and groups that were most affected by the strikes. The geospatial analysis also provides a visual representation of the distribution of drone strikes, allowing for a better understanding of the scope and scale of the strikes. Overall, the analysis demonstrates the value of data analysis and visualization in gaining insights into complex issues such as drone strikes.

### Summary Table

| Finding                                                                  | Description                                                                                          |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| Majority of the drone strikes in Pakistan targeted leaders and militants | Civilian casualties accounted for a relatively small percentage.                                     |
| Most targeted region                                                     | FATA, followed by Khyber Pakhtunkhwa and Balochistan.                                                |
| Number of drone strikes                                                  | Increased sharply from 2009 to 2010, reaching a peak in 2010, before gradually declining until 2016. |
| Most targeted organization                                               | The Taliban, followed by Al-Qaeda and Haqqani Network.                                               |
| Geographical distribution of drone strikes                               | Highly concentrated in certain regions, with clusters of strikes occurring in specific areas.        |
| Fatalities                                                               | Majority of casualties were militants.                                                               |

## 7. Explore the notebook

- [ Data Wrangling ](https://nbviewer.org/github/MShahnoor/Counterterrorism-Wars-Drone-Strikes-Analysis-in-Pakistan/blob/main/notebooks/Counterterrorism_Wars_Data_Wrangling.ipynb)
- [ Analysis and Visualization ](https://nbviewer.org/github/MShahnoor/Counterterrorism-Wars-Drone-Strikes-Analysis-in-Pakistan/blob/main/notebooks/Counterterrorism_Wars_Data_Analysis_and_Visualization.ipynb)
- [ Geospatial Analysis ](https://nbviewer.org/github/MShahnoor/Counterterrorism-Wars-Drone-Strikes-Analysis-in-Pakistan/blob/main/notebooks/Counterterrorism_Wars_Drone_Attacks_Geospatial_Analysis.ipynb)

## 8. Repository Structure

```

├── assets
│   ├── MQ-9_Afghanistan_takeoff_1_Oct_07.jpeg
│   ├── interactive_map.gif
│   ├── casualties_by_category_pie.png
│   ├── most_casualties_by_regions_bar.png
│   ├── casualties_by_organization_bar.png
│   ├── most_targeted_regions_pie.png
│   ├── casualties_by_year_line.png
│   └── strikes_by_year_hist.png
│
├── data
│   ├── drone-attacks-data-cleaned.csv
│   └── drone_attacks.csv
│
├── notebooks
│   ├── Counterterrorism_Wars_Data_Analysis_and_Visualization.ipynb
│   ├── Counterterrorism_Wars_Data_Wrangling.ipynb
│   └── Counterterrorism_Wars_Drone_Attacks_Geospatial_Analysis.ipynb
│
├── README.md
│
└── LICENSE

```

## 9. Contribution

This project is open to contributions from interested parties. To ensure a streamlined process, kindly follow these guidelines:

- Pull requests are welcome.
- Suggestions, data, and resources related to drone strikes in Pakistan are appreciated.
- Collaboration opportunities in geospatial analysis and data visualization are also encouraged.

Thank you for your interest in contributing to this project. Your contributions are valuable and greatly appreciated.

## 10. License

This project is licensed under the MIT License, which allows for free and open use, modification, and distribution of the code. Please refer to the [LICENSE.txt](LICENSE) file for more information.
