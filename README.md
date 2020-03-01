# Apriori_Homework_CMI
## Project Group:
> Md.Sadil Khan(MDS201927)

> Prince Kumar(MDS201923)

## Output File:
>> kos_2_0.2.csv: Frequent 2-itemset generation of KOS dataset with min_sup=0.2

>> nips_3_0.5.csv: Frequent 3-itemset generation of NIPS dataset with min_sup=0.5

>> enron_3_0.02.csv: Frequent 3-itemset generation of ENRON dataset with min_sup=0.02

## Output-mis File:
>> MIS_KOS.csv: Frequent 2-itemset generation of KOS dataset with alpha=0.2,lmbda=3,phi=0.1

>> nips_3_0.5.csv: Frequent 3-itemset generation of NIPS dataset with min_sup=0.5

>> enron_3_0.02.csv: Frequent 3-itemset generation of ENRON dataset with min_sup=0.02



## The Task

The "Bag of Words" data set from the UCI Machine Learning Repository contains five text collections in the form of bags-of-words. The URL for the UCI repository is http://archive.ics.uci.edu/ml/datasets/Bag+of+Words.

Your task is to compute frequent itemsets for this data.

    First use the standard a priori algorithm with a fixed global value for minimum support. Try out different values for minimum support.

    Next, explore the multiple minimum support approach described in Section 2.4 of the book Web Data Mining by Bing Liu. See also Mining Association Rules with Multiple Minimum Supports, Liu et al, KDD 1999. You can assign minimum support values to words based on the frequency with which they occur across each text collection.

    For this part, skip the Enron email dataset and work only with the NIPS full papers and KOS blog entries datasets.
    
    
## Approach

#### Task 1
We at first created a function called DatasetGeneration which will return a dataframe with docid,wordid,count and words
and then we used pandas groupby function to generate transaction-style list of lists.
Then we used mlxtend library in python and created frequent k-itemset using apriori algorithm.

#### Task 2

We wrote the code of Multiple Minimum Support from scratch by using the algorithm presented in "Section 2.4 of the book Web Data Mining by Bing Liu". In the algorithm due to resource limitation we will consider those items whose supports are greater than alpha.
lmbda is a parmeter that takes a value between 0 and 1
phi is maximum support difference.














