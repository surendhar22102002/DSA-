# 1 Largest Element in an Array  [GFG Link](https://www.geeksforgeeks.org/problems/largest-element-in-array4009/1)

```java
int LargestElementArray(int[] arr){  
    int maxElement = arr[0];  
    for (int i = 0; i < arr.length; i++){  
        if (arr[i] > maxElement) {  
            maxElement = arr[i];  
        }  
    }  
    return maxElement; 
}
```
___


# 2 Second Largest element in an array  [GFG Link](https://www.geeksforgeeks.org/problems/second-largest3735/1)

### Better Solution : 
 -  Time Complexity  - O(n²)

```java
int SecondLargestElementArray(int[] arr){  
    /* Find the first largest element */  
  int largest = arr[0];  
    for (int i = 0; i < arr.length; i++) {  
        if (arr[i] > largest){  
            largest = arr[i];  
        }  
    }  
    
    /* Find the second largest element*/  
  int secondLargest = -1;  
    for (int i = 0; i < arr.length; i++){  
        if (arr[i] > secondLargest && arr[i] != largest){  
            secondLargest = arr[i];  
        }  
    }  
    
    /* Return the Aswer */
    return secondLargest;  
}



```

### Optimal Solution : 

 - Time Complexity - O(n)
```java
int SecondLargestElementArray(int[] arr){  
    int largest = arr[0];  
    int secondLargest = -1;  
  
    for (int i = 0; i < arr.length; i++){  
        if (arr[i] > largest){  
            secondLargest = largest;  
            largest = arr[i];  
        } else if (arr[i] < largest && arr[i] > secondLargest) {  
            secondLargest = arr[i];  
        }  
    }  
    return secondLargest;  
}




```

___


# 3 Check if array is sorted [GFG Link](https://www.geeksforgeeks.org/problems/check-if-an-array-is-sorted0701/1)

### Optimal Solution : 
 -  Time Complexity  - O(n)

```java
boolean ArraySortedOrNot(int[] arr){  
  
    for (int i = 1; i < arr.length; i++){  
        if (arr[i] >= arr[i-1]){  
        }else {  
            return false;  
        }  
    }  
   return true;  
}


```

___

