
/*
Row Increment - Last Element Unit Digit
The program must accept an integer matrix of size R*C as input. Then the elements in a given row must be incremented by the value of the unit
digit of the last element in that specific row. Finally the program must print the revised matrix values.
Boundary Condition(s):
1 <= R, C <= 100
Input Format:
The first line contains the value of R and C separated by space(s).
The next R lines contain C integers separated by space.
Output Format:
R lines each containing C integers modified as per the given conditions.
Example Input/Output 1:
Input:
3 4
10 12 13 15
23 88 12 42
99 89 79 11
Output:
15 17 18 20
25 90 14 44
100 90 80 12

*/#include <iostream>
 
using namespace std;

int main(int argc, char** argv)
{
    int i,j,n,m,a[1000][1000],b[1000];
    cin>>n>>m;
    for(i=1;i<=n;i++)
    {
        for(j=1;j<=m;j++)
        {
            cin>>a[i][j];
        }
    }
    for(i=1;i<=n;i++)
    {
        b[i]=a[i][m]%10;
    }
    for(i=1;i<=n;i++)
    {
        for(j=1;j<=m;j++)
        {
            cout<<a[i][j]+b[i]<<" ";
        }
        cout<<"\n";
    }


}
