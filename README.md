# Assignment 0 - CS 5304 Data Science in the Wild

Robert Konigsberg
rak275@cornell.edu

## Summary
The zip file for this submission has code / results for two tasks: 
1) Word count 
2) Conditional bigram distribution 

## Contents
The zip file accompanying this submission contains the following: <br />
> This README.md file <br />
> Wiki.txt file used for this assignment <br />
> [Step 4] Python code used for the word count of wiki.txt: <br />
> [Step 4] Output file for the word count program <br />
> [Step 5] Python code for the conditional bigram distribution of wiki.txt <br />
> [Step 5] Output file for all bigrams in wiki.txt <br />
> [Step 5] Output file for the conditional bigram distribution <br />

## How to run code and where to find the output
Step 4:
> Download the file wordcount.py along with wiki.txt <br />
> Navigate to the folder that contains this file, and ensure that the machine has Spark installed (as indicated in CS5304 lecture) <br />
> Run the following in the command line: spark-submit ./wordcount.py ./wiki.txt ./output<br />
> Go to the "output" folder, and load the file "part-00000" to inspect results<br />

Step 5: 
> Download the file bigram.py along with wiki.txt <br />
> Navigate to the folder that contains this file, and ensure that the machine has Spark installed (as indicated in CS5304 lecture) <br />
> Run the following in the command line: spark-submit ./bigram.py ./wiki.txt ./output <br />
> Go to the "output" folder, and load the file "part-00000" to inspect results <br />

Note: every time python code is ran, ensure the folder "Output" is deleted in the directory 

## Results
Step 4: 
> A sample line of the output file is: ('social', 3201) <br />
> This indicates the word social appeared in wiki.txt 3201 times <br />

Step 5: 
> A sample line of the output file is: (Row(_1='mansions', _2='and'), 3, 0.16666666666666666) <br />
> This indicates that the bigram "mansions and" appeared in wiki.txt 3 times. The conditional frequency of this bigram is ~0.1667, achieved by taking the count of the bigram and dividing by the count of the first word. <br />

Note: when running the code for step 5, see the terminal for easy to view results of the wordcount of wiki.txt, bigram count of wiki.txt and the bigram frequency distribution of wiki.txt <br />

## Additional Sources
> https://stackoverflow.com/questions/70522152/calculate-relative-frequency-of-bigrams-in-pyspark
> https://stackoverflow.com/questions/35544170/bigram-count-using-spark-python-producing-strange-output
