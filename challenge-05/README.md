# Challenge 5#

answered by [@fepas](https://github.com/fepas)

```js
/*
Crie uma variável qualquer, que receba um array com alguns valores aleatórios
- ao menos 5 - (fica por sua conta os valores do array).
*/
var arr = [0, 1, 2, 3, 4];

/*
Crie uma função que receba um array como parâmetro, e retorne esse array.
*/
function returnArr(array){
    return array;
}

/*
Imprima o segundo índice do array retornado pela função criada acima.
*/
returnArr(arr)[1];

/*
Crie uma função que receba dois parâmetros: o primeiro, um array de valores; e o
segundo, um número. A função deve retornar o valor de um índice do array que foi passado
no primeiro parâmetro. O índice usado para retornar o valor, deve ser o número passado no
segundo parâmetro.
*/
function arrPosition(array, position){
    return array[position];
}


/*
Declare uma variável que recebe um array com 5 valores, de tipos diferentes.
*/
var arrTypes = [true, null, 7, 'string', false];

/*
Invoque a função criada acima, fazendo-a retornar todos os valores do último
array criado.
*/
arrPosition(arrTypes, 0);
arrPosition(arrTypes, 1);
arrPosition(arrTypes, 2);
arrPosition(arrTypes, 3);
arrPosition(arrTypes, 4);

/*
Crie uma função chamada `book`, que recebe um parâmetro, que será o nome do
livro. Dentro dessa função, declare uma variável que recebe um objeto com as
seguintes características:
- esse objeto irá receber 3 propriedades, que serão nomes de livros;
- cada uma dessas propriedades será um novo objeto, que terá outras 3
propriedades:
    - `quantidadePaginas` - Number (quantidade de páginas)
    - `autor` - String
    - `editora` - String
- A função deve retornar o objeto referente ao livro passado por parâmetro.
- Se o parâmetro não for passado, a função deve retornar o objeto com todos
os livros.
*/
function book(bookName){
    var response;

    var books = {
      'Eragon' : {
        quantidadePaginas: 357,
        autor: 'Cris Paolini',
        editora: 'Rocco'
      },
      'Eredin' : {
        quantidadePaginas: 357,
        autor: 'Fepas Campos',
        editora: 'LuckyCat'
      },
      'Eldest' : {
        quantidadePaginas: 603,
        autor: 'Cris Paolini',
        editora: 'Leya'
      }    
    }
    
    return !bookName ? books : books [ bookName ];
  }

/*
Usando a função criada acima, imprima o objeto com todos os livros.
*/
book();

/*
Ainda com a função acima, imprima a quantidade de páginas de um livro qualquer,
usando a frase:
"O livro [NOME_DO_LIVRO] tem [X] páginas!"
*/
console.log('O livro Eldest tem ' + book('Eldest').quantidadePaginas + ' páginas!');

/*
Ainda com a função acima, imprima o nome do autor de um livro qualquer, usando
a frase:
"O autor do livro [NOME_DO_LIVRO] é [AUTOR]."
*/
console.log('O autor do livro Eldest é ' + book('Eldest').autor + '.');

/*
Ainda com a função acima, imprima o nome da editora de um livro qualquer, usando
a frase:
"O livro [NOME_DO_LIVRO] foi publicado pela editora [NOME_DA_EDITORA]."
*/
console.log('O livro Eldest foi publicado pela editora ' + book('Eldest').editora + '.');
```