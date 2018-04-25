# Fibonacci
#include <stdio.h>
int main(){
	int x = 0;
	printf("%i\n", suma(2,4));
	printf("Diga un numero\n");
	scanf("%i", &x);
	printf("%i\n", fibonacci(x));
	//printf("%i\n", sumatoria(4));
	return 0;
}

int suma(int a, int b){
	return a+b;
}

int fibonacci(int a){
	int rta = 0;
	int x = 0;
	int y = 1;
	int cont;
	if (a==0){
		return 0;
	}
	if (a==1){
		return 1;
	}
	if (a>1){
		for (cont=1; cont<a; cont=cont+1){
			rta = x + y;
			x = y;
			y = rta;
		}
		return rta;
}

int sumatoria(int a){
	int rta = 0;
	int cont;
	for (cont=0; cont<=a; cont=cont+1){
		rta=rta+cont;
	}
	return rta;
}

}
