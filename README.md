# Subway Data Analysis

# Introduction
O sistema de ônibus e trens de Nova Iorque - o Metro Transit Authority - fornece seus dados para download através de arquivos CSV. Dentre as informações disponíveis estão os registros semanais de dados das catracas do metrô.

Estes registros contém contagens cumulativas das entradas e saídas, normalmente agrupadas em períodos de 4 horas, com dados adicionais que permitem identificar a estação e catraca específica correspondente a cada linha do arquivo. Neste projeto iremos utilizar um desses registros, mas não precisa baixar nada agora! O primeiro exercício será escrever um código Python para fazer isso por você :-)

# Sobre este projeto
Neste projeto você irá aplicar todos os conhecimentos adquiridos neste primeiro mês de curso, com tarefas básicas de aquisição e limpeza de dados. No processo iremos descobrir informações essenciais sobre os dados, utilizando o que foi aprendido no curso de estatística.

O objetivo deste projeto é explorar a relação entre os dados das catracas do metrô de Nova Iorque e o clima no dia da coleta. Para isso, além dos dados do metrô, precisaremos dos dados de clima da cidade de Nova Iorque.

Os principais pontos que serão verificados neste trabalho:

Coleta de dados da internet
Utilização de estatística para análise de dados
Manipulação de dados e criação de gráficos simples com o Pandas
Como conseguir ajuda: Sugerimos que busque apoio nos canais abaixo, na seguinte ordem de prioridade:

# Sobre o dataset

Descrição das colunas:

C/A,UNIT,SCP,STATION,LINENAME,DIVISION,DATE,TIME,DESC,ENTRIES,EXITS

C/A      = Agrupamento de catracas de que a catraca faz parte (_Control Area_)

UNIT     = Cabine de controle associada à estação onde a catraca se encontra (_Remote Unit for a station_)

SCP      = Endereço específico da catraca (_Subunit Channel Position_)

STATION  = Nome da estação onde a catraca se encontra

LINENAME = Código representando todas linhas que passam na estação*

DIVISION = Código representando a concessionária original da linha, antes da prefeitura assumir a gestão   

DATE     = Representa a data (no formato MM-DD-YY) do evento de auditoria agendado

TIME     = Representa o horário (hh:mm:ss) do evento de auditoria agendado

DESc     = Descreve o tipo de evento de auditoria registrado:
           1. "REGULAR" representando um evento de auditoria padrão, em que a contagem é feita a cada 4 horas
           2. "RECOVR AUD" significa que o valor específico estava perdido, mas foi recuperado posteriormente 
           3. Diversos códigos sinalizam situações em que auditorias são mais frequentes devido a atividades de
              planejamento ou solução de problemas. 
              
ENTRIES  = A contagem cumulativa de entradas associadas à catraca desde o último registro

EXITS    = A contagem cumulativa de saídas associadas à catraca desde o último registro

*  Normalmente as linhas são representadas por um caractere. LINENAME 456NQR significa que os trens 4, 5, 6, N, Q e R passam pela estação.
