# Deduplication using simhash.

What is represented here is a simplish code that demonstrates the concept of feature extraction and how near duplication is represented in the simhashed scores. 

One seminal source which brings together everything is [Detecting
Near-Duplicates for Web Crawling](http://www.wwwconference.org/www2007/papers/paper215.pdf) by Manku et al.

This code includes another [project](https://github.com/leonsim/simhash) which implements the simhashing algorithm as described in the Manku paper. 


## Requirements
To use the code you'd need:
* Nltk
* Simhash from the above [project](https://github.com/leonsim/simhash).
* It's written in python. So preferebly run it on Linux.

## To use it
* Place whatever text files you want in the corpus directory. All of them will be read and each one will be mapped against the other to show the similarity score.
* The file to run is **hashtest.py**.
* The result table will pop up in **results.csv**. 
* To intepret the results. Values that are closer to 0 shows that the two files are similar, and further apart indicates differences.

## Inferences
* Removing stopwords and stemming give better results of differences. 
* When trying to hash on the n-gram or shingles, the results become stricter and even small changes are given high differences.


