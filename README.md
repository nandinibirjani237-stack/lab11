# lab11
#include<stdio.h>

struct patient{
    char name[50];
    int id,age;
float fee;
};
int main(){
    struct patient p;
    printf("enter patient ID\n");
    scanf("%d",&p.id);
    printf("enter patient name\n");
    scanf(" %[^\n]",p.name);
    printf("enter patient age\n");
    scanf("%d",&p.age);
    printf("enter consultation fee\n");
    scanf("%f",&p.fee);
    
    printf("%d\n",p.id);
    printf("%s\n",p.name);
    printf("%d\n",p.age);
    printf("%f\n",p.fee);
}
# task2
#include<stdio.h>
struct room{
    int number;
    char type[30];
    int occupants;
    float rent;
};
int main(){
    struct room r[5];
    float total=0;
    for(int i=0;i<5;i++){
printf("room number\n");
scanf("%d",&r[i].number);
printf("room type\n");
scanf(" %[^\n]",r[i].type);
printf("occupants\n");
scanf("%d",&r[i].occupants);
printf("rent\n");
scanf("%f",&r[i].rent);
total+=r[i].rent;
    }
    for(int i=0;i<5;i++){
        printf(" room %d \t number %d \t type %s \t occupants %d \t rent %.2f",i+1,r[i].number,r[i].type,r[i].occupants,r[i].rent);
       
       
}
 printf("%.2f\n",total);
}

# task3
#include<stdio.h>
struct Customer{
    char name[50];
    int id;
float unit,rate;
};
void calculate(struct Customer p){

printf("%d\n",p.id);
printf("%s\n",p.name);
printf("%.2f\n",p.unit);
printf("%.2f\n",p.rate);
float bill=p.rate*p.unit;
printf("%.2f\n",bill);
};
int main(){
    struct Customer p;
    printf("enter patient ID\n");
    scanf("%d",&p.id);
    printf("enter patient name\n");
    scanf(" %[^\n]",p.name);
     printf("enter units\n");
    scanf("%f",&p.unit);
    printf("enter rate\n");
    scanf("%f",&p.rate);
calculate(p);

}
# task 4
#include<stdio.h>
#include<string.h>

struct owner{
    int id;
    char name[60];
char number[12];
};
struct vehicle{
char number[20];
char model[50];
int year;
struct owner o;
};
int main(){
    struct vehicle v;
    struct vehicle *ptr;
    ptr=&v;
    printf("enter vehicle registration number");
scanf("%s",ptr->number);
printf("enter vehicle model");
scanf("%s",ptr->model);
printf("enter year" );
scanf("%d",&ptr->year);
printf("enter id");
scanf("%d",&ptr->o.id);

printf("enter  Owner Name");
scanf("%s",ptr->o.name);

printf("enter  Owner contact");
scanf("%s",ptr->o.number);
printf("registration number %s\n",ptr->number);
printf(" vehicle model %s\n",ptr->model);
printf(" id %d\n",ptr->o.id) ;
printf("year  %d\n",ptr->year );
printf(" name %s\n",ptr-> o.name);
printf(" number %s\n",ptr-> o.number);

}
# task 5
#include<stdio.h>
#include<string.h>
struct dep{
    int depid;
    char depname[50];
    int enrolledstudent;
    struct head{
        int empid;
        char name[50];
char designation[50];

    }head;
};
int main(){
    struct dep d;
    printf("enter department id");
    scanf("%d",&d.depid);
    printf("enter department name");
    scanf("%s",d.depname);
    printf("enter number of enrolled students");
    scanf("%d",&d.enrolledstudent);
    printf("enter head emp id");
    scanf("%d",&d.head.empid);
     printf("enter head designation)");
    scanf("%s",d.head.designation);
 printf("enter head emp name");
    scanf("%s",d.head.name);

printf("department ID     %d\n", d.depid);
    printf("department name   %s\n", d.depname);
    printf("enrolled students %d\n", d.enrolledstudent);
    printf("head employee id %d\n", d.head.empid);
    printf("head name         %s\n", d.head.name);
    printf("head designation  %s\n", d.head.designation);
}
# task 6
#include<stdio.h>
#include<string.h>
int multiply(int a,int b){
    if(b==0) return 0;
    return a+multiply(a,b-1);
}
int main(){
    int num1,num2;
    printf("enter num1");
scanf("%d",num1);
 printf("enter num2");
scanf("%d",num2);
int result=multiply(num1,num2);
printf("%d %d %d",num1,num2,result);
}
# task 7
#include<stdio.h>
#include<string.h>
void even(int index,int size,int arr[]){
    if(index==size){
        return;
    }
    if(arr[index]%2==0){
        printf("%d",arr[index]);
    }
    even( index+1, size, arr);
}
int main(){
    int arr[10];
    printf("enter 10 numbers");
    for (
        int i = 0; i < 10; i++)
    {
       scanf("%d",&arr[i]);
    }
    printf(0,10,arr);

}
# task 8
#include<stdio.h>
#include<string.h>
 
float calculateSum(int n){
    if(n==0) return 0;
    return n+calculateSum(n-1);
}
int main(){
    int num;
   
    printf("enter number");
    scanf("%d",&num);
int sum=calculateSum(num);
printf("%d",sum);

}
