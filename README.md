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
''' 
Program for linear search method to match the item in a list
Developed by: P.Jeshwanth Kumar
RegisterNumber: 23002519
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if (array[i]==k):
            return i
    return -1
    
    
array = eval(input())
array.sort()
n=len(array)
# sort the array
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
result = linearSearch(array,n,k)# use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: P.Jeshwanth kumar
RegisterNumber: 23002519
'''
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
k = eval(input())
result=binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
    





```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: P.Jeshwanth Kumar
RegisterNumber: 23002519
'''
def BinarySearch(arr, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return BinarySearch(array,k,low,mid-1)
        else:
            return BinarySearch(array,k,mid+1,high)
    return -1
    
   
    
    
array = eval(input())
array.sort()
k = eval(input()) 
result=BinarySearch(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
    

# use the binary search function to find the result

# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result




```
## Sample Input and Output
i.
![image](https://github.com/Jeshwanthkumar07/Search-Algorithm/assets/142886483/82817b5d-6d5b-4d63-9da5-d1576798e3a4)

ii.
![image](https://github.com/Jeshwanthkumar07/Search-Algorithm/assets/142886483/a45205f2-e112-494c-9a7e-0a44e6becde4)

iii.
![image](https://github.com/Jeshwanthkumar07/Search-Algorithm/assets/142886483/40b499b7-01d6-4678-9835-bf3b7ea470bf)









## Result
Thus the linear search and binary search algorithm is implemented using python programming.
