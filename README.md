# 🎮 Xbox Game Pass — Dashboard de Assinantes

Dashboard analítico de assinantes do Xbox Game Pass desenvolvido em Microsoft Excel, com dados estruturados, cálculos automatizados e visualização executiva.

---

## 📋 Sobre o Projeto

Este projeto simula um cenário real de análise de base de assinantes de uma plataforma de jogos por assinatura (modelo Game Pass). O objetivo é transformar dados brutos de assinantes em indicadores estratégicos (KPIs) organizados em um dashboard de fácil leitura, atualização automática e pronto para apresentação.

---

## 📁 Estrutura do Repositório

```
📦 xbox-gamepass-dashboard
 ┣ 📊 dashboard_xbox.xlsx   # Arquivo Excel com dashboard completo
 ┗ 📄 README.md             # Documentação do projeto
```

### Abas do Excel

| Aba | Descrição |
|---|---|
| `Assets` | Paleta de cores e elementos visuais do projeto |
| `Bases` | Base de dados bruta com 295 assinantes |
| `Cálculos` | Todas as métricas e fórmulas intermediárias |
| `Dashboard` | Painel executivo com KPIs e tabelas analíticas |

---

## 📊 Os Dados

A base contém **295 registros de assinantes** com as seguintes colunas:

| Campo | Descrição |
|---|---|
| `Subscriber ID` | Identificador único do assinante |
| `Name` | Nome do assinante |
| `Plan` | Plano contratado (Ultimate / Standard / Core) |
| `Start Date` | Data de início da assinatura |
| `Auto Renewal` | Renovação automática ativa (Yes/No) |
| `Subscription Price` | Preço base da assinatura (R$) |
| `Subscription Type` | Tipo de cobrança (Monthly / Quarterly / Annual) |
| `EA Play Season Pass` | Possui add-on EA Play (Yes/No) |
| `EA Play Season Pass Price` | Valor do add-on EA Play (R$) |
| `Minecraft Season Pass` | Possui add-on Minecraft (Yes/No) |
| `Minecraft Season Pass Price` | Valor do add-on Minecraft (R$) |
| `Coupon Value` | Valor de desconto/cupom aplicado (R$) |
| `Total Value` | Valor total cobrado (R$) |

### Distribuição da Base

- **Planos:** Core (101) · Ultimate (98) · Standard (96)
- **Tipos:** Monthly (139) · Quarterly (85) · Annual (71)

---

## 📈 KPIs e Cálculos

A aba **Cálculos** centraliza todas as métricas usando fórmulas dinâmicas que referenciam a aba Bases. Os principais indicadores são:

### KPIs Gerais
- Total de Assinantes
- Receita Total (R$)
- Ticket Médio (R$)
- Total de Cupons Utilizados (R$)
- Receita Líquida (R$)
- Taxa de Renovação Automática (%)
- Assinantes com Ambos os Add-ons

### Por Plano e Tipo de Assinatura
- Quantidade e % de participação
- Receita e ticket médio por segmento
- Taxa de renovação por plano

### Add-ons
- % de adoção de EA Play Season Pass
- % de adoção de Minecraft Season Pass
- Receita gerada por add-on

### Crescimento Mensal
- Novos assinantes por mês (Jan/24 a Jan/25)
- Acumulado de assinantes ao longo do período

---

## 🖥️ Dashboard

O painel executivo (aba **Dashboard**) apresenta:

- **Header** com título e data automática
- **5 KPI Cards** destacados com cores por categoria
- **Tabela de Distribuição por Plano** com totais
- **Tabela de Tipo de Assinatura** lado a lado
- **Tabela de Adoção de Add-ons** com receita
- **Tabela de Crescimento Mensal** com acumulado

Todas as células do Dashboard são vinculadas à aba Cálculos — qualquer atualização na base reflete automaticamente em todo o painel.

---

## 🚀 Como Reproduzir

### Pré-requisitos
- Microsoft Excel 2016 ou superior  
  *(ou Google Sheets — compatibilidade parcial)*

### Passos

1. **Clone o repositório**
   ```bash
   git clone https://github.com/grantdanust/dio-dashboard-projeto-totvs.git
   cd dio-dashboard-projeto-totvs
   ```

2. **Abra o arquivo**
   ```
   Abra dashboard_xbox.xlsx no Microsoft Excel
   ```

3. **Habilite as macros/atualizações** se solicitado pelo Excel

4. **Atualize os dados (opcional)**  
   Adicione ou edite linhas na aba `Bases` — os cálculos e o dashboard atualizam automaticamente.

5. **Explore o Dashboard**  
   Navegue até a aba `Dashboard` para visualizar todos os KPIs.

---

## 🔄 Como Atualizar a Base de Dados

Para adicionar novos assinantes, basta inserir uma nova linha na aba `Bases` seguindo o mesmo padrão das colunas existentes. Todas as fórmulas nas abas `Cálculos` e `Dashboard` estão configuradas para expandir automaticamente até a linha 500.

---

## 🎨 Paleta de Cores

| Cor | Hex | Uso |
|---|---|---|
| Verde Escuro | `#107C10` | Header, footer, destaques |
| Verde Médio | `#22C55E` | Cabeçalhos de seção |
| Verde Claro | `#9BC848` | Cabeçalhos de tabela |
| Teal | `#2AE6B1` | KPI Ticket Médio |
| Verde Neon | `#5BF6A8` | KPI Add-ons |

---

## 🛠️ Tecnologias

- **Microsoft Excel** — tabelas, fórmulas e dashboard
- **Fórmulas utilizadas:** `COUNTIF`, `COUNTIFS`, `SUMIF`, `SUMPRODUCT`, `IFERROR`, `AVERAGE`, `TEXT`, `TODAY`, `YEAR`, `MONTH`

---

## 📝 Licença

Este projeto foi desenvolvido para fins de portfólio e análise de dados. Livre para uso e adaptação.
