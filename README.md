# CASH


#include <stdio.h>
#include <cs50.h>


int main (void)
{

    float troco = 0;
    float var0 = 0.1, var1 = 0.5, var2 = 0.10, var3 = 0.25; 
    int moedas = 0;
    int troco2 = 0;
    
    do {
        
        troco = get_float ("insira o troco aqui:");
        troco2 = troco *100;
    }
     while (troco < 0 || troco >100);
    while (troco2 > 1){
    
        
        if (troco2 >= 25)
        {
            var3++;
            troco2 -= 25;
        }
        else if (troco2 >= 10)
        {
            var2++;
            troco2 -= 10;
        }
        else if (troco2 >= 5)
        {
            var1++;
            troco2 -= 5;
        }
        else if (troco2 >= 1)
        {
            var0++;
            troco2 -= 1;
        }
    }
        
        moedas = var0 + var1 + var2 +var3;
        
        printf("\n");
        printf("moedas = %i", moedas);
        printf("\n");
    }
