# NovaRetail+ – Explorando Factores de Comportamiento y Rentabilidad

Este repositorio contiene el proyecto de análisis exploratorio, validación de calidad de datos y evaluación correlacional del comportamiento de los clientes de **NovaRetail+**, una plataforma de comercio electrónico en Latinoamérica.

---

## 🎯 Objetivo del proyecto

El objetivo principal de este proyecto es responder a la pregunta clave del equipo de **Crecimiento y Retención** para el cierre de 2024: **¿Qué factores del comportamiento del cliente están más fuertemente asociados con el ingreso anual generado?** A través de un análisis exploratorio y estadístico, se busca identificar patrones de interacción, medir correlaciones clave y generar *insights* accionables para potenciar las ventas y mitigar la tasa de cancelación (*churn*).

> **Nota metodológica:** Este proyecto es un análisis **correlacional** (exploratorio). **Correlación ≠ causalidad.**

---

## 📊 Dataset utilizado

El análisis se fundamenta en un conjunto de datos integral con **15,000 registros** y **12 variables** (`/datasets/novaretail_comportamiento_clientes_2024.csv`):

* **Variables Demográficas y de Perfil:** `id_cliente`, `edad`, `nivel_ingreso`, `region` (*norte, sur, este, oeste*) y `tipo_dispositivo` (*móvil, escritorio, tablet*).
* **Variables de Interacción y Marketing:** `visitas_mes`, `compras_mes`, `gasto_publicidad_dirigida` y `satisfaccion` (escala del 1 al 5).
* **Variables de Estado y Métrica Objetivo:** `miembro_premium` (binaria), `abandono` (binaria) e `ingreso_anual` (métrica principal de impacto económico).

---

## 🛠️ Etapas del análisis realizadas

1. **Diagnóstico y Preparación de Datos:**
   - Validación de integridad del dataset (15,000 registros completos sin valores nulos).
   - Estandarización de tipos de datos (conversión de `edad` a entero).
   - Análisis descriptivo de variables numéricas, binarias (desbalance en membresía *premium* con 13.9% y *churn* con 15.1%) y categóricas (predominio del canal *móvil* con 65.5%).
2. **Análisis Visual de Relaciones (EDA):**
   - Generación de matriz de correlación (*Heatmap*) para detectar asociaciones lineales entre variables numéricas.
   - Evaluación de dispersión (*Scatterplots*) en pares de variables clave (`compras_mes` vs. `ingreso_anual` y `visitas_mes` vs. `gasto_publicidad_dirigida`).
3. **Evaluación Estadística y Correlacional:**
   - Aplicación de coeficientes adecuados según la naturaleza de cada variable: **Pearson** (relaciones lineales), **Spearman** (relaciones monótonas), **Punto Biserial** (numérica–binaria) y **V de Cramér** (asociaciones categóricas).
4. **Conclusiones y Hallazgos Clave:**
   - Identificación de la frecuencia de compra (`compras_mes`, $r = 0.97$) como el principal impulsor asociado al `ingreso_anual`.
   - Determinación del impacto positivo moderado de la publicidad dirigida sobre el tráfico mensual ($r = 0.58$) y la nula correlación lineal de factores demográficos (`edad`, `nivel_ingreso`) con el gasto en la plataforma.

---

## 🚀 Cómo ejecutar el notebook

Puedes explorar y ejecutar el análisis interactivo de dos formas:

### Opción 1: Abrir en Google Colab (Recomendado)
Haz clic en el siguiente botón para abrir el cuaderno directamente en Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ml5K82VTXoynzBM_l9rbkm8JZ57i6s0J?usp=sharing)

*(Nota: Recuerda actualizar el enlace del badge si este cuaderno tiene una URL distinta en tu Google Drive).*

### Opción 2: Desde el visor de GitHub
1. Haz clic en el archivo `.ipynb` correspondiente dentro de este repositorio para ver la versión pre-renderizada directamente en tu navegador.
2. Utiliza el botón **Open in Colab** que aparece en la parte superior del visor de GitHub.

---

## 📖 Guía de reproducción local

Sigue estos pasos para ejecutar el notebook en tu entorno local (Jupyter Notebook / VS Code):

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/Diego230703/S7-Project-ConnectaTel.git](https://github.com/Diego230703/S7-Project-ConnectaTel.git)
