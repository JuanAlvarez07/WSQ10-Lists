# WSQ10-Lists
#include <iostream>
#include <cstdlib>
#include <cmath>
using namespace std;

float Insert_Array_Value(float n){
  float value;
  cout<<"Please introduce a value: ";
  cin>>value;
  return value;
}

int Average(int list[], int size){
  int sum=0;
  for(int i=0;i<size;i++){
    sum=sum+list[i];
  }

  float average=sum/size;
  return average;
}
float Standard_deviation(int list[],int size)
{

  float mean_of_average=Average(list,size);
  float Num_subtract_mean=0;
  for(int i=0;i<size;i++)
  {
   Num_subtract_mean = ((list[i]-mean_of_average)*(list[i]-mean_of_average))+Num_subtract_mean;
  }
  float test = size-1;
  float Standard_dev = sqrt((Num_subtract_mean)/(test));
  return Standard_dev;

}

int main()
{
  int size,value;
  cout<<"Please introduce the size of the list: ";
  cin>>size;
  int list[size];

  for(int i=0;i<size;i++){
  list[i]= Insert_Array_Value(value);
  }

  cout<<"The average of the list is :"<<Average(list, size)<<endl;
  cout<<"The standard deviation of the list is: "<<Standard_deviation(list,size)<<endl;
  return 0;
}
