# 🌳 Árvore de Decisão - Do Treinamento ao Deploy

Este projeto apresenta um pipeline completo de Machine Learning utilizando o algoritmo de **Árvore de Decisão**, com foco em boas práticas de organização, rastreamento de experimentos e deploy em produção.


## 📌 Descrição

O objetivo do projeto é demonstrar o fluxo de desenvolvimento de um modelo de ML do início ao fim, incluindo:

- Pré-processamento dos dados
- Treinamento e validação de modelo com **Scikit-learn**
- Rastreamento de experimentos com **Weights & Biases (wandb)**
- Criação de uma **API com FastAPI** para servir o modelo
- Deploy da aplicação com **Heroku**

## 🧰 Tecnologias Utilizadas

- Python 3.10+
- Scikit-learn
- Pandas
- FastAPI
- Uvicorn
- wandb
- Heroku
- Git

## 🧪 Pipeline com Weights & Biases

O projeto utiliza `wandb` para:

- Rastrear métricas de validação (ex: acurácia, matriz de confusão)
- Comparar diferentes configurações de hiperparâmetros
- Armazenar versões de modelos treinados

Para usar, configure sua conta do wandb com:

```bash
wandb login
```

E execute o treinamento com:

```bash
python train.py
```

## 🚀 API com FastAPI

A API é responsável por receber os dados de entrada e retornar a predição do modelo treinado.

Para rodar localmente:

```bash
uvicorn app.main:app --reload
```

Endpoints disponíveis:

- `GET /` → Rota de teste
- `POST /predict` → Enviar os dados de entrada (JSON) e obter a predição



## ☁️ Deploy com Heroku

O projeto está pronto para deploy no Heroku. Após configurar os arquivos `requirements.txt`, `Procfile` e `setup.sh`, o deploy pode ser feito com:

```bash
heroku create nome-do-app
git push heroku main
```

## 📊 Resultados

O modelo obteve uma acurácia de **XX%** no conjunto de validação (substituir com valor real).  
Outras métricas podem ser visualizadas diretamente no painel do wandb.

## 👨‍💻 Autor

**André Vinícius da Silva Brandão**  
[LinkedIn](https://www.linkedin.com/in/andrebrandaopro) | [GitHub](https://github.com/andrebrandaopro)  
