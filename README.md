# Automação Consultar Vagas no LinkedIn

Este projeto tem como objetivo realizar uma consulta automatizada de vagas de emprego no LinkedIn utilizando **Python** e as bibliotecas `requests`, `BeautifulSoup` e `pandas`.

## Funcionalidades

- Permite ao usuário informar:
  - Nome da vaga
  - Cidade
  - Estado
  - País
  - Número de páginas a serem buscadas
- Monta dinamicamente a URL de pesquisa no LinkedIn.
- Faz o download do conteúdo da página.
- Utiliza **web scraping** para extrair informações de vagas.
- Exibe no console o título da vaga e o nome da empresa.

## Pré-requisitos

- Python 3.8 ou superior instalado.
- Bibliotecas necessárias:
  ```bash
  pip install requests beautifulsoup4 pandas

Aqui está um exemplo de **README.md** em português, bem estruturado e sem emojis, para documentar o projeto **Automação Consultar Vagas no LinkedIn**:

```markdown
# Automação Consultar Vagas no LinkedIn

Este projeto tem como objetivo realizar uma consulta automatizada de vagas de emprego no LinkedIn utilizando **Python** e as bibliotecas `requests`, `BeautifulSoup` e `pandas`.

## Funcionalidades

- Permite ao usuário informar:
  - Nome da vaga
  - Cidade
  - Estado
  - País
  - Número de páginas a serem buscadas
- Monta dinamicamente a URL de pesquisa no LinkedIn.
- Faz o download do conteúdo da página.
- Utiliza **web scraping** para extrair informações de vagas.
- Exibe no console o título da vaga e o nome da empresa.

## Pré-requisitos

- Python 3.8 ou superior instalado.
- Bibliotecas necessárias:
  ```bash
  pip install requests beautifulsoup4 pandas
  ```

## Estrutura do Código

1. **Importação de bibliotecas**
   - `requests` para realizar requisições HTTP.
   - `BeautifulSoup` para parsear o HTML.
   - `pandas` para manipulação de dados (pode ser usado para salvar os resultados em CSV ou Excel).

2. **Entrada de dados**
   - O usuário informa os parâmetros da busca (vaga, cidade, estado, país e número de páginas).

3. **Tratamento de strings**
   - Substituição de espaços por `%20` para adequação à URL.

4. **Construção da URL**
   - A URL é montada dinamicamente com base nos parâmetros informados.

5. **Coleta de dados**
   - O conteúdo da página é baixado com `requests`.
   - O HTML é processado com `BeautifulSoup`.

6. **Extração de informações**
   - São buscados os elementos `div` com a classe `base-card`.
   - Para cada vaga encontrada, são exibidos:
     - Título da vaga (`h3`)
     - Nome da empresa (`h4`)

## Exemplo de Uso

```bash
python consultar_vagas.py
```

Exemplo de entrada no terminal:

```
Digite o nome da vaga: Cientista de Dados
Digite a cidade: São Paulo
Digite o estado: SP
Digite o país: Brasil
Quantas páginas quer buscar? 2
```

Saída esperada (exemplo):

```
Cientista de Dados
Empresa XYZ
Analista de Dados
Empresa ABC
```

## Observações Importantes

- O LinkedIn pode alterar a estrutura do HTML, o que pode exigir ajustes no código.
- O uso de scraping em sites pode estar sujeito a termos de uso. Utilize este código apenas para fins educacionais.
- Para salvar os resultados em arquivo, pode-se adaptar o código para armazenar os dados em um `DataFrame` do pandas e exportar para CSV ou Excel.

## Próximos Passos

- Implementar salvamento automático em CSV.
- Adicionar tratamento de erros para páginas sem resultados.
- Criar função para percorrer múltiplas páginas de forma iterativa.
