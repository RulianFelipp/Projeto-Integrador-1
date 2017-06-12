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

}projeto[10];


void CriarProjeto (){
    system("cls");
    printf("Informe o codigo Codigo do projeto: ");
	scanf ("%i", &projeto[contadorProjeto].codigo);
	printf("Informe o nome do Projeto (ate 20 caracteres): ");
	scanf ("%s", &projeto[contadorProjeto].nome);
	printf("Informe o nome do analista de testes (ate 20 caracteres): ");
    scanf ("%s", &projeto[contadorProjeto].testeNome);
    ConsultarProjeto();
    contadorProjeto++; // aumentos variavel que contra a localicao nos vetores
    system("cls");
    printf ("\t\tProjeto incluido com sucesso.\n");
}

void AlterarProjeto(){
    system("cls");
    printf("Funcao em Desenvolvimento.");

}

void ExcluirProjeto(){
    system("cls");
    printf("Funcao em Desenvolvimento.");
}

void ConsultarProjeto(){
    int x;
    printf("\n\nCodigo do projeto: %i", &projeto[contadorProjeto].codigo);
	printf("\nNome do Projeto: %s", &projeto[contadorProjeto].nome);
	printf("\nAnalista de testes %s", &projeto[contadorProjeto].testeNome);
	scanf("%i", &x);
}



void menuProjeto(){

    int menu = 5;

    system("cls");
    printf("1. Incluir Projeto\n");
    printf("2. Alterar Projeto\n");
    printf("3. Excluir Projeto\n");
    printf("4. Consultar Projeto\n");
    printf("0. Voltar\nDigite a sua opcao: ");
    scanf ("%d", &menu);

    switch (menu)
    {
        case (1):
            CriarProjeto ();
        break;
        case (2):
            AlterarProjeto();
        break;
        case (3):
            ExcluirProjeto();
        break;
        case (4):
            if (contadorProjeto==0) // feito para tirar um erro que estava ocorrendo quando cliente cliente sem ter nada cadrastrado
                printf ("\t\t\tNao existe medicamento cadratrado.\n\n");
            else
                printf("Funcao Excluir ainda nao criada");
                //consulta ();
        break;
        case (0):
        break;
        default:
            printf ("\t\t\tOpcao invalida, digite novamente.\n\n");

    }


    return;
}



//-------------------------------------------Desevolvedores----------------------------------------------------
struct Desenvolvedores{
	int codigo;
	char nome [20];

}desenvolvedor[30];

void CriarDesenv(){
    system("cls");
    printf("Informe o codigo Codigo do projeto: ");
	//scanf ("%i", &projeto[contadorProjeto].codigo);
	printf("Informe o nome do Projeto (ate 20 caracteres): ");
	//scanf ("%s", &projeto[contadorProjeto].nome);
    //contadorProjeto++; // aumentos variavel que contra a localicao nos vetores
    system("cls");
    printf ("\t\tDesenvolvedor incluido com sucesso.\n");
}

void AlterarDesenv(){
    system("cls");
    printf("Funcao em Desenvolvimento.");

}

void ExcluirDesenv(){
    system("cls");
    printf("Funcao em Desenvolvimento.");
}




void menuDesenv(){

    int menu = 5;

    system("cls");
    printf("1. Incluir Desenvolvedor\n");
    printf("2. Alterar Desenvolvedor\n");
    printf("3. Excluir Desenvolvedor\n");
    printf("4. Consultar Desenvolvedor\n");
    printf("0. Voltar\nDigite a sua opcao: ");
    scanf ("%d", &menu);

    switch (menu)
    {
        case (1):
            CriarDesenv();
        break;
        case (2):
            AlterarDesenv();
        break;
        case (3):
            ExcluirDesenv();
        break;
        case (4):
            if (contadorProjeto==0) // feito para tirar um erro que estava ocorrendo quando cliente cliente sem ter nada cadrastrado
                printf ("\t\t\tNao existe medicamento cadratrado.\n\n");
            else
                printf("Funcao Excluir ainda nao criada");
                //consulta ();
        break;
        case (0):
        break;
        default:
            printf ("\t\t\tOpcao invalida, digite novamente.\n\n");

    }


    return;
}

//-------------------------------------------Defeito----------------------------------------------------
struct Defeito{
	int codigo;
	char funcionabilidade [100];
	int desenvolvedor;
	int severidade;

}defeito[30];


void CriarDefeito(){
    system("cls");
    printf("Funcao em Desenvolvimento.");

}


void AlterarDefeito(){
    system("cls");
    printf("Funcao em Desenvolvimento.");

}

void ExcluirDefeito(){
    system("cls");
    printf("Funcao em Desenvolvimento.");
}






void menuDefeito(){

    int menu = 5;

    system("cls");
    printf("1. Incluir Defeito\n");
    printf("2. Alterar Defeito\n");
    printf("3. Excluir Defeito\n");
    printf("4. Consultar Defeito\n");
    printf("0. Voltar\nDigite a sua opcao: ");
    scanf ("%d", &menu);

    switch (menu)
    {
        case (1):
            CriarDefeito();
        break;
        case (2):
            AlterarDefeito();
        break;
        case (3):
            ExcluirDefeito();
        break;
        case (4):
            if (contadorProjeto==0) // feito para tirar um erro que estava ocorrendo quando cliente cliente sem ter nada cadrastrado
                printf ("\t\t\tNao existe medicamento cadratrado.\n\n");
            else
                printf("Funcao Excluir ainda nao criada");
                //consulta ();
        break;
        case (0):
        return;
        default:
            printf ("\t\t\tOpcao invalida, digite novamente.\n\n");
    }


    return;
}














//-------------------------------------------Menu-------------------------------------------------
main()
{
	int menu=3;
	int posicao;
	for (;menu!=0;)
	{

	    printf("1. Projeto\n");
		printf("2. Desenvolvedor\n");
		printf("3. Defeito\n");
		printf("0. Sair\nDigite a sua opcao: ");
        scanf ("%d", &menu);

        switch (menu)
        {
            case (1):
                menuProjeto();
            case (2):
                menuDesenv();
            case (3):
                menuDefeito();
            case (0):
                exit(0);
            default:
                printf ("\t\t\tOpcao invalida, digite novamente.\n\n");
        }

    }
}


