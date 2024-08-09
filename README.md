# Missão Prática | Nível 2 | Mundo 3

# Material de orientações para desenvolvimento da missão prática do 2º nível de conhecimento.

## RPG0015  - Vamos manter as informações!

### Modelagem e implementação de um banco de dados simples, utilizando como base o SQL Server.

# Objetivos da prática

* Identificar os requisitos de um sistema e transformá-los no modelo
adequado.
* Utilizar ferramentas de modelagem para bases de dados relacionais.
* Explorar a sintaxe SQL na criação das estruturas do banco (DDL).
* Explorar a sintaxe SQL na consulta e manipulação de dados (DML)
*No final do exercício, o aluno terá vivenciado a experiência de modelar a
base de dados para um sistema simples, além de implementá-la, através
da sintaxe SQL, na plataforma do SQL Server.

# Materiais necessários para a prática

* Ferramenta de modelagem DBDesigner, banco de dados SQL Server e
gerenciador SQL Server Management Studio.

### Equipamentos:
 
  1- Computador com acesso à Internet.

  2- Banco de dados SQL Server, com gerenciador SQL Server Management
  Studio.

  3- Ferramenta de modelagem DBDesigner.

# Desenvolvimento da prática

# 👉 1º Procedimento | Criando o Banco de Dados

### 1. Baixar e executar a ferramenta de modelagem:

a- Acessar o endereço https://sourceforge.net/projects/dbdesigner-fork/

b- Efetuar o download do DBDesigner Fork no formato Zip

c- Descompactar e executar o aplicativo, como apresentado a seguir :
<img width="553" alt="DB-MODEL-ESTOQUE" src="https://github.com/user-attachments/assets/55406034-b1aa-4007-a185-53175070f775">


### 2.   Definir o modelo de dados para um sistema com as características apresentadas nos tópicos seguintes:

a- Deve haver um cadastro de usuários para acesso ao sistema, os quais
irão atuar como operadores para a compra e venda de produtos.

b- Deve haver um cadastro de pessoas físicas e pessoas jurídicas, com
os dados básicos de identificação, localização e contato,
diferenciando-se apenas pelo uso de CPF ou CNPJ.

c- Deve haver um cadastro de produtos, contendo identificador, nome,
quantidade e preço de venda.

d- Os operadores (usuários) poderão efetuar movimentos de compra
para um determinado produto, sempre de uma pessoa jurídica,
indicando a quantidade de produtos e preço unitário.

e- Os operadores (usuários) poderão efetuar movimentos de venda para
um determinado produto, sempre para uma pessoa física, utilizando o
preço de venda atualmente na base.

# Observação! No futuro sistema, criado na plataforma Java, será utilizada a herança na definição de pessoas físicas e jurídicas.

## 3.   Utilizar o SQL Server Management Studio para criar a base de dados modelada no tópico anterior:

a- Logar como usuário sa (System Administrator) e adicionar o logon loja, com senha loja.

<img width="942" alt="criandologin" src="https://github.com/user-attachments/assets/c12583b2-889d-494f-bb00-c46122f7ec42">

  b- Logar novamente com o usuário loja, que deve ter permissão para
criação de tabelas e demais estruturas do banco de dados

 c- Utilizar o editor de SQL para criar as estruturas do modelo.

<img width="676" alt="fgrgrgre" src="https://github.com/user-attachments/assets/0eb4d2eb-92f6-4d58-95a9-780d4c568d5b">

d- Definir uma sequence para geração dos identificadores de pessoa,
dado o relacionamento 1x1 com pessoa física ou jurídica.

e- Salvar o script completo para criação do banco de dados em um
arquivo com extensão .sql


# 👉 2º Procedimento | Alimentando a Base

1- Utilizar o SQL Server Management Studio para alimentar as tabelas com dados básicos do sistema:

a- Logar como usuário loja, senha loja.

b- Utilizar o editor de SQL para incluir dados na tabela de usuários, de
forma a obter um conjunto como o apresentado a seguir:

![0000000](https://github.com/user-attachments/assets/59d728c2-c7d7-474b-9f87-8a6c3af599ce)

# Observação!
Usuário op1, com senha op1, e usuário op2, com senha op2,
sem criptografia. Para sistemas reais seria necessário armazenar o hash da
senha, codificado para Base64.

c- Inserir alguns produtos na base de dados, obtendo um conjunto como
o que é apresentado a seguir:

![11111111111](https://github.com/user-attachments/assets/3765c5f8-fa46-4931-91dc-9ce01917848a)

2- Criar pessoas físicas e jurídicas na base de dados:

a- Obter o próximo id de pessoa a partir da sequence

b- Incluir na tabela pessoa os dados comuns

c- Incluir em pessoa física o CPF, efetuando o relacionamento com pessoa.

![22222222222222](https://github.com/user-attachments/assets/d8eba9a8-9342-4a66-8d16-696aed42bb6c)

 d- Incluir em pessoa jurídica o CNPJ, relacionando com pessoa.

![33333333333333333333](https://github.com/user-attachments/assets/db80198c-684b-4b57-9b1e-f98d480acdb8)


3- Criar algumas movimentações na base de dados, obtendo um conjunto
como o que é apresentado a seguir, onde E representa Entrada e S
representa Saída.

![44444444444444444](https://github.com/user-attachments/assets/b18d3ae8-09bd-46de-be61-4f50cb8706e3)

 
<img width="612" alt="4545454" src="https://github.com/user-attachments/assets/97bd9f09-cbaa-478f-b87b-5fdd65809d13">

