# Project 1

Exploring data as a group led us to data.gov, where we set our sights on a dataset on public safety. We selected the 'Crash Data in Tempe, Arizona' dataset because of its dual format of a CSV file and accompanying JSON properties.

Variety in data representation held the potential for a more nuanced and insightful analysis.

# Cleaning Data

Exploratory Data Analysis:

- Imported the CSV file and initiated exploratory data analysis.
- Used crash_data.shape to determine the dataset's dimensions (rows and columns).
- Employed crash_data.isna().sum() to identify missing values, with a focus on  Driver 2-related columns.

Time Range Selection:

- Initially considered data from 2020 to 2023 but opted for a broader scope, excluding pre-Covid years.
- Used the loc method to filter the dataset for the selected years.

Missing Values Update:

- Reassessed missing values using isna() and sum() specifically on the chosen years, noting a significant reduction.

Concise Data Summary:

- Utilized the info method to obtain a concise summary of the dataset, including column data types.

Statistical Analysis:

- Employed the describe method to gather statistical insights into the dataset, including non-numerical values.

Outlier Identification:

- Generated box plots for numerical data to detect and identify outliers.
- Applied detect_and_treat_outliers function to calculate z-scores, identify outliers, and remove affected rows.

Column Removal:

- Excluded unnecessary columns ('x', 'y', 'OBJECTID').
- Filtered the dataset to include only driver-vs-driver incidents.

Additional Column Removal:

- Removed 'Unittype_One' and 'Unittype_Two' columns as they were not relevant for the narrowed focus.

Summary Update:

- Reviewed and summarized null entries in the modified dataset.

Outlier Treatment:

- Utilized the detect_and_treat_outliers function to handle outliers based on z-scores and IQR, resulting in a cleaner dataset.

Handling Missing Values:

- Retained missing values in 'Cross Streets' column, recognizing that not all accidents occurred at intersections.
- Imputed missing values in 'Cross Streets' using the fillna method, replacing empty cells with "unknown."

Verification:

- Checked the shape of the dataset to ensure completeness.
- Examined accident counts on 'Cross Streets' and imputed missing values to enhance dataset integrity.

Data Preparation:

- Separated DateTime columns into two distinct columns and dropped the original DateTime column.
- Updated column names for clarity and readability.
- Exported the cleaned dataset as a new CSV file.

# GeoMapping

We used geomapping techniques to unravel insights into collision occurrences in Tempe, Arizona, spanning the years 2019 to 2022. The initial heatmap provides a visual representation of collision hotspots, revealing a concentrated cluster in red. In the actual HTML link, we discovered that this hotspot is situated within a 2-mile radius of the Arizona State University Tempe Campus, and 7-mile radius from Phoenix International Airport.


The bar graph illustrates the frequency of collisions per Cross Street. As you can see, McClintock Dr is the street with the highest collision count over the four-year period.

The following maps illustrate collisions based on coordinates and intersections. The color density in these maps reflects collision counts, with darker shades indicating higher occurrences. The second map, highlights the top 20 intersections for collisions by cross streets, further emphasizing a consistent pattern of high collision incidence within the same Tempe area.

Lastly, we delved into mapping the top 50 intersections of collisions, categorized by the cause of the collision. The interactive HTML file allows for zooming in to examine each icon's representation of accidents and their respective causes, as detailed in the accompanying dataframe snippet.

Through the data, we hone in on the specific intersection of McClintock and Don Carlos Ave had the highest count of collision occurrence with the cause being driveers failing to yield the right of way. 

Two images further illustrate the the street view of this intersection.

These comprehensive visualizations and analyses not only pinpoint critical collision areas but also shed light on causal factors, enabling us to make informed decisions towards enhancing road safety and formulating targeted intervention strategies.

# Hourly/Daily/Yearly Data Analysis 

In the course of this project, we conducted a comprehensive analysis of the temporal aspects of accidents. Our examination encompassed the identification of peak days for accident occurrences, an investigation into annual accident frequencies to discern potential trends, and an assessment of the average number of accidents within each hourly interval across a 24-hour period.

In our analysis of daily accident counts, notable peaks were observed during holiday seasons and the summer months. In the annual breakdown, a surge in accidents was evident in 2019 (pre-COVID), followed by a sharp decline in 2020, presumably attributed to the impact of the COVID-19 pandemic and associated quarantine measures. Subsequently, from 2021 onwards, a discernible upward trend in accident frequencies emerged.

The hourly breakdown of average accident counts within a 24-hour period revealed an elevated average from 12 am to 4 am, followed by a subsequent decline in the ensuing hours. Notably, the average accident count experienced a resurgence in the late-night hours, particularly from 10 pm onwards. Overall, the general pattern indicates a higher average accident count throughout a 24-hour period in 2019, a decrease in 2020, and a subsequent recovery from 2021 onwards.

# Statistics 

The F-statistic is a value you get from the ANOVA test which basically tells you if the variances between your groups are significantly different. 
The P-value tells you the statistical significance of your result. 
Commonly, a P-value <0.05 is considered significant, meaning that the group means are statistically significantly different.
Based on the data available for Age of Drivers from who possibly caused the crash and who was the one impacted, there is a statistical significant difference seen in the age groups.

We compared the means of the two variables which were Driver Age 1 and Age 2 for which we got the results which were t-statistic: 2.1908902300206643
p-value: 0.05983787551928609
Fail to reject the null hypothesis: There is no significant difference.

# Conclusion 

In our ongoing effort to enhance public safety and emergency response effectiveness, we recently conducted a thorough analysis of traffic accidents in Tempe, Arizona. Our dataset, meticulously gathered, includes information such as longitude, latitude, cross streets, street names, injury severity, and the cause of each accident.

Due to the frequency of accidents occurring near specific intersections, we sought to understand the proximity of medical care available to potential accident victims. Leveraging an API key, we conducted a search for hospitals in the area. The results were quite illuminating.

From our map visualization, it became evident that the hospital is strategically located within the hotspots of frequent accidents in the city of Tempe. This insight is invaluable, as it sheds light on the accessibility of medical assistance for those involved in accidents in these critical zones.

Our findings not only contribute to our understanding of the geographical distribution of accidents but also provide essential information for emergency responders and policymakers. This data-driven approach is instrumental in shaping strategies for optimizing emergency services and improving overall public safety.

# Resources

- Class Activity Solved Files
- Past Homework Files
- Online Research
- Study sessions supporting one another 