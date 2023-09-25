
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

matrix1, matrix2
