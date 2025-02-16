# Hello all, I am sharing how to use Aggregate functions in SQL  

## The main idea behind an aggregate function is to take multiple inputs and return a single input.  
## Most common aggregate functions ;
         1. AVG () = returns average value
         2. COUNT () = returns number of values
         3. MAX () = returns maximum value
         4. MIN () = returns minimum value
         5. SUM() = returns the sum of all values  

## Aggregate function calls happen only in SELECT statement or HAVING statement.  

## AVG() returns a floating point value. So we can use ROUND() to specify precision after decimel.  

### Examples  

#### Suppose we have a table T1 which has columns named film_id and replacement_cost.  

1. Find minimum replacement cost among all.
``` 
SELECT MIN(replacement_cost) FROM T1 ;
```  


2. Find maximum replacement cost among all.  
``` 
SELECT MAX(replacement_cost) FROM T1 ;
```  


3. Find minimum and maximum replacement cost.  
``` 
SELECT MIN(replacement_cost), MAX(replacement_cost) FROM T1 ;
```   


Note - `SELELCT MAX(replacement_cost), film_id FROM T1` : This code won't work because aggregate function cannot be combined with any other column of a table.  


4. Find average replacement cost
``` 
SELECT AVG(replacement_cost) FROM T1 ;
```   

5. Find average replacement cost and round it to 2 decimal places.  
``` 
SELECT ROUND (AVG(replacement_cost), 2) FROM T1 ;
```  

4. Find SUM of replacement cost  
``` 
SELECT SUM(replacement_cost) FROM T1 ;
```  

## That's it for the Aggregate functions, see you in the next chapter !!