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

Uma possível abordargem seria compreender quais são os fatores que possa desencadear estes pontos. Para idenificar, seguem algumas sugestões de dinâmicas e acompanhamentos

 ### Health Check do time
 
 - Dinâmica de curto prazo 
 
 - Dinâmica para compreender, considerando grandes eixos, como por exemplo:
  - sentimento de colaborativismo
  - orgulho da qualidade de entrega
  - capacidade de aprendizagem (tanto para aprender quanto para ensinar)
  - propósito e engajamento
  - visão estratégica
  - ambiente e bem estar

- Output: identificar potenciais pontos de evolução e criar planos de ação para evoluir

### Realização de 1:1

- Dinâmica de médio prazo

- Realizar um acompanhamento de carreira com o time, a fim de identificar oportunidades de evolução técnica e pessoal
  - Alinhamento de expectativas
  - Alinhamento de roleguide, caso exista
  - Definição de um plano de ação para criar oportunidade e evidências para evolução na carreita, tanto de forma vertical quanto horizontal
  
 ### PDCA
 
 - Dinâmica contínua
 
 - Apresentar, reforçar e acompanhar a evolução dos OKR´s/KR´s definidos durante o quarter e como está o progresso dos objetivos
 - Mapear potenciais riscos, pedidos de apoio e celebração
 - Oportunidade para engajar, esclarecer dúvidas e realinhar o time com a estratégia planejada
 - Convidar o time e apresentar as propostas de objetivos para os próximos quarters
 
### Qualidade 

- Possuir ambientes de teste/homologação
- Realizar a segregação para validação das features e também cenários e hipóteses de forma controlada
- Possuir gates de inspeção de qualidade de código, como Sonarqube, por exemplo
- Definir gates de cobertura de código e cenários de testes para aplicar como DOD das features/histórias entregues
- Definição de templates de code review com um padrão de issue a ser seguido, definindo pontos necessários como evidências para abertura de PR/MR

### Interoperabilidade

- Mapear quais os pontos de conexão ou potenciais oportunidades para comunicação entre domínios que não se conversam
- EDA (Arquitetura Orientada a Eventos) resolveria este tipo de problema? Qual o nível da falta de comunicação?

### Otimização e consistência dos dados

- Aplicar prática de fail-fast
  - Adicionar lógicas de validação no app pode onerar o tamanho/build do projeto?
    - Uma possibilidade é usar BFF (Backend For Frontend) para validações em um middleware entre o front/canal e o servidor/API
- Garantir também as consistências no back-end, pois esta responsabilidade deve e precisa ser compartilhada (low trust)


### Aprendizagem contínua

- Apresentar proposta e dinâmicas de lifelong learning com time
- Embasamento a partir da aprendizagem significativa
- Tech Drops para compartilhamento e repasse de conhecimento entre o time
  - Incentivo a participação de eventos dentro da empresa e na comunidade
- Proposta de geração de conhecimento com bonificações
  - Gamefication?
  - Brindes?
  - Cursos?
  - Certificações?
- Buddy/mentoria interna
  - Necessário avaliar pares de papel
