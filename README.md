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

Afterwards, the normalized array will be saved using this line of code:

    np.save("X_normalized.npy", X_normalized)

## B. CUBES DIVISIBLE BY 4 PROBLEM

### Code:

    C = (np.arange(1,101) ** 3).reshape(10,10)

The code **np.arange(1, 101)** creates the first 100 positive integers. The ** 3 operation cubes each integer as ** means exponential. Lastly, the **reshape(10,10)** reshapes the results into a 10x10 ndarray. In other words, this line of code creates an array of the first 100 positive integers, cubes them, and reshapes the array size into a 10x10.

### Boolean Filtering

    div_by_4 = C[C % 4 == 0]

This line of code uses Boolean indexing to identify the values in C that are divisible by 4. The **C % 4** calculates the remainder when each element is divided by 4. The condition **C % 4 == 0** identifies all the values inside the array that would have a remainder of 0 when divided by 4.

    print("Number of Selected Elements:", div_by_4.size)

This line of code identifies how many elements are divisible by 4. The result should be **50**.

These values are then stored in this line of code:

    np.save("div_by_4.npy", div_by_4)

## C. ABOVE-MEAN SQUARES PROBLEM

### Code:

    S = (np.arange(1,37) ** 2).reshape(6,6)

This line of code creates an array with a size of 6x6 containing the squares of 36 positive integers. The code **np.arange(1, 37) creates the positive integers, ** 2 squares them, and **reshape(6,6)** defines their size. These values are arranged in increasing row-major order.

    S_mean = S.mean()

This line of code calculates the mean of all the elements inside the array and stores it in **S_mean**.

### Boolean Filtering

    above_mean = S[S > S_mean]

This line of code uses Boolean indexing to identify the values that are greater than the mean, specifically the operation **S > S_mean**.

    print("Number of Selected Elements: ")
    print(above_mean.size)

These lines of codes identifies how many elements are above the mean. The result should be **15**.

These values are then stored in this line of code:

    np.save("above_mean.npy", above_mean)



    
