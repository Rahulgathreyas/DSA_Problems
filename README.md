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
