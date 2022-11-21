1 .py
Class Solution:
     def solve(self , n):
           sign = ‘-‘ if n<0 else ‘ ’
            n=abs(n)
            if  n < 3:
                 return str(n)
                 s =’ ‘
            while n !=0:
                 s =str(n%3) + s
                 n =n//3
           return sign+s
ob= Solution()
n=int(input())
print(ob.solve(n))


2.question
 
 2.py
n=input()
a=input()
x=a[-1]
print(n.count(x))

3.py

int helper(vector<vector<int>> & mat, int a, int b) {
        
        int m = mat.size();
        int n = mat[0].size();
        int count = 0;
        int bound = n;
        
        for (int i=a; i<m; i++) {
            for (int j=b; j<bound; j++) {
                if (mat[i][j]) count += 1;
                else bound = j;
            }
        }
        
        return count;

    }

    int numSubmat(vector<vector<int>>& mat) {
        
        int m = mat.size();
        int n = mat[0].size();
        int count = 0;
        
        for (int i=0; i<m; i++) {
         for (int j=0; j<n; j++) {
                count += helper(mat, i, j);
            }
        }
        
        return count;

    }
