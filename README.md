**1.	Data Overview**
-	The data set is titled “Supermarket Sale”. This contains information about supermarket sales transaction, which focus on the behavior of customers across different brand names and product categories. It is valuable for analyzing sales performance, customer preferences, and revenue trends.
-	It contains 254 rows and 8 columns: Sale ID, Branch, City, Customer Type, Product Name, Product Category, Quantity, and Total Price.

 	**•	Sale ID** represents the unique identifier assigned to each transaction in the dataset. Data type is number.

 	**•	Branch** indicates the brand name of the supermarket where the sale took place (A and B) in the dataset. Data type is text.

 	**•	City** shows the location (city) of the supermarket, including Chicago, New York, and Los Angeles. Data type is text.

 	**•	Customer Type** specifies the classification of customers, such as member and normal (non-member). Data type is text.

 	**•	Product Name** lists the name of each product sold. Data type is text.

 	**•	Product Category** identifies a group of products purchased. Data type is text.

 	**•	Quantity** indicates the number of units sold in every transaction. Data type is number.
 	
 	**•	Total Price** shows the total sales amount for each transaction. Data type is number.

  <img width="944" height="387" alt="image" src="https://github.com/user-attachments/assets/e5f35e50-3298-46fc-bc8e-0cd0e1c41f3a" /> 
  
                           Figure 1 Data set of supermarket sales 
- Although the source of the dataset is not mentioned, it is presumed to be from retail transaction systems or open-access datasets. These sources commonly offer retail transaction data suitable for academic research, market analysis, and decision–making process.
This dataset helps understand customer purchasing behavior, assess the sales trend, and evaluating product performance across different supermarket branches and cities. 

**2.	Data Cleaning**

*Missing value* 
<img width="944" height="133" alt="image" src="https://github.com/user-attachments/assets/cd9860bf-d690-4d7a-a6b0-623c52fb8306" />
                          
                           Figure 2 Missing value of column D

- The missing value in column D (Customer Type) at rows 34, 38, and 48. They are missing the customer type. 

 <img width="257" height="110" alt="image" src="https://github.com/user-attachments/assets/3eb95fa7-7c01-4bd0-8280-04359704442c" />

Figure 3 Tendency of Member and Normal 

<img width="948" height="120" alt="image" src="https://github.com/user-attachments/assets/7ba6ef12-4a76-40ae-8062-3bbab627f43c" />
                           
                           Figure 4 Handling missing value of column D
                           
-	With the attribute of data, I filled the value using the most frequent value (imputation). Member appeared 131 times, so I filled Member for the missing value in column D, minimizing data loss.

<img width="949" height="209" alt="image" src="https://github.com/user-attachments/assets/270d69d6-19fb-4627-81ac-51121e1290a5" />
                             
                             Figure 5 Missing value of column F
- The missing value in the column F (Product Category) at rows 33, 35 , 53, 72, 91 and 103.

<img width="956" height="148" alt="image" src="https://github.com/user-attachments/assets/7b8a79ba-eee8-422d-af8d-a6ea090eb644" />
                          
                          Figure 6 Pivot Table of column F

-	For the Product category column, missing data were handled using a PivotTable analysis. It helps to count how many times each product name appeared under different categories. The category that appeared most frequently for the same product name was selected and filled in. For Orange Juice, it most commonly appeared under the Household category. Since Detergent appeared under the Household category, and Shampoo was appeared under Fruit category.

<img width="949" height="124" alt="image" src="https://github.com/user-attachments/assets/796a504f-8aac-4246-b16c-ba9543baf678" />
                          
                          Figure 7 Missing value of column G

- The Missing value in column G (Quantity) at rows 22,48, and 65. 

<img width="961" height="148" alt="image" src="https://github.com/user-attachments/assets/2cc2a771-915a-4f7f-b0f1-81021dc3b2a9" />
                          
                          Figure 8 Handling missing value of column G
-	Addressing this issue, the mean (average) value of the quantity of product “Detergent” (11) was used to replace the missing entries. Selecting the mean, which provides a balanced estimate that shows the central tendency of the data, minimizes the effect of fluctuations in sales volume without distorting overall sales patterns.

-	The median was not selected because it is suitable for skewed or highly variable data distributions. For this dataset, the quantity value spreads within a narrow range.

*Duplicate Rows*

<img width="949" height="199" alt="image" src="https://github.com/user-attachments/assets/4f3b3330-44ae-431f-a003-199b8d4e125e" />
                          
                          Figure 9 Duplicate value from sort and filter

<img width="895" height="324" alt="image" src="https://github.com/user-attachments/assets/5102fcec-9a7d-4723-b3ea-0632e20c02d5" />
                          
                          Figure 10 Remove duplicate value

Duplicate values: 3 

- Choose Data --> Select all data sets --> Click on Remove Duplicates.

- Since each record in the dataset indicates a unique sales transaction, keeping duplicates can cause inflated totals for sales revenue and quantity. When removing duplicates, it ensures each sale was counted only once and the results remain correct.

**3.	Descriptive Statistics**

<img width="803" height="514" alt="image" src="https://github.com/user-attachments/assets/e4752eb0-ac48-4cc1-85be-c431b0c60057" />

***Key Insight 1:Total of Quantity Sold by Branch and City***

<img width="792" height="464" alt="image" src="https://github.com/user-attachments/assets/a321959d-7803-4c83-82cb-f91c3bc1c25e" />
                        
                         Figure 11 Total quantity sold by branch and city
                         
This shows that Branch A recorded the highest number of products sold, showing strong customer demand and higher transactions in that branch. It also demonstrated New York experienced the highest quantity sold.  Brand B had the lower quantity sold.

This insight highlights potential differences in each branch and store performance and customer behavior across cities. The supermarket could manage inventory and give a promotional plan for future sales.

***Key Insight 2: Distribution of Total Sales per Transaction***

<img width="880" height="478" alt="image" src="https://github.com/user-attachments/assets/ae4969e4-6fd0-402d-b007-183e1a1b6d09" />
                        
                        Figure 12 Distribution of total prices
                        
The histogram shows that most transactions fall between $50 and $150, confirming that customers generally make moderate purchases. A few transactions exceed $400, which represent outliers or high-value purchases, consistent with the positive skewness observed in the data.

Overall, this distribution indicates spending patterns in supermarkets, where small to medium purchases dominate daily transactions, with only a small proportion of large transactions.
                            
