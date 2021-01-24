### 1 Nesse exercício, dado um número, encontre o seu oposto.**

Exemplos:

1: -1

14: -14

-34: 34


 ~~~javascript 
 function oposto( numero )

{

   if (numero => 0)

  return numero * -1

} ~~~





////////////////////////////////////////////////////////



**2 Dado um array de inteiros representados como strings e números, retorne a soma dos valores do array como se todos os itens fossem números.**



Exemplo de array passado como parâmetro:



[ 1, '2', '3', 4, 5 ]; // Neste caso, retornaria 15

Sua função deve retornar um número.





function somaMista( arr )

{

 let soma = 0;

 for (let i in arr){

  var num = parseFloat(arr[i])

  soma += num

 }

 //

   return soma

 }



///////////////////////////////////////////////////////////////////////





**Crie uma função que recebe dois argumentos:**



1) Um array de objetos, onde cada objeto possui propriedades relativas a temporada, o time e o país vencedor da Liga dos Campeões.



2) País (uma string, por exemplo, 'Portugal')



Sua função deve retornar o número de vezes que uma equipe de um determinado país ganhou. Retorne 0 se não houver vitórias.



Por exemplo, se a matriz de entrada for a seguinte:



const winnerList1 = [

 {season: '1999-00', team: 'Real Madrid', country: 'Spain'},

 {season: '2000-01', team: 'Bayern Munich', country: 'Germany'},

 {season: '2001-02', team: 'Real Madrid', country: 'Spain'},

 {season: '2002-03', team: 'Milan', country: 'Italy'},

 {season: '2003-04', team: 'Porto', country: 'Portugal'}

]

Os possíveis resultados possíveis são:



countWins(winnerList1, 'Spain') => deve retornar 2

countWins(winnerList1, 'Portugal') => deve retornar 1

countWins(winnerList1, 'Sportland') => deve retornar 0



const winnerList1 = [

 { season: '1996–97', team: 'Borussia Dortmund', country: 'Germany' },

 { season: '1997–98', team: 'Real Madrid', country: 'Spain' },

 { season: '1998–99', team: 'Manchester United', country: 'England' },

 { season: '1999–00', team: 'Real Madrid', country: 'Spain' },

 { season: '2000–01', team: 'Bayern Munich', country: 'Germany' },

 { season: '2001–02', team: 'Real Madrid', country: 'Spain' },

 { season: '2002–03', team: 'Milan', country: 'Italy' },

 { season: '2003–04', team: 'Porto', country: 'Portugal' },

 { season: '2004–05', team: 'Liverpool', country: 'England' },

 { season: '2005–06', team: 'Barcelona', country: 'Spain' },

 { season: '2006–07', team: 'Milan', country: 'Italy' },

 { season: '2007–08', team: 'Manchester United', country: 'England' },

 { season: '2008–09', team: 'Barcelona', country: 'Spain' },

 { season: '2009–10', team: 'Internazionale', country: 'Italy' },

 { season: '2010–11', team: 'Barcelona', country: 'Spain' },

 { season: '2011–12', team: 'Chelsea', country: 'England' },

 { season: '2012–13', team: 'Bayern', country: 'Germany' },

 { season: '2013–14', team: 'Real Madrid', country: 'Spain' },

 { season: '2014–15', team: 'Barcelona', country: 'Spain' },

 { season: '2015–16', team: 'Real Madrid', country: 'Spain' }

];



///////////////////////////////////////////////////////////////////////////////////





\### 4 Quem deveria ganhar uma bicicleta?

Eu sou pai de três filhos maravilhosos.

Antes do início do ano letivo, prometi a eles que compraria uma bicicleta para quem trouxesse as melhores notas no final do ano. Agora eu preciso cumprir a promessa e vou precisar da sua ajuda.



Você tem 3 objetos de entrada (os boletins) com as disciplinas e notas (que vão de 1 até 10). Por exemplo:



{

 'matematica': 6,

 'historia': 8,

 'fisica': 9,

 'geografia': 2,

 'quimica': 9

}

Por favor, retorne o seguinte



'Eu preciso comprar uma bicicleta para meu primeiro filho.' // a soma das notas é a mais alta no primeiro diário.



'Eu preciso comprar uma bicicleta para meu segundo filho.' // a soma das notas é a mais alta no segundo diário.



'Eu preciso comprar uma bicicleta para meu terceiro filho.' // a soma das notas é a mais alta no terceiro diário.

Se dois ou três filhos têm as mesmas notas mais altas, você precisa escolher o mais jovem. Use a tabela de idade que é constante e já está pré-carregada:





const tabelaIdades = {

 'idadePrimeiroFilho': 14,

 'idadeSegundoFilho': 9,

 'idadeTerceiroFilho': 8

}





recompensa(

​                 {

​                  'matematica': 6,

​                  'historia': 7,

​                  'fisica': 8,

​                  'geografia': 9,

​                  'quimica': 10

​                 },

​                 {

​                  'matematica': 8,

​                  'historia': 7,

​                  'fisica': 8,

​                  'geografia': 9,

​                  'quimica': 10

​                 },

​                 {

​                  'matematica': 6,

​                  'historia': 5,

​                  'fisica': 5,

​                  'geografia': 9,

​                  'quimica': 10

​                 }





​             

​             

function recompensa(boletim1, boletim2, boletim3) {

 

 var soma1 = 0;

 var soma2 = 0;

 var soma3 = 0;



 

for (let i in boletim1) {

   soma1 += boletim1[i];

};

  

for (let i in boletim2) {

   soma2 += boletim2[i];

};

 

for (let i in boletim3) {

   soma3 += boletim3[i];

};

 

 if(soma1 > soma2 && soma1 > soma3){

  return 'Eu preciso comprar uma bicicleta para meu primeiro filho.'

 }

 else if(soma2 > soma1 && soma2 > soma3){

  return 'Eu preciso comprar uma bicicleta para meu segundo filho.'

 }

 else if(soma3 > soma2 && soma3 > soma1){

  return 'Eu preciso comprar uma bicicleta para meu terceiro filho.'

 }

 else if( soma1 == soma2 && soma1 > soma3){

 return 'Eu preciso comprar uma bicicleta para meu segundo filho.'}

 

  else if( soma1 == soma2 && soma1 > soma3){

 return 'Eu preciso comprar uma bicicleta para meu terceiro filho.'}

 

  else if( soma2 == soma3 && soma2 > soma1){

 return 'Eu preciso comprar uma bicicleta para meu terceiro filho.'}

 

  else if( soma1 == soma2 && soma2 == soma3){

 return 'Eu preciso comprar uma bicicleta para meu terceiro filho.'}

}

  



  ///////////////////////////////////////////////////////////////////





\### 5 Seu objetivo neste desafio é implementar uma função de diferença, que subtrai uma lista da outra e retorna a lista resultante.



Ele deve remover todos os valores da lista a, que estão presentes na lista b.



arrayDiff([1,2], [1]); // Retorna [2]

Se um valor estiver presente em b, todas as suas ocorrências devem ser removidas de a:



function arrayDiff(a, b)

{

 

 

 for (let i of b){

 

 for (let j = a.length; j >= 0; j--){

  

  if ( i == a[j]){

   a.splice(j,1)

  }

 }

 }

 return a;

}



///////////////////////////////////////////////////////////////////////////////////////////////





\### 6 No número de 6 dígitos abaixo:



283910

91 é a maior sequencia de 2 dígitos consecutivos.



No número de 10 dígitos abaixo:



1234567890

67890 é a maior sequencia de 5 dígitos consecutivos.



Complete a função que irá retornar a maior sequencia de 5 dígitos consecutivos encontrada em qualquer número de entrada.



O número na entrada será passado como uma string somente com dígitos, nenhuma letra.



O retorno deverá ser um número inteiro. O número passado pode ter no mínimo 5 dígitos e no máximo 1000 dígitos.





function solucao( digitos )

{

 let arr = [];

 let num = 0;

 

 for (let i =0; i < digitos.length; i++){

  arr.push(digitos[i] + digitos[i + 1]+digitos[i + 2] + digitos[i + 3] + digitos[i + 4]);

 }

 for (let i = 0; i < arr.length; i++){

  if(arr[i] > num){

   num = arr[i];

  }

}

  return parseFloat(num);

}