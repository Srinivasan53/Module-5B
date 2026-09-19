# NumPy Program: Column-wise Sorting of a 2D Array

## Aim

To write a NumPy program that sorts the elements in each column of a given 2D array in ascending order.

## Algorithm

1. Import the NumPy library.
2. Create a 2D NumPy array.
3. Use `np.sort()` with `axis=0` to sort each column in ascending order.
4. Store the sorted array in a new variable.
5. Display the original array and the sorted array.

## Program

```python id="q7m2vx"
import numpy as np

a = np.array([[3, 2, 1],
              [6, 5, 4],
              [9, 8, 7]])

print("Original Array:")
print(a)

sorted_array = np.sort(a, axis=0)

print("Column-wise Sorted Array:")
print(sorted_array)
```

## Output

```text id="r8k4pn"
Original Array:
[[3 2 1]
 [6 5 4]
 [9 8 7]]

Column-wise Sorted Array:
[[3 2 1]
 [6 5 4]
 [9 8 7]]
```

## Result

Thus, the NumPy program successfully sorts the elements of each column of a 2D array in ascending order.

# NumPy Program: Find Indices Where Elements in Array `x` are Greater Than or Equal to Corresponding Elements in Array `y`

## Aim

To write a Python program using NumPy that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

## Algorithm

1. Import the NumPy library.
2. Define two NumPy arrays, `x` and `y`.
3. Compare the corresponding elements using `x >= y`.
4. Use `np.where()` to find the indices where the condition is `True`.
5. Print the indices.

## Program

```python id="t3k7qm"
import numpy as np

x = np.array([10, 20, 30, 40, 50])
y = np.array([5, 25, 30, 45, 40])

indices = np.where(x >= y)

print("Indices where x is greater than or equal to y:")
print(indices[0])
```

## Output

```text id="n5p8rx"
Indices where x is greater than or equal to y:
[0 2 4]
```

## Result

Thus, the NumPy program successfully finds and displays the indices where the elements of array `x` are greater than or equal to the corresponding elements of array `y`.

# NumPy Program: Replace the Second Column in a 2D Array

## Aim

To write a NumPy program that deletes the second column from a given 2D array and inserts a new column at the same position.

## Algorithm

1. Import the NumPy library.
2. Create a 2D NumPy array and a new column.
3. Delete the second column using `np.delete()`.
4. Insert the new column at the second column's original position using `np.insert()`.
5. Display the updated array.

## Program

```python id="v6m2kp"
import numpy as np

a = np.array([[1, 2, 3],
              [4, 5, 6],
              [7, 8, 9]])

new_column = np.array([10, 20, 30])

a = np.delete(a, 1, axis=1)
a = np.insert(a, 1, new_column, axis=1)

print("Updated Array:")
print(a)
```

## Output

```text id="k3r8qn"
Updated Array:
[[ 1 10  3]
 [ 4 20  6]
 [ 7 30  9]]
```

## Result

Thus, the NumPy program successfully replaces the second column of the given 2D array with a new column.

# Pandas Program: Create and Display a DataFrame with Custom Index Labels

## Aim

To create and display a DataFrame using the Pandas library in Python from a given dictionary and apply specific index labels to the rows.

## Algorithm

1. Import the required libraries, `pandas` and `numpy`.
2. Create a dictionary `exam_data` with the keys `name`, `score`, `attempts`, and `qualify`.
3. Create a list of custom index labels called `labels`.
4. Create the DataFrame using `pd.DataFrame()`.
5. Display the DataFrame.

## Program

```python id="m4k8qx"
import pandas as pd
import numpy as np

exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily'],
    'score': [12.5, 9, 16.5, np.nan, 9],
    'attempts': [1, 3, 2, 3, 2],
    'qualify': ['yes', 'no', 'yes', 'no', 'no']
}

labels = ['a', 'b', 'c', 'd', 'e']

df = pd.DataFrame(exam_data, index=labels)

print(df)
```

## Output

```text id="x7p3vn"
         name  score  attempts qualify
a   Anastasia   12.5         1     yes
b        Dima    9.0         3      no
c   Katherine   16.5         2     yes
d       James    NaN         3      no
e       Emily    9.0         2      no
```

## Result

Thus, the Pandas program successfully creates and displays a DataFrame with custom index labels.

Here is the completed version:

# Pandas Program: Join Two DataFrames Along Rows

## AIM

To write a Python program using Pandas to join two DataFrames along rows and assign all data to a new DataFrame.

## ALGORITHM

1. Import the `pandas` library.
2. Create the first DataFrame using `student_data1`.
3. Create the second DataFrame using `student_data2`.
4. Use `pd.concat()` with `axis=0` to join the DataFrames row-wise.
5. Display the combined DataFrame.

## PROGRAM

```python
import pandas as pd

student_data1 = {
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Danni', 'Ravi', 'Alex', 'Kumar', 'John'],
    'marks': [85, 90, 78, 88, 92]
}

student_data2 = {
    'student_id': ['S6', 'S7', 'S8', 'S9', 'S10'],
    'name': ['Sara', 'David', 'Priya', 'Mike', 'Anu'],
    'marks': [80, 75, 89, 91, 86]
}

df1 = pd.DataFrame(student_data1)
df2 = pd.DataFrame(student_data2)

new_df = pd.concat([df1, df2], axis=0, ignore_index=True)

print(new_df)
```

## OUTPUT

```text
  student_id   name  marks
0         S1  Danni     85
1         S2   Ravi     90
2         S3   Alex     78
3         S4  Kumar     88
4         S5   John     92
5         S6   Sara     80
6         S7  David     75
7         S8  Priya     89
8         S9   Mike     91
9        S10    Anu     86
```

## RESULT

Thus, the two DataFrames were successfully joined row-wise using Pandas `concat()` and the combined data was stored in a new DataFrame.
