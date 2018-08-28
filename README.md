N101 Computer Science
=====================

## IB SL year 1
#### Bubble Sort
  > A simple sorting algorithm to run through a list of numbers and sort them from smallest to largest
 
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

#### Selection Sort
 > Another sorting algorithm, but a bit more efficient than the Bubble Sort method as it takes the min value and then 
 > places it at its corresponding spot.

```javascript
static int[] selectionSort (int[] a) {
        for(int i=0; i<a.length; i++) {
            int minPos = getMinPos(a, i);
            int temp = a[i];
            a[i] = a[minPos];
            a[minPos] = temp;
        }
        return a;
    }
    
    private static int getMinPos(int[] a, int start) {
        int min = a[start];
        int minPos = start;
        for (int i=start; i<a.length; i++) {
            if (a[i] < min) {
                min = a[i];
                minPos = i;
            }
        }
        return minPos;
    }
```

