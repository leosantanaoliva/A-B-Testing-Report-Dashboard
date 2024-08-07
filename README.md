# A-B-Testing-Report-Dashboard

The project goal is to support the company’s next decision by enhancing the visibility of A/B Testing.
## Dataset:

This dataset concerns a marketing campaign involving ads. Since the market might seem complex, the company chose to run an A/B test to measure how successful the marketing campaign has been. 

The companies are interested in answering two questions:
Would the campaign be successful?
If the campaign was successful, how much of that success could be attributed to the ads?

To create this test, people were segmented into two groups: one group saw the ads, and the other saw the public service announcement.
### Dataset Structure:

- Index: Row index
- User id: User ID (unique)
- test group: If "ad" the person saw the advertisement, if "psa" they only saw the public service announcement
- converted: If a person bought the product then True, else is False
- total ads: Amount of ads seen by person
- most ads day: Day that the person saw the biggest amount of ads
- most ads hour: Hour of day that the person saw the biggest amount of ads

## Project Structure:

- Data Extraction
Data was extracted from the source using a REST API process.

- Data Cleaning
To ensure data accuracy and consistency, the following steps were taken:

  - The index column was dropped as it was not important for the analysis.
  - Outliers were identified and addressed since they can significantly mislead the analysis results.

- Dashboard Development
![ab_testing_page-0001](https://github.com/leosantanaoliva/A-B-Testing-Report-Dashboard/assets/74313125/bc663eee-c8a0-421b-a5d0-1955dc7c10c4)

## Tools used:
- Python
- Power BI

## Results

### Would the campaign be successful?

To determine if the campaign would be successful, we need to compare the conversion rates between the two groups (ads and PSA).

Conversion Rate for Ads Group: 1.34%.

Conversion Rate for PSA Group: 1.03%.

The ads group has a higher conversion rate (1.34%) compared to the PSA group (1.03%).

### If the campaign was successful, how much of that success could be attributed to the ads?

To determine how much of the success can be attributed to the ads, we can look at the total number of conversions and the conversion rates.

Total Users in Ads Group: 514.72K.

Total Users in PSA Group: 21.20K.

Total Conversions in Ads Group: 6889.

Total Conversions in PSA Group: 219.

From these numbers, we can calculate the increase in conversions due to the ads:

Difference in conversion rates = 1.34% - 1.03% = 0.31%.

Total conversions attributable to the ads = (Conversion Rate Difference) * (Total Users in Ads Group).

Total conversions attributable to the ads = 0.31% * 514,720 = 1,595.63 (approximately 1,596 conversions).

Approximately 1,596 conversions can be attributed to the ads.

### Insights from the Dashboard

- Conversion Analysis:
The conversion rate is higher for the ads group compared to the PSA group.
Conversion rates vary by day of the week and hour of the day, suggesting that timing can influence ad effectiveness.

- Ad Exposure Analysis:
The distribution of total ads seen indicates that most users saw fewer than 20 ad

Conversion rates and ad exposure times suggest that certain days and hours are more effective for ad campaigns.
These insights can help optimize future marketing strategies by focusing ad exposure during the most effective times and ensuring that the frequency of ads remains within the optimal range.

## References
https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing/data 
