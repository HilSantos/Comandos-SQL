# Comandos de Banco de Dados
Criação de um Banco de Dados SQL.

CREATE DATABASE db_ti35_teste; -- Criar base de dados
-- Isto é um comentario
CREATE TABLE tb_alunos(
    id_aluno          INT PRIMARY KEY AUTO_INCREMENT,
    nome_aluno        VARCHAR(80),
    telefone_aluno    VARCHAR(14),
    email_aluno       VARCHAR(40),
    cpf_aluno         VARCHAR(11),
    endereco_aluno    VARCHAR(80),
    nascimento_aluno  DATE,
    mensalidade_aluno DECIMAL(7,2));

  -- Inserir dados na tabela
    INSERT INTO tb_alunos(nome_aluno, telefone_aluno, email_aluno, cpf_aluno, endereco_aluno, nascimento_aluno,
     mensalidade_aluno)
VALUES('Paulo Castro', '5516994037928', 'silvasantos1933@proton.me', '88534521099', 'Av. Washington Luis, 777',
       '1984-03-22', 160.00)
