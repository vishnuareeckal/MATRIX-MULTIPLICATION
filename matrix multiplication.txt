#include <stdio.h>
void main()
{
  printf("MATRIX MULTIPLICATION\n\n");
  printf("done by me;)\n");
  int m,n,c,d,p,q,k,sum=0;
  int first[10][10],second[10][10],x[10][10];
  printf("\nenter the no. of rows and columns of first matrix\n");
  scanf("%d%d",&m,&n);
  printf ("chosen %dx%d matrix\n",m,n);
  
  printf("\nenter the %d elements of first matrix\n",m*n);
  
  for(c=0;c<m;c++)
    for(d=0;d<n;d++)
    scanf("%d",&first[c][d]);
  printf("\nenter the no. of rows and columns of second matrix\n");
  scanf("%d%d",&p,&q);
  
  /*
    *
      *
        *
          *
            *
              */
  
  if(n!=p)
  {
    printf ("\nsuch matrix cannot be multiplied\n\n");
  }
  else
  {
    printf ("\nenter the %d elements of second matrix\n\n",m*n);
  }
  for(c=0;c<p;c++)
    for(d=0;d<q;d++)
    scanf("%d",&second[c][d]);
 
 
 //printing first matrix
 
 printf("\n\nfirst matrix is :\n");
 for(c=0;c<m;c++)
 {
    for(d=0;d<n;d++)
   {
     printf ("%d\t",first[c][d]) ;
   }
   printf("\n");
 } 
 printf("\n");
 
 /*
   *
     *
       *
         *
           *
             */
 
 //printing second matrix
 
 printf("\n\nsecond matrix is :\n");
 for(c=0;c<p;c++)
 {
   for(d=0;d<q;d++)
   {
     printf ("%d\t",second[c][d]);
   }
   printf("\n");
 }
 
  //multiplication  
   
   for(c=0;c<m;c++)
   {
     for(d=0;d<q;d++)
     {
       for(k=0;k<p;k++)
       {
         sum=sum+first[c][k]*second[k][d];
       }
       x[c][d]=sum; //product matrix
       
     }
   }
   
   //printing product matrix
   
   printf("\n\nproduct matrix is\n");
   for(c=0;c<m;c++)
 {
   for(d=0;d<q;d++)
   {
     printf ("%d\t",x[c][d]);
   }
   printf("\n");
 }
 
 printf("\n\n\ncoding is nice💤");
  return 0;
}
