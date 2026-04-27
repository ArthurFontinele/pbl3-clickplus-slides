# Roteiro de Apresentação · PBL 3 — ClickPlus

> Estudo de Correlação e Regressão Linear · Equipe: Arthur Fontinele · Matheus Veras · Pedro Fernando · Luis Mateus · Marco André

**Tempo total estimado:** 12–15 minutos · **Sugestão:** dividir os slides entre os 5 integrantes (3 slides por pessoa).

---

## 🎬 Slide 1 — Capa

**(quem fala: 1º integrante — abertura)**

> "Boa tarde a todos. Somos a equipe **Arthur, Matheus, Pedro, Luis e Marco**, e hoje vamos apresentar nosso PBL 3 de Estatística Descritiva: um **Estudo de Correlação e Regressão Linear** aplicado à empresa **ClickPlus**, um e-commerce de eletrônicos.
>
> Nosso objetivo é mostrar como técnicas estatísticas simples podem ajudar uma empresa real a tomar decisões melhores sobre quanto investir em marketing digital."

**Dica:** apertar **F** para entrar em fullscreen antes de começar.

---

## 🎬 Slide 2 — Contexto

> "Vivemos hoje uma era de transformação digital, em que as empresas precisam tomar decisões cada vez mais rápidas e baseadas em **dados**, não em intuição.
>
> A análise de dados serve para três coisas principais:
> 1. **Medir relações** entre variáveis — por exemplo, será que investir mais em marketing realmente aumenta as vendas?
> 2. **Prever comportamentos** — quanto a empresa vai vender no próximo mês?
> 3. **Otimizar recursos** — onde colocar cada real para ter o maior retorno?
>
> Empresas como Amazon e Netflix já usam isso há anos. A boa notícia é que essas técnicas estão acessíveis também para empresas médias — e é exatamente isso que vamos demonstrar."

---

## 🎬 Slide 3 — A empresa ClickPlus

> "A **ClickPlus** é uma empresa fictícia, mas montada com características realistas:
>
> - **Segmento:** B2C, varejo digital de eletrônicos — smartphones, notebooks, gadgets;
> - **Marketing:** foca em mídia paga (Google Ads, Meta Ads, influenciadores) e campanhas sazonais como Black Friday e Natal;
> - **Métricas-chave:** cliques no site, taxa de conversão e ROI;
> - **Infraestrutura:** plataforma própria com logística terceirizada;
> - **Maior desafio:** alta concorrência e necessidade de **otimizar o orçamento de marketing**.
>
> A equipe de análise da ClickPlus monitorou **12 meses** de operação. Esses dados são a matéria-prima do nosso estudo."

---

## 🎬 Slide 4 — O Problema

**(quem fala: 2º integrante)**

> "A pergunta que vamos responder é direta:
>
> **Como a ClickPlus pode otimizar seu investimento em marketing digital para maximizar as vendas, usando correlação e regressão linear?**
>
> Para responder, vamos olhar 4 variáveis monitoradas mês a mês:
> - **Investimento em Marketing** (R$ mil) — quanto foi gasto em anúncios;
> - **Cliques no Site** (mil) — quantos visitantes clicaram nos anúncios;
> - **Taxa de Conversão** (%) — quantos desses cliques viraram venda;
> - **Vendas Mensais** (R$ mil) — receita gerada.
>
> Os objetivos do estudo, conforme o briefing, são: **organizar os dados**, **identificar relações**, **criar um modelo preditivo simples** e **discutir as limitações** desse modelo."

---

## 🎬 Slide 5 — Dados completos (12 meses)

> "Aqui está a tabela com os 12 meses observados. Repare nos extremos:
>
> - O **menor mês** teve apenas R$ 5 mil em marketing e gerou R$ 28 mil em vendas;
> - O **maior mês** teve R$ 22 mil em marketing e gerou R$ 95 mil em vendas.
>
> Já dá para suspeitar visualmente: quando o investimento sobe, as vendas sobem junto. Mas ‘achar’ não basta — precisamos **medir** essa relação. É o que vem a seguir."

---

## 🎬 Slide 6 — Estatística descritiva

> "Antes de qualquer modelo, sempre olhamos o **resumo estatístico**:
>
> - O investimento médio mensal foi de **R$ 13,08 mil**, variando de R$ 5 a R$ 22 mil;
> - A média de cliques foi **6,74 mil**, e a média de conversão foi **8,92%**;
> - As vendas médias foram **R$ 59,75 mil** por mês, com desvio-padrão alto (R$ 21,5 mil).
>
> Esse desvio-padrão alto é importante: ele mostra que as vendas **variam muito** de mês para mês. E é justamente essa variação que vamos tentar **explicar** com as outras variáveis."

---

## 🎬 Slide 7 — Correlação (Pearson)

**(quem fala: 3º integrante)**

> "Aqui calculamos o **coeficiente de correlação de Pearson** (representado por *r*) entre cada variável e as vendas. Esse coeficiente vai de −1 a +1:
>
> - Próximo de **+1** = relação positiva forte (sobe junto);
> - Próximo de **0** = sem relação;
> - Próximo de **−1** = relação negativa forte (uma sobe, a outra desce).
>
> Os resultados foram impressionantes:
>
> - **Cliques × Vendas: r = 0,9941** ← a correlação mais forte
> - **Investimento × Vendas: r = 0,9857**
> - **Conversão × Vendas: r = 0,9849**
>
> Todas as três são correlações **muito fortes e positivas**. A vencedora é a quantidade de **cliques**.
>
> ⚠️ **Cuidado:** as três variáveis também são correlacionadas entre si — isso é típico de uma cadeia em funil: **investir gera cliques, que geram vendas**. Vamos tratar disso nas limitações."

---

## 🎬 Slide 8 — Diagrama de Dispersão

> "Este é o **gráfico de dispersão** entre Investimento (eixo X) e Vendas (eixo Y). Cada ponto azul é um mês.
>
> Repare como os pontos formam uma linha quase reta, subindo da esquerda para a direita. A linha verde tracejada é a chamada **reta de regressão** — a melhor linha que conseguimos traçar passando ‘pelo meio’ dos pontos, usando o método dos **mínimos quadrados**.
>
> Os números à direita serão explicados no próximo slide."

---

## 🎬 Slide 9 — Regressão Linear

**(quem fala: 4º integrante)**

> "Encontramos a equação:
>
> **Vendas = 8,37 + 3,93 × Investimento**
>
> O que significa cada parte?
>
> - **β₀ = 8,37** → é o **intercepto**: se o investimento fosse zero, esperaríamos cerca de R$ 8,37 mil em vendas (vendas ‘orgânicas’, sem propaganda).
> - **β₁ = 3,93** → é a **inclinação**: para **cada R$ 1.000 a mais investidos** em marketing, esperamos **R$ 3.930 a mais em vendas**. É o ROI estimado.
> - **R² = 0,972** → significa que **97,2% da variação das vendas é explicada pelo investimento**. É um modelo extremamente forte.
>
> Os coeficientes vêm da fórmula clássica: β₁ = Sxy ÷ Sxx (covariância dividida pela variância de X), e β₀ = ȳ − β₁·x̄."

---

## 🎬 Slide 10 — Previsão

> "Com a equação na mão, podemos **prever** o que vai acontecer em diferentes cenários:
>
> - Investindo **R$ 8 mil** → vendas previstas ≈ **R$ 39,8 mil**;
> - Investindo **R$ 13 mil** (média atual) → vendas previstas ≈ **R$ 59,5 mil**;
> - Investindo **R$ 20 mil** → vendas previstas ≈ **R$ 86,9 mil**.
>
> Isso responde a primeira pergunta da tomada de decisão: **‘se aumentarmos o investimento em R$ 1 mil, quanto deve subir nas vendas?’** Resposta: cerca de R$ 3.930."

---

## 🎬 Slide 11 — Tomada de decisão I (orçamento ideal)

**(quem fala: 5º integrante)**

> "O briefing pediu: **qual o orçamento ideal para um mês com meta de R$ 80 mil em vendas?**
>
> É só inverter a equação: x = (80 − 8,37) ÷ 3,93 ≈ **R$ 18,2 mil**.
>
> Ou seja: investindo cerca de R$ 18,2 mil em marketing, esperamos atingir a meta. Esse valor é só ~10% acima da média histórica — uma meta **factível**, não uma loucura.
>
> O multiplicador de retorno é de aproximadamente **4,4×**: cada R$ 1 investido retorna cerca de R$ 4,40 em vendas esperadas."

---

## 🎬 Slide 12 — Tomada de decisão II (cliques vs conversão)

> "A segunda pergunta de decisão era: **a ClickPlus deve focar em aumentar cliques ou em melhorar a taxa de conversão?**
>
> - **Aumentar cliques** (Estratégia A): cada 1 mil cliques a mais ≈ R$ 8,9 mil em vendas. Vantagem: efeito direto. Desvantagem: o custo por clique sobe quando se escala.
> - **Melhorar conversão** (Estratégia B): cada **+1 ponto percentual** de conversão ≈ R$ 15,3 mil em vendas. Vantagem: alavanca o tráfego que **já está sendo pago**.
>
> **Nossa recomendação é uma estratégia híbrida**: continuar a expansão de cliques (canal já dominado) e investir paralelamente em **CRO** — Conversion Rate Optimization, ou seja, melhorias no checkout, no frete, em prova social, na experiência do site. Cada ponto percentual ganho na conversão multiplica o resultado de toda a verba já gasta."

---

## 🎬 Slide 13 — Limitações

**(qualquer integrante — momento de honestidade científica)**

> "Nenhum modelo é perfeito. Por isso, é importante listar as limitações:
>
> 1. **Correlação ≠ Causalidade.** Mesmo com r = 0,99, não está provado que o investimento *causa* as vendas. Pode haver uma terceira variável (sazonalidade, por exemplo) puxando os dois.
> 2. **Tamanho da amostra:** apenas 12 meses. Pouco para conclusões muito firmes.
> 3. **Sazonalidade:** Black Friday e Natal podem inflar tanto o investimento quanto as vendas.
> 4. **Fatores externos:** concorrência, economia, lançamentos não estão no modelo.
> 5. **Linearidade assumida:** em valores muito altos de investimento, o retorno tende a achatar (saturação) — não é linear para sempre.
> 6. **Multicolinearidade:** as três variáveis preditoras estão muito correlacionadas entre si, o que dificulta uma regressão múltipla limpa.
>
> Para validar de verdade as recomendações, o ideal seria fazer **testes A/B controlados**."

---

## 🎬 Slide 14 — Conclusões

> "Resumindo o que aprendemos com a ClickPlus:
>
> 1. As três variáveis têm correlação **acima de 0,98** com as vendas — relação quase linear perfeita;
> 2. O modelo de regressão simples atinge **R² = 0,972** — explica 97% da variação;
> 3. O **ROI projetado** é de aproximadamente **3,9×** por real investido;
> 4. A meta de R$ 80 mil é **viável** com R$ 18,2 mil de marketing;
> 5. Otimizar a conversão tem **alto retorno** — cada ponto vale ~R$ 15 mil;
> 6. Antes de decisões estratégicas grandes, é preciso **mais dados** e **testes A/B** para confirmar causalidade."

---

## 🎬 Slide 15 — Encerramento

> "Foi assim que aplicamos correlação e regressão linear em um caso prático de e-commerce. A estatística descritiva, mesmo em sua forma mais simples, é uma ferramenta poderosa para transformar planilhas em **decisões fundamentadas**.
>
> Agradecemos a atenção! Estamos abertos a perguntas.
>
> **Equipe:** Arthur Fontinele, Matheus Veras, Pedro Fernando, Luis Mateus e Marco André.
>
> **Bibliografia consultada:**
> - BUSSAB & MORETTIN — *Estatística Básica*
> - DOWNING & CLARK — *Estatística Aplicada*
> - LEVINE et al. — *Estatística: Teoria e Aplicações*"

---

## 🧠 Dicas para a apresentação

- **Não decore** — entenda o raciocínio. Se travar, volte para o conceito: "correlação mede relação, regressão prevê valores".
- **Use o gráfico de dispersão** (slide 8) como apoio visual: ele convence muito.
- Se alguém perguntar **"por que cliques teve r maior que investimento?"** → responda que o efeito do investimento passa pelos cliques antes de virar venda; cliques estão "mais perto" do desfecho no funil.
- Se perguntarem **"o R² alto não é suspeito?"** → diga que sim, é um indicativo de overfitting potencial dado o n pequeno (12), mas que a relação é teoricamente esperada e plausível.
- **Tempo:** ~1 minuto por slide. Treine 2× para soltar.
