# Hospital_banco

algums comandos utilizados em um banco de dados :

use consultas;

-- Criação da tabela 'hospital'
CREATE TABLE hospital (
    id_paciente INT PRIMARY KEY,
    nome_paciente VARCHAR(100),
    idade_paciente INT,
    
    id_medico INT,
    nome_medico VARCHAR(100),
    especialidade_medico VARCHAR(50),
    crm_medico VARCHAR(20),
    
    id_quarto INT,
    tipo_quarto VARCHAR(50),
    valor_diaria_quarto DECIMAL(10, 2),
    
    id_consulta INT,
    data_consulta DATE,
    valor_consulta DECIMAL(10, 2),
    convenio_consulta VARCHAR(50),
    especialidade_consulta VARCHAR(50),
    
    id_internacao INT,
    data_entrada_internacao DATE,
    data_alta_internacao DATE,
    prevista_alta_internacao DATE,
    valor_diaria_quarto_internacao DECIMAL(10, 2),
    procedimento_internacao VARCHAR(100)
);


select * from hospital;

INSERT INTO hospital VALUES
(1, 'Fernando Amorim', 25, 1, 'Médico 1', 'Gastroenterologia', 'CRM123', 1, 'Enfermaria', 50.00, 1, '2020-01-15', 100.00, 'Sim', 'Gastroenterologia', 1, '2020-02-10', '2020-02-20', '2020-02-18', 50.00, 'Procedimento 1'),


(2, 'Natan de souza', 30, 2, 'Médico 2', 'Pediatria', 'CRM456', 2, 'Apartamento', 60.00, 2, '2021-05-20', 80.00, 'Não', 'Pediatria', 2, '2021-08-05', '2021-08-15', '2021-08-12', 60.00, 'Procedimento 2'),


(5, 'Eva', 33, 2, 'Dr. Wilson', 'Ginecologia', 'CRM111', 1, 'Enfermaria', 55.00, 3, '2022-03-15', 95.00, 'Sim', 'Ginecologia', 9, '2022-04-01', '2022-04-10', '2022-04-05', 55.00, 'Procedimento 7'),


(6, 'Frank', 28, 3, 'Dr. White', 'Oftalmologia', 'CRM222', 2, 'Apartamento', 80.00, 5, '2021-07-05', 100.00, 'Não', 'Oftalmologia', 10, '2021-07-20', '2021-08-05', '2021-08-01', 80.00, 'Procedimento 8'),


(7, 'Grace', 45, 1, 'Dr. Taylor', 'Pneumologia', 'CRM333', 4, 'Apartamento', 70.00, 4, '2020-08-10', 120.00, 'Sim', 'Pneumologia', 11, '2020-09-01', '2020-09-15', '2020-09-10', 70.00, 'Procedimento 9'),


(8, 'Harry', 38, 2, 'Dr. Harris', 'Ortopedia', 'CRM444', 3, 'Enfermaria', 50.00, 1, '2022-06-20', 90.00, 'Sim', 'Ortopedia', 12, '2022-07-05', '2022-07-15', '2022-07-10', 50.00, 'Procedimento 10'),


(9, 'Ivy', 31, 4, 'Dr. Irving', 'Cardiologia', 'CRM555', 1, 'Apartamento', 60.00, 3, '2021-01-12', 80.00, 'Não', 'Cardiologia', 13, '2021-02-01', '2021-02-10', '2021-02-05', 60.00, 'Procedimento 11'),


(10, 'Jack', 26, 3, 'Dr. Jones', 'Dermatologia', 'CRM666', 2, 'Enfermaria', 45.00, 5, '2020-12-01', 110.00, 'Sim', 'Dermatologia', 14, '2021-01-02', '2021-01-10', '2021-01-08', 45.00, 'Procedimento 12'),


(11, 'Karen', 39, 1, 'Dr. King', 'Neurologia', 'CRM777', 4, 'Apartamento', 65.00, 2, '2020-04-15', 95.00, 'Não', 'Neurologia', 15, '2020-05-01', '2020-05-10', '2020-05-05', 65.00, 'Procedimento 13'),


(12, 'Leo', 29, 2, 'Dr. Lewis', 'Gastroenterologia', 'CRM888', 1, 'Enfermaria', 55.00, 4, '2022-02-10', 100.00, 'Sim', 'Gastroenterologia', 16, '2022-03-01', '2022-03-10', '2022-03-05', 55.00, 'Procedimento 14'),


(13, 'Mia', 32, 3, 'Dr. Miller', 'Oftalmologia', 'CRM999', 3, 'Enfermaria', 60.00, 5, '2021-09-10', 85.00, 'Não', 'Oftalmologia', 17, '2021-09-25', '2021-10-05', '2021-10-01', 60.00, 'Procedimento 15'),


(14, 'Noah', 36, 1, 'Dr. Nelson', 'Pneumologia', 'CRM101', 2, 'Apartamento', 75.00, 1, '2021-04-05', 110.00, 'Sim', 'Pneumologia', 18, '2021-04-20', '2021-05-05', '2021-05-01', 75.00, 'Procedimento 16'),


(15, 'Alice', 28, 3, 'Dr. Smith', 'Cardiologia', 'CRM789', 4, 'Apartamento', 70.00, 5, '2022-01-10', 120.00, 'Não', 'Cardiologia', 7, '2022-02-15', '2022-03-01', '2022-02-25', 70.00, 'Procedimento 3'),


(16, 'Bob', 35, 1, 'Dr. Johnson', 'Ortopedia', 'CRM234', 2, 'Enfermaria', 50.00, 3, '2021-08-20', 90.00, 'Sim', 'Ortopedia', 6, '2021-09-01', '2021-09-10', '2021-09-05', 50.00, 'Procedimento 4'),


(17, 'Carol', 22, 2, 'Dr. Davis', 'Dermatologia', 'CRM567', 1, 'Apartamento', 60.00, 4, '2020-05-12', 80.00, 'Sim', 'Dermatologia', 5, '2020-06-01', '2020-06-15', '2020-06-10', 60.00, 'Procedimento 5'),


(18, 'David', 40, 4, 'Dr. Brown', 'Neurologia', 'CRM890', 3, 'Enfermaria', 45.00, 2, '2021-11-05', 110.00, 'Não', 'Neurologia', 8, '2022-01-02', '2022-01-10', '2022-01-08', 45.00, 'Procedimento 6');


SELECT AVG(valor_consulta) AS media_consultas FROM hospital WHERE YEAR(data_consulta) = 2020 OR convenio_consulta = 'Sim';


SELECT * FROM hospital WHERE data_alta_internacao < prevista_alta_internacao;


SELECT * FROM hospital WHERE id_consulta = (SELECT MIN(id_consulta) FROM hospital);


SELECT * FROM hospital WHERE convenio_consulta = 'Não' ORDER BY valor_consulta DESC LIMIT 1;


SELECT * FROM hospital WHERE convenio_consulta = 'Não' ORDER BY valor_consulta ASC LIMIT 1;


SELECT 
    data_entrada_internacao,
    procedimento_internacao,
    id_quarto
FROM hospital WHERE tipo_quarto = 'Apartamento';


SELECT 
    nome_paciente,
    nome_medico,
    data_entrada_internacao,
    procedimento_internacao
FROM hospital WHERE especialidade_medico = 'Gastroenterologia'

