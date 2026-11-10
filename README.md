# Perfil de clientes y aceptación del depósito a plazo

**Autor/a:** Sofia Jazmin Ruiz

**Curso:** Herramientas básicas para el Análisis de Datos - UTN BA.

**Cohorte:** 185761

## Objetivo

Identificar qué perfiles de clientes de un banco (ocupación, nivel educativo y edad) tienen mayor tasa de aceptación del depósito a plazo y cómo se relacionan con su saldo. La subpregunta es qué segmentos superan la tasa global.

## Dataset

Bank Marketing (`bank-full.csv`), del UCI Machine Learning Repository: 45.211 clientes y 17 variables de campañas de telemarketing de un banco portugués. Fuente: [archive.ics.uci.edu/dataset/222/bank+marketing](https://archive.ics.uci.edu/dataset/222/bank%2Bmarketing). 
El original está en [`data/raw/`](data/raw/).

## Pasos realizados

1. **Limpieza (Python):** auditoría de tipos, nulos, duplicados y outliers. Los valores "unknown" de ocupación y educación (4,5% de los registros) se convirtieron en nulos y se excluyeron de cada análisis. Los outliers de edad y saldo se conservaron por ser valores plausibles. Las categorías se tradujeron al español.
2. **Exploración (Python):** cuatro gráficos con Seaborn y Matplotlib, cada uno con su interpretación.
3. **KPIs:** tasa de aceptación global (11,7%), clientes que aceptaron (5.289) y saldo mediano (448 euros).
4. **Dashboard (Power BI):** tarjetas de KPIs, cuatro gráficos y filtros por ocupación, nivel educativo y tramo de edad.

## Principales hallazgos

- Estudiantes (28,7%) y jubilados (22,8%) aceptan más del doble que el promedio.
- La tasa crece con el nivel educativo: de 8,6% en primaria a 15,0% en terciaria.
- Por edad forma una U: es más alta en menores de 26 años y en mayores de 65.
- Quienes aceptaron tienen un saldo mediano de 733 euros, frente a 417 de quienes no.

## Alcance y limitaciones

Los resultados describen asociaciones, no causas. Los segmentos más chicos, como los mayores de 65 años (751 clientes), son menos estables. Los saldos se expresan en euros. El dataset incluye el mes de contacto pero no el año.

## Enlaces

- Notebook:
https://github.com/sofiaajruiz/herramientasbasicas-ruiz-sofiajazmin/tree/main/herramientasbasicas-ruiz-sofiajazmin/Notebooks

- Dashboard:
https://github.com/sofiaajruiz/herramientasbasicas-ruiz-sofiajazmin/blob/main/herramientasbasicas-ruiz-sofiajazmin/Dashboard/dashboard_bankmarketing.pbix

## Fuentes

- Moro, S., Rita, P. y Cortez, P. (2014). *A data-driven approach to predict the success of bank telemarketing*. Decision Support Systems, 62, 22-31.
- Moro, S., Rita, P. y Cortez, P. (2012). *Bank Marketing* [conjunto de datos]. UCI Machine Learning Repository.
- Las capturas del dashboard son de elaboración propia.
REPOSITORIO	El nombre exacto de tu repositorio
NOMBRE_NOTEBOOK	El nombre del .ipynb, por ejemplo herramientasbasicas_eda_bank_marketing
