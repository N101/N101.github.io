N101 Computer Science
=====================

## IB SL year 1
#### Bubble Sort
 
```javascript
static int[] selectionSort (int[] a) {
        for(int i=0; i<a.length-1; i++) {
            int min = i;
            for (int x=i+1; x<a.length; x++) {
                if (a[i] < a[min]) {
                    min = x;
                }
                int temp = a[min];
                a[min] = a[i];
                a[i] = a[temp];
            }
        }
        return a;
    }
```

