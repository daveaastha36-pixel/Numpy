1.
Install NumPy using pip and write a Python script list_vs_array.py that creates a list and a NumPy array, each containing the numbers from 1 to 1000.

***answer***
import numpy as np

# Create a Python list containing numbers from 1 to 1000
numbers_list = list(range(1, 1001))

# Create a NumPy array containing numbers from 1 to 1000
numbers_array = np.array(range(1, 1001))

print("Python List:")
print(numbers_list)

print("\nNumPy Array:")
print(numbers_array)

2.
In your script, measure and print the memory usage (in bytes) of both the Python list and the NumPy array containing 1000 integers.<br><br><em><strong>Hint:</strong> Use the sys.getsizeof() function for the list and the nbytes attribute for the NumPy array.</em>

***answer***
import sys
import numpy as np

# Create list and NumPy array
numbers_list = list(range(1, 1001))
numbers_array = np.array(range(1, 1001))

# Calculate memory usage
list_memory = sys.getsizeof(numbers_list)
array_memory = numbers_array.nbytes

# Print memory usage
print("Memory used by Python List:", list_memory, "bytes")
print("Memory used by NumPy Array:", array_memory, "bytes")

3.
Write a function compare_addition_speed() that adds 5 to every element in both a Python list and a NumPy array of 10,000 integers, and prints the time taken for each.<br><br><em><strong>Hint:</strong> Use the time module to measure execution time.</em>

***answer***
import time
import numpy as np


def compare_addition_speed():

    # Create list and NumPy array of 10,000 integers
    numbers_list = list(range(1, 10001))
    numbers_array = np.array(range(1, 10001))

    # Python list addition
    start_time = time.time()

    list_result = []
    for number in numbers_list:
        list_result.append(number + 5)

    list_time = time.time() - start_time

    # NumPy array addition
    start_time = time.time()

    array_result = numbers_array + 5

    array_time = time.time() - start_time

    # Print results
    print("Python List Addition Time:", list_time, "seconds")
    print("NumPy Array Addition Time:", array_time, "seconds")


compare_addition_speed()

4.
Explain with code how vectorized operations in NumPy can replace for-loops when multiplying all elements of an array by 2. Show both the loop and the vectorized version using a Zomato-style example: multiplying all restaurant ratings by 2.

***answer***
import numpy as np

ratings = np.array([4.2, 3.8, 4.5, 4.0, 3.5])

#using loop
loop_result = []

for rating in ratings:
    loop_result.append(rating * 2)

print("Using For-Loop:")
print(loop_result)

#using numpy vactorization
vectorized_result = ratings * 2

print("Using NumPy Vectorization:")
print(vectorized_result)

