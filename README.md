This program developed with java for to correct spelling errors by using Hidden Markov Models (HMMs).  
This program runs with a data set (giving with txt format in arg[0]) and gives the output as a text file(arg[1]). the dataset must has misspelled words and their correct forms which is given in this  format basically :
<ERR targ="correctForm"> misspelledWord </ERR>

Firstly we create an object from InputText class. It is our main object which represents the data that need to be handled. When inputText object created, the dataset text is handled in Ngram class and produce unigram, bigram models and list of misspelled words list in the text. Misspelled words are kept as an object of class MisspelledWord which has has raw and correct forms of the word. 
After handled all dataset, we are starting to try  to correct spelling errors. 
We use edit distance algorithm for detect possible alternatives of misspelled words in dataset which have edit distance "d=1" between that word. We kept that possible forms for all misspelled words in thats own object.

We use HMM class for calculating initial, transition and emission probabilities. For this calculating operations we benefit from datas which are kept in Ngram object of InputText object. In Viterbi class we firstly handle the dataset for obtain all possible forms of all sentences.  Then, we calculate the possibility of all possible sentence forms and choose only one which is the highest probability. At that point we kept all chosen sentences  in a list in Viterbi class and kept that which possible correct form is choosen instead of which misspelled word. 
And we calculate accuracy(num of correct found words/num of total misspelled words) for evaluate our result.
At the and we write on output text, all of the generated sentences and the accuracy value.

When the program tested with small data set, it produces true results speedly. But it takes a lot of time when large data sets are used (slow work is caused by my computer).

Hazal Çağlan 21228161
