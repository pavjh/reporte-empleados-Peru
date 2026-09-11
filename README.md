# Reporte de Plantilla de Empleados – Perú

Dashboard interactivo en Power BI para el análisis de plantilla de personal: distribución de empleados activos e inactivos.

![Dashboard principal](screenshots/dashboard-principal.png)

## Contexto del proyecto

Este dashboard fue diseñado para responder preguntas típicas de un área de Recursos Humanos:

- ¿Cuál es la composición actual de la plantilla (activos vs. inactivos)?
- ¿Cómo varía la contratación y el cese de personal mes a mes?
- ¿Cuál es la distribución por grupo de edad, género y estado civil de los empleados?
- ¿Existen picos estacionales de rotación que deban anticiparse?

## Fuente de datos

> ⚠️ *Nota: los datos utilizados son simulados, generados con fines de práctica al portafolio. No corresponden a información confidencial de ninguna empresa.*

El dataset contiene ~7,500 registros de empleados con variables como: país, fecha de ingreso, fecha de cese (si aplica), género, fecha de nacimiento y estado civil.

## Proceso

1. **Transformación de datos (Power Query):** limpieza de tipos de dato, cálculo de edad a partir de fecha de nacimiento, creación de columna de estado (activo/inactivo) en base a la fecha de cese.
2. **Modelado:** relación entre la tabla de empleados y una tabla de calendario para permitir el análisis por mes y año.
3. **Medidas DAX:** total de empleados, empleados activos, empleados inactivos, promedio de edad, todas calculadas de forma dinámica según los filtros seleccionados.
4. **Visualización:** tarjetas KPI, gráfico de barras (altas por mes), gráfico de líneas combinado (activos/inactivos/total por año de ingreso y cese), gráfico de edad por estado civil, y segmentadores (país, mes, año, género).

## Insights clave

- La plantilla activa representa aproximadamente el 65% del total histórico de empleados registrados.
- Se observa un incremento notable de altas en noviembre y diciembre, lo que sugiere estacionalidad en la contratación.
- El grupo de edad de 31–45 años concentra la mayor cantidad de empleados, con una edad promedio general de 53 años entre el personal activo.
- La mayoría de empleados activos se concentra en los estados civiles "soltero/a" y "casado/a".


