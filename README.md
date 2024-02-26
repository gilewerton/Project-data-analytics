
# Análise de Regressão Linear - Faturamento vs Desconto

Este projeto em Python realiza uma análise de regressão linear para investigar a relação entre o faturamento e o desconto em uma série temporal de 52 semanas. O objetivo é determinar se o aumento no faturamento pode ser explicado pelo aumento nos descontos oferecidos.

## Introdução
A empresa Alfa, no último ano, implementou a estratégia de usar descontos como parte de seu plano de marketing para atrair mais clientes e aumentar as vendas. Este projeto visa analisar se a estratégia de desconto adotada pela empresa refletiu no aumento das vendas.

## Conjunto de Dados
O conjunto de dados pode ser acessado [aqui](https://docs.google.com/spreadsheets/d/1H2G8KApyyZVyJ82viDbeotyJG4zcQmMn/edit?usp=sharing&ouid=108379818747706290436&rtpof=true&sd=true). Contém informações semanais de faturamento em reais (R$), desconto total em reais (R$), e a porcentagem de desconto em relação ao faturamento, distribuídos ao longo de 52 semanas.


## Como Funciona
O script em Python utiliza técnicas de regressão linear para analisar a relação entre as variáveis dependentes (faturamento) e independentes (desconto). Realiza uma análise estatística para avaliar a significância da relação e gera visualizações gráficas para facilitar a interpretação dos resultados.

## Requisitos
Certifique-se de ter Python instalado em seu ambiente. Utilize o arquivo de dados fornecido para executar o script.

## Base

| Nu_semana | Faturamento  | Desconto      | % Desconto |
|-----------|--------------|---------------|------------|
| 1         | 1.693.225    | 220.119,25    | 13%        |
| 2         | 1.965.814    | 275.213,96    | 14%        |
| 3         | 988.227      | 39.308,00     | 4%         |
| 4         | 1.939.352    | 290.902,80    | 15%        |
| 5         | 1.035.995    | 176.119,15    | 17%        |
| 6         | 344.336      | 39.785,00     | 12%        |
| 7         | 1.324.270    | 238.368,60    | 18%        |
| 8         | 768.171      | 54.301,00     | 7%         |
| 9         | 1.104.538    | 132.544,56    | 12%        |
| 10        | 882.609      | 49.375,00     | 6%         |
| 11        | 427.652      | 52.669,00     | 12%        |
| 12        | 1.255.683    | 213.466,11    | 17%        |
| 13        | 1.901.857    | 304.297,12    | 16%        |
| 14        | 1.051.444    | 178.745,48    | 17%        |
| 15        | 1.501.909    | 195.248,17    | 13%        |
| 16        | 1.352.342    | 162.281,04    | 12%        |
| 17        | 1.594.301    | 271.031,17    | 17%        |
| 18        | 441.634      | 38.319,00     | 9%         |
| 19        | 1.638.284    | 196.594,08    | 12%        |
| 20        | 1.593.894    | 270.961,98    | 17%        |
| 21        | 426.372      | 27.945,00     | 7%         |
| 22        | 1.805.569    | 252.779,66    | 14%        |
| 23        | 528.790      | 39.992,00     | 8%         |
| 24        | 1.603.719    | 224.520,66    | 14%        |
| 25        | 602.586      | 35.793,00     | 6%         |
| 26        | 1.276.039    | 178.645,46    | 14%        |
| 27        | 1.983.026    | 337.114,42    | 17%        |
| 28        | 1.751.256    | 297.713,52    | 17%        |
| 29        | 1.832.509    | 329.851,62    | 18%        |
| 30        | 488.102      | 32.878,00     | 7%         |
| 31        | 1.103.074    | 198.553,32    | 18%        |
| 32        | 439.956      | 52.797,00     | 12%        |
| 33        | 1.937.403    | 309.984,48    | 16%        |
| 34        | 1.006.697    | 171.138,49    | 17%        |
| 35        | 1.597.205    | 191.664,60    | 12%        |
| 36        | 1.714.801    | 274.368,16    | 16%        |
| 37        | 601.838      | 38.177,00     | 6%         |
| 38        | 1.268.533    | 152.223,96    | 12%        |
| 39        | 598.298      | 41.592,00     | 7%         |
| 40        | 1.069.919    | 160.487,85    | 15%        |
| 41        | 1.211.049    | 157.436,37    | 13%        |
| 42        | 1.804.288    | 306.728,96    | 17%        |
| 43        | 1.969.081    | 354.434,58    | 18%        |
| 44        | 1.404.732    | 224.757,12    | 16%        |
| 45        | 549.792      | 48.405,00     | 9%         |
| 46        | 1.369.643    | 178.053,59    | 13%        |
| 47        | 1.569.229    | 219.692,06    | 14%        |
| 48        | 1.797.336    | 215.680,32    | 12%        |
| 49        | 1.012.722    | 162.035,52    | 16%        |
| 50        | 1.483.581    | 237.372,96    | 16%        |
| 51        | 1.976.206    | 276.668,84    | 14%        |
| 52        | 652.218      | 53.343,00     | 8%         |


## Requisitos
Certifique-se de ter Python instalado em seu ambiente. Utilize o arquivo de dados fornecido para executar o script. As bibliotecas necessárias incluem pandas, altair, statsmodels e seaborn.

## Exemplo de Utilização
A análise a seguir foi desenvolvida no ambiente do [Google Colab](https://colab.google/). Para reproduzir a análise, basta carregar o conjunto de dados no ambiente de sua escolha e executar o script Python fornecido.


## Deploy

Importando a biblioteca pandas e utilizando o apelido 'pd' para facilitar a referência.

```bash
  import pandas as pd
```
Exibindo informações sobre o DataFrame 'df', como número de entradas não nulas e tipos de dados das colunas.

```bash
df.info()
```
## Avaliando os dados 
```bash
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 52 entries, 0 to 51
Data columns (total 4 columns):
 #   Column           Non-Null Count  Dtype  
---  ------           --------------  -----  
 0   Núm_Semana       52 non-null     int64  
 1   Faturamento(R$)  52 non-null     int64  
 2   Desconto (R$)    52 non-null     float64
 3   %Desconto        52 non-null     float64
dtypes: float64(2), int64(2)
memory usage: 1.8 KB
```
Ao analisar o DataFrame, podemos notar que o arquivo contém quatro colunas: “Núm_Semana”, “Faturamento(R$)”, “Desconto (R$)” e “%Desconto”, com 52 entradas cada. As duas primeiras colunas "Núm_Semana" e "Faturamento" são do tipo inteiro e as duas últimas colunas do tipo float.

## Visualizar tabela
```bash
df.head()
```
```bash
Núm_Semana	Faturamento(R$)	   Desconto(R$)	   %Desconto
	1	        1693225	        220119.25	     0.13
	2	        1965814	        275213.96	     0.14
	3	        988227	        39308.00	     0.04
	4	        1939352	        290902.80	     0.15
	5	        1035995	        176119.15	     0.17
```
Ao executar o comando acima, podemos visualizar agora a tabela e valores contidos no dataframa em formato de tabela contendo as primeiras 5 linhas e colunas existentes. Nota-se que o os valores estão sem formatação, sem os separadores de milhares. Sendo assim vamos inserir uma formação para uma melhor visuaização dos valores.

```bash
df.applymap(lambda x: " {:_.2f}".format(x).replace(".", ",").replace("_", "."))
```
Esse código irá formatar os valores do DataFrame com duas casas decimais, separador de milhares (.) e separador decimal (,).

```bash
Núm_Semana	    Faturamento(R$)	  Desconto (R$)	  	%Desconto
1,00			1.693.225,00		220.119,25		0,13
2,00			1.965.814,00		275.213,96		0,14
3,00			988.227,00		    39.308,00		0,04
4,00			1.939.352,00		290.902,80		0,15
5,00			1.035.995,00		176.119,15		0,17
6,00			344.336,00		    39.785,00		0,12
```

## visualização: Gráfico de dispersão

```bash
from matplotlib import pyplot as plt

df.plot(kind='scatter', x='Desconto (R$)', y='Faturamento(R$)', s=32, alpha=.8)
plt.gca().spines[['top', 'right',]].set_visible(False)
plt.title('Faturamento vs Desconto')
```
![regressao1](https://github.com/gilewerton/Projeto.data-analytics/assets/161247234/c97a3767-da4c-421e-bd3d-6f11875ab075)

Para visualizarmos o gráfico, iremos utilizar a biblioteca [matplotlib](https://matplotlib.org/stable/index.html) e import pyplot. Para geração do gráfico iremos utilizar alguns parâmetros fundamentais, são eles:

* **kind='scatter':** Isso indica que você está criando um gráfico de dispersão, que mostra a relação entre duas variáveis numéricas.
* **x='Desconto (R$)':** O eixo x é baseado nos dados da coluna ‘Desconto (R$)’, que representa o valor do desconto aplicado em cada venda.
* **y='Faturamento(R$)':** O eixo y é baseado nos dados da coluna ‘Faturamento(R$)’, que representa o valor total da venda.
* **s=32:** Define o tamanho dos marcadores no gráfico de dispersão, que são os pontos azuis que representam cada dado observado. Neste caso, o tamanho é fixo e igual a 32.
* **alpha=.8:** Controla a opacidade dos marcadores, que é o grau de transparência dos pontos. Neste caso, eles são relativamente opacos, com um valor de 0.8 (onde 0 é totalmente transparente e 1 é totalmente opaco).

## Linha de Regresão 
```bash
X = df['Desconto (R$)']
y = df['Faturamento(R$)']

# Adicionando uma constante à variável independente
X = sm.add_constant(X)

# Criando o modelo de regressão linear
model = sm.OLS(y, X).fit()

# Imprimindo os resultados da regressão
print(model.summary())

# Criando o gráfico com Seaborn
plt.figure(figsize=(8, 4))
sns.regplot(x='Desconto (R$)', y='Faturamento(R$)', data=df, scatter_kws={'s': 50})

plt.title('Distribuição do Faturamento vs. Desconto com Linha de Regressão')

plt.show()
```

* **Dados de entrada:** Estamos usando um DataFrame df e selecionando as colunas ‘Desconto (R$)’ e ‘Faturamento(R$)’ para representar os dados no eixo X e Y, respectivamente.
* **Modelo de regressão linear:** Está sendo criado um modelo de regressão linear com a biblioteca statsmodels, onde ‘Desconto (R$)’ é tratado como variável independente após adicionar uma constante a ela, e ‘Faturamento(R$)’ como variável dependente.
* **Gráfico com Seaborn:** Vamos utilizar a biblioteca Seaborn para criar o gráfico. O tamanho do gráfico é definido por figsize=(8, 4). Os dados são plotados usando o método regplot, onde os parâmetros x=‘Desconto (R$)’, y=‘Faturamento(R$)’, data=df são usados para definir os dados que serão plotados. O parâmetro scatter_kws={'s': 50} é usado para definir o tamanho dos marcadores no gráfico. Ajuste conforme a necessidade  para uma melhor visualização.
* **Título do Gráfico:** O (plt.title) estamos utilizando para nomear o gráfico como o título “Distribuição do Faturamento vs. Desconto com Linha de Regressão”.

```bash
  OLS Regression Results                            
==============================================================================
Dep. Variable:        Faturamento(R$)   R-squared:                       0.892
Model:                            OLS   Adj. R-squared:                  0.890
Method:                 Least Squares   F-statistic:                     412.6
Date:                Mon, 26 Feb 2024   Prob (F-statistic):           8.28e-26
Time:                        18:42:03   Log-Likelihood:                -699.67
No. Observations:                  52   AIC:                             1403.
Df Residuals:                      50   BIC:                             1407.
Df Model:                           1                                         
Covariance Type:            nonrobust                                         
=================================================================================
                    coef    std err          t      P>|t|      [0.025      0.975]
---------------------------------------------------------------------------------
const          3.861e+05    4.9e+04      7.884      0.000    2.88e+05    4.84e+05
Desconto (R$)     4.9186      0.242     20.313      0.000       4.432       5.405
==============================================================================
Omnibus:                        3.217   Durbin-Watson:                   1.726
Prob(Omnibus):                  0.200   Jarque-Bera (JB):                2.567
Skew:                           0.413   Prob(JB):                        0.277
Kurtosis:                       2.292   Cond. No.                     4.15e+05
==============================================================================
```
[![regresão2](https://github.com/gilewerton/Projeto.data-analytics/assets/161247234/acf3c0ff-ee53-4340-9a61-4a9e534adbca)](https://github.com/gilewerton/Projeto.data-analytics/issues/1#issue-2155282500)

## Análise dos dados:
* **R-quadrado:** O valor de R-quadrado é 0,892, o que significa que o modelo de regressão linear explica cerca de 89,2% da variação no faturamento em função do desconto. Isso indica um bom ajuste do modelo aos dados, pois quanto mais próximo de 1, melhor.
* **Coeficientes:** O coeficiente para o desconto é 4,9186, o que significa que para cada aumento de R$1 no desconto, podemos esperar um aumento de aproximadamente R$4,92 no faturamento.
* **Gráfico:** O gráfico dispersão com uma linha de regressão, representando a relação entre o desconto e o faturamento. Os pontos estão dispersos, mas seguem uma tendência ascendente clara, indicada pela linha de regressão. Isso confirma a correlação positiva entre as duas variáveis.

## Conclusão
A análise dos resultados da regressão mostra uma forte **correlação positiva** entre o desconto (R$) e o faturamento (R$), com um R-quadrado de 0,892. Isso indica que aproximadamente 89,2% da variação no faturamento pode ser explicada pela variação no desconto. O coeficiente para o desconto é 4,9186, sugerindo que para cada aumento de R$1 no desconto, podemos esperar um aumento de aproximadamente R$4,92 no faturamento.

A relação positiva entre o desconto e o faturamento implica dizer que aumentos nos descontos implinca em aumentos substanciais no faturamento. Portanto, estratégias que envolvem oferecer descontos podem ser eficazes para aumentar o faturamento. Claro, nessa análise de exemplo não iremos analisar a rentabilidade ou outro indicador de lucratividade.

Nessa análise, podemos observar como o análise de regresão pode ser um instrumento importante no dia-a-dia de um profissional quando queremos analisar a influência ou comportamento de duas variáveis. Outra análises como:

* Qual a relação entre IDH (Indice de desenvolvimento humano) com o PIB( Produto Interno Bruto) de um país?
* Analise a relação entre o nível de educação de uma população (por exemplo, percentual de pessoas com ensino superior) e a renda média do país. Isso pode ajudar a entender como investimentos em educação impactam o desenvolvimento econômico.
* A relação entre preços de imóveis em uma região e características locais, como acesso a transporte público, proximidade de centros urbanos e qualidade de vida. Isso pode ser interessante para entender os fatores que influenciam o mercado imobiliário.
