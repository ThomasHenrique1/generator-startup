## Startup Idea Generator
Este projeto é uma aplicação web simples que utiliza APIs para gerar ideias inovadoras para startups com base em um tema fornecido pelo usuário. A aplicação oferece duas formas de gerar respostas: usando a API do OpenAI ou a RapidAPI (um serviço de API para o ChatGPT). O frontend está implementado em Flask, e o backend faz chamadas às APIs para gerar a ideia de startup.

## Funcionalidades

- Gera ideias de startups com base em temas fornecidos.
- Utiliza duas formas de consulta: API do OpenAI e RapidAPI.
- Exibe o resultado formatado com negrito e subtítulos.
- Backend em Flask.
- Frontend simples com HTML, CSS e JavaScript.

## Estrutura do Projeto

`app.py`                 # Arquivo principal usando API do OpenAI
`app_rapidapi.py`         # Arquivo secundário usando API da RapidAPI

+ `static/`               # Pasta para arquivos estáticos (CSS e JS)
    + `style/ `           # Pasta para arquivos CSS
        - `style.css`     # Arquivo CSS personalizado
    + `js/`               # Pasta para arquivos JavaScript
        - `index.js`      # Código JavaScript para requisições AJAX

+ `templates/`            # Pasta para templates HTML
    - `index.html`        # Frontend HTML principal

- `README.md`             # Documentação do projeto
- `requirements.txt`      # Lista de dependências do projeto


## Vídeo Explicativo

[![Assista ao vídeo explicativo](https://img.youtube.com/vi/3aT5NSTXhmQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=3aT5NSTXhmQ)


## Requisitos

- Python 3.x
- Flask
- Requests
- Conta na OpenAI (para usar a API do GPT)
- Conta no RapidAPI (para usar a API ChatGPT via RapidAPI)

## Instalação

> Clone o repositório:

```bash 
git clone https://github.com/seu-usuario/startup-idea-generator.git
cd startup-idea-generator
```

> Crie um ambiente virtual e ative-o:

```bash
python -m venv venv
source venv/bin/activate  # No Windows use: venv\Scripts\activate
```
> Instale as dependências:

```bash
pip install -r requirements.txt
```
> Crie um arquivo .env (opcional para manter sua chave da API segura) ou defina diretamente no código sua chave da API.

- No caso da OpenAI, insira sua chave no código onde estiver escrito `YOUR_OPENAI_API_KEY`.

- No caso da RapidAPI, insira a chave no código onde estiver `YOUR_RAPIDAPI_KEY`.

## Estrutura dos Arquivos

### `app.py` (Usando OpenAI API)
- Este arquivo contém a lógica para a geração de ideias de startup através da API do OpenAI. A função `test_openai_api` realiza a chamada para a API do `gpt-3.5-turbo` e retorna uma resposta formatada.

### `app_rapidapi.py` (Usando RapidAPI)
- Similar ao `app.py`, mas este arquivo faz as chamadas à API do ChatGPT através do serviço da RapidAPI. A função `test_rapidapi` lida com a requisição para a API da RapidAPI.

### `index.html`
- A interface simples onde o usuário pode inserir um tema de startup e receber a ideia gerada pela API.

### `index.js`
- Código JavaScript que lida com as requisições AJAX, enviando o tema para o backend e recebendo a resposta da API.

### `style.css`
- Arquivo de estilos CSS para o layout e design da página.

## Considerações

- O uso da API do `OpenAI` está sujeito a limites de requisição e possíveis custos dependendo do seu plano.
- A `RapidAPI` também possui limites de uso gratuito, e você pode precisar verificar a documentação deles para entender os custos adicionais.
    + Para a RapidAPI sera deixado dois links de API's gratuitas para caso tenha interesse em testar, o nome do arquivo contendo so links se chama `sites.txt`, é necessario ter conta na RapidAPI.
- Você pode alternar entre as duas formas de requisição rodando os arquivos corretos (`app.py` ou `app_rapidapi.py`).


## Contato

Se você tiver dúvidas ou sugestões, entre em contato com [Thomas Henrique](mailto:thomasnhenrique@gmail.com).
