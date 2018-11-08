# BINARY-SEARCH
#include<stdio.h>
#include<conio.h>
int binarySearch(int arr[],int num,int size)
{
	int low,high,mid;
	  low=0;
	  high=size-1;
	  while(low<=high)
	{
		mid=(low+high)/2;
	if(arr[mid]==num)
	{
		return mid+1;
	}
	else if(arr[mid]>num)
	{
		high=mid-1;
	}
	else if(arr[mid]<num)
	{
		low=mid+1;
	}
	}
	return -1;
}
int main(void)
{
	int arr[12]={7,9,11,13,23,27,33,37,41,47,53,57},len,num,result;
	int target;
	printf("\n values in array:\t");
	for(len=0;len<=11;len++)
	{
		printf("%d\t",arr[len]);
	}
	printf("\nenter element to search\t");
	scanf("%d",&target);
	result = binarySearch(arr,target,12);
	if(result>=0)
	{
		printf("\n%d found at location %d",target,result);
	}
	else
	{
		printf("\n%d not found in array",target);
	}
	getch();
}
