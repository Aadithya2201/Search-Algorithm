# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
#Program for linear search method to match the item in a list
#Developed by:Aadithya.R
#RegisterNumber: 23006361

def linearSearch(array,n,k):
    array=sorted(array)
    for i in range(0,n):
        if(k==array[i]):
            return i
    
array = eval(input())
print(sorted(array))
k = eval(input()) 
n=len(array)
result=linearSearch(array,n,k)
if(result==None):
    print("Element not found")
else:
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
#Program to find the element in a list using Binary Search(Iterative Method)..
#Developed by:Aadithya.R
#RegisterNumber: 23006361

def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
    
array = eval(input())
array.sort()
k = int(input()) 
low=0
high=len(array)-1
result=binarySearchIter(array, k, low, high)
print(array)
if(result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Aadithya.R
RegisterNumber: 23006361
'''
def BinarySearch(array, k, low, high):
    if low<=high:
        mid=(high+low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return BinarySearch(array, k, low, mid-1)
        else:
            return BinarySearch(array, k,  mid+1, high)
    else:
        return -1
    
array = eval(input())
array.sort()
print(array)
k = eval(input()) 
low=0
high=len(array)-1
result=BinarySearch(array, k, low, high)
if(result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)
```
## Sample Input and Output
![Screenshot 2023-12-28 154253](https://github.com/Aadithya2201/Search-Algorithm/assets/145917810/6e9a2548-2cc9-4b0b-9f34-8434bdaf8e13)

![Screenshot 2023-12-28 154310](https://github.com/Aadithya2201/Search-Algorithm/assets/145917810/1a5fd164-315e-4830-8589-3cabed144495)

![Screenshot 2023-12-28 154333](https://github.com/Aadithya2201/Search-Algorithm/assets/145917810/97f2835e-81c2-47aa-b6bf-ed9832ad3b9c)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
