# Plataforma EAD Ensino Técnico/Profissionalizante

## Sobre o Projeto
Repositório oficial do projeto de modelagem e implementação do banco de dados relacional para a plataforma de Educação a Distância (EAD) voltada ao Ensino Técnico e Profissionalizante.

## Estrutura de Arquivos SQL

Os scripts estao organizados na pasta database/ seguindo a ordem de dependencia relacional:

   ```bash
database/
│
├── 01_schema.sql         # Criação das 12 tabelas, chaves primárias e estrangeiras
├── 02_views.sql          # Visões analíticas (vw_boletim_aluno, vw_grade_docente_salas)
├── 03_procedures.sql     # Stored Procedures e Funções (sp_efetivar_matricula, fn_calcular_media_modulo, etc.)
└── 04_triggers.sql       # Triggers de segurança por perfil e validação de regras de negócio
 ```
## Como Executar
1. Certifique-se de utilizar um SGBD compatível com **PostgreSQL 15+**.
2. Crie uma base de dados vazia para o projeto.
3. Execute os scripts em ordem sequencial:
   
   ```bash
   psql -U seu_usuario -d sua_base -f database/01_schema.sql
   psql -U seu_usuario -d sua_base -f database/02_views.sql
   psql -U seu_usuario -d sua_base -f database/03_procedures.sql
   psql -U seu_usuario -d sua_base -f database/04_triggers.sql
