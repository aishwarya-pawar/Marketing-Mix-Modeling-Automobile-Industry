# Marketing-Mix-Modeling-Automobile-Industry
Optimized marketing mix- effective promotion channels and price for different product types, for car industry using regression model

## Project Title:

Marketing Mix Modeling - Regression 

## Motivation:

"Half the money I spend on advertising is wasted; the trouble is, I don't know which half." - John Wanamaker 
E. Jerome McCarthy proposed the marketing mix with 4 Ps - Product, Price, Promotion and Place. The optimal mix of these 4 Ps defines a successful marketing effort. 
In this project, I am analyzing these 4 Ps to see how automobile industry is performing as per their marketing efforts.



## Data Source:

My Professor at University of Texas, Austin helped with us with the confidential data for the industry. The data had information about the models, their years sales and prices. In the advertisement data, there was retail and corporate level advertising efforts at month level. 
** Note : The data is from year 1995 to 2005. Hence the insights are not applicable for the current car industry


## Analysis Steps:

- Data wrangling was the biggest challenge in this project as the data was very cluttered and in different files. 
  - First we extracted the brand and model information from the advertising channel information
  - Cleaned the channel descriptions to extract maximum information about channel and retail markeitng effort 
  - Filtered unlikely combination of brand and model-line
  - Aggregated the channel spending at model ID level as the sales data was yearly and advertising data was monthly.
  - Merged the files to obtain sales and ad spend data in the same table
- Created flags for luxury and non-luxury models; and domestic and international brands manually
- Exploratory Data Analysis
- Manually create flags for luxury vs non-luxury brands; and domestic vs international brands
- Overall regression model to understand the price elasticity. Since the price elasticity in the initial iterations was positive, we decided to capture the granularity of the data using year flags and brand flags. When the results were intuitive, we proceeded with product split regression analysis
- Built regression model (OLS) and log-log model at following levels  - overall, luxury brands, non-luxury brands, domestic brands, and international brands. Dependent variable : sales 
- Log-log model coefficients represent the elasticity of the variable with the sales. Hence, we checked the correlation of the variables using OLS and elasticity using log-log model

## Findings:

- Significant Variables with their elasticities:

  - Overall:
    - TV (0.21%); Price (-0.54%)
  - Luxury :
    - TV (0.24%); Price (-0.34%)
  - Non-luxury models:
    - TV (0.17%); Price (-0.54%)
  - International Brands:
    - TV (0.13%); Radio(0.07%) ; Print(0.08%); Price (-2.32%)
  - Domestic Brands:
    - TV (0.21%);  Online (0.02%) ; Price (-0.54%)    

- For Luxury models and international brands, the current marketing mix is not optimal and hence there is a potential to optimize it by changing price and channel ad spend mix


## Recommendations:

- For Non-Luxury models, the market is more sensitive towards prices as compared to Luxury models
  - Price centric advertisement campaigns are more likely to be effective for non-luxury segment 
- Among the channels, television has the most impact on driving sales across  segments
- For International brands, print media and radio , along with TV are observed to have potential of driving sales
- By smaller change in price, International brands would be able to capture more sales compared to domestic models; as they are more price sensitive 

## Future Scope:

- Incorporation of monthly trends to calculate inter-advertising spends precisely 
    - Seasonal  effect on channel mix
    - Lag effect on channel mix 
- With online channel information, sales attribution for the channels would be possible. This attribution is not possible with current level of information for offline ad spend 
- Using marketing mix model for future vehicle launches to optimize marketing strategy for pricing and ad spend
