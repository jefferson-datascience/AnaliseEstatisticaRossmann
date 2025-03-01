# 1.0 Objetivo do Projeto

O objetivo deste projeto de estudo é realizar uma análise estatística sobre uma base de dados públicos para melhorar habilidades sobre analise de correlação e influência de variáveis sobre uma variável alvo e, para que isso ocorresse, utilizamos um bsae de dados públicos de uma competição no kaggle em que, nessa competição, o objetivo era prever as vendas das próximas 6 semanas de uma rede de drogarias. Entretanto, adaptamos o problema de negócio para entender quais variáveis influenciavam o aumento ou a queda nas vendas. Logo abaixo, você encontrará a visão geral do problemas e a resolução que foi dada.

# 2.0 Problema de Negócio

A Rede de Drogarias Rossmann é uma rede com 3.000 lojas espalhadas por 7 países europeus e com mais de 30 anos de mercado. Os superintendentes solicitaram planos e ações para os gerentes das lojas para que uma melhoria no faturamento dessas redes. Em apoio a esses gerentes, recebemos a demanda de entender quais variáveis influenciam positivamente ou negativamente o faturamento dessas lojas para que, a partir dessas variáveis, realizem planos estratégicos e melhores organizações de times para o atingimento desse objetivo.

## 2.1 Proposta de Solução

Entendido o nosso problema de negócio, uma solução inicial para a resolução desse problema é a estruturação de uma análise de correlação com o intuito de entender como as variáveis são relacionadas com o faturamento das lojas e, além disso, uma análise de regressão para que possamos entender como as variáveis impactam diretamente no faturamento.

##  2.2 Entrega Final

Nossa entrega final será um relatório com as variáveis que impactam os faturamento, uma análise sobre essas variáveis e, por fim, recomendações a partir dessa análise.

## 2.3 Base de Dados Principal

Após a junção dos dados de cadastro da loja e os dados com informações de vendas, promoções ativas e outros detalhes, trabalhamos com a seguinte base de dados, com uma volumetria de aproximadamente 1.1 Milhão de dados, composta das seguintes colunas:

**Store**: Um identificador único para cada loja.

**Sales**: O faturamento de qualquer dia específico (isso é o que você está prevendo).

**Customers**: O número de clientes em um dado dia.

**Open**: Um indicador se a loja estava aberta: 0 = fechada, 1 = aberta.

**StateHoliday**: Indica um feriado estadual. Normalmente, todas as lojas, com poucas exceções, estão fechadas em feriados estaduais. Note que todas as escolas estão fechadas em feriados públicos e fins de semana. a = feriado público, b = feriado de Páscoa, c = Natal, 0 = Nenhum.

**SchoolHoliday**: Indica se a (Loja, Data) foi afetada pelo fechamento das escolas públicas.

**StoreType**: Diferencia entre 4 modelos de lojas diferentes: a, b, c, d.

**Assortment**: Descreve um nível de sortimento: a = básico, b = extra, c = estendido.

**CompetitionDistance**: Distância em metros até a loja concorrente mais próxima.

**CompetitionOpenSinceMonth/Year**: Dá o ano aproximado e o mês em que a loja concorrente mais próxima foi aberta.

**Promo**: Indica se uma loja está realizando uma promoção nesse dia.

**Promo2**: Promo2 é uma promoção contínua e consecutiva para algumas lojas: 0 = a loja não está participando, 1 = a loja está participando.

**Promo2SinceYear/Month:** Descreve o ano e a semana do calendário em que a loja começou a participar da Promo2.

**PromoInterval**: Descreve os intervalos consecutivos em que a Promo2 é iniciada, nomeando os meses em que a promoção é reiniciada. Por exemplo, "Fev, Mai, Ago, Nov" significa que cada rodada começa em fevereiro, maio, agosto e novembro de qualquer ano para aquela loja.

# 3.0 Análise Exploratória dos Dados

