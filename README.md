#include <iostream>
#include<math.h>
#include<conio.h>
#include <stdio.h>
using namespace std;

int a,b,c,X1,X2;
int V;
int  xo,vo,t,A;


void funV()
{

printf ("Ingrese el primer coeficiente: ");
scanf ("%d",&a);
printf ("Ingrese el segundo coeficiente: ");
scanf ("%d",&b);
printf("Ingrese el tercer coeficiente: ");
scanf("%d",&c);


}
int fun1x1(int a,int b,int c) {
	int resultado1;
	resultado1= X1 = (-b+sqrt(pow(b,2)-4*a*c))/(2*a);
	return resultado1;
}
int fun1x2(int a,int b,int c){
	int resultado2;
	resultado2 = X2= (-b-sqrt(pow(b,2)-4*a*c))/(2*a);
	return resultado2;
}

void funVE(){

	printf ("Ingresa el radio de la esfera: ");
	scanf ("%d",&V);
}
int funV(int V){
int Vo;

if (V>0){
	Vo=(4/3) *(M_PI*pow(V,3));
}
else{
	printf("Ingrese un valor valido");
} 
return Vo;
}

void funDes(){

printf ("Introduzcir la posicion inicial: ");
scanf ("%d",&xo);
printf ("Introduzca la velocidad inicial: ");
scanf ("%d", &vo);
printf ("Introduzca el tiempo: ");
scanf ("%d", &t);
printf ("Introduzca la aceleracion: ");
scanf ("%d",&A);
}
int funD(int xo, int vo, int t, int A){

int Df;
Df= (xo+vo+(a*(pow(t,2))/2));

return Df;
}

int main (){
	int n;
		printf ("Seleccione una de las tres calculos: \n" );
		printf ("1-la raiz de un polinomio de 2-G\n2-Volumen de una esfera\n3-Desplazamineto de un movil en MRUV\n");
	scanf ("%d", &n);
	
	switch (n){
		case 1: 
		funV();
		printf ("\nX1= %.2f",fun1x1(a,b,c));
		printf ("\nX2= %.2f",fun1x2(a,b,c));
		break;
		
		case 2: 
		funVE();
		printf ("\nEl valor del volumen de la esfera es: %.2f", funV(V));
		break;
		
		case 3:
			funDes();
			printf ("\nEl desplazamiento final del movil es: %.2f",funD(xo,vo,t,A));
			break;
	}
   
	return 0;
}
