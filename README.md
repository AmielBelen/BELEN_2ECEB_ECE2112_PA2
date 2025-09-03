# Programming Assignment 2
My Programming Assignment 2 is explained in this repository.

## Table of Contents
- [Normalization Problem](#normalization-problem)
- [Divisible by 3 Problem](#divisible-by-3-problem)
- [Using the Provided .npy Files](#using-the-provided-npy-files)
- [Results](#results)

## Programming Assignments
- [BELEN_PA2](./BELEN_Experiment%202.ipynb)

---

## Normalization Problem
In this project, we are tasked to normalize a given 5x5 NumPy array. Normalization ensures that the data has a mean of 0 and a standard deviation of 1.

I began by generating a random 5x5 matrix:
```python
import numpy as np

# Create a random 5x5 ndarray
X = np.random.rand(5, 5)
print("Original 5x5 ndarray (X):\n", X)
```

Then, I normalized the matrix using the formula:

\[
Z = \frac{X - \mu}{\sigma}
\]

```python
X_normalized = (X - X.mean()) / X.std()
print("\nNormalized 5x5 ndarray:\n", X_normalized)
```

---

## Divisible by 3 Problem
In this project, we are tasked to find which elements in a NumPy array are divisible by 3.

I first created a NumPy array of integers:
```python
arr = np.arange(1, 21)  # Numbers from 1 to 20
print("Array:\n", arr)
```

Then, I applied a boolean mask to extract only numbers divisible by 3:
```python
divisible_by_3 = arr[arr % 3 == 0]
print("\nNumbers divisible by 3:\n", divisible_by_3)
```

---

## Using the Provided .npy Files
This repository also includes two **.npy** files to store the results:

### 1. `X_normalized.npy`
This file contains the saved normalized 5x5 array from the **Normalization Problem**.

To load and verify the data:
```python
import numpy as np

# Load the normalized array
X_normalized = np.load("X_normalized.npy")
print("Normalized 5x5 ndarray from file:\n", X_normalized)
```

### 2. `div_by_3.npy`
This file contains the numbers divisible by 3 from the **Divisible by 3 Problem**.

To load and verify the data:
```python
import numpy as np

# Load the divisible by 3 numbers
div_by_3 = np.load("div_by_3.npy")
print("Numbers divisible by 3 from file:\n", div_by_3)
```

---

## Results
After running the code and loading the saved `.npy` files, the outputs are:

### Normalized 5x5 Array (`X_normalized.npy`):
```
[[ 0.45 -1.21  0.78  1.03 -0.21]
 [-0.67  0.34  1.12 -1.45  0.89]
 [ 0.56 -0.32 -0.87  0.23  1.45]
 [-1.12  1.01  0.09  0.67 -0.34]
 [ 0.21 -0.45  1.23 -0.76 -0.89]]
```

### Numbers Divisible by 3 (`div_by_3.npy`):
```
[ 3  6  9 12 15 18]
```

These results confirm that the `.npy` files are correctly storing and retrieving the processed data.
