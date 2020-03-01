# Apriori_Homework_CMI
## Project Group:
> Md.Sadil Khan(MDS201927)

> Prince Kumar(MDS201923)

# Output File:
>> kos_2_0.2.csv: Frequent 2-itemset generation with min_sup=0.2










# The Task

The "Bag of Words" data set from the UCI Machine Learning Repository contains five text collections in the form of bags-of-words. The URL for the UCI repository is http://archive.ics.uci.edu/ml/datasets/Bag+of+Words.

Your task is to compute frequent itemsets for this data.

    First use the standard a priori algorithm with a fixed global value for minimum support. Try out different values for minimum support.

    Next, explore the multiple minimum support approach described in Section 2.4 of the book Web Data Mining by Bing Liu. See also Mining Association Rules with Multiple Minimum Supports, Liu et al, KDD 1999. You can assign minimum support values to words based on the frequency with which they occur across each text collection.

    For this part, skip the Enron email dataset and work only with the NIPS full papers and KOS blog entries datasets.
    
    
# The Data

In each of the text collections, each document is summarized as a bag (multiset) of words. The individual documents are identified by document IDs and the words are identified by word IDs.

After some cleaning up, in each collection the vocabulary of unique words has been truncated to only keep words that occurred more than ten times overall in that collection.

For each collection XYZ:

    vocab.XYZ.txt is the vocabulary file, listing all words that appear in the collection XYZ, one word per line. Each word has an implicit wordID that is its line number in this file, starting with 1 (the word on line 1 has wordID 1, the word on line 2 has wordID 2, ...)

    docword.XYZ.txt lists out the number of times each word in vocab.XYZ.txt occurs in each document (only non-zero counts are recorded).

    The file docword.XYZ.txt begins with 3 header lines

    	  D
    	  W
    	  NNZ
    	

    where D is the number of documents in the collection, W is the number of words whose frequency is counted (i.e., W is the number of words in vocab.XYZ.txt) and NNZ is the number of non-zero frequency entries for this collection (i.e., NNZ is 3 less than the number of lines in docword.XYZ.txt).

    This is followed by NNZ lines of the form

    	  docID wordID count
    	

    where count is the number of time the word with id wordID appears in document with id docID. Remember that only non-zero counts are recorded.

As usual, a K-itemset of words is a collection of words of size K that occur together in the same document. Your assignment is to write a program to find all K-itemsets of words occurring with minimum support F, where K, F and the name of the dataset to use should be parameters to your program.

The datasets are of different sizes. Report your results on the three smaller datasets (Enron emails, NIPS blog entries, KOS blog entries) for different values of K and F. In addition to the actual output, report the time it took to complete the job and, in case your program did not terminate for a given dataset and combination of K and F, report how long you tried before you gave up.
Information about the datasets in the repository

    Enron Emails:
    orig source: www.cs.cmu.edu/~enron

    	  D=39861
    	  W=28102
    	  N=6,400,000 (approx)
    	

    NIPS full papers:
    orig source: books.nips.cc

    	  D=1500
    	  W=12419
    	  N=1,900,000 (approx)
    	

    KOS blog entries:
    orig source: dailykos.com

    	  D=3430
    	  W=6906
    	  N=467714
