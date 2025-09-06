# PA2---Dangiwan

# NORMALIZATION PROBLEM
``` python
import numpy as np
#accessing functions from the numpy library and calling it as np

X = np.random.random((5,5))
#creating a 5x5 array with random values using the random function 
z = np.mean(X)
#calculating the average of all the values using np.mean()
v = np.std(X)
#calculating the standard deviation using np.std()

normalized = (X-z)/v
#calculating the normalized data by deducting the mean from the X array and dividing by the standard deviation

np.save('X_normalized', normalized)
#saving the normalized array into an .npy file called 'X_normalized'

Normalized_Data = np.load('X_normalized.npy')
#reads the data in 'X.normalized.npy', loads and saves it to 'Normalized_Data'

print(Normalized_Data)
#printing the result saved on 'Normalized_Data'
```

# DIVISIBLE BY 3 PROBLEM
``` python
import numpy as nd
#accessing the numpy library and calling it as nd

w = nd.arange(1,101,1)
#creating a 1d array containing the numbers 1-100 by starting the array by 1, 
#incrementing by 1 up to 100 excluding the terminal value 101
#data is stored in w
y = nd.arange(1,101,1)
#creating another 1d array with the same elements as array w
n = w * y
#element-wise multiplication of the array w and array y to get their squares
#storing the data in n
j = n.reshape(10,10)
#reshaping the data in n into a 10x10 array and storing it in j
print(j)
#printing the reshaped array j


print("\nThe numbers divisible by 3 are:")
#label for the list of the numbers divisible by 3)
divisible = [] 
#making a list named 'divisible' to store the numbers divisible by 3
for k in n:
#a for loop to check for divisibility for each element in n
    if k % 3 == 0:
    #determining if the value of k is divisible by 3 through modulo
        divisible.append(k)
        #adding the last element divisible by 3 to the list
        
nd.save('div_by_3', divisible)
#saving the values within the list divisible as a .npy file named 'div_by_3'
b = nd.load('div_by_3.npy')
#reading the .npy file, loading it and storing it into b
print(b)
#print the values in b
```
