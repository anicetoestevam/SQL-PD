# SQL-PD
Resolva crimes cibernéticos enquanto pratica comandos SQL.


O site do jogo: https://sqlpd.com/

🎯**O que é SQL?**

SQL (Structured Query Language - Linguagem de Consulta Estruturada) é uma linguagem utilizada para acessar e manipular dados armazenados em bancos de dados relacionais.
- Tabelas: Estrutura principal de armazenamento
- Colunas: Campos que definem os tipos de dados
- Linhas: Registros individuais da tabela

🏗️**Estrutura Básica**

```
SELECT nome_da_coluna
FROM nome_da_tabela
WHERE condição;
```
> Importante: Toda instrução SQL deve terminar com ponto e vírgula (;)

📤**Selecionando Dados**

```
SELECT *
FROM funcionarios;
```
> O asterisco (*) retorna todas as colunas da tabela.

🎯**Selecionar Colunas Específicas**

```
SELECT nome, idade
FROM alunos;
```
> Especifique as colunas desejadas separadas por vírgula.

🏗️**Eliminar Duplicatas**

```
SELECT DISTINCT nome
FROM alunos;
```
> Use DISTINCT para remover valores duplicados.

🔍**Filtrando Dados com WHERE**

```
SELECT produto
FROM inventario
WHERE codigo = 'ABC123';
```
> A cláusula WHERE filtra registros baseados em condições específicas. Apenas registros que atendem à condição são retornados.

⚖️**Operadores de Comparação**

| Operador | Descrição | Exemplo |
| --- | --- | --- |
| = | Igual a | quantidade = 10 |
| < | Menor que | preco < 50 | 
| <= | Menor ou igual | idade <= 18 |
| > | Maior que | salario > 3000 | 
| >= | Maior ou igual | nota >= 7 |
| != ou <> | Diferente de | status != 0 | 

**Exemplo com números:** Retirna produtos com quantidade até 10.

```
SELECT produto
FROM estoque
WHERE quantidade <= 10;
```
**Exemplo com Strings:** Retorna produtos que começam com 'A'.

```
SELECT productName
FROM inventory
WHERE productName < 'B';
```
⚠️**Importante:**

> Strings devem estar entre aspas simples: 'texto'
> Letras maiúsculas vêm antes das minúsculas

📤**Operador relacional IN (=, <, >, IN, BETWEEN):** É um dos operadores de comparação que compara um valor a outro de forma exata ou matemática.
 

```
SELECT produto
FROM estoque
WHERE quantidade IN (1, 5, 10);
```
> Filtra por múltiplos valores possíveis. Retorna produtos onde quantidade é exatamente 1, 5 ou 10.

