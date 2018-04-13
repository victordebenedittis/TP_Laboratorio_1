#include <stdio.h>
#include <stdlib.h>
#include "funciones.h"

int main()
{
    char seguir='s';
    int opcion=0;
    float op1=0, op2=0;
    float resultado;

    while(seguir=='s')
    {
        system("cls");
        printf("********************************************");
        printf("\n* 1- Ingresar 1er operando (A=%f)    *",op1);
        printf("\n* 2- Ingresar 2do operando (B=%f)    *",op2);
        printf("\n* 3- Calcular la suma (A+B)                *");
        printf("\n* 4- Calcular la resta (A-B)               *");
        printf("\n* 5- Calcular la division (A/B)            *");
        printf("\n* 6- Calcular la multiplicacion (A*B)      *");
        printf("\n* 7- Calcular el factorial (A!)            *");
        printf("\n* 8- Calcular todas las operaciones        *");
        printf("\n* 9- Salir                                 * ");
        printf("\n********************************************\n");


        scanf("%d",&opcion);



        switch(opcion)
        {
            case 1:
                 printf("Ingrese el primer numero: ");
                    scanf("%f", &op1);
                break;
            case 2:
                 printf("Ingrese el segundo numero: ");
                    scanf("%f", &op2);
                break;
            case 3:
                 resultado=sumar(op1, op2);
                    printf("La suma de los numeros es %f\n", resultado);
                    system("pause");
                break;
            case 4:
                 resultado=restar(op1, op2);
                printf("La resta de los numeros es %f\n", resultado);
                system("pause");
                break;
            case 5:
                 if(op1!=0 && op2!=0)
                    {
                        resultado=dividir(op1, op2);
                        printf("La division de los numeros es %2.f\n", resultado);
                        system("pause");
                    }
                else
                    {
                        printf("Error. No se puede dividir si uno de los dos numeros es cero\n");
                        system("pause");
                    }
                break;
            case 6:
                    resultado=multiplicar(op1, op2);
                    printf("La multiplicacion de los numeros es %f\n", resultado);
                    system("pause");
                break;
            case 7:
                    resultado=factorial(op1);
                    printf("El factorial del numero es %f\n", resultado);
                    system("pause");
                break;
            case 8: resultado=sumar(op1, op2);
                    printf("La suma es %f\n", resultado);
                    resultado=restar(op1, op2);
                    printf("La resta es %f\n", resultado);

                    if(op1!=0 && op2!=0)
                        {
                            resultado=dividir(op1, op2);
                            printf("La division de los numeros es %2.f\n", resultado);
                            system("pause");
                        }
                        else
                        {
                            printf("Error. No se puede dividir si uno de los dos numeros es cero\n");
                        }

                    resultado=multiplicar(op1, op2);
                    printf("La multiplicacion es %f\n", resultado);

                    resultado=factorial(op1);
                    printf("El factorial es %f\n", resultado);
                    system("pause");

                break;

            case 9:

                break;
        }
}
    return 0;

}
