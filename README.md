# Carteira-de-investimentos
Carteira ótima de investimentos
#### Aluno: Maria Elisa Guerisoli Puertas
#### Orientador: [Felipe Borges](https://github.com/FelipeBorgesC) 

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".


### Resumo

Uma carteira de investimentos é um grupo de ativos que pertence a um investidor, pessoa física ou pessoa jurídica. Estes ativos podem ser ações, fundos, títulos públicos, debêntures, aplicações imobiliárias, entre outros.
Uma boa carteira é a que satisfaz as expectativas de rentabilidade e de prazo do investidor, ponderadas pela sua tolerância ao risco. 
Vamos montar uma carteira de investimentos ótima, composta por fundos de renda fixa, ações e multimercados.


### 1. Introdução

**Problema :** Um investidor quer alocar recursos em fundos de investimentos de maneira que consiga a melhor rentabilidade com menor risco.

Para isto, selecionamos uma carteira ótima, a partir de dados disponíveis no mercado.
Partimos de uma seleção de 97 fundos de ações, Renda fixa e multimercado.

Serão apresentados 3 cenários: 2 automáticos, variando o valor máximo a ser investido em cada fundo, e 1 manual. 
A diversificação é importante para equilibrar eventuais perdas.

### 2. Modelagem

**Carteira ótima sugerida:**
Dado o valor a ser investido, será sugerida uma carteira balanceada, a partir da seleção de até 10 fundos de investimentos, entre fundos de ações, multimercado e renda fixa. 

**Variáveis:**
Informar o valor a ser investido

**Condições para seleção da amostra de fundos:**
Fundos sem taxa de performance
Investimento mínimo <= 5000
Cotização <= d+4

**Objetivo**
Máxima rentabilidade com menor volatilidade - O índice sharp foi utilizado

**Função objetivo:**
Max (Indice Sharp ponderado)

**Restrições**
Total de fundos alocados <= 10
Fração de alocação em cada fundo >= 0

**Cenário1 :** Fração de alocação em cada fundo <= 0,2

**Cenário2 :** Fração de alocação em cada fundo <= 0,3

**Cenário3 :** Escolha manual

**Valor alocado :** 100.000

**Excel  | Solver**

**Solving Method : GRC Nonlinear**

O Cálculo foi feito com valores de 2023.

### 3. Resultados

**Cenários :**

**Cenário 1 :** Ponderação de no máximo **20%** de investimento em um mesmo fundo. A solução apresentou alguns fundos com valores muito baixos e foi aplicado um filtro para que fossem considerados apenas investimentos > 100. Para valores de investimento total mais altos, esses fundos serão automaticamente considerados.

**Cenário 2:** Ponderação de no máximo **30%** de investimento em um mesmo fundo. A solução apresentou alguns fundos com valores muito baixos, foi aplicado um filtro para que fossem considerados apenas investimentos > 100. Para valores de investimento total mais altos, esses fundos serão automaticamente considerados.

**Cenário 3:** Seleção manual de fundos – Selecionei, usando filtro, os 10 fundos com maior índice sharp e estabeleci um investimento de 10% em cada fundo

**Análises :**
•	Comparação entre os 3 cenários acima
•	Comparação com o CDI (benchmark) 

**Cenário 1:** Carteira automática 0.2
Carteira com investimentos em 7 fundos, 6 de RF e 1 Multimercado. O Indice Sharp da carteira ponderado ficou em 9,20. 
Este cenário apresentou uma boa diversificação, concentração em renda fixa e mais de 50% da carteira com liquidação D0

**Cenário 2:**  Carteira automática 0.3
Carteira com investimentos em 7 fundos, mesmos do cenário anterior, com ponderação diferente. O Indice Sharp da carteira ponderado ficou em 11,85. 
Este cenário apresentou uma boa diversificação, concentração em renda fixa e mais de 50% da carteira com liquidação D0

**Cenário 3:** Carteira manual
Carteira com investimentos em 10 fundos, 10% em cada. O Indice Sharp da carteira ponderado ficou em 5,75. 

Comparação com benchmark (CDI) :

CDI - 11,79% X Rentab : 13,99

Gráficos e compartivos estão disponíveis no arquivo "BIMaster_carteira de investimentos.pdf"

### 4. Conclusões

O cálculo da carteira ótima foi realizado com base nos valores do índice sharp de 2023 para os fundos da amostra.
As rentabilidades passadas foram apenas carregadas da base original para comparação.
Podemos observar que a rentabilidade da carteira ótima foi similar à da carteira manual.
Isto se deu, pois os valores de rentabilidade dos fundos escolhidos é muito próximo e, por isso, o fator de ponderação entre as carteiras dos cenários não fez muito diferença.
**No entanto, podemos ver que a carteira do cenário 2 tem um índice sharp bem maior (11,85), representando a solução ótima em relação à rentabilidade X volatilidade, que era o que buscávamos.**
Usamos como benchmark o CDI e em 2023 a carteira supera o CDI.
**Carteira ótima: cenário 2**

	
---

Matrícula: 212.100.380

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
