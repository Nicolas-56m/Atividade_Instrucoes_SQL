# Atividade_Instrucoes_SQL

/* Instrução 1 */
USE vendas_informatica;
SELECT * FROM produto;

/* Instrução 2 */
USE vendas_informatica;
SELECT nome_produto, marca, estoque FROM produto

/* Instrução 3 */
USE vendas_informatica;
SELECT nome_produto, categoria, preco_unitario, data_cadastro 
FROM produto 
ORDER BY marca ASC;

/* Instrução 4 */
USE vendas_informatica;
SELECT nome_produto, marca, estoque, data_cadastro 
FROM produto 
ORDER BY data_cadastro ASC;

/* Instrução 5 */
USE vendas_informatica;
SELECT * FROM cliente;

/* Instrução 6 */
USE vendas_informatica;
SELECT nome_cliente, email, cidade, estado 
FROM cliente;

/* Instrução 7 */
USE vendas_informatica;
SELECT nome_cliente, cidade, estado 
FROM cliente 
ORDER BY estado ASC;

/* Instrução 8 */
USE vendas_informatica;
SELECT nome_cliente, email, estado 
FROM cliente 
ORDER BY data_cadastro DESC;

/* Instrução 9 */
USE vendas_informatica;
SELECT * FROM venda;

/* Instrução 10 */
USE vendas_informatica;
SELECT cliente.nome_cliente, data_venda, preco_unitario_venda, forma_pagamento 
FROM cliente 
INNER JOIN venda;

/* Instrução 11 */
USE vendas_informatica;
SELECT produto.nome_produto, data_venda, quantidade, status_venda 
FROM produto 
INNER JOIN venda;

/* Instrução 12 */
USE vendas_informatica;
SELECT produto.nome_produto, produto.preco_unitario, venda.forma_pagamento 
FROM produto 
INNER JOIN venda 
ON venda.id_produto = produto.id_produto 
WHERE venda.forma_pagamento 
IN ('Pix', 'Boleto');

/* Instrução 13 */
USE vendas_informatica;
SELECT cliente.nome_cliente, produto.nome_produto, venda.data_venda, quantidade 
FROM cliente 
INNER JOIN produto 
INNER JOIN venda;

/* Instrução 14 */
USE vendas_informatica;
SELECT produto.nome_produto, venda.desconto_percentual, forma_pagamento 
FROM produto 
INNER JOIN venda 
ORDER BY data_venda ASC;

/* Instrução 15 */
USE vendas_informatica;
SELECT produto.nome_produto, cliente.nome_cliente, venda.desconto_pagamento, status_venda 
FROM produto
INNER JOIN venda
ORDER BY status_venda DESC;

/* Instrução 16 */
USE vendas_informatica;
