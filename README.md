# TPE Fundamentos de la Ciencia de Datos 2026 — Stack Overflow Developer Survey 2025

**Grupo 5:** Landolfi, Mateo Nicolás · Bottini, Yaco · Barletta, Ian Franco Pehuen
**Ayudante asignada:** Daniela Godoy

Análisis exploratorio, limpieza y validación de hipótesis sobre la encuesta anual de Stack Overflow a personas que trabajan en desarrollo de software.

## Contenido del repositorio

| Archivo | Descripción |
| --- | --- |
| `TPE_Fundamentos_de_la_Ciencia_de_Datos.ipynb` | Notebook con todo el análisis, organizada en secciones |
| `Informe_TPE_Fundamentos_de_la_Ciencia_de_Datos.pdf` | Informe con los hallazgos y conclusiones |
| `results.csv.gz` | Datos de la encuesta (CSV comprimido) |
| `requirements.txt` | Librerías necesarias para ejecutar la notebook |
| `README.md` | Este archivo |

## Datos

Se usa el archivo de resultados de la **Stack Overflow Developer Survey 2025** (49.191 respuestas y 172 columnas), publicado en el repositorio oficial [StackExchange/Survey](https://github.com/StackExchange/Survey).

El CSV original pesa unos 140 MB y GitHub no admite archivos de más de 100 MB, por eso se incluye comprimido como `results.csv.gz` (16 MB). **No hace falta descomprimirlo:** pandas lo lee directamente.

## Cómo ejecutar la notebook

**Requisitos:** Python 3.11 o superior (probado con Python 3.13) y `pip`.

1. Clonar o descargar el repositorio y entrar a la carpeta:

   ```bash
   git clone <URL-del-repositorio>
   cd <carpeta-del-repositorio>
   ```

2. (Opcional, recomendado) Crear y activar un entorno virtual:

   ```bash
   python -m venv .venv
   source .venv/bin/activate      # Linux / macOS
   .venv\Scripts\activate         # Windows
   ```

3. Instalar las dependencias:

   ```bash
   pip install -r requirements.txt
   ```

4. Abrir la notebook:

   ```bash
   jupyter notebook TPE_Fundamentos_de_la_Ciencia_de_Datos.ipynb
   ```

5. Ejecutar todas las celdas en orden con **Kernel → Restart & Run All**. El archivo `results.csv.gz` tiene que estar en la misma carpeta que la notebook. La ejecución completa tarda unos minutos.

### Alternativa: Google Colab

1. Abrir la notebook en Colab (**Archivo → Subir notebook**).
2. Subir `results.csv.gz` desde el panel **Archivos** (ícono de carpeta, a la izquierda).
3. Ejecutar todo con **Entorno de ejecución → Ejecutar todas**.

Si no se sube `results.csv.gz`, la primera celda descarga automáticamente el CSV original desde el repositorio oficial de Stack Overflow.

## Estructura de la notebook

1. **Análisis exploratorio inicial:** origen de los datos, atributos, valores nulos, distribución de las variables y valores atípicos.
2. **Limpieza de la base:** eliminación de columnas, corrección de inconsistencias, tratamiento de valores extremos y codificación de variables.
3. **Hipótesis propias:** planteo y validación de la hipótesis univariada (A), bivariada (B) y multivariada (C).
4. **Hipótesis propuestas por la cátedra:** validación de las hipótesis a), b) y c).

El informe hace referencia explícita a estas secciones.
