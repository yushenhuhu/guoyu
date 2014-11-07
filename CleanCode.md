//A fifty-line clean code.

//This is a simple replacement of array.

#include<iostream>
#include<ctime>
#define lenth 4
using namespace std;
void print (int x[lenth][lenth]);
void product(int x[lenth][lenth]);
void main(){
    int a[lenth][lenth];
    product(a);
    print (a);
    cout<<endl;
    int i,j;
    for(i=0;i<lenth;i++){
        for(j=0;j<i;j++){
            int temp;
            temp=a[i][j];
            a[i][j]=a[j][i];
            a[j][i]=temp;
        }
    }
    print (a);
    cout<<endl;
}
void print (int x[lenth][lenth]){
    int i,j;
    for(i=0;i<lenth;i++){
        for(j=0;j<lenth;j++)
            cout<<x[i][j]<<' ';
        cout<<endl;
    }
}
void product(int x[lenth][lenth]){
    srand((unsigned)time(NULL));
    int i,j;
    for(i=0;i<lenth;i++)
        for(j=0;j<lenth;j++)
            x[i][j]=rand()%50;
}