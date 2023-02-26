# US-Power-Outages

# Introduction
Between **January 2000 to July 2016**, there were total of 1534 number power outrage that impacted at least 50,000 customers or caused an unplanned firm load loss of atleast 300 MW occured in United State. The largest power outage affected approximately 3.5 million people, and a maximum of 41,788 MW Peak Demand Power was lost during a single outage event. The focus of our website is to investigate the relationship between monthly electricity prices in the residential sector (labeled as "RES.PRICE" in the dataset) and power outages caused by intentional attacks. Specifically, we aim to determine **whether regions with a top 25% residential electricity price are more likely to experience power outages caused by intentional attacks.** 

To do this, our team will analyze data from the "RES.PRICE," "Number of customers affected by the power outage event" (CUSTOMERS.AFFECTED), and "Categories of all the events causing the major power outages" (CAUSE.CATEGORY) columns.

# Data Cleaning
First, we identify and drop redundant information: The raw dataframe contains several columns or rows of NaN values that do not provide any useful information for the analysis. Removing redundant columns can improve processing times and reduce noise in the data.

Secondly, we identify and convert data to the correct types: If the data contains datatypes that do not match the data value (e.g., an integer value with a string type), they should be converted to the desired datatype to ensure consistency of the dataframe and prevent errors when performing calculations or data aggregation.

Alongside, we consolidate rows with repetitive information: The raw data separates each column title and its corresponding units. The information about units needs to be combined into the same row for what it is describing. This makes the data easier to work with and avoids confusion when analyzing the data.

Similarly, our team also found several columns describing time objects but separate day and time. Merging that information allows for more accurate and precise analysis of time-related data.

Lastly, we rename columns: Many column names from the raw dataframe were abbreviations and ambiguous. During the cleaning process, they were renamed to names that are easier to understand and interpret.

The impact of these data cleaning steps on subsequent analyses will depend on the specific research question and the nature of the data. However, in general, cleaning the data can help ensure accuracy and consistency in the analysis, reduce errors and noise in the data, and make the data easier to work with and interpret. Ultimately, the goal of data cleaning is to improve the quality and reliability of the data for analysis.

# Univariate Analysis

This plot counts the total amount of power outage occurrences in different states.
<iframe src="assets/state_fig.html" width=800 height=600 frameBorder=0></iframe>


This plot indicates the percentage of categories of all the events causing the major power outages.
<iframe src="assets/cause_fig.html" width=800 height=600 frameBorder=0></iframe>

This boxplot shows the distribution of the residential power price, measured in cents per kilowatt-hour. The total price distribution was split into two categories based on the third quartile: the top 25% of residential electricity prices are categorized as high price, while the rest are categorized as low price. This visualization aims to investigate whether there is a correlation between the price category and the category of power outage causes. The plot suggests that higher residential prices may correlate with intentional attacks and severe weather conditions.
<iframe src="assets/res_price_fig.html" width=800 height=600 frameBorder=0></iframe>

# Assessment of Missingness
|   RES.PRICE(cents / kilowatt-hour) |   COM.PRICE(cents / kilowatt-hour) |   IND.PRICE(cents / kilowatt-hour) |   TOTAL.PRICE(cents / kilowatt-hour) |
|-----------------------------------:|-----------------------------------:|-----------------------------------:|-------------------------------------:|
|                            11.6718 |                           10.3195  |                            7.6286  |                             10.1533  |
|                            14.7898 |                           12.6902  |                            8.6248  |                             12.6672  |
|                            **12.1265** |                           10.0933  |                            7.16923 |                             10.0774  |
|                            13.2293 |                           11.7702  |                            8.77413 |                             11.5096  |
|                            10.8541 |                            9.19797 |                            6.70174 |                              9.25551 |
|                            11.7143 |                            9.88085 |                            7.22776 |                              9.90073 |
|                            12.139  |                           10.6279  |                            7.79025 |                             10.4984  |

The table suggests a correlation between severe weather and intentional attacks and the price of electricity. To test the hypothesis that higher electricity prices may cause people to be unable to pay for electricity and, consequently, sabotage the electricity supply, we propose performing a permutation test.
