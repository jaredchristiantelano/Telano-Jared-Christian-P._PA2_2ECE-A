# Telano-Jared-Christian-P._PA2_2ECE-A
This assignment used different codes to create Python programs with the use of NumPy library. 

**Normalization Problem**

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

**Divisible By 3 Problem**

**Description:** In this problem, NumPy library was imported first. Then, a 1D array with positive integers from 1 to 100 was created. The 1D array was then shaped into a 10x10 2D array using the function .reshape(). The values in that 2D array was then squared. After creating the needed array, a function that checks whether the element in that array is divisible by 3. If the element is divisible by 3, the number is retained. If not, the element is returned as 0. The function returns the new array, where elements that are divisible by 3 are returned. 


**Code**

```
# Divisible by 3 Problem

import numpy as np                               # Imports NumPy library 

C = np.arange(1, 101)                            # Create a 1D array with numbers from 1 to 100
B = C.reshape(10, 10)                            # Reshape the 1D array into a 10x10 2D array
A = B**2                                         # Squares every element in the array 

def find_divisible_by_3(A):                      # The elements are first checked whether they are divisible by 3. The array 
  return A * (A % 3 == 0)                        # is multiplied again. If True, elements are retained that are divisible by 3, while 
                                                 # elements that are not divisible by 3 are replaced with 0
    
D = find_divisible_by_3(A)                       # Calls the function 
print("Square of first 100 positive integers: ")
print(A)
print("Elements divisible by 3: ")               # Dsiplays the array with elements that are divisible by 3
print(D)                                
np.save('div_by_3.npy', D)                       # Saves the NumPy array
```

Output 

```
array([[   0,    0,    9,    0,    0,   36,    0,    0,   81,    0],
       [   0,  144,    0,    0,  225,    0,    0,  324,    0,    0],
       [ 441,    0,    0,  576,    0,    0,  729,    0,    0,  900],
       [   0,    0, 1089,    0,    0, 1296,    0,    0, 1521,    0],
       [   0, 1764,    0,    0, 2025,    0,    0, 2304,    0,    0],
       [2601,    0,    0, 2916,    0,    0, 3249,    0,    0, 3600],
       [   0,    0, 3969,    0,    0, 4356,    0,    0, 4761,    0],
       [   0, 5184,    0,    0, 5625,    0,    0, 6084,    0,    0],
       [6561,    0,    0, 7056,    0,    0, 7569,    0,    0, 8100],
       [   0,    0, 8649,    0,    0, 9216,    0,    0, 9801,    0]])
```
