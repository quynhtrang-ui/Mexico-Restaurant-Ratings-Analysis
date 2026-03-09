# Mexico Restaurant Ratings Analysis

# Data Model

The dataset includes information about:

- Restaurants
- Customer reviews
- Consumer demographics
- Restaurant amenities

The model integrates multiple tables including restaurant details, consumer profiles, and rating information.

<img width="1707" height="758" src="https://github.com/user-attachments/assets/3bb8eb72-ed28-4df5-91b4-0d3bcf3bc400" />


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

# Dashboard Overview

The Power BI report contains four main pages:

### Market Overview
Provides a general view of the restaurant market.

Key metrics include:
- 1161 reviews
- 120 customers
- 130 restaurants
- 4 cities

<img width="1135" height="642" src="https://github.com/user-attachments/assets/e3435bc7-ffd6-4673-b2ce-efa1fbd28add" />

---

### Restaurant Amenities
Analyzes how restaurant features impact ratings.

Examples include:
- price range
- parking availability
- alcohol service
- smoking policy

<img width="1148" height="658" src="https://github.com/user-attachments/assets/c05b446d-4362-4ae3-b6ee-4c0dc61bc888" />

---

### Customer Demographics
Explores customer characteristics such as:

- age groups
- occupation
- budget levels
- lifestyle habits

<img width="1132" height="645" src="https://github.com/user-attachments/assets/fceb43ba-6881-45f2-9372-5496c23e9ea3" />

---

### Restaurant Performance
Ranks restaurants and highlights rating differences across locations.

<img width="1161" height="679" src="https://github.com/user-attachments/assets/2e6dd8c1-6bc7-4801-9aa4-8971ca54e56b" />

---

# Key Insights

- **Service quality (1.09)** is rated lower than **food quality (1.22)**, suggesting service improvement is the biggest opportunity for restaurants.
- Restaurants offering **Wine & Beer tend to receive higher ratings**.
- The customer base is dominated by **young students with medium budgets**.
- **Restaurant price level has limited impact on ratings**.
- A small group of restaurants consistently achieves **outstanding ratings**.

---

# Tools Used

- **Power BI**
- **DAX**
- **Data Modeling**

