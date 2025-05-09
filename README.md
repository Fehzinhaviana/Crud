Este projeto tem como objetivo principal demonstrar o funcionamento de um sistema CRUD (Create, Read, Update, Delete) voltado ao gerenciamento de usuários. A aplicação é composta por um backend desenvolvido com Node.js e SQLite, e um frontend responsivo utilizando HTML, CSS, JavaScript e Bootstrap.

Backend: Node.js com Express e SQLite
O servidor é construído com o framework Express, responsável por criar e gerenciar as rotas da aplicação. O banco de dados utilizado é o SQLite3, ideal para projetos de pequeno porte, por não exigir um servidor dedicado e armazenar os dados localmente em um arquivo.

O sistema inicia verificando a existência da tabela usuarios. Caso não exista, ela é criada automaticamente com os campos id (chave primária autoincremental) e nome (campo de texto). O middleware CORS é usado para permitir a comunicação entre o backend e o frontend, enquanto o Body-Parser trata os dados JSON enviados pelas requisições.

O backend expõe as seguintes rotas:

POST /salvar: Cadastra um novo usuário.

GET /usuarios: Retorna todos os usuários cadastrados.

PUT /editar/:id: Atualiza o nome de um usuário existente.

DELETE /deletar/:id: Remove um usuário do banco de dados.

Essas rotas cobrem todas as operações essenciais de um CRUD, permitindo a manipulação total dos registros.

Frontend: HTML, CSS, JavaScript e Bootstrap
A interface do usuário foi desenvolvida com foco na simplicidade e na funcionalidade. O HTML é dividido em seções claras: um formulário para entrada de dados, uma lista dinâmica para exibição dos usuários e áreas para mensagens de sucesso ou erro.

O formulário permite cadastrar novos nomes ou editar usuários existentes. Os dados são enviados ao backend por meio de requisições assíncronas utilizando fetch. Toda interação com o servidor é feita no arquivo script.js, que contém funções como:

salvarUsuario(): Envia um novo usuário via POST.

carregarUsuarios(): Carrega todos os usuários da API.

editarUsuario(id, nome): Preenche o formulário para edição.

deletarUsuario(id): Remove um usuário via DELETE.

A lista de usuários é atualizada automaticamente após cada ação, garantindo que os dados exibidos estejam sempre sincronizados com o banco.

Estilização e Experiência Visual
O CSS personalizado define uma paleta de cores suaves e elementos visuais harmoniosos. O layout é centralizado com bordas arredondadas e uso de sombras para destacar os principais componentes. O Bootstrap oferece responsividade e ícones modernos, melhorando a usabilidade.

Botões de ação possuem efeitos de hover e cores distintas para facilitar a identificação das ações de edição e exclusão. O uso de variáveis CSS permite maior controle e organização da estilização.
