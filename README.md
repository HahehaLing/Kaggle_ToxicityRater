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
Try transfer learning on transformer-trained BERT sentiment models. 

# Authors
Eric (Yue) Ling

# Acknowledgments
Jason Trinh for code review and tips about speeding up the search. 
Natalie Ahn for giving tips about training the models and different methods of data transformation, data cleaning tips using regex. 

