# am-at2-redes-neurais

# iFood Campaign Intelligence

Projeto de Machine Learning desenvolvido para analisar dados de campanhas de marketing e prever a resposta de clientes a novas campanhas.

A proposta é utilizar informações demográficas, hábitos de consumo e histórico de interação com campanhas para treinar uma rede neural capaz de estimar a probabilidade de um cliente responder positivamente.

## Objetivo

Desenvolver um modelo de classificação binária utilizando uma rede neural MLP (*Multilayer Perceptron*).

O projeto também contempla a preparação dos dados, análise exploratória, avaliação do modelo e disponibilização das previsões por meio de uma API REST com FastAPI.

## Dataset

O projeto utiliza o dataset [iFood Marketing Campaigns](https://www.kaggle.com/datasets/fayez7/ifood-marketing-campaigns), disponibilizado no Kaggle.

Os dados contêm informações sobre clientes, características demográficas, gastos, canais de compra e respostas a campanhas anteriores.

A variável `Response` será utilizada como alvo da classificação:

- `0`: cliente não respondeu positivamente à campanha.
- `1`: cliente respondeu positivamente à campanha.

Por se tratar de uma base histórica, os resultados representam os padrões encontrados nesse conjunto de dados e não necessariamente o comportamento atual dos clientes do iFood.

## Tecnologias

- Python
- Pandas e NumPy
- Matplotlib e Seaborn
- Scikit-learn
- Jupyter Notebook
- Joblib
- FastAPI
- Pydantic
- UV

## Estrutura do projeto

```text
am-at2-redes-neurais/
│
├── data/
│   └── dataset.csv
│
├── models/
│   └── pipeline_rede_neural.joblib
│
├── notebooks/
│   └── analise_treinamento.ipynb
│
├── src/
│   ├── __init__.py
│   ├── app.py
│   └── schemas.py
│
├── .gitignore
├── pyproject.toml
├── uv.lock
├── requisicoes.http
└── README.md
```

## Configuração do ambiente

O projeto utiliza o [UV](https://docs.astral.sh/uv/) para gerenciamento de dependências e do ambiente Python.

Após clonar o repositório, execute:

```bash
uv sync
```

Esse comando instala as dependências definidas no projeto.

## Executando o notebook

Para iniciar o Jupyter Lab:

```bash
uv run jupyter lab
```

Abra o arquivo `notebooks/analise_treinamento.ipynb` para acompanhar a análise dos dados e o treinamento do modelo.

## Executando a API

Após a implementação da API, ela poderá ser iniciada com:

```bash
uv run fastapi dev src/app.py
```

A documentação interativa estará disponível em:

```text
http://127.0.0.1:8000/docs
```

## Etapas do desenvolvimento

- [x] Seleção e preparação inicial do dataset
- [x] Configuração do ambiente e estrutura do projeto
- [ ] Análise exploratória dos dados
- [ ] Pré-processamento e preparação das variáveis
- [ ] Treinamento da rede neural MLP
- [ ] Avaliação dos resultados
- [ ] Exportação do pipeline treinado
- [ ] Desenvolvimento da API com FastAPI
- [ ] Testes dos endpoints
- [ ] Documentação e demonstração do projeto

---

Desenvolvido como parte da atividade de Machine Learning da FATEC — Desenvolvimento de Software Multiplataforma.
