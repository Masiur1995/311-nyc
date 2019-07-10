Project 5  NYC Hackathon 4/29/19 DSI-7  
Brian Schor 
John Healy
Masiur Abik
Eric Kropf

# 311 Service Requests from 2010 to Present | NYC Open Data

   The NYC 311 DataSet compiles all calls to 311 from 2010 to present, and is updated daily. Our task is to examine the data and to imagine how 311 calls may change over time.The table lists complaint types, boroughs, zip codes and geographic data. The dataset is quite large and downloading as a csv is not feasible. The API key was provided by NYC Open Data and using the API key, 500,000 rows of data were pulled . Exploratory data analysis discovered many nulls which were deleted. Value counts by neighborhood and complaint types were investigated. Visualizations were created to understand the data better.The index was set to the created date column to filter the data by time as well. The column borough was mapped into numbers BROOKLYN: 1, MANHATTAN: 2, QUEENS: 3, BRONX: 4,STATEN ISLAND: 5 to use this feature for modeling. A pipeline was created for Count Vectorizer and Logistic Regression to use with the feature Complaint Type and target Borough Num. The purpose of the model is to predict the complaint types by borough.The model output was Best score of our model with gridsearched parameters: 0.3789371996146528
Ideal parameters: {'cvec__max_features': 2500, 'cvec__ngram_range': (1, 2), 'lr__penalty': 'l2'}
Score of our train model: 0.3797911546272353
Score of our test model: 0.3807411795787333
Groupbys were used to investigate relationships among the data as well. A table was created showing the most used and least used complaint types for each borough. 