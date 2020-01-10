API construída em NodeJS, utilizando o framework Express e o banco de dados MySQL.
O objetivo da API é oferecer um serviço de agendamento e consulta de serviços em um Pet-shop.


Após clonar o projeto, siga os passos para instalar as dependencias e iniciar a aplicação, é necessário ter o NodeJS previamente instalado no computador.

$ cd pet-shop
$ npm install
$ npm start


Rotas de resposta da API:
<br>
<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos<br>
<br>
Listar dados<br>
método HTTP: GET<br>
Resposta: Retorna um objeto JSON com todos os serviços agendados no banco de dados.<br>
<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos<br>
<br>
Criar registro<br>
método HTTP: POST<br>
Resposta: Envia para o servidor uma requisição com os campos necessários para ser agendado um novo serviço, caso a requisição tenha sucesso é retornado um objeto JSON criado.<br>

Campos necessários para a requisição:

-> cliente: String com o nome do cliente 
-> pet: String com o nome do pet
-> servico: String com o nome do serviço a ser agendado no pet-shop
-> status: String com o status do serviço (Agendado/Cancelado/Adiado...)
-> observacoes: String com as observações a respeito do animal
-> data: Data no formato DD/MM/YYYY, informando a data do serviço
<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos/id<br>
<br>
Buscar por ID<br>
Método HTTP: GET<br>
Resposta: Retorna um objeto JSON associado ao ID passado na url da requisição.<br>
<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos/id<br>
<br>
Deletar Registro<br>
Método HTTP: DELETE<br>
Resposta: Deleta o registro associado ao ID passado como parâmetro.<br>
<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos/id<br>
<br>
Editar Registro<br>
Método HTTP: PATCH<br>
Resposta: Envia uma requisição ao servidor passando no body os campos a serem editados em um registro existente, deve ser passado o id do registro na url da requisição.<br>
<br>
<br>