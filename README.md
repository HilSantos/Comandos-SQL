# Comandos de Banco de Dados
Criação de um Banco de Dados SQL.

CREATE DATABASE db_ti35_teste; -- Criar base de dados
-- Isto é um comentario
CREATE TABLE tb_alunos(
    id_aluno          INT PRIMARY KEY AUTO_INCREMENT, -- No caso de haver mais do que uma Chave Primaria, digitar apenas PRIMARY KEY (incluir as duas linhas), lá no final --
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
INSERT INTO tb_alunos(nome_aluno,telefone_aluno,email_aluno,cpf_aluno,endereco_aluno,nascimento_aluno,mensalidade_aluno)
VALUES('Paulo Castro','5516995456787','paulommc@gmail.com','12345678978','Rua 13 de agosto, 1222','1995-02-25',150.55);

INSERT INTO tb_alunos(nome_aluno,telefone_aluno,email_aluno,cpf_aluno,endereco_aluno,nascimento_aluno,mensalidade_aluno)
VALUES('Maria Silva','5511987654321','maria.silva@gmail.com','98765432100','Avenida Paulista, 1000','1990-05-15',200.75);

INSERT INTO tb_alunos(nome_aluno,telefone_aluno,email_aluno,cpf_aluno,endereco_aluno,nascimento_aluno,mensalidade_aluno)
VALUES('João Souza','5511998765432','joao.souza@gmail.com','87654321099','Rua das Flores, 500','1988-11-30',180.00);

INSERT INTO tb_alunos(nome_aluno,telefone_aluno,email_aluno,cpf_aluno,endereco_aluno,nascimento_aluno,mensalidade_aluno)
VALUES('Ana Pereira','5511976543210','ana.pereira@gmail.com','76543210988','Rua dos Pinheiros, 300','1992-07-20',220.50);

INSERT INTO tb_alunos(nome_aluno,telefone_aluno,email_aluno,cpf_aluno,endereco_aluno,nascimento_aluno,mensalidade_aluno)
VALUES('Carlos Lima','5511965432109','carlos.lima@gmail.com','65432109877','Avenida Brasil, 1500','1985-03-10',250.00);

INSERT INTO tb_alunos(nome_aluno,telefone_aluno,email_aluno,cpf_aluno,endereco_aluno,nascimento_aluno,mensalidade_aluno)
VALUES('Fernanda Costa','5511954321098','fernanda.costa@gmail.com','54321098766','Rua da Liberdade, 800',
'1993-09-25',190.25);
INSERT INTO `tb_alunos` (`id_aluno`, `nome_aluno`, `telefone_aluno`, `email_aluno`,`cpf_aluno`,`endereco_aluno`,
 `nascimento_aluno`, `mensalidade_aluno`) 
VALUES (NULL, 'Paulo Castro', '5516994037928', 'silvasantos1933@proton.me', '88534521099','Av. Washington Luis, 777',
 '1984-03-22', '160.00'), (NULL, 'Louis Johanson', '5511994037928','usuario@admin.com.br', '02096618344',
  'R. Voluntarios da Patria, 113', '1978-12-04', '125.00'), 
(NULL, 'Mike Dismore', '5516988031205', 'dismorem@yahoo.com', '67720154032', 'Av. Profº Francisco Morato, 2237',
'1933-12-30', '210.00'), (NULL, 'Irene Cara', '5511997015643', 'carairene@outlook.com', '33179051288',
'R. Frei Durão, 76', '2001-06-01', '106.00'), (NULL, 'Maria de Lourdes Silva', '5511988471234',
'silvalouma@hotmail.com', '09125842100', 'Av. do Cursino, 61', '2013-09-17', '90.00');
-- Select são os dados da tabela
-- From vem da tabela
-- Where é a condição do aluno
-- Order by é a ordenação
========================================================================================================================
SELECT telefone_aluno, mensalidade_aluno, nome_aluno
FROM tb_alunos
WHERE nome_aluno LIKE '%M%'
--Depois clique em Executar

SELECT telefone_aluno, mensalidade_aluno, nome_aluno
FROM tb_alunos
WHERE id_aluno > 2 AND mensalidade_aluno < 200
--O mesmo que o anterior, mas com mais de uma condição

UPDATE tb_alunos
SET telefone_aluno = '5516994032879', mensalidade_aluno = 90.00
WHERE id_aluno = 1
--Atualiza o telefone do aluno com id 1

DELETE FROM tb_alunos
WHERE id_aluno = 2
--Deleta o aluno com id 2
