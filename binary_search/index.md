# Binary Search


```java
public boolean binary_search (int[] arr, int tar){
  // [T,T,T,T,F,F,F] to find first false.
  // [1,2,3,4,5,5,7] find first (num < 5) -> check statement
  int n = arr.length;
	int l = 0;
  int r = n; // let right boundary inaccessible
  while(l<r){
    int mid = (l+r)/2;
    if(arr[mid] < tar){ 
      // if check() == true, we don't need this mid in our range
			l = mid + 1;
    } else {
      // if false, right boundary can still be mid cuz l will stop when it meets r
			r = mid;
    }
  }
  return l;
}
```


