## The Science of Fashion Trends

<img width="816" alt="Screenshot 2024-07-29 at 4 04 13 PM" src="https://github.com/user-attachments/assets/f3de08d8-e4e9-47bf-9a9b-001d3e0a6578">

## What Was Our Objective?

While it is common knowloedge that fashion trends have **patterns in their cyclical nature** here we aim to study how they **propagate across different countries** and to identify underlying patterns.



## How Did We Approach This Project?

### **Methodology**:
#### 0. **Data Collection**:
  * We collected 200 datasets from google trends including 40 fashion brands from five critical fashion hubs: the US, UK, Italy, Australia, and France
  * *Why Google Trends?* --> Wealth of data generally accessible to public that is reliably consistent across countries and avoids focusing only on certain demographics 

#### 1. **Data Processing**: 
  * Used Python's **pandas** library for rigorous data cleaning and organization into detailed datasets
    
#### 2. **Data Smoothing**: 
  * To reduce noise and lessen the impact of short-term fluctuations in a dataset, we decided to smooth the data to make the underlying trends more visible.
  * We used a moving average to smooth the data, with a window size of 2
      * **Window Size:** *refers to the number of data points considered for each average calculation. We consider 2 (ie 2 weeks). The larger the window size, the smoother the data will be, but it may lose finer details*

#### 3. **Data Analysis**:
  * **Find delay with moving average**
      * We defined the following function to use when calculating the moving average
         <img width="464" alt="Screenshot 2024-07-29 at 3 55 29 PM" src="https://github.com/user-attachments/assets/4086dbee-80e5-4d5d-ab0e-f299cefc6e80">

      * *What does this mean?* See this is the delay of 4 weeks for the Armani Exchange trend in Spain from when it first started in the US  
        
         <img width="539" alt="Screenshot 2024-07-29 at 3 55 53 PM" src="https://github.com/user-attachments/assets/ce4e27ba-61fa-4ee6-9de9-249c5ab23948">

 #### 4. **Find delay matrix**
  * Function to find delay matrix for an x item
  * Note: the input is a list of the smoothed interests of all countries we want for that item x 
     <img width="872" alt="Screenshot 2024-07-29 at 3 33 47 PM" src="https://github.com/user-attachments/assets/e50b0802-3958-4d05-b42f-40fb8fa3ff11">


* *What would this mean for a specific trend?*
  * Here for instance there is a delay of -3 from US to Italy. This means that the US is on average 3 days ahead for the UGG trend.
    
       <img width="463" alt="Screenshot 2024-07-29 at 3 42 12 PM" src="https://github.com/user-attachments/assets/aaf5f3a6-7983-43ee-be52-915c1513a48e">
       
#### 5. **Average the delay matrices**
* To find the average delay of each country we make an average of all delays for all countries
  
  <img width="345" alt="Screenshot 2024-07-29 at 3 50 07 PM" src="https://github.com/user-attachments/assets/d874cd6d-a54a-4cac-9839-ee60bf35e8b4">


  #### 6. **Visualization**: 
   * We created heatmaps using **Matplotlib and Geopandas** to effectively illustrate the variation in trend adoption times across countries.
      <img width="603" alt="Screenshot 2024-07-29 at 4 02 13 PM" src="https://github.com/user-attachments/assets/8890615b-c6c8-48b3-8e4e-9cf6712034cd">


## What Did We Discover?

Our analysis shows that contrary to intuition, for mainstream trends (such as adidas Gazelle) **the United States and Australia typically lead,** with European countries like Italy and the UK following them. 
This may be because the main trends we analyzed were from items sold worldwide which likely started to produce in the US. Naturally, if some items were famous and exclusively sold in Italy for instance, we would have excluded the item from the study.

## How is this relevant for fashion brands and trend followers?

This project offers strategic insights for fashion brands and marketers, suggesting a focused approach in areas that quickly embrace new trends. We recommend amplifying marketing efforts in the US and Australia due to their leading roles in trendsetting.


## What Challenges Did We Encounter?

**Challenges**:
- **Data Collection**: Navigated significant hurdles due to the restrictions on scraping Google Trends and the complex integration of multiple datasets.
- **Data Compatibility**: Encountered and resolved issues with code compatibility and data representation, choosing heatmaps as the most effective method to summarize our findings.

## How Can This Project Be Improved?

Future enhancements could include the development of an interactive dashboard that allows real-time trend mapping and the integration of predictive algorithms to forecast the directions of future fashion trends.




