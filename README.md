# Sistema de Gerenciamento de Usuários

## Descrição

Este é um sistema de gerenciamento de usuários simples desenvolvido em **PHP** e utilizando o banco de dados **MySQL**. Ele permite cadastrar, listar, editar e excluir usuários, armazenando informações como nome, e-mail, senha (criptografada) e data de nascimento. A interface utiliza o **Bootstrap** para estilização e responsividade.

## Funcionalidades

- **Cadastrar Usuários**: Insere os dados de novos usuários no banco de dados.
- **Editar Usuários**: Permite modificar os dados de um usuário existente.
- **Excluir Usuários**: Remove um usuário do banco de dados.
- **Listar Usuários**: Exibe todos os usuários cadastrados em uma tabela.

## Tecnologias Utilizadas

### 1. PHP
O sistema é desenvolvido em **PHP**, uma linguagem de programação para o desenvolvimento de aplicações web. Os principais componentes PHP incluem:

- **Operações CRUD**: Implementadas com as funcionalidades de `switch` para realizar diferentes operações (Cadastrar, Editar, Excluir).
- **Formulários HTML**: Envio de dados dos usuários para o servidor via método POST.
- **Interação com Banco de Dados**: Utiliza a extensão `MySQLi` para conexão e execução de queries no banco de dados.

### 2. MySQL
O banco de dados utilizado é o **MySQL**. Ele armazena informações sobre os usuários, incluindo nome, e-mail, senha (criptografada com **MD5**) e data de nascimento. As principais operações incluem:

- **INSERT**: Para cadastrar novos usuários.
- **UPDATE**: Para editar informações de usuários existentes.
- **DELETE**: Para excluir registros de usuários.
- **SELECT**: Para listar todos os usuários.

### 3. Bootstrap 4
A interface do sistema utiliza o **Bootstrap 4** para fornecer uma estrutura responsiva e visualmente agradável. Isso inclui:

- **Formulários estilizados** para inserção de dados.
- **Tabelas** para exibir os usuários cadastrados.
- **Botões** para ações como editar e excluir.

### 4. HTML & JavaScript
O sistema utiliza **HTML** para a estruturação da interface e **JavaScript** para validação e interações dinâmicas, como os alertas e confirmações de exclusão.

## Estrutura do Projeto

- **index.php**: Página principal que gerencia a navegação e inclui os componentes de acordo com as ações do usuário.
- **config.php**: Arquivo de configuração que contém as credenciais de conexão com o banco de dados.
- **novousuario.php**: Formulário para cadastrar novos usuários.
- **listarusuario.php**: Página que exibe todos os usuários cadastrados.
- **salvarusuario.php**: Lida com as ações de salvar, editar e excluir usuários.
- **editarusuario.php**: Formulário para editar um usuário existente.

## Instalação

1. Clone este repositório no seu servidor web.
2. Crie um banco de dados no MySQL e importe o seguinte script SQL para criar a tabela de usuários:

    ```sql
    CREATE TABLE usuarios (
        id INT AUTO_INCREMENT PRIMARY KEY,
        nome VARCHAR(100),
        email VARCHAR(100),
        senha VARCHAR(100),
        data_nasc DATE
    );
    ```

3. Atualize as credenciais de conexão no arquivo `config.php` conforme necessário:

    ```php
    define('HOST', 'localhost');
    define('USER', 'root');
    define('PASS', '');
    define('BASE', 'cadastro');
    ```

4. Abra o navegador e navegue até o caminho do projeto no servidor.

## Como Usar

1. **Cadastro de Usuário**:
   - Navegue até "Novo Usuário" no menu de navegação.
   - Preencha o formulário com as informações do usuário.
   - Clique em "Enviar".

2. **Listar Usuários**:
   - Navegue até "Listar Usuários" no menu de navegação.
   - Uma tabela será exibida com os dados dos usuários cadastrados.

3. **Editar Usuário**:
   - Na tabela de listagem de usuários, clique no botão "Editar" ao lado do usuário que deseja modificar.
   - Altere os dados e clique em "Enviar".

4. **Excluir Usuário**:
   - Na tabela de listagem de usuários, clique no botão "Excluir" ao lado do usuário que deseja remover.
   - Confirme a exclusão na janela de diálogo.

## Requisitos

- Servidor com suporte a **PHP 7+**.
- Banco de dados **MySQL**.
- Conexão com a internet para carregar os recursos do **Bootstrap** e **jQuery**.



