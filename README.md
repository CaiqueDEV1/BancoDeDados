# BancoDeDados
Banco de Dados, Hospital.



<h1>1. Atividade para criar um diagrama para um Hospital.</h1>

O hospital necessita de um sistema para sua área clínica que ajude a controlar consultas realizadas. Os médicos podem ser generalistas, especialistas ou residentes e têm seus dados pessoais cadastrados em planilhas digitais. Cada médico pode ter uma ou mais especialidades, que podem ser pediatria, clínica geral, gastroenterologia e dermatologia. Alguns registros antigos ainda estão em formulário de papel, mas será necessário incluir esses dados no novo sistema.

Os pacientes também precisam de cadastro, contendo dados pessoais (nome, data de nascimento, endereço, telefone e e-mail), documentos (CPF e RG) e convênio. Para cada convênio, são registrados nome, CNPJ e tempo de carência.

As consultas também têm sido registradas em planilhas, com data e hora de realização, médico responsável, paciente, valor da consulta ou nome do convênio, com o número da carteira. Também é necessário indicar na consulta qual a especialidade buscada pelo paciente.

Deseja-se ainda informatizar a receita do médico, de maneira que, no encerramento da consulta, ele possa registrar os medicamentos receitados, a quantidade e as instruções de uso. A partir disso, espera-se que o sistema imprima um relatório da receita ao paciente ou permita sua visualização via internet.


<h3>O centro do diagrama é o Paciente. Para o Lado Direito, está o que acontece depois das consultas. Para o Lado Esquerdo está os médicos e os dados deles.</h3>


![diagramaHospital](https://github.com/CaiqueDEV1/BancoDeDados/assets/125465166/ba605327-ef9d-4ca8-8b83-d2f35a575a43)

<h1>3ª PARTE - O Prisioneiro dos Dados<h1>
<h2>Povoamento inicial do sistema<h2>
 Este repositório contém os scripts de povoamento das tabelas desenvolvidas na atividade anterior, conforme as regras estabelecidas.
 Para garantir o bom funcionamento do sistema, é essencial que as seguintes atividades sejam observadas durante o povoamento inicial:
  
  <p>Inclusão de pelo menos dez médicos de diferentes especialidades;<p>

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
