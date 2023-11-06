fibonacci series (recursion)

def recur_fibo(n):  
   if n <= 1:  
       return n  
   else:  
       return(recur_fibo(n-1) + recur_fibo(n-2))  
# take input from the user  
nterms = int(input("How many terms? "))  
# check if the number of terms is valid  
if nterms <= 0:  
   print("Plese enter a positive integer")  
else:  
   print("Fibonacci sequence:")  
   for i in range(nterms):  
       print(recur_fibo(i))  
-------------------------------------------------------------------

# Program to display the Fibonacci sequence up to n-th term

nterms = int(input("How many terms? "))

# first two terms
n1, n2 = 0, 1
count = 0

# check if the number of terms is valid
if nterms <= 0:
   print("Please enter a positive integer")
# if there is only one term, return n1
elif nterms == 1:
   print("Fibonacci sequence upto",nterms,":")
   print(n1)
# generate fibonacci sequence
else:
   print("Fibonacci sequence:")
   while count < nterms:
       print(n1)
       nth = n1 + n2
       # update values
       n1 = n2
       n2 = nth
       count += 1
------------------------------------------------------------------
#count fibonacci
def countFibs(low, high):
     
    # Initialize first three 
    # Fibonacci Numbers
    f1, f2, f3 = 0, 1, 1
 
    # Count fibonacci numbers in 
    # given range
    result = 0
 
    while (f1 <= high):
        if (f1 >= low):
            result += 1
        f1 = f2
        f2 = f3
        f3 = f1 + f2
 
    return result
 
# Driver Code
low, high = 10, 100
print("Count of Fibonacci Numbers is", 
                 countFibs(low, high))

----------------------------------------------------------------

#fractional knapsack
# Structure for an item which stores weight and
# corresponding value of Item
class Item:
	def __init__(self, profit, weight):
		self.profit = profit
		self.weight = weight

# Main greedy function to solve problem
def fractionalKnapsack(W, arr):

	# Sorting Item on basis of ratio
	arr.sort(key=lambda x: (x.profit/x.weight), reverse=True) 

	# Result(value in Knapsack)
	finalvalue = 0.0

	# Looping through all Items
	for item in arr:

		# If adding Item won't overflow, 
		# add it completely
		if item.weight <= W:
			W -= item.weight
			finalvalue += item.profit

		# If we can't add current Item, 
		# add fractional part of it
		else:
			finalvalue += item.profit * W / item.weight
			break
	
	# Returning final value
	return finalvalue


# Driver Code
if __name__ == "__main__":
	W = 50
	arr = [Item(60, 10), Item(100, 20), Item(120, 30)]

	# Function call
	max_val = fractionalKnapsack(W, arr)
	print(max_val)
------------------------------------------------------------------
#0 1 knapsack problem using dp
# A Dynamic Programming based Python 
# Program for 0-1 Knapsack problem 
# Returns the maximum value that can 
# be put in a knapsack of capacity W 
def knapSack(W, wt, val, n): 
	K = [[0 for x in range(W + 1)] for x in range(n + 1)] 

	# Build table K[][] in bottom up manner 
	for i in range(n + 1): 
		for w in range(W + 1): 
			if i == 0 or w == 0: 
				K[i][w] = 0
			elif wt[i-1] <= w: 
				K[i][w] = max(val[i-1] + K[i-1][w-wt[i-1]], K[i-1][w]) 
			else: 
				K[i][w] = K[i-1][w] 

	return K[n][W] 

# Driver program to test above function 
val = [60, 100, 120] 
wt = [10, 20, 30] 
W = 50
n = len(val) 
print(knapSack(W, wt, val, n)) 

---------------------------------------------------------------------
# QuickSort

# Function to find the partition position
def partition(array, low, high):

	# choose the rightmost element as pivot
	pivot = array[high]

	# pointer for greater element
	i = low - 1

	# traverse through all elements
	# compare each element with pivot
	for j in range(low, high):
		if array[j] <= pivot:

			# If element smaller than pivot is found
			# swap it with the greater element pointed by i
			i = i + 1

			# Swapping element at i with element at j
			(array[i], array[j]) = (array[j], array[i])

	# Swap the pivot element with the greater element specified by i
	(array[i + 1], array[high]) = (array[high], array[i + 1])

	# Return the position from where partition is done
	return i + 1

# function to perform quicksort


def quickSort(array, low, high):
	if low < high:

		# Find pivot element such that
		# element smaller than pivot are on the left
		# element greater than pivot are on the right
		pi = partition(array, low, high)

		# Recursive call on the left of pivot
		quickSort(array, low, pi - 1)

		# Recursive call on the right of pivot
		quickSort(array, pi + 1, high)


data = [1, 7, 4, 1, 10, 9, -2]
print("Unsorted Array")
print(data)

size = len(data)

quickSort(data, 0, size - 1)

print('Sorted Array in Ascending Order:')
print(data)
