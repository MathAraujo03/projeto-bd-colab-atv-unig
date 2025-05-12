Este notebook em Python, projetado para o Google Colab, demonstra operações básicas de um sistema de gerenciamento de banco de dados (SGBD) com SQLite, simulando uma loja com clientes, produtos e vendas.

1. Conexão e Criação do Banco de Dados

Importa sqlite3 e os.

Define o banco como loja.db.

Remove o arquivo anterior, se existir, para reiniciar o banco.

Cria uma nova conexão com loja.db.

2. Criação de Tabelas

Cria três tabelas:

Clientes (id, nome, e-mail).

Produtos (id, nome, preço).

Vendas (id, id_cliente, id_produto, quantidade, data), com foreign keys para Clientes e Produtos.

Salva as alterações com conn.commit().

3. Inserção de Dados

Insere:

3 clientes.

4 produtos.

4 vendas com data atual.

4. Consultas (SELECT)

Clientes: lista todos os registros.

Produtos acima de R$200: usa condição WHERE.

Vendas detalhadas: JOIN entre Vendas, Clientes e Produtos, mostrando nome do cliente, produto e valor total.

Produtos comprados por "Ana Silva": JOIN com filtro por cliente.

Total gasto por cliente: usa funções de agregação (SUM e GROUP BY) e ordena por valor gasto.

5. Exibição dos Resultados

Cada consulta imprime os resultados diretamente na saída do Colab.

6. Fechamento da Conexão

Finaliza a conexão com conn.close() para liberar recursos e salvar alterações.
