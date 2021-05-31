# SIMPLE FORM
PHP, MySQL e React - REST API

Para este projeto iremos utilizar PHP juntamente com React para criar uma aplicação REST simples com operações de um CRUD. No back-end usaremos PHP com o banco MySQL.

No front-end criaremos formulários em React e enviaremos dados de formulário com Axios.

Serviremos o React a partir do PHP, uma vez que o back-end e o front-end serão servidos no mesmo domínio, não precisaremos habilitar o CORS (Cross-Origin Resource Sharing), que é um mecanismo que permite que recursos restritos em uma página da web sejam recuperados por outro domínio fora do domínio ao qual pertence o recurso que será recuperado.

### **Pré-requisitos**:

inicialmente, deveremos ter os seguintes pré-requisitos para construir este projeto confortavelmente: 
- **PHP 7.4 e MySql**: Para Configurarmos o ambiente básico, utilizaremos o [XAMPP 7.4.19 / PHP 7.4.19](https://windows.php.net/download#php-7.4).

> O XAMPP é um pacote com os principais servidores de código aberto do mercado, incluindo FTP, banco de dados MySQL e Apache com suporte as linguagens PHP e Perl.

- **Ao final iremos configurar nosso projeto em uma docker.**


## **Criação do banco de dados MySQL**:
- Criando banco:
    ```SQL
        create database reactdb;
    ```
    
A seguir, vamos adicionar uma tabela SQL em nosso banco de dados. Basta executar as seguintes instruções SQL

- Criando tabela:
    ```SQL
    use reactdb; -- Para entrar no banco via terminal

    CREATE TABLE `contacts` (
    `id` int(11) NOT NULL PRIMARY KEY AUTO_INCREMENT,
    `name` varchar(100) NOT NULL,
    `email` varchar(100) NOT NULL,
    `city` varchar(100),
    `country` varchar(100),
    `job` varchar(100)
    );
    ```

Primeiro, executamos a instrução SQL de uso para selecionar o banco de dados reactdb como nosso banco de dados de trabalho atual. A seguir, invocamos a instrução `CREATE TABLE ${nome_da_tabela}` para criar uma tabela SQL que possui as seguintes colunas:

- **id**: um identificador único para a pessoa;
- **name**: o nome da pessoa;
- **email**: o email da pessoa;
- **city**: a cidade da pessoa;
- **country**: o país da pessoa;
- **job**: o trabalho ocupado pela pessoa

Basicamente, este é um banco de dados simples para gerenciar os dados de nossos contatos.
