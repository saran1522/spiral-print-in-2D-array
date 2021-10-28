#include<bits/stdc++.h>
using namespace std;
int main(){
  int arr[100][100], m, n;// rs, re, cs, ce, count;
  cout<<"enter the no of rows and colums: ";
  cin>>n>>m;
  for (int i = 0; i < n; i++)
  {
    for (int j = 0; j < m; j++)
    {
      cin>>arr[i][j];
    }
    
  }
  int rs=0, re=n-1, cs=0, ce=m-1, count=0, i=0, j=0;
  while (count<m*n)
  {
      if (i==rs)
      {
          while (j<=ce)
          {
              cout<<arr[i][j]<<" ";
              j++;
              count++;
          }
          i=++rs;
          j=ce;
      }
      if (j==ce)
      {
          while (i<=re)
          {
            cout<<arr[i][j]<<" ";
            i++;
            count++;
          }
         j=--ce;
         i=re; 
      }
      if (i==re)
      {
          while (j>=cs)
          {
              cout<<arr[i][j]<<" ";
              j--;
              count++;
          }
          i=--re;
          j=cs;
      }
      if (j==cs)
      {
          while (i>=rs)
          {
            cout<<arr[i][j]<<" ";
            i--;
            count++;
          }
          j=++cs;
          i=rs;
      }
  }
  
  return 0;
}