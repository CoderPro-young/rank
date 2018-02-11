#include<stdio.h>
#include<string.h>


void deal(int n,char str[]);

void rank(int n,char ch[]);

void swap(char str[],int x,int y);
int length=0;//字符串的长度 
//int cnt;
int main()
{
	char ch[7];
	scanf("%s",ch);
	
	length=strlen(ch);
	rank(length,ch); 
	//printf("%d",cnt);
	return 0;
}
/*从前到后依次将每个字母放到首位，并递归地对后面的序列进行排序*/
/*将第n个字母放到首位*/
void deal(int n, char str[])
{
	if (n == 0) {
		return;
	}
	int i = 0;
	int j = 0;
	char c;
	/*for (i = 0; i<n; i++) {
		c = str[0];//this step can not be ignored
		for (j = 0; j<length - 1; j++) {
			str[j] = str[j + 1];
		}
		str[length - 1] = c;
	}
	*/
	c = str[n];
	for (i = n ; i > 0; i--) {
		str[i] = str[i - 1];
	}
	str[0] = c;
	return;

}
/*对给定字符串后n位进行排序*/
void rank(int n,char ch[])
{
	//int n=strlen(ch);
	if(n==1){
		printf("%s",ch);
		//cnt++;
	}
	if(n==2){
		printf("%s\n",ch); 
		swap(ch,length-1,length-2);
		printf("%s\n",ch); 
	//	cnt+=2;
		return ;
	}
	int i=0;
	int j=0;
	for(i=0;i<n;i++){
		char str[7];
	    strcpy(str,ch);
	    //将每个字母放到首位 
	    deal(i,str);
	    rank(n-1,str);//对后面的部分递归排序 
	}
	
	
}
void swap(char str[],int x,int y)
{
	char c;
	c=str[x];
	str[x]=str[y];
	str[y]=c;
}

