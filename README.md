#include<stdio.h>
int dectobin(int n){
	int str[100000],count=0,i=0;
	while(n>0){
		int a=n%2;
		str[i]=a;
		n=n/2;
		i++;
		count++;
	}
	int str2[count];
	for(int i=0;i<count;i++){
		str2[count-1-i]=str[i];
	}
	for(int j=0;j<count;j++){
		printf("%d",str2[j]);
	}
}
int dectooct(int n){
	int str[100000],count=0,i=0;
	while(n>0){
		int a=n%8;
		str[i]=a;
		n=n/8;
		i++;
		count++;
	}
	int str2[count];
	for(int i=0;i<count;i++){
		str2[count-1-i]=str[i];
	}
	for(int j=0;j<count;j++){
		printf("%d",str2[j]);
	}
}
int dectohex(int n){
	int str[100000],count=0,i=0;
	while(n>0){
		int a=n%16;
		str[i]=a;
		n=n/16;
		i++;
		count++;
	}
	int str2[count];
	for(int i=0;i<count;i++){
	str2[count-1-i]=str[i];
		str2[count-1-i]=str[i];
	}
	for(int j=0;j<count;j++){
		printf("%d",str2[j]);
	}

}
int main(){
	int n,a,count=0;
	printf("click 1 to convert decimal to binary\n");
	printf("click 2 to convert decimal to octal\n");
	printf("click 3 to convert decimal to hexadecimal\n");
	scanf("%d",&a);
	printf("enter the decimal number you want to convert\n");
	scanf("%d",&n);
	if(a==1){
		dectobin(n);
	}
	if(a==2){
		dectooct(n);
	}
	if(a==3){
		dectohex(n);
	}
	return 0;
}



