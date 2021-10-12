# Raspador do Jornal da USP - Editoria de Saúde
Olá! 

Esse repositório abriga um raspador que criei para a disciplina de Pensamento Computacional, do primeiro trimestre do Master em Jornalismo de Dados, Automação e Data Storytelling do Insper. 

## Descrição

Este raspador foi feito na linguagem **Python**, versão 3.7.12, usando o Google Colaboratory. 

## Objetivo

O objetivo do trabalho foi tornar mais fácil o trabalho de ronda de notícias feito pelos jornalistas de saúde. Por isso, criei um código para raspar o site [Jornal da USP](https://jornal.usp.br), na editoria de Saúde, e retornar um arquivo .csv todas as notícias de um tema específico, inserido pelo usuário.

## Por que um raspador do Jornal da USP?

Considerando que a USP é a maior universidade da América Latina, as pesquisas feitas na instituição têm uma grande diversidade de temas e estão conectadas com os debates mais relevantes em suas áreas de estudo. Muitas vezes, o jornalista de saúde tem dificuldades de encontrar pautas relevantes para a editoria em que escreve e tende a repercutir mais o progresso da ciência de países da América do Norte e Europa do que do Brasil.

Com esse raspador, meu objetivo é tornar mais fácil o dia a dia dos profissionais da imprensa especializada no Brasil, além de promover a divulgação científica da USP.

## Como o raspador funciona?

O público-alvo da ferramenta desenvolvida é o jornalista, que não necessariamente tem um conhecimento técnico de programação. Por isso, o raspador funciona em softwares que executam o Python versão 3.7.12 e tenham interface gráfica. Recomendo executá-lo no Google Colaboratory, ferramenta a qual todos os que têm uma conta no Google tem acesso. A seguir, explico como funciona o passo a passo nesta ferramenta.

* Importe o arquivo .ipynb no Google Colaboratory
* Execute a célula em que o código aparece
* Na área de saída do código, responda à pergunta e insira um tema relativo à saúde que deseja pesquisar
* Aperte -enter e aguarde o código ser executado, na nuvem. 
* Abra a área de arquivos do Colaboratory e encontre o arquivo .csv escrito

Considerando que o Google Colaboratory é executado na nuvem, é necessário baixar o arquivo criado para tê-lo em sua máquina. 

## Bibliotecas usadas

O código foi criado usando as bibliotecas [csv](https://docs.python.org/3/library/csv.html) e [requests](https://docs.python-requests.org/en/latest/). 

A primeira tem a função de criar um arquivo separado com vírgulas com as informações que encontramos. Já a segunda nos permite obter e manipular o código de sites da internet, que funcionam sob o protocolo http.

## Detalhamento do código

O código criado tem três partes: 
* **Manipulação de strings**: Pede um tema do usuário e, dele, retira espaços e letras em caixa alta. Também substitui os espaços entre as palavras por _ , para compor o nome do arquivo criado. Feito usando métodos e funções nativas do Python (strip, lower, replace)
* **Raspagem do site**: Busca o código html da URL inserida (página de notícias de saúde do Jornal da USP), encontra todos os trechos que contém um link e um título da matéria e os formata em listas. Também passa página a página procurando por esse termo inserido pelo usuário.
* **Criação de arquivo .csv**: Cria um arquivo .csv, duas colunas (_Título_ e _link_) e depois o preenche com as informações dos links encontrados na raspagem

## O que o raspador não faz 
* Busca matérias relacionadas a áreas que não da saúde 
* Registra informações além de título e link, como autor e meta-descrição
* Busca matérias com mais de um ano

## Ideias para colaborar com o raspador
O raspador de notícias sobre saúde do Jornal da USP foi criado em um contexto de pandemia, em que a ciência, o jornalismo científico e a colaboração entre profissionais se mostrou muito importante. O site raspado é construído em WordPress, o que facilita reproduzir esse raspador para outros sites. Abaixo, algumas ideias a serem executadas tendo como base o código criado por mim: 
* Criar raspagem de outras editorias do Jornal da USP
* Criar um raspador de alguma outra instituição de pesquisa brasileira
* Automatizar o código, retornando um arquivo .csv periodicamente

Muito obrigada por ler até aqui! esse código é fruto do meu primeiro trimestre enquanto programadora, e é muito satisfatório pensar que posso compartilhá-lo com mais pessoas.
