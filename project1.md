1. **A description of the housing data you scraped from zillow:**
- 400 homes from Austin, Texas were collected from the Zillow website. There were no missing entries in the initial dataset and therefore all the datapoints were retained. This table below includes the descriptive statistics of the dataset: 

| measure | price ($) | # of beds | # of baths | sqft |
|---------|-------|-----------|------------|------|
| mean    | 823865     | 3  |      3      |    2556  |
| std     |  1271322|    1.12   |     1.37       |    1774.36  |
| min     | 95000 |      1    |    1        |   401   |
| 25%     |  325000|     3 |       2     |  1624    |
| 50%     |482500       |  4     |  3          |  2161    |
| 75%     |749750       |    4   |   3         | 3054     |
| max     |12900000       |  8  |     10       |    10887  |

- It is unsurprising to see that more expensive houses have more beds and bathrooms, and are significantly larger than the less expensive houses. In fact, houses who rank at 75 percentile in price is almost twice as large as houses with prices ranked in 25% percentile. Across houses of different prices, the number of bedrooms and bathrooms only varied in a small amount. This may be explained by the common sense that houses do not need an excessive amount of bedrooms and bathrooms since we no longer live in Victorian castles. This also might mean that the number of bedrooms and bathrooms would not be good predictors for house price. On the other hand, since the sqft of the house is generally positively correlated with the price of the house, sqft may be a better predictor for price compared to the number of bedrooms and bathrooms. 
- 
