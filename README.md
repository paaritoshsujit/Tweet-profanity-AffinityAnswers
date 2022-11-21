# Tweet-profanity-AffinityAnswers

This project aims to detect the degree of profanity of each sentence read from a file of tweets sent by users. They are judged as profane or not based on the number of matches found based on a pre-decided and pre-existing set of racial slurs.

Here we have used two variables which are important to distinguis from one another:

profanity_count -> it is a set of values which denotes the number of profanities found in each sentence.
profanity_degree -> based on the number of profanities found, we assign a fuzzy linguistic value along with its hedge to depict how profane the sentence is.


The program can be further expanded to count for different word formations of the same racial slurs (which would bring us to stemming, lemmatization etc.).
