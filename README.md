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
 
1. Capulet spoke 34 times
1. Montague spoke 13 times

## Process to finish this assignment 

### Commands

- ```Curl "http://shakespeare.mit.edu/romeo_juliet/full.html" > data.txt```

- ```tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr | result.txt```

- ```grep -c "CAPULET" result.txt```

- ```grep -c "MONTAGUE" result.txt```
