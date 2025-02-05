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
