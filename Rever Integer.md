int reverse(int x) {
    int sum=0;
    int j;
    int i;
    int a[256];
    int t;
    for(j=1;(x/(pow10(j)))!=0;)
    {
        a[j]=(x%(int)pow10(j))/(int)pow10(j-1);
       
        x-=a[j]*(int)pow10(j-1);
          j++;
          t=j;
    }
                            
    for(i=1;i<j;i++)
   {
         --t;
         sum+=a[i]*(int)(pow10(t));         
   }
                 
    return(sum/10);
}
