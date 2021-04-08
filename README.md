#include<stdio.h>
//the function to compute the average and print the result
void average(int ave[50]){
 char x;
 float av;
 float sum=0;
 for (int i=0;i<50;i++)
 sum+=ave[i];
 av=sum/50;
 if (av>=40&&av<50)
 x='A';
 else if (av>=30&&av<40)
 x='B';
 else if (av>=20&&av<30)
 x='C';
 else if (av>=10&&av<20)
 x='D';
 else
 x='F';
 printf("Average marks of student =    %f\nAverage grades of student =    %c\n",av,x);
 }
 //the function to add 5 as a bonus to the students
int add(int h){
 int l;
 l=h+5;
 return l;}
 //the function to sort the grades array and print it
 void sort(int sorte[50]){
  int count;
   for ( int i=0; i< 50; i++){
for (int j=i; j< 50-1; j++)

if (sorte[i]> sorte[j+1] ){

count= sorte[i];
sorte[i]= sorte[j+1];
sorte[j+1]= count;}}
printf("the Arrange of degree :\n");
 for (int y=0;y<50;y++)
 printf("%d\n   ",sorte[y]); 
}
int main()
{
    int r=50 ;int addm[50];
    int count;
    int j,som;
    int c,first,last,middle,n=50,search;
    int arr[50][2]={{1,22},{2,41},{3,13},{4,27},{5,33}
    ,{6,31},{7,7},{8,43},{9,38},{10,11},{11,18},{12,24}
    ,{13,29},{14,36},{15,23},{16,16},{17,39},{18,18},{19,29}
    ,{20,40},{21,12},{22,19},{23,26},{24,31},{25,38},{26,30},
    {27,42},{28,9},{29,14},{30,27},{31,31},{32,29},{33,28},{34,19},
    {35,11},{36,38},{37,41},{38,38},{39,20},{40,10},{41,8},{42,33},
    {43,5},{44,35},{45,25},{46,29},{47,31},{48,13},{49,17},{50,42}};
    

 printf("%s%20s\n","Serial number","student grades");
    for(int i=0;i<r;i++){

        printf("%7d %20d\n", arr[i][0],arr[i][1]);

    }

   int Grade[50]={22, 41, 13, 27, 33, 31, 7, 43, 38, 11, 18, 24, 29, 36, 23, 16, 39, 18, 29, 40, 12, 19, 26,
     31, 38, 30, 42, 9, 14, 27, 31, 29, 28, 19, 11, 38, 41, 38, 20, 10, 8, 33, 5, 35, 25, 29, 31, 13, 17, 42};
    int g1=0, g2=0, g3=0, g4=0, g5=0, g6=0, g7=0, g8=0, g9=0, g10=0;
    int i;
    for(i=0;i<=r;i++)
    {
     
      if(Grade[i]<50 && Grade[i]>=45)
            g1++;

        else if(Grade[i]<=44 && Grade[i]>=40)
            g2++;

        else if(Grade[i]<=39 && Grade[i]>=35)
            g3++;

        else if(Grade[i]<=34 && Grade[i]>=30)
            g4++;

        else if(Grade[i]<=29 && Grade[i]>=25)
            g5++;

        else if(Grade[i]<=24 && Grade[i]>=20)
            g6++;

        else if(Grade[i]<=19 && Grade[i]>=15)
            g7++;

        else if(Grade[i]<=14 && Grade[i]>=10)
            g8++;

        else if(Grade[i]<=9 && Grade[i]>=5)
            g9++;

        else if(Grade[i]<=4 && Grade[i]>=0)
            g10++;
    }
    printf("\nNumber of Student who grade is between 50 and 45 are : %d\n ",g1);
    printf("\nNumber of Student who grade is between 44 and 40 are : %d\n",g2);
    printf("\nNumber of Student who grade is between 39 and 35 are : %d\n" ,g3);
    printf("\nNumber of Student who grade is between 34 and 30 are : %d\n" ,g4);
    printf("\nNumber of Student who grade is between 29 and 25 are : %d\n" ,g5);
    printf("\nNumber of Student who grade is between 24 and 20 are : %d\n" ,g6);
    printf("\nNumber of Student who grade is between 19 and 15 are : %d\n ",g7);
    printf("\nNumber of Student who grade is between 14 and 10 are : %d\n" ,g8);
    printf("\nNumber of Student who grade is between 9 and 5 are : %d\n" ,g9);
    printf("\nNumber of Student who grade is between 4 and 0 are : %d\n" ,g10);
    //compute the average of student grade
    printf("\n");
   int Gradee[50]={22, 41, 13, 27, 33, 31, 7, 43, 38, 11, 18, 24, 29, 36, 23, 16, 39, 18, 29, 40, 12, 19, 26,
     31, 38, 30, 42, 9, 14, 27, 31, 29, 28, 19, 11, 38, 41, 38, 20, 10, 8, 33, 5, 35, 25, 29, 31, 13, 17, 42};

     for (int k=0;k<50;k++)
     {
      //call the function 
  som+=Gradee[k];
     addm[k]=add(Gradee[k]);
     }
 
     average(Gradee);
 
sort(addm);
  
//using binary search to know the degree intered is found 
  printf("\n\nEnter value to find\n");
  scanf("%d", &search);

first = 0;
  last = 50- 1;
  middle = (first+last)/2;

  while (first <= last) {
    if (addm[middle] < search)
      first = middle + 1;
    else if (addm[middle] == search) {
      printf("%d found its serial number is %d.\n", search, middle+1);
      break;
    }
    else
      last = middle - 1;

    middle = (first + last)/2;
  }
  if (first > last)
    printf("Not found in the list.\n", search);}
