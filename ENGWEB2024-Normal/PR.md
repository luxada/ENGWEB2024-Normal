começei por transformar o csv fornecido num json array através do script.py
de seguida, no json array, alterei o campo "idcontrato" para "_id"



utilizei o script-db.py para colocar o json no mongodb


ex1:

comecei por gerar a estrutura do exercicio com o seguinte comando:

npx express-generator --no-view ex1

Depois, criei duas novas diretorias, "models" - para guardar o schema do MongoDB e "controllers" - para guardar as interações com a base de dados

Depois criei as rotas para a API, que estão no ficheiro "routes/contratos.js".

Também foi necessário mudar o ficheiro app.js para fazer a ligação entre o Mongoose e o MongoDB.

Antes de correr a API, instalei as dependências necessárias com o comando:

npm install

E depois instalei o Mongoose com o comando:

npm install mongoose

A rota que tem a entidade como query string (GET /contratos?entidade=X) utiliza o NIPC da entidade



ex2:


Para desenvolver a interface, utilizei o PUG, criando um ficheiro para cada uma das 3 páginas da interface (index, contrato e entidade).

A interface alimenta-se da API, utilizando o axios para fazer pedidos.

Criei um novo ficheiro de rotas na diretoria "routes", chamado "entidades.js", para lidar com o pedido da página de uma entidade específica.

 Também é calculado o montante total dos contratos associados a essa entidade, pois não estava uma rota para isso na API e a interface necessitava dessa informação.
