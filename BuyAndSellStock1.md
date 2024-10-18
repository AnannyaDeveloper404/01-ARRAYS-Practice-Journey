# Best Time to Buy and Sell Stock

```java
class Solution {
    public int maxProfit(int[] arr) {
        int maxProfit=0;
        int l=0;
        int r=1;
        while(l<arr.length && r<arr.length){
            if(arr[l]>=arr[r]){
                l=r;
                r++;
            }else if(arr[l]<arr[r]){
                maxProfit=Math.max(maxProfit,arr[r]-arr[l]);
                r++;
            }
        }
        return maxProfit;
    }
}
```

## Approach:

- It made use of two pointer
