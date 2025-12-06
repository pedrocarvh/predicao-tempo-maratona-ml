# Predição de Tempo Final em Maratona: XGBoost e Engenharia de Features 🎯

## Objetivo
Prever o tempo oficial de conclusão de maratonistas utilizando **Machine Learning**, com base apenas nas informações dos primeiros 15 km da prova.

## Dados
- Dataset: **Maratonas de Boston (2015-2017)**  
- Contém informações de desempenho dos corredores nos primeiros segmentos da prova.

## Metodologia
- **Modelos Avaliados:**
  - Regressão Linear
  - Random Forest
  - XGBoost
- **Features Chave:**
  - Criação de **deltas de desempenho** para capturar a variação do ritmo (*pacing*) nos segmentos iniciais.

## Resultados Principais
O modelo **XGBoost** demonstrou o melhor desempenho, capturando padrões não-lineares sutis.

| Modelo             | MAE (s) | R²     |
|-------------------|---------|--------|
| XGBoost           | 538.80  | 0.8985 |
| Regressão Linear  | 550.29  | 0.8948 |
| Random Forest     | 562.49  | 0.8916 |

> O **MAE de 538,80s (~9 minutos)** é considerado adequado para aplicações práticas de **monitoramento e análise esportiva**.

## Conclusão e Viabilidade
- O **XGBoost** apresentou excelente desempenho, com baixo custo computacional.
- O modelo é **praticamente aplicável** para previsão de tempo final em corridas de longa distância.

## Como Executar o Projeto
O notebook foi desenvolvido no **Google Colab**. Para reproduzir os resultados:

### 1️⃣ Acessando a Base de Dados do Kaggle
Para baixar os dados automaticamente no Colab, é necessário ter acesso ao dataset da **Maratona de Boston (2015-2017)** no Kaggle.

**O que é necessário:**
- **Username do Kaggle**  
- **API Key (Token) do Kaggle)**

**Como obter a API Key:**
1. Acesse sua conta no [Kaggle](https://www.kaggle.com/).  
2. Clique na sua foto de perfil → **Account** → role até **API**.  
3. Clique em **Create New API Token**.  
4. Copie a **key/token** que aparece na tela.

> ⚠️ Observação: o Kaggle **não gera mais o arquivo `kaggle.json` automaticamente**. Por isso, no notebook do Colab já existe um trecho de código pronto para criar o `kaggle.json` usando suas credenciais. Basta colar o **username** e a **API Key** nos campos indicados.

### 2️⃣ Executando o Notebook
1. Abra o arquivo `notebooks/projeto-ml-2.ipynb` no Colab.  
2. Insira suas credenciais no bloco indicado para criar o `kaggle.json`.  
3. Execute as células do notebook na ordem.

> ⚠️ Cada usuário deve usar suas próprias credenciais. Não compartilhe sua API Key com terceiros.

## Autor
Pedro Carvalho Almeida
