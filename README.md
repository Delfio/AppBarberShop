
----------- Suscrase ----------------
Utilizando uma biblioteca para atualizar a versão do js do node - Sucrase - ficando "import routes from './routes';etc..
Sintaxe antiga utilizada pelo node - const routes = require('./routes')

----------- Nodemon ----------------
Nodemon para gerar um script para automatizar a inicialização do app.
Necessario configurar para o sucrase, para ele executar com o sucrase não com o nodemon direto!. Criar um arquivo nodemon.js
no arquivo colocar {execMap: {"js": sucrase-node}} - "yarn dev"

----------- Sequelize ----------------
ORM - abstração de banco de dados --- banco postgres ou outro, não importa, funciona na mesma linguagem -
Tabelas viram models -> users, companies, projects, ---> User.js, Company.js, Project.js
Manipulação dos dados do banco CRUD -> sem linguagem sql, somente javascript - pesquisar documentação.
Migrations - controle de versões do banco, contem instruções para CRUD, caso erre a migration ou passe pra outro ambiente,
ela não pode ser mais editada... necessário criar outra migration. Cada Migration é expecifico para 1 tabela
Arquitetura MVC.
Model não possui regra de negocio somente abstração do banco
Controller Ponto de entrada das requisições da aplicação, uma rota geralmente é associada a um metodo do controller
devsController.store
View é o retorno do cliente, aplicações que não são rest as views retornam o html, no padrão rest retorna um json
para a aplicação.

O controller será criado somente quando existir outra entidade no banco de dados, cada model possui seu controller.
Pode ocorrer que um Controller não possua model - sesionController, criação de sesão
o controller tem 5 métodos: index, show, store, update, delete
