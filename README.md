# Email-Classifier-Spam-Ham-
Machine Learning for Classify a text is of " Spam " or " non Spam " type.
Multinomial naiv bayes classifier is used.

directory containing of 2 files classifier_accuracy ans runtime_filter.
classifier_accuracy.py sonsist of some basic functions for following use

1. keep(clfr,name) - Using cPickle, we dump compressed version of our computed classifier settings into a file, So that for any further process we do not need to recreate the dataset and we can directly use the results.

2. make_dictionary() - we iterate through each email (raw data) in directory superset_email, and read them followed by appending each word in a list by splitting them in space and change in line, we will remove non alphanumeric terms from dictionary as they are irrelevant to our method (can't conclude anything), and we will choose 3000 most common words to make final dictionary consisting word and frequency, we will use most_common function for same.

3. make_dataset(dictionary) - we start by iterating over all the raw email files, now for each emails we run on dictionary and for word at index i we store each word's frequency in a list, same for all emails.
followed by appending all the lists to a list of lists name features. maintaining a label list containing values 0 and 1 respectively, for non spam and spam emails.

train_test_split from sklearn is used to split the data into two parts, one for training naiv bayes model and other one to evaluate the accuracy keeping test_size = 0.2 (can be changed), followed by fitting the train data into multinomialNB() and testing them using function accuracy_score.






