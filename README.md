# Magnified-X

Magnified X

Problem Description

请你编程画一个放大的’X’。

如3*3的’X’应如下所示：

X X

 X
 
X X


5*5的’X’如下所示：

X   X

 X X
 
  X
  
 X X
 
X   X

Input

输入数据第一行是一个整数T，表示有T组测试数据；

接下来有T行，每行有一个正奇数n（3 <= n <= 79），表示放大的规格。

Output

对于每一个n打印一个规格为n * n放大的’X’；每组输出后面空一行。

Sample Input

2 3 5

Sample Output

X X X X X X X X X X X X X X


代码：

#include <cstdlib> 
  
#include <iostream> 
  
using namespace std; 

int main(int argc, char *argv[]) 

{ 

    int a,n,t;     
    
    int i,j,k,i1; 
    
    cin>>t; 
    
    for(i1=0;i1<t;i1++)
    
    { 
    
    cin>>n; 
    
    a=n/2+1; 
    
    for(i=1;i<=a;i++) 
    
    { 
    
        for(k=1;k<=(i-1);k++) 
        
            cout<<" "; 
            
        for(j=1;j<=(2*a+1-2*i);j++) 
        
        { 
        
            if(j==1 || j==2*a+1-2*i)cout<<"X"; 
            
            else cout<<" "; 
            
        } 
        
        cout<<'\n'; 
        
    } 
    
    for(i=2;i<=a;i++) 
    
    { 
    
        for(k=1;k<=(a-i);k++) 
        
            cout<<" "; 
            
        for(j=1;j<=(2*i-1);j++) 
        
        { 
        
            if(j==1 || j==2*i-1)cout<<"X"; 
            
            else cout<<" "; 
            
        } 
        
        cout<<endl; 
        
    } 
    
    cout<<endl; 
    
    } 
    
    return EXIT_SUCCESS; 
    
} 

