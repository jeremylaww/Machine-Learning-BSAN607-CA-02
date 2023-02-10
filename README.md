# Machine-Learning-BSAN607-CA-02

## Spam Detector Using Naive Bayes Algorithm

Packages 
For this to work, the necessary python packages are as follows: os, Counter from collections, accuracy_score from sklearn.metrics, and GaussianNB from sklearn.naive_bayes.

Desription
This assignment is meant to take in a set of emails and figure out which emails are considered "Spam" using a Naive Bayes algorithm. The program first takes in a portion of the emails to train itself, and then uses the other portion of the emails to test itself. It does this by first creating a dictionary to store all the words in each email. Fro there it will loop over each file to extral all of the words within each email. Then it will create another dictionary that records the frequency of each word, then proceeeds to loop through each dictionaries to remove any words that are no alphabetical or that are only one letter. Finally this first function will return the most common 3000 words from the dictionary. The next function makes a features matrix out fot he emails and begins to label each emails as either spam (1) or not spam (0). 

Finally the training is done through model.fit(featuers_matrix, labels), the model is tested using model.predict(test_features_matrix) and the accuracy score is found after running accuracy_score(test_labels, label_predicted)

NOTE!!!!
This file was based off a template given from my professor. He made this template using a mac which makes the file pathing different a little different from a windows machine. As such, if you are using a mac, the "filepathTokens" must have only ONE "\" instead of two. Furthermore, the initial path to get to your documents are different as well. (take a look at examples at bottom)

Ex:  

     OS: filepathTokens = fil.split('/') 
         TRAIN_DIR = 'C:/Users/13235/Desktop/Machine Learning/train-mails'
         TEST_DIR = 'C:/Users/13235/Desktop/Machine Learning/test-mails'
         
     Windows: filepathTokens = fil.split('\\')
              TRAIN_DIR = 'Data/train-mails'
              TEST_DIR = 'Data/test-mails'
