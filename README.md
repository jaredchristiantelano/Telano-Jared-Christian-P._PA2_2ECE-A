# Telano-Jared-Christian-P._PA2_2ECE-A
This assignment use different codes to create Python programs with the use of NumPy library. 

**Normalization Problem
**

**Description:** In this problem, NumPy library was used to perform a normalization technique, specifically performing the z-score normalization. To start, a random 5x5 ndarray with random floating point values was created. Then, the average and standard deviation of the elements in the array are calculated using np.mean() and np.std(), respectively. The calculated values were then used for the z-zcore normalization.

**Code**
```
# Normalization Problem
import numpy as np                      # Imports NumPy library 

X = np.random.random((5, 5))            # Creates a 5x5 array with random floating point values 

mean = np.mean(X)                       # Calculates the average of the elements in the created array
std = np.std(X)                         # Calcuates the standard deviation of the array 

X = (X - mean) / std                    # Normalizes X 
print(X)                                # Prints X 
np.save('X_normalized.npy', X)          # Saves the NumPy array 
```
**Output**
```
[[-0.94877624  1.37849769 -1.1929761  -2.24600106  0.79851006]
 [-1.03390308  0.6597996   0.08974712  1.43624399  1.36898711]
 [ 0.56514916 -0.2190846  -0.19540352  1.54987897  0.79384071]
 [ 0.78806155 -0.85866236 -0.73990502  0.88011281 -1.32853001]
 [-0.93428443 -0.42399008 -0.49554684  0.61017021 -0.30193564]]
```

**Divisible By 3 Problem
**

**Description:** In this problem, a 10x10 ndarray was created with values of the square of the first 100 positive integers. Then, the elements of the array are then filtered, retaining elements that are divisible by 3, and replacing other numbers with zeroes.
