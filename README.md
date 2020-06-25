# Tech Challenge Gerente de BI - Delivery Much

----

## Estruturação de Time

Para uma equipe de BI atender a todas áreas da Delivery Much, creio que a melhor forma seria horizontalmente, onde atenderia a todos os times e ficaria abaixo de CTO, CEO e CFO & COO.

![DeliveryMuch](https://github.com/theadriano/DeliveryMuch/blob/master/deliverymuch.PNG)

Para a estruturação de time, antes de mais nada, teria que entender as demandas totais de trabalho para serem analisados os perfis a serem disponibilizados. Entretanto, penso que para compôr um time de BI deveria ter profissionais como: Arquiteto de Dados, responsável em organizar o Data Warehouse ou Data Lake; Engenheiro de Dados, responsável na construção dos pipelines que irão popular o DW ou o Data Lake; Analista de Dados, responsável pela construção dos dashboards dentro da ferramenta utilizada na Delivery Much.

Após o levantamento das características de perfis para o time, seria dado início ao processo de seleção dos profissionais. Penso que o processo de entrevista deve ter três etapas após a divulgação e a inscrição dos candidatos nas vagas oferecidas:

1. Entrevista com o RH da empresa para entender o perfil do profissional.
2. Teste técnico focando nas características da vaga. Por exemplo, na vaga para um Analista de Dados, seria confeccionado um teste em que o candidato deveria criar um dashboard com os dados fornecidos pela Delivery Much.
3. Uma entrevista final, nesse caso com o Gerente de BI, para ele entender completamente o perfil do candidato. Nessa entrevista, procuraria entender os projetos que os candidatos trabalharam e qual o papel que exerceram dentro dos projetos. Com esse entendimento, será possível montar uma equipe mais eficiente, bem como, trazer novas ideias para o time.

Após essas três etapas, o candidato sendo aprovado, seria feito todo o onboarding com o profissional onde é dado as boas-vindas e o devido treinamento é aplicado.

----
## Visão de Negócio

Após a extração dos dados pertinentes, construção dos dashboards e a apresentação dos mesmos aos diretores e analistas de cada departamento, é possível ter uma visão macro de todo o negócio da Delivery Much.

Os setores Financeiro e de Operações, conseguiriam traçar estratégias de como angarearmais fornecedores, em quais cidades expandir o serviço, em quais prazos de entrega aplicar melhorias, entre outros.

Para os setores de Engenharia e Produto, mostraria dashboards contendo feedback dos usuários, performance do aplicativo e servidores; sempre visando a melhoria do que é entregue ao usuário final.

Marketing e Gente, usuariam dashboards também para ver o feedback dos usuários e para planejar a comunicação com eles e, também, planejar a divulgação dos serviços do aplicativo.

----
## Gestão do dia-a-dia
Para a criação de um backlog, utilizei a ferramenta Trello da Atlassian.
Para uma sprint quinzenal, envolvendo 5 analistas, baseei-me na seguinte pontuação Fibonacci:

1 ponto - 1 hora

2 pontos - 1 dia

3 pontos - 3 dias

5 pontos - 5 dias

8 pontos - 7 dias

13 pontos - 10 dias

21 pontos - 15 dias

>[Link Kanban](https://trello.com/b/YdH9EJgi/delivery-much)

![Kanban](https://github.com/theadriano/DeliveryMuch/blob/master/kanban.PNG)

----
## Conhecimento Técnico
![Google Cloud Plataform](https://github.com/theadriano/DeliveryMuch/blob/master/google%20cloud%20plataform.PNG)

Usei a plataforma do Google Cloud para poder fazer a extração e análise dos dados. Escolhi essa plataforma pois, dentre as plataformas cloud que já utilizei, a da Google foi com a qual me senti mais facilidade para o trabalho. Além disso, Como eu já tinha gasto os nas outras clouds os valores que é dado gratuitamente, optei pela Google Cloud. Dentro dela, consegui fazer upload dos arquivos compartilhados para o teste dentro de um composer para ser utilizado o Apache Airflow, que foi necessário para orquestrar todo o pipeline de dados. O composer é um kubernete que é serverless, sendo fácil a utilização pois inicia com um serviço ou aplicação que queira. Além disso, o Apache Airflow é melhor para o monitoramento das tasks. Dentro do Apache Airflow utilizei a linguagem Python para fazer a manipulação das tasks. Além disso, com o Airflow, tenho maior gerenciamento, dinamismo e manutenção do pipeline.
Para a manipulação dos dados, utilizei comandos bash, linguagem Python e yml (arquivos utilizados estão logo abaixo). Por exemplo, para o download dos arquivos, foi utilizado o comando curl. Tal comando é usado para fazer o download de endereços http e https.

>[Monitoramento Airflow](https://github.com/theadriano/DeliveryMuch/blob/master/airflow_monitoring.py)
>[Arquivo de Configuração](https://github.com/theadriano/DeliveryMuch/blob/master/DeliveryMuch.yml)
>[Execução dos Processos](https://github.com/theadriano/DeliveryMuch/blob/master/DagCode.py)
No Google Cloud Plataform, utilizei o Google Big Query para fazer a análise das tabelas. Decidi utilizar o Big Query pois ele armazena dados de diferentes formatos e tem particionamento de tabelas. E, também, utilizei Cloud Storage para melhor utilizar os source files.
Para a criação do dashboard, utilizei o Tableau, onde fiz conexão com o Google Big Query.

>[Link para acompanhar os processos Airflow](https://console.cloud.google.com/composer/environments/detail/southamerica-east1/deliverymuch/monitoring?project=opportune-balm-281114)

![ETL](https://github.com/theadriano/DeliveryMuch/blob/master/ETL.PNG)

Usando como base de dados "stores", criei um dashboard onde mostra o tempo de entrega que a Delivery Much oferece ao usuário e a média que leva para o pedido ser entregue.
Tomando em contrapartida o dashboard, ele serviria para o time de Operações para criar uma estratégia adequada de melhoramento no serviço proposto. Assim como, angariar novos franqueados que buscam melhorias nos seus serviços de entrega. Para o departamente de Marketing, o dashboard é ideal para ser criado uma propaganda onde mostra a qualidade e rapidez no serviço de entrega da Delivery Much. Criei, também, um dashboard onde mostra a contagem de registros (pedidos) relacionados ao tempo de entrega proposto pela Delivery Much. Através da análise do dashboard, é possível até fazer uma melhoria no tempo de entrega proposto.

Abaixo está o link para o Tableau mostrando os dashboards criados:

>[Dashboards Delivery Much](https://public.tableau.com/profile/adriano.mendes#!/vizhome/DeliveryMuch/Histria-DeliveryMuch?publish=yes)

----
## Observação

Adicionei o e-mail tech.challenge@deliverymuch.com.br para que possa visualizar o Kanban na ferramenta Trello e, também, o e-mail foi adicionado no Google Cloud para que possa ver os processos Airflow.
