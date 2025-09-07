# Análise da Epidemia de Dengue no Brasil (2014-2024)

## 📖 Visão Geral do Projeto

Este projeto realiza uma análise de dados exploratória completa sobre a epidemia de dengue no Brasil, utilizando dados públicos do DATASUS, IBGE e fontes climatológicas (ECMWF/ERA5) para o período de 2014 a 2024. O objetivo é investigar padrões, identificar os principais fatores de risco e entender a dinâmica por trás do maior surto da história, ocorrido em 2024.

---

## 🎯 Principais Questões Analisadas

1.  Qual é o padrão temporal e sazonal da dengue no Brasil?
2.  Quais são as áreas geográficas de maior impacto em volume vs. risco real?
3.  Qual o perfil demográfico mais vulnerável a casos graves (hospitalização)?
4.  Como a gravidade da doença (taxa de letalidade) evoluiu na última década?
5.  Quais fatores podem explicar o surto recorde de 2024?

---

## 🛠️ Metodologia e Ferramentas

* **Linguagem:** Python
* **Bibliotecas Principais:** Pandas (para manipulação de dados), Matplotlib e Seaborn (para visualização).
* **Fontes dos Dados:** DATASUS (SINAN), IBGE (Censo 2022) e ECMWF/ERA5.

O projeto foi estruturado seguindo as etapas do processo **KDD (Knowledge Discovery in Databases)**, com foco em transformar dados brutos em insights acionáveis:

1.  **Seleção e Coleta de Dados:** Definição e extração de dados das múltiplas fontes públicas citadas.
2.  **Pré-Processamento e Feature Engineering:** Limpeza, tratamento e aplicação da técnica de **"_Proportional Disaggregation_"** para unificar as tabelas e alcançar a granularidade `Município-Ano-Mês`.
3.  **Análise Exploratória de Dados (EDA) e Análise Estatística:** Aplicação de técnicas de visualização para identificar padrões e tendências, seguida pelo uso da Análise de Correlação de Pearson para quantificar a força das relações entre as variáveis.
4.  **Interpretação e Avaliação:** Contextualização dos achados estatísticos com pesquisas externas (Fiocruz, Instituto Butantan) para gerar conclusões.

---

## 📊 Principais Insights

* **Gatilho Climático:** Foi confirmada uma correlação sazonal entre o aumento da precipitação/temperatura e o pico de casos de dengue, com um atraso (lag) de 1 a 2 meses.
* **Risco vs. Volume:** A análise demonstrou que, enquanto o maior **volume** de hospitalizações ocorre em adultos, a **taxa de risco** de desenvolver um caso grave é maior em adolescentes (10-19 anos) e bebês (<1 ano).
* **Baixa Percepção de Risco:** A população ainda encara a dengue como uma doença com baixo potencial de risco, o que contraria os dados. A **taxa de letalidade** tem evoluído bastante nos últimos anos, e de de 2022 para 2024 houve um **aumento de aproximadamente 500%**, um número totalmente alarmante. 
* **Surto de 2024:** O surto recorde de 2024 foi contextualizado como um surto multifatorial, combinando anomalias climáticas (El Niño), falha nas medidas preventivas, aumento no volume pluviométrico, circulação simultânea dos 4 sorotipos do vírus, falta de vacina e conscientização.
* **Soluções Promissoras:** A análise contextualizou a importância das vacinas e de novas tecnologias, como o método Wolbachia, que demonstrou eficácia de 69% a 96% em estudos de campo.

---

## 🚀 Como Executar o Projeto

1.  Clone este repositório.
2.  Certifique-se de que os arquivos de dados brutos (da pasta `/dados`) estejam acessíveis para o notebook.
3.  Abra o arquivo `.ipynb` em um ambiente como Google Colab ou Jupyter Notebook.
4.  Execute as células em sequência.

## 🚀 Como Executar o Projeto

Este notebook foi desenvolvido no ambiente Google Colab. Para reproduzir a análise completamente, siga os passos abaixo:

1.  **Clone o Repositório:** Através do terminal ou prompt de comando, ou, faça o download do repositório (DONWLOAD ZIP).

2.  **Upload dos Arquivos:** Faça o upload do notebook (`.ipynb`) e da pasta de dados (`/dados`) para o seu ambiente de preferência (Google Colab ou Jupyter).

3.  **Configuração do Google Cloud (Obrigatório):**
    * A análise da **Taxa de Incidência por Município** requer uma consulta ao Google BigQuery para obter dados de população do Censo 2022. Para executar esta parte, é necessário:
        * Possuir uma conta Google Cloud.
        * Criar um projeto no Google Cloud Platform.
        * Ativar a API do BigQuery para este projeto.
        * No Google Colab, criar um "Secret" (no ícone de chave 🔑) com o nome `GCP_PROJECT_ID` e adicionar o ID do seu projeto como valor.

4.  **Execute as Células:** Com a configuração pronta, execute as células do notebook em sequência para reproduzir toda a análise.






