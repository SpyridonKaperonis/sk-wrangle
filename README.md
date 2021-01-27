# sk-wrangle
Description: Bonus Challenge Big Data


## Assigned Play 
- Romeo and Juliet
## Speakers
1. Capulet
1. Montague
## Question asked
- How many times did Capulet and Montague speak ?

## Answer
 
1. Capulet spoke 30 times
1. Montague spoke 9 times

## Process to finish this assignment 

### Commands
1. Store the html in data.txt.  Sort it, remove tags and save it in result.txt
- ```Curl "http://shakespeare.mit.edu/romeo_juliet/full.html" > data.txt```

- ```tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr | result.txt```
2. Find the count of how many times Capulet and Montague speak. Save the files of count separately.

- ```grep -ic "<b>CAPULET</b>" result.txt```
- ```grep -i "<b>CAPULET</b>" result.txt > capulet.txt```
- ```grep -ic "<b>CAPULET</b>" result.txt > capuletCount.txt```  

- ```grep -ic "<b>MONTAGUE</b>" result.txt```
- ```grep -i "<b>MONTAGUE<\b>" result.txt > montague.txt```
- ```grep -ic "<b>MONTAGUE<\b>" result.txt > montagueCount.txt```
3. Calculate the sum of how many times Capulet and Montague speak. 
I had to learn some more bash  [StackExchange](https://unix.stackexchange.com/questions/93029/how-can-i-add-subtract-etc-two-numbers-with-bash) & [Bash - add number to a variable](https://infoheap.com/bash-add-number-variable/)

- ```capulet=$(grep -i '<b>CAPULET</b>' result.txt -c) ```
- ```montague=$(grep -i '<b>MONTAGUE</b>' result.txt -c) ```
- ```total=$(($capulet + $montague))```
4. Save the sum in sum.txt
- ```echo $total > sum.txt``` 

## Problems 

1. I had to separate the times Capulet speaks from the times the name appears in the text. I used the ```<b></b>``` to separate it since the times she speaks appears with bold letters in the html. I did the same for Montague.

1. I had to figure out how to add the two numbers. I had to learn some more bash. 