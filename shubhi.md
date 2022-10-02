###Shubhankshi Saraf
img-https://imgur.com/gCMm5S4
Location-India
Github Profile-https://github.com/shubhi0222

#include <iostream>
using namespace std;

void quickSort(int a[], int first, int last){
    int pivot,i,j,temp;
    if(first<last){
        i=first;
        j=last;
        pivot=first;

        while(i<j){
            while(a[i] <= a[pivot] && i<last){
                i++;
            }
            while(a[j]>a[pivot]){
                j--;
            }
            if(i<j){
                temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
        }
        temp=a[pivot];
        a[pivot]=a[j];
        a[j]=temp;
        quickSort(a,first,j);
        quickSort(a,j+1,last);
    }
}

int main(){
    int a[]={9,4,7,6,2,23,53,32,76,43};
    quickSort(a,0,9);
    for (int i = 0; i < 10; i++)
    {
        cout<<a[i]<<" ";
    }
    return 0;
}
