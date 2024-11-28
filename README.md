# Searching Algorithms in Python

This repository provides implementations and comparisons of various searching algorithms in Python.  It includes examples of linear search, binary search, jump search, and interpolation search.  Each algorithm is implemented as a separate function, and example usage is demonstrated.  Basic timing comparisons are included to show the relative performance of each algorithm under different conditions.

## Algorithms Included

* **Linear Search:** A simple search that iterates through the entire list sequentially.  Suitable for unsorted lists but inefficient for large datasets.
* **Binary Search:** An efficient algorithm for searching in sorted lists.  It repeatedly divides the search interval in half.
* **Jump Search:** An improvement over linear search, particularly for large lists.  It jumps ahead by a fixed step size and then performs a linear search within a smaller subarray.
* **Interpolation Search:** Similar to binary search but uses interpolation to estimate the position of the search key.  It's most efficient when the data is uniformly distributed.


## Usage

Each algorithm is implemented as a function. To use them:

1. **Ensure your list is sorted** if using Binary Search, Jump Search or Interpolation Search.  Linear Search works on both sorted and unsorted lists.
2. Call the appropriate function with your list and the search key as arguments.  The function will return the index of the key if found, or -1 otherwise.


```python
import my_search_algorithms #Import your file containing the functions.

my_list = [2, 5, 7, 8, 11, 12]  #Example -Remember to sort for Binary, Jump, Interpolation

#Linear Search (works on sorted and unsorted)
index = my_search_algorithms.linear_search(my_list, 11)
print(f"Linear Search: Item found at index {index}")

#Binary Search (requires sorted list)
index = my_search_algorithms.binary_search(my_list, 8)
print(f"Binary Search: Item found at index {index}")

#Jump Search (requires sorted list)
index = my_search_algorithms.jump_search(my_list, 12)
print(f"Jump Search: Item found at index {index}")


#Interpolation Search (requires sorted list)
index = my_search_algorithms.interpolation_search(my_list, 7)
print(f"Interpolation Search: Item found at index {index}")
