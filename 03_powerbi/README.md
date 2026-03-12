# Dashboard de Despesas Pessoais – Arquivo Power BI

Esta pasta contém o arquivo do **Power BI Desktop** (.pbix) com o dashboard completo de análise de despesas pessoais (2022–2024). O dashboard foi desenvolvido a partir de dados fictícios e conta com 5 páginas interativas, medidas DAX personalizadas e design pensado para usabilidade.

## 📁 Arquivo: `Dashboard_Despesas.pbix`

### 🖼️ Prévia das Páginas

![Página 01 – Home](https://raw.githubusercontent.com/carvalhodatadev/despesas-Power-Bi/main/03_powerbi/screnshot01.PNG)

![Página 02 – Análise por Categoria](https://raw.githubusercontent.com/carvalhodatadev/despesas-Power-Bi/main/03_powerbi/screnshot02.PNG)

![Página 03 – Análise Temporal](https://raw.githubusercontent.com/carvalhodatadev/despesas-Power-Bi/main/03_powerbi/screnshot03.PNG)

![Página 04 – Formas de Pagamento](https://raw.githubusercontent.com/carvalhodatadev/despesas-Power-Bi/main/03_powerbi/screnshot04.PNG)

![Página 05 – Detalhamento](https://raw.githubusercontent.com/carvalhodatadev/despesas-Power-Bi/main/03_powerbi/screnshot05.PNG)

## ✅ Pré‑requisitos

- Ter o **[Power BI Desktop](https://powerbi.microsoft.com/desktop/)** instalado (gratuito).
- Fazer o download ou clone deste repositório.

## 🚀 Como usar

1. Abra o arquivo `Dashboard_Despesas.pbix` no Power BI Desktop.
2. Se necessário, ajuste a fonte de dados:
   - Vá em **Página Inicial** > **Transformar Dados** > **Configuração da Fonte de Dados**.
   - Aponte para o arquivo `despesas_2022_2024_etl.csv` (localizado na pasta `02_dados`).
3. Explore as páginas e utilize os filtros interativos.

## 📊 Visão Geral das Páginas

| Página | Descrição |
|--------|-----------|
| **Home** | Visão executiva com KPIs, evolução mensal, ranking de categorias e proporção essencial/não essencial. |
| **Análise por Categoria** | Média e distribuição dos gastos por categoria, com evolução ao longo dos anos. |
| **Análise Temporal** | Gasto mensal com médias móveis, comparação anual e evolução de essenciais. |
| **Formas de Pagamento** | Totais, distribuição percentual e valores médios por forma de pagamento (débito, crédito, dinheiro, pix). |
| **Detalhamento** | Tabela interativa com todas as transações e filtros avançados. |

## 📌 Principais Medidas DAX

Algumas das medidas criadas para o dashboard:

- `Total Geral = SUM(despesas[Valor])`
- `Média Mensal = AVERAGEX(VALUES(dcalendario[Data]), [Total Geral])`
- `% Essenciais = DIVIDE([Total Essenciais], [Total Geral], 0)`
- `Média Móvel 3M = CALCULATE([Total Geral], DATESINPERIOD(dcalendario[Data], LASTDATE(dcalendario[Data]), -3, MONTH)) / 3`
- `Var % Mensal = DIVIDE([Total Geral] - [Total Mês Anterior], [Total Mês Anterior])`

*(A lista completa pode ser encontrada no próprio arquivo .pbix, na seção de Campos.)*

## 🔗 Links Úteis

- [Power BI Desktop – Download](https://powerbi.microsoft.com/desktop/)
- [Documentação DAX](https://docs.microsoft.com/pt-br/dax/)

---

**Nota:** Os dados utilizados são fictícios e foram gerados apenas para fins de demonstração.
