
# 📊 Análise de Consumo – Condomínio Setin Downtown Nova República

Este repositório contém o notebook em Python desenvolvido para análise técnica e transparente das contas de consumo do Condomínio **Setin Downtown Nova República**, com foco na avaliação do impacto dos trocadores de calor sobre os custos de operação.

O objetivo é fornecer uma base objetiva para discussão em conselho, fundamentada em dados reais e metodologia replicável.

---

## 🎯 Objetivos da Análise

- Avaliar a evolução do consumo de:
  - Energia elétrica (Enel)
  - Gás (Comgás)
  - Água (Sabesp)
- Padronizar os consumos para permitir comparações justas entre meses.
- Verificar a relação entre consumo de água e gás (eficiência térmica).
- Analisar o custo dos trocadores de calor e seu impacto no curto prazo.
- Demonstrar, com dados, que análise financeira isolada é uma **foto de momento**, enquanto a análise de consumo é um **filme de comportamento**.

---

## 📁 Estrutura do Projeto

```
/
├── analise_consumo_downtown_notebook.ipynb
├── dados_consumo_nova_replublica.xlsx
└── README.md
```

---

## 📓 Notebook principal

O notebook `analise_consumo_downtown_notebook.ipynb` realiza:

- Leitura das abas:
  - Energia  
  - Gás  
  - Água  
  - Trocadores  

- Processamentos:
  - Padronização de consumo para 30 dias  
  - Tratamento de datas  
  - Inclusão manual da fatura Comgás de novembro/2025  

- Gráficos gerados:
  - Consumo padronizado de energia (kWh / 30 dias)
  - Valor total da fatura de energia
  - Consumo padronizado de gás (m³ / 30 dias)
  - Valor total da fatura de gás
  - Consumo de água
  - Comparação Água x Gás
  - Razão Gás / Água (indicador de eficiência térmica)
  - Custo mensal dos trocadores de calor

- Interpretação:
  - Análise técnica baseada em série histórica
  - Comparação entre consumo e não apenas valores pagos
  - Identificação de tendência de ganho de eficiência após entrada plena dos trocadores

---

## 🧮 Metodologia

### Padronização temporal
Como os ciclos de leitura não são fixos, todo consumo foi convertido para uma base de **30 dias**, segundo a fórmula:

```
Consumo padronizado = (Consumo / Dias de leitura) * 30
```

### Indicador de eficiência térmica
Utiliza-se a razão:

```
Razão Gás / Água = m³ de gás / m³ de água
```

Quanto menor essa razão ao longo do tempo, maior a eficiência do sistema de aquecimento.

---

## 📌 Dependências

Execute no início do notebook:

```python
%pip install pandas matplotlib numpy openpyxl
```

---

## ▶️ Como executar

1. Clone o repositório:
```bash
git clone <URL_DO_REPOSITORIO>
```

2. Abra o notebook:
```bash
jupyter notebook analise_consumo_downtown_notebook.ipynb
```

3. Ajuste o caminho do Excel, se necessário:
```python
EXCEL_PATH = "Pasta1.xlsx"
```

4. Execute as células sequencialmente.

---

## ⚠️ Observações Importantes

- O gás é utilizado exclusivamente para aquecimento central de água.
- A entrada em operação dos trocadores foi gradual, atingindo plena capacidade apenas a partir de outubro/2025.
- A forte redução observada em novembro/2025 indica que os resultados devem ser avaliados como tendência, não como evento isolado.

---

## 👤 Autor

**Gabriel Izar**  
Conselheiro Suplente  
Condomínio Setin Downtown Nova República  

Documento técnico criado em resposta a questionamentos internos e para assegurar transparência na gestão condominial.

---

## 📜 Licença

Este projeto é de uso exclusivo do Condomínio Setin Downtown Nova República, destinado a fins de auditoria interna, transparência e suporte à tomada de decisão.

---

## 💬 Considerações finais

Este repositório busca transformar debate político em análise técnica baseada em dados, promovendo decisões mais justas, racionais e fundamentadas para o coletivo.

“Dados contam histórias. Planilhas não mentem — apenas precisam ser interpretadas.”

---
