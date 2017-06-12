# Projeto-Integrador-1
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int contadorProjeto=0; // variavel responsavel pela organizaçao da struct.

//-------------------------------------------Projeto----------------------------------------------------
struct Projeto{
	int codigo;
	char nome [20];
	int desenvolvedor;
	char testeNome[20];
	char gerenteNome[20];

}projeto[];


void CriarProjeto (){
    system("clear");
    printf("Informe o codigo Codigo do projeto: ");
	scanf ("%i", &projeto[contadorProjeto].codigo);
	printf("Informe o nome do Projeto (ate 20 caracteres): ");
	scanf ("%s", &projeto[contadorProjeto].nome);
	printf("Informe o nome do analista de testes (ate 20 caracteres): ");
    scanf ("%s", &projeto[contadorProjeto].testeNome);    
    contadorProjeto++; // aumentos variavel que contra a localicao nos vetores
    system("clear");
    printf ("\t\tProjeto incluido com sucesso.\n");
}

void CriarProjeto(){

}




//-------------------------------------------Desevolvedores----------------------------------------------------
struct Desenvolvedores{
	int codigo;
	char nome [20];

}desenvolvedor[30];

void CriarDesenv(){
    system("clear");
    printf("Informe o codigo Codigo do projeto: ");
	scanf ("%i", &projeto[contadorProjeto].codigo);
	printf("Informe o nome do Projeto (ate 20 caracteres): ");
	scanf ("%s", &projeto[contadorProjeto].nome);    
    contador_medicamento++; // aumentos variavel que contra a localicao nos vetores
    system("clear");
    printf ("\t\tDesenvolvedor incluido com sucesso.\n");
}

void AlterarDesenv(){

}

void ExcluirDesenv(){

}


//-------------------------------------------Defeito----------------------------------------------------
struct Defeito{
	int codigo;
	char funcionabilidade [100];
	int desenvolvedor;
	int severidade;
	
}projeto[30];











//-------------------------------------------Menu-------------------------------------------------
main()
{
	int menu=0;
	int posicao;
	for (;menu!=5;)
	{
		printf("1. Incluir um medicamento\n");
		printf("2. Alterar um medicamento\n");
		printf("3. Excluir um medicamento\n");
		printf("4. Consultar um medicamento\n");
		printf("5. Sair\nDigite a sua opcao: ");
		scanf ("%d", &menu);
		system("clear");
		switch (menu)
			{
			case (1):
				cadastramento ();
			break;
			case (2):
				alteracao ();
			break;
			case (3):
			    exuclusao();
			break;
			case (4):
				if (contador_medicamento==0) // feito para tirar um erro que estava ocorrendo quando cliente cliente sem ter nada cadrastrado
					printf ("\t\t\tNao existe medicamento cadratrado.\n\n");
				else
			    	consulta ();
            break;
			case (5):
			break;
			default:
				printf ("\t\t\tOpcao invalida, digite novamente.\n\n");
        }

	}

}

