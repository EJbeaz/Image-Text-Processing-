# Image-Text-Processing-
The following report composites the methodology and results of four image processing subtasks. 
The first subtask involved the retrieval and extraction of information in a CSV database, which contained 5006 movie reviews. 
Each review (‘text’ column) has an associated review ID, author, and score range (0.0-1.0) giving the dataset 4 attribute headers. 
From this dataset it was expected that 3 predefined movie titles (Star Wars, The Lion King and Starship Troopers) were to be extracted alongside the 
corresponding movie director from the ‘Text’ column and moreover an average score was to be calculated for each movie across its extracted reviews (IE task).
The reviews of each film were then to be split into two subcategories (IR task) which defined whether the text was an actual review of the movie (reviews) 
or just mentioned the movie (mentions). In order to evaluate the task, the ground data (see appendix 6.A.1) was provided as a comparative baseline allowing 
several performance metrics (Recall, Precision and F1 score) to be calculated to ascertain the efficiency of the implemented IR and IE systems.


The second subtask required a sentiment analysis of a subsequent CSV datafile that contained around 17,340 amazon reviews stored into 4 attribute
headers: the sentiment label, the review in text format, the wordcount of the review, and the review score. 
This subtask required the implementation of this sentiment analysis to classify the reviews into three sentiment labels (Negative, positive and neutral). 
The dataset was split into training (70%) and testing (30%) keeping balanced the distribution of labels in each set. 
Once the sentiment analyser had been created, the testing set was utilised in two different approach methods.
One utilised a convolutional neural network (CNN) and the other, a fully connected neural network (FCNN) to provide scoring metrics for the efficiency 
of the sentiment analyser and a visual representation, via confusion matrix. This allowed visual assessment of the predicted label vs Ground truth for both
approaches, as well as the performance metrics (F1, recall and precision) for further comparison.


The third subtask required two topic modelling approaches to be used to classify documents within a datafile folder into 7 topic 
labels (Accounts, Biology, Geography, History, Maths, Physics and Software). Much alike the second subtask, the dataset was again split into 70% training 
and 30% testing. Once the automatic topic labeller had been created, the testing set was again employed in two different approach methods. 
In this subtask one approach used Bag of Words (BoW) and ngrams as pre-processing methods and a support vector machine for analysis. 
The other utilised term frequency-inverse document frequency (TF-IDF) as a pre-processing technique a random forest classifier (RFC) to provide scoring metrics
for the efficiency of topic labeller and a visual representation, via confusion matrix. Once more, the confusion matrix permitted a visual evaluation of 
the predicted label vs Ground truth for both approaches, as well as the performance metrics (F1, recall and precision) for further comparison. 
In this subtask ‘Test Labels’ was representative of the ground truth.

The final subtask simply involved implementing a text-to-speech approach to the code in task 1 that summarises the information extracted for each movie.
This was formatted as per below:
“You have requested information about {xy film}, the directors of this movie are {' xy film's director}, there is a total of {no of reviews for xy film} 
reviews of this movie in the database, there are {no of mentions for xy film} mentions of this movie in other movies reviews. 
The average review score for this movie is {average score across all reviews for xy film },
which makes it a {good or bad- as defined by my own personal preference in my freetime = 0.6>} recommendation to watch.”
