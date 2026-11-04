# Livrariadb
1. Domínio do Banco de Dados
O domínio escolhido é o gerenciamento de uma livraria.
O banco de dados será utilizado para armazenar e organizar informações sobre livros, autores, editoras, clientes, vendas, pagamentos e categorias.

2. Contextualização
A livraria é uma empresa que comercializa livros de diferentes gêneros e autores. Ela precisa controlar seu estoque, cadastrar clientes, registrar vendas e acompanhar os pagamentos realizados.
Sem um Sistema Gerenciador de Banco de Dados Relacional (SGBD), essas informações poderiam ficar espalhadas em planilhas e arquivos separados, dificultando a organização e a consulta dos dados.

Os principais problemas seriam:
- Dificuldade para localizar informações sobre livros e clientes.
- Duplicidade de registros.
- Erros no controle de vendas e pagamentos.
- Dificuldade para consultar o estoque.
- Falta de integração entre as informações.


3. Proposta de melhoria
A solução proposta é a utilização do MySQL como SGBD relacional.
Com ele, a livraria poderá centralizar suas informações, relacionar os dados por meio de chaves primárias e estrangeiras e realizar consultas de forma rápida e organizada.
O sistema permitirá controlar livros, autores, editoras, categorias, clientes, vendas, itens vendidos e pagamentos.


4. Modelagem lógica do banco de dados
O banco de dados será composto pelas seguintes tabelas:
Tabela	Finalidade
livros	Cadastro dos livros
autores	Cadastro dos autores
editoras	Cadastro das editoras
categorias	Classificação dos livros
livro_autor	Relacionamento entre livros e autores
livro_categoria	Relacionamento entre livros e categorias
clientes	Cadastro dos clientes
vendas	Registro das vendas
itens_venda	Livros vendidos em cada venda
pagamentos	Registro dos pagamentos

As chaves primárias identificam cada registro de forma única. As chaves estrangeiras permitem relacionar as tabelas.


5. Aplicação das Formas Normais
- 1FN — Primeira Forma Normal: cada campo armazena apenas um valor, sem listas ou grupos de valores repetidos.
- 2FN — Segunda Forma Normal: todos os campos dependem da chave primária completa. Nas tabelas de relacionamento, como livro_autor, a chave é composta por id_livro e id_autor.
- 3FN — Terceira Forma Normal: os campos que não são chaves dependem diretamente da chave primária, sem dependências transitivas. Por exemplo, os dados da editora ficam separados dos dados do livro.
- 4FN — Quarta Forma Normal: os relacionamentos independentes de muitos para muitos são separados. Assim, autores e categorias ficam em tabelas próprias, relacionadas aos livros por tabelas intermediárias.
A aplicação dessas formas normais reduz a duplicidade de informações e facilita a manutenção do banco de dados.


6. Instruções SQL
Os scripts SQL do projeto devem conter:
1. Criação do banco livraria_db.
2. Criação das tabelas com seus campos, tipos de dados, chaves primárias e estrangeiras.
3. Inserção de pelo menos cinco registros em cada tabela.
4. Criação de 15 consultas contextualizadas, com os comandos INNER JOIN, WHERE, LIKE, GROUP BY, ORDER BY, BETWEEN e SUM.
As consultas devem apresentar uma pergunta relacionada à livraria, o comando SQL utilizado e o resultado obtido no MySQL Workbench.


7. Dump do banco de dados
O dump será realizado pelo MySQL Workbench, utilizando a opção de exportação de dados.
O arquivo deverá conter tanto a estrutura das tabelas quanto os registros inseridos.
O arquivo será salvo no formato .sql, permitindo que o banco de dados seja recriado em outro ambiente.


8. Comitar o projeto
O projeto será enviado para um repositório no GitHub, contendo os scripts SQL e os demais arquivos necessários para a entrega.


9. Subir no classroom:
   9.1. Link do Repositório com os scripts,
   9.2. Print da modelagem.
