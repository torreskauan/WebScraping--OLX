# OLX Web Scraping Project

## Descrição

Este projeto realiza a raspagem de dados de imóveis disponíveis para aluguel no site **OLX**. O objetivo é extrair informações como o número de quartos, banheiros, vagas de garagem, área, localidade e o valor de aluguel de cada imóvel listado. O projeto utiliza a API do ZenRows para contornar proteções contra raspagem, e o conteúdo extraído é estruturado em um **DataFrame** do **Pandas** para análises posteriores.

## Funcionalidades

- Raspagem de dados sobre imóveis de aluguel diretamente do site OLX.
- Extração de informações detalhadas de cada imóvel: link do anúncio, número de quartos, banheiros, vagas de garagem, área, localidade e valor.
- Paginação automática para raspar múltiplas páginas de resultados.
- Armazenamento dos dados coletados em um **DataFrame** para facilitar a manipulação e análise.
- Remoção de dados duplicados.

## Tecnologias Utilizadas

- **Python**: Linguagem principal utilizada.
- **BeautifulSoup**: Biblioteca para parsear HTML e extrair dados.
- **Requests**: Utilizada para fazer as requisições HTTP via a API do ZenRows.
- **Pandas**: Usado para criar um DataFrame e organizar os dados coletados.
- **ZenRows API**: Proxy para contornar bloqueios de raspagem no OLX.

## Como Executar

1. **Clone o repositório**:

   ```bash
   git clone https://github.com/seuusuario/seurepositorio.git
   ```

2. **Instale as dependências**:

   As dependências podem ser instaladas via pip:
   
   ```bash
   pip install requests beautifulsoup4 pandas
   ```

3. **Configure a chave da API do ZenRows**:

   Obtenha uma chave de API em [ZenRows](https://www.zenrows.com) e adicione-a ao código:

   ```python
   apikey = 'SUA_CHAVE_API_ZENROWS_AQUI'
   ```

4. **Execute o script**:

   O script pode ser executado diretamente em Python:

   ```bash
   python scrape_olx.py
   ```

## Estrutura do Projeto

```plaintext
📁 OLX-Web-Scraping
│
├── README.md               # Instruções e informações do projeto
├── scrape_olx.py           # Código principal de raspagem da web
└── requirements.txt        # Lista de dependências do projeto
```

## Resultados

Após a execução, os dados dos imóveis raspados serão organizados em um **DataFrame**. Cada imóvel terá as seguintes colunas:

- **link**: URL do anúncio do imóvel.
- **area**: Área total do imóvel.
- **quartos**: Número de quartos.
- **vagas**: Número de vagas de garagem.
- **banheiros**: Número de banheiros.
- **local**: Localização do imóvel (cidade ou bairro).
- **valor**: Valor do aluguel.

## Problemas Conhecidos

- Algumas listagens podem não conter todos os dados, como o número de quartos ou banheiros. O código foi desenvolvido para lidar com essas inconsistências sem quebrar o fluxo de execução.
- O OLX implementa proteções contra bots que podem impedir o acesso ao site sem o uso de proxies ou serviços como o ZenRows.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.
