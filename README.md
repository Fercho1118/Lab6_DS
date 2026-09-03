# Laboratorio 6 - Análisis de redes sociales en YouTube

CC3084 Data Science, Universidad del Valle de Guatemala, Semestre II 2026.
Fernando Rueda (23748) y Fernando Hernández (23645).

Análisis de participación en YouTube a partir de `youtube_videos.csv` (293 videos)
y `youtube_comments.csv` (406 comentarios). El trabajo cubre carga e integración,
limpieza y preprocesamiento, análisis exploratorio, y la red bipartita autor-video
con sus proyecciones, comunidades, centralidad y sentimiento.

## Requisitos y ejecución

```
python3.10 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python -m spacy download es_core_news_sm
jupyter nbconvert --to notebook --execute --inplace notebooks/lab6.ipynb
```

El notebook lee los dos CSV de la carpeta data/ y escribe los conjuntos procesados en
`salidas/` (no versionada). Los comentarios están en español, por lo que la
limpieza usa stopwords en español y lematización con spaCy.

## Contenido del notebook

1. Carga, comprensión e integración de los datos por `video_id`.
2. Calidad, limpieza y preprocesamiento, con `texto_original` y `texto_limpio`.
3. Análisis exploratorio: descriptivos, concentración de la participación, popularidad
   frente a participación, visualizaciones y respuestas a las preguntas del enunciado.
4. Red bipartita autor-video: construcción, tablas de nodos y aristas, y visualización
   de la red completa.

## Salidas generadas

El notebook escribe en `salidas/` (carpeta no versionada) los conjuntos procesados
`videos_procesado.csv`, `comentarios_procesado.csv` e `integrado.csv`, y las tablas de la
red `red_nodos.csv` y `red_aristas.csv`.
