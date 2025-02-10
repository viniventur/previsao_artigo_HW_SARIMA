# Previsão de Receitas Estaduais - Análise dos Métodos de Suavização Exponencial e SARIMA

## Sobre o Projeto
Este repositório contém o código e a documentação relacionados ao artigo **"Previsão de Receitas Estaduais: análise dos métodos de suavização exponencial e SARIMA para projeção do ICMS e IPVA em Alagoas"**. O estudo tem como objetivo analisar a aplicação de modelos de suavização exponencial (SE) e SARIMA na previsão das receitas de ICMS e IPVA no estado de Alagoas, visando auxiliar no planejamento fiscal e orçamentário.

## Autores
- Vinícius de Oliveira Cunha Ventura - Supervisor de Acompanhamento e Projeção da Receita, Orçamento e de Parâmetros Econômicos Fiscais - SEPLAG/AL
- Cayo Luca Gomes Santana - Supervisor de Monitoramento das Ações Orçamentárias - SEPLAG/AL
- Caio Cesar de Melo - Assessor de Projetos - SEPLAG/AL
- Keuler Hissa Teixeira - Professor Associado - FEAC/UFAL

## Dados Utilizados
Os dados foram obtidos a partir do **Sistema Integrado da Administração Financeira de Alagoas (SIAFE/SEFAZ-AL)** e estão acessíveis pelo portal da transparência do estado. A amostra cobre o período de **janeiro de 2008 a dezembro de 2023**, totalizando **192 observações mensais**, com testes de robustez incluindo dados até junho de 2024.

## Metodologia
- **Separação dos Dados:**
  - Treinamento: Janeiro de 2008 a Agosto de 2022
  - Teste: Setembro de 2022 a Dezembro de 2023

- **Modelos Aplicados:**
  - Suavização Exponencial (Holt-Winters)
  - SARIMA (Box-Jenkins)

- **Critérios de Avaliação:**
  - Critério de Informação de Akaike (AIC)
  - Erro Percentual Absoluto Médio (MAPE)
  - Erro Médio Absoluto (MAE)
  - Raiz do Erro Quadrático Médio (RMSE)

## Resultados Principais
- **Modelos Otimizados:**
  - **ICMS:** Suavização Exponencial (Aditivo-Aditivo) e SARIMA(1,1,1)(1,0,0)12
  - **IPVA:** Suavização Exponencial (Multiplicativo-Multiplicativo) e SARIMA(1,0,1)(0,1,0)12
- O modelo SARIMA apresentou melhor desempenho para o ICMS, enquanto a suavização exponencial teve melhor performance no IPVA.
- O erro percentual dos modelos otimizados foi menor do que o previsto na LOA 2023, com um erro absoluto menor no IPVA.

## Estrutura do Repositório

- `SARIMA_artigo_hw_sarima_anpec.ipynb`: Previsão utilizando SARIMA
- `holt_winters_artigo_hw_sarima_anpec.ipynb`: Previsão utilizando suavização exponencial
- `template_holt_winters.ipynb`: Template para estimar com suavização exponencial de maneira otimizada
- `testes_robustez_SARIMA_artigo_hw_sarima_anpec.ipynb`: Testes de robustez estimações SARIMA
- `testes_robustez_holt_winters_artigo_hw_sarima_anpec.ipynb`: Testes de robustez estimações suavização exponencial

## Dependências

- google.colab
- pandas
- numpy
- statsmodels
- pmdarima
- arch
- seaborn
- matplotlib
