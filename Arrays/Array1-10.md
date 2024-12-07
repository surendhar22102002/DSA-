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
    
    /* Return the Answer */
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


# 4 Remove Duplicates from Sorted Array [LeetCode ](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)


### Optimal Solution : 

 - Time Complexity - O(n)

 
```java
int removeDuplicate(int[] arr){  
    int j = 0;  
    for (int i = 1; i < arr.length; i++){  
        if (arr[i] != arr[j]){  
            j++;  
            arr[j] = arr[i];  
        }  
    }  
    return j + 1;  
}

```

___


# 5 Rotated Array [LeetCode ](https://leetcode.com/problems/rotate-array/)




### Optimal Solution : 

 - Time Complexity - O(n)
```java
 public static void rightRotated(int[] arr, int k){
        int size = arr.length;
        k = k % size;
        reverse(arr,0,size-1);
        reverse(arr,0,k-1);
        reverse(arr,k,size-1);
    }

    public static void reverse(int[] arr, int start, int end){
        while (start < end ){
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            start++;
            end--;
        }
    }
```

___




# 6 Move Zeroes [LeetCode ](https://leetcode.com/problems/move-zeroes/description/)




### Better Solution: 

 - Time Complexity - O(n²)

```java

 void moveZeros(int[] arr){  
    for (int i = 1; i < arr.length; i++){  
        for (int j = 0; j < arr.length-i; j++ ){  
            if (arr[j] == 0) {  
                int temp = arr[j];  
                arr[j] = arr[j +1];  
                arr[j+1] = temp;  
            }  
        }  
    }  
}
```


### Optimal  Solution :

 - Time Complexity - O(n)
```java 

void moveZeros(int[] nums){  
   int j = 0;  
   for (int i = 1; i < nums.length; i++){  
       if(nums[i] != 0){  
           int temp = nums[j];  
           nums[j] = nums[i];  
           nums[i] = temp;  
       }  
       if (nums[j] != 0){  
           j++;  
       }  
   }  
}
```


___




