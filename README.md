This program developed with java for implementing N-gram laguage models, calculating probability- perplexity of sentences and generating sentences.
This program runs with a data set  (giving with txt format in arg[0]) and gives the output as a text file. (file named arg[1])
In the text class the data file is handled. First %60 giving as train set and the last 40% giving as test set. When creating a object from Text class, firstly the file is split into train and test part (using the sentence number in file in "calculateNumOfTrainSentences" method ) then this values kept in the object's attributes. 
We can create language models (unigram, bigram and trigram) with using handleTextforUnigram,handleTextforBigram,handleTextforTrigram methods in Text class. This methods creates a language model and keeps Hash maps for words/word pairs frequency in train set.

When we calling the handleTextFor(N)gram methods in Text class, the methods that in Ngram class which calculating probablity and perplexity of sentences in test set are authomatically called  for each language models. These results are written to the output file for each sentence and each language model.

Generation class is designed to generate sentences using information of models. When we call the  generateSentenceTri/Uni/Bi methods, this methods can generate sentences and calculates their probbility. These result are also written in output file under the title of "GENERATED SENTENCES".

When the program tested with small data set, it produces true results speedly. But it takes a lot of time when large data sets are used(more than an hour for  data set2 for this assignment/ this may be due to my computer).

Hazal Çağlan 21228161
