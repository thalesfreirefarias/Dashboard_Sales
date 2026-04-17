# Dashboard_Sales
Power BI Sales Dashboard


![GitHub repo size](https://img.shields.io/github/repo-size/SEU_USER/SEU_REPO?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/SEU_USER/SEU_REPO?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/SEU_USER/SEU_REPO?style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/SEU_USER/SEU_REPO?style=for-the-badge)

---

## 📌 Project Overview

Power BI dashboards focused on **sales analysis** , **manufacturing productivity** and **HR**, showcasing data modeling, DAX calculations, and data visualization best practices.


---

## Sales

This first Power Bi presents :
Revenue by Brand
Revenue and Sales Quantity by Month
Revenue by Continent


<table>
  <tr>
    <td align="center">
      <a href="#" title="Age">
        <img src="imagens/1.png" width="1000" alt="Sales"/><br>
      </a>
    </td>
  </tr>
</table>

```
Codes 
:AnoMes = FORMAT('Planilha1'[Data da Venda], "YYYY-MM")

AnoMesOrdenacao = 
YEAR('Planilha1'[Data da Venda]) * 100 +
MONTH('Planilha1'[Data da Venda])

Mes = FORMAT('Planilha1'[Data da Venda], "MMM")
MesNum = MONTH('Planilha1'[Data da Venda])
```


## Manufactor

The second one focuses on:
Productivity
Produced Items
Total Hours Worked
Approved / Rejected Parts

<table>
  <tr>
    <td align="center">
      <a href="#" title="Age">
        <img src="imagens/2.png" width="1000" alt="Manufactor"/><br>
      </a>
    </td>
  </tr>
</table>

```
Code:
worked_hours = sum('BaseProdução'[Total Horas]) 
hours_produced = CALCULATE(SUM('BaseProdução'[Total Horas]),'BaseProdução'[Ocorrência]=blank()) 
```
---

## HR

The Third one focuses on:
Number of Active Employees
Number of Hires
Number of Employees Terminated
Salary Analysis
Role and Department Analysis
Gender Distribution (%)


<table>
  <tr>
    <td align="center">
      <a href="#" title="Age">
        <img src="imagens/3.png" width="1000" alt="Manufactor"/><br>
      </a>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td align="center">
      <a href="#" title="Age">
        <img src="imagens/4.png" width="1000" alt="Manufactor"/><br>
      </a>
    </td>
  </tr>
</table>

```
Code:

Fun.ativos = 
CALCULATE(
    COUNTROWS(BaseFuncionarios),
    ISBLANK(BaseFuncionarios[Data de Demissao])
)

func.desligadas = COUNT(BaseFuncionarios[Data de Demissao])
Turnover = BaseFuncionarios[func.desligadas]/[contratações]
```
---

---

## 🛠️ Technologies Used

* Power BI
* Dax

---

## 🤝 Author

<table>
  <tr>
    <td align="center">
      <a href="https://www.linkedin.com/in/thalesfreirefarias/" target="_blank">
        <img src="grecia.jpg" width="100" alt="Thales Farias"/><br>
        <sub><b>Thales Farias</b></sub>
      </a>
    </td>
  </tr>
</table>
