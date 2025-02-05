# Debugging

## EXERCISE 1
### ❓ It does not print the fruit at the correct index, why is the returned result wrong?
A : The fruits parameter is a Set, which means its elements are unordered.
### 🤔 How could this be fixed?
A : Instead of a Set, use a List to maintain index order for fruits param by replacing curly braces {} with square brackets [].

## EXERCISE 2
### ❓ Can you spot the obvious error?
A : The error in "coords[:, 0], coords[:, 1], coords[:, 2], coords[:, 3], = coords[:, 1], coords[:, 1], coords[:, 3], coords[:, 2]" is due to copying instead of swapping. The first column duplicates the second, leaving the second unchanged. Similarly, the third column copies the fourth, and the fourth copies the third, causing its value to remain the same.
### 🤔 After fixing the obvious error it is still wrong, how can this be fixed?
A : Fixing it with NumPy indexing will correctly swap the columns.

## EXERCISE 3
### ❓ For some reason the plot is not showing correctly, can you find out what is going wrong?
A : First, the data has blank rows, raising a ValueError('all input arrays must have the same shape'). Second, the coordinates are mismatched, with precision on the x-axis and recall on the y-axis. Finally, the plot only displays two values: [0.013, 0.951] and [0.376, 0.851].
### 🤔 How could this be fixed??
A : First, fix the data by adding newline='' in the f variable to prevent blank lines. Then, swap the result index in plot() and update the x, y labels. Finally, convert the result values from strings to float using np.array(results, dtype=float).

## EXERCISE 4
### ❓ Changing the batch_size from 32 to 64 triggers the structural bug
A :
### 🤔 Can you also spot the cosmetic bug?
A : 