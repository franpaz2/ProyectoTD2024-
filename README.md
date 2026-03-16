# ProyectoTD2024- — Análisis de tickets de compra (Mercadona)

Proyecto de **Tratamiento de Datos (Grado en Ciencia de Datos, UV)** centrado en el análisis de tickets de compra de **Mercadona (2023–2024)**.  
El objetivo es extraer, estructurar y explorar información de compra para identificar **patrones de consumo**, **productos más frecuentes**, **horas de mayor actividad** y **métricas relacionadas con el IVA**.

---

## En una frase
De tickets en PDF a un análisis reproducible en R: **convertimos tickets a texto, los estructuramos en un dataset y respondemos preguntas con visualizaciones claras**.

---

## Qué incluye el repositorio
- **Informe principal en RMarkdown**: `ProyectoTD2024.Rmd`  
  Genera salidas en **HTML / PDF / notebook** con secciones, visualizaciones y conclusiones.
- **Exportaciones del informe**: `ProyectoTD2024.html`, `ProyectoTD2024.pdf`, `ProyectoTD2024.nb.html` (y otros entregables).
- **Conversión PDF → TXT (opcional)**: `TicketPDF2TXT.ipynb` (Python)  
  Automatiza la extracción de texto desde PDFs guardados en `data/`.
- **Datos**: carpeta `data/` con tickets en **.txt** (y algunos **.pdf**).

---

## Preguntas que responde el análisis
A partir de los tickets estructurados, el proyecto trabaja preguntas como:
- **¿Cuáles son los productos más comprados?** (ranking por frecuencia)
- **¿A qué hora se realizan más compras?** (distribución por hora)
- **¿Cuál es el valor medio por tipo de IVA (0%, 5%, 10%, 21%)?**
- **Relación entre productos más/menos frecuentes y su precio** (exploratorio)

---

## Stack
- **R / RMarkdown**: limpieza, transformación, análisis y visualización.
- **Paquetes (principalmente)**: `dplyr`, `lubridate`, `tidyverse`, `ggplot2`, `readr`, `tidytext`, `quanteda`, `wordcloud`, `paletteer`, etc.
- **Python (notebook auxiliar)**: extracción de texto desde PDFs con `PyPDF2` (y notas de instalación para `camelot`/`tabula`).

---

## Cómo ejecutar
### Opción A — Ejecutar el informe (recomendado)
1. Abre el proyecto en **RStudio** (archivo `.Rproj`).
2. Asegúrate de tener la carpeta `data/` con los `.txt`.
3. Renderiza el RMarkdown:

```r
rmarkdown::render("ProyectoTD2024.Rmd", output_format = "html_document")
