# Lpuquiz_challenge1

#include<iostream>
using namespace std;
int main()
{
    int n,i,j,l,b,area,max1=0;
    cin>>n;
    int length[n];
    for(i=0;i<n;i++)
    {
        cin>>length[i];
    }
    for(i=0;i<n-1;i++)
    {
        for(j=i+1;j<n;j++)
        {
            if(length[i]>length[j])
            {
                b=length[j];
                l=j-i;
                area=l*b;
                if(max1<area)
                {
                    max1=area;
                }
            }
            else
            {
                b=length[i];
                l=j-i;
                area=l*b;
                if(max1<area)
                {
                    max1=area;
                }
            }
        }
    }
    cout<<max1;
}
