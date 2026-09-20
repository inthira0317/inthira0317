

### 1. `README.md`

Create/update:

`inthira0317/inthira0317/README.md`

Then paste this:

```markdown
<!-- ===================================================== -->
<!--                    HEADER                             -->
<!-- ===================================================== -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0FAAFF,50:087EA4,100:005B82&height=220&section=header&text=Inthira%20Priyatharshini&fontSize=42&fontColor=ffffff&fontAlignY=38&desc=SAP%20ABAP%20Developer&descAlignY=58&descSize=20&animation=fadeIn" width="100%"/>

<br>

<a href="https://git.io/typing-svg">
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2800&pause=900&color=0FAAFF&center=true&vCenter=true&width=700&lines=SAP+ABAP+Developer;Classical+ALV+%7C+Smart+Forms+%7C+Open+SQL;SAP+MM+%7C+SAP+HR;Building+Business+Solutions+with+ABAP" />
</a>

<br><br>

<a href="https://www.linkedin.com/in/bminthira">
<img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<a href="https://github.com/inthira0317">
<img src="https://img.shields.io/badge/GitHub-Profile-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="https://leetcode.com/u/inthira0317/">
<img src="https://img.shields.io/badge/LeetCode-Profile-FFA116?style=for-the-badge&logo=leetcode&logoColor=black"/>
</a>

</div>

---

<!-- ===================================================== -->
<!--                    ABOUT                               -->
<!-- ===================================================== -->

## 👋 About Me

```text
SAP ABAP Developer
│
├── SAP MM
│   ├── Purchase Orders
│   ├── Service Entry Sheets
│   ├── Vendor & Invoice Data
│   └── ALV Reporting
│
├── SAP HR
│   ├── Employee Eligibility
│   ├── Loan Processing
│   ├── Repayment Plans
│   └── Accrued Interest
│
└── ABAP Development
    ├── Open SQL
    ├── Smart Forms
    ├── Function Modules
    ├── Debugging
    └── Data Validation
```

I build practical SAP ABAP solutions around **reporting, forms, business logic, data processing, and validation**.

Currently expanding my knowledge into **Object-Oriented ABAP, CDS, OData, RAP, Fiori, ABAP Cloud and SAP BTP**.

---

# ⚡ SAP TECH STACK

<div align="center">

### ABAP

<img src="https://img.shields.io/badge/SAP_ABAP-0FAAFF?style=for-the-badge&logo=sap&logoColor=white"/>
<img src="https://img.shields.io/badge/Open_SQL-1F2937?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Internal_Tables-1F2937?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Function_Modules-1F2937?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Debugging-1F2937?style=for-the-badge"/>

### Reporting & Forms

<img src="https://img.shields.io/badge/Classical_ALV-0FAAFF?style=for-the-badge"/>
<img src="https://img.shields.io/badge/REUSE_ALV_GRID_DISPLAY-0FAAFF?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Smart_Forms-0FAAFF?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Field_Catalog-1F2937?style=for-the-badge"/>

### SAP Modules

<img src="https://img.shields.io/badge/SAP_MM-087EA4?style=for-the-badge&logo=sap&logoColor=white"/>
<img src="https://img.shields.io/badge/SAP_HR-087EA4?style=for-the-badge&logo=sap&logoColor=white"/>

### Modern SAP Development

<img src="https://img.shields.io/badge/OO_ABAP-444444?style=for-the-badge"/>
<img src="https://img.shields.io/badge/CDS-444444?style=for-the-badge"/>
<img src="https://img.shields.io/badge/OData-444444?style=for-the-badge"/>
<img src="https://img.shields.io/badge/RAP-444444?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Fiori-444444?style=for-the-badge"/>
<img src="https://img.shields.io/badge/ABAP_Cloud-444444?style=for-the-badge"/>
<img src="https://img.shields.io/badge/SAP_BTP-444444?style=for-the-badge"/>

</div>

---

# 🧠 REAL-WORLD ABAP

## 📊 Classical ALV

```abap
SELECT
    ekpo~matnr,
    makt~maktx,
    ekpo~ebeln,
    ekpo~ebelp,
    ekpo~menge,
    ekpo~netwr,
    ekko~lifnr,
    lfa1~name1
  FROM ekpo
  INNER JOIN ekko
    ON ekko~ebeln = ekpo~ebeln
  LEFT JOIN makt
    ON makt~matnr = ekpo~matnr
  LEFT JOIN lfa1
    ON lfa1~lifnr = ekko~lifnr
  INTO CORRESPONDING FIELDS OF TABLE @gt_output.
```

### ALV Features

```text
Selection Screen
      ↓
Open SQL Joins
      ↓
Internal Table
      ↓
Field Catalog
      ↓
Sorting / Totals
      ↓
Conditional Cell Color
      ↓
Interactive ALV
      ↓
MM03 / ME23N / XK03
```

---

# 📄 SMART FORMS

### PO + SES → Business Document

<div align="center">

```text
┌───────────────────┐
│   PURCHASE ORDER  │
└─────────┬─────────┘
          │
          │
┌─────────▼─────────┐
│ SERVICE ENTRY     │
│ SHEET              │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│    ABAP DRIVER    │
│     PROGRAM       │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│ SAP TABLE DATA    │
│ EKKO / EKPO       │
│ ESSR / LFA1       │
│ RBKP / RSEG       │
│ EKBE / MAKT       │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│   SMART FORM      │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│ FINAL DOCUMENT    │
└───────────────────┘
```

</div>

### Form Data

`PO Details` · `SES Details` · `Vendor` · `Service Period` · `Invoice` · `Payment` · `Amounts`

---

# 👨‍💼 SAP HR ABAP

```text
              EMPLOYEE
                  │
                  ▼
        ┌─────────────────┐
        │ ELIGIBILITY     │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ VALIDATION      │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ LOAN PROCESSING │
        └────────┬────────┘
                 │
          ┌──────┴──────┐
          ▼             ▼
    LOAN BALANCE    REPAYMENT PLAN
          │             │
          └──────┬──────┘
                 ▼
        ┌─────────────────┐
        │ ACCRUED         │
        │ INTEREST        │
        └─────────────────┘
```

### SAP HR Objects

```text
PA0045
PA0078
HR_GET_LOAN_BAL_PAID_AMT
PCLO_BUILD_REPAYMENT_PLAN
```

---

# 🔥 ABAP OBJECTS I'VE WORKED WITH

<div align="center">

| Area | Technologies |
|---|---|
| Reports | ABAP Reports · Classical ALV |
| Database | Open SQL · JOIN · Internal Tables |
| Forms | Smart Forms · Driver Programs |
| Logic | Function Modules · FORM Routines |
| MM | EKKO · EKPO · EKBE · ESSR · LFA1 |
| Invoice | RBKP · RSEG |
| HR | PA0045 · PA0078 |
| HR Logic | Eligibility · Loans · Repayment · Interest |
| Debugging | Breakpoints · Data Analysis · Error Resolution |

</div>

---

# 🚀 FEATURED PROJECTS

<div align="center">

<table>
<tr>

<td width="50%" valign="top">

<h3>📄 Smart Forms — PO & SES</h3>

<p>
ABAP-driven Smart Form solution accepting Purchase Order
and Service Entry Sheet inputs and dynamically retrieving
business information.
</p>

<img src="https://img.shields.io/badge/ABAP-0FAAFF?style=flat-square"/>
<img src="https://img.shields.io/badge/Smart_Forms-0FAAFF?style=flat-square"/>
<img src="https://img.shields.io/badge/SAP_MM-087EA4?style=flat-square"/>

</td>

<td width="50%" valign="top">

<h3>📊 Material PO ALV</h3>

<p>
Classical ALV report using Open SQL joins with totals,
sorting, conditional cell coloring and interactive
transaction navigation.
</p>

<img src="https://img.shields.io/badge/ALV-0FAAFF?style=flat-square"/>
<img src="https://img.shields.io/badge/Open_SQL-087EA4?style=flat-square"/>
<img src="https://img.shields.io/badge/SAP_MM-087EA4?style=flat-square"/>

</td>

</tr>

<tr>

<td width="50%" valign="top">

<h3>👨‍💼 HR Eligibility Processing</h3>

<p>
HR ABAP program for employee eligibility, amount
validation, data retrieval and controlled updates.
</p>

<img src="https://img.shields.io/badge/ABAP-0FAAFF?style=flat-square"/>
<img src="https://img.shields.io/badge/SAP_HR-087EA4?style=flat-square"/>

</td>

<td width="50%" valign="top">

<h3>💰 HR Loan Processing</h3>

<p>
Function module enhancement for loan validation,
loan balance, repayment plan and accrued interest
calculation.
</p>

<img src="https://img.shields.io/badge/PA0045-0FAAFF?style=flat-square"/>
<img src="https://img.shields.io/badge/PA0078-087EA4?style=flat-square"/>
<img src="https://img.shields.io/badge/ABAP-0FAAFF?style=flat-square"/>

</td>

</tr>
</table>

</div>

> **Note:** Add repository links to these cards once the corresponding ABAP repositories are public.

---

# 📈 GITHUB ACTIVITY

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=inthira0317&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github" height="170"/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=inthira0317&layout=compact&theme=tokyonight&hide_border=true" height="170"/>

<br>

<img src="https://streak-stats.demolab.com/?user=inthira0317&theme=tokyonight&hide_border=true" width="70%"/>

</div>

---

# 📊 CONTRIBUTION ACTIVITY

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=inthira0317&theme=tokyo-night&hide_border=true&area=true" width="95%"/>

</div>

---

# 🐍 CONTRIBUTION SNAKE

<div align="center">

<picture>
  <source
    media="(prefers-color-scheme: dark)"
    srcset="https://raw.githubusercontent.com/inthira0317/inthira0317/output/github-snake-dark.svg">
  <source
    media="(prefers-color-scheme: light)"
    srcset="https://raw.githubusercontent.com/inthira0317/inthira0317/output/github-snake.svg">
  <img
    alt="github contribution snake"
    src="https://raw.githubusercontent.com/inthira0317/inthira0317/output/github-snake.svg">
</picture>

</div>

---

# 🌱 CURRENTLY LEARNING

<div align="center">

```text
                    SAP ABAP
                       │
          ┌────────────┴────────────┐
          ▼                         ▼
      OO ABAP                    CDS Views
          │                         │
          └────────────┬────────────┘
                       ▼
                     OData
                       │
                       ▼
                      RAP
                       │
                       ▼
                     Fiori
                       │
                       ▼
                  ABAP Cloud
                       │
                       ▼
                    SAP BTP
```

</div>

---

# 💡 DEVELOPMENT MINDSET

```text
Understand the Requirement
          ↓
Understand the SAP Data Model
          ↓
Design the ABAP Logic
          ↓
Write the Code
          ↓
Debug 🔍
          ↓
Test 🧪
          ↓
Optimize ⚡
          ↓
Deliver 🚀
```

---

# 📫 LET'S CONNECT

<div align="center">

<a href="https://www.linkedin.com/in/bminthira">
<img src="https://img.shields.io/badge/LinkedIn-BM%20Inthira%20Priyatharshini-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<a href="https://github.com/inthira0317">
<img src="https://img.shields.io/badge/GitHub-inthira0317-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="https://leetcode.com/u/inthira0317/">
<img src="https://img.shields.io/badge/LeetCode-inthira0317-FFA116?style=for-the-badge&logo=leetcode&logoColor=black"/>
</a>

</div>

<br>

<div align="center">

### `ABAP • Debug • Build • Improve 🚀`

</div>

<!-- ===================================================== -->
<!--                    FOOTER                             -->
<!-- ===================================================== -->

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:005B82,50:087EA4,100:0FAAFF&height=120&section=footer" width="100%"/>
```

### 2. Add the animated contribution snake

The snake is not just a README image—you need a GitHub Action to generate its SVG. This is the same general approach used by the `snk` ecosystem; contribution-snake animations require a workflow to generate the output. :chatgpt-content-reference{index="1"}

Create:

```text
.github/
└── workflows/
    └── snake.yml
```

Put this inside `snake.yml`:

```yaml
name: Generate Contribution Snake

on:
  schedule:
    - cron: "0 0 * * *"

  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest

    permissions:
      contents: write

    steps:
      - name: Generate snake
        uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark

      - name: Publish to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          build_dir: dist
        env:
          GH_PAT: ${{ secrets.GITHUB_TOKEN }}
          BUILD_CONTRIBUTION_GRAPH: true
```

### 3. Your profile will then have this flow

```text
                    YOUR PROFILE
                         │
                         ▼
              ┌────────────────────┐
              │ Animated SAP Header │
              └──────────┬─────────┘
                         ▼
                 About / Identity
                         │
                         ▼
                 SAP Tech Stack
                         │
             ┌───────────┼───────────┐
             ▼           ▼           ▼
            ALV      Smart Forms    HR ABAP
             │           │           │
             └───────────┼───────────┘
                         ▼
                  Featured Projects
                         │
                         ▼
                  GitHub Statistics
                         │
                         ▼
                  Activity Graph
                         │
                         ▼
                🐍 Contribution Snake
                         │
                         ▼
                  Learning Roadmap
                         │
                         ▼
                     Connect
