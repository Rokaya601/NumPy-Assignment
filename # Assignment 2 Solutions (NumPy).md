# Assignment 2 Solutions (NumPy)

## Q1: 3x3 random integers (1-100) then normalize to [0, 1]

```python
import numpy as np

print("=== Q1 ===")
arr1 = np.random.randint(1, 101, size=(3, 3))
normalized = (arr1 - arr1.min()) / (arr1.max() - arr1.min())
print("Original:\n", arr1)
print("Normalized:\n", normalized)

```

## Q2: 1D array of 10 random numbers, find the closest to X
```python
print("\n=== Q2 ===")
arr2 = np.random.randint(1, 101, size=10)
print("Array:", arr2)
x = float(input("Enter a value X: "))
closest = arr2[np.abs(arr2 - x).argmin()]
print("Closest value to X:", closest)

```
## Q3: 5x5 random array, second-largest value in each column

```python
print("\n=== Q3 ===")
arr3 = np.random.randint(1, 100, size=(5, 5))
second_largest = np.sort(arr3, axis=0)[-2]   
print("Array:\n", arr3)
print("Second-largest per column:", second_largest)

```
## Q4: 6x4 random integers, rows whose sum is even

```python
print("\n=== Q4 ===")
arr4 = np.random.randint(1, 100, size=(6, 4))
row_sums = arr4.sum(axis=1)
even_rows = np.where(row_sums % 2 == 0)[0]
print("Matrix:\n", arr4)
print("Row sums:", row_sums)
print("Indices of rows with even sum:", even_rows)

```
## Q5: 30 random integers (1-50), replace multiples of 3 or 5 with -1

```python

print("\n=== Q5 ===")
arr5 = np.random.randint(1, 51, size=30)
print("Original:", arr5)
arr5[(arr5 % 3 == 0) | (arr5 % 5 == 0)] = -1
print("Modified:", arr5)

```
## Q6: 3x3 random array, subtract each row's mean from that row

```python
print("\n=== Q6 ===")
arr6 = np.random.randint(1, 100, size=(3, 3)).astype(float)
result = arr6 - arr6.mean(axis=1, keepdims=True)
print("Original:\n", arr6)
print("After subtracting row means:\n", result)

```


