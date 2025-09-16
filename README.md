🏡 House Price Prediction – King County (Seattle)

📌 Sobre o Projeto
Este projeto foi desenvolvido como parte de um laboratório de Data Analysis e Machine Learning.
O objetivo é analisar e prever preços de casas residenciais no condado de King, que inclui Seattle, utilizando atributos como metragem, número de quartos, banheiros, presença de vista para a água, ano de construção e outros.

📊 Dataset
O conjunto de dados contém informações sobre casas vendidas entre maio de 2014 e maio de 2015 no condado de King (Seattle).

Principais variáveis:
price: Preço da casa (variável alvo – target)
bedrooms: Número de quartos
bathrooms: Número de banheiros
sqft_living: Área em pés quadrados da casa
sqft_lot: Área total do terreno
floors: Número de andares
waterfront: Vista para a água (1 = sim, 0 = não)
view: Se a casa já foi vista
condition: Condição geral da casa
grade: Nota de qualidade (sistema de King County)
sqft_above: Área da casa acima do porão
sqft_basement: Área do porão
yr_built: Ano de construção
yr_renovated: Ano da última reforma
zipcode: Código postal
lat, long: Coordenadas geográficas
sqft_living15, sqft_lot15: Áreas medidas em 2015 (com possíveis reformas)

Fonte: House Sales Dataset (Kaggle/IBM)

🚀 Metodologia
1- Exploração dos Dados (EDA)
  - Estatísticas descritivas
  - Visualização de correlações
  - Distribuição dos preços

2- Pré-processamento
  - Tratamento de valores nulos (bedrooms, bathrooms)
  - Remoção de colunas irrelevantes (id, Unnamed: 0)

3- Modelagem
  - Regressão Linear Simples e Múltipla
  - Pipeline com PolynomialFeatures
  - Regressão Ridge (com e sem polinômio)

4 - Avaliação
  - Divisão em treino e teste (85% / 15%)
  - Métrica principal: R²

📈 Resultados Obtidos

- Linear Regression (1 variável)
long → R² ≈ 0.00047
sqft_living → R² ≈ 0.493

- Linear Regression (multivariada)
R² ≈ 0.658

- Pipeline (Scaler + Polynomial + Linear)
R² ≈ 0.751

- Ridge Regression (α=0.1)
Sem polinômio (teste): R² ≈ 0.648
Com polinômio de 2ª ordem (teste): R² ≈ 0.700

✅ Conclusões

Área útil (sqft_living, sqft_above), grade e banheiros são fortes preditores do preço.

Modelos polinomiais de 2ª ordem capturam melhor a relação entre variáveis e preço.

Ridge Regression melhora a generalização, reduzindo overfitting.
