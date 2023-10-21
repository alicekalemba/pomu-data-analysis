# Pomucapital Data Analysis

## Project Introduction
This is the data analytics repository for the Pomucapital website 
(pomucapital.com). We can also help other micro-finance institutions to vet 
businesses, in this we can go ahead to help them grow their new clientile and 
if possible provide the data which we can use to project for their upfront 
performance.

## Description
This project provides scripts to generate mock customer data and their 
corresponding transaction data. It's especially useful for developers and 
testers who need to populate databases or systems with large amounts of 
realistic data for testing purposes.

### Dependencies and Virtual env
Python 3.x
`pandas` library
`csv` module

### Linux

Open the terminal and install virtual environment( With python3 there you can 
just use `venv` )

`pip install virtualenv`

Create Virtual Environment:

`$ virtualenv venvpomu` or `$ python3 -m venv venvpomu`

Activate Virtual environment:

> On Linux, any of these can work; 
 `$ source venvpomu/bin/activate` 
 or
 `$ . venvpomu/bin/activate`

> On Windows, use ;
`venvpomu\scripts\activate`

Install all application requirements from the requirements file found in the 
root folder

`$ pip install -r requirements.txt`

### How to run the project
1. Generate bulk customer data by running the `customer_data_generator.ipynb` 
script. The output will be saved to `customer_data.csv`.

2. Generate bulk transaction data realted to the above generated customers, 
by running the `transactions_data_generator.ipynb` and the output will be saved 
to `transactions_data.csv`.

3. Combine the customer data with the transactions data, clean it and encode 
it so that it's ready for clustering and machine learning modelling. 
Run `data_clean_and_encode.csv` to produce the `encoded_data.csv` file.

4. Run Cluster analysis to group data into clusters to help with marketing 
decisions. Run `cluster_analysis.ipynb`. Note. This creates clusters, but we 
have no yet exported them or related graphs to a report or wesbite. 
This will be worked on soon. 

5. Use the `encoded_data.csv` generated in part 3 to train an ML model to 
predict business Perfomance Index. Run `predictive_modelling.ipynb` to create a 
model.

6. Generate single customer data by running 
`single_customer_data_generator.ipynb`, followed by 
`single_customer_transactions_generator.ipynb` to create single 
customer and transactions data to generate `single_customer_data.csv` and 
`single_customer_transactions_data.csv` respectively.

7. Combine the single customer data and transactions data into a format which 
can be accepted as an input into the model generated in part 5. Run 
`new_customer_data_processing.ipynb` to create `new_customer_data_encoded.csv` 
to be used in the ML model. Note this is still in progress (POM-13).
 
Note: When pushing, avoid pushing newly generated csv files to keep Git diffs
low in PRs. Use the existing files unless there's new data you need added to them.
No need to run the generation scripts unless required.