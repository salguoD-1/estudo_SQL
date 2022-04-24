# O que é um banco de dados?

Um banco de dados é basicamente qualquer coleção de dados relacionados.
	

Por exemplo:

* Uma lista telefônica

* Uma lista de tarefas

* Base de usuários do Facebook

* Uma lista de compras

Todos os itens citados acima são coleções de dados relacionados. Por exemplo, a lista telefônica armazena o nome e o número de uma pessoa, há uma coleção de dados agrupados.

Banco de dados podem ser armazenados de diferentes formas:

* Em um papel

* Na sua mente

* Em um computador

Por exemplo, uma lista com os seus cinco melhores amigos estão armazenados em sua mente.


## A Amazon armazena trilhões de informações

* Armazenam informações como produtos, reviews, pedidos, usuários etc.

* Todas as informações são armazenadas em um computador, computadores são excelentes em armazenar informações.

# Sistema de gerenciamento de banco de dados(SGBD ou DBMS)

* SGBD é basicamente um software que nos permite criar e gerenciar o nosso banco de dados de forma especial, ele facilita o gerenciamento de forma fácil.

* Além disso, o SGBD ajudam a lidar com a segurança dos dados, onde apenas quem tem a senha de acesso pode fazer uso do SGBD.

* Ajuda a fazer backup dos seus dados, e ajuda no processo de importar/exportar dados.

* Por exemplo a Amazon faz uso de um SGBD para processar informações em seu site, onde informações são enviadas e recebidas.

# CRUD

CRUD é uma sigla que significa:
* CREATE:
	* Criar

* READ:
	* Ler

* UPDATE:
	* Atualizar

* DELETE:
	* Excluir

CRUD representa as quatros principais operações que são feitas em um banco de dados.

# Dois tipos de banco de dados

Os dois principais tipos de banco de dados são:

* Banco de dados relacionais(SQL)
	* Basicamente organiza os dados em uma ou mais tabelas.
	
	* Cada tabela há linhas e colunas.

	* Possui uma chave de identificação única para cada linha.

* Banco de dados não relacionais(noSQL)
	* Basicamente organiza os dados de uma forma diferente, o que foge da tabela tradicional.

	* Por exemplo, armazenam informações em key-value(valore-chave), documentos(JSON, XML), gráficos e tabelas flexiveis.


# Sistema de gerenciamento de banco de dados relacionais(SGBDR ou RDBMS)

* Basicamente ajuda a criar e manter(gerenciar) um banco de dados relacional.
	* Alguns exemplos são: MySQL, Oracle, PostgreSQL, mariaDB, etc.

* SQL(Structured Query Language) ou Linguagem de Consulta Estruturada
	* É uma linguagem padronizada para interagir com sistemas de gerenciamento de dado relacional.

	* É uma linguagem utilizada para realizar operações CRUD e outras atividades administrativas do sistema.

	* É utilizada para definir tabelas e estruturas.


## Exemplo de banco de dados não relacional(noSQL)

O exemplo abaixo armazena os arquivos no formato JSON(JavaScript Object Notation)

```javascript
[{
    "_id": 1345,
    "name": "Douglas",
    "major": "Sistemas de informação"
}, {
    "_id": 2267,
    "name": "Mateus",
    "major": "Sociologia"
}, {
    "_id": 2453,
    "name": "Guilherme",
    "major": "Inglês"
}]
```

# Sistema de gerenciamento de banco de dados não relacionais(Em inglês: NRDBMS = Non-Relation Database Management Systems)

* Ajuda a usuários criar e manterem o seu banco de dados não relacional:
	* Exemplo: mongoDB, dynamoDB, firebase, etc.


* Especifico de implementação:
	* Não existe uma linguagem padrão para interagir com o sistema de gerenciamento de banco de dados não relacional.

	* A maioria dos NRDBMS irão implementar suas próprias linguagens para realizar operações CRUD.


# Consulta de banco de dados

* Queries(consultas) são requisições feitas para o sistema de banco de dados pedindo informações específicas.

* O google search é uma query.

# Tabelas e chaves(Tables and Keys)

![Tables_and_keys](/imagens/tables.PNG)

* Note que nessa tabela temos 3 colunas, sendo elas:
    * student_id, name e major.

	* Nessa tabela estamos armazenando 3 informações sobre cada aluno.

	* Cada coluna terá apenas um atributo.

	* As linhas representam uma entrada ou um aluno real.

Sempre que estamos criando uma tabela em um banco de dados relacional, queremos ter uma coluna especial que é chamada de chave primária, basicamente ela define exclusivamente a linha no banco de dados. No exemplo acima, student_id é a nossa chave primária. No exemplo acima, temos o nome Jack aparecendo duas vezes, note que são informações iguais, nesse caso a chave primária atua fazendo com que cada informação tenha o seu próprio identificador(nesse caso 2 e 4 são os id's).

## Outro exemplo

![Tables_and_keys2](/imagens/tables2.PNG)

Note que no exemplo acima a nossa chave primária está na coluna email, cada email é único e possui as suas devidas informações em cada linha.

## Outro exemplo

![Tables_and_keys3](/imagens/tables3.PNG)

No exemplo acima a nossa chave primária é emp_id.

# Chave estrangeira

Uma chave estrangeira basicamente armazena a chave primária de uma linha em outra tabela do banco de dados.

![Tables_and_keys4](/imagens/tables4.PNG)

## Exemplo detalhado

No exemplo abaixo Jan Levinson(emp_id = 100) possui uma branch_id como sendo 1, esse 1 é basicamente a chave primária da tabela branch_id(segunda imagem).

![Tables_and_keys5](/imagens/tables5.PNG)

![Tables_and_keys6](/imagens/tables6.PNG)

Em resumo, uma chave estrangeira nos permite definir relacionamentos entre as duas tabelas.

Podemos ter duas ou mais chaves primárias, que são chamadas de chaves compostas.

# Noções Básicas de SQL

## Structured Query Language(SQL):

* É uma linguagem híbrida, contendo 4 típos de linguagens em uma só:
	* Data Query Language(DQL):
		* É utilizado para fazer consultas no banco de dado para obter informações.	
		
		* Pega as informações que já estão armazenadas no banco de dados.

	* Data Definition Language(DDL):
		* É utilizado para definir esquemas.

	* Data Control Language(DCL):
		* É utilizado para controlar o acesso a dados no banco de dados.
		
		* Gerenciamento de usuários e permissões.

	* Data Manipulation Language(DML):
		* É utilizado para inserir, atualizar e deletar informações do banco de dados.


# Queries

* Uma query(consulta) é um conjunto de instruções dadas ao RDBMS(Relational Database Management System) que basicamente diz ao RBDMS qual informação nós queremos recuperar.

Exemplo de query

```sql
SELECT employee.name, employee.age
FROM employee
WHERE employee.salary > 30000;
```

Basicamente o que essa query faz é:
- Seleciona o nome e idade do empregado
- Utiliza o nome da tabela(employee) para fazer a consulta(query)
- Recebe apenas informações sobre salários acima de 30000.

# Criando um banco de dados

Para criar um banco de dados basta executar o seguinte comando:

```sql
CREATE DATABASE <nome_do_banco_de_dados>;
```

OBS: Toda declaração precisa de um ponto e vírgula no final.

# Alguns tipos de dados usados na linguagem SQL

* INT - Números inteiros

* DECIMAL(M, N) - Números decimais
	* M = Quantidade de números que queremos armazenar
	
	* N = Número de casas decimais que queremos ter

* VARCHAR(10) - String de texto
	* Armazena uma string de 10 caracteres

* BLOB - Conhecido como Binary Large Object, armazena binários

* DATE - Tipo data(YYYY-MM-DD)

* TIMESTAMP - Armazena data e hora(YYYY-MM-DD HH:MM:SS)
	* É utilizado para gravar a data e hora que algo aconteceu(Ex: Gravar a data/hora que um item foi inserido no banco de dados).

# Criando tabelas

Para criar tabelas em nosso banco de dados fazemos uso do comando:

```sql
CREATE TABLE <nome_da_tabela> ();
```

## Criando uma tabela onde armazena informações sobre estudantes

```sql
CREATE TABLE student (
	student_id INT PRIMARY KEY,
	name VARCHAR(20),
	major VARCHAR(20)
);
```

Note que no exemplo acima criamos uma tabela chamada student que possui 3 colunas(student_id, name e major) e seus respectivos atributos. A coluna student_id é a nossa primary key(chave primária). Separamos cada atributo utilizando vírgula.

Utilizando o comando:
```sql
DESCRIBE <nome_da_tabela>;
```

Irá exibir todas as informações sobre a quantidade de colunas/linhas e os atributos.


Utilizando o comando:
```sql
DROP TABLE <nome_da_tabela>;
```

O comando acima irá excluir a nossa tabela.

Usando o comando:
```sql
ALTER TABLE student ADD gpa DECIMAL(3, 2);
```

O comando acima adiciona uma nova coluna a nossa tabela student, essa coluna se chama gpa e tem o tipo DECIMAL contendo 3 números com duas casas decimais.

Usando o comando:
```sql
DESCRIBE student;
```

Teremos o seguinte resultado:

```
+------------+--------------+------+-----+---------+-------+
| Field      | Type         | Null | Key | Default | Extra |
+------------+--------------+------+-----+---------+-------+
| student_id | int          | NO   | PRI | NULL    |       |
| name       | varchar(20)  | YES  |     | NULL    |       |
| major      | varchar(20)  | YES  |     | NULL    |       |
| gpa        | decimal(3,2) | YES  |     | NULL    |       |
+------------+--------------+------+-----+---------+-------+
```

Podemos remover uma coluna da nossa tabela usando o comando:
```sql
ALTER TABLE student DROP COLUMN gpa;
```

O comando acima irá remover a coluna gpa da nossa tabela student.


## Usando o terminal para manipular o nosso banco de dados

Utilizando os comandos no terminal:

```sql
SHOW DATABASES;
```

O comando acima irá exibir todos os bancos de dados na nossa máquina.

```sql
USE <nome_do_banco_de_dados>;
```

O comando acima irá utilizar o banco de dados que queremos.

```sql
SHOW TABLES;
```

O comando acima irá exibir todas as tabelas do nosso banco de dados que selecionamos.

# Inserindo dados

Inserindo dados em nossa tabela student

Para inserir dados fazemos uso do comando:
```sql
INSERT INTO <nome_da_tabela> VALUES();
```

O comando acima basicamente irá inserir dados dentro da nossa tabela. Dentro dos parênteses em VALUES passamos os valores para cada coluna fazendo uso da ordem de cada coluna, nesse caso a primeira coluna é student_id, a segunda é name e a última é major, devemos seguir a ordem das colunas.

## Inserindo os dados na nossa tabela student
```sql
INSERT INTO student VALUES(1, 'Jack', 'Biology);
```

O comando acima irá inserir o student_id(1), o name('Jack') e o major('Biology') dentro da nossa tabela student.


## Verificando todos os dados da nossa tabela
Para acessar todas as informações da nossa tabela student fazemos uso do comando:
```sql
SELECT * FROM student;
```

O resultado seria:
```
+------------+------+---------+
| student_id | name | major   |
+------------+------+---------+
|          1 | Jack | Biology |
+------------+------+---------+
```

Inserindo mais dados na nossa tabela student:
```sql
INSERT INTO student VALUES(2, 'Kate', 'Sociology');
```

O resultado será:
```
+------------+------+-----------+
| student_id | name | major     |
+------------+------+-----------+
|          1 | Jack | Biology   |
|          2 | Kate | Sociology |
+------------+------+-----------+
```

## Inserindo valores de forma específica

Digamos que o nosso aluno não tenha um major, nesse caso podemos manipular a inserção de dados fazendo com que passemos apenas o seu student_id e o seu name para a tabela:
```sql
INSERT INTO student(setudent_id, name) VALUES(3, 'Claire');
```

Note que especificamos os dois atributos(student_id e name) no qual iremos adicionar.

O resultado será:
```
+------------+--------+-----------+
| student_id | name   | major     |
+------------+--------+-----------+
|          1 | Jack   | Biology   |
|          2 | Kate   | Sociology |
|          3 | Claire | NULL      |
+------------+--------+-----------+
```

Note que o major do student_id 3 é NULL, é NULL porque não passamos nenhuma informação para a coluna major.

NOTA: Não podemos inserir dados duplicados, a chave primária não permitiria dados duplicados.


# Constraints(Restrições)

Atributos especificos

* NOT NULL - Basicamente nos permite definir uma ou mais colunas da tabela que não podem ser NULL.

Por exemplo, utilizando a tabela student podemos utilizar o atributo NOT NULL na coluna name, ou seja, a coluna name não pode ter o valor NULL(Nenhum valor).

```sql
CREATE TABLE student(
	student_id INT PRIMARY KEY,
	name VARCHAR(20) NOT NULL,
	major VARCHAR(20)
);
```

Outro exemplo seria o atributo UNIQUE, vejamos:

```sql
CREATE TABLE student(
	student_id INT PRIMARY KEY,
	name VARCHAR(20) NOT NULL,
	major VARCHAR(20) UNIQUE
);
```

Note que utilizamos UNIQUE na coluna major, ou seja, caso tenhamos um valor na coluna major esse valor não pode ser repetido, ele será rejeitado.

## O exemplo seria:
```sql
+------------+-------------+------+-----+---------+-------+
| Field      | Type        | Null | Key | Default | Extra |
+------------+-------------+------+-----+---------+-------+
| student_id | int         | NO   | PRI | NULL    |       |
| name       | varchar(20) | NO   |     | NULL    |       |
| major      | varchar(20) | YES  | UNI | NULL    |       |
+------------+-------------+------+-----+---------+-------+
```

## Inserindo dados e testando a tabela student

```sql
INSERT INTO student VALUES(1, 'Jack', 'Biology');
INSERT INTO student VALUES(2, 'Kate', 'Sociology');
INSERT INTO student VALUES(3, NULL,'Chemistry');
INSERT INTO student VALUES(4, 'Jack', 'Biology');
INSERT INTO student VALUES(5, 'Mike', 'Computer Science');
```

Note que o student_id 3 daria problema na coluna name, pois definimos o atributo NOT NULL para a coluna name e estamos passando NULL como argumento, isso resulta no seguinte erro:
```
INSERT INTO student VALUES(3, NULL,'Chemistry');
ERROR 1048 (23000): Column 'name' cannot be null
```

Note que o student_id 4 da tabela major daria problema, pois Biology ja foi declarado no student_id 1. Isso resulta no seguinte erro:

```
INSERT INTO student VALUES(4, 'Jack', 'Biology');
ERROR 1062 (23000): Duplicate entry 'Biology' for key 'student.major'
```

## Primary Key

A primary-key(chave primária) ela possui tanto o atributo NOT NULL como o atributo UNIQUE. Ela não é vazia e é única.

Nesse caso NOT NULL e UNIQUE são Constraints(restrições).

# Usando o atributo DEFAULT

Digamos que uma pessoa não forneça o seu major, nesse caso podemos utilizar o atributo DEFAULT para atribuir um valor "padrão" caso o usuário não o forneça para a coluna.

```sql
CREATE TABLE student(
	student_id INT PRIMARY KEY,
	name VARCHAR(20),
	major VARCHAR(20) DEFAULT 'undecided'
);
```

Caso o usuário não passe nenhuma informação para a coluna major, o valor padrão(default) será undecided. Vejamos o resultado:

```sql
INSERT INTO student(student_id, name) VALUES(3, 'Douglas');
```

Como não inserimos o argumento para a coluna major, o resultado será undecided(padrão).

```sql
+------------+---------+-----------+
| student_id | name    | major     |
+------------+---------+-----------+
|          3 | Douglas | undecided |
+------------+---------+-----------+
```

# Utilizando o atributo AUTO_INCREMENT

O atributo AUTO_INCREMENT basicamente faz o incremento automático, podemos fazer isso na coluna student_id para incrementar automaticamente.

```sql
CREATE TABLE student(
	student_id INT PRIMARY KEY AUTO_INCREMENT,
	name VARCHAR(20),
	major VARCHAR(20)
);
```

## Inserindo dados

```sql
INSERT INTO student(name, major) VALUES('Jack', 'Biology');
INSERT INTO student(name, major) VALUES('Kate', 'Sociology');
INSERT INTO student(name, major) VALUES(NULL,'Chemistry');
INSERT INTO student(name, major) VALUES('Jack', 'Biology');
INSERT INTO student(name, major) VALUES('Mike', 'Computer Science');
```

Como o atributo AUTO_INCREMENT faz a incrementação automatica da coluna student_id, temos:

```sql
+------------+------+------------------+
| student_id | name | major            |
+------------+------+------------------+
|          1 | Jack | Biology          |
|          2 | Kate | Sociology        |
|          3 | NULL | Chemistry        |
|          4 | Jack | Biology          |
|          5 | Mike | Computer Science |
+------------+------+------------------+
```

## Atualizando(Update) valores dentro da nossa tabela

Digamos que queremos atualizar a coluna major da nossa tabela acima e modificar os valores Biology para Bio, fazemos isso utilizando o comando:

```sql
UPDATE student SET major = 'Bio' WHERE major = 'Biology';
```

O resultado será:

```sql
+------------+---------+-------------------+
| student_id | name    | major             |
+------------+---------+-------------------+
|          1 | Jack    | Bio               |
|          2 | Kate    | Sociology         |
|          3 | NULL    | Chemistry         |
|          4 | Jack    | Bio               |
|          5 | Mike    | Computer Science  |
|          6 | Douglas | Sistemas de Info. |
+------------+---------+-------------------+
```

Fazemos uso do atributo SET para definir qual coluna queremos alterar e em seguida passamos a informação nova para a coluna. No entanto é necessário especificar que queremos alterar apenas os valores que contem o major "Biology", para isso utilizamos do atributo WHERE que especifica o que queremos alterar na tabela, nesse caso queremos alterar apenas as colunas que possuem o valor "Biology".

NOTA: Podemos usar operadores como:

* Igual(=)

* Diferente(<>)

* Maior que(>)

* Menor que(<)

* Maior ou igual que(>=)

* Menor ou igual que(<=)

No exemplo acima, fizemos uso do operador de igualdade(=).

## Fazendo múltilas atualizações

Digamos que queremos alterar dois valores de uma tabela de vez, fazemos isso da seguinte forma:

```sql
UPDATE student SET major = 'Biochemistry' WHERE major = 'Bio' OR major = "Chemistry";
```

No exemplo acima estamos atualizando as colunas que possuem o major Bio e Chemistry para o novo major que é Biochemistry, nesse caso o operador lógico OR irá alterar ao menos uma coluna que possua Bio ou Chemistry como valor.

Antes de executar o código acima tinhamos a tabela como sendo:

```sql
+------------+---------+-------------------+
| student_id | name    | major             |
+------------+---------+-------------------+
|          1 | Jack    | Bio               |
|          2 | Kate    | Sociology         |
|          3 | NULL    | Chemistry         |
|          4 | Jack    | Bio               |
|          5 | Mike    | Computer Science  |
|          6 | Douglas | Sistemas de Info. |
+------------+---------+-------------------+
```

Após executar o comando temos o seguinte resultado:

```sql
+------------+---------+------------------+
| student_id | name    | major            |
+------------+---------+------------------+
|          1 | Jack    | Biochemistry     |
|          2 | Kate    | Sociology        |
|          3 | NULL    | Biochemistry     |
|          4 | Jack    | Biochemistry     |
|          5 | Mike    | Computer Science |
|          6 | Douglas | Sistemas de Info.|
+------------+---------+------------------+
```


Outro exemplo:

```sql
UPDATE student SET name = 'Guilherme', major = 'undecided' WHERE student_id = 2;
```

O exemplo acima irá alterar o nome e o major para Guilherme/undecided onde o student_id é 2, nesse caso o nosso student_id tem o nome "Kate" e o major "Sociology", esse valor será alterado.

```sql
+------------+-----------+------------------+
| student_id | name      | major            |
+------------+-----------+------------------+
|          1 | Jack      | Biochemistry     |
|          2 | Guilherme | undecided        |
|          3 | NULL      | Biochemistry     |
|          4 | Jack      | Biochemistry     |
|          5 | Mike      | Computer Science |
|          6 | Douglas   | S.I              |
+------------+-----------+------------------+
```

## Deletando dados de uma tabela

Para deletar dados de uma tabela fazemos uso do comando DELETE FROM <nome_da_tabela> e em seguidas passamosa tributos para especificar o que queremos deletar, caso contrário, iremos deletar todas as linhas da tabela. 

No exemplo abaixo iremos deletar todos os dados onde o student_id seja igual a 5, vejamos:

```sql
DELETE FROM student WHERE student_id = 5;
```

Toda a linha que contém o student_id = 5 será deletada.

```sql
+------------+-----------+--------------+
| student_id | name      | major        |
+------------+-----------+--------------+
|          1 | Jack      | Biochemistry |
|          2 | Guilherme | undecided    |
|          3 | NULL      | Biochemistry |
|          4 | Jack      | Biochemistry |
|          6 | Douglas   | S.I          |
+------------+-----------+--------------+
```

Note que não temos mais o student_id 5 e nenhuma informação na linha. Toda a linha é deletada.

Assim como nos exemplos em Update, podemos explicitar ainda mais, vejamos:

```sql
DELETE FROM student WHERE name = 'Guilherme' AND major = 'undecided';
```

O resultado:

```sql
+------------+---------+--------------+
| student_id | name    | major        |
+------------+---------+--------------+
|          1 | Jack    | Biochemistry |
|          3 | NULL    | Biochemistry |
|          4 | Jack    | Biochemistry |
|          6 | Douglas | S.I          |
+------------+---------+--------------+
```

Note que todas as informações da linha 2 foram excluidas. Isso acontece porque o operador lógico AND atua caso ambos os valores sejam verdadeiros(existam).


## Basic Queries(Consultas básicas)

Podemos especificar quais colunas queremos consultar, para isso utilizamos o nome da(s) coluna(s) no lugar de utilizar o símbilo *.

```sql
SELECT name FROM student;
```

O resultado:

```sql
+---------+
| name    |
+---------+
| Jack    |
| NULL    |
| Jack    |
| Douglas |
+---------+
```

Podemos também selecionar o name e o major:

```sql
SELECT name, major FROM student;
```

O resultado:

```sql
+---------+--------------+
| name    | major        |
+---------+--------------+
| Jack    | Biochemistry |
| NULL    | Biochemistry |
| Jack    | Biochemistry |
| Douglas | S.I          |
+---------+--------------+
```

Bem prático né?

## Ordenando nossa tabela

Podemos ordenar nossa tabela de forma númerica e/ou alfabética utilizando o atributo ORDER BY <nome_da_coluna>

```sql
SELECT name, major FROM student ORDER BY name;
```

O resultado:

```sql
+---------+--------------+
| name    | major        |
+---------+--------------+
| NULL    | Biochemistry |
| Douglas | S.I          |
| Jack    | Biochemistry |
| Jack    | Biochemistry |
+---------+--------------+
4 rows in set (0.00 sec)
```

O resultado será ordenado pela coluna name que foi a que passamos para o ORDER BY.

Caso queira ordenar de forma contrária(decrescente) basta adicionar um DESC após o name, ex:

```sql
SELECT name, major FROM student ORDER BY name DESC;
```

O resultado: 

```sql
+---------+--------------+
| name    | major        |
+---------+--------------+
| Jack    | Biochemistry |
| Jack    | Biochemistry |
| Douglas | S.I          |
| NULL    | Biochemistry |
+---------+--------------+
```

Note que invertamos a ordem da tabela name, está ao contrário(decrescente).

Por padrão a ordem é ASC(crescente), mas por algum acaso a tabela esteja decrescente basta adicionar um ASC após o name.

## Limitando a quantidade de dados na pesquisa

Digamos que você queira limitar a quantidade de resultados na sua consulta ao banco de dados, para isso fazemos uso do atributo LIMIT <quantidade_a_ser_mostrada>;

```sql
SELECT * FROM student LIMIT 2;
```

O comando acima irá exibir apenas duas linhas de dados.

Exemplo:

```sql
+------------+------+--------------+
| student_id | name | major        |
+------------+------+--------------+
|          1 | Jack | Biochemistry |
|          3 | NULL | Biochemistry |
+------------+------+--------------+
```

## Utilizando o atributo IN

Digamos que queremos especificar quais valores queremos consultar na nossa tabela, para isso fazemos uso do atributo IN, vejamos:

```sql
SELECT * FROM student WHERE name IN ('Douglas', 'Gabriela');
```

O código acima irá selecionar todos os valores Douglas e Gabriela que estão presentes na coluna name.

```sql
+------------+----------+-------+
| student_id | name     | major |
+------------+----------+-------+
|          6 | Douglas  | S.I   |
|          7 | Gabriela | C.C   |
+------------+----------+-------+
```


## Trabalhando com consulas mais complexas

Iremos trabalhar na modelagem de tabelas mais complexas, onde iremos realizar consultas complexas, vejamos o exemplo abaixo:

![Data-Base-Schema](imagens/company-database-1.png)

Temos Chaves primárias, chaves estrangeiras, temos várias tabelas, veremos mais como modelar tudo isso.

## Criando o banco de dados

Nesse exemplo iremos criar o banco de dados da nossa empresa

```sql
CREATE DATABASE company_database;
```

Confirmando que o banco de dados foi criado

```sql
SHOW DATABASES;
```

Acessando o banco de dados

```sql
USE company_database;
```

## Criando as tabela employee e as suas colunas

```sql
CREATE TABLE employee(
	emp_id INT PRIMARY KEY,
	first_name VARCHAR(40),
	last_name VARCHAR(40),
	birth_day DATE,
	sex VARCHAR(1),
	salary INT,
	super_id INT,
	branch_id INT
);
```

Note que nossa primary-key(chave primária) é a coluna emp_id. Lembrando que a coluna super_id e branch_id são foreign-keys(chaves estrangeiras), elas são tabelas que serão criadas daqui a pouco.

## Criando a tabela branch

```sql
CREATE TABLE branch(
	branch_id INT PRIMARI KEY,
	branch_name VARCHAR(40),
	mgr_id INT,
	mgr_start_date DATE,
	FOREIGN KEY(mgr_id) REFERENCES employee(emp_id) ON DELETE SET NULL
);
```

* Definimos uma FOREIGN KEY(Chave estrangeira) usando a palavra reservada: FOREIGN KEY(nome_da_coluna) REFERENCES nome_da_tabela(nome_da_coluna) ON DELETE SET NULL

Veremos mais sobre ON DELETE SET NULL mais para frente, mas o resultado seria:

Em resumo nossa chave estrangeira irá fazer uma referência a tabela employee ligada a coluna emp_id, o restante da declaração veremos mais para frente.

## Alterando as colunas branch_id e super_id da tabela employee para fazer a "ligação" com a chave estrangeira

```sql
ALTER TABLE employee ADD FOREIGN KEY(branch_id) REFERENCES branch(branch_id) ON DELETE SET NULL;
```

Basicamente o exemplo acima faz um alteração na tabela employee onde adicionamos a coluna branch_id como sendo uma foreign key(chave estrangeira) e em seguida fazemos referência a essa coluna utilizando a tabela branch com a coluna branch_id.

Em resumo: A coluna branch_id da tabela employee irá fazer referência a chave primaria da tabela branch que possui a coluna branch_id.

```sql
ALTER TABLE employee ADD FOREIGN KEY(super_id) REFERENCES employee(emp_id) ON DELETE SET NULL;
```

O exemplo acima é semelhante ao anterior, basicamente fazemos a alteração na tabela employee para adicionar uma chave estrangeira, nesse caso a coluna super_id e fazemos referência a coluna emp_id da mesma tabela(employee). 

Em resumo: A coluna super_id da tabela employee irá fazer referência a tabela employee(a sí mesma) só que com a chave primária emp_id.

## Criando a tabela client

```sql
CREATE TABLE client(
	client_id INT PRIMARY KEY,
	client_name VARCHAR(40),
	branch_id INT,
	FOREIGN KEY(branch_id) REFERENCES branch(branch_id) ON DELETE SET NULL
);
```

No exemplo acima criamos a tabela client e passamos a foreign key passando branch_id como argumento e fazendo referência a tabela branch que possui a chave primária branch_id.

## Criando a tabela works_with

```sql
CREATE TABLE works_with(
	emp_id INT,
	client_id INT,
	total_sales INT,
	PRIMARY KEY(emp_id, client_id),
	FOREIGN KEY(emp_id) REFERENCES employee(emp_id) ON DELETE CASCADE,
	FOREIGN KEY(client_id) REFERENCES client(client_id) ON DELETE CASCADE
);
```

Tanto a chave primária emp_id quanto a chave primária client_id são foreign keys(chaves estrangeiras), a tabela works_with é bem exclusiva e possui chaves compostas. Iremos falar sobre ON DELETE CASCADE E ON DELETE SET NULL futuramente.

## Criando a tabela branch_supplier

```sql
CREATE TABLE branch_supplier(
	branch_id INT,
	supplier_name VARCHAR(40),
	supply_type VARCHAR(40),
	PRIMARY KEY(branch_id, supplier_name),
	FOREIGN KEY(branch_id) REFERENCES branch(branch_id) ON DELETE CASCADE
);
```

A tabela branch_supplier é semelhante a tabela works_with, a diferença é que a tabela branch_supplier tem apenas uma chave primária que é estrangeira(branch_id), já supplier_name é única. Fazemos referência a tabela branch e pegamos a coluna branch_id.

## Criamos todas as nossas tabelas, agora iremos inserir dados nelas.

Para inserir dados nas tabelas é um pouco diferente, vejamos:

* Empresa Corporate.

```sql
INSERT INTO employee VALUES(100, 'David', 'Wallace', '1967-11-17', 'M', 250000, NULL, NULL);

INSERT INTO branch VALUES(1, 'Corporate', 100, '2006-02-09');

UPDATE employee SET branch_id = 1 WHERE emp_id = 100;

INSERT INTO employe VALUES(101, 'Jan', 'Levinson', '1961-05-11', 'F', 110000, 100, 1);
```

Na primeira declaração inserimos os valores, no entanto note que os dois ultimos são NULL, pois antes não passamos valores para a tabela branch. Logo em seguida, inseremos valores na tabela branch e fazemos a atualização da coluna branch_id da tabela employee, onde branch_id 1 bate com o emp_id 100. Por fim inseremos valores normalmente na tabela employee.


O resultado:

```sql
+--------+------------+-----------+------------+------+--------+----------+-----------+
| emp_id | first_name | last_name | birth_day  | sex  | salary | super_id | branch_id |
+--------+------------+-----------+------------+------+--------+----------+-----------+
|    100 | David      | Wallace   | 1967-11-17 | M    | 250000 |     NULL |         1 |
|    101 | Jan        | Levinson  | 1961-05-11 | F    | 110000 |      100 |         1 |
+--------+------------+-----------+------------+------+--------+----------+-----------+
```

* Inserindo dados para a empresa Scraton

```sql
INSERT INTO employee VALUES(102, 'Michael', 'Scott', '1964-03-15', 'M', 75000, 100, NULL);

INSERT INTO branch VALUES(2, 'Scranton', 102, '1992-04-06');

UPDATE employee
SET branch_id = 2
WHERE emp_id = 102;

INSERT INTO employee VALUES(103, 'Angela', 'Martin', '1971-06-25', 'F', 63000, 102, 2);
INSERT INTO employee VALUES(104, 'Kelly', 'Kapoor', '1980-02-05', 'F', 55000, 102, 2);
INSERT INTO employee VALUES(105, 'Stanley', 'Hudson', '1958-02-19', 'M', 69000, 102, 2);
```
* Inserindo dados para a empresa Stamford

```sql
INSERT INTO employee VALUES(106, 'Josh', 'Porter', '1969-09-05', 'M', 78000, 100, NULL);

INSERT INTO branch VALUES(3, 'Stamford', 106, '1998-02-13');

UPDATE employee
SET branch_id = 3
WHERE emp_id = 106;

INSERT INTO employee VALUES(107, 'Andy', 'Bernard', '1973-07-22', 'M', 65000, 106, 3);
INSERT INTO employee VALUES(108, 'Jim', 'Halpert', '1978-10-01', 'M', 71000, 106, 3);
```

## Após inserir esses dados, teremos:

```sql
+--------+------------+-----------+------------+------+--------+----------+-----------+
| emp_id | first_name | last_name | birth_day  | sex  | salary | super_id | branch_id |
+--------+------------+-----------+------------+------+--------+----------+-----------+
|    100 | David      | Wallace   | 1967-11-17 | M    | 250000 |     NULL |         1 |
|    101 | Jan        | Levinson  | 1961-05-11 | F    | 110000 |      100 |         1 |
|    102 | Michael    | Scott     | 1964-03-15 | M    |  75000 |      100 |         2 |
|    103 | Angela     | Martin    | 1971-06-25 | F    |  63000 |      102 |         2 |
|    104 | Kelly      | Kapoor    | 1980-02-05 | F    |  55000 |      102 |         2 |
|    105 | Stanley    | Hudson    | 1958-02-19 | M    |  69000 |      102 |         2 |
|    106 | Josh       | Porter    | 1969-09-05 | M    |  78000 |      100 |         3 |
|    107 | Andy       | Bernard   | 1973-07-22 | M    |  65000 |      106 |         3 |
|    108 | Jim        | Halpert   | 1978-10-01 | M    |  71000 |      106 |         3 |
+--------+------------+-----------+------------+------+--------+----------+-----------+
```

Até esse momento trabalhamos com as tabelas employee e branch, inseremos e atualizamos os dados.

* Inserindo dados na tabela BRANCH SUPPLIER

```sql
INSERT INTO branch_supplier VALUES(2, 'Hammer Mill', 'Paper');
INSERT INTO branch_supplier VALUES(2, 'Uni-ball', 'Writing Utensils');
INSERT INTO branch_supplier VALUES(3, 'Patriot Paper', 'Paper');
INSERT INTO branch_supplier VALUES(2, 'J.T. Forms & Labels', 'Custom Forms');
INSERT INTO branch_supplier VALUES(3, 'Uni-ball', 'Writing Utensils');
INSERT INTO branch_supplier VALUES(3, 'Hammer Mill', 'Paper');
INSERT INTO branch_supplier VALUES(3, 'Stamford Lables', 'Custom Forms');
```

* Inserindo dados na tabela CLIENT

```sql
INSERT INTO client VALUES(400, 'Dunmore Highschool', 2);
INSERT INTO client VALUES(401, 'Lackawana Country', 2);
INSERT INTO client VALUES(402, 'FedEx', 3);
INSERT INTO client VALUES(403, 'John Daly Law, LLC', 3);
INSERT INTO client VALUES(404, 'Scranton Whitepages', 2);
INSERT INTO client VALUES(405, 'Times Newspaper', 3);
INSERT INTO client VALUES(406, 'FedEx', 2);
```

* Inserindo dados na tabela WORKS_WITH

```sql
INSERT INTO works_with VALUES(105, 400, 55000);
INSERT INTO works_with VALUES(102, 401, 267000);
INSERT INTO works_with VALUES(108, 402, 22500);
INSERT INTO works_with VALUES(107, 403, 5000);
INSERT INTO works_with VALUES(108, 403, 12000);
INSERT INTO works_with VALUES(105, 404, 33000);
INSERT INTO works_with VALUES(107, 405, 26000);
INSERT INTO works_with VALUES(102, 406, 15000);
INSERT INTO works_with VALUES(105, 406, 130000);
```

## Mais alguns comandos básicos

Utilizando o atributo AS para mostrar a(s) saída(s) da(s) coluna(s) personalizada(s).

Ex: Digamos que queremos exibir o primeiro e último nome da pessoa, mas de forma com que as colunas fiquem personalizadas, para isso fazemos o seguinte:

```sql
SELECT first_name AS forename, last_name AS surname FROM employee;
```

O resultado:

```sql
+----------+----------+
| forename | surname  |
+----------+----------+
| David    | Wallace  |
| Jan      | Levinson |
| Michael  | Scott    |
| Angela   | Martin   |
| Kelly    | Kapoor   |
| Stanley  | Hudson   |
| Josh     | Porter   |
| Andy     | Bernard  |
| Jim      | Halpert  |
+----------+----------+
```

Dessa forma podemos exibir uma saída com as colunas "personalizadas".

* O comando DISTINCT retorna valores distintos(diferentes), nesse caso se utilizarmos na coluna sex irá retornar apenas M, F, vejamos:

```sql
SELECT DISTINCT sex FROM employee;
```

O resultado:

```sql
+------+
| sex  |
+------+
| M    |
| F    |
+------+
```


## SQL Functions(Funções)

Digamos que queremos contar quantos emp_id's há na nossa tabela employee, para isso fazemos uso da função COUNT(nome_da_coluna).

```sql
SELECT COUNT(emp_id) FROM emplyee;
```

O resultado:

```sql
+---------------+
| COUNT(emp_id) |
+---------------+
|             9 |
+---------------+
```

Basicamente retorna 9 id's da coluna emp_id

Outro exemplo, encontre o número de funcionárias nascidas depois do ano 1970

```sql
SELECT COUNT(emp_id) FROM employee WHERE sex = 'F' AND birth_date > '1970-01-01';
```

O resultado:

```sql
+---------------+
| COUNT(emp_id) |
+---------------+
|             2 |
+---------------+
```

Encontrando a média salarial de todos os funcionários da tabela employee

```sql
SELECT AVG(salary) FROM employee;
```

No exemplo acima fazemos uso da função AVG() que retorna a média de válores da tabela.

O resultado:

```sql
+-------------+
| AVG(salary) |
+-------------+
|  92888.8889 |
+-------------+
```

Encontrando a soma total de todos os salários dos funcionários da tabela employee

```sql
SELECT SUM(salary) FROM employee;
```

A função SUM() retorna a soma de todos os valores de uma coluna.

O resultado:

```sql
+-------------+
| SUM(salary) |
+-------------+
|      836000 |
+-------------+
```

## Usando a função COUNT() juntamente com o GROUP BY

Digamos que queremos ver o total de dados na tabela sex e também queremos agrupar o total separando M e F, vejamos:

```sql
SELECT COUNT(sex), sex FROM employee GROUP BY sex;
```

O exemplo acima irá contar o total de dados que há na tabela sex e em seguida irá exibir os valores(M e F) ordenados pelo seu sexo(Ex: 3 F e 6 M).

Vejamos o resultado:

```sql
+------------+------+
| COUNT(sex) | sex  |
+------------+------+
|          6 | M    |
|          3 | F    |
+------------+------+
```

Mas digamos que queremos saber o total que um funcionário vendeu(Nesse caso o da tabela works_with que possui as colunas emp_id, client_id e total_sales)

```sql
SELECT SUM(total_sales), emp_id FROM works_with GROUP BY emp_id;
```

O exemplo acima realiza a soma de todas as vendas de cada funcionário, para isso fazemos a soma utilizando a função SUM() que recebe como argumento a coluna total_sales da tabela works_with e em seguida passamos mais uma coluna que é a imp_id, após isso indicamos que estamos querendo acessar as informações da tabela works_with e utilizamos o atributo GROUP BY para ordenar a coluna emp_id. Dessa forma irá retornar o total de venda na primeira coluna e o emp_id de cada um. Vejamos:

```sql
+------------------+--------+
| SUM(total_sales) | emp_id |
+------------------+--------+
|           282000 |    102 |
|           218000 |    105 |
|            31000 |    107 |
|            34500 |    108 |
+------------------+--------+
```

## Wildcards(curingas)

