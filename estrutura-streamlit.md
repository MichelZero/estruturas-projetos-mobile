# Estrutura de Projeto Streamlit

Este documento descreve uma estrutura recomendada para projetos Streamlit, facilitando a organização e manutenção do seu código para dashboards e aplicativos web interativos.

## Estrutura Básica de Pastas
```plaintext
nome_do_projeto_streamlit/
├── app.py # Arquivo principal do Streamlit
├── pages/ # Para múltiplas páginas (opcional)
│ ├── page1.py
│ ├── page2.py
│ └── ...
├── data/ # Dados utilizados pelo aplicativo
│ ├── raw_data.csv # Dados brutos (opcional)
│ ├── processed_data.csv # Dados processados (opcional)
│ └── ...
├── utils/ # Funções utilitárias
│ ├── data_processing.py # Funções de processamento de dados
│ ├── visualization.py # Funções de visualização
│ └── ...
├── assets/ # Imagens, ícones, etc. (opcional)
│ └── ...
├── requirements.txt # Dependências do projeto
├── README.md # Este arquivo
└── .gitignore # Arquivos a serem ignorados pelo Git


```

## Descrição das Pastas e Arquivos

* **`app.py`:** O arquivo principal do seu aplicativo Streamlit.  Contém o código que define a interface do usuário e a lógica do aplicativo.

* **`pages/` (opcional):** Se o seu aplicativo tiver várias páginas, crie uma pasta `pages` e coloque cada página em um arquivo Python separado dentro dela.  O Streamlit reconhecerá automaticamente esses arquivos como páginas e as adicionará à barra de navegação.

* **`data/` (opcional):**  Armazene os dados usados pelo seu aplicativo nesta pasta. Separe os dados brutos dos dados processados para melhor organização.

* **`utils/` (opcional):**  Crie funções utilitárias e as organize em arquivos separados dentro da pasta `utils`.  Isso ajuda a manter o código `app.py` mais limpo e facilita a reutilização de código.

* **`assets/` (opcional):** Armazene imagens, ícones e outros recursos estáticos nesta pasta.

* **`requirements.txt`:** Liste as dependências do seu projeto neste arquivo.  Isso permite que outras pessoas instalem facilmente as bibliotecas necessárias usando `pip install -r requirements.txt`.

* **`README.md`:** Este arquivo, contendo informações sobre o projeto.

* **`.gitignore`:**  Especifique os arquivos e pastas a serem ignorados pelo Git (por exemplo, dados brutos grandes, arquivos temporários, etc.).


## Executando o Aplicativo

1. **Navegue até o diretório do projeto:** `cd nome_do_projeto_streamlit`
2. **Instale as dependências:** `pip install -r requirements.txt`
3. **Execute o aplicativo Streamlit:** `streamlit run app.py`



## Exemplo de `app.py`

```python
import streamlit as st
import pandas as pd
from utils.data_processing import load_data, process_data  # Importe funções de utils/

# Carregar e processar dados
data = load_data("data/raw_data.csv")
processed_data = process_data(data)


# Título do aplicativo
st.title("Meu Aplicativo Streamlit")

# Exibir um DataFrame
st.write(processed_data)

# Criar um gráfico
st.bar_chart(processed_data['coluna'])

# ... resto do seu código Streamlit ...
```
## Dicas Adicionais

Modularize o código: Divida a lógica em funções e módulos para facilitar a manutenção e reutilização.

Use a pasta pages para múltiplas páginas: Isso melhora a organização e a navegação em aplicativos maiores.

Documente seu código: Adicione comentários e docstrings para explicar o que o código faz.

Use um ambiente virtual: Isso ajuda a isolar as dependências do seu projeto. (recomendado: python3 -m venv .venv e source .venv/bin/activate)


