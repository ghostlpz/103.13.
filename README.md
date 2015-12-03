# 103.13.
// 
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main()
{
	int i,n,j,k;
	int arr[10];
	int len=10;
//	scanf("%d",&n);
	srand(time(NULL));
	for(i=0;i<len;i++)
	{
		arr[i]=rand()%10;
		printf("%d ",arr[i]);
	}
	printf("\n");
	for(i=0;i<len;i++)
		for(j=1+i;j<len;j++)
			if(arr[i]==arr[j])
			{
				for(k=j;k<len-1;k++)			
					arr[k]=arr[k+1];
				len--;
				j--;
			}
				
		
	for(i=0;i<len;i++)
	printf("%d ",arr[i]);

}
