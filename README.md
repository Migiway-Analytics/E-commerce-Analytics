# E-commerce-Analytics
End-to-end e-commerce analytics project. Data preprocessing, RFM &amp; Cohort analysis in Python (Pandas) with interactive business dashboards built in Power BI
# E-Commerce Sales & Customer Analytics (RFM + Cohort Analysis)

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data_Processing-150458?style=for-the-badge&logo=pandas)
![Power BI](https://img.shields.io/badge/Power_BI-Data_Visualization-F2C811?style=for-the-badge&logo=powerbi)
![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20BEFF?style=for-the-badge&logo=kaggle)

## 📌 Описание проекта
Данный проект посвящен сквозному анализу транзакционных данных интернет-магазина (на базе популярного датасета Online Retail). В ходе исследования "сырые" логи продаж были очищены, агрегированы и преобразованы в аналитические витрины данных с помощью Python, после чего была построена интерактивная BI-отчетность для бизнеса.

**Главная цель проекта** — сегментировать клиентскую базу, выявить поведенческие паттерны покупателей, оценить показатели удержания (Retention) и предоставить руководству инструмент для принятия data-driven решений.

---

## 🛠 Технологический стек
* **Язык разработки:** Python (Jupyter / Kaggle Notebook)
* **Библиотеки:** Pandas, NumPy, Matplotlib, Seaborn
* **Бизнес-аналитика:** Microsoft Power BI, Power Query, DAX
* **Источники данных:** Ссылки на CSV-экспорты таблиц RFM и Когорт

---

## ⚙️ Этапы реализации проекта в Python

### 1. Предобработка и очистка данных (Data Cleaning)
* Исходный датасет содержал **541,909 строк**.
* Была проведена фильтрация транзакций: удалены отмененные заказы (депозиты/возвраты с префиксом `C` в `InvoiceNo`), а также записи с некорректным количеством товара (`Quantity <= 0`).
* Очищены критические пропуски в идентификаторах клиентов (`CustomerID`).
* Проведено обогащение данных: добавлен расчет выручки по каждой позиции (`Revenue`), извлечены временные признаки (`Month`, `DayOfWeek`).

### 2. Формирование витрин данных для BI
Для построения дашбордов в Power BI код генерирует и экспортирует три оптимизированные таблицы:
1. `clean_retail.csv` — очищенные транзакционные данные для анализа продаж.
2. `rfm_table.csv` — результаты **RFM-анализа** (Recency, Frequency, Monetary) для сегментации клиентов по активности и ценности.
3. `cohort_table.csv` — подготовленная матрица для **Когортного анализа** по месяцу первой покупки пользователя.

---

## 📊 Интерактивный дашборд Power BI
На основе выгруженных данных в Power BI разработан комплексный бизнес-отчет. Он включает в себя следующие дашборды:

1. **Sales & Orders Overview:** Динамика выручки, объема продаж и среднего чека (AOV) по месяцам, дням недели и странам.
2. **Cohort Retention Matrix:** Интерактивная тепловая карта (Heatmap), отражающая метрику Retention Rate по месячным когортам, помогающая отслеживать «смерть» и удержание клиентов.
3. **RFM Segmentation:** Распределение клиентской базы по сегментам (например: *Champions, Loyal Customers, At Risk, Hibernating*), позволяющее точечно настраивать маркетинговые кампании.
