  
## About Me and the Objective of the Project  
I am shiva kumar from Hyderabad,India. <br>
I have completed my undergraduation from MVSR Engineering College, Hyderabad in Civil Enginnering Department, 2015.<br>
I have worked in Infosys as Systems Engineer for 21 months as Application Developer.  
The objective of the prject is to find the word count in a file using spark.


## Dataset:  
It is the data from shakepeare's Measure of Measure book. It is from the Act 1 The Street Scene 2 Where we have the conversation of two gentlemen. 

http://shakespeare.mit.edu/measure/measure.1.2.html

## Commands used:
> val inputFile = sc.textFile("C:\44517\Spark-scala-wordCountShiva\shakespeare.txt")  
Commad to load shakespeare.txt data

>val counts = inputFile.flatMap(line => line.split(" ")).map(word => (word,1)).reduceByKey(_ + _);  
command to count words with space deliminator

> counts.saveAsTextFile("c:/tmp/show-spark/ShakespeareOutput.txt")  
Command to save the results in ShakespeareOutput.txt  
## Result

| Word    | Count|
|---------|------|
| the      | 61  |
| of      | 39   |
| i      | 36   |
| LUCIO      | 27   |
| to       | 24   |
| a     | 24   |
| in       | 22   |
| Gentleman    | 21   |
| for      | 21   |
| and | 20   |


By observing the results we see that "the" is the most repeating word in the article followed by other words. You can see the markdown table to view the results.

## Screenshot of results graph
![wprdcountgraph](https://user-images.githubusercontent.com/31738370/48320918-1f959100-e5e4-11e8-980f-caf460ef6e02.PNG)
