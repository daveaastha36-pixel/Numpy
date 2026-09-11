1.
Create a NumPy array representing the number of likes on 7 Instagram posts and print its ndim, shape, size, dtype, itemsize, and nbytes properties.

***answer***
import numpy as np

# Number of likes on 7 Instagram posts
likes = np.array([120, 250, 180, 350, 420, 275, 500])

print("Array:", likes)
print("ndim:", likes.ndim)
print("shape:", likes.shape)
print("size:", likes.size)
print("dtype:", likes.dtype)
print("itemsize:", likes.itemsize, "bytes")
print("nbytes:", likes.nbytes, "bytes")

2.
Given a 2D NumPy array of daily step counts for 5 days (each row is a day, columns are morning and evening), use reshape() to convert it into a 1D array, then back to a 2D array with 5 rows and 2 columns.<br><br><em><strong>Hint:</strong> Use the shape attribute to check your array after each reshape.</em>

***answer***
import numpy as np

# Daily step counts for 5 days
# Columns: Morning, Evening
steps = np.array([
    [2500, 3500],
    [3000, 4000],
    [2800, 3700],
    [3200, 4200],
    [2900, 3800]
])

print("Original Array:")
print(steps)
print("Original Shape:", steps.shape)

# Convert 2D array into 1D array
one_d = steps.reshape(10)

print("\n1D Array:")
print(one_d)
print("1D Shape:", one_d.shape)

# Convert back to 2D array with 5 rows and 2 columns
two_d = one_d.reshape(5, 2)

print("\nBack to 2D Array:")
print(two_d)
print("2D Shape:", two_d.shape)

3.
Build a NumPy array representing the prices of 12 food items from a Zomato order, then use ravel(), flatten(), and resize() to create different shaped versions of the data and print each result.<br><br><em><strong>Constraint:</strong> Show the difference between ravel() and flatten() in your code comments.</em>

***answer***
import numpy as np

# Prices of 12 food items from a Zomato order
prices = np.array([
    120, 150, 80, 200,
    100, 250, 90, 180,
    130, 160, 70, 220
])

# Convert into a 3x4 array
food = prices.reshape(3, 4)

print("Original 3x4 Array:")
print(food)

# ravel() returns a flattened view whenever possible
ravel_result = food.ravel()
print("\nUsing ravel():")
print(ravel_result)

# flatten() always creates a new copy of the array
flatten_result = food.flatten()
print("\nUsing flatten():")
print(flatten_result)

# resize() changes the shape of the array itself
food.resize(4, 3)

print("\nUsing resize() - 4x3 Array:")
print(food)

4.
Take a 3x3 NumPy array representing a mini Spotify playlist grid (rows: playlists, columns: song counts in categories like Pop, Rock, Indie). Use both T and np.transpose() to swap rows and columns, then print the transposed array.

***answer***
import numpy as np

# Spotify playlist grid
# Rows = Playlists
# Columns = Pop, Rock, Indie
playlist = np.array([
    [20, 10, 15],
    [15, 25, 10],
    [30, 12, 18]
])

print("Original Playlist Grid:")
print(playlist)

# Transpose using T
transpose_T = playlist.T

print("\nTranspose using T:")
print(transpose_T)

# Transpose using np.transpose()
transpose_function = np.transpose(playlist)

print("\nTranspose using np.transpose():")
print(transpose_function)

5.
Given a 1D NumPy array of 15 Flipkart product ratings, use reshape() to convert it into a 3x5 array, then use flatten() to return it to a 1D array. Explain in a comment when you would use flatten() versus ravel() in real projects.


***answer***
import numpy as np

# 15 Flipkart product ratings
ratings = np.array([
    4, 5, 3, 4, 5,
    2, 4, 5, 3, 4,
    5, 4, 3, 5, 4
])

# Convert 1D array into 3x5 array
ratings_2d = ratings.reshape(3, 5)

print("3x5 Ratings Array:")
print(ratings_2d)

# Convert 3x5 array back to 1D using flatten()
ratings_1d = ratings_2d.flatten()

print("\nBack to 1D Array:")
print(ratings_1d)

# In real projects:
# Use flatten() when you need an independent copy.
# Use ravel() when you want a flattened view and better memory efficiency.
