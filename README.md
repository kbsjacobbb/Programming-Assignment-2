# ECE 2112 - Experiment 2: Numerical Pythong (NUMPY)

Balagtas, Jacob T.

2ECE-B

9/3/2026

## Objective of the Experiment

The objective of this experiment is to hone and develop Python skills. In these activities, it will help develop skills pertaining to creating and reshaping NumPy arrays, performing vectorized numerical operations, and computing array statistics using Boolean conditions.

## A. REPRODUCIBLE NORMALIZATION PROBLEM

### Code:

    np.random.seed(2112)
    X = np.random.randint(10, 101, size=(5, 5))
    X

This set of codes creates a reproducible random 5 x 5 integer ndarray that contains integers ranging from 10 to 100. The code of **np.random.seed(2112)** gives it the ability to produce random integers. On the other hand, **np.random.randint(10, 101, size=(5, 5))** is the code that sets conditions for these random integers such as their range and size.

    X_mean = X.mean()
    X_std = X.std()

This set of codes defines functions to calculate the mean and standard deviation for each of the 25 elements in the array. **X.mean()** calculates the mean of all the elements, while **X.std()** calculates the standard deviation.

    X_normalized = (X - X_mean) / X_std

This line of code is the equation used to solve each integer in the Normalized Array. It subtracts the values of X (random integers) from the X_mean (mean), then divides them by X_std (standard deviation). After normalization, the mean of X_normalized must equal to **0**, while the standard deviation should approximately equal to **1**.

## B. CUBES DIVISIBLE BY 4 PROBLEM

### Code:

    C = (np.arange(1,101) ** 3).reshape(10,10)

This line of code creates the first 100 positive integers, cubes them, and reshapes the results into a 10x10 ndarray. The code **np.arange(1, 101)** creates the first 100 positive integers, ****3** cubes each integer as ****** means exponential, and **reshape(10,10)** reshapes the results into a 10x10 ndarray.



    
