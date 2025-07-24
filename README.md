# Proyecto de Análisis Comparativo de Ingresos (2023-2025)

## Descripción General

Este proyecto se centra en el análisis detallado y comparativo de los ingresos generados desde 2023 hasta la fecha actual de 2025. El objetivo principal es identificar tendencias, patrones estacionales, eliminar el ruido estadístico y proporcionar insights accionables para la optimización del flujo de efectivo, la planificación de pagos a proveedores, sueldos, gastos pequeños y préstamos.

## Objetivos del Análisis

* **Análisis Comparativo de Ingresos Generales:** Comprender la evolución total de los ingresos a lo largo de los años.
* **Análisis Comparativo por `INDICE`:** Desglosar los ingresos por categorías de alto nivel (`INDICE`) para identificar cuáles son los principales motores de ingresos.
* **Análisis Comparativo por `RECAT`:** Profundizar en las subcategorías (`RECAT`) para un entendimiento más granular de las fuentes de ingreso.
* **Análisis de Series de Tiempo (`INDICE`):** Aplicar técnicas de suavizado y desestacionalización a los ingresos por `INDICE` para predecir comportamientos futuros y eliminar el ruido estadístico.
* **Estrategias de Optimización:** Generar recomendaciones basadas en los hallazgos para mejorar las entradas de efectivo y optimizar la programación de pagos.

## Estructura del Proyecto

* `data/`: Contiene el archivo de datos original (`ingresos_data.xlsx`).
* `scripts/`: Contiene el script de R (`analisis_ingresos.Rmd` o `.R`).
* `output/`: Contendrá los resultados generados, incluyendo el tablero de control HTML.
* `README.md`: Este archivo, con la descripción del proyecto.

## Fuente de Datos

Los datos provienen de un archivo Excel (`ingresos_data.xlsx`) con los siguientes campos:

| Campo                | Descripción                                                                                              |
| :------------------- | :------------------------------------------------------------------------------------------------------- |
| `FECHA`              | Fecha de la transacción.                                                                                |
| `DIA`                | Día de la transacción.                                                                                   |
| `MES`                | Mes de la transacción.                                                                                   |
| `ANIO`               | Año de la transacción.                                                                                   |
| `TIPO_DIA`           | Día de la semana (Lunes a Domingo), iniciando la semana los lunes.                                      |
| `NUMERO_DE_LA_SEMANA` | Número de la semana dentro de un mes.                                                                    |
| `QUINCENA`           | Si es la primera o segunda quincena del mes.                                                            |
| `MONTO`              | Monto de la transacción (saldo de la transacción).                                                      |
| `BANCO`              | Institución financiera asociada a la transacción.                                                        |
| `CONCEPTO`           | Concepto original bajo el cual se registró la transacción.                                               |
| `COMENTARIOS`        | Datos relevantes o notas adicionales para la transacción.                                                |
| `SALDO_ACUM`         | Suma diaria acumulada del campo `MONTO` (se reinicia cada cambio de mes).                                |
| `RECAT`              | Reclasificación de los conceptos originales (`CONCEPTO`).                                                |
| `AGRUPACION`         | Clasificación superior del campo `RECAT`.                                                                |
| `INDICE`             | Nivel elevado de agrupación para los conceptos (categoría principal).                                    |

## Herramientas Utilizadas

* **RStudio:** Para el análisis de datos y la generación de visualizaciones.
* **R Markdown:** Para crear reportes dinámicos y tableros de control.
* **Git/GitHub:** Para control de versiones y colaboración.

## Cómo Ejecutar el Proyecto

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/TuUsuario/Analisis_Ingresos_2023_2025.git](https://github.com/TuUsuario/Analisis_Ingresos_2023_2025.git)
    ```
2.  **Abrir el proyecto en RStudio:** Abre el archivo `.Rproj` (si lo creas) o el script de R.
3.  **Instalar paquetes de R:** Si no los tienes, instala los paquetes necesarios (mencionados en el script de R).
4.  **Colocar los datos:** Asegúrate de que el archivo `ingresos_data.xlsx` esté en la carpeta `data/`.
5.  **Ejecutar el script:** Corre el script `analisis_ingresos.Rmd` para generar los resultados y el tablero de control HTML en la carpeta `output/`.

## Resultados Clave y Tablero de Control

El análisis generará un tablero de control interactivo en HTML (ubicado en `output/dashboard_ingresos.html`) con las siguientes secciones:

* Resumen de ingresos por año.
* Comparativa de ingresos mensuales por año.
* Desglose de ingresos por `INDICE` y `RECAT`.
* Análisis de series de tiempo de `INDICE`, incluyendo componentes de tendencia y estacionalidad.

## Conclusiones y Recomendaciones



## Contacto


miguel.patino.mba@gmail.com


---
