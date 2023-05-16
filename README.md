# BancoDeDados
Banco de Dados, Hospital.



<h1>1. Atividade para criar um diagrama para um Hospital.</h1>

O hospital necessita de um sistema para sua área clínica que ajude a controlar consultas realizadas. Os médicos podem ser generalistas, especialistas ou residentes e têm seus dados pessoais cadastrados em planilhas digitais. Cada médico pode ter uma ou mais especialidades, que podem ser pediatria, clínica geral, gastroenterologia e dermatologia. Alguns registros antigos ainda estão em formulário de papel, mas será necessário incluir esses dados no novo sistema.

Os pacientes também precisam de cadastro, contendo dados pessoais (nome, data de nascimento, endereço, telefone e e-mail), documentos (CPF e RG) e convênio. Para cada convênio, são registrados nome, CNPJ e tempo de carência.

As consultas também têm sido registradas em planilhas, com data e hora de realização, médico responsável, paciente, valor da consulta ou nome do convênio, com o número da carteira. Também é necessário indicar na consulta qual a especialidade buscada pelo paciente.

Deseja-se ainda informatizar a receita do médico, de maneira que, no encerramento da consulta, ele possa registrar os medicamentos receitados, a quantidade e as instruções de uso. A partir disso, espera-se que o sistema imprima um relatório da receita ao paciente ou permita sua visualização via internet.


<h3>O centro do diagrama é o Paciente. Para o Lado Direito, está o que acontece depois das consultas. Para o Lado Esquerdo está os médicos e os dados deles.</h3>


![diagramaHospital](https://github.com/CaiqueDEV1/BancoDeDados/assets/125465166/ba605327-ef9d-4ca8-8b83-d2f35a575a43)

<h1>3ª PARTE - O Prisioneiro dos Dados</h1>
<h2>Povoamento inicial do sistema</h2>
 Este repositório contém os scripts de povoamento das tabelas desenvolvidas na atividade anterior, conforme as regras estabelecidas.
 Para garantir o bom funcionamento do sistema, é essencial que as seguintes atividades sejam observadas durante o povoamento inicial:
 
  Inclusão de pelo menos dez médicos de diferentes especialidades;

  Inclusão de pelo menos sete especialidades (considerando a afirmação de que “entre as especialidades há pediatria, clínica geral, gastrenterologia e dermatologia”);

  Inclusão de pelo menos 15 pacientes;

  Registro de 20 consultas de diferentes pacientes e médicos, com datas entre 01/01/2015 e 01/01/2022. Pelo menos dez consultas devem ter receituário com dois ou mais 
  medicamentos;

  Inclusão de pelo menos quatro convênios médicos, com associação a pelo menos cinco pacientes e cinco consultas;

  Criação de entidade de relacionamento entre médico e especialidade;

  Criação de entidade de relacionamento entre internação e enfermeiro;

  Correção da chave estrangeira no relacionamento entre convênio e médico;

  Criação de entidade entre internação e enfermeiro;

  Inclusão de chaves estrangeiras dentro da tabela de internação (chaves de Médico e Paciente);

  Registro de pelo menos sete internações, com datas entre 01/01/2015 e 01/01/2022. Pelo menos dois pacientes devem ter se internado mais de uma vez. Pelo menos três 
  quartos devem ser cadastrados;

  Inclusão dos dados de pelo menos três tipos de quarto (apartamento, quarto duplo e enfermaria), com valores diferentes;

  Inclusão dos dados de dez profissionais de enfermagem, com associação de cada internação a pelo menos dois enfermeiros. Por fim, é importante destacar que os dados de 
  tipo de quarto, convênio e especialidade são essenciais para a operação do sistema e, portanto, devem ser povoados assim que o sistema for instalado. Assim, garantimos 
  que o sistema esteja completo e funcional desde o seu primeiro uso.
  
  <h3>Utilizando os seguintes códigos, inserindo as informações</h3>
  
  INSERT INTO medico (nome) VALUES
  ('Luiz'),
  ('Livia'),
  ('Gabriel'),
  ('Guylherme'),
  ('Dudu'),
  ('Grazieli'),
  ('Lucas'),
  ('Iago'),
  ('Thaina'),
  ('Julia');


INSERT INTO especialidade (nome) VALUES
('Ortopedia'),
('Cardiologia'),
('Gastrenterologia'),
('Dermatologia'),
('Pediatria'),
('Neurologia'),
('Clinica geral');

INSERT INTO paciente (nome, data_nascimento, telefone, endereco) VALUES
('Anderson', '2000-01-01', '11 1111-1111', 'Rua A, 123'),
('Sidoka', '1995-05-20', '11 2222-2222', 'Rua B, 456'),
('Kayque', '1980-12-31', '11 3333-3333', 'Rua C, 789'),
('Daniel', '1999-02-15', '11 4444-4444', 'Rua D, 1011'),
('Elisa', '1992-10-10', '11 5555-5555', 'Rua E, 1213'),
('Fernando', '1985-07-07', '11 6666-6666', 'Rua F, 1415'),
('Giovanna', '2005-11-30', '11 7777-7777', 'Rua G, 1617'),
('Hugo', '1998-04-25', '11 8888-8888', 'Rua H, 1819'),
('Isabela', '1990-09-09', '11 9999-9999', 'Rua I, 2021'),
('Joana', '2002-03-18', '11 1010-1010', 'Rua J, 2223'),
('Kerline', '1996-08-12', '11 1212-1212', 'Rua K, 2425'),
('Lucas', '1997-06-23', '11 1313-1313', 'Rua L, 2627'),
('Kathelyn', '1987-03-04', '11 1414-1414', 'Rua M, 2829'),
('Nathalia', '1994-12-15', '11 1515-1515', 'Rua N, 3031'),
('Olavo', '1983-09-26', '11 1616-1616', 'Rua O, 3233'),
('Paulo', '2000-11-20', '11 1717-1717', 'Rua P, 3435');


INSERT INTO convenio (nome, cnpj) VALUES
('SulAmérica', '123456789'),
('Amil', '123456789'),
('Unimed', '123456789'),
('Bradesco Saúde', '123456789');

INSERT INTO consulta (data_consulta, hora_consulta, id_paciente, id_medico) VALUES
 ('2016-02-15', '09:30', 1, 1),
 ('2017-05-22', '15:45', 2, 2),
 ('2018-01-10', '11:15', 3, 3),
 ('2019-03-03', '14:30', 4, 4),
 ('2016-07-12', '10:00', 5, 5),
 ('2017-08-21', '11:45', 6, 6),
 ('2018-06-09', '16:15', 7, 7),
 ('2019-10-30', '08:30', 8, 8),
 ('2020-02-18', '09:30', 9, 9),
 ('2016-05-05', '11:00', 10, 1),
 ('2017-04-18', '12:30', 11, 2),
 ('2018-07-07', '15:00', 12, 3),
 ('2019-11-02', '09:00', 13, 4),
 ('2020-12-10', '14:30', 14, 5),
 ('2016-09-25', '08:15', 15, 6),
 ('2017-07-11', '10:45', 16, 7);
 
  INSERT INTO `tipo_quarto` (`descricao`, `valor_diaria`) VALUES
  ('Apartamento', 500.00),
  ('Quarto Duplo', 300.00),
  ('Enfermaria', 200.00);
  
 INSERT INTO `quarto` (`numero`, `id_tipoquarto`) VALUES
  (101, 1),
  (102, 1),
  (201, 2),
  (202, 2),
  (301, 3),
  (302, 3);
 
  INSERT INTO `enfermeiro` (`nome`, `CPF`, `CRE`) VALUES
  ('Enf. Ana', 123456789, 12345),
  ('Enf. Bruna', 234567890, 23456),
  ('Enf. Carlos', 345678901, 34567),
  ('Enf. Daniel', 456789012, 45678),
  ('Enf. Elisa', 567890123, 56789),
  ('Enf. Fernando', 678901234, 67890),
  ('Enf. Giovanne', 789012345, 78901),
  ('Enf. Hugo', 890123456, 89012),
  ('Enf. Isabelly', 901234567, 90123),
  ('Enf. João', 123456780, 12340);
 
 INSERT INTO internacao (data_entrada, data_prev_alta, data_alta, procedimento, enfermeiro_id) VALUES
('2022-01-01 10:00:00', '2022-01-03 10:00:00', NULL, 'Cirurgia de apendicite', 1),
('2022-01-02 10:00:00', '2022-01-06 10:00:00', NULL, 'Cirurgia de vesícula', 2),
('2022-01-03 10:00:00', '2022-01-07 10:00:00', NULL, 'Cirurgia de hérnia', 3),
('2022-01-04 10:00:00', '2022-01-09 10:00:00', NULL, 'Cirurgia de tireoide', 4),
('2022-01-05 10:00:00', '2022-01-08 10:00:00', NULL, 'Cirurgia de próstata', 5),
('2022-01-06 10:00:00', '2022-01-10 10:00:00', NULL, 'Cirurgia de joelho', 6),
('2022-01-07 10:00:00', '2022-01-11 10:00:00', NULL, 'Cirurgia de coluna', 7),
('2022-01-08 10:00:00', '2022-01-12 10:00:00', NULL, 'Cirurgia de coração', 8),
('2022-01-09 10:00:00', '2022-01-13 10:00:00', NULL, 'Cirurgia de pulmão', 9),
('2022-01-10 10:00:00', '2022-01-14 10:00:00', NULL, 'Cirurgia de rim', 10);
