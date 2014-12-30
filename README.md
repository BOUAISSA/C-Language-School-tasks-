#include<stdio.h>

main()
{  int t[10]={31,-41,59,26,-53,58,97,-93,-23,84};
   int max,som,i,j,indice_debut,indice_fin,som2,n,m,max_resul;
    max=t[0];
    for(j=0;j-1<10;j++)
        { som=0;
         for(i=j;i<10;i++) som=som+t[i];
         if (max<som) {max=som; indice_debut=j;}
        }
        //printf("le premiere max qu'on obtien %d\n",max);
        printf("indice debut: %d\n",indice_debut);

    max_resul=0;
    for(n=10;indice_debut<n;n--)
    {
        som2=0;
        for(m=indice_debut;m<n;m++) som2=som2+t[m];
        if (max_resul<som2)
        {max_resul=som2;
         indice_fin=n-1;
        }
    }
    printf("indice fin: %d\n",indice_fin);
    printf("le max general qu'on obtien %d\n",max_resul);
    for (i=indice_debut;i<indice_fin;i++) printf("  %d '",t[i]);

    return 0;
}

