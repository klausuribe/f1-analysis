# F1 Analysis

Proyecto de la asignatura **Módulo VII – Data Engineering** (Clase 4): pipeline de datos con datos de Fórmula 1 usando [FastF1](https://github.com/theOehrly/Fast-F1) y almacenamiento en Parquet.

## Estructura del repositorio

```
├── data/
│   ├── cache/     # Caché de FastF1 (sesiones descargadas)
│   └── raw/       # Archivos .parquet generados
├── scripts/
│   ├── extract.py # Extracción desde FastF1 → Parquet
│   └── load.py    # Carga / lectura de datos
├── utils.py       # Utilidades compartidas (rutas, configuración, etc.)
├── requirements.txt
└── README.md
```

## Requisitos

- Python 3.10+ (recomendado)
- Entorno virtual

## Instalación

```bash
cd f1-analysis
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

> **Nota:** `requirements.txt` se completará en el Paso 2 del curso (p. ej. `fastf1`, `pandas`, `pyarrow`).

## Uso (previsto)

1. Configurar rutas de caché y salida en `utils.py` (Paso 3).
2. Ejecutar la extracción: `python scripts/extract.py` (Paso 4).
3. Cargar datos con `scripts/load.py` según lo definas en el curso.

## Datos

- **Cache:** FastF1 guarda aquí las descargas para no repetir peticiones a la API.
- **Raw:** Parquet con tablas listas para análisis o etapas ETL posteriores.

## Licencia y créditos

Datos de carreras: propiedad de la FIA / Formula One; FastF1 es un cliente no oficial para fines educativos y de análisis.
