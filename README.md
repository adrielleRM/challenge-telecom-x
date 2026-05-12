# challenge-telecom-x

Projeto Telecom X: Análise de Churn em Telecomunicações
Este projeto faz parte da formação de Ciência de Dados da Alura + Oracle (Next Education). O objetivo principal é realizar o tratamento e a análise exploratória de dados de uma empresa de telecomunicações para identificar padrões que levam ao cancelamento de clientes (Churn).

📌 Contexto
O cancelamento de clientes é um dos maiores desafios em empresas de serviços. Identificar quais perfis de clientes possuem maior probabilidade de sair permite que a empresa tome ações proativas de retenção.

🛠️ Tecnologias Utilizadas
Python: Linguagem principal.

Pandas: Manipulação, limpeza e transformação de dados.

JSON: Formato original da extração de dados.

Matplotlib: Visualização de dados e gráficos.

Google Colab: Ambiente de desenvolvimento.

🗂️ Etapas do Projeto
1. Extração e Carregamento
Os dados brutos foram extraídos de um arquivo JSON hospedado no Google Drive. A estrutura inicial continha colunas aninhadas (dicionários dentro de células), exigindo um processo de normalização.

2. Transformação e Limpeza
Normalização: Utilizei pd.json_normalize para achatar a estrutura JSON e transformar colunas complexas em um DataFrame tabular.

Tratamento de Dados Nulos: Identifiquei e tratei valores nulos na coluna account_charges_total, substituindo-os por 0 (casos onde o tempo de permanência era zero).

Conversão de Tipos: Colunas numéricas que estavam como texto foram convertidas para float64.

Filtragem: Removi registros onde a variável alvo churn estava vazia, pois não permitiam uma análise conclusiva.

3. Análise Exploratória (EDA)
Realizei uma análise estatística e visual para entender o perfil da base de clientes:

Distribuição de Churn: A base apresenta aproximadamente 26,5% de taxa de cancelamento.

Perfil de Faturamento: A média de cobrança mensal é de 64,76 e o tempo médio de permanência é de 32 meses.

📊 Visualizações
Foram gerados gráficos de barras para visualizar a proporção entre clientes que permaneceram e clientes que cancelaram o serviço, facilitando a compreensão da taxa de evasão.

🚀 Conclusões Iniciais e Próximos Passos
A análise indica que o Churn está fortemente ligado ao tipo de contrato, forma de pagamento e tempo de permanência.
As recomendações incluem:

Incentivar a migração para contratos anuais.

Investigar falhas na experiência de pagamento via "Electronic Check".

Desenvolver modelos preditivos para identificar riscos de cancelamento antecipadamente.

https://colab.research.google.com/drive/1LSD4uf15D-emQTOQfFUs_mOJbLmwk4l-?usp=sharing
