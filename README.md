# JS-Memories

[Aula 001]: (Node.js terminal) Ctrl + L => Limpa a tela 

*********[Vídeo 000]: **Briefing**
>Somente um brief sobre as aulas.
******************************************************************************************
*********[Vídeo 001]: **Variaveis**	
>Variaveis, EX: var nomedavar = valorqualquer;
> Quotes, no JavaScript, Single or Double Quotes são entendidas da mesma forma. EX: 'hello' or "hello"
> Boolean, pode ser setado uma variavel como TRUE or FALSE
>NULL, é setado a ficar vazio, diferente de undefined que não há valor definido. (Pequenas diferenças)
>Objetos, representado entre {} Representa diversas caracteristicas comuns a aplicação EX: 
	objeto pessoa =>  pessoa = {
			altura: 1.87,  	//Usa : ao inves de = para objetos
			peso: 90
			}
para acessar uma propriedade/atributo dentro usa-se assim, "pessoa(objeto).altura(atributo)" é possivel
alterar valores de dentro do objeto acessando os atributos e dando novos valores:

	pessoa.altura = 1.90 (1.87 valor antigo) , acessando o objeto tera o novo valor armazenado.
>Array, uma serie de valores em uma unica variavel, que são acessadas por indices
EX: var numeros = [] (Já torna um array) para passar valores,
numeros = [1, 2, 3, 4, 5, 6] para acessar os valores são utilizado chaves
numero[0], retorna 1 e assim por diante, para chaves associativa *JavaScript does not support arrays with named indexes*
'Javascript não existem array, eles são objetos'
EX:  pessoa.altura ou pessoa['altura'], retorna os mesmos valores.
*****************************************************************************************************
*********[Vídeo 002/3]: **Operadores**
>Operadores: + or - or * or /
>Operadores(Incremento/Decremento)(Abreviados): ++ or -- **Pré Incremento e PósIncremento**
>Operadores(Abreviados): Outros formatos, += or -= or *= or /=
>Operadores igualdades relacionais: 

== (Vê se é igual os valores armazenados independente de tipo) or != (Vê se são diferentes os valores independente do tipo)
 ===  (Vê se os valores eo tipo são iguais) or !==  (Vê se os valores ou tipo são diferentes)
> (Vê se um valor é maior ), < (Vê se um valor é menor), >= (Vê se o valor é maior ou igual), <=(Vê se o valor é menor ou igual)
*******************************************************************************************************

*********[Vídeo 004]: **Funções**
>Função suporta códigos dentro de chaves EX:function nomeDaFuncao(){},  e pode ser invocada como EX: nomeDaFuncao()
>EX Concatenar String1 + "  " + String2
>Funções criam escopo, toda variavel declarada dentro de uma função, só pode ser utilizada dentro daquela função, podem ser
acessadas com o RETURN da função, mas as funções devem ser invocadas antes.
>Funções podem ser manipuladas como EX:
 function num() {
x = 2;			num() + 2; //Retorna 4
return x; }		

>Funções pode receber parâmetros, dentro dos parenteses EX: function soma(x, y) {return x + y;} 
soma(2, 3) => retorna 5 //Passando 2 e 3 como parâmetros
*******************************************************************************************************
[Aula 002]:
	[Aula 002/007]**Operadores Lógicos**
| | = *ou* condição de 'um parametro ou outro ser verdadeiro/falso
&& = *e* condição de 'um parametro e outro serverdadeiro/faslo
*******************************************************************************************************
	[Aula 002/008]**Operadores Unários**
Os operadores de + e - podem ser usados para converter tipos de variaveis
EX: +'3' to 3, nesse caso converteu uma string em um Número, +'Leo' to NaN, é convertido em numero mas não pode ser representado
>Para concatenar 'Leo' + 'Goes' to 'Leo Goes',  3 + '3' to '33', o inverso tbm é o mesmo, o JS sempre que soma-se uma string
com um número ele entende que você quer concatenar. Com o operado menos não é possivel retorna NaN.
>A conversão com o operador - precedendo ocorre da mesma forma, ele altera o tipo para numero e ainda seta para negativo
o valor, porém, não altera o valor fixo, somente naquela aplicaçao.
EX: x = '3', -x to -3, x retorna '3'.
> !(string,var,int,bool) => inverte o valor(para o mesmo tipo)
*******************************************************************************************************
	[Aula 002/007]**Estrutura Léxica**
> JS é Case sensitive
> Comentários podem ser feitos usando // or /**/
>Literais fazem parte da linguagem strings, bools, null, objetos, arrays, ints
>Identificadores podem ser iniciados com: _ ou $ ou letras de a,z ou letras de A,Z ou digitos de 0,9 e podem caracter UNICODE
**Identificadores funcionam com carcteres UNICODE mas não devem ser usados******
>Palavras reservadas
********************************************************************************************************
	[Aula 002/007]**Instruções Condicionais**
>IF(Condition){ #CodeIfTrue}else{#CodeIfFalse}
>Ver se passou parametros setar como undefined pq null dever ser declarado com null
********************************************************************************************************
	[Aula 003/0015]**Objetos e Funções**
>armazenar uma funcao em uma variavel EX: var myVar = function addVar(){return 'Varception';}
> É possível adicionar um novo atributo em um objeto somente passando o nome do objeto e do novo atributo e atribuir o valor
desejado EX: pessoa = {nome: 'Leo'} pessoa.sobrenome ='Goes', pessoa={nome:'Leo', sobrenome:'Goes'}
>É possivel armazenar um funcção dentro de uma variavel dentro de um obejto, para acessar a funcao deve ser invocada
com uso dos parenteses no final da variavel EX: pessoa.nome() -> isso pode ser usado para alterar valores dos atributos
como incrementar ou decrementar a propriedade idade de dentro do objeto assim quando for invocada o atributo dentro do
objeto será alterado. EX: pessoa.altera = function alterIdade(){return pessoa.idade++;)
>Propriedades que recebem funções são chamadas de METODOS,
********************************************************************************************************
	[Aula 004/0015]**Truthy e Falsy**
>Falsy: Undefined, null, NaN, 0, -0, " "(String vazia), false
>Truthy: Todos os outros
Descobrir a representação booleana !!(inverte duas vezes e converte para bool)
********************************************************************************************************
	[Aula 004/0016]**Operador Ternário**
> Condição ? Caso verdade : Caso falso;
********************************************************************************************************
	[Aula 004/0017]**Escopo de variáveis**
Escopo é o local onde a varivel foi declarada, existem declarações globais e locais.
>Sempre utilizar variaveis de escopo local e acessa-las atraves das funções, outra coisa é o "garbage collector",
o JS vê pelo código se a var declarada em escopo local, vai ser utilizada em  outra parte do código, se não for, elimina da memoria aumentando espaço na memoria. 
>Declarar uma variavel em escopo local sem o uso de "var", cria uma variavel com escopo global pq o JS não consegue definir
o escopo e nem utilizar o garbage collector, por isso SEMPRE USE VAR!!!!
Parametros de funçoes são sempre locais,
