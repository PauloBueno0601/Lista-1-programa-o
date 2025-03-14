# Lista-1-programa-o
Ponderada semana 6
 
# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
a) A saída será undefined seguido de erro 

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

A resposta é a letra "a" porque a váriavel foi declarava como var, então é uma variável global, o console.log reconhece que possui uma variável mas não reconhece seu valor, por isso será undefined. Já no segundo acontece erro pos let não é uma variável global, então ela não lê nada no console, por isso erro.

**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

A resposta é a letra "a" pois da maneira que está escrita o código está lendo apenas o b, por isso não funciona da maneira correta.

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

b) O código imprime 200.

c) O código imprime 50.

d) O código gera um erro.

A resposta correta será a letra b, ele imprimirá 200 pois é um caso de switch, e após chamar o caso de eletrônicos não foi declarado o break para ir para o próximo caso, então quando solicidado eletrônico, o console está lendo vestuário.

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

d) 24

A resposta será "d" pois, no numeros.map, multiplica todos os valores do array por 2, já no filter ele filtra somente os valores maiores que 5, já no reduce ele soma todos os valores o que resulta em 24.
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"]

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

A resposta é a letra "C", pois no lista.splice, mostra que o elemento 1 (maça) da lista será trocado, e o número 2 mostra que dois elementos será trocado, e serão substituidos por abacaxi e manga.
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

Resposta: Letra "A"  Classes em Java Script são declaradas usando o prefixo class e com elas é possível criar subclasses utilizando os seus atributos e métodos, para isso é necessário utilizar um extends e informar o nome da classe que está sendo usada como a classe pai, sendo assim letra a está correta.
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras.

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

Resposta: letra 'A'. O uso de 'extends Pessoa' indica que a classe funcionaria está herdando da classe Pessoa e ao usar super(nome, idade) ele acessa os atribudos da classe Pessoa.  já  no item II: O método apresentar() da classe Funcionario sobrepôe o apresentar() da classe Pessoa mas faz isso incrementando o método da classe Pessoa dentro dele usando super.apresentar(). E no item III: O código roda perfeitamente pois, é possível ter uma herança de classe com classes e subclasses. 

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

A resposta correta é a "B" O polimorfismo é um dos pilares da Programação Orientada a Objetos (POO) e permite que objetos de diferentes classes possam ser tratados como objetos de uma classe base, mas respondam a métodos de maneira específica de acordo com sua própria implementação. Isso significa que diferentes objetos podem responder à mesma mensagem, então é correta, já a razão está incorreta pois, em JavaScript, não existe suporte nativo para sobrecarga de métodos.

______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```
Resposta:


 function somaArray(numeros) {
    var soma = 0  // declarando a variável soma
     for (let i = 0; i < numeros.length; i++) { // o correto é numeros.length não numeros.size
         soma += 2*numeros[i]; // para somar todos os números o correto é usar += e não =
     }
     return soma;
 } 
 console.log(somaArray([1, 2, 3, 4]));

______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.


class Produto {
    constructor(nome, preco) {
        this.nome = nome;
        this.preco = preco;
    }

    calcularDesconto() {
        this.preco *= 0.9; // Aplica 10% de desconto
        console.log(this.preco);
    }
}

class Livro extends Produto {
    constructor(nome, preco) {
        super(nome, preco); // Chama o construtor da classe pai (Produto)
    }

    calcularDesconto() {
        this.preco *= 0.8; // Aplica 20% de desconto
        console.log(this.preco);
    }
}

Herança: A classe Livro herda atributos e métodos da classe Produto, permitindo reutilização de código e extensibilidade.
Sobrescrita de método: O método calcularDesconto() é redefinido na classe Livro para aplicar um desconto específico para livros (20%).
Polimorfismo: O mesmo método (calcularDesconto()) tem comportamentos diferentes dependendo da classe em que é chamado.
