# British-Airways-Reviews-Dashboard

## Project Overview
This project involves creating an interactive Tableau dashboard to analyze customer reviews for British Airways, focusing on service quality, satisfaction trends, and key performance metrics. The dashboard visualizes average ratings across categories like overall experience, cabin staff, entertainment, food, ground service, seat comfort, and value for money. It allows users to explore trends over time (by month), geography (by country), aircraft type, traveler type, and other filters. Built using data scraped from customer feedback sites, this dashboard highlights patterns such as declining ratings in recent years and variations by aircraft model, providing insights to help British Airways improve customer satisfaction.

To embed the dashboard (publish to Tableau Public first and replace the src with your view's URL):

<div class='tableauPlaceholder' id='viz1768265049692' style='position: relative'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Br&#47;BritishAirwaysReviews_17682633728490&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='BritishAirwaysReviews_17682633728490&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Br&#47;BritishAirwaysReviews_17682633728490&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>

## Data Sources
- **Primary Dataset**: Customer reviews scraped from Skytrax (airlinequality.com/airline-reviews/british-airways), available on platforms like Kaggle (e.g., "Airline Reviews - British Airways Customer Feedback Dataset").
  - Contains details such as review date, country, seat type, traveler type, aircraft, route, ratings (1-5 or 1-10 scale), and recommendation status.
  - Data spans from March 2016 to October 2023, with approximately 2,500-3,000 reviews depending on the version.

## Tools Used
- **Tableau**: Dashboard creation, visualization, interactivity, and mapping (using Mapbox/OpenStreetMap integration).
- **Optional Preprocessing Tools**: Excel or Python (e.g., Pandas for initial cleaning if needed), but primarily handled in Tableau Prep or directly in Tableau.

## Data Cleaning/Preparation
1. **Handling Missing Values**:  
   - Filled or removed incomplete ratings (e.g., nulls in entertainment or food categories); filtered out reviews without key fields like date or overall rating.
2. **Outlier Treatment**:  
   - Identified and excluded anomalous ratings (e.g., extreme values not aligned with trends) to ensure accurate averages.
3. **Data Type Standardization**:  
   - Converted date strings to proper Date format for time-based analysis; normalized country names for mapping; grouped aircraft models for consistency (e.g., "Boeing 747" variants).
4. **Additional Steps**:  
   - Joined with a country mapping table for geographic visualization; created calculated fields for aggregated averages and filters.

## Exploratory Data Analysis (EDA)
Key questions explored:  
1. How have overall ratings trended monthly from 2016 to 2023? (Line chart shows fluctuations with a general decline, dipping below 3 in recent years—possibly due to post-pandemic issues.)  
2. Which countries report the highest/lowest satisfaction? (Choropleth map indicates variations, with some European countries showing lower averages around 3-4.)  
3. How do ratings differ by aircraft type? (Bar chart reveals premium models like Boeing 747-400 scoring highest at 4.7, while economy-focused A321 scores lowest at 3.6, correlated with review volume.)  
4. What are the weakest service areas? (Summary KPIs highlight low entertainment (1.4) and food (2.4), suggesting improvement opportunities.)  
5. Impact of filters like traveler type or seat class on ratings? (Interactive elements allow slicing, e.g., business travelers may rate higher than leisure.)

Overall insights: British Airways maintains a moderate 4.2 average rating, but declining trends and low scores in entertainment/value indicate areas for enhancement. Higher-rated aircraft correlate with fewer but more positive reviews.
