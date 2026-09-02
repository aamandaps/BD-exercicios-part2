# Exercícios Banco de Dados - Especialização, Generealização e Herança.

### Exercício 01

Num aeroclube, estão inscritos pilotos, instrutores e alunos de pilotagens. Todos inscritos
são sócios e são identificados por um número de matrícula. Além do número de matrícula
os sócios são caracterizados por nome, endereço (logradouro, número, complemento, cep
e cidade). Os pilotos possuem um número de brevê (único). Todos os instrutores são
pilotos com formação adicional de instrutor e, devem ser registrados, o nome do curso
realizado, a instituição onde a formação foi realizada, bem como a data da obtenção do
diploma.
Para os alunos de pilotagem, guarda-se o registro de todas as suas saídas para a
contabilização de horas, necessário para a obtenção do brevê. Para cada saída, que pode
ser feita com instrutores diferentes, registra-se a data, a hora de saída, de chegada, bem
como o instrutor que realizou a saída e seu parecer sobre o voo. A escola só ministra cursos
básicos, portanto, não existem casos de professores que também são alunos de cursos
avançados. Para a emissão do brevê é necessário a comprovação do número mínimo de
horas de voo, bem como a apresentação dos pareceres dos instrutores sobre as
habilidades desenvolvidas a cada aula prática.

---

### Exercício 02
Um atacadista vende produtos em grande quantidade para seus clientes. Os produtos
estão cadastrados no sistema pelo seu código de barras, seu nome, seu valor unitário e
pela unidade de medida em que é oferecido. Os clientes que compram produtos devem ser
cadastrados pelo seu nome, seus diversos telefones de contato, um ou vários e-mails de
contato, o limite de crédito e um endereço que deve conter o logradouro, o número de
porta, o bairro e a cidade. Como aos finais de semana, o atacadista vende também para
pessoas físicas, além das jurídicas, é importante saber:

*Das pessoas físicas: além dos dados de qualquer cliente, o CPF, o valor máximo para
compra com cartão de crédito, o valor máximo para compra com cartão de débito
(Compras a dinheiro não tem limite).
Das pessoas jurídicas: além dos dados de qualquer cliente, também é necessário
saber seu CNPJ.*

Um cliente pode comprar diversos produtos em ocasiões diferentes, bem como um
produto pode ser comprado por diversos clientes em ocasiões diferentes. Existem
produtos que não podem ser vendidos para pessoas físicas, tendo, portanto, armazenado
um código de venda para pessoa jurídica nesses produtos. Modelar conforme as
informações acima.

---

### Exercício 03
Uma imobiliária aluga imóveis para clientes. Para ser cliente da imobiliária, é necessário
cadastrar no sistema seu CPF único, seu nome, um e-mail e todos os telefones possíveis
para contato. Os clientes podem ser os proprietários dos imóveis e os locatários. Dos
proprietários, é necessário saber seu endereço para contato, composto por logradouro,
número, cidade e CEP, o código, o número da agência e o número da conta do banco que
recebe os aluguéis. Dos locatários, é necessário saber o número da apólice do seguro
fiança, a renda mensal, a data de ingresso no emprego atual (Mesmo que seja empresa
própria) e um telefone de contato próximo. Um proprietário pode ter diversos imóveis, mas
seu cadastro só ficará no sistema se houver, ao menos, um imóvel seu para locação. Um
locatário pode alugar mais de um imóvel, uma vez que pode alugar um ou mais imóveis
comerciais e imóvel residencial, no entanto, o registro do locatário só fica no sistema se
houver alguma locação sua em vigência. Todo imóvel tem um número identificador único
no sistema, um endereço, composto por logradouro, número, cidade e CEP, o tipo
(comercial ou residencial) e o valor base para locação. Toda locação tem uma data inicial,
um valor acordado entre proprietário e locatário e uma data para revisão do valor (O valor
da locação pode ser aumentado ou reduzido na data de revisão e essa data será estendida).

---

# Exercícios p/ casa

### Exercício 01 - Agência de Modelos

O sistema a ser modelado será utilizado pelo Sindicato das Agências de Moda e Desfile,
devendo guardar informações sobre as diversas Agências cadastradas no sindicato.

Uma Agência possui armazenado, em seu banco de dados, todos os dados sobre todas
as pessoas com quem tem relação. Entre as pessoas armazenadas estão os
modelos masculinos e femininos, os clientes (fabricantes de roupas, lojistas), e
outras pessoas que simplesmente gostam de moda (pessoas comuns). Sobre
modelos, ficam armazenados dados como nome completo, CPF, endereço, cor dos
olhos, cor da pele, tamanho (altura, coxas, cintura, busto), peso, sexo e RG. Sobre
os Clientes, ficam armazenados nome completo, RG, CPF, endereço, sexo,
informação dizendo se é proprietário de loja ou fábrica, e um código único para sua
identificação. Sobre outras pessoas, ficam guardados o CPF, o endereço, o nome
completo, e um atributo descritivo indicando qual é o seu interesse em desfiles. Os
modelos de uma determinada Agência pertencem a uma única Agência, não
podendo desfilar para outras Agências. Devem ser armazenados todos os Desfiles
organizados por uma determinada Agência, guardando dados, como Nome_Desfile,
a data, o Local, o Estilo_do_Desfile. Para cada Desfile, deseja-se saber quais foram
os modelos que desfilaram, quais foram os clientes que o frequentaram, e quais
pessoas comuns também estiveram presentes, ou seja, que assistiram ao desfile. É
interessante notar que os desfiles diyidem-se naturalmente entre Desfiles de Moda-
Verao e Desfiles de Moda-Inverno. E de interesse também guardar informações
sobre o número de pessoas que fequentou um determinado desfile, a duração em
minutos de um determinado desfile e quais foram os patrocinadores de um
determinado desfile.

---

### Exercício 02 - Seguradora de automóveis

Desenhe um diagrama E-R para uma seguradora de automoveis em que cada cliente possua
um ou mais carros. O cliente fica registrado no sistema pelo seu CNH, seu nome completo, a
categoria do seu CNH, seu endereço de contato (Apenas CEP e numero de Porta). Cada carro,
cadastrado no sistema pela sua placa, marca, modelo, cor e ano, tem associado a ele zero ou
mais acidentes registrados. A seguradora precisa saber se o carro e de passeio ou para uso
profissional. Para carros de uso profissional, e necessario saber o tipo de uso e a quantidade
de horas por dia do carro em trânsito. Os acidentes são definidos no sistema pelo seu tipo,
valor mínimo e valor máximo de cobertura. Cada apólice de seguro, que é definida por um
código, cobre um ou mais carros e tem um ou varios planos de pagamentos de premios
associadas a ela. Os planos de pagamento sao caracterizados por um codigo e um
valor. Cada pagamento de apólice tem uma data de vencimento associada, além da data
em que o pagamento foi recebido. Diversas apólices podem estar registradas com o
mesmo plano de pagamento ou outro plano.
