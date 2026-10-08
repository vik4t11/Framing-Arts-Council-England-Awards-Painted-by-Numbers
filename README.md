# <u>**Framing Arts Council England Awards Painted by Numbers**</u>

*Framing Arts Council England Awards Painted by Numbers* unpacks visual insights from Arts Council England (ACE) National Lottery Project Grants awarded between 2023-2026. 

The purpose of this project is to demonstrate a full analytics workflow - Extract, Transform, Load (ETL), Exploratory Data Analysis (EDA), feature engineering, Machine Learning (ML), and dashboard storytelling to paint a bigger picture on cultural funding patterns across England, diciplines and fundign-streams. 

## <u>**Dataset**</u>

**Dataset used**: (1) National Lottery Project Grants - List of Awards in Year 2023-2024 and (2) National Lottery Project Grants - List of Awards in Year 2025-2026

**Source**: Arts Council – Project Grants Data

**Dataset link**: https://www.artscouncil.org.uk/ProjectGrants/project-grants-data

**Format**: EXCEL sheets exported as CSV files 

**Columns**: Recipient, Activity name, Award amount, Decision date, Decision month, Decision quarter, ACE Area, Local authority, Main discipline, Time-Limited Priority. 

Details for each column are included on the EXCEL cover page. 

## <u>**Disclaimer**</u>

*Framing Arts Council England Funds Painted by Numbers* is for educational purposes as part of the Code Institute Advanced Data Analytics, Visualisation and Machine Learning Summative Assessment 2. Thus, whilst this project aims to simulate a real world analysis it also integrates skills learned to complete the Data Analytics with AI Skills Diploma. 

## <u>**Business Requirements**</u>

To understand potential patterns, identify differences in distribution of awards and present actionable insights on National Lottery Project Grants for policy-makers, organisations and artists alike in the cultural sector a comprehensive technical analysis meets the business requirements below:

1. **Ethical and Compliant** - Data governance principles are considered from the start. Publicly available data dowloaded from the Arts England website is used. There is no record of unsuccessful applications. GDPR restricts success rates being calculated by excluding personal identifiable or financial information to comply with ACE publication policy. An additional anonymisation measure in the ETL notebook removes columns identifying reciptents names and project details to ensure ethical handling of data. 

2. **Descriptive Analysis** - the datasets are a record that tell what has happened in the past. Thus, this analysis is to observe where the money went and how much different diciplines received between 2023-2026. Stakeholders can access a dashboard to unpack selected visualisations from the EDA and ML Modeling notebooks. 

3. **Actionble Insights** - Analytical discoveries translate into practical prompts for decision making. Whilst, a machine learning model assumes to predict future outcomes, it is a tool to understand the past for humans to make decisions in the future. Identifying artforms receiving investment, regional differences, and trends in funding streams can inform strategic outreach efforts, organisations applying for grants and applicants effectively positioning their projects. 

## <u>**Project Plan**</u>

An end‑to‑end analytical workflow, moves from raw data to an insightful dashboard visualisation presenting discoverings during the EDA and a simple machine‑learning model engineered to identify funding patterns.

**Data collection** - Two public accessible ACE National Lottery Project Grants (2023-2024 and 2025-2026) datasets from the Arts Council website are loaded to complete this project. 

**Extract, Transform, Load (ETL)** - Ensuring data integrity prior to analysis includes standardising column names, inspecting and addressing missing, unique or duplicate records. Reviewing DataTypes ensures numerical, date-time and categorical columns are compatible for plotting in the EDA notebook. The final step is to join the two datasets with an additional year column followed by dropping columns containing potential sensitive information to ensure it is compliant with ethical data handling. The DataFrame will be saved into the clean data folder.  

**Exploratory Data Analysis (EDA)** - Patterns for award amounts are explored between ACE areas, main diciplines and funding streams using visuliation libraries - Pandas, NumPy Matplotlib and Seaborn - to plot boxplots, scatterplots, histograms and bar charts. 

**Feature engineering** - The clean joined DataFrame is engineered in the Feature Engineering notebook preperation for the ML Modeling notebook. A multiclass classification model requires award amount to be transformed into a funding tiers target column. Data leakage from columns which can impact the quality of the model are dropped and a model DataFrame file is saved. 

**Machine‑learning model** - A multi-class classification model is trained and tested to predict award amount tiers because the datasets feature mostly categorical and one numerical column. Feature importance is assessed following an accuracy evaluation to understand which attributes determine the target result.  

**Dashboard creation** - A Tableau dashboard frames visualisations and paints the numbers of year-on-year award amounts received between ACE areas, main diciplines and funding streams. Questions raised in the hypothesis are addressed in an accessible interactive storyline connecting the dots. The use of engineering a multi-class machine learning algorithm for stakeholders to identify patterns is also presented with details on model performance.   

## **Hypothesis**

The instinctual hypothesis motivating this project stems from a familiar question within the arts sector: is ACE awards fairly distributed across regions, artforms and funding‑streams? This assumption reflects anxieties many artists carry when navigating public funding systems.

The questions below will move between descriptive and diagnostic analysis to primarily help understand *why award amounts differ?*

1. *Are ACE National Lottery Project Grants unevenly distributed across geographic areas?* We expect to see certain ACE areas to consistently award higher amounts or a greater number of awards compared to other areas. To test this hypothesis award amounts are compared in a univariate and bivariate analysis in the EDA notebook. 

2. *Do certain main diciplines receive more or less funding than others?* Systemic differences in award amounts are visible between main diciplnes.  

3. *Can the size of award be predicted using categorical features?* Feature importance will reveal which attributes influence the ML Model prediction and thereby indicate structural patterns in award amounts.

## <u>**Analysis Techniques Used**</u>

**Statistical Overview** - Numeric statistics are reviewed to identify mean, mode, percentiles and identify anomilies in columns which may require further inspection to ensure data quality and improve model performance.  

**Univariate Analysis** - A histogram, boxplot and barcharts are used to visualise the distribution of awards across different numeric or categorical variables to determine whether National Lottery Project Grants vary between geographic areas and if certain main diciplines receive more or less funding. 

**Bivariate Analysis** - Award amounts are visualised to show how much different categories received. This anlysis technique clarifies what was the exact amount recipients received. 

**Outlier Inspection** - Anomolies identified in the statistical overview are inspected to ensure data quality and determine how they should be handled for the machine learning model.  

## Development Roadmap 

**ETL** intially data types are converted in the notebook. However, missing values identified at the beginning were not handled prior to converting categorical columns into category which meant the time-limited piority column failed to convert from its default string data type. Thus, I took a step back to ensure the values contained in the rows are cleaned. 

Data-time columns took a moment to adjust accordingly due to a misunderstanding with built-in Copilot on the task to modify code. Stack Overflow informed me on the difference between <code>normalize()</code> and <code>.dt.date</code> usage. 

## Credits 

**Extract, Transform and Load**

*Markdown for Jupyter Notebooks* https://www.ibm.com/docs/en/watson-studio-local/1.2.3?topic=notebooks-markdown-jupyter-cheatsheet

*Pandas Cheat Sheet* - https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf

*Standardise column names* - https://support.dataquest.io/en/articles/819-messy-column-names-here-s-how-to-fix-them-with-pandas

*Convert data types* - https://stackoverflow.com/questions/15891038/change-column-type-in-pandas

*Time-stamp removal from date-time column* - https://stackoverflow.com/questions/16176996/keep-only-date-part-when-using-pandas-to-datetime

*Research time-limited priority column* - https://www.artscouncil.org.uk/ProjectGrants/national-lottery-project-grants-guidance-library#t-in-page-nav-5

*Research multiple local authorities partnerships* https://www.artscouncil.org.uk/sites/default/files/2023-09/Place%20Partnership%20projects%20and%20Project%20Grants%20-%20Information%20sheet.pdf

*How to concat pandas DataFrame* - https://stackoverflow.com/questions/73100882/how-to-concat-pandas-dataframe

**Exploratory Data Analysis**

*Plotting charts using different libraries* https://lms.codeinstitute.net/learner_module/show/125519?lesson_id=537117&section_id=2067795

*Distribution of wealth in Great Britain* - https://www.ons.gov.uk/peoplepopulationandcommunity/personalandhouseholdfinances/incomeandwealth/bulletins/distributionofindividualtotalwealthbycharacteristicingreatbritain/april2018tomarch2020

*Indices of Deprivation in Birmingham* - https://cityobservatory.birmingham.gov.uk/pages/indices_of_deprivation_2025_in_birmingham/

*Biggest cities by population in UK* - https://www.ciphr.com/infographics/biggest-cities-in-the-uk-by-population

*Winsorization statistic technique to cap outliers* - https://amplitude.com/explore/experiment/data-winsorization

*Zero award amounts data quality check* - https://www.whatdotheyknow.com/request/discrepancies_3_ace_grants_for_t

*Model selection to conclude EDA* - https://www.geeksforgeeks.org/machine-learning/tree-based-machine-learning-algorithms/
