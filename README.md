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
