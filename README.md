<p align="center">
  <a href="" rel="noopener">
</p>

<h3 align="center">Crypto Ranking API</h3>

<div align="center">

![Status](https://img.shields.io/badge/status-active-success.svg)

</div>

---

<p align="center">API para listar criptomoedas previamente salvas em um banco de dados com um sistema simples de "ranking de popularidade" através de votos.
    <br> 
</p>

#### 📝 Índice

- [Pré-requisitos](#pre)
- [Execução](#execucao)
- [Recursos da API](#recursos)
- [Stack(tecnologias)](Stack)

#### 🏁 Intro <a name = "intro"></a>
Estas instruções fornecerão uma cópia do projeto em funcionamento em sua máquina local para fins de desenvolvimento e testes.

#### Pré-requisitos: <a name = "pre"></a>

Para fazer uma cópia do projeto em sua máquina local para fins de desenvolvimento e teste, você precisará seguir alguns passos.

1. Certifique-se de ter o Python instalado em sua máquina.  
  - python.org

2. Clone o repositório do projeto para a sua máquina usando o Git. Abra o terminal e execute o seguinte comando:

```
git clone https://github.com/thomasdev5832/api-ranking
```
3. Acesse o diretório do projeto:
```
cd api-ranking
```
##### Configuração do Ambiente Virtual (Opcional, mas recomendado):
1. Crie um ambiente virtual para isolar as dependências do projeto. No diretório do projeto, execute:
```
python -m venv venv
```
2. Ative o ambiente virtual:
- No Windows:
```
.\venv\Scripts\activate
```
- No MacOS/Linux
```
source venv/bin/activate
```
##### Instalação de Dependências: 
1. Instale as dependências (requirements.txt) do projeto usando o `pip`:
```
pip install -r requirements.txt
```

##### Configuração do Banco de Dados:
1. Certifique-se de ter o SQLite instalado
- [SQLite Download](https://www.sqlite.org/download.html)
2. Como o banco de dados é SQLite, quando o projeto for executado, o arquivo de banco de dados 'database.db' será criado na raiz do projeto.

#### Execução <a name = "execucao"></a>

1. Execute o aplicativo Flask:
- No Windows:
```
python app.py
```
- No Mac/Linux:
```
python3 app.py
```
2. O aplicativo estará disponível em http://127.0.0.1:5000/
 Acesse esta URL em um navegador para testar a API localmente.

##### Teste da API:
1. Use ferramentas como [Postman](https://www.postman.com/), [Insomnia](https://insomnia.rest/) ou o próprio navegador para enviar requisições à API e verificar se está funcionando corretamente.

---

#### 🚀 Recursos da API <a name="recursos"></a>

**Content-Type**
O retorno de dados da API será via `JSON`.
`Content-Type: application/json.`


##### - Listar Criptomoedas [GET /api/criptos/]

+ Response 200 (application/json)
  + Atributos
    - id: 1 (number) - ID da criptomoeda
    - nome: Bitcoin (string) - Nome da criptomoeda
    - votos: 111 (number) - Número de votos da criptomoeda


##### - Adicionar Voto [POST /api/criptos/votar/{id}]

+ Parameters
  + id: 1 (number, path) - ID da criptomoeda que receberá o voto

+ Response 200 (application/json)
  + Atributos
    - votos: 112 (number) - Número de votos atualizado

+ Response 404 (application/json)
  + Atributos
    - error: ID não encontrado (string) - Mensagem de erro quando o ID não é encontrado


#### ⛏️ Stack <a name = "stack"></a>

- [SQLite](https://www.sqlite.org/index.html) - Database
- [Python](https://www.python.org/) - Programming Language
- [Flask](https://flask.palletsprojects.com/) - Web Framework
- [Heroku](https://www.heroku.com/) - Cloud Service Platform

---

✍️ [Gabriel Thome](https://github.com/thomasdev5832/) 
📝[MIT License](https://opensource.org/license/mit/) 

