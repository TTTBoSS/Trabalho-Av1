# Trabalho-Av1
#include < stdio.h>
#include < stdin.h>
#define max 10

typedef struct{
    char nome[50];
    int idade;
    char cpf[11];
    char solicitacao;
}Pessoa;//estrutura pessoa

typedef struct Pessoa2{
    Pessoa x;
    struct Pessoa2 *prox;
}P2;

P2* criarPessoa(P2 *p);
P2* remover(P2 *p);
void imprimirLista (P2 *p);
void editarPessoa(P2 *p);
void removerPessoa(P2 *p);

int main(){
    int opcao= -1, opcao2, op3, existe=0;
    Pessoa pessoa;
    Pessoa *p=NULL;
    While(opcao !=0){
        system ("cls");
        printf("qual usuario voce e?");
        printf("--------------\n");
        printf("1-Cliente");
        printf("2-Atendente");
        printf("3-Gerente");
        printf("4-Sair");
        printf("opcao: ");
        scanf("%d", op3);

        switch(op3){
            case 1:
                if (existe){
                    printf("Senha já criada!");
                    }else{
                        p = criarPessoa(p)
                        existe=1;
                    }}
                    break;
            case 2:
                if (existe==1){`
                if(p==NULL){
                    system("cls");
                    printf("Fila vazia");
                    system('pause");
                }else{
                    system("cls");
                    imprimirLista(p);
                }
            } 
            else{
                system("cls");
                printf("fila nao inciada");
                system("pause");
            } 
                break;   
            case 3:
                if(existe ==1){
                    if(p==NULL){
                        system ("cls");
                        printf("Fila Vazia");
                        system("pause");
                    }else{
                        system("cls");
                        excluirPessoa(p);
                    }
                }
                else{
                    system ("cls");
                    printf("fila não iniciada");
                    system ("pause");
                } 
                break;
            case 4:
             if(existe == 1){
                if(p==NULL){
                    system("cls");
                    printf("fila vazia");
                    system ("pause");
                }
                else{
                    system("cls");
                    printf("fila não iniciada");
                    system("pause");
                }break;
            }
        }
    }
}

P2* criarPessoa(P2 *p){
    p2 *n = (P2) malloc(sizeof(P2));
    if(n ==NULL){
        printf("Impossivel acrescentar mais alguem na fila");
        system("pause");
        returnp;
    }else{
        if(p==NUL){
            printf("\nDigite o nome: " );
            scanf("%100[\n]", &n->x.nome);
            printf("\nDigite a idade: " );
            scanf("%d", &n->x.idade);
            printf("\nDigite o cpf: " );
            scanf("%s", &n->x.cpf);
            printf("Digite a solicitacao: ");
            scanf("%s", &n->x.solicitacao);
            system ("pause");
            n->prox=NULL;
            printf("%s entrou na fila", n->x.nome);
            system ("pause");
            return;
            }else{
            printf("digite o nome: ");
            scanf("%100[\n]", &n->x.nome);
            printf("\nDigite a idade: " );
            scanf("%d", &n->x.idade);
            printf("\nDigite o cpf: " );
            scanf("%s", &n->x.cpf);
            printf("Digite a solicitacao: ");
            scanf("%s", &n->x.solicitacao);
            n->prox->p;
            system ("pause");
            printf("\n %s Entrou na final\n",n->x.nome);
            system("pause");
            return n;
            }
    }
}
void imprimirLista(P2 *p){
    Pessoa fila [max];
    int i=0, contador=0;
    int num = 1;
    P2 *q;
    q=p;
    while(q!=NULL){
        q = q->prox;
        contador++;
        }
        q=p;
        do{
            strcpy(fila[i].nome, q->x.nome);
            strcpy(fila[i].cpf, q->x.cpf);
            strcpy(fila[i].sloicitacao, q->x.solicitacao);
            i++;

            q=q->prox;
            }while{q!=NULL};
            printf("Ordem de atendimento: \n);
            for(i=contador-1; i>-1;i--){
                printf("posicao: %d---------, num);
                printf("|%s\t|%s\t|%s\t", fila[i].nome, fila[i].cpf, fila[i].solicitacao);
                num++;
            }
            system ("pause");
            contador=0;
        }
        void editarPessoa(P2 *p){
    int i, pos=0;
    Pessoa usu;
    P2 *u;
    u = p;
    printf(" \n Digite um nome: ");
    scanf("%s",u->x.nome);
    strcpy(usu[i].nome, u->x.nome);

for(i=0; i<10; i++) {
    if(strcpy(u->x.nome)== 0) {
        printf("\n Registro encontrado! ");
        pos = i;
    } else {
        pos = -1;
    }
}
if(pos = -1) {
    printf(" \n Registro não encontrado! ");
} else {
    printf(" \n Registro Encontrado: %s");

    printf(" Digite o nome da pessoa: %s",usu[i].nome);
    printf("Selecione qual dado voce quer editar: ");
    printf("1- Nome;");
    printf("2- Idade;");
    printf("3- CPF;");
    system("PAUSE");
    scanf("%d",op1);

	switch(op1)
	{
		case 1:
			printf("Digite o novo nome: \n");
			scanf("%s", &p->x.nome);
			break;
		case 2:
			printf("Digite a nova idade: \n");
			scanf("%d", &p->x.idade);
			break;
		case 3:
			printf("Digite o novo CPF: \n");
			scanf("%s", &p->x.cpf);
			break;
		default:
			printf("Opcao Invalida!\n");
			system("pause");
			break;
	}}
}
void excluirPessoa(P2 *p){
P2 *q, *ant;
 q = p;
 if(q->prox == NULL)
   {
   printf("%s foi atendido!\n", q->x.nome);

   system("pause");
   free(q);
   return NULL;
   }
 else{
   do{
     ant = q;
     q = q->prox;
     }while(q->prox != NULL);

   printf("%s foi antendido!\n", q->x.nome);

   system("pause");
   free(q);
   ant->prox = NULL;

   return ant;
}}
