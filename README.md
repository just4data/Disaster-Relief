# Disaster Response Message Classification Pipelines

This repo analyses disaster data from [Figure Eight](https://www.figure-eight.com), a company specialising in data analytics and machine learning, to build a model for an API that classifies disaster messages. The goal is to direct each message to the relief agency that can provide the quickest assistance.

# File Description:

__disaster_messages.csv:__ dataset including all the messages<br>
__disaster_categories.csv:__ dataset including all the categories<br>
__disaster_response_pipeline.ipynb:__ contains ETL & ML pipeline scripts<br>
__cleaned_dataset.db:__ output of the ETL pipeline, SQLite database containing messages and categories data<br>

# Analysis:

__ETL pipeline:__
- Modify the Category csv; split each category into a separate column
- Merge Data from the two csv files (messages.csv & categories.csv)
- Remove duplicates and any non-categorized valued
- Create SQL database DisasterResponse.db for the merged data sets

__Text Preprocessing:__
- Tokenize text
- remove special characters
- remove stop words


__Machine Learning Pipeline:__
- Build Pipeline with countevectorizer and tfidtransformer
- Seal pipeline with multioutput classifier with random forest
- Train Pipeline (with Train/Test Split)
- Print classification reports and accuracy scores
