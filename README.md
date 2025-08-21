
# Hackathon Group Project - Car Price Analysis - Team NaMiPaJay Crew
**Group Members:**
- Project Manager - Ajay
- Data Architect - Nasra
- Data Architect - Milos
- Data Analyst - Payal

**Car Price Analysis** 
- An automobile company aims to enter the US market and compete with local and European manufacturers. The goal is to analyse car prices based on various independent variables to understand the factors affecting car pricing in the US market. Develop interactive dashboards to provide insights into car pricing dynamics, helping the company design cars and develop business strategies that meet market demands.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* The dataset used is a cleaned version of the [Kaggle Car Price Prediction dataset](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction), titled `cleaned_data_stage1.csv`. It includes key attributes such as:
- `Car_company`, `car_model`,`Fuel_Type`, `curb weight`
- `Mileage`, `Engine size`, `horespower`, `car length`, `car height` and `price`

Each row represents an individual car listing from the US used car market.


## Business Requirements
 **The business aims to:**
- Understand pricing patterns by brand and car specifications.
- Explore the impact of fuel type, engine size, and transmission on price.
- Help marketing and design teams create competitive pricing strategies.

##
**Hypotheses:**
- As part of the analytical workflow, a dedicated hypothesis testing notebook was created to statistically validate key insights identified in the Power BI dashboard. This step ensures that observed patterns in the data are not just visually compelling but also statistically significant.
1. Cars with higher horsepower have higher prices.
2. Luxury brands (e.g., Jaguar, Porsche, Buick) have statistically higher prices than standard brands.
3. Engine size, curb weight, and car dimensions all show a strong positive correlation with car price.
4. Fuel efficiency (highway MPG) is negatively correlated with price, indicating that more economical vehicles are generally less expensive.
5. Diesel cars retain higher value compared to petrol.


**Validation Method:**
These were validated using scatter plots, bar charts, pie charts, and KPI comparisons in Power BI.

## Project Plan
- **Step 1**: Understand the dataset and assign roles (Architect, Analyst, PM).
- **Step 2**: Clean the dataset (handle missing values, fix data types, derive new fields).
- **Step 3**: Load and model data using star schema in Power BI.
- **Step 4**: Build interactive visualisations tied to business questions.
- **Step 5**: Present findings with storytelling and dashboard walkthrough.

## The rationale to map the business requirements to the Data Visualisations

| Business Requirement                              | Visual Type         |
|---------------------------------------------------|---------------------|
| Average price by brand                            | Bar Chart           |
| Price distribution by fuel type                   | Stacked Column Chart|
| Relationship between price and price per cc by car company | Scatter Plot|
| Car powered by each Fuel type                     | Pie Chart           |
| Average price, horsepower, citympg, highwaympg    | KPI Cards           |
| Average of car length, height and width           | Line Chart        |

## Analysis techniques used

- **Data Preprocessing**: Handled data types and encodings using Pandas, numpy.
- **Visualization Tools**: Plotly, Seaborn, Matplotlib, Power BI and clean plots for insightful visuals.
- **Limitations**: The data that was given had information lacking on pre-existing time and date ranges.This impacted cost and market price.
- **Generative AI Usage**: Used to brainstorm visualization types, code refactoring, and interpret statistical results more effectively.

## Ethical considerations
- Dataset is publicly available and anonymised.
- No sensitive or personal user data is included.
- Bias could exist in sampling (used cars from a specific market), and results are interpreted with this in mind.

## Dashboard Design
We used PowerBI to build a dashboard. To review the dashboard, please download the .pbix file from the [# dashboard] folder and open it locally on your system.

**Main Dashboard Features:**
- KPI Cards (Avg price, Avg horsepower, Avg citympg, Avg highwaympg)
- Column Chart: Average Price by Brand
- Scatter Plot: Average of price vs Average of Price per cc by brand
- Pie Chart: Fuel type
- Line Chart: Average of price by engine size, curb weight and highwaympg
- Line Chart: Price by average of car length, width and height
- Interactive Slicers: Car company, car model and Fuel Type

The dashboard was designed to support both exploration and insight delivery for business stakeholders and data-savvy users.


## Unfixed Bugs
- Minor inconsistency in some brand naming (e.g., "VW" vs "Volkswagen")—standardisation could improve grouping.
- Some fields like `Mileage` or `Power` may still contain partially cleaned values (e.g., missing units or blanks).
- There are time and date related issues with the data provided as there were none given, so this impacted the data analysing and comparing. If they were there we could show the visual in a more efficient way regarding the market pricing and trends.

- Feedback from peers helped clarify insights and led to improvements in visual layout and story flow.

## Development Roadmap
- As a Project Manager(Ajay) one of the key challenges I faced was coordinating tasks and timelines among team members with varying technical skill levels; I overcame this by breaking down tasks into clear, manageable steps and using a shared project board to maintain transparency and accountability. Based on this experience, I plan to deepen my skills in using Trello and GitHub for collaborative project tracking, and learn more about dashboard storytelling techniques to improve future data presentations.

- As a Data Analyst(Payal) One of the main challenges I faced was working with GitHub in a group setting for the first time. Coordinating version control, managing branches, and resolving merge conflicts was initially quite challenging. However, I had practiced using GitHub before starting the project, which helped me understand the basic workflow. Throughout the project, we used clear communication, frequent commits, and consistent branch naming conventions to stay organized. Based on this project experience, I plan to deepen my knowledge of and GitHub and also interested in learning more about power BI tool.

- As the Data Architect(Nasra), one of the key challenges faced was handling inconsistent data formats and missing values, which required careful data cleaning and validation to ensure reliability. Another challenge was structuring the ETL process to balance automation and clarity while collaborating smoothly with teammates. Additionally, performing statistical hypothesis testing to validate dashboard insights required careful interpretation of p-values and assumptions. Based on this experience, learning advanced SQL and exploring data pipeline tools like Apache Airflow or DBT are top priorities to enhance future data architecture workflows.

- As the Data Architect (Milos), challenge I faced was applying advanced encoding and scaling techniques to prepare the dataset for analysis. I overcame this by carefully using One-Hot Encoding for categorical variables and StandardScaler for numerical features to ensure data consistency. Additionally, performing hypothesis testing required precise statistical understanding, which I managed by applying appropriate tests like t-tests and correlation analysis. Next, I plan to deepen my knowledge of feature engineering and predictive modeling.

## Main Data Analysis Libraries
- **Pandas** - For data manipulation.
- **Seaborn** - For statistical plotting.
- **Matplotlib** - For basic plot customization.
- **Plotly** - For interactive and dynamic visualizations.
- **Libraries** - used for hypothesis 
- **scipy.stats** - module provides a wide range of statistical functions. It was used here to perform hypothesis testing.
- **ttest_ind** - A function from scipy.stats that performs the independent two-sample t-test.
- **pearsonr** - Also from scipy.stats, this function calculates the Pearson correlation coefficient and its p-value to test for linear relationships
- **warnings warnings.filterwarnings("ignore"**) - A built-in Python module that manages warning messages during execution.
- **Power BI Desktop** – For data modelling and dashboard creation
- **Power Query** – For ETL tasks
- **DAX** – For basic measures (average, count, max)
- **ChatGPT (AI)** – For documentation, visual planning, and storytelling support

## Credits 
### 📘 Content
**Dataset Source:**
- The primary dataset used for this project is the Car Price Prediction Dataset sourced from Kaggle, published by hellbuoy.
The dataset was cleaned and pre-processed into a version titled cleaned_data_stage1.csv and stage_2_encoded_clean_dataset.csv

**Data Dictionary Reference:**
- A supplementary data dictionary file titled Data Dictionary - carprices.xlsx was used to understand and describe the fields accurately.

- Power BI Learning Resources
- Power BI Guided Learning
- YouTube tutorials for Power BI dashboard basics and slicer configuration

**ETL & Data Modelling Guidance:**

- **Assistance from Generative AI Tools:**
    - ChatGPT (by OpenAI)
    - Copilot 

- Guide project planning and milestone creation
- Suggest relevant visuals and their business interpretation
- Help structure this README.md and other documentation
- Provide design ideas and explanation for storytelling

**Peer Feedback & Mentorship:**
- Support and review provided by hackathon mentors and teammates during the 3-day event.
- Feedback during daily milestone stand-ups helped improve visual clarity and narrative flow.

### Media

🎨 Media
- Power BI Visuals and Icons:
All visuals used in the dashboard (cards, bar charts, pie charts, scatter plots, slicers, etc.) are native components within Microsoft Power BI Desktop.
- Color Palette and Themes:
- A modern business-themed color palette was applied from the built-in Power BI Theme Gallery.
- No external images were used. All dashboard design elements are Power BI native.


## Acknowledgements
- As Project Manager, I would like to extend my sincere thanks to the entire team for their outstanding collaboration on what was our first group data analytics project. Despite this being a new experience for all of us, the team quickly aligned on responsibilities and demonstrated a strong understanding of the project lifecycle—from ideation through to execution. Each member advanced confidently into their role with analytical thinking, clear communication, and a commitment to delivering high-quality outcomes.

- Throughout the project, we maintained consistent communication via group chats and coordinated live calls to address any challenges or errors as a team. This not only fostered problem-solving but also helped build a collaborative chemistry that strengthened our delivery. The use of Trello as our project board ensured transparency and task alignment, enabling us to stay on track both individually and collectively.

- We acknowledge the valuable contributions of every team member—from project management to data architecture, data analysis, and dashboard design. The team’s professionalism and willingness to support one another made it possible to meet all daily milestones and ultimately deliver a successful and insightful dashboard.