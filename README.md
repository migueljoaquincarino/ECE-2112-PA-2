# ECE-2112-PA-2
Miguel Joaquin T. Cariño 2 ECE-D
# Programming Assignment 2
## A. Reproducible Normalization Problem
## Objective
The objective of this problem is to create a reproducible 5x5 array and to normalize all of its elements using the mean and standard deviation while using numpy. 
## Discussion of Methods:
The random number generator was first made reproducible by using 2112 as its fixed seed, with the use of numpy a 5x5 array produces random integers from 10 to 100.
The mean and standard deviation were calculated using numpy's mean and standard deviation functions.
The array was normalized by using the formula
The array was saved as a Numpy file. 
## B. Cubes Divisible by 4 Problem
## Objective 
The objective of this problem is to create a 10x10 array in which containts the cubes of the first 100 positive integers and use a boolean condition to select the values that are divisible by 4
## Discussion of Methods:  
Using np.arange the first 100 positive integers was generated and each element was cubed.
The resulting array waas reshaped intoa 10x10 array shape
Boolean was used in selecting the values that are divisible by 4 
The array was saved as a Numpy file.
## C. Above Mean Squares Problem
## Objective
The objective of this problem is to create a 6x6 array in which contains the squares of the first 36 positive intgers, calculate for its mean, and use boolean to select values that are strictly greater than the mean 
## Discussion of Methods
Using np.arange the first 36 positive integers were generated using and squaring its elements
The resulting values were then reshaped into a 6x6 array
The mean of all elements was calculated using numpy's mean function. 
Boolean was then used to select the elements that are greater than the mean 
The selected arry was then saved as a numpy file 
