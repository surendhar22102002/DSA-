# 1 Largest Element in an Array  
#### [Geeks For Geeks Link](https://www.geeksforgeeks.org/problems/largest-element-in-array4009/1)

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
