# 🚀 Projeto de Engenharia de Dados | Automação Web Scraping com Selenium

![Excel_transformacao_Web_Scraping](https://github.com/tiagodalmeida87/excel_webscraping_automacao/blob/main/assets/transf_planilha_add_informacao.jpg)

> *ALteração, alimentação e transformação de planilha em Excel desenvolvido no VsCode com Python, Pandas e Automação RPA. 

## 📌 Sobre o Projeto

Desenvolvimento de uma automação de coleta e atualização de dados utilizando **Python, Selenium e Pandas**, com foco em resolução de problemas de negócio através de técnicas de **Web Scraping** e automação de processos (RPA).

O projeto simula um desafio técnico de **Engenharia de Dados**, onde foi necessário consumir dados de uma planilha Excel, acessar um portal do Banco Central e atualizar automaticamente valores monetários corrigidos por índices econômicos.

---

# 🎯 Problema de Negócio

A empresa precisava automatizar o processo de atualização monetária de contratos utilizando índices econômicos como:

* IPCA
* IGPM

O processo era realizado manualmente através da Calculadora do Cidadão do Banco Central, tornando-se:

* Repetitivo
* Suscetível a erros
* Demorado
* Pouco escalável

A solução deveria:

✅ Ler dados de uma planilha Excel
✅ Consumir informações de um portal web
✅ Automatizar preenchimentos no navegador
✅ Capturar os valores corrigidos
✅ Atualizar automaticamente a planilha final

---

# 🛠️ Tecnologias Utilizadas

* Python
* Selenium
* Pandas
* OpenPyXL
* VS Code
* Jupyter Notebook

---

# ⚙️ Arquitetura da Solução

## 1️⃣ Leitura e Tratamento dos Dados

A automação inicia realizando a leitura da planilha `.xlsx` utilizando Pandas.

### Etapas realizadas:

* Leitura do arquivo Excel
* Conversão de tipos de dados
* Tratamento de datas
* Padronização dos valores monetários
* Estruturação do DataFrame

### Exemplo:

```python
df = pd.read_excel("dados.xlsx")

df["original_value"] = df["original_value"].astype(float)
```

---

## 2️⃣ Iteração dos Registros

Foi utilizada iteração linha a linha do DataFrame para alimentar dinamicamente o processo de automação web.

### Objetivo:

* Capturar:

  * índice econômico
  * data inicial
  * valor original
* Preparar os dados para envio ao portal web

---

## 3️⃣ Automação Web com Selenium

A solução utiliza Selenium para controlar o navegador Chrome e interagir automaticamente com o site da Calculadora do Cidadão.

### Funcionalidades implementadas:

✅ Abertura automática do navegador
✅ Navegação até o portal
✅ Identificação de elementos HTML
✅ Preenchimento automático dos campos
✅ Clique automatizado nos botões
✅ Extração do valor corrigido

### Técnicas utilizadas:

* `find_element`
* `By.ID`
* `By.NAME`
* `By.CLASS_NAME`
* `send_keys`
* `click`
* `clear`

---

# 🔍 Estratégia de Web Scraping

Durante o projeto foi realizada inspeção dos elementos HTML para localizar corretamente os campos necessários da aplicação web.

Exemplo:

```python
campo_indice = driver.find_element(By.ID, "indice")
```

---

# 📊 Tratamento dos Dados

Após a captura dos valores corrigidos:

* Os dados foram convertidos para formato numérico
* Foi calculada a diferença entre:

  * valor original
  * valor atualizado
* Os resultados foram armazenados em memória

---

# 📁 Atualização da Planilha

Ao final da automação:

✅ A planilha foi atualizada automaticamente
✅ Os novos valores corrigidos foram inseridos
✅ O cálculo de diferença foi realizado automaticamente

---

# 🧠 Principais Desafios Técnicos

## 🔹 Manipulação dinâmica de elementos web

Necessidade de identificar corretamente os elementos HTML utilizando diferentes estratégias de localização.

---

## 🔹 Tratamento de datas

O portal exigia um formato específico (`MMYYYY`), exigindo transformação dos dados antes do envio.

---

## 🔹 Automação resiliente

Implementação de limpeza de campos (`clear`) antes do preenchimento para evitar inconsistências.

---

## 🔹 Conversão de tipos

Tratamento de valores monetários para evitar erros durante cálculos e preenchimentos automáticos.

---

# 📈 Resultados Obtidos

✅ Automação completa do fluxo manual
✅ Redução significativa de tempo operacional
✅ Padronização do processo
✅ Redução de erros humanos
✅ Maior escalabilidade do processo

---

# 💡 Competências Demonstradas

## Engenharia de Dados

* Manipulação de dados
* Tratamento de dados
* ETL
* Automação de processos
* Estruturação de pipelines

## Automação

* Selenium
* Web Scraping
* RPA
* Navegação automatizada

## Programação

* Python
* Estruturas de repetição
* Tratamento de exceções
* Manipulação de DataFrames

---

# 📚 Aprendizados

Este projeto reforçou habilidades importantes para atuação em Engenharia de Dados:

* Resolução de problemas
* Estruturação de automações
* Integração entre dados e aplicações web
* Organização lógica de pipelines
* Estratégias de Live Coding

---

# 🔗 Possíveis Melhorias Futuras

* Modularização do código
* Tratamento avançado de exceções
* Implementação de logs
* Dockerização da aplicação
* Agendamento automatizado
* Integração com banco de dados
* Criação de pipeline orquestrado

---

# 📌 Conclusão

Este projeto demonstra na prática a aplicação de conceitos de Engenharia de Dados e automação para resolução de problemas reais de negócio.

A solução integra coleta, transformação e atualização de dados de forma automatizada, evidenciando conhecimentos em:

* Python
* Selenium
* Pandas
* Web Scraping
* ETL
* Automação de Processos

Além da capacidade de análise técnica, resolução de problemas e construção de soluções escaláveis.

---

# 👨‍💻 Autor

[Tiago Almeida](https://github.com/tiagodalmeida87)

Desenvolvido como **projeto de portfólio de Análise de Dados e Business Intelligence**.

📧 Entre em contato via [LinkedIn](https://www.linkedin.com/in/tiago-l-almeida)

---

# 📜 Licença

Este projeto é de uso livre para fins educacionais e de portfólio.  
