# Projeto: Qual o melhor plano?

Você trabalha como analista para a empresa de telecomunicações Megaline. A empresa oferece aos clientes dois planos pré-pagos: Surf e Ultimate. O departamento comercial quer saber qual dos planos gera mais receita para ajustar o orçamento de publicidade. Você vai realizar uma análise preliminar dos planos com base em uma pequena seleção de clientes. Você terá dados de 500 clientes da Megaline: que clientes são, de onde eles são, qual plano usam e o número de chamadas e mensagens realizadas em 2018. Seu trabalho é analisar o comportamento dos clientes e determinar qual plano pré-pago gera mais receita.

Devemos determinar qual dos dois planos pré-pagos hoje utilizados pela Megaline, Surf ou Ultimate, gera mais receita para atender ao pedido do departamento de marketing de ajuste do orçamento de relações públicas. Estudaremos o comportamento do cliente usando uma amostra de 500 usuários coletada de 1º de janeiro de 2018 a 31 de dezembro de 2018. Idade, cidade, número e duração das chamadas, duração das sessões de internet e número de mensagens de texto usadas por cada usuário estão incluídos na amostra. O cálculo da receita de uso e das estatísticas descritivas da população de usuários é necessário para se chegar a uma conclusão sobre a atividade de um plano para a empresa. Calcular as quantidades de elementos do plano que cada usuário utiliza, retirar a restrição de inclusão do plano, limitar o uso do exedente e adicionar um valor mensal definido são os próximos passos. 

Depois de fazer isso, começaremos a examinar a média, a distribuição e quais conclusões podemos tirar das duas populações. Dadas as nossas conclusões quanto ao comportamento histórico dos usuários de ambos os planos, testaremos as duas hipóteses a seguir:

**Hipótese 1**
*A receita média gerada pelos usuários dos planos Ultimate e Surf é diferente.*

**Hipótese 2**
*Os usuários da região NY-NJ têm uma receita média diferente dos usuários de outras regiões.*

**Ações a serem tomadas:**

- Revisar a estrutura dos dataframes.
- Modificar os dataframes conforme necessário (exemplo de tipo de dados em cada coluna).
- Por ter várias tabelas com dados diferentes em cada uma, é necessário unificar todas as informações em uma única  tabela que permite fazer mais facilmente os cálculos tendo as informações de cada usuário, de acordo com seu plano, para cada mês que o serviço foi contratado.
- Fazer uma análise através de gráficos para observar o comportamento de cada plano.
- Conferir as hipóteses estabelecidas pela Megaline.

Por fim, descreveremos as nossas conclusões relativamente à eficácia de ambos os planos e faremos uma recomendação ao departamento de marketing sobre em qual plano devem concentrar os seus esforços e concentrar o orçamento de relações públicas.

**Conclusões**

Inicialmente foi realizado uma descrição dos dados e DataFrames disponíveis. Após as análises iniciais do DataFrame, foram feitas correções ao nível de tipo dos dados. Foi necessário um refinamento dos dados, tanto para adicionar novas variáveis que facilitassem nossas análises, como os excedentes de consumo como o mês vinculado a cada receita dos clientes. Posteriormente foi necessário criar um DataFrame que fosse a junção de todos os outros necessários para a realização do estudo. Os valores ausentes foram tratados, com exceção de uma variável, churn_date, que não era relevante para a concretização do estudo. Os outros valores ausentes foram substituídos por zero (0), uma vez que a ausência de consumo implica na não utilização. Após o refinamento, seguimos para as análises dos dados.

O comportamento e consumo dos clientes foram descritos. Também foi possível sugerir políticas de negócios e ações a serem tomadas pela empresa, visando uma maior fidelização e experiência de usuário para seus clientes, junto as suas próprias necessidades. A análise dos dados seguiu com a visualização em gráficos de histogramas e dispersão, tanto da visualização da receita, consumo e excedentes dos clientes, quanto da visualização da receita por idades e por cidades de residência dos usuários. Medidas de desvio padrão, variância, média e mediana foram realizadas para todo o DataFrame.

**De acordo com o que foi observado no comportamento dos usuários em cada plano:**

* O uso da Internet é o mesmo em ambos os planos. 
* As principais diferenças encontram-se no número de mensagens enviadas e no total de minutos utilizados nas chamadas; para estas categorias, os usuários do **plano ultimate** tiveram maior atividade em comparação com os usuários do **plano surf**.

**Em relação às hipóteses:**

**HIPÓTESE 1**
- Foi realizado um teste de hipótese com alpha de 5% no qual resultou na informação de que a receita média dos usuários dos planos Ultimate e Surf são diferentes.
- Aplicado também o teste de levene onde verificamos que as variâncias das amostras eram significativamente diferentes.

**HIPÓTESE 2**
- A hipótese 2, levantava a questão de que a receita média gerada pelos usuários das regiões NY e NJ eram diferentes aos de outras regiões, na qual foi confirmada via t-test e o método levene de que sim, há evidências estatísticas de que a receita média dos usuários da área de NY-NJ difere dos usuários das demais regiões. 

**Conclusão de negócios:**

Relativamente ao problema empresarial a resolver inicialmente colocado, a que plano deverão ser dedicados mais esforços publicitários? 

Pode-se concluir que a melhor opção para tal é aumentar a publicidade do **plano surf**, pois, embora geralmente gere receitas semelhantes às do **plano ultimate**, os usuários deste plano tendem a ultrapassar mais frequentemente os limites do seu plano, o que se traduz em "receita excedente" para a empresa.
