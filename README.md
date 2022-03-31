# __Fraud detection__
# Overview
This project is focused on detecting fraudulent transactions via the Ugandan mobile payment company Xente. Every 500th Xente transaction is fraudulent, which makes up 1/3 rd of the total transaction volume, 300M UGX. This means that Xente is heavily used for criminal transactions, puts Xente's valued customers at risk of fraud and strongly damages the reputation of Xente. So an automatic fraud detection algorithm is really important to prevent these criminal transactions and hence to protect Xente's customers. <br>
For this algorithm to work properly, Machine Learning is needed in order to accurately detect fraudulent transactions instead of falsely accusing valued customers.     

Fraud Detection:<br>
Value of Product:<br>
This project is focused on detecting fraudulent transactions via the Ugandan mobile payment company Xente. Every 500th Xente transaction is fraudulent, which makes up 1/3 rd of the total transaction volume, 300M UGX. This means that Xente is heavily used for criminal transactions, puts Xente's valued customers at risk of fraud and strongly damages the reputation of Xente. So an automatic fraud detection algorithm is really important to prevent these criminal transactions and hence to protect Xente's customers. <br>
For this algorithm to work properly, Machine Learning is needed in order to accurately detect fraudulent transactions instead of falsely accusing valued customers. <br>
Prediction:<br>
Transaction is fraudulent <br>
Evaluation Metric:
f1-score <br>
Its very important to accurately detect frauds and not to accuse innocent people while still detecting the majority of fraudulent transactions
Baseline Model:<br>
Transaction is fraudulent
- if transaction is used for financial services
- if money is spent rather than deposited
- if the value of transaction exceeds 200K UGX
- if transaction happened through a provider 1, 3 and 5
- if transaction happened for a specific product category (15)
- if transaction happened through a specific channel (3)
- if the customer account is subscribed to a certain pricing policy (0 and 2)<br>

Score:<br>
f1-score = 0.55

# ds-modeling-pipeline
Skeleton project for building a simple model in python script
This is the simplest way to do it. We train a simple model in the jupyter notebook, where we select only some features and do minimal cleaning. The output is then stored in simple python scripts.

Data used is the  [coffee quality dataset](https://github.com/jldbc/coffee-quality-database).

##
Requirements:
- pyenv with Python: 3.9.4

### Environment

Same procedure as last time...

Use the requirements file in this repo to create a new environment.

```BASH
make setup 

#or 

pyenv local 3.9.4
python -m venv .venv
pip install --upgrade pip
pip install -r requirements.txt
```

If You encounter errors related to statsmodels, try:

```BASH
OPENBLAS="$(brew --prefix openblas)" pip install numpy statsmodels
```

## Usage

In order to train the model and store test data in the data folder and the model in models run:

```bash
#activate env
source .venv/bin/activate

python train.py  
```

In order to test that predict works on a test set you created run:

```bash
python predict.py models/linear_regression_model.sav data/X_test.csv data/y_test.csv
```

## Limitations

development libraries are part of the production environment, normally these would be separate as the production code should be as slim as possible
