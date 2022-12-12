# challenge-elastic
Desafio Head Tech


**Missão 1: fazer a feature de geração de relatórios rodar lisa sem falhas.**

1. Identifique algumas falhas no código.
2. O que você observaria na revisão do código para encontrar mais informações para garantir a solução completa do problema?
3. Como você faria para resolver esse problema no curto, médio e longo prazo?

**Missão 2 : Escalar a solução a partir da capacidade do servidor  para suportar milhões de usuários simultaneamente.** 

Falhas por falta de capacidade do servidor: Tempo de requisição alto, falha nas requisições, demora na emissão de relatório e perda de informações. 

Contexto-Nosso servidor encontra-se em uma única instância e que já está no limite da capacidade. Acreditamos que deveria ainda suportar os acessos que temos.

1. O que ele faria pra diagnosticar e apresentar um relatório completo do que ser feito.
2. Descreva como faria uma estruturação de API/servidor para suportar 10 mil empresas e 1 milhão de pacientes. Quais soluções você buscaria para resolver esse problema? E como você acompanharia a resolução do problema e garantiria o resultado das soluções?
3. Qual indicador mostraria que teve sucesso na resolução desse problema?

> Considerar:
1. Cada empresa possui um acesso e os pacientes HOJE não acessam.
2. Cada ação no app representa 5 consultas.
3. O sistema de cache foi implantado no último mês para algumas partes do produto.
>

**Missão 3: Extrair insights por meio dos dados armazenados no nosso banco de dados**

**Contexto:** 

Temos os dados brutos estruturados no banco e não conseguimos extrair informações a partir dos dados.

Gostaríamos de mapear o comportamento do cliente, verificar correlações e tirar insights para os times de Produto e Sucesso do Cliente. 

1. O que você faria para que as áreas conseguissem tirar insights dentro do que a gente tem? 

**Missão 4: Desenvolvimento técnico dos liderados**

**Contexto:** 

O time não desenvolve testando- teste no desenvolvimento não é uma premissa

Falta zelo na escrita do código impactando a estrutura

Alguns componentes do código não se conversam

Acesso do front end a API não tratam muitos erros

Banco de dados local gera problemas de atualização de dados

Falta uma cultura de aprendizagem no time

1. Como você desenvolveria o time nesses aspectos?
