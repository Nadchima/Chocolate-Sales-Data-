# 📊Data Analysis Report: Chocolate Sales Data🍫
# 1. Objective
    The objective of this report is to analyze the sales performance of various chocolate products to uncover key trends, customer behavior, and sales drivers. The findings aim to support decision-making in marketing, product development, and inventory management.

# 2. Data Overview
    The dataset contains records of chocolate sales, including:
    - Product Categories (e.g., Dark Chocolate, Milk Chocolate, White Chocolate)
    - Sales by Country and Region
    - Unit Prices, Quantities Sold, and Revenue
    
# 3. Key Visualizations & Findings
**💻Comparison of export countries:** 
    Australia, Canada, India, New Zealand, USA, United Kingdom

**🔝Top 5 best-selling products:** 
    Smooth Silky Salty, White Chocolate, Peanut Butter Cubes, Spicy Special Slims, Raspberry Chocolate

**🎯Seasonal trend:**
    Sales peak in January and June, Sales decline in February

**📆Monthly Trand By Product:**
    Comparison of each product's sales on a monthly basis.

# 4. Insights
**📢Promotions during festive seasons effectively boost sales:**
    Running promotions during festivals such as Valentine’s Day and Christmas significantly helps increase sales. This reflects consumer behavior trends, where customers tend to purchase gifts or snacks during special occasions.

**📈Countries with low sales:**
    It was found that New Zealand and Canada consistently have lower sales compared to other export markets. It is recommended to consider appropriate marketing strategies, such as country-specific promotional campaigns or researching local consumer needs to enhance growth opportunities.



# 5. Exploratory Data Analysis (EDA) in Google Colab
**1. Import Libraries**
    
    import pandas as pd
    
**2. Load the Dataset**
    
    df = pd.read_csv("/content/Chocolate Sales.csv")
    print(df.head())
    
**3. Basic Info & Summary**

    print(df.info())
    print(df.describe())
    print(df.isnull().sum())
    df.duplicated().sum()
    
**4. Data Relationship**
    import matplotlib.pyplot as plt
    import seaborn as sns

    # Histogram
    
    df['Product'].hist()
    
![image](https://github.com/user-attachments/assets/24e64cae-3887-4600-8b2d-390dabb27ca6)

    sns.boxplot(x=df['Product'])
    
![image](https://github.com/user-attachments/assets/27eb2cd5-9397-4d7e-b1d8-ae9af1d973ed)

    sns.countplot(x='Product', data=df)
    plt.title('Amount')
    plt.show()
    
![image](https://github.com/user-attachments/assets/9263a21e-f1bc-4cea-b316-f8d4739c3c83)

    sns.histplot(df['Product'])
    plt.show()

![image](https://github.com/user-attachments/assets/72cbdd48-210a-47a8-bbab-2d0873897943)

**5. Data Export**

    df.to_csv('Chocolate Sales Data.csv', index=False)

# 6. Data Analysis Process in Power BI

**Data Import:**
    
    Import data from Excel or other data sources into Power BI to start the analysis.
      
**Data Cleaning:**
    
    In this project, data cleaning was minimal as the imported data was already structured and clean. There were no duplicate records, and missing values were either not present or irrelevant to the analysis. Therefore, no major transformations were performed in the Power Query Editor.
      
**Data Modeling:**

    Link tables and create Measures/Columns using DAX for analytical calculations.

**Example:** 

    Month Name = FORMAT('Chocolate Sales Data'[Date], "MMMM")

    Unit Price = 'Chocolate Sales Data'[Amount] / 'Chocolate Sales Data'[Boxes Shipped]
    
**Visualization:**
    
    Create interactive charts and dashboards such as Bar Charts, Pie Charts, and Slicers to display the results.
    
![image](https://github.com/user-attachments/assets/f7804de8-25df-4953-943e-484018503eef)

![image](https://github.com/user-attachments/assets/ef564608-7054-4300-b6ad-c3cc2fb9328d)







