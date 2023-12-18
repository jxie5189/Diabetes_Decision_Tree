# Diabetes_Decision_Tree

A decision tree  assignment from Machine Learning Class using sklearn

Dataset: https://www.kaggle.com/datasets/nanditapore/healthcare-diabetes

Original code from Google colab, the code assumes that the dataset is already in the google drive. The notebook makes a connection to the google drive and extracts the dataset. The dataset is read via pandas and a correlation map is displayed. The label is changed to to Diabetes for 1 and No Diabetes for 0 in the 'Outcome' column. 

The Training/Testing is done via train_test_split on only [Glucose, BMI, Age] features. Test size of 20% with random state of 45. Total Training sample is 2214. The decision tree (DT) is made via sklearn with 'entropy' as it's criterion and sets random state 45. 

A grid search is made to obtained with various depth and accuracy as it's metrics. The results are compiled into a dataframe and plotted. For simplicity sake, a depth of 4 was choosen for the model with an accuracy of ~77.6% with the training data. (no validation set was carried out in this demo) 

To graph the DT, I use export_graphviz from sklearn(input model, outfile name, feature names, label names). 

# Application 

I created 2 class for this demo, model and entry. The model class basically takes the entry object and passes into our DT model that was already established (might have to incorprate the actual DT into our model). The entry class encapsulates the features/inputs (Glucose, BMI, Age). 

# Misc. 
The rest of the code are basic data exploration (changing the BMI for all samples vs. only for diabetic samples) 

