# Ripple-Summer-Project
Defined key metrics, built data, analysis, and ML pipelines, feature engineering, and dashboard engineering. Data was collected from blockchain nodes, containing information about customer quotes and payments. Focused on quotes... (Presentation Link)[https://drive.google.com/file/d/1iopuDiZqogBLO_4gM9QTY8PPuO8ndj48/view?usp=sharing]

This is my presentation from my summer at Ripple. I continued working there part-time for an extra semester as well. Below are some screenshots and short explanations of the presentation. A lot of information is blacked out in the pdf because of proprietary and confidential information...

# The issue

Data relating to quotes had been largely unexplored. Meaning all we had at the time was the raw data from the blockchain nodes. The company wanted to work on creating data and analysis pipelines for all funnels within the entire service process. My job was to lay the foundations and present initial findings. 

There are over a hundred million quotes, and millions of corresponding payments. We needed to engineer meaningful features, high-level dashboards for managers, and conduct EDA and further analysis to make any important suggestions.

# The solution

I built a data pipeline in Google Cloud Platform using Big Query. This was primarily done in SQL. This required aggregating data from dozens of sources, including collecting market maker information, Refinitiv FX rates, XRP information, customer info, etc... This pipeline can be easily accessed for ad-hoc queries, dashboards, ML models through AirFlow.


# Data Pipeline and Architecture
Quote to payment process:
* All payments must first start as a quote. The quote is an automated procedure that then requests confirmations from all involved parties and market makers. Quotes contain information about requested amounts, conversion rates, etc.

![image](https://user-images.githubusercontent.com/79114425/213817144-2f0a183d-c554-4f75-8d3a-6141f1f812a7.png)


ERD Diagram: Database architecture of pipelines used for analysis and dashboards

![image](https://user-images.githubusercontent.com/79114425/213817386-4d769c25-f79e-4c70-8d35-a504673d8e9d.png)

# Dashboards 
A butterfly graph giving some high-level views of the quote data

![image](https://user-images.githubusercontent.com/79114425/213817460-35479385-677c-4716-a8f5-53dfff373bc3.png)

Weekly quote performance for managers

![image](https://user-images.githubusercontent.com/79114425/213818176-dd786bfd-e62f-465c-886c-b4f3f9a8cd5f.png)

Created several different corridor analysis. The customer one is below

![image](https://user-images.githubusercontent.com/79114425/213818256-8b4a6a79-8d28-4561-b4bd-02fc9260b9d3.png)

# EDA

Time series analysis of quote batches

![image](https://user-images.githubusercontent.com/79114425/213818433-24a6e063-f3ec-44c1-ad72-ce2d5abc258b.png)

Quote volume correlation with crypto market. Annual and quarterly metrics

![image](https://user-images.githubusercontent.com/79114425/213818544-d1b338c2-fd37-4551-b1af-e57c1e04e74e.png)

Gave in-depth explanations of customer behaviors and the relevant suggestions

# LR model

Built a multi-linear regression model as an example of how to use pipeline for ML


