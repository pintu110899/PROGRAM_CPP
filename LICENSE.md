/******************************************************************************

Welcome to GDB Online.
GDB online is an online compiler and debugger tool for C, C++, Python, PHP, Ruby, 
C#, VB, Perl, Swift, Prolog, Javascript, Pascal, HTML, CSS, JS
Code, Compile, Run and Debug online from anywhere in world.

*******************************************************************************/
#include <stdio.h>
#include<bits/stdc++.h>
using namespace std;
int RBinsearch(int a[],int l,int h,int key)
{
    int mid;
    if(l<=h)
    {
        mid=(l+h)/2;
        if(mid==key)
        {
            return mid;
        }
        else if(key>mid)
        {
            //l=mid+1;
            return RBinsearch(a,mid+1,h,key);
        }
        else 
        {
           // h=mid-1;
           return RBinsearch(a,l,mid-1,key);
           
        }
    }
    return -1;
}
int main()
{
    int arr[]={2,3,4,5,6,7,8,9};
    //int l=0;
   // int h=arr.length-1;
   int key1;
   cin>>key1;
    int result=RBinsearch(arr,0,sizeof(arr)/sizeof(arr[0]),key1);
    if(key1==result)
    cout<<"key found "<<key1;
    else
    cout<<"KEY NOT FOUND";
    //cout<<result;
    //printf("Hello World");

    return 0;
}
