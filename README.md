# 📈 Análise de Cointegração e Modelo de Correção de Erros (VECM)

Este repositório apresenta um framework completo de **Econometria de Séries Temporais** aplicado à macroeconomia brasileira. O objetivo é investigar a relação de equilíbrio de longo prazo entre atividade econômica, inflação, preços de combustíveis e política monetária.

## 📝 Visão Geral do Projeto

A análise de cointegração é fundamental para evitar a **regressão espúria**, garantindo que as relações encontradas entre as variáveis não sejam apenas fruto de tendências temporais comuns, mas sim de uma conexão econômica real.

### 🎯 Problema Econômico
O estudo busca responder: **Como variações no preço da gasolina e na taxa de juros impactam o produto interno bruto (PIB) e a inflação no longo prazo?** As variáveis utilizadas no modelo são:
* **Atividade Econômica:** PIB (ou IBC-Br)
* **Inflação:** IPCA
* **Preço da Gasolina:** Preço médio ao consumidor
* **Taxa de Juros:** SELIC

---

## 🛠️ Metodologia e Workflow

O projeto segue um rigoroso fluxo de validação estatística:

1.  **Fundamentação Teórica:** Justificativa da necessidade de cointegração para séries não estacionárias.
2.  **Testes de Raiz Unitária:** Verificação da ordem de integração das séries através de três abordagens:
    * **ADF (Augmented Dickey-Fuller):** Teste de raiz unitária com correção para autocorrelação.
    * **Phillips-Perron (PP):** Teste robusto a formas genéricas de heterocedasticidade.
    * **KPSS:** Teste de hipótese nula de estacionariedade (ferramenta de confirmação).
3.  **Teste de Cointegração de Johansen:** Identificação do número de vetores de cointegração (Rank do sistema).
4.  **Modelo de Correção de Erros (VECM):** Caso a cointegração seja confirmada, o modelo estima:
    * **Relação de Longo Prazo:** O equilíbrio estável entre as variáveis.
    * **Dinâmica de Curto Prazo:** Como o sistema reage a choques imediatos.
    * **Velocidade de Ajuste ($\alpha$):** O tempo necessário para retornar ao equilíbrio após um desvio.

---

## 📋 Requisitos para o Modelo

Para a aplicação do **VECM**, este projeto valida as seguintes premissas:
* As séries devem ser **não estacionárias** em nível.
* Todas as variáveis devem ser integradas de mesma ordem, usualmente $I(1)$.
* Deve haver, no mínimo, uma relação de cointegração identificada pelo teste de Johansen.

---

## 🚀 Tecnologias Utilizadas

* **Python** (Pandas, NumPy, Matplotlib)
* **Statsmodels** (Módulos de séries temporais e modelos lineares)
* **LaTeX** (Para documentação de fórmulas econométricas)

---

## 📂 Como Utilizar

1. Clone o repositório:
   ```bash
   git clone [https://github.com/seu-usuario/nome-do-projeto.git](https://github.com/seu-usuario/nome-do-projeto.git)
