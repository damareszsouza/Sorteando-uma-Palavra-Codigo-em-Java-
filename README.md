# Sorteando-uma-Palavra-Codigo-em-Java-

Ir para o conteúdo principal
Damares Costa de Souza 
Moodle - IFRS

Programação Básica com Java III - Turma 2022B
Painel Meus cursos  PBJIII2022B 4. Procedimentos, Funções e Métodos  4.11.1. Sorteando uma Palavra
4.11.1. Sorteando uma Palavra
O primeiro método que iremos implementar é o método sorteiaPalavra. Este método deve retornar um vetor de char contendo as letras de uma palavra sorteada.  Assim, podemos construir o cabeçalho abaixo:

static char[] sorteiaPalavra()

Veja que o tipo de retorno do método é o mesmo que utilizamos para declarar as variáveis palavra e tabuleiro no método main. Quando desejamos que um  método retorne um vetor, devemos informar o mesmo tipo que usaríamos ao declarar uma variável.

Já vimos em Java como sortear números inteiros, mas como sortear palavras? Infelizmente, não existe nenhum recurso pronto para isso. O que podemos fazer, é sortear um número inteiro e associar cada palavra possível a um número diferente. Em nosso jogo, teremos dez palavras diferentes associadas a nomes de frutas, cada uma associada a um número de 1 a 10, nessa ordem: UVA, BANANA, ABACAXI, MANGA, MARACUJA, LARANJA, MORANGO, LIMAO, ACEROLA, CAQUI.

Assim, podemos construir o código para o método, mostrado abaixo. Este método começa com a declaração da variável sorteio, que irá conter o número associado à palavra sorteada. Sorteamos esse número utilizando o método Math.random (você pode encontrar mais detalhes sobre o uso desse método no curso Programação Básica com Java II).



static char[] sorteiaPalavra() {

       int sorteio = (int)(Math.random()*10)+1;

 

       switch(sorteio) {

             case 1: return new char[]{‘U’,‘V’,‘A’};

             case 2: return new char[]{‘B’,‘A’,‘N’,‘A’,‘N’,‘A’};

             case 3: return new char[]{‘A’,‘B’,‘A’,’C’,’A’,’X’,’I’};

             case 4: return new char[]{‘M’,‘A’,‘N’,’G’,’A’};

             case 5: return new char[]{‘M’,‘A’,‘R’,’A’,’C’,’U’,’J’,’A’};

             case 6: return new char[]{‘L’,‘A’,‘R’,’A’,’N’,’J’,’A’};

             case 7: return new char[]{‘M’,‘O’,‘R’,’A’,’N’,’G’,’O’};

             case 8: return new char[]{‘L’,‘I’,‘M’,’A’,’O’};

             case 9: return new char[]{‘A’,‘C’,‘E’,’R’,’O’,’L’,’A’};

             case 10: return new char[]{‘C’,‘A’,‘Q’,’U’,’I’};

       }

       return new char[0];

}



Utilizamos uma estrutura switch para selecionar a palavra a ser retornada pelo método, com base no valor da variável sorteio. Em cada case desta estrutura há um return, onde um vetor diferente é criado e preenchido. Veja o estilo diferente que utilizamos para criar e preencher o vetor! Essa sintaxe mistura o modo tradicional de se criar um vetor, utilizando o comando new, com uma lista de inicialização. Note que o tamanho do vetor não é informado dentro dos colchetes, mas é inferido pela JVM a partir da quantidade de elementos listados dentro do par de chaves.

Não colocamos o comando break em nenhum case, como tradicionalmente utilizamos, pois o comando return, quando executado, já encerrará a execução do método. Note que na última instrução do método, incluímos um comando return que devolve um vetor vazio. Isso foi necessário, pois o compilador Java raciocina que, se o valor da variável sorteio não for um número de 1 a 10 (o que não poderá acontecer de acordo com o nosso código), o método não retornará nada. Infelizmente, o compilador não é tão experto o suficiente para identificar esse detalhe.

Última atualização: domingo, 1 nov 2020, 20:53
Seguir para...
Academi
Dúvidas? 
Perguntas frequentes

Fale conosco | Suporte | Contato

Informação
Termos e Condições de Uso
Aviso de Privacidade e Proteção de Dados Pessoais
Contato
Rua Gen. Osório, 348, Bento Gonçalves/RS
Siga-nos
Copyright © 2017 - Desenvolvido por LMSACE.com. Distribuído por Moodle
