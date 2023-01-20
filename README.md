EXPLORATOY DATA ANALYSIS (EDA) ON THE INDIAN STARTUP FUNDING DATASET
Introduction
Data Analysis is the process of inspecting, cleaning, processing and modeling data to extract meaningful information to make decisions. This project uses a dataset about the Indian start-up companies and their information such as location, year founded, company name, etc. as well as their funding history from 2018 to 2021, To perform an exploratory data analysis and draw insights from useful information found. One of the great way for a good analysis work is to understand the business problem you are trying to solve. For a better understanding of the problem, create an objective or a scenario to work around. The dataset contains four different csv files with information about Indian startup funding separated by years. Each file has data with common files such as industry, round/series, amount, location and other about the company.

Project Workflow
EDA is a data analysis technique used to understand all aspect of data. In this project the CRISP – DM framework was adopted as a guide. This framework includes
Business Understanding: Understanding the needs of the company and the solutions requested from the data. This is where the objective of analyzing the data is formulated. This can be done by developing a hypothesis with some supportive questions as guidance. The hypothesis and questions below were formulated about the dataset to be a guide in the analysis.
Hypothesis
 Null Hypothesis - Indian Start-ups in the technology industry are likely to receive funding
Alternative Hypothesis - Indian startups in the technology industry are not likely to receive funding¶
Question to guide
1. what are the top five sectors where funding is maximum?
2. what is the highest type of investment made?
3. what is the maximum amount of funding received by a startup?¶
4. what are the top five startups which are investor's favorite?
5. what is the total amount of funds each year?
6. In which year did a startup receive the highest amount of funding?

Data Understanding which involves exploring the data to understand what the dataset is about and all the information in the data. With regards to the Indian startup dataset, there are four files and each file contains information about the Indian startup ecosystem separately grouped yearly from 2018 to 2021. From previewing each file, the following issues were identified about the dataset;
The 2018 DataFrame
The columns in 2018 are different from those of 2019 - 2021, meaning they have to be renamed for concatenation. The amounts in the 2018 DataFrame are a mix of Indian Rupees (INR) and US Dollars (USD), meaning they have to be converted into same currency. The industry and location columns have multiple information. A decision is to be made between selecting the first value before the separator (,) as the main value, or representing that column with a word.
The 2019 DataFrame
The datatype of the "Founded" column is set to float64. It should be set to a string for uniformity. The headquarter column has multiple information. A decision is to be made between selecting the first value before the separator (,) as the main value, or representing that column with a word.
The 2020 DataFrame
There is an extra column called "Unnamed:9", giving it a total of 10 columns. It should be dropped since most of the entries in that columns are null to ensure complete alignment with the other DataFrames for ease of concatenation.
The 2021 DataFrame
The datatype of the "Founded" column is set to float64. It should be set to a string for uniformity. There are some cells that have null values, "Amount" has 3 null cells.

General Observations
The currency signs and commas have to be removed from each of amount column for each DataFrame. 
Data Cleaning or data preprocessing involves cleaning the data set by removing null values, duplicate values, formatting the data types, removing inconsistent values etc. Based on the observations made from previewing each data file, the following assumptions were made:
•	The 2022 average INR/USD rate will be used to convert the Indian Rupee values to US Dollars in the 2018 DataFrame.
•	First values of industry and location in the 2018 data will be selected as the primary sector and headquarters respectively.
•	Amounts without currency symbols are assumed to be in USD ($)
•	Financial analysis will be narrowed to transactions whose amounts are available in the loaded data.
Using the above assumption, each data file was cleaned and all missing values or duplicates that could affect the end result eliminated.


Data processing involves manipulating the data to draw insights and conclusions. After the data was cleaned, all files were concatenated. Using the questions as guide to either affirm or refute the hypothesis.
Conclusion
Based on the analysis on the dataset, my analysis of the Indian startup funding reveals that startups in the tech space are more likely to receive funding. Specifically, I found a strong positive correlation between the number of startups operating within the technology sector and their likelihood for receiving funding based on the results obtained from question one and three which had the technology industry in the top five sectors and a startup from the same industry being the organization with the highest amount of funding. Aside generally the tech sector seemed to attract large amount of money. Therefore, it is safe to say that within India’s ecosystem, technology has proven itself as an attractive industry for investors looking to place their financial resources into startups.

