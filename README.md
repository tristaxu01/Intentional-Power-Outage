#### Created by Trista Xu and Tunan Li
# Introduction
Between **January 2000 to July 2016**, there were total of 1534 number power outrage that impacted at least 50,000 customers or caused an unplanned firm load loss of atleast 300 MW occured in United State. The largest power outage affected approximately 3.5 million people, and a maximum of 41,788 MW Peak Demand Power was lost during a single outage event. The focus of our website is to investigate the relationship between monthly electricity prices in the residential sector (labeled as "RES.PRICE" in the dataset) and power outages caused by intentional attacks. Specifically, we aim to determine **whether regions with a top 25% residential electricity price are more likely to experience power outages caused by intentional attacks.** 

To do this, our team will analyze data from the "RES.PRICE," "Number of customers affected by the power outage event" ("CUSTOMER AFFECTED"), and "Categories of all the events causing the major power outages" ("CAUSE CATEGORY") columns.

|   YEAR |   MONTH | U.S._STATE   | POSTAL.CODE   | NERC.REGION   | CLIMATE.REGION     |   ANOMALY.LEVEL(numeric) | CLIMATE.CATEGORY   | OUTAGE.STAR (Y-M-D time)   | OUTAGE.RESTORATION (Y-M-D time)        | CAUSE.CATEGORY     | CAUSE.CATEGORY.DETAIL   |   HURRICANE.NAMES |   OUTAGE.DURATION(mins) |   DEMAND.LOSS.MW(Megawatt) |   CUSTOMERS.AFFECTED |   RES.PRICE(cents / kilowatt-hour) |   COM.PRICE(cents / kilowatt-hour) |   IND.PRICE(cents / kilowatt-hour) |   TOTAL.PRICE(cents / kilowatt-hour) |   RES.SALES(Megawatt-hour) |   COM.SALES(Megawatt-hour) |   IND.SALES(Megawatt-hour) |   TOTAL.SALES(Megawatt-hour) |   RES.PERCEN(%) |   COM.PERCEN(%) |   IND.PERCEN(%) |   RES.CUSTOMERS |   COM.CUSTOMERS |   IND.CUSTOMERS |   TOTAL.CUSTOMERS |   RES.CUST.PCT(%) |   COM.CUST.PCT(%) |   IND.CUST.PCT(%) |   PC.REALGSP.STATE(USD) |   PC.REALGSP.USA(USD) |   PC.REALGSP.REL(fraction) |   PC.REALGSP.CHANGE(%) |   UTIL.REALGSP(USD) |   TOTAL.REALGSP(USD) |   UTIL.CONTRI(%) |   PI.UTIL.OFUSA(%) |   POPULATION |   POPPCT_URBAN(%) |   POPPCT_UC(%) |   POPDEN_URBAN(persons per square mile) |   POPDEN_UC(persons per square mile) |   POPDEN_RURAL(persons per square mile) |   AREAPCT_URBAN(%) |   AREAPCT_UC(%) |   PCT_LAND(%) |   PCT_WATER_TOT(%) |   PCT_WATER_INLAND(%) |
|-------:|--------:|:-------------|:--------------|:--------------|:-------------------|-------------------------:|:-------------------|:---------------------------|:---------------------------------------|:-------------------|:------------------------|------------------:|------------------------:|---------------------------:|---------------------:|-----------------------------------:|-----------------------------------:|-----------------------------------:|-------------------------------------:|---------------------------:|---------------------------:|---------------------------:|-----------------------------:|----------------:|----------------:|----------------:|----------------:|----------------:|----------------:|------------------:|------------------:|------------------:|------------------:|------------------------:|----------------------:|---------------------------:|-----------------------:|--------------------:|---------------------:|-----------------:|-------------------:|-------------:|------------------:|---------------:|----------------------------------------:|-------------------------------------:|----------------------------------------:|-------------------:|----------------:|--------------:|-------------------:|----------------------:|
|   2011 |       7 | Minnesota    | MN            | MRO           | East North Central |                     -0.3 | normal             | 2011-07-01 17:00:00        | Sunday, July 03, 2011 8:00:00 PM       | severe weather     | nan                     |               nan |                    3060 |                        nan |                70000 |                              11.6  |                               9.18 |                               6.81 |                                 9.28 |                    2332915 |                    2114774 |                    2113291 |                      6562520 |         35.5491 |         32.225  |         32.2024 |         2308736 |          276286 |           10673 |           2595696 |           88.9448 |           10.644  |            0.4112 |                   51268 |                 47586 |                    1.07738 |                    1.6 |                4802 |               274182 |          1.75139 |                2.2 |      5348119 |             73.27 |          15.28 |                                    2279 |                               1700.5 |                                    18.2 |               2.14 |             0.6 |       91.5927 |            8.40733 |               5.47874 |
|   2014 |       5 | Minnesota    | MN            | MRO           | East North Central |                     -0.1 | normal             | 2014-05-11 18:38:00        | Sunday, May 11, 2014 6:39:00 PM        | intentional attack | vandalism               |               nan |                       1 |                        nan |                  nan |                              12.12 |                               9.71 |                               6.49 |                                 9.28 |                    1586986 |                    1807756 |                    1887927 |                      5284231 |         30.0325 |         34.2104 |         35.7276 |         2345860 |          284978 |            9898 |           2640737 |           88.8335 |           10.7916 |            0.3748 |                   53499 |                 49091 |                    1.08979 |                    1.9 |                5226 |               291955 |          1.79    |                2.2 |      5457125 |             73.27 |          15.28 |                                    2279 |                               1700.5 |                                    18.2 |               2.14 |             0.6 |       91.5927 |            8.40733 |               5.47874 |
|   2010 |      10 | Minnesota    | MN            | MRO           | East North Central |                     -1.5 | cold               | 2010-10-26 20:00:00        | Thursday, October 28, 2010 10:00:00 PM | severe weather     | heavy wind              |               nan |                    3000 |                        nan |                70000 |                              10.87 |                               8.19 |                               6.07 |                                 8.15 |                    1467293 |                    1801683 |                    1951295 |                      5222116 |         28.0977 |         34.501  |         37.366  |         2300291 |          276463 |           10150 |           2586905 |           88.9206 |           10.687  |            0.3924 |                   50447 |                 47287 |                    1.06683 |                    2.7 |                4571 |               267895 |          1.70627 |                2.1 |      5310903 |             73.27 |          15.28 |                                    2279 |                               1700.5 |                                    18.2 |               2.14 |             0.6 |       91.5927 |            8.40733 |               5.47874 |
|   2012 |       6 | Minnesota    | MN            | MRO           | East North Central |                     -0.1 | normal             | 2012-06-19 04:30:00        | Wednesday, June 20, 2012 11:00:00 PM   | severe weather     | thunderstorm            |               nan |                    2550 |                        nan |                68200 |                              11.79 |                               9.25 |                               6.71 |                                 9.19 |                    1851519 |                    1941174 |                    1993026 |                      5787064 |         31.9941 |         33.5433 |         34.4393 |         2317336 |          278466 |           11010 |           2606813 |           88.8954 |           10.6822 |            0.4224 |                   51598 |                 48156 |                    1.07148 |                    0.6 |                5364 |               277627 |          1.93209 |                2.2 |      5380443 |             73.27 |          15.28 |                                    2279 |                               1700.5 |                                    18.2 |               2.14 |             0.6 |       91.5927 |            8.40733 |               5.47874 |
|   2015 |       7 | Minnesota    | MN            | MRO           | East North Central |                      1.2 | warm               | 2015-07-18 02:00:00        | Sunday, July 19, 2015 7:00:00 AM       | severe weather     | nan                     |               nan |                    1740 |                        250 |               250000 |                              13.07 |                              10.16 |                               7.74 |                                10.43 |                    2028875 |                    2161612 |                    1777937 |                      5970339 |         33.9826 |         36.2059 |         29.7795 |         2374674 |          289044 |            9812 |           2673531 |           88.8216 |           10.8113 |            0.367  |                   54431 |                 49844 |                    1.09203 |                    1.7 |                4873 |               292023 |          1.6687  |                2.2 |      5489594 |             73.27 |          15.28 |                                    2279 |                               1700.5 |                                    18.2 |               2.14 |             0.6 |       91.5927 |            8.40733 |               5.47874 |

# Exploratory Data Analysis
## Data Cleaning
First, we identify and drop redundant information: The raw dataframe contains several columns or rows of NaN values that do not provide any useful information for the analysis. Removing redundant columns can improve processing times and reduce noise in the data.

Secondly, we identify and convert data to the correct types: If the data contains datatypes that do not match the data value (e.g., an integer value with a string type), they should be converted to the desired datatype to ensure consistency of the dataframe and prevent errors when performing calculations or data aggregation.

Alongside, we consolidate rows with repetitive information: The raw data separates each column title and its corresponding units. The information about units needs to be combined into the same row for what it is describing. This makes the data easier to work with and avoids confusion when analyzing the data.

Similarly, our team also found several columns describing time objects but separate day and time. Merging that information allows for more accurate and precise analysis of time-related data.

Lastly, we rename columns: Many column names from the raw dataframe were abbreviations and ambiguous. During the cleaning process, they were renamed to names that are easier to understand and interpret.

The impact of these data cleaning steps on subsequent analyses will depend on the specific research question and the nature of the data. However, in general, cleaning the data can help ensure accuracy and consistency in the analysis, reduce errors and noise in the data, and make the data easier to work with and interpret. Ultimately, the goal of data cleaning is to improve the quality and reliability of the data for analysis.



## Univariate Analysis
<iframe src="assets/state_fig.html" width=800 height=600 frameBorder=0></iframe>
This plot counts the total amount of power outage occurrences in different states.

<iframe src="assets/cause_fig.html" width=800 height=600 frameBorder=0></iframe>
This plot indicates the percentage of categories of all the events causing the major power outages.

<iframe src="assets/res_price_fig.html" width=800 height=600 frameBorder=0></iframe>
This boxplot shows the distribution of the residential power price, measured in cents per kilowatt-hour. The total price distribution was split into two categories based on the third quartile: the top 25% of residential electricity prices are categorized as high price, while the rest are categorized as low price. This visualization aims to investigate whether there is a correlation between the price category and the category of power outage causes. Our team decide to drop the NaNs in the "RES.PRICE" since the number of NaNs is negligible to the whole dataset(only less than 1% of data are NaNs). The plot suggests that higher residential prices may correlate with intentional attacks and severe weather conditions.

| index   |   RES.PRICE(cents / kilowatt-hour) |
|:--------|-----------------------------------:|
| count   |                         1512       |
| mean    |                           11.9684  |
| std     |                            3.08863 |
| min     |                            5.65    |
| 25%     |                            9.54    |
| 50%     |                           11.46    |
| 75%     |                           13.9     |
| max     |                           34.58    |

## Assessment of Missingness

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


# Assessment of Missingness

## NMAR Analysis: 
After analyzing the cleaned dataset, our team has determined that the column **"OUTAGE.RESTORATION (Y-M-D time)"** is **N**ot **M**issing **A**t **R**andom. This column indicates the time when power is restored in the outage region. However, due to the nature of power restoration, which may occur gradually by neighborhood over a period of several hours, it is not always possible to record the exact restoration time as a fixed point in time. Consequently, in some instances, the restoration time has been recorded as NaN in the dataframe.
## Missingness Dependency
To measure the "distance" between categorical distributions, we use the total variation distance.
### Assessing Missingness of "CUSTOMER AFFECTED" with “Climate Change Category”
<iframe src="assets/obeserved TVD.html" width=800 height=600 frameBorder=0></iframe>
The plot compares the distribution of the Climate Change Category when "CUSTOMER AFFECTED" is missing to the distribution of the Climate Change Outage Category when "CUSTOMER AFFECTED"" is not missing.

<iframe src="assets/TVD.html" width=800 height=600 frameBorder=0></iframe>
Based on the plot, we conclude that the distribution of the Climate Change Category when "CUSTOMER AFFECTED" is missing is the same as the distribution of the Climate Change Category when "CUSTOMER AFFECTED" is not missing. 
**The Missingness of "CUSTOMER AFFECTED" may not depend on "Climate Change Category"**

### Assessing Missingness of "CUSTOMER AFFECTED" with “U.S. STATE”

<iframe src="assets/obeserved TVD in US states.html" width=800 height=600 frameBorder=0></iframe>
The plot compares the distribution of the state of the power outage region when "CUSTOMER AFFECTED" is missing to the distribution of the state of the power outage region when "CUSTOMER AFFECTED"" is not missing.

<iframe src="assets/TVD distribution in US states.html" width=800 height=600 frameBorder=0></iframe>
Based on the plot, we conclude that the distribution of the "U.S. States" when "CUSTOMER AFFECTED" is missing is not the same as the distribution of the "U.S. States" when "CUSTOMER AFFECTED" is not missing. 
**The Missingness of "CUSTOMER AFFECTED" may depend on “U.S. STATE”(the state of the power outage region)**

# Hypothesis Testing
 
#### H0: Number of intentional attack in high price region == Number of intentional attack in high price region
**Null Hypothesis:** The distribution of residential electricity prices and the number of power outages caused by intentional attack is not different. Any differences observed in our samples are due to random chance.

#### H1: Number of intentional attack in high price region > Number of intentional attack in high price region
**Alternative Hypothesis:** A higher residential electricity price leads to more power outages caused by intentional attack. Any differences observed in our samples are not due to random chance.

To test these hypotheses, we use the difference in power outage occurrence between the high electricity price region (i.e., the region that pays the top 25% of electricity prices in the US) and the lower electricity price region (i.e., the region that pays less than the top 25% of electricity prices in the US) as our test statistic.

The significance level of 0.05 is a common choice in statistical analysis.
We chose the difference in proportion as our test statistic because it provides a clear indication of whether larger values support the alternative hypothesis or smaller values support the null hypothesis.

<iframe src="assets/Hypo.html" width=800 height=600 frameBorder=0></iframe>

### p-value = 0.4454
Based on our analysis, we have set the significance level at **0.05**. However, the p-value we obtained was **0.4454**, which is much higher than the significance level. Therefore, we fail to reject the null hypothesis, and we cannot conclude that the price of electricity causes the number of sabotages that lead to power outages.

