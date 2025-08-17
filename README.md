🔁 AutoFlow – Lead Flow Automation (Salesforce)

🇧🇷 Português | 🇺🇸 English

🇧🇷 Português
📌 Visão Geral

AutoFlow é um projeto prático em Salesforce que automatiza a atualização do Status do Lead com base em eventos simples do dia a dia (ex.: alteração da Data do Primeiro Contato).
O objetivo é reduzir trabalho manual, padronizar o funil e gerar relatórios e dashboards confiáveis para acompanhamento.

➡️ Resultado atual: quando a Data do Primeiro Contato muda, o Status do Lead é atualizado automaticamente para “Working – Contacted”.
Um relatório filtrado e um dashboard acompanham os resultados.

🚀 Funcionalidades

Flow Record-Triggered no objeto Lead (modo declarativo, sem código).

Atualização automática do campo Status → “Working – Contacted”.

Campo de apoio Data do Último Contato (Date) para evoluções futuras.

Relatório “AutoFlow – Leads Qualificados” (filtro por Status).

Dashboard “AutoFlow – Monitoramento de Leads” (tabela/gráfico).

🧰 Tecnologias & Ferramentas

Salesforce Lightning (Trailhead Playground)

Flow Builder

Reports & Dashboards

Git + GitHub (documentação/portfólio)

🛠️ Como Reproduzir (resumido)

1. Ambiente

Acesse um Trailhead Playground (ou org Developer).

2. Campo de apoio

Object Manager → Lead → Fields & Relationships → New.

Tipo: Date → “Data do Último Contato” → Salvar.

3. Flow

Setup → Flows → New Flow → Record-Triggered Flow.

Object: Lead

Trigger: A record is updated

Condition: Data do Primeiro Contato Is Changed = True

Run: Every time a record is updated

Action: Update Records → Field: Status → Value: Working – Contacted

Ative o Flow.

4. Relatório

Reports → New Report → Leads

Filtro: Lead Status = Working – Contacted

Salve como “AutoFlow – Leads Qualificados”.

5. Dashboard

Dashboards → New Dashboard → “AutoFlow – Monitoramento de Leads”

Component → selecione o relatório → Table/Chart → Save.

6. Teste

Edite um Lead, altere a Data do Primeiro Contato → Salve.

Verifique se o Status = Working – Contacted.

Atualize o Dashboard.


📸 Capturas de Tela

Fluxo – Setup
![Flow Setup](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/flow-setup.png)

Fluxo – Condição
![Flow Condition](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/flow-condition.png)

Fluxo – Ação
![Flow Action](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/low-action.png)

Relatório (Filtro por Status)
![Report Filter](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/report-filter.png)

Dashboard (Leads Qualificados)
![Dashboard View](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/dashboard-view.png)



🗺️ Roadmap (evoluções futuras)

Follow-up automático por inatividade (Scheduled Path + Email Alert).

Lead Scoring baseado em Tags de Interesse / atividades.

Atribuição automática por fila/território (Round Robin).

Métricas visuais (gráficos de tendência por semana/mês).

👤 Autor

George Franklin — Salesforce Admin/Dev | Engenharia de Software | Automação

LinkedIn

GitHub

📄 Licença

MIT – uso livre para fins educacionais e portfólio.

🇺🇸 English
📌 Overview

AutoFlow is a hands-on Salesforce project that automates Lead Status updates based on simple day-to-day events (e.g., updating the First Contact Date).
The goal is to reduce manual work, standardize the pipeline, and generate reliable reports and dashboards.

➡️ Current result: whenever First Contact Date changes, the Lead Status is automatically updated to “Working – Contacted.”
A filtered report and a monitoring dashboard are included.

🚀 Features

Record-Triggered Flow on Lead (declarative, no code).

Automatic update of field Status → “Working – Contacted.”

Supporting field Last Contact Date (Date) for future upgrades.

Report “AutoFlow – Qualified Leads” (status filter).

Dashboard “AutoFlow – Lead Monitoring” (table/chart).

🧰 Tech & Tools

Salesforce Lightning (Trailhead Playground)

Flow Builder

Reports & Dashboards

Git + GitHub (documentation/portfolio)

🛠️ How to Reproduce (quick steps)

1. Org

Use a Trailhead Playground (or Developer org).

2. Supporting Field

Object Manager → Lead → Fields & Relationships → New.

Type: Date → “Last Contact Date” → Save.

3. Flow

Setup → Flows → New Flow → Record-Triggered Flow.

Object: Lead

Trigger: A record is updated

Condition: First Contact Date Is Changed = True

Run: Every time a record is updated

Action: Update Records → Field: Status → Value: Working – Contacted

Activate the Flow.

4. Report

Reports → New Report → Leads

Filter: Lead Status = Working – Contacted

Save as “AutoFlow – Qualified Leads.”

5. Dashboard

Dashboards → New Dashboard → “AutoFlow – Lead Monitoring”

Component → select the report → Table/Chart → Save.

6. Test

Edit a Lead, change the First Contact Date → Save.

Check Status = Working – Contacted.

Refresh the Dashboard.

📸 Screenshots

Fluxo – Setup
![Flow Setup](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/flow-setup.png)

Fluxo – Condição
![Flow Condition](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/flow-condition.png)

Fluxo – Ação
![Flow Action](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/low-action.png)

Relatório (Filtro por Status)
![Report Filter](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/report-filter.png)

Dashboard (Leads Qualificados)
![Dashboard View](https://raw.githubusercontent.com/georgefranklin-dev/AutoFlow-Lead-Flow-Automation/main/assets/dashboard-view.png)

🗺️ Roadmap

Automatic follow-up on inactivity (Scheduled Path + Email Alert).

Lead Scoring using Interest Tags / activities.

Auto assignment by queue/territory (Round Robin).

Visual metrics (trend charts per week/month).

👤 Author

George Franklin — Salesforce Admin/Dev | Software Engineering | Automation

LinkedIn

GitHub

📄 License

MIT – free to use for educational and portfolio purposes.
