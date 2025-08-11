# 🔁 AutoFlow – Lead Flow Automation (Salesforce)

[🇧🇷 Português](#português) | [🇺🇸 English](#english)

---

## Português

### 📌 Visão Geral
**AutoFlow** é um projeto prático em Salesforce que automatiza a atualização do **Status do Lead** com base em eventos simples do dia a dia (ex.: alteração da *Data do Primeiro Contato*). O objetivo é reduzir trabalho manual, padronizar o funil e gerar **relatórios e dashboards** confiáveis para acompanhamento.

**Resultado atual:** quando a *Data do Primeiro Contato* muda, o **Status** do Lead é atualizado automaticamente para **“Working – Contacted”**. Há um relatório filtrando esses leads e um **dashboard** para monitoramento.

---

### 🚀 Funcionalidades
- **Flow Record-Triggered** no objeto **Lead** (modo declarativo, sem código).
- Atualização automática do campo **Status** → “Working – Contacted”.
- Campo de apoio **Data do Último Contato** (Date) para futuras evoluções.
- **Relatório** “AutoFlow – Leads Qualificados” (filtro por Status).
- **Dashboard** “AutoFlow – Monitoramento de Leads” (tabela/gráfico).

---

### 🧰 Tecnologias & Ferramentas
- Salesforce Lightning (Trailhead Playground)
- **Flow Builder**
- **Reports & Dashboards**
- Git + GitHub (documentação/portfólio)

---

### 🛠️ Como Reproduzir (passo a passo resumido)
1. **Ambiente**
   - Acesse um **Trailhead Playground** (ou org Developer).
2. **Campo de apoio**
   - Em *Object Manager → Lead → Fields & Relationships → New*  
   - Tipo **Date** → **Data do Último Contato** → salve.
3. **Flow**
   - *Setup → Flows → New Flow* → **Record-Triggered Flow**
   - **Object**: Lead  
   - **Trigger**: *A record is updated*  
   - **Condition Requirements**: *All Conditions Are Met*  
   - **Condition**: *Data do Primeiro Contato* **Is Changed** = **True**  
   - **Run Flow for Updated Records**: *Every time a record is updated*  
   - **Action**: *Update Records* (use the record that triggered the flow)  
     - **Field**: *Status*  
     - **Value**: **Working – Contacted** (exatamente esse texto)  
   - **Activate** o Flow.
4. **Relatório**
   - *Reports → New Report → Leads*  
   - Filtro: **Lead Status = Working – Contacted**  
   - Salve como **“AutoFlow – Leads Qualificados”**.
5. **Dashboard**
   - *Dashboards → New Dashboard →* **AutoFlow – Monitoramento de Leads**  
   - **+ Widget/Component** → selecione o relatório acima → **Table** ou **Chart** → **Add** → **Save** → **Done**.
6. **Teste**
   - Em **Leads**, edite um registro e altere a **Data do Primeiro Contato** → salve.  
   - Verifique o **Status** = *Working – Contacted* e **atualize** o dashboard.

---

### 📸 Capturas (adicione na pasta `assets/`)
- `assets/autoflow-flow.png` – Flow (Start + Update Records)
- `assets/autoflow-report.png` – Relatório filtrado
- `assets/autoflow-dashboard.png` – Dashboard final

> No README, referencie assim:  
> `![AutoFlow Dashboard](assets/autoflow-dashboard.png)`

---

### 🗺️ Roadmap (próximas evoluções)
- **Follow-up automático por inatividade** (Scheduled Path + Email Alert).
- **Lead Scoring** baseado em *Tags de Interesses* / atividades.
- **Atribuição automática** por fila/território (Round Robin).
- Métricas visuais (gráficos de tendência por semana/mês).

---

### 👤 Autor
**George Franklin** — Salesforce Admin/Dev | Engenharia de Software | Automação  
LinkedIn: https://www.linkedin.com/in/georgefranklin-dev  
GitHub: https://github.com/georgefranklin-dev

---

### 📄 Licença
MIT – uso livre para fins educacionais e portfólio.

---

## English

### 📌 Overview
**AutoFlow** is a hands-on Salesforce project that automates **Lead Status** updates based on simple day-to-day events (e.g., changing *First Contact Date*). The goal is to reduce manual work, standardize the pipeline, and generate reliable **reports and dashboards**.

**Current result:** whenever *First Contact Date* changes, the Lead **Status** is automatically updated to **“Working – Contacted.”** A filtered report and a **monitoring dashboard** are included.

---

### 🚀 Features
- **Record-Triggered Flow** on **Lead** (declarative, no code).
- Automatic Lead **Status** update → “Working – Contacted.”
- Supporting field **Last Contact Date** (Date) for future upgrades.
- **Report** “AutoFlow – Qualified Leads” (status filter).
- **Dashboard** “AutoFlow – Lead Monitoring” (table/chart).

---

### 🧰 Tech & Tools
- Salesforce Lightning (Trailhead Playground)
- **Flow Builder**
- **Reports & Dashboards**
- Git + GitHub (documentation/portfolio)

---

### 🛠️ Reproduce (quick steps)
1. **Org**
   - Use a **Trailhead Playground** (or Developer org).
2. **Supporting Field**
   - *Object Manager → Lead → Fields & Relationships → New*  
   - Type **Date** → **Last Contact Date** → save.
3. **Flow**
   - *Setup → Flows → New Flow* → **Record-Triggered Flow**  
   - **Object**: Lead  
   - **Trigger**: *A record is updated*  
   - **Condition Requirements**: *All Conditions Are Met*  
   - **Condition**: *First Contact Date* **Is Changed** = **True**  
   - **Run Flow for Updated Records**: *Every time a record is updated*  
   - **Action**: *Update Records* (use the record that triggered the flow)  
     - **Field**: *Status*  
     - **Value**: **Working – Contacted** (exact text)  
   - **Activate** the Flow.
4. **Report**
   - *Reports → New Report → Leads*  
   - Filter: **Lead Status = Working – Contacted**  
   - Save as **“AutoFlow – Qualified Leads.”**
5. **Dashboard**
   - *Dashboards → New Dashboard →* **AutoFlow – Lead Monitoring**  
   - **+ Component** → pick the report → **Table** or **Chart** → **Add** → **Save** → **Done**.
6. **Test**
   - In **Leads**, edit a record and change **First Contact Date** → save.  
   - Check **Status** = *Working – Contacted* and **refresh** the dashboard.

---

### 📸 Screens (put under `assets/`)
- `assets/autoflow-flow.png` — Flow (Start + Update Records)
- `assets/autoflow-report.png` — Filtered report
- `assets/autoflow-dashboard.png` — Final dashboard

---

### 🗺️ Roadmap
- **Automatic follow-up on inactivity** (Scheduled Path + Email Alert).
- **Lead Scoring** using *Interest Tags* / activities.
- **Auto assignment** by queue/territory (Round Robin).
- Visual metrics (trend charts per week/month).

---

### 👤 Author
**George Franklin** — Salesforce Admin/Dev | Software Engineering | Automation  
LinkedIn: https://www.linkedin.com/in/georgefranklin-dev  
GitHub: https://github.com/georgefranklin-dev

---

### 📄 License
MIT – free to use for educational and portfolio purposes.
