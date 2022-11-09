# DSA_Problems
#include <stdio.h>
struct student {
    int R_no;
    char name[10];
    int marks;
};
void main() {
    int n,max,itr,pos;
    printf("Enter the number of students\n");
    scanf("%d",&n);
    struct student st[n];
    printf("Enter the details of students\n");
    for(itr=0; itr<n; itr++)
    {
        scanf("%d%s%d",&st[itr].R_no,st[itr].name,&st[itr].marks);
    }
    
    printf("The students with maximum marks is:\n");
    for(itr=1; itr<n; itr++)
    {
        max=st[0].marks;
        if(st[itr].marks>max)
        {
            max=st[itr].marks;
            pos=itr;
        }
    }
    printf("ROLL_NO=%d\nName=%s", st[pos].R_no,st[pos].name);
}
//Problem_1
#include <stdio.h>
#define SIZE 3
struct student{
        int R_no;
        char name[20];
        int marks1,marks2,marks3;
    };
int main() {
    struct student st[SIZE];
    int n,itr;
    printf("Enter the details in the order of R_no,name,marks1,marks2,marks3\n");
    for(itr=0; itr<SIZE; itr++)
    {
        scanf("%d\n %s\n %d \n %d\n%d\n",&st[itr].R_no,st[itr].name,&st[itr].marks1,&st[itr].marks2,&st[itr].marks3);
    }
    printf("The details are\n");
      for(itr=0; itr<SIZE; itr++)
    {
        printf("ROLL_NO:%d\nNAME:%s\nMARKS1:%d\nMARKS2:%d\nMARKS3:%d\n",st[itr].R_no,st[itr].name,st[itr].marks1,st[itr].marks2,st[itr].marks3);
    }
    int sum=0,avg=0;
    sum=st[itr].marks1+st[itr].marks2+st[itr].marks3;
    avg=sum/SIZE;
    if(avg>90 && avg<100)
        printf("S\n");
    else if(avg>70 && avg<=90)
        printf("A\n");
    else if(avg>50 && avg<=70)
        printf("B\n");
    else    printf("F\n");
    return 0;
}
