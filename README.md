# assignment4-python-
import numpy as np
# Question 1: Array Creation
# 1.1 
arr1 = np.arange(5, 26)
print("1.1 1D Array:\n", arr1)

# 1.2 
arr2 = np.random.randint(10, 51, size=(3, 4))
print("\n1.2 2D Random Array:\n", arr2)

# Question 2: Array Attributes

# 2.1
print("\n2.1 Attributes of 1D Array:")
print("Shape:", arr1.shape)
print("Size:", arr1.size)
print("Data Type:", arr1.dtype)

# 2.2 
print("\n2.2 Attributes of 2D Array:")
print("Shape:", arr2.shape)
print("Size:", arr2.size)
print("Data Type:", arr2.dtype)

# Question 3: Array Operations
# 3.1
array1 = np.array([2, 4, 6, 8, 10])
array2 = np.array([1, 3, 5, 7, 9])

# 3.2 
print("\n3.2 Array Operations:")
print("Addition:", array1 + array2)
print("Subtraction:", array1 - array2)
print("Multiplication:", array1 * array2)
print("Division:", array1 / array2)

# Question 4: Broadcasting
# 4.1
arr3 = np.arange(1, 10).reshape(3, 3)
print("\n4.1 2D Array:\n", arr3)

# 4.2 
print("\n4.2 After Broadcasting (x5):\n", arr3 * 5)


# Question 5: Slicing and Indexing

# 5.1 
arr4 = np.arange(10, 26).reshape(4, 4)
print("\n5.1 2D Array (4x4):\n", arr4)

# 5.2 
print("\n5.2 Second Row:", arr4[1])
print("5.2 Last Column:", arr4[:, -1])

# 5.3 
arr4[0] = 0
print("\n5.3 After Replacing First Row with Zeros:\n", arr4)


# Question 6: Boolean Indexing
# 6.1
arr5 = np.random.randint(20, 41, size=10)
print("\n6.1 Random 1D Array:", arr5)

# 6.2
print("6.2 Elements > 30:", arr5[arr5 > 30])

arr5 = np.random.randint(20, 41, size=10)
print("\n6.1 Random 1D Array:", arr5)

# 6.2 Extract elements greater than 30
print("6.2 Elements > 30:", arr5[arr5 > 30])



# Question 7: Reshaping

# 7.1 
arr7 = np.arange(11, 23)
print("7.1 Array:", arr7)

# 7.2 
arr7_reshaped = arr7.reshape(3, 4)
print("\n7.2 Reshaped (3x4):\n", arr7_reshaped)

# Question 8: Matrix Operations
# 8.1 
A = np.array([[1, 2],
              [3, 4]])
B = np.array([[5, 6],
              [7, 8]])

# 8.2 Matrix multiplication and transpose of A
print("\n8.2 A @ B:\n", A @ B)        # [[19 22], [43 50]]
print("8.2 A.T:\n", A.T)              # [[1 3], [2 4]]


# Question 9: Statistical Functions
# 9.1 
arr9 = np.random.randint(10, 61, size=15)
print("\n9.1 Array:", arr9)

# 9.2 
print("9.2 Mean:", np.mean(arr9))
print("9.2 Median:", np.median(arr9))
print("9.2 Std (ddof=0):", np.std(arr9, ddof=0))


# Question 10: Linear Algebra
# 10.1 
A10 = np.array([
    [2, 1, 3],
    [0, 5, 6],
    [7, 8, 9]
], dtype=float)

# 10.2 
detA = np.linalg.det(A10)
invA = np.linalg.inv(A10)
eigvals, eigvecs = np.linalg.eig(A10)

print("\n10.2 det(A):", detA)          # ≈ -69.0
print("10.2 inv(A):\n", invA)
print("10.2 eigenvalues:\n", eigvals)
print("10.2 eigenvectors (columns correspond to eigenvalues):\n", eigvecs)


# Question 11: Robot path distances
positions = np.array([(0, 0), (2, 3), (4, 7), (7, 10), (10, 15)], dtype=float)

# 11.1 
print("\n11.1 First→Last distance:", np.linalg.norm(positions[-1] - positions[0]))  # ≈ 18.027756...

# 11.2 Total 
total_dist = np.sum(np.linalg.norm(np.diff(positions, axis=0), axis=1))
print("11.2 Total path length:", total_dist)  # ≈ 18.151279...


