### Predict Black Friday Sales
#### CSE 351 - Exercise 3 

-------------

### Contributor
- Wha Suk Lee
- Haein Park
- P.K.

-------------
### Tools
- KNIME 4.1.0

-------------
### Data
Variable  | Definition
------------- | -------------
User_ID | User ID
Product_ID|Product ID
Gender|Sex of User
Age|Age in bins
Occupation|Occupation (Masked)
City_Category|Category of the City (A,B,C)
Stay_In_Current_City_Years|Number of years stay in current city
Marital_Status|Marital Status
Product_Category_1|Product Category (Masked)
Product_Category_2|Product may belongs to other category also (Masked)
Product_Category_3|Product may belongs to other category also (Masked)
Purchase|Purchase Amount (Target Variable)
-------------
### Description

- ####Preprocessing
	- There are some missing values found in columns,
		- Stay_In_Current_City_Years
		- Product_Category_2
		- Product_Category_3

	- Two naive approaches are suggested to remove missing values in category columns
		1) Why not remove unnecesary categories?
		2) If any missing value is found, replace it with the uppercategory.

	- To remove missing values in "Stay_In_Current_City_Years" column
		- Replace missing values with zeros

- ####Node
	-	Column Filter
![](https://doc-0o-34-docs.googleusercontent.com/docs/securesc/3hbt226i21h0438kcut1eog5i4rv6ier/gcn980h222jeq1u1gdq54t535kvmv5pe/1587197850000/17647385581214940908/17647385581214940908/1WzVVI-C9aZpH5mvfMiJU1sBKs7Imsodo?authuser=0&nonce=622gbpung8k2u&user=17647385581214940908&hash=sd2edbtqi211rcflali1coadamd9se8u =50)
		Removes selected columns in the table.
		It is used to remove unnecesary category columns.

	-	Missing Value
![](https://doc-0o-34-docs.googleusercontent.com/docs/securesc/3hbt226i21h0438kcut1eog5i4rv6ier/i9v2co2e4s3sjukds63qc2dicuf2bpo6/1587198000000/17647385581214940908/17647385581214940908/1Zq9rl4S6CBNLPHt5K9DNA-KO29r5w-P9?authuser=0 =50)
		Using regular expressions or conditions, replace missing values with
		specific values.
		It is used to replace missing values with zeros in "Stay_In_Current_City_Years" column

	-	Rule Engine
![](https://doc-0k-34-docs.googleusercontent.com/docs/securesc/3hbt226i21h0438kcut1eog5i4rv6ier/2dskf4jrggue83qvk129bjrd3c7ci0r5/1587198000000/17647385581214940908/17647385581214940908/1Be01hUlDgRfpdziBiWxIbTWeN1hvt-Kv?authuser=0 =50)
		Use conditions to update specific attributes in a row.
		If any missing value is found in category columns, replace it with the upper category.
-------------
### Links
`<link>` : <https://datahack.analyticsvidhya.com/contest/black-friday/#ProblemStatement>

