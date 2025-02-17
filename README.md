# Feedbacks - Banco de Dados

Este projeto visa criar um sistema simples e eficiente para armazenar feedbacks de usuários. Ele foi desenvolvido para registrar e organizar informações relacionadas a feedbacks, como o nome, e-mail, data e o conteúdo fornecido pelos usuários, permitindo uma gestão eficiente desses dados.

![Imagem ilustrativa](./docs/img/print_front.png)


---

## Tecnologias Utilizadas

*Frontend:*
- *HTML*: Utilizado para estruturar as páginas do sistema, criando a base do conteúdo que será apresentado ao usuário.
- *CSS*: Responsável pela estilização e pelo layout das páginas, garantindo que a interface do sistema seja visualmente agradável e fácil de navegar.
- *JavaScript*: Usado para implementar funcionalidades interativas e adicionar lógica ao comportamento das páginas, tornando a experiência do usuário mais dinâmica.

*Backend:*
- *Node.js*: Ambiente de execução JavaScript no servidor, permitindo que o código JavaScript seja executado fora do navegador e interaja diretamente com o servidor.
- *Express*: Framework minimalista para Node.js, utilizado para criar o servidor web, configurar as rotas e gerenciar requisições HTTP de forma simples e eficiente.

*Banco de Dados:*
- *MySQL*: Sistema de gerenciamento de banco de dados relacional (RDBMS) utilizado para armazenar e organizar os feedbacks. O MySQL facilita consultas rápidas e a integridade dos dados.

*Ferramentas:*
- *Git*: Ferramenta de controle de versão que permite gerenciar o histórico do código e colaborar com outras pessoas no desenvolvimento. 
- *VSCode*: Editor de código-fonte altamente recomendado para o desenvolvimento de aplicações, especialmente com suporte para Node.js e integração com Git, o que facilita o trabalho com o código-fonte e a colaboração.

---

## Estrutura do Banco de Dados

O banco de dados *feedbacks* contém uma tabela chamada *feedbacks*, que organiza os dados dos feedbacks recebidos. A estrutura da tabela é a seguinte:

| Nome da Coluna | Tipo de Dado   | Descrição                                                  |
|----------------|----------------|------------------------------------------------------------|
| feedback_id  | INTEGER        | Identificador único para cada feedback, gerado automaticamente pelo sistema (auto incremento). |
| data         | DATE           | A data em que o feedback foi enviado pelo usuário.         |
| nome         | VARCHAR(100)    | Nome do usuário que forneceu o feedback.                   |
| email        | VARCHAR(100)    | E-mail do usuário que forneceu o feedback.                 |
| feedback     | VARCHAR(255)    | O conteúdo do feedback dado pelo usuário.                  |

Esses campos permitem registrar as informações essenciais sobre o feedback e garantir que cada registro seja único e facilmente acessado.

---

## Requisitos

Antes de começar a configurar o projeto, é necessário garantir que algumas ferramentas estejam instaladas em seu ambiente de desenvolvimento. Elas são essenciais para o funcionamento correto do sistema:

- *Git*: Sistema de controle de versão, permitindo o gerenciamento do código-fonte e a colaboração entre desenvolvedores. [Baixe o Git aqui.](https://git-scm.com/)
- *Node.js*: Ambiente de execução JavaScript no lado do servidor, que permite rodar o código fora do navegador. [Baixe a versão mais recente do Node.js aqui.](https://nodejs.org/)
- *MySQL*: Sistema de gerenciamento de banco de dados, utilizado para armazenar os dados dos feedbacks. [Baixe o MySQL aqui.](https://dev.mysql.com/downloads/)
- *VSCode*: Editor de código-fonte leve e poderoso, altamente recomendado para desenvolvimento com Node.js. [Baixe o VSCode aqui.](https://code.visualstudio.com/)

---

## Como Testar o Banco de Dados

Siga os passos abaixo para configurar e testar o banco de dados do projeto na sua máquina local:

### 1. Clone o Repositório

Para começar, você precisa clonar o repositório do projeto para o seu computador. No terminal, execute:

```bash
git clone https://github.com/GabrielaHelena/feedbacks.git
cd feedbacks

### 2. Instale as Dependências
Depois de clonar o repositório, você precisa instalar as dependências do projeto. No diretório do projeto, execute o seguinte comando para instalar todos os pacotes necessários:

bash
Copiar
npm install
Este comando vai buscar e instalar todas as dependências listadas no arquivo package.json, como o Express, para configurar o servidor, e outras bibliotecas necessárias.

3. Crie o Banco de Dados
Agora, é hora de criar o banco de dados MySQL. Abra o terminal do MySQL e execute os seguintes comandos para configurar o banco de dados e a tabela de feedbacks:

sql
Copiar
CREATE DATABASE feedbacks;
USE feedbacks;

CREATE TABLE feedbacks(
    feedback_id INTEGER PRIMARY KEY AUTO_INCREMENT,
    data DATE NOT NULL,
    nome VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL,
    feedback VARCHAR(255) NOT NULL
);
Isso criará o banco de dados feedbacks e a tabela feedbacks com a estrutura mencionada anteriormente.

4. Execute o Backend
Para iniciar o servidor e fazer o backend rodar localmente, use o comando:

bash
Copiar
npm start
O servidor agora estará rodando localmente, geralmente acessível em http://localhost:4000. Com isso, você pode começar a interagir com a aplicação, enviando e recebendo feedbacks.
