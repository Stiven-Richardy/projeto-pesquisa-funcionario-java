# 🏢 Projeto: Cadastro de Funcionários (Java GUI)

Este projeto acadêmico foi desenvolvido como parte da disciplina de **Linguagem de Programação II**, com o objetivo de integrar uma aplicação **Java** com um banco de dados **SQL Server** via **JDBC**, implementando funcionalidades de pesquisa e navegação de registros.

## 🎯 Objetivos

- **Interface Gráfica**: Desenvolver um formulário Java (Swing/AWT) contendo campos para pesquisa por nome e exibição detalhada dos dados do funcionário (Nome, Salário, Cargo) .
- **Modelagem de Dados**: Criar um banco de dados SQL Server chamado `aulajava` com tabelas relacionais de cargos e funcionários.
- **Conexão JDBC**: Estabelecer a comunicação entre a aplicação Java e o banco de dados SQL Server.
- **Pesquisa Dinâmica**: Implementar a busca de funcionários utilizando a cláusula SQL `LIKE` e `PreparedStatement` para preencher o `ResultSet`.
- **Navegação**: Implementar botões "Anterior" e "Próximo" para navegar entre os registros retornados pela consulta.

## 🛠️ Ferramentas Utilizadas

- Java
- VS Code
- Git e GitHub

## 🗄️ Estrutura do Banco de Dados

O projeto utiliza o banco de dados **SQL Server** chamado `aulajava` com as seguintes tabelas:

#### Tabela: `tbcargos`
| Column Name | Data Type | Length | Allow Nulls | Descrição |
| :--- | :--- | :--- | :--- | :--- |
| **cd_cargo** | `smallint` | 2 | Não | Chave Primária (PK) |
| **ds_cargo** | `char` | 20 | Sim | Descrição do cargo |

#### Tabela: `tbfuncs`
| Column Name | Data Type | Length | Allow Nulls | Descrição |
| :--- | :--- | :--- | :--- | :--- |
| **cod_func** | `decimal` | 9 | Não | Chave Primária (PK) |
| **nome_func** | `char` | 30 | Sim | Nome do funcionário |
| **sal_func** | `money` | 8 | Sim | Salário do funcionário |
| **cod_cargo** | `smallint` | 2 | Sim | Chave Estrangeira (FK) para `tbcargos` |

## 🗂️ Estrutura do Projeto

```
📁 projeto-calculadora-e-cadastra-pessoa-java/
├── 📁 lib/
│   └── 📄 mssql-jdbc-13.2.1.jre8.jar
├── 📄 Form.java
├── 📄 .gitignore
└── 📄 README.md
```

## 🚀 Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/Stiven-Richardy/projeto-pesquisa-funcionario-java
```

2. Acesse a pasta do projeto:
```bash
cd projeto-pesquisa-funcionario-java
```

3. Compile os arquivos:
```bash
javac -encoding UTF-8 -cp ".;lib/mssql-jdbc-13.2.1.jre8.jar" Form.java
```

4. Execute os programas (Um de cada vez):
```bash
java -cp ".;lib/mssql-jdbc-13.2.1.jre8.jar" Form
```

## 👨‍🏫 Autores

- **Stiven Richardy Silva Rodrigues**  
  Estudante de Análise e Desenvolvimento de Sistemas | IFSP — Campus Cubatão  
  [@Stiven-Richardy](https://github.com/Stiven-Richardy)

- **Guilherme Mendes de Sousa**  
  Estudante de Análise e Desenvolvimento de Sistemas | IFSP — Campus Cubatão  
  [@Guilh3rme-M3ndes](https://github.com/Guilh3rme-M3ndes)

## 📚 Referências

- Documentação oficial do Java: https://docs.oracle.com/en/java/
- Baixar o JDBC Driver para SQL Server: https://learn.microsoft.com/pt-br/sql/connect/jdbc/download-microsoft-jdbc-driver-for-sql-server?view=sql-server-ver17
