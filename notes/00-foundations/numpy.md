# NumPy

## What Is NumPy?

NumPy, short for **Numerical Python**, is a Python library used for working with numbers, arrays,
matrices, and mathematical operations.

It provides a special data structure called an **array**. A NumPy array is similar to a Python list,
but it is designed specifically for numerical data and calculations.

NumPy is commonly imported using the name `np`:

    import numpy as np


## Why Is NumPy Useful?

Machine Learning involves working with large amounts of numerical data, which NumPy facillitates.
For example, a dataset might contain:

* the ages of thousands of people
* the prices of houses 
* the pixel values in images
* the measurements collected by sensors
* the features used to train a machine-learning model

NumPy makes it much easier to store, organize, and perform calculations on this data.Instead of
 processing every number individually, NumPy can perform an operation on an entire array at once.

## Python Lists vs NumPy Arrays

A regular Python list can store numbers:

```python
numbers = [1, 2, 3, 4]
```

A NumPy array can store the same values:

```python
numbers = np.array([1, 2, 3, 4])
```

The important difference is how they handle numerical operations.

With a Python list:

```python
numbers = [1, 2, 3, 4]
```

Writing `numbers * 2` repeats the list:

```python
[1, 2, 3, 4, 1, 2, 3, 4]
```

With a NumPy array:

```python
numbers = np.array([1, 2, 3, 4])
print(numbers * 2)
```

The result is:

```text
[2 4 6 8]
```

NumPy multiplies every element in the array by two.

## Vectorization

Performing an operation on an entire array without manually looping through every value is called **vectorization**.

Without NumPy:

```python
numbers = [1, 2, 3, 4]
doubled = []

for number in numbers:
    doubled.append(number * 2)
```

With NumPy:

python
numbers = np.array([1, 2, 3, 4])
doubled = numbers * 2


The NumPy version is shorter and usually faster, especially when working with large datasets.

## Creating an Array

```python
import numpy as np

scores = np.array([85, 90, 78, 92])
print(scores)
```

Output:

```text
[85 90 78 92]
```

NumPy arrays can also contain multiple dimensions.

```python
data = np.array([
    [1, 2, 3],
    [4, 5, 6]
])
```

This creates a two-dimensional array with two rows and three columns.

## Useful Array Information

### Shape

The `shape` attribute shows the dimensions of an array.

```python
print(data.shape)
```

Output:

```text
(2, 3)
```

This means the array has two rows and three columns.

### Number of Dimensions

The `ndim` attribute shows how many dimensions the array has.

```python
print(data.ndim)
```

### Number of Elements

The `size` attribute shows the total number of values.

```python
print(data.size)
```

## Basic Calculations

NumPy can perform calculations across an entire array.

```python
scores = np.array([85, 90, 78, 92])

print(scores.mean())
print(scores.sum())
print(scores.min())
print(scores.max())
```

These calculate the:

* average value
* total value
* smallest value
* largest value

## Why NumPy Matters in Machine Learning

Most machine-learning data is represented using arrays or matrices.

For example, a dataset might look like this:

```python
students = np.array([
    [5, 8, 90],
    [3, 6, 75],
    [7, 9, 95]
])
```

Each row could represent one student, while the columns could represent:

1. hours studied
2. hours slept
3. exam score

Machine-learning models use structures like these to process many observations and features at once.

Libraries such as pandas, scikit-learn, TensorFlow, and PyTorch also rely heavily on NumPy-style arrays and numerical operations.

## Benefits of using NumPy

* performs numerical calculations efficiently
* works with large arrays and matrices
* reduces the need for manual loops
* provides many built-in mathematical functions
* forms the foundation of many data-science and machine-learning libraries

## TLDR

NumPy is a Python library designed for numerical computing.Its main data structure is the NumPy array,
which makes it possible to store and calculate with large amounts of numerical data efficiently.
The biggest idea to remember is that NumPy lets me perform operations on entire arrays instead of 
processing each value individually.

