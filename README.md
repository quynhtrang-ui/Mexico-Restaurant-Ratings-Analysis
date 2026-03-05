# Mexico Restaurant Ratings Analysis

## Model view
<img width="1707" height="758" alt="Screenshot 2026-03-05 181131" src="https://github.com/user-attachments/assets/3bb8eb72-ed28-4df5-91b4-0d3bcf3bc400" />

## Calculated Fields
#### Age Group
```
AgeGroup = 
SWITCH(
  TRUE(),
    consumers[Age] <= 18, "Children",
    consumers[Age] <= 30, "Young Adults",
    consumers[Age] <= 60, "Adults",
    "Elderly"
)
```
#### Service Rating Category
```
Service_Rating_Category = SWITCH(
    TRUE(),
    ratings[Service_Rating] = 0, "Poor",
    ratings[Service_Rating] = 1, "Good",
    ratings[Service_Rating] = 2, "Outstanding",
    "Unknown"
)
```
#### Overall Rating Category
```
Overall_Rating_Category = SWITCH(
    TRUE(),
    ratings[Service_Rating] = 0, "Poor",
    ratings[Service_Rating] = 1, "Good",
    ratings[Service_Rating] = 2, "Outstanding",
    "Unknown"
)
```
#### Food Rating Category
```
Food_Rating_Category = SWITCH(
    TRUE(),
    ratings[Service_Rating] = 0, "Poor",
    ratings[Service_Rating] = 1, "Good",
    ratings[Service_Rating] = 2, "Outstanding",
    "Unknown"
)
```

## Overview
This Power BI dashboard provides comprehensive insights into the restaurant market in Mexico, with a focus on customer satisfaction, dining preferences, and the impact of amenities on overall ratings. The dashboard is split into four pages: **Market Overview**, **Restaurant Amenities**, **Customer Information**, and **Detailed Performance & Rankings**.

## Page 1:
<img width="1135" height="642" alt="1" src="https://github.com/user-attachments/assets/e3435bc7-ffd6-4673-b2ce-efa1fbd28add" />

### Key Visuals:

1. **Overview KPI Cards**:
  - Visualizes the overall scale of the dataset, including total reviews, customers, restaurants, cuisines, and geographical reach.
  - **Key Insight**: The analysis is based on a robust sample size of 1,161 reviews from 120 customers, covering 130 restaurants across 4 cities.

2. **Overall Consumer Ratings**:
  - Visualizes the distribution of overall customer feedback into three categories: Outstanding, Good, and Poor.
  - **Key Insight**: The general customer sentiment is highly positive, with "Outstanding" (486) and "Good" (421) making up the vast majority of reviews compared to "Poor" (254).

3. **Top Highest Rated Restaurants**:
  - Highlights the best-performing restaurants ranked by their average rating scores (up to 2.00).
  - **Key Insight**: Emilianos, Michiko Restaurant, and Restaurant La... are the top market leaders, achieving perfect rating scores of 2.00.

4. **Most Popular Cuisine Types**:
  - Compares the frequency of different cuisine categories available among the listed restaurants.
  - **Key Insight**: Mexican cuisine is overwhelmingly the most dominant choice in the market, significantly outpacing other options like Bar, Cafeteria, and Fast Food.

## Page 2:
<img width="1148" height="658" alt="2" src="https://github.com/user-attachments/assets/c05b446d-4362-4ae3-b6ee-4c0dc61bc888" />

### Key Visuals:

1. **Restaurant Price & Parking**:
  - Key Insight: Restaurants in the Low and Medium price segments make up the vast majority of the "None" parking category, whereas Valet parking is more frequently associated with High-priced venues.

2. **Closed/Open Restaurant Ratings**:
  - Key Insight: The vast majority of restaurants in the dataset are recorded as Closed (115 locations), and interestingly, this group achieves a noticeably higher average rating score than the Open group.

3. **Alcohol Service Ratings**:
  - Key Insight: Although most venues do not serve alcohol (87 locations), establishments that offer "Wine & Beer" or a "Full Bar" achieve significantly higher rating scores compared to those that offer none.

4. **Ratings of All Restaurants**:
  - Key Insight: There is considerable volatility in scores among different brands, indicating highly variable service quality and customer experiences across the market.

5. **Smoking in Restaurant Ratings**:
  - Key Insight: While the majority of restaurants enforce a strict no-smoking policy (No - 95 locations), the highest average rating scores are actually found at venues that restrict smoking to "Bar Only".

## Page 3:
<img width="1132" height="645" alt="3" src="https://github.com/user-attachments/assets/fceb43ba-6881-45f2-9372-5496c23e9ea3" />

### Key Visuals

1. **Customer Age Group**:
  - Visualizes the proportion of customers across different age demographic segments (Young Adults, Elderly, Adults, Children).
  - **Key Insight**: An overwhelming 90% of the customer base consists of Young Adults.

2. **Customer Distribution by City & State**:
  - Key Insight: Customers are heavily concentrated in a few specific urban areas (such as San Luis Potosi, Cuernavaca, and Ciudad Victoria), directly aligning with the restaurant locations.

3. **Marital Status vs. Smoking & Drinking**:
  - Key Insight: The dominant customer profile is Single individuals who do not smoke and identify as "Abstemious" (non-drinkers). This is closely followed by Single "Casual Drinkers" who also do not smoke.

4. **Occupation and Budget**:
  - Key Insight: The vast majority of the audience are Students operating on "Medium" or "Low" budgets, indicating a highly price-sensitive consumer base.

## Page 4:
<img width="1161" height="679" alt="4" src="https://github.com/user-attachments/assets/2e6dd8c1-6bc7-4801-9aa4-8971ca54e56b" />

## Future Enhancements:
- **Operational Strategy**: Do not waste capital on real estate with large parking lots. Instead, prioritize securing a liquor license (specifically for Wine & Beer) to increase ancillary revenue and elevate the perceived dining experience.
- **Competitive Advantage**: Invest heavily in customer service training. Because the overall market is being dragged down by poor service scores (1.09), a budget-friendly restaurant that consistently delivers fast, friendly service will immediately stand out and easily capture market share.

