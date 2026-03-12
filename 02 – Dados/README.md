# Dados de Despesas (2022-2024)

Esta pasta contém o arquivo `despesas_2022_2024_etl.csv` com dados **fictícios** de despesas , gerados para simular um cenário real de controle financeiro.
Os dados foram utilizados como fonte para o dashboard de despesas pessoais desenvolvido no Power BI.

## 📁 Arquivo: `despesas_2022_2024_etl.csv`

### Estrutura das Colunas

| Coluna | Descrição | Exemplo |
|--------|-----------|---------|
| `Data` | Data da transação (formato DD/MM/AAAA) | `01/01/2022` |
| `Categoria` | Categoria do gasto (ex: Alimentação, Transporte, Moradia, etc.) | `Transporte` |
| `Descrição` | Breve descrição da despesa | `Despesa com transporte` |
| `Essencial` | Indica se o gasto é essencial (`Sim`) ou não (`Não`) | `Sim` |
| `FormaPagamento` | Forma de pagamento utilizada (Dinheiro, Cartão de Crédito, Cartão de Débito, Pix) | `Cartão de Crédito` |
| `Valor` | Valor da despesa em R$ (formato decimal) | `1211.68` |

### Características dos Dados
- **Período coberto:** 2022 a 2024
- **Volume:** Aproximadamente [3.000] linhas
- **Dados fictícios:** Todos os valores e descrições foram gerados artificialmente para fins de demonstração .
- **Privacidade:** Nenhum dado pessoal ou real foi utilizado.

### Como os dados foram gerados
Os dados foram criados para simular um cenário realista de finanças pessoais, com variações sazonais, categorias variadas e diferentes formas de pagamento.
Eles servem como base para explorar as funcionalidades do dashboard e demonstrar técnicas de análise em Power BI.

### Uso no Dashboard
No Power BI, este arquivo CSV é importado e utilizado como fonte para as tabelas de fatos e dimensões, permitindo a criação de medidas, relacionamentos e visuais interativos.
