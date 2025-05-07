# Lista.JS

#### Tutorial de Manipulação de Listas com Map, Filter e Reduce.

### Manipulação de listas com Map, Filter e Reduce.


## MAP 
**O método map percorre o array transformando cada item usando o callback e retorna um novo array sem modificar o original.** 

 Exemplo 1- Um array de números é criado e guardado na variável numbers, uma segunda variável é criada para guardar a nova lista, o método recebe uma função de **callback** e o elemento atual da lista. numbers.map vai percorrer por toda lista multiplicando o elemento atual por 2 (de acordo como foi passado no callback) e trazendo uma nova lista com os valores modificados **e do mesmo tamanho que a original.**

`var numbers = [2, 4, 8];
var doubles = numbers.map(function(num) {
 return num * 2;
});
console.log (doubles) //[4, 8, 16]`




Exemplo 2- Um array de objetos é criado, no console.log é passado o método map, dentro dele o callback, o elemento e uma arrow function Um array de objetos é criado e armazenado na variável usuarios. No console.log, o método map é utilizado no array usuarios. Dentro do map, é passada uma **arrow function** como callback. Essa arrow function recebe o elemento atual e retorna o valor da idade de cada objeto. O map percorre toda a lista e cria um novo array, contendo apenas os valores de idade de cada usuário."

`let usuarios = [ {idade: 21, nome: 'Alice'},
 {idade: 21, nome: 'Victor'},
 {idade: 20, nome: 'Vitória'},
]
console.log(usuarios.map((usuario) => usuario.idade)) //[21,21,20]`


## Vantagens do Map : 

Permite que cada elemento do array seja percorrido e sujeito a uma operação específica.
Não modifica a lista original, Tem melhor performance que outros métodos de loop. 





                        
## FILTER

 **O filter percorre o array e filtra os itens criando uma nova lista apenas com os que passaram no teste definido pelo callback.** 

Exemplo 1 - Um array de números é criado e armazenado na variável idade, outra variável é criada para armazenar o novo array. filter percorre por idades pegando apenas aquelas que passaram pelo teste no callback o qual pedia apenas idades maiores ou iguais a 18. O filter também exibe uma nova lista, **porém diferente do map nem sempre a lista será do mesmo tamanho que a original**, neste caso do nosso exemplo a lista retornada é bem menor que a original.


`const idades = [32, 33, 16, 40];
const resultado = idades.filter(idade => idade >= 18);
console.log(resultado); // [32, 33, 40]`


## Vantagens Filter: 

- Maneira eficiente de filtrar e transformar dados nos arrays. 
- Economia de Tempo redução de erros 








## REDUCE 
**O reduce percorre cada elemento do array com o objetivo de gerar um valor único.** 

Exemplo = Temos um array de objetos que é guardado na variável produtos, uma nova variável é criada para armazenar o valor reduzido. o reduce é usado no array produtos e vai receber um callback com um **acumulador** e um **elemento**. o reduce vai percorrer o array e vai somar o preço de cada produto de acordo com o que foi passado no callback. o resultado será o total do preço de todos os produtos em uma única lista. 

`const produtos = [
 { nome: "saia", preco: 50 },
 { nome: "bota", preco: 250 },
 { nome: "colar", preco: 15 }
];
const totalPrecoReduce = produtos.reduce((soma, produto) => soma + produto.preco, 0);
console.log("Total preço (reduce):", totalPrecoReduce);`

## Vantagens do Reduce:

- Combina elementos em um único valor
- Oferece uma abordagem elegante e eficaz para transformar os dados.
- Facilita a realização de cálculos. 

