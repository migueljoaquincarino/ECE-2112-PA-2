# ECE-2112-PA-2
Miguel Joaquin T. Cariño 2 ECE-D
# Programming Assignment 2
## A. Reproducible Normalization Problem
## Objective
The objective of this problem is to create a reproducible 5x5 array and to normalize all of its elements using the mean and standard deviation while using numpy. 
## Discussion of Methods:
The random number generator was first made reproducible by using 2112 as its fixed seed, with the use of numpy a 5x5 array produces random integers from 10 to 100.
```python
np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))
```
The mean and standard deviation were calculated using numpy's mean and standard deviation functions.
```python
Mean = np.mean(X)
STD = np.std(X)
```
The array was normalized by using the formula
```python
X_normalized = (X-Mean)/STD
```
The array was saved as a Numpy file. 
```pyhton
np.save("X_normalized.npy", X_normalized)
```
## Result
```
X-Normalized:
[[ 0.06340841 -1.36714726 -1.2124926   0.79801809 -0.98051059]
 [-1.36714726 -0.20723725 -1.28981993  0.75935442 -0.86451959]
 [ 0.95267275  1.26198209  0.25672675  0.79801809  0.91400909]
 [ 1.18465476 -0.43921926  1.72594609 -1.05783793  1.91926443]
 [-0.43921926  0.29539042 -0.36189192 -0.20723725 -1.13516526]]
 
X:
[[48 11 15 67 21]
 [11 41 13 66 24]
 [71 79 53 67 70]
 [77 35 91 19 96]
 [35 54 37 41 17]]
 
Mean:
46.36
 
Standard Deviation:
25.864075471588002
 
X-Normalized Mean:
0.0
 
X-Normalized STD:
0.9999999999999999
```
## B. Cubes Divisible by 4 Problem
## Objective 
The objective of this problem is to create a 10x10 array in which containts the cubes of the first 100 positive integers and use a boolean condition to select the values that are divisible by 4
## Discussion of Methods:  
Using np.arange, the first 100 positive integers were generated, and each element was cubed.
```python
A = np.arange(1, 101)
B = A*A*A
```
The resulting array was reshaped into a 10x10 array shape
```python
C = B.reshape(10, 10)
```
A Boolean condition was used in selecting the values that are divisible by 4 
```python
div_by_4 = C[C % 4 == 0]
```
The array was saved as a Numpy file.
```python
np.save("div_by_4.npy", div_by_4)
```
## Result
```
Shape of C
(10, 10)
 
div_by_4:
[      8      64     216     512    1000    1728    2744    4096    5832
    8000   10648   13824   17576   21952   27000   32768   39304   46656
   54872   64000   74088   85184   97336  110592  125000  140608  157464
  175616  195112  216000  238328  262144  287496  314432  343000  373248
  405224  438976  474552  512000  551368  592704  636056  681472  729000
  778688  830584  884736  941192 1000000]
 
Number of Elemets:
50
```
## C. Above Mean Squares Problem
## Objective
The objective of this problem is to create a 6x6 array in which contains the squares of the first 36 positive intgers, calculate for its mean, and use boolean to select values that are strictly greater than the mean 
## Discussion of Methods
Using np.arange the first 36 positive integers were generated using and squaring their elements.
```python
S = np.arange(1, 37)
S = S*S
```
The resulting values were then reshaped into a 6x6 array
```python
S = S.reshape(6, 6)
```
The mean of all elements was calculated using numpy's mean function.
```python
S_mean = np.mean(S)
```
Boolean was then used to select the elements that are greater than the mean 
```python
above_mean = S[S > S_mean]
```
The selected array was then saved as a numpy file
```python
np.save("above_mean.npy", above_mean)
```
## Result
```
S:
[[   1    4    9   16   25   36]
 [  49   64   81  100  121  144]
 [ 169  196  225  256  289  324]
 [ 361  400  441  484  529  576]
 [ 625  676  729  784  841  900]
 [ 961 1024 1089 1156 1225 1296]]
 
Mean:
450.1666666666667
 
Above Mean:
[ 484  529  576  625  676  729  784  841  900  961 1024 1089 1156 1225
 1296]
 
Number of Elements:
15
```
Version History

