# POTD-22-4-2024
**Row with minimum number of 1's**

class Solution {
    int minRow(int n, int m, int a[][]) {
        int min_ind=-1;
        int min_num=Integer.MAX_VALUE;
        for(int i=0;i<n;i++){
            int cnt=0;
            for(int j=0;j<m;j++){
                if(a[i][j]==1) cnt++;
            }
            if(cnt<min_num){
                min_num=cnt;
                min_ind=i;
            }
        }
        return min_ind+1;
    }
};


Input:
n = 4,m = 4
a = [[1, 1, 1, 1],
     [1, 1, 0, 0], 
     [0, 0, 1, 1],
     [1, 1, 1, 1]]
Output:
2
Explanation:
Rows 2 and 3 contain the minimum number 
of 1's(2 each).Since,row 2 is less than row 3.
Thus, the answer is 2.
