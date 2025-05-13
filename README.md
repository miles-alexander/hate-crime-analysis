# Hate Crime in America: State-Level Patterns and Insights  
**Author:** [@miles-alexander](https://github.com/miles-alexander)  


---

## Project Overview

This project explores hate crimes in the United States, with a specific focus on the year 2019. The goal is to identify patterns across states and examine the types of crimes most commonly associated with bias-based offenses. By cleaning, transforming, and analyzing data from multiple official FBI sources, this project aims to inform potential strategies for better-targeted community policing and stronger policy intervention.

---

## Research Questions

- Which states report higher levels of hate crime activity?
- What are the most common bias types or offense categories?
- Are there any relationships between age groups of victims and crime type?
- What patterns emerge when analyzing bias alongside crime descriptors like intimidation?

---

## Data Sources

    1. [Hate Crime Statistics 1991–2020 (CSV)](https://www.kaggle.com/datasets/lyonabido/hate-crime-statistics-annual-report-for-2020)  
    2. [FBI Crime in the U.S. – Table 5 (Website)](https://ucr.fbi.gov/crime-in-the-u.s/2019/crime-in-the-u.s.-2019/topic-pages/tables/table-5)  
    3. [FBI Crime Data API](https://api.usa.gov/crime/fbi/cde/)  

All datasets were legally acquired and sourced from the FBI’s public data services.

---

## Data Preparation & Transformation

- Standardized column names across all datasets for consistency (e.g., replacing whitespace with underscores).
- Replaced `NaN` with `NA` where data absence was intentional.
- Dropped null rows only when necessary to preserve data integrity.
- Removed unnecessary columns (e.g., "Year") where all values were identical.
- Applied hierarchical indexing in applicable datasets to improve structure and readability.
- Attempted multiple join strategies based on `state`, `bias`, and `offense_name`.

---

## Final Dataset Approach

Despite initial plans to join all three datasets on `state` and `offense type`, API limitations required a pivot. Two primary join strategies were implemented:

    1. Joined on bias category between datasets to analyze common forms of hate-related offenses.
    2. Joined on state to visualize overall geographic distribution of hate crimes.

---

## Key Visualizations

- Distribution of hate crime occurrences by **state**
- Count of crimes by **bias type**
- Relationship between **juvenile and adult victims**
- Count of victims by **age group**
- Connection between **bias** and **intimidation**

---

## Ethical Considerations

- No assumptions were made in data cleaning that would distort original records.
- Data transformations prioritized fidelity and transparency.
- Ethical implications were considered, particularly regarding misrepresentation of patterns that could influence public policy or law enforcement strategies.

---

## Tools Used

- Python (Pandas, Matplotlib, Seaborn)
- Jupyter Notebook
- FBI API documentation
- Kaggle Datasets
- FBI UCR Table Resources

---

## View the Report

To view the analysis and visualizations:

Open the HTML file in your web browser:

Right-click the file and select "Open with" → "Your Browser" (e.g., Chrome, Firefox).

Explore the interactive elements and visual representations within the report.

Important Note:
It appears that the FBI Crime Data API endpoints have changed, and some of the data originally used in this analysis may no longer be accessible through the same methods. As a result, this project may not be fully reproducible with the original code and data sources. The report, however, remains available for exploration and insight.

---

## License

This project is for educational and demonstration purposes only. No personally identifiable information (PII) is included. All data comes from publicly available government sources and is used in compliance with relevant terms of service.
