#include<stdio.h>
int main(){
int t[10][10],i,j,d,k;
d=1;
k=0;
for(i=1;i<=4;i++){
 for(j=1;j<=4;j++){
t[i][j]=d++;
 }
}

for(i=1;i<=4;i++){
 for(j=1;j<=4;j++){
  if(i!=j && j>i){
    k=t[i][j];
    t[i][j]=t[j][i];
    t[j][i]=k;
  }
 }
}

for(i=1;i<=4;i++){
 for(j=1;j<=4;j++){
printf("%d|\t",t[i][j]);
 }
 printf("\n");
}

return 0;
}
