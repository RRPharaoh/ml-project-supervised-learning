# machine_learning_project-supervised-learning

## Project/Goals
The objective of the project is to utilize supervised learning techniques to build a machine learning model that can predict whether a patient has diabetes or not, utilizing key diagnostic measurements. 
The ultimate goal of the project is to gain insights from the data sets and communicate these insights to stakeholders using appropriate visualizations and metrics to make informed decisions based on the business questions asked
##Process

### 1st Step: data analysis
The first step of this project was to access and explore a dataset comprised of patients with key metrics. I started by analyzing the data utilizing the EDA process. I began by looking at key metrics within the descriptive statistics and checking the data frame for completion. I noticed that although there were no null value within the dataset, there was a large number of zero values that skewed the data. Before altering the data, I decided to investigate further with pair plots and investigating the significance of each column.
**Key takeaways**
- There are a total of 768 entries, with 0 null values in each column
- However, there a number of zero values within columns that normally should not have any, therefore these could be considered missing values
- Average age of individuals in the dataset is 33.2
- Average age of individuals with diabetes is 37, without is 31
- Average BMI of individuals with diabetes is 35, without is 30
- average glucose levels of individuals within the dataset with diabetes is 141, without is 109
It seems that individuals who have diabetes are more likely to have a higher level of BMI, Glucose, Blood pressure and insulin.
Highest correlation is seen between:
- Glucose and outcome 
- insulin and Skin Thickness 
- insulin and Glucose

### Step 2 : Data Preprocessing
The step involved addressing outliers, normalizing the data and handling the zero values.
There were 3 columns with relatively small  amounts of zero values, so the rows containing the values were removed from the dataset. 
I decided to further analyze the Insulin and Skin thickness columns since they both had zero values within the triple digits. With consideration to the dataset, and after reviewing the plairplot, violin plots and overall impact on the data, I determined that both columns were to important to outright remove. Considering that both were heavily correlated with each other and exhibited and positive correlation.
I also noticed that they both shared a uniqueness in the dataset, as they both had similar zero values per patient. So, by eliminating the entries that had zero values of Insulin (the metric with the most zero values) I effectively eliminated all remaining zero values from the dataset.  Once the dataset was normalized, I then opted remove the pregnancies column entirely as it proved inconsequential to the dataset. 
### Step 3 Training model implementation
The first model I implemented was a multiple Regression Model after utilizing a standard scaler to normalize the values within the dataset. I then followed with a random forest classifier.

### Results
Both models had an accuracy at about 79% which indicates consistency with predictiion,
to be fair, it 
