# Experiment-5
## AIM:Write a python program for Binary Search and inspect for failures. 

# ALGORITHM
Start the program.
2. Get the list from the user
3. Get the element to be searched
4. Compare the mid element with the key, if same return the index
5. If key is greater, search it in the right side, else search it in the left side.
6. If not found return -1
 7. Stop the program. 

 # PROGRAM
```
def binary_search(arr, x):
    low = 0
    high = len(arr) - 1
    mid = 0

    while low <= high:
        mid = (high + low) // 2

        if arr[mid] < x:
            low = mid + 1
        elif arr[mid] > x:
            high = mid - 1
        else:
            return mid  # Fixed return value

    return -1  # Moved return -1 outside the loop


arr = [2, 3, 4, 10, 40]

try:
    x = int(input("Enter the element to be searched: "))  # Fixed quotes
    result = binary_search(arr, x)

    if result != -1:
        print("Element is present at index", str(result))
        print("Test Case:Pass")
    else:
        print("Element is not present in array")
        print("Test Case:Pass")

except ValueError:  # Catching specific exception
    print("Enter a valid input!")
    print("Test Case:Fail")

```
 # OUTPUT

<img width="1476" height="646" alt="image" src="https://github.com/user-attachments/assets/f400cf6f-4bd7-4f44-917a-01077255f609" />

 # RESULT

Thus, the python program of binary search is implemented and the output is verified successfully.
