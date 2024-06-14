# credit-card-fraud-detection

This is a small project I put together while I learn machine learning this summer.
The porject was originally done in Google Colab, and I acquired the data using a Kaggle
API key. For your convenience. I also uploaded the creditcard.csv data file that I 
used for this project, which contains a series of credit card transactions from European
cardholders in September 2013. Unfortunately, the data was incredibly unbalanced -- 
0.172% of all transactions were actually fraudlent, and this was reflected in the models'
performances.

# What I did

I trained a Logistic Regression to determine whether I transaction was a fraud or 
not a fraud. This process resulted in a precision of 0.73 and recall of 0.44 for the 
fraudulent transactions and a precision and recall of 1.00 for the regular transactions.

Next, I built a shallow neural network to see how it would perform as well. The neural
network had a precision of 0.46 and recall of 0.67 for the fraudulent transactions and a 
precision and recall of 1.00 for the regular transactions. So the neural network was a 
little better at identifying fraudulent activity, but it also flagged more regular transactions 
as being fraudulent, which could be annoying for a consumer if this model were actually 
being used in real life.

Finally, to see how much the unbalanced data was affecting the model performance. I created 
a new dataframe after shuffling the values where the number of fraudulent charges and 
real transactions were much closer in number. For this, the precision and recall for non-fradulent
transactions were 0.94 and 0.95 respectively, and the precision and recall for the fraudulent
transactions were 0.96 and 0.95 respectively. This showed how the shallow neural network
performed a lot better on a dataset that was a lot more balanced.