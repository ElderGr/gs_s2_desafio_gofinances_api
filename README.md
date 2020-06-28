# Desafio GoStack: TypeORM e upload de arquivos
Projeto desenvolvido durante a Semana 2 do bootcamp GoStack onde, por meio de uma aplicação node.js com typescript, deveriamos evoluir os conceitos de arquitetura de software exercitados no desafio anterior com o acrescimo do TypeORM e o upload de arquivos com o multer.

## ⚙ Pré-requisitos
Para a execução do projeto em seu ambiente local é necessário possuir instalado:

- NodeJS em sua versão LTS
> https://nodejs.org/en/

## 🛠 Guia de instalação
1. Faça download do projeto do github
2. Após ter feito download do projeto, acesse o diretorio raiz do mesmo via linha de comando
3. No terminal, execute o comando npm install para instalar as dependências do projeto (Caso você tenha o yarn instalado em sua máquina, execute apenas yarn para a instalação das dependencias)
4. Tendo finalizado o processo anterior, execute o comando npm run dev (ou yarn dev), para executar a API e a partir desse momento a API estará sendo executada de forma local na porta 5000

## 📩 Rotas disponíveis na API
*`POST /transactions`: A rota recebe `title`, `value`, `type` e `category` dentro do corpo da requisição, sendo o `type` o tipo da transação, que deve ser `income` para entradas (depósitos) e `outcome` para saídas (retiradas). Ao cadastrar uma nova transação;

*`GET /transactions`: Essa rota retorna uma listagem com todas as transações que você cadastrou até agora, junto com o valor da soma de entradas, retiradas e total de crédito;

*`DELETE /transactions/:id`: A rota deleta uma transação com o `id` presente nos parâmetros da rota;

*`POST /transactions/import`: A rota permite a importação de um arquivo com formato `.csv` contendo as mesmas informações necessárias para criação de uma transação `id`, `title`, `value`, `type`, `category_id` onde cada linha do arquivo CSV deve ser um novo registro para o banco de dados, e por fim retorne todas as transactions que foram importadas para seu banco de dados. O arquivo `csv`, deve seguir o seguinte modelo.

## 📋 Comandos disponíveis
* dev:server: execução da API em ambiente local
* test: execução dos testes validando o desenvolvimento da api
* typeorm: execução dos comandos disponiveis da cli do typeorm
* build: gera o bundler dos arquivos Typescript da aplicação

## 📙 Enunciado
Todo o desafio foi realizado baseado no enunciado:
> https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-database-upload
