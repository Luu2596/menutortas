#include <stdio.h>
#include <stdlib.h>
main(){
	int productos[4] = {0, 0, 0, 0};
	int seleccion;
	while(1){
		printf("1) Torta cubana.\n2) Torta de jamon.\n3) Torta especial.\n4) Refresco.\n5) Salir (Imprimir ticket).\n\n");
		printf("Que desea ordenar? ");
		scanf("%d",&seleccion);
		while(1){
			if(seleccion>0 && seleccion<6) break;
			printf("Error: Opcion no valida. Indique una opcion del menu: ");
			scanf("%d",&seleccion);
		}
		if(seleccion==5) break;
		productos[seleccion-1] += 1;
		printf("Ha elegido: ");
		switch(seleccion){
			case 1: 
				printf("Torta cubana.\n");
				break;
			case 2:
				printf("Torta de jamon.\n");
				break;
			case 3:
				printf("Torta especial.\n");
				break;
			case 4:
				printf("Refresco.\n");
				break;
		}
	}
	printf("\nSu ticket de compra:\n\n");
	if(productos[0]>0)
		printf("%d Torta(s) cubana(s).\n",productos[0]);
	if(productos[1]>0)
		printf("%d Torta(s) de jamon.\n",productos[1]);
	if(productos[2]>0)
		printf("%d Torta(s) especial(es).\n",productos[2]);
	if(productos[3]>0)
		printf("%d Refresco(s).\n",productos[3]);
	printf("\nGracias por su compra.");
	system("pause");
}
