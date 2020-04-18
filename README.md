# Predict Black Friday Sales
In this exercise, you will solve a data challenge as a group project using the following approach: 	
1) Visit the data challenge page. 
2) Read carefully the problem to be solved. 
3) Download dataset. 
4) Figure out suitable approaches for solving the problem. 
5) Preprocess data for creating a dataset suitable for experimentation. 
6) Use your favorite data analysis tool to solve the problem. 
7) Report the approach taken, steps for using your favorite data analysis tool and your results in a PPT format and submit on Blackboard. 
8) Create a Github repository, upload your preprocessed data, steps for using your favorite data analysis tool and your results. Submit the Github link on blackboard.
## Contributor
- Wha Suk Lee
- Haein Park
- P.K.
## Tools
- KNIME 4.1.0
## Data
| Variable | Definition |
|--|--|
|User_ID |User ID|
|Product_ID|Product ID|
|Gender|Sex of User|
|Age|Age in bins|
|Occupation|Occupation (Masked)|
|City_Category|Category of the City (A,B,C)
|Stay_In_Current_City_Years|Number of years stay in current city
|Marital_Status|Marital Status
|Product_Category_1|Product Category (Masked)
|Product_Category_2|Product may belongs to other category also (Masked)
|Product_Category_3|Product may belongs to other category also (Masked)
|Purchase|Purchase Amount (Target Variable)
-------------

## Preprocessing
There are some missing values found in columns,
- Stay_In_Current_City_Years
- Product_Category_2
- Product_Category_3

Two naive approaches are suggested to remove missing values in category columns
1) Why not remove unnecessary categories?

2) If any missing value is found, replace it with the upper category.

To remove missing values in "Stay_In_Current_City_Years" column
	
1) Replace missing values with zeros

  
## Nodes

### Column Filter
![Column Filter](/assets/Column_filter.png)

Removes selected columns, such as Product_Category_ 2 and 3, in the table.

### Missing Value
![Column Filter](/assets/Missing_value.png)

Using regular expressions or conditions, replace missing values with specific values. It is used to replace missing values with zeros in "Stay_In_Current_City_Years" column

### Rule Engine
![Column Filter](/assets/Rule_engine.png)

Use conditions to update specific attributes in a row. If any missing value is found in category columns, replace it with the upper category. (For example, if Product_Category_2 has no value, replace it with the value of Product_Category_1)

### Links
`<URL>` : <https://datahack.analyticsvidhya.com/contest/black-friday/#ProblemStatement>
`<Course URL>` : <https://ppawar.github.io/Spring2020/CSE351-S20/Exercises/Exercise%203.pdf>
