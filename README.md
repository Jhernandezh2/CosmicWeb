# Cosmic Web Classification with ASTRA – BGS DESI

Este proyecto realiza la clasificación de estructuras cósmicas (voids, sheets, filaments y knots) usando el algoritmo **ASTRA** aplicado al catálogo **BGS (Bright Galaxy Sample)** del **survey DESI**, incluyendo análisis Monte Carlo con 100 iteraciones de archivos random por roseta.  

Se incluyen métricas estadísticas, gráficas comparativas y tablas exportadas listas para LaTeX/Overleaf.

---

## Descripción General

- 🚀 Conversión de coordenadas esféricas (RA, DEC, Z) a cartesianas (X, Y, Z).
- 🔍 Clasificación estructural punto a punto con ASTRA (basado en análisis del tensor de deformación).
- 🎲 Generación de 100 randoms por roseta para análisis de robustez y cálculo de **entropía de Shannon**.
- 📊 Visualizaciones comparativas (datos vs randoms), tablas de fracciones por tipo, y curvas PDF de entropía.
- 📁 Exportación en CSV + PNG para uso directo en presentaciones y artículos científicos.

---

## Requisitos

- Python 3.8+
- Paquetes: `numpy`, `pandas`, `matplotlib`, `scipy`, `astropy`, `tqdm`, `sklearn`, `pickle`

## 📁 Estructura del Proyecto

<details>
<summary><strong>01_raw_data/</strong> – Datos originales</summary>

- `importar_datos_1.ipynb` – Carga y limpieza de datos originales del BGS y randoms DESI.
</details>

<details>
<summary><strong>02_exploracion/</strong> – Exploración preliminar</summary>

- `exploracion_rosetas.ipynb` – Distribución espacial y conteo inicial por roseta.
</details>

<details>
<summary><strong>03_cartesianas/</strong> – Conversión a coordenadas cartesianas</summary>

- `coordenadas_cartesianas.ipynb` – Conversión RA, DEC, Z → X, Y, Z.
</details>

<details>
<summary><strong>04_clasificacion/</strong> – Clasificación con ASTRA</summary>

- `clasificacion_ASTRA.ipynb` – Clasificación tipo cósmico (void/sheet/filament/knot).
</details>

<details>
<summary><strong>05_Cargar_randoms/</strong> – Carga y división de randoms</summary>

- `procesar_randoms.ipynb` – Separación y guardado de randoms individuales por roseta.
</details>

<details>
<summary><strong>06_astrology_random_MC/</strong> – Análisis de 100 iteraciones Monte Carlo</summary>

- `Random_final.ipynb` – Entropía y clasificación para 100 archivos randoms.
</details>

<details>
<summary><strong>07_visualizaciones_100_random_vs_datos/</strong> – Plots y tablas finales</summary>

- `100_random_plots/` – PDFs, histogramas y distribución de entropía.
- `100_random_tablas/` – Tablas individuales y generales (PNG y CSV).
- `random_vs_datos.ipynb` – Notebook de visualización resumen.
</details>

<details>
<summary><strong>typed_by_rosetta/</strong> – Archivos `.pkl` por roseta</summary>

- Contiene 20 archivos `df_typed_rosetta_i.pkl`, cada uno con 100 iteraciones clasificadas.
</details>

<details>
<summary><strong>XYZ_outputs/</strong> – Coordenadas cartesianas finales</summary>

- `XYZ_data/` – Coordenadas de los datos reales.
- `XYZ_random/` – Coordenadas de los datos random.
</details>

---

## Resultados

- Tablas de fracción por tipo estructural para datos y randoms, por roseta y general.
- Histogramas de entropía normalizada con KDE.
- Gráficas comparativas PC1 vs PC2 filtradas por tipo (void, sheet, filament, knot).
- Tablas exportadas en CSV listas para LaTeX y presentación académica.

---

## Créditos

Este análisis se basa en el algoritmo **ASTRA**, adaptado al catálogo **DESI BGS**.  
Desarrollado por **@jhernandezh2** como parte de un proyecto de investigación cosmológica.

---
