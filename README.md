
import numpy as np

# Read values for the first matrix
rows1 = int(input("Enter the number of rows for Matrix 1: "))
cols1 = int(input("Enter the number of columns for Matrix 1: "))

matrix1 = []
for i in range(rows1):
    row = []
    for j in range(cols1):
        element = float(input(f"Enter element for Matrix 1 at row {i + 1}, column {j + 1}: "))
        row.append(element)
    matrix1.append(row)

# Read values for the second matrix
rows2 = int(input("Enter the number of rows for Matrix 2: "))
cols2 = int(input("Enter the number of columns for Matrix 2: "))

matrix2 = []
for i in range(rows2):
    row = []
    for j in range(cols2):
        element = float(input(f"Enter element for Matrix 2 at row {i + 1}, column {j + 1}: "))
        row.append(element)
    matrix2.append(row)

matrix1 = np.array(matrix1)
matrix2 = np.array(matrix2)

# 1. Dot Product
dot_product = np.dot(matrix1, matrix2)

# 2. Transpose
transpose_matrix1 = np.transpose(matrix1)
transpose_matrix2 = np.transpose(matrix2)

# 3. Trace
trace_matrix1 = np.trace(matrix1)
trace_matrix2 = np.trace(matrix2)

# 4. Rank
rank_matrix1 = np.linalg.matrix_rank(matrix1)
rank_matrix2 = np.linalg.matrix_rank(matrix2)

# 5. Determinant
determinant_matrix1 = np.linalg.det(matrix1)
determinant_matrix2 = np.linalg.det(matrix2)

# 6. Inverse
try:
    inverse_matrix1 = np.linalg.inv(matrix1)
    inverse_matrix2 = np.linalg.inv(matrix2)
except np.linalg.LinAlgError:
    inverse_matrix1 = "Inverse does not exist for Matrix 1"
    inverse_matrix2 = "Inverse does not exist for Matrix 2"

# 7. Eigenvalues and Eigenvectors
eigenvalues_matrix1, eigenvectors_matrix1 = np.linalg.eig(matrix1)
eigenvalues_matrix2, eigenvectors_matrix2 = np.linalg.eig(matrix2)

# Display results
print("\nMatrix 1:")
print(matrix1)
print("\nMatrix 2:")
print(matrix2)

print("\n1. Dot Product:")
print(dot_product)

print("\n2. Transpose of Matrix 1:")
print(transpose_matrix1)
print("2. Transpose of Matrix 2:")
print(transpose_matrix2)

print("\n3. Trace of Matrix 1:", trace_matrix1)
print("3. Trace of Matrix 2:", trace_matrix2)

print("\n4. Rank of Matrix 1:", rank_matrix1)
print("4. Rank of Matrix 2:", rank_matrix2)

print("\n5. Determinant of Matrix 1:", determinant_matrix1)
print("5. Determinant of Matrix 2:", determinant_matrix2)

print("\n6. Inverse of Matrix 1:")
print(inverse_matrix1)
print("6. Inverse of Matrix 2:")
print(inverse_matrix2)

print("\n7. Eigenvalues and Eigenvectors of Matrix 1:")
print("Eigenvalues:")
print(eigenvalues_matrix1)
print("Eigenvectors:")
print(eigenvectors_matrix1)

print("\n7. Eigenvalues and Eigenvectors of Matrix 2:")
print("Eigenvalues:")
print(eigenvalues_matrix2)
print("Eigenvectors:")
print(eigenvectors_matrix2)
```

This code will calculate and display all the requested matrix operations for the two matrices you've entered.
