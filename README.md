# CNS
//defihellman
#include<stdio.h>
int power(int base,int exp,int mod){
	int result=1;
	for(int i=0;i<exp;i++){
		result=(result*base)%mod;
		}
	return result;
}
int main(){
	int q,g,xa,xb,ya,yb;
	int s1,s2;
	q=7,g=3,xa=6,xb=3;
	ya=power(g,xa,q);
	yb=power(g,xb,q);
	s1=power(yb,xa,q);
	s2=power(ya,xb,q);
	printf("%d,%d,%d,%d\n",ya,yb,s1,s2);
	if(s1==s2){
		printf("key is:%d",s1);
	}
	else{
		printf("key exchange failed");
	}
}
