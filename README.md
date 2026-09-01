# 🚗 Restauración de Placas Vehiculares mediante Visión Computacional y OCR

Sistema de visión computacional desarrollado para la **restauración y reconocimiento de placas de rodaje de vehículos menores en imágenes desenfocadas**, utilizando técnicas de procesamiento digital de imágenes, segmentación y reconocimiento óptico de caracteres (OCR).

Proyecto desarrollado para el curso **Procesamiento Digital de Señales II** de la **Universidad Nacional de Piura**.

---

# 📌 Descripción del proyecto

El objetivo del proyecto es desarrollar un sistema capaz de recuperar información de placas vehiculares afectadas por:

- Desenfoque de movimiento.
- Baja resolución.
- Inclinación de perspectiva.
- Variaciones de iluminación.

El software implementa un flujo completo de procesamiento:

1. Localización de la placa vehicular.
2. Corrección geométrica mediante transformación de perspectiva.
3. Restauración de imagen utilizando filtro Wiener.
4. Mejora visual mediante técnicas de realce.
5. Segmentación de caracteres.
6. Reconocimiento mediante OCR.
7. Validación del resultado mediante reglas de formato de matrícula.

---

# ⚙️ Características principales

✅ Detección automática de placas mediante segmentación HSV.

✅ Selección manual mediante cuatro puntos cuando la detección automática falla.

✅ Corrección de perspectiva para placas inclinadas.

✅ Restauración mediante deconvolución Wiener.

✅ Mejora de contraste utilizando CLAHE.

✅ Binarización y procesamiento morfológico.

✅ Extracción y análisis de caracteres.

✅ Reconocimiento OCR mediante EasyOCR.

✅ Validación inteligente de formatos de placas.

✅ Exportación de resultados a archivos Excel.

---

# 🏗️ Arquitectura del sistema

El sistema presenta una arquitectura modular donde cada etapa del procesamiento se encuentra separada:
Imagen de entrada
|
↓
Carga y normalización
|
↓
Detección de placa
|
↓
Corrección de perspectiva
|
↓
Restauración Wiener
|
↓
Mejora de contraste
|
↓
Segmentación
|
↓
OCR
|
↓
Validación
|
↓
Resultado final

---

# 🛠️ Tecnologías utilizadas

## Lenguaje

- Python 3.13

## Librerías principales

- OpenCV
- NumPy
- Pillow
- Pandas
- OpenPyXL
- EasyOCR
- RawPy
- Tkinter

---

# 📂 Estructura del proyecto
Restauracion-Placas-Vehiculares-OCR/

│
├── app.py
│ └── Interfaz gráfica y control principal
│
├── utils/
│
│ ├── auto_crop.py
│ ├── roi.py
│ ├── restoration.py
│ ├── segmentation.py
│ ├── ocr_utils.py
│ ├── validation.py
│ ├── pipeline.py
│ ├── excel_report.py
│ └── debug_tools.py
│
├── resultados/
│
│ ├── debug/
│ └── reports/
│
├── Informe_Proyecto_Restauracion_Placas_OCR.pdf
│
└── README.md

---

# 🧩 Descripción de módulos

| Archivo | Función |
|---------|---------|
| app.py | Interfaz gráfica, carga de imágenes y ejecución del flujo |
| auto_crop.py | Detección automática de regiones de placa |
| roi.py | Ordenamiento de puntos y transformación de perspectiva |
| restoration.py | Restauración mediante filtro Wiener |
| segmentation.py | Binarización y extracción de caracteres |
| ocr_utils.py | Reconocimiento mediante OCR |
| validation.py | Validación de formatos de matrícula |
| pipeline.py | Coordinación del procesamiento completo |
| excel_report.py | Generación de reportes |

---

# 📊 Evaluación del sistema

El sistema fue probado con **12 fotografías propias de vehículos menores capturadas en vías públicas de Piura, Castilla y Veintiséis de Octubre**.

Resultados obtenidos:

| Indicador | Resultado |
|-----------|-----------|
| Imágenes evaluadas | 12 |
| Coincidencias exactas | 12 |
| Errores de placa completa | 0 |
| Exactitud observada | 100% |
| Detección automática HSV | 58.3% |
| Selección manual | 41.7% |

---

# 🖥️ Flujo de procesamiento

El usuario puede:

1. Cargar una imagen del vehículo.
2. Ejecutar detección automática de placa.
3. Realizar selección manual si es necesario.
4. Visualizar las etapas intermedias:
   - ROI detectada.
   - Imagen restaurada.
   - Segmentación.
   - Caracteres extraídos.
   - Resultado OCR.
5. Guardar el resultado obtenido.

---

# 📷 Evidencias del proyecto

El repositorio contiene:

- Código fuente completo.
- Imágenes de pruebas.
- Resultados intermedios del procesamiento.
- Reportes generados.
- Informe técnico del proyecto.

---

# 🚀 Instalación

Clonar el repositorio:

```bash
git clone https://github.com/jerssonpingo/Restauracion-Placas-Vehiculares-OCR.git
Ingresar a la carpeta:
cd Restauracion-Placas-Vehiculares-OCR
Instalar dependencias:
pip install -r requirements.txt
Ejecutar la aplicación:
python app.py

📄 Informe técnico

El informe completo del proyecto se encuentra dentro del repositorio:

Informe_Proyecto_Restauracion_Placas_OCR.pdf

👨‍💻 Autor
Jersson Yair Pingo Umbo

Estudiante de Ingeniería Electrónica y Telecomunicaciones
Universidad Nacional de Piura

Áreas de interés:

Visión computacional.
Procesamiento digital de señales.
Sistemas embebidos.
Redes y telecomunicaciones.
Inteligencia artificial aplicada.
