# Trabalho ABNT — PBL 3 · Estatística Decisória

> Formato: Times New Roman 12pt · espaçamento 1,5 · margens sup/esq 3cm · inf/dir 2cm · recuo de parágrafo 1,25cm · títulos em negrito.

---

## CAPA

```
CENTRO UNIVERSITÁRIO UNDB
ESTATÍSTICA DECISÓRIA




ARTHUR FONTINELE
LUIS MATEUS
MARCO ANDRÉ
MATHEUS VERAS
PEDRO FERNANDO






ESTUDO DE CORRELAÇÃO E REGRESSÃO LINEAR APLICADO À EMPRESA CLICKPLUS:
otimização do investimento em marketing digital com base em estatística decisória










SÃO LUÍS
2026
```

---

## FOLHA DE ROSTO

```
ARTHUR FONTINELE
LUIS MATEUS
MARCO ANDRÉ
MATHEUS VERAS
PEDRO FERNANDO




ESTUDO DE CORRELAÇÃO E REGRESSÃO LINEAR APLICADO À EMPRESA CLICKPLUS:
otimização do investimento em marketing digital com base em estatística decisória




Trabalho apresentado ao Centro Universitário
UNDB como requisito parcial para avaliação na
disciplina de Estatística Decisória, sob orientação
do Prof. André Fernandes.




SÃO LUÍS
2026
```

---

## SUMÁRIO

```
1   INTRODUÇÃO ............................................................... 03
2   APRESENTAÇÃO DA EMPRESA E DO PROBLEMA ..................................... 04
2.1 A empresa ClickPlus ...................................................... 04
2.2 Problema de pesquisa ..................................................... 04
3   FUNDAMENTAÇÃO TEÓRICA .................................................... 05
3.1 Correlação linear de Pearson ............................................. 05
3.2 Regressão linear simples ................................................. 05
3.3 Coeficiente de determinação (R²) ......................................... 06
4   METODOLOGIA E DADOS ...................................................... 06
5   ANÁLISE E RESULTADOS ..................................................... 07
5.1 Estatística descritiva ................................................... 07
5.2 Análise de correlação .................................................... 08
5.3 Modelo de regressão linear simples ....................................... 09
5.4 Previsões e cenários ..................................................... 10
6   TOMADA DE DECISÃO ........................................................ 11
6.1 Orçamento ideal para meta de R$ 80 mil ................................... 11
6.2 Cliques versus taxa de conversão ......................................... 11
7   LIMITAÇÕES DO ESTUDO ..................................................... 12
8   CONCLUSÃO ................................................................ 13
    REFERÊNCIAS .............................................................. 14
```

---

## 1 INTRODUÇÃO

No cenário contemporâneo de transformação digital, marcado pela alta competitividade entre empresas de comércio eletrônico, a tomada de decisão baseada em dados deixou de ser um diferencial e passou a constituir condição essencial para a sustentabilidade dos negócios. A análise estatística, em particular, oferece ferramentas concretas para identificar padrões, antecipar tendências e fundamentar ações em evidências objetivas, em substituição a decisões baseadas apenas em intuição (BUSSAB; MORETTIN, 2010).

Entre as técnicas estatísticas mais utilizadas pelo mercado, destacam-se a análise de correlação e a regressão linear, que permitem mensurar relações entre variáveis, prever comportamentos e otimizar a alocação de recursos. Empresas como Amazon e Netflix são exemplos consolidados de aplicação dessas metodologias para personalizar estratégias e aumentar a eficiência operacional. No entanto, conforme apontam Levine et al. (2000), a aplicação dessas técnicas está hoje acessível também a empresas de médio porte, que podem se beneficiar de modelos preditivos para competir em um mercado cada vez mais dinâmico.

O presente trabalho tem por objetivo aplicar os conceitos de correlação e regressão linear ao caso da empresa ClickPlus, um e-commerce especializado em produtos eletrônicos, com o intuito de responder à seguinte pergunta-problema: **como a ClickPlus pode otimizar seu investimento em marketing digital para maximizar suas vendas mensais?** Para tanto, foram analisados doze meses de operação da empresa, considerando quatro variáveis: investimento em marketing (R$ mil), número de cliques no site (mil), taxa de conversão (%) e vendas mensais (R$ mil).

O trabalho está estruturado em oito seções. Após esta introdução, apresenta-se a empresa e o problema de pesquisa; em seguida, a fundamentação teórica que sustenta a análise; a metodologia e os dados; os resultados da análise estatística; as decisões recomendadas; as limitações do estudo; e, por fim, a conclusão.

---

## 2 APRESENTAÇÃO DA EMPRESA E DO PROBLEMA

### 2.1 A empresa ClickPlus

A ClickPlus é uma empresa de comércio eletrônico (e-commerce) fundada em 2018, especializada na venda de produtos eletrônicos, tais como smartphones, notebooks, acessórios e gadgets. A empresa atua no segmento Business to Consumer (B2C), oferecendo tecnologia de qualidade a preços competitivos por meio de uma experiência de compra online eficiente.

A estratégia de marketing da empresa concentra-se em mídias digitais — Google Ads, Meta Ads e parcerias com influenciadores —, complementada por campanhas sazonais associadas a eventos como Black Friday e Natal. As métricas-chave acompanhadas pela empresa são os cliques no site, a taxa de conversão e o retorno sobre o investimento (ROI). A infraestrutura conta com plataforma própria de e-commerce e logística terceirizada via transportadoras.

Entre os principais desafios enfrentados pela ClickPlus destacam-se a alta concorrência no setor e a necessidade constante de otimização do orçamento de marketing, especialmente diante da pressão por margens em um setor de varejo digital de baixa diferenciação.

### 2.2 Problema de pesquisa

A equipe de análise da ClickPlus monitorou, durante doze meses consecutivos, o desempenho mensal da empresa nas seguintes variáveis:

- Investimento em marketing (R$ mil) — verba destinada a anúncios digitais;
- Cliques no site (mil) — número de visitantes que clicaram nos anúncios;
- Taxa de conversão (%) — percentual de cliques que resultaram em compra efetiva;
- Vendas mensais (R$ mil) — receita total gerada no período.

A partir desses dados, formula-se a seguinte pergunta-problema: **como a ClickPlus pode otimizar seu investimento em marketing digital para maximizar as vendas, utilizando análise de correlação e regressão linear?**

---

## 3 FUNDAMENTAÇÃO TEÓRICA

### 3.1 Correlação linear de Pearson

O coeficiente de correlação linear de Pearson, representado pela letra *r*, mede a força e o sentido da associação linear entre duas variáveis quantitativas. Seu valor varia entre −1 e +1, sendo que valores próximos de +1 indicam correlação positiva forte (as variáveis crescem juntas), valores próximos de −1 indicam correlação negativa forte (uma cresce enquanto a outra decresce), e valores próximos de zero indicam ausência de relação linear (DOWNING; CLARK, 1999). A fórmula utilizada é:

```
r = Σ[(xᵢ − x̄)(yᵢ − ȳ)]  /  √[Σ(xᵢ − x̄)² · Σ(yᵢ − ȳ)²]
```

### 3.2 Regressão linear simples

A regressão linear simples consiste em ajustar uma reta que melhor descreva a relação entre uma variável independente *x* (preditora) e uma variável dependente *y* (resposta). O modelo é dado pela equação:

```
ŷ = β₀ + β₁ · x
```

Os coeficientes β₀ (intercepto) e β₁ (inclinação) são estimados pelo método dos mínimos quadrados ordinários, que minimiza a soma dos quadrados dos resíduos, isto é, das diferenças entre os valores observados e os preditos pelo modelo (BUSSAB; MORETTIN, 2010). As fórmulas para estimação são:

```
β₁ = Sxy / Sxx       β₀ = ȳ − β₁ · x̄
```

onde Sxy é a soma dos produtos dos desvios e Sxx é a soma dos quadrados dos desvios da variável independente.

### 3.3 Coeficiente de determinação (R²)

O coeficiente de determinação, R², expressa a proporção da variabilidade da variável dependente que é explicada pelo modelo de regressão. Numericamente, é igual ao quadrado do coeficiente de correlação: R² = r². Seu valor varia entre 0 e 1, sendo que valores próximos de 1 indicam que o modelo explica bem o comportamento dos dados (LEVINE et al., 2000).

---

## 4 METODOLOGIA E DADOS

A pesquisa caracteriza-se como um estudo quantitativo, descritivo e aplicado, fundamentado em dados secundários fornecidos pela equipe de análise da empresa ClickPlus, referentes a doze meses consecutivos de operação. As variáveis monitoradas foram organizadas em uma tabela única para fins de análise, conforme apresentado a seguir.

**Tabela 1 — Dados mensais coletados pela ClickPlus (12 meses)**

| Mês | Investimento (R$ mil) | Cliques (mil) | Taxa de Conversão (%) | Vendas (R$ mil) |
|:---:|:---:|:---:|:---:|:---:|
| 1   | 10  | 5,2  | 8,1   | 42 |
| 2   | 15  | 7,1  | 9,3   | 65 |
| 3   | 8   | 4,0  | 7,8   | 38 |
| 4   | 12  | 6,5  | 8,9   | 58 |
| 5   | 18  | 8,7  | 10,2  | 76 |
| 6   | 5   | 3,2  | 6,5   | 28 |
| 7   | 20  | 9,9  | 10,5  | 88 |
| 8   | 14  | 7,8  | 9,7   | 72 |
| 9   | 6   | 3,8  | 7,0   | 35 |
| 10  | 16  | 8,2  | 9,5   | 70 |
| 11  | 11  | 6,0  | 8,5   | 50 |
| 12  | 22  | 10,5 | 11,0  | 95 |

Fonte: Dados fornecidos pela empresa ClickPlus (2026).

Os procedimentos analíticos seguiram quatro etapas: (1) cálculo das estatísticas descritivas das quatro variáveis; (2) cálculo do coeficiente de correlação de Pearson entre cada variável preditora e as vendas; (3) ajuste de um modelo de regressão linear simples entre o investimento em marketing e as vendas mensais; e (4) aplicação do modelo para previsão de cenários e suporte à tomada de decisão.

---

## 5 ANÁLISE E RESULTADOS

### 5.1 Estatística descritiva

A análise descritiva permite caracterizar o comportamento de cada variável ao longo dos doze meses. A Tabela 2 sintetiza as principais medidas obtidas.

**Tabela 2 — Estatísticas descritivas das variáveis (n = 12)**

| Variável | Média | Mediana | Desvio-Padrão | Mínimo | Máximo |
|---|:---:|:---:|:---:|:---:|:---:|
| Investimento (R$ mil) | 13,08 | 13,00 | 5,40  | 5     | 22   |
| Cliques (mil)         | 6,74  | 6,80  | 2,39  | 3,2   | 10,5 |
| Conversão (%)         | 8,92  | 9,10  | 1,39  | 6,5   | 11,0 |
| Vendas (R$ mil)       | 59,75 | 61,50 | 21,52 | 28    | 95   |

Fonte: Elaborado pelos autores (2026).

Observa-se que o desvio-padrão das vendas é elevado em relação à média (coeficiente de variação aproximado de 36%), o que evidencia uma alta heterogeneidade entre os meses analisados. É justamente essa variabilidade que se busca explicar a partir das variáveis preditoras.

### 5.2 Análise de correlação

Aplicou-se o coeficiente de correlação de Pearson entre cada variável preditora (investimento, cliques e taxa de conversão) e a variável resposta (vendas mensais). Os resultados são apresentados na Tabela 3.

**Tabela 3 — Correlação de Pearson entre as variáveis preditoras e as vendas mensais**

| Variável preditora | r | Interpretação |
|---|:---:|---|
| Cliques no site         | 0,9941 | Correlação positiva muito forte |
| Investimento em marketing | 0,9857 | Correlação positiva muito forte |
| Taxa de conversão       | 0,9849 | Correlação positiva muito forte |

Fonte: Elaborado pelos autores (2026).

Verifica-se que **o número de cliques apresenta a correlação mais forte com as vendas** (*r* = 0,9941), seguido pelo investimento em marketing (*r* = 0,9857) e pela taxa de conversão (*r* = 0,9849). As três variáveis exibem associação positiva muito próxima da unidade, o que sugere que todas se comportam como bons preditores das vendas.

Ressalta-se, contudo, que as três variáveis preditoras também são correlacionadas entre si. Isso é compreensível à luz da lógica do funil de marketing digital: o investimento gera tráfego (cliques), que por sua vez se converte em vendas. Tal interdependência será discutida na seção de limitações.

### 5.3 Modelo de regressão linear simples

Considerando que o investimento em marketing é a variável de maior interesse gerencial — por ser diretamente controlável pela empresa — e dada sua forte correlação com as vendas, optou-se por ajustar um modelo de regressão linear simples na forma:

```
Vendas = β₀ + β₁ · Investimento
```

A partir dos dados observados, foram calculadas as somas de desvios:

- Sxx = Σ(xᵢ − x̄)² = 320,92
- Sxy = Σ(xᵢ − x̄)(yᵢ − ȳ) = 1.260,25
- Syy = Σ(yᵢ − ȳ)² = 5.094,25

Aplicando-se as fórmulas dos mínimos quadrados:

```
β₁ = Sxy / Sxx = 1.260,25 / 320,92 ≈ 3,93
β₀ = ȳ − β₁ · x̄ = 59,75 − 3,93 × 13,08 ≈ 8,37
```

Portanto, o modelo estimado é:

```
Vendas = 8,37 + 3,93 · Investimento
```

O coeficiente β₁ ≈ 3,93 indica que, a cada R$ 1.000,00 adicionais investidos em marketing, espera-se um aumento médio de aproximadamente **R$ 3.930,00** nas vendas mensais. O coeficiente β₀ ≈ 8,37 representa as vendas estimadas em um cenário hipotético de investimento zero — ou seja, as vendas de base (orgânicas), sem qualquer campanha paga.

O coeficiente de determinação foi calculado como:

```
R² = r² = (0,9857)² ≈ 0,972
```

Isso significa que **aproximadamente 97,2% da variação observada nas vendas mensais é explicada pelo investimento em marketing**, indicando um ajuste de qualidade muito alta. Os 2,8% restantes correspondem a variações atribuíveis a fatores não incorporados ao modelo (sazonalidade, concorrência, mix de produtos, entre outros).

### 5.4 Previsões e cenários

A aplicação direta do modelo permite estimar as vendas esperadas em diferentes cenários de investimento, conforme apresentado na Tabela 4.

**Tabela 4 — Previsão de vendas em diferentes cenários de investimento**

| Cenário | Investimento (R$ mil) | Vendas previstas (R$ mil) |
|---|:---:|:---:|
| Conservador        | 8  | 39,8 |
| Médio (atual)      | 13 | 59,5 |
| Moderadamente expansivo | 18 | 79,1 |
| Expansivo          | 20 | 86,9 |

Fonte: Elaborado pelos autores (2026).

---

## 6 TOMADA DE DECISÃO

### 6.1 Orçamento ideal para meta de R$ 80 mil

Para responder à pergunta sobre o orçamento adequado a uma meta mensal de R$ 80.000,00 em vendas, basta isolar a variável independente na equação de regressão:

```
x = (ŷ − β₀) / β₁ = (80 − 8,37) / 3,93 ≈ 18,24
```

Conclui-se que, **para atingir a meta de R$ 80.000,00 em vendas mensais, a ClickPlus deve investir aproximadamente R$ 18.240,00 em marketing digital**. Esse valor representa um incremento de cerca de 10% em relação ao investimento médio histórico (R$ 13,08 mil), o que caracteriza uma meta plenamente factível dentro do intervalo de dados observado.

O multiplicador de retorno estimado é de aproximadamente 4,4 vezes, ou seja, cada R$ 1,00 investido em marketing está associado a aproximadamente R$ 4,40 de receita esperada — indicador favorável à expansão controlada do orçamento publicitário.

### 6.2 Cliques versus taxa de conversão

A segunda decisão estratégica refere-se à escolha entre **aumentar o número de cliques** ou **melhorar a taxa de conversão**. A partir dos coeficientes de regressão simples calculados separadamente para cada par de variáveis, obtêm-se as seguintes estimativas marginais:

- Cada **1 mil cliques adicionais** está associado a um aumento médio de aproximadamente **R$ 8,9 mil** em vendas;
- Cada **+1 ponto percentual na taxa de conversão** está associado a um aumento médio de aproximadamente **R$ 15,3 mil** em vendas.

Verifica-se, portanto, que o impacto marginal da taxa de conversão é, em termos absolutos, maior do que o do volume de cliques. Isso ocorre porque uma melhoria na conversão alavanca o tráfego que **já está sendo pago**, multiplicando o resultado de toda a verba já alocada em mídia.

Recomenda-se, assim, a adoção de uma **estratégia híbrida**: manter a expansão do volume de cliques — canal já dominado pela empresa — e, simultaneamente, investir em ações de Conversion Rate Optimization (CRO), tais como melhorias na experiência do usuário, otimização do checkout, redução do frete, prova social e personalização da jornada de compra. Essa combinação tende a oferecer o melhor equilíbrio entre crescimento de tráfego e eficiência do funil.

---

## 7 LIMITAÇÕES DO ESTUDO

Embora os resultados obtidos sejam estatisticamente expressivos, é necessário discutir as limitações que circunscrevem a interpretação do modelo:

1. **Correlação não implica causalidade.** Coeficientes de correlação muito elevados não comprovam relação de causa e efeito. É possível que uma terceira variável (como sazonalidade) influencie simultaneamente o investimento e as vendas, gerando associação espúria. A confirmação de causalidade exige experimentos controlados, como testes A/B.

2. **Tamanho reduzido da amostra.** Com apenas n = 12 observações, o estudo possui poder estatístico limitado para detectar efeitos sutis ou para generalizações robustas. A ampliação da janela temporal — ou o uso de granularidade semanal — fortaleceria a confiança nas estimativas.

3. **Sazonalidade.** Eventos sazonais como Black Friday e Natal podem inflar simultaneamente investimento e vendas, sem que o modelo linear simples capture esse efeito. A introdução de variáveis dummy ou a decomposição da série temporal seriam aprimoramentos pertinentes.

4. **Fatores externos não controlados.** Variáveis como concorrência, conjuntura macroeconômica, lançamentos de produtos e variações cambiais não foram incorporadas ao modelo, podendo enviesar os coeficientes.

5. **Pressuposto de linearidade.** O modelo assume relação linear entre investimento e vendas. Em níveis muito altos de investimento, a relação tende a apresentar retornos decrescentes (saturação), o que sugere que modelos não-lineares (logarítmicos ou polinomiais) podem ser mais adequados em cenários extremos.

6. **Multicolinearidade.** A forte correlação entre as três variáveis preditoras (investimento, cliques e conversão) inviabiliza, na prática, uma regressão múltipla com coeficientes facilmente interpretáveis, dado o caráter funil das relações.

---

## 8 CONCLUSÃO

O presente trabalho aplicou as técnicas de correlação linear de Pearson e regressão linear simples ao caso da empresa ClickPlus, com o objetivo de orientar a otimização do investimento em marketing digital para maximização das vendas mensais.

Os resultados evidenciaram correlações positivas muito fortes entre as três variáveis preditoras e as vendas, com destaque para o número de cliques (*r* = 0,9941). O modelo de regressão linear simples ajustado, **Vendas = 8,37 + 3,93 · Investimento**, apresentou coeficiente de determinação R² = 0,972, indicando que aproximadamente 97% da variabilidade das vendas mensais é explicada pelo investimento em marketing.

A partir do modelo, concluiu-se que: (i) cada R$ 1.000,00 adicionais de investimento estão associados a um incremento médio de R$ 3.930,00 nas vendas; (ii) para atingir a meta mensal de R$ 80.000,00 em vendas, recomenda-se um investimento aproximado de R$ 18.240,00; e (iii) o impacto marginal de melhorias na taxa de conversão é superior ao de aumentos no volume de cliques, justificando a recomendação de uma estratégia híbrida que combine expansão de tráfego e otimização do funil de conversão.

Os objetivos do estudo foram cumpridos: os dados foram organizados e tratados; foram identificadas as relações entre as variáveis; um modelo preditivo simples foi construído; e as principais limitações foram discutidas, com destaque para a distinção entre correlação e causalidade. Recomenda-se, em pesquisas futuras, a ampliação da amostra, o controle de fatores sazonais por meio de variáveis adicionais e a validação experimental das relações observadas mediante testes A/B controlados.

---

## REFERÊNCIAS

BUSSAB, Wilton de O.; MORETTIN, Pedro A. **Estatística básica**. 6. ed. São Paulo: Saraiva, 2010.

DOWNING, Douglas; CLARK, Jeffrey. **Estatística aplicada**. São Paulo: Saraiva, 1999.

LEVINE, David M. et al. **Estatística**: teoria e aplicações. Rio de Janeiro: LTC, 2000.
