# Steam Game Recommender

## Visão Geral
Este repositório contém um sistema de recomendação de jogos da Steam, desenvolvido utilizando Python e FastAPI. O objetivo é fornecer sugestões de jogos com base na similaridade, melhorando a experiência do usuário ao explorar novos títulos.

O sistema utiliza um modelo treinado para prever quais jogos podem ser do interesse do usuário, baseado em um conjunto de dados extraído da Steam.

**Nota:** O deploy deste projeto **não está disponível na nuvem**. Apenas os arquivos necessários estão disponíveis no repositório do GitHub para que os usuários possam rodá-lo localmente.

## Tecnologias Utilizadas
- **Linguagem**: Python
- **Framework Web**: FastAPI
- **Bibliotecas para Análise de Dados**: Pandas
- **Armazenamento de Modelo**: Pickle
- **Servidor ASGI**: Uvicorn
- **Ambiente Virtual**: Conda

## Estrutura do Repositório
```
/
├── recommender.ipynb   # Notebook com a criação do sistema de recomendação
├── main.py             # Aplicativo FastAPI para recomendação de jogos
├── models/
│   ├── recommender.pkl # Modelo treinado salvo
├── requirements.txt    # Dependências do projeto
├── README.md           # Documentação do projeto
```

## Instalação e Configuração

### Criar e ativar o ambiente virtual Conda:
```sh
conda create --name recomendation python=3.11.11
conda activate recomendation
```

### Instalar as dependências:
```sh
pip install -r requirements.txt
```

### Dependências do Projeto
O ambiente foi configurado com as seguintes bibliotecas listadas no `requirements.txt`:
```
pandas==2.2.3
seaborn==0.13.2
matplotlib==3.10
scipy==1.15.1
ipykernel==6.29.5
scikit-learn==1.6.1
streamlit==1.28.0
```

## Como Executar o Projeto
Para iniciar o servidor FastAPI, execute:
```sh
python main.py
```
A API estará acessível em: `http://127.0.0.1:8000`

## Endpoints Disponíveis

### 📌 Página Inicial
**GET /**  
Retorna uma mensagem de boas-vindas ao usuário.

### 🎮 Listar Jogos
**GET /list_games**  
Retorna uma lista com todos os jogos disponíveis no banco de dados.

### 🔍 Buscar Jogos
**GET /search_games?pattern=<substring>**  
Realiza uma busca por jogos cujo nome contenha a substring fornecida.

### ⭐ Recomendar Jogos
**GET /recommend?game=<nome_do_jogo>&max_recommendations=<número>**  
Retorna uma lista de jogos recomendados com base no título informado.

## Testando a API
Uma forma simples de testar os endpoints é utilizando o **Swagger UI**, disponível automaticamente ao rodar o projeto, acessando:
```
http://127.0.0.1:8000/docs
```
Outra opção é o **Redoc**, acessível em:
```
http://127.0.0.1:8000/redoc
```

## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir **issues** e **pull requests** para sugerir melhorias ou correções.

## Licença
Este projeto está sob a licença **MIT**, permitindo seu uso, modificação e distribuição.

---
🚀 Desenvolvido com paixão pela comunidade open-source!

