# Data Cleaning: Stop-and-Search Incidents in England (December 2019 - February 2020)

***

# Motivation and goals

In my young career as a data scientist, I realised I hadn't published a project devoted solely to data cleaning. I believe that
this part of a data science project is underestimated and underrated. If done effectively, it can lead to significant gains in
model performance. Moreover, a large chunk of a professional data scientist's time is spent doing exactly this task. Hence, I
wanted to take multiple dirty datasets, find an interesting angle to explore and then clean the datasets to be ready for the 
next steps in a project's pipeline.

After a great deal of time spent searching for adequately interesting and dirty datasets, I found data on stop-and-search 
incidents that occurred in 7 different counties in England from December 2019 to February 2020. These incidents refer to instances
where police officers suspect civilians of carrying illegal substances and exercise their authority to search civilians. The 'end
goal' would be to predict the 'Outcome' variable, which illustrates the decision an officer makes after having conducted the search.

Upon exploring the datasets, I found around a fifth of the data to be missing. Some features contributed to this figure much 
more than others. For each feature, I:

- explored the quantity of data missing
- visualised the variable if needed
- hypothesised how important of a feature it could bein predicting the target variable
- used the above point to inform my decision as to how to handle the missing data

I used a combination of dropping observations, replacing missing values using 'back fill' and 'forward fill' plus using the Imputer
class to replace missing data with summary statistics, among other approaches. Most variables are categorical, but two critical
variables, Latitude and Longitude, were interval-level. Given their location-based nature, I used a combination of histograms, 
overlaying the Lat-Long values over a map of England and external coordinate data regarding the extreme points of human settlement
in England to find outliers and decided how to manage them.



There are three individual posts in this series in the form of Jupyter Notebooks:

Part 0: A bird's eye view of NLP in the context of Sentiment Analysis & Text Classification
Part 1: Tokenising and Pre-processing textual data
Part 2: Methods of text vectorisation, also known as feature representation

# How to run this project

- Download the Jupyter notebook
- Download the data files
- Download the map images
- Ensure you import all the required modules. The code for this is already present in the Notebooks
- Change paths to load the multiple datasets from your local machine. This can get tedious so I have included the final merged dataset also, so you can just load this instead
- Run the Jupyter notebook
