# Verb Transitivity

This repo contains data on verb transitivity in English and script to extract transitivity information from Google's syntactic ngrams corpus.

For a recent project, I needed transitivity information for English verbs: For each verb what percentage of the time was it intransitive, transitive and ditransitive? After much unfruitful online searching I generated the data myself, using the Google Syntactic NGram corpus. The data and extraction script are available in this repo. 

### verb_transitivity.tsv
This file contains extracted transitivity information for all verb forms that occur more than 2,000 times in the [Google Syntactic NGrams "English 1 Million" Corpus](http://commondatastorage.googleapis.com/books/syntactic-ngrams/index.html) (7965 verb forms total) Verbs are not lemmaized, thus "give" "gives" and "gave" all appear in the top-10 most common ditransitive verbs. In some cases, verbs were recorded as occurring with indirect but no direct object. I marked these cases as cross-transitive ("xtrans" in the .tsv file).

There are 10 verb forms that always occur intransitively. They are:
Verb | Percent Transitive
targeted | 1.00
mineralized | 1.00
circumstanced | 1.00
atrophied | 1.00
dehydrated | 1.00
truncated | 1.00
televised | 1.00
synchronized | 1.00
interrelated | 1.00
succumbed | 1.00
is | 0.999941

The Top-10 Most transitive verb forms are:
Verb | Percent Transitive
murder | 0.977389
access | 0.976555
avenge | 0.975976
reminds | 0.975470	
defray | 0.971862
frequent | 0.968574
extricating | 0.966914
extricate | 0.965874
undecieve | 0.965505
garrison | 0.964685

The Top-10 Most ditransitive verb forms are:
Verb | Percent Ditransitive
give | 0.319187
gave | 0.315119
cost | 0.230948
handling | 0.218010
gives | 0.194149
lend | 0.185281
giving | 0.175866
shewed | 0.122527
handed | 0.116729
grant | 0.110312


### arg_structure_extractor.py
This file is a python script for extracting the verb transitivity information from the Google Syntactic NGram Corpus. To run it, place the files you wish to extract transitivity information from in a directory titled "verb_args" in the same directory as this script.

