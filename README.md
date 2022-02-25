# Comment Toxic-Severity Rater

## Background
Conventional toxicity comment rater Kaggle competitions focus on correctly classifying toxic comments. This Jigsaw competition focuses equally on correctly identifying the comments' vulgar/ benign levels. For example, on a scale of 0 to 1 with 0 being completely benign, 1 being extremely vulgar, and 0.5 for neutral comment. Correctly rating a comment as 0.2 is just as important as identifying a 1 for an extremely profane comment. 

* https://www.kaggle.com/c/jigsaw-toxic-severity-rating/overview/description

## Data Format
The data provided by Jigsaw is rated by a number of judges on a pair of 2 comments. The judges rate which of the two comments are more toxic. This pair of comment rating ensures a higher level of comformity in the judges' rating. Otherwise, every judge may have their own bar of toxicity and the labeling scale would not be uniform. For example, one judge may rate the same comment as a 0.3, while another judge may view the same comment as a 0.5. With a pair of 2 comments, it would be easier to differentiate which comment is more toxic when 1 is obviously more vulgar than the other. 

# Getting Started
Notebook bow_biranktrain.ipynb contains the model trained on the pair of comments provided in the Jigsaw dataset. The accuracy on the reserved test data is 79%. 

# Prerequisites
Pip dependencies in the requirements.txt file.

    pip3 install -r requirements.txt 
    
# Future work 
Try transfer learning on pre-trained, transformer-based BERT sentiment models. The higher performance models in articles and latest NLP research are BERT models, because they can be trained on much bigger datasets (with parallelization) on a shorter time than LSTM could. LSTM, with its recurrent architecture, is also limited in the number of preceeding word it can remember, whereas the attention-emphasis and feedforward architecture of transformers have locational and embeddings allowing for context representations of the text without losing overall information as a result of "too distanted" preceeding words. Training on my own models (LSTM, XGB, SVM, Random Forest...etc.) are also limited by the small amount of data so fine-tuning my data on pre-trained sentiment models may drastically increase the overall accuracy significantly. 

## Hyperparameter tuning
   * random selection 

# Authors
Eric (Yue) Ling

# Acknowledgments
Josh Baltar, Henry Apfel, Yagnik Vadher, and Jason Trinh for code review, brainstorming session, and tips about speeding up the search. 

Natalie Ahn for giving tips about training the models, different methods of data transformation, hyperparaemter tuning, and data cleaning tips using regex. 

