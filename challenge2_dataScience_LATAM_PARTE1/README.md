<h1 align="center">📡Telecom X LATAM-Análisis de Evasión de Clientes 📡</h1>
<h1 align="center">(Challenge 2)</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.12.0-blue?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-2.2.2-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Plotly-5.24.1-3F4F75?style=for-the-badge&logo=plotly&logoColor=white"/>
  <img src="https://img.shields.io/badge/STATUS-FINALIZADO-green?style=for-the-badge"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Google%20Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white"/>
</p>

---

## 📋 Índice

- [Descripción del Proyecto](#-descripción-del-proyecto)
- [El Desafío](#-el-desafío)
- [Funcionalidades y Análisis](#-funcionalidades-y-análisis)
- [Tecnologías Utilizadas](#️-tecnologías-utilizadas)
- [Resultados Clave](#-resultados-clave)
- [Visualizaciones](#-visualizaciones)
- [Cómo Ejecutar el Proyecto](#-cómo-ejecutar-el-proyecto)
- [Estructura del Proyecto](#-estructura-del-proyecto)
- [Conclusión Final](#-conclusión-final)

---

## 🎯 Descripción del Proyecto

Este proyecto es un **análisis completo de datos de telecomunicaciones** realizado para ayudar a **Telecom X** a entender y reducir la fuga de clientes (_churn_): el fenómeno en el que los usuarios cancelan su contrato y dejan de usar el servicio.

El análisis cubre el ciclo completo de un pipeline ETL + EDA: extracción de datos desde una API pública, limpieza y transformación, análisis exploratorio de más de **20 variables** (categóricas y numéricas), y un informe final con conclusiones y recomendaciones accionables.

### 💡 Objetivo Principal

Identificar el **perfil del cliente que cancela**, descubrir qué variables están relacionadas con el churn, y proporcionar **7 recomendaciones concretas** para reducir la evasión.

---

## 🚀 El Desafío

**Practicando Python para Data Science: Challenge 2 — TelecomX**
_Especialización en Data Science - Alura LATAM_

El desafío consistió en:

- ✅ Extraer datos desde una **API pública de GitHub** en formato JSON
- ✅ Limpiar, normalizar y transformar el dataset con **Pandas**
- ✅ Crear visualizaciones impactantes e interactivas con **Plotly Express**
- ✅ Analizar variables categóricas y numéricas en relación al churn
- ✅ Crear una columna derivada (`cuentas_diarias = valor_mensal / 30`)
- ✅ Elaborar un **Informe Final** con perfil del cliente y recomendaciones

---

## 🔍 Funcionalidades y Análisis

El proyecto está organizado en **4 capítulos**:

### 1️⃣ **Cap 1 — Extracción de Datos**

- Solicitud HTTP a la API de GitHub con `requests`
- Carga del JSON en un DataFrame de Pandas
- Exploración inicial: dimensiones, tipos de datos, primeras filas

### 2️⃣ **Cap 2 — Transformación y Limpieza**

- Normalización de columnas anidadas (`pd.json_normalize`)
- Eliminación de duplicados y registros con valores nulos
- Conversión de tipos de datos (`valor_mensal`, `total_cobrado` a numérico)
- Creación de columna `cuentas_diarias` (cargo diario aproximado)
- Estandarización de variables binarias: `Yes/No → 1/0`
- Traducción de categorías al español (género, contrato, método de pago, etc.)

### 3️⃣ **Cap 3 — Análisis Exploratorio (EDA)**

#### Cap 3-1: Análisis Descriptivo

- Estadísticas generales del dataset (`describe()`)
- Distribución y rango de variables numéricas clave

#### Cap 3-2: Distribución de Churn

- Conteo y porcentaje de clientes que cancelaron vs. los que permanecieron
- **Visualización**: Gráfico de barras + gráfico de torta

#### Cap 3-3: Variables Categóricas (15 variables)

- Comparación de tasa de churn por cada variable categórica
- Variables analizadas: `genero`, `tiene +60`, `posee_pareja`, `posee_dependientes`, `servicio_telefono`, `multiples_lineas`, `tipo_internet`, `seguridad_online`, `backup_online`, `proteccion_dispositivo`, `soporte_tecnico`, `streaming_tv`, `streaming_peliculas`, `tipo_contrato`, `metodo_pago`, `factura_digital`
- **Visualización**: Histogramas agrupados interactivos (Plotly Express)

#### Cap 3-4: Variables Numéricas (4 variables)

- Distribución de cada variable numérica separada por clientes activos vs. cancelados
- Variables analizadas: `tiempo_contrato`, `valor_mensal`, `total_cobrado`, `cuentas_diarias`
- **Visualización**: Histogramas superpuestos (overlay) con Plotly Express

### 4️⃣ **Cap 4 — Informe Final**

- Síntesis de todos los hallazgos del análisis
- Perfil del cliente que cancela vs. el cliente fiel
- 7 recomendaciones estratégicas con respaldo en los datos

---

## 🛠️ Tecnologías Utilizadas

| Tecnología           | Versión | Uso en el Proyecto                           |
| -------------------- | ------- | -------------------------------------------- |
| **Python**           | 3.12.0  | Lenguaje principal                           |
| **Pandas**           | 2.2.2   | Manipulación y análisis de datos             |
| **Requests**         | 2.32.x  | Extracción de datos vía HTTP                 |
| **Plotly Express**   | 5.24.1  | Visualizaciones interactivas (Cap 3-3 y 3-4) |
| **Matplotlib**       | 3.10.0  | Visualizaciones estáticas (Cap 3-2)          |
| **Seaborn**          | 0.13.2  | Soporte visual complementario                |
| **Jupyter Notebook** | .ipynb  | Formato del proyecto                         |
| **Google Colab**     | -       | Entorno de desarrollo                        |

---

## 📊 Resultados Clave

### 📉 Distribución de Churn

| Estado                 | Clientes | Porcentaje |
| ---------------------- | -------- | ---------- |
| **Permanecen**         | ~5,174   | 74% ✅     |
| **Cancelaron (Churn)** | ~1,869   | 26% 🔴     |
| **Total**              | ~7,043   | 100%       |

> **1 de cada 4 clientes cancela el servicio.**

### 🔴 Variables Categóricas con Mayor Impacto

| Variable                          | Hallazgo Principal                                          |
| --------------------------------- | ----------------------------------------------------------- |
| **Tipo de contrato**              | Los contratos mensuales concentran casi todo el churn       |
| **Método de pago**                | El cheque electrónico tiene la tasa de cancelación más alta |
| **Tipo de internet**              | La fibra óptica cancela más que el DSL                      |
| **Tiene +60 años**                | Los mayores de 60 cancelan proporcionalmente más            |
| **Factura digital**               | Quienes reciben factura por correo se van más fácilmente    |
| **Sin pareja / Sin dependientes** | Clientes solos y sin familia cancelan más                   |

### 📈 Variables Numéricas con Mayor Impacto

| Variable               | Hallazgo Principal                                                  |
| ---------------------- | ------------------------------------------------------------------- |
| **Tiempo de contrato** | Los que cancelan llevan pocos meses; pasado el año casi nadie se va |
| **Valor mensual**      | A mayor cobro mensual, más cancelaciones                            |
| **Total cobrado**      | Los que cancelan han pagado poco en total: son clientes nuevos      |
| **Cobro diario**       | Confirma el mismo patrón que el cobro mensual                       |

---

## 📈 Visualizaciones

El proyecto incluye **visualizaciones a lo largo de 4 etapas de análisis**:

1. 🥧 **Gráfico de torta** (Cap 3-2): Distribución porcentual de churn vs. retención
2. 📊 **Gráfico de barras** (Cap 3-2): Conteo absoluto de clientes por estado
3. 📊 **Histogramas agrupados interactivos** (Cap 3-3): 16 gráficos, uno por variable categórica, con `barmode='group'` en Plotly Express
4. 📊 **Histogramas superpuestos interactivos** (Cap 3-4): 4 gráficos para variables numéricas con `barmode='overlay'` en Plotly Express

Todas las visualizaciones incluyen:

- ✅ Separación visual entre clientes que cancelaron y los que permanecen
- ✅ Títulos descriptivos por variable
- ✅ Interactividad (zoom, hover, filtros) en los gráficos de Plotly
- ✅ Paleta de colores consistente

---

## 💻 Cómo Ejecutar el Proyecto

### Opción 1: Visual Studio Code (Recomendado)

```bash
# 1. Clonar o descargar el repositorio
git clone <tu-repositorio>
cd challenge2_dataScience_LATAM_jjms

# 2. Instalar dependencias
pip install pandas requests plotly matplotlib seaborn jupyter

# 3. Abrir el archivo en VS Code
code TelecomX_1_LATAM_jjms.ipynb

# 4. Ejecutar las celdas con Shift + Enter (o "Run All")
```

### Opción 2: Jupyter Notebook local

```bash
# Instalar dependencias
pip install pandas requests plotly matplotlib seaborn jupyter

# Ejecutar Jupyter
jupyter notebook TelecomX_1_LATAM_jjms.ipynb
```

### Opción 3: Google Colab

```bash
1. Descarga el archivo TelecomX_1_LATAM_jjms.ipynb
2. Abre Google Colab (https://colab.research.google.com/)
3. Carga el archivo: Archivo > Subir notebook
4. Ejecuta todo: Entorno de ejecución > Ejecutar todo
```

**📌 Nota**: Los datos se cargan automáticamente desde la URL pública de GitHub, no requiere archivos locales.

---

## 📁 Estructura del Proyecto

```
challenge2_dataScience_LATAM_jjms/
│
├── TelecomX_1_LATAM_jjms.ipynb    # Notebook principal con análisis completo
└── README.md                  # Documentación del proyecto
```

### Estructura Interna del Notebook:

1. **Cap 1-1** → Extracción de datos vía HTTP (JSON desde GitHub)
2. **Cap 1-2** → Exploración inicial del DataFrame
3. **Cap 2-1** → Normalización y estructura del dataset
4. **Cap 2-2** → Limpieza: nulos, duplicados y tipos de datos
5. **Cap 2-3** → Creación de columna `cuentas_diarias`
6. **Cap 2-4** → Estandarización: binarios (1/0) y traducción al español
7. **Cap 3-1** → Análisis descriptivo general
8. **Cap 3-2** → Distribución de churn (barras + torta)
9. **Cap 3-3** → Variables categóricas (16 gráficos interactivos)
10. **Cap 3-4** → Variables numéricas (4 histogramas interactivos)
11. **Cap 4** → Informe Final: conclusiones y recomendaciones

---

## 🎓 Conclusión Final

### ➡️ **Perfil del Cliente que Cancela**

> _Nuevo cliente, con contrato mensual, que paga caro, vive solo, revisa su factura por correo electrónico y paga con cheque electrónico._

**🔴 Señales de riesgo:**

- Lleva pocos meses en la empresa → no ha construido fidelidad
- Tiene contrato mes a mes → puede cancelar sin penalización
- Paga con cheque electrónico → proceso manual que facilita la cancelación
- Recibe factura digital → ve el cobro cada mes y lo compara fácilmente
- Sin pareja ni dependientes → no comparte el servicio ni tiene presión familiar
- Mayor de 60 años → puede sentir que el servicio no está pensado para él

**🟢 Perfil del cliente fiel (contraste):**

- Contrato de 1 o 2 años, pago automático (tarjeta o transferencia), varios servicios activos, con familia en casa

### 📌 Las 7 Recomendaciones

| #   | Recomendación                                                              | Variable de Apoyo             |
| --- | -------------------------------------------------------------------------- | ----------------------------- |
| 1   | **Blindar el primer año** con beneficios de bienvenida                     | Tiempo de contrato            |
| 2   | **Incentivar contratos anuales o bianuales** con descuentos                | Tipo de contrato              |
| 3   | **Promover el pago automático** con ventajas exclusivas                    | Método de pago                |
| 4   | **Revisar la experiencia de fibra óptica** (precio vs. calidad)            | Tipo de internet              |
| 5   | **Incluir servicios adicionales** en paquetes básicos (seguridad, soporte) | Servicios adicionales         |
| 6   | **Atención especial a mayores de 60** con opciones adaptadas               | Tiene +60                     |
| 7   | **Acompañar a clientes solos sin familia** con programas de fidelización   | Con pareja / Con dependientes |

---

<p align="center">
  <img src="https://img.shields.io/badge/Proyecto-Challenge%202%20Alura%20LATAM-orange?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Fecha-Marzo%202026-blue?style=for-the-badge"/>
</p>

<p align="center">
  Hecho con 💙 y ☕ para Alura LATAM
</p>
