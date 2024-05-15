programa
{  
  inteiro indicehospede=0,v=0
  inteiro totaldespesas=0
  cadeia nome[10]
  real cpf[10]
 inteiro despesa[10],dias[10]
funcao inicio() {
    menu()
    
  }
  funcao menu(){
      
     inteiro opcao=5
     enquanto(opcao!=0){
    escreva("\n-----------menu---------\n")
    escreva("digite 1-cadastrar hospedes\n")
    escreva("digite 2-exibir hospedes\n")
    escreva("digite 3-reservar area de lazer\n")
    escreva("digite 4-calcular total a pagar\n")
    escreva("digite 0-sair")
    
    escreva("\ndigite a sua opcao:")
    leia(opcao)
    escolha(opcao){
      caso 1:
    cadastrar()
      pare
      caso 2:
      exibir()
      pare
      caso 3:
       lazer()
      pare
      caso 4:
      
      totaldespesas=calcular()
      escreva("O/A hospede cujo nome e:",nome[indicehospede]," ","tem q pagar",totaldespesas,"reais")
      
     
      
      pare
      caso 0:
        escreva("saindo do programa")
      pare
    }
     
  }
  }
  funcao cadastrar(){
 inteiro i=0
 caracter continuar='s'
 enquanto(continuar=='s' e i<10){
    

 	escreva("digite o nome do hospede:")
 	leia(nome[i])
 	escreva("digite o cpf do hospede:")
 	leia(cpf[i])
 	escreva("digite a duracao da viagem:")
 	leia(dias[i])
 	despesa[i]=0
 	
 	

      
    escreva("deseja continuar S(para continuar) ou N(para ir para o menu):")
 leia(continuar)
 i++
 se(i>=10){
 	escreva("numero de hospedes  lotado")
 }
 }

    
  }
   funcao exibir(){
  para(inteiro j=0;j<10;j++){
      escreva(j+1,"-","hospede:",nome[j],"-","CPF do hospede:",cpf[j],"-","despesas:",despesa[j],"-","Duracao da hospedagem:",dias[j],"\n")
    }
   }
   funcao lazer(){
   	
   	inteiro valor1=0,valor2=0,valor3=0
	inteiro i=0,cont1=1,cont2=1,cont3=1
   	caracter opc
   	para(i=0;i<10;i++){
	escreva(i+1,"Hopsede:",nome[i],"-","despesas:",despesa[i],"\n")
}
faca{
	escreva("digite o indice hospede(de 1 ate 10)")
	leia(indicehospede)
	indicehospede=indicehospede-1
	escreva("No hotel a tres opcoes de lazer escolha dentre elas a Academia,Salao de festas e Restaurante \n")
	escreva("digite sua opcao A(para a Academia),S(para o Salao de festas) e R(para o Restaurante):")
	leia(opc)
	se(opc=='A'ou opc=='a'){
		escreva("O usuario selecionou a Academia que custa 20 reais\n")
		despesa[indicehospede]+=20
	    
	
	}
	senao se(opc=='S'ou opc=='s'){
		escreva("O usuario selecionou o salao de festas que custa 50 reais\n")
		despesa[indicehospede]+=50
		
		
	}
	senao se(opc=='R' ou opc=='r'){
		escreva("O usuario selecionou o Restaurante que custa 35 reais\n")
		despesa[indicehospede]+=35
		
	}
	
	 escreva("deseja continuar S(para continuar) ou N(para ir para o menu):")
	leia(opc)
	
     
}enquanto(opc=='s')
 
    para(i=0;i<10;i++){
	escreva(i+1,nome[i],"-",despesa[i],"\n")}
   }
   funcao inteiro calcular(){
   	inteiro i=0
   	caracter ocp='s'
      
   	para(i;i<10;i++){
   		escreva(i+1,"-",nome[i],"-",despesa[i],"-",dias[i],"\n")
   	}
   	
    	escreva("digite o indice hospede(de 1 ate 10)")
	leia(indicehospede)
	indicehospede=indicehospede-1
	totaldespesas=despesa[indicehospede]+(dias[indicehospede]*100)
	retorne totaldespesas
    
      
   }
   
  
}
