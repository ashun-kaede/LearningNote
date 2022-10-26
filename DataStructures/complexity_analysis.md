# Complexity Analysis
## Big-O notation
Big-O notation gives an upper bound of the complexity in the WORST case, helping to quantify performance as the input size becomes arbitrarily large. 

- Constant Time: O(1)
- Logarithmic Time: O(log(n))
- Linear Time: O(n)
- Linearithmic Time: O(nlog(n))
- Quadric Time: O(n^2)
- Cubic Time: O(n^3)
- Exponential Time: O(b^n), b>1
- Factorial Time: O(n!)

## Example

### Contant O(n)
```pascal
i := 0
While i<n Do
    i = i + 3

//f(n) = 3/n
//O(f(n)) = O(n)
```
### Quadric O(n^2)
```pascal
For(i:=0; i<n; i=i+1)
    For(j:=0; j<n; j+1)

//O(f(n)) = O(n^2)
```

### Logarithmic O(log(n))
Here is a code to find index of a particular value in the sorted array.

```pascal
low := 0
high := n-1
while low<=high Do
    mid := (low + high)/2

    If array[mid] == value: return mid
    Else If array[mid] < value: low = mid + 1
    Else If array[mid] > value: high = mid - 1

//f(n) = log2(n)
//O(n) = O(log(n))
```

### More complex situation:
```pascal
i := 0
While i<n Do
    j = 0
    While j < 3*n Do
        j = j + 1
    j = 0
    While j < 2*n Do
        j = j + 1
    i = i + 1

//f(n) = n*(3n+2n) = 5n^2
//O(f(n)) = O(n^2)
```

