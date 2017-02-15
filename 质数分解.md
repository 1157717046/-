#include<stdio.h>
int main(){
	int i;
	int n;
	int x[15];
	int c=0;
	scanf("%d",&n);
	int isprime=n;
	for(i=0;i<16;i++){
		x[i]=1;
	}
	while(n>=2){
		for(i=2;i<=n;i++){
			if(n%i==0){
			x[c++]=i;
			n/=i;
			break;	
			}
		}
			if(n==isprime){
		 		break;
			}
	}
	if(n>2){
		printf("您所输入的数是素数"); 
	}
	else{
		printf("%d",x[0]);
	for(i=1;i<15;i++){
			if(x[i]>1){
				printf("x%d",x[i]);
		}
	}
}
	return 0;
} 
