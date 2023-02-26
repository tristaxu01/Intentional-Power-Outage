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