# Proyecto de Estandarización y Geocodificación de Direcciones

Este repositorio contiene un script en Python (`main.py`) que permite:

- **Estandarizar direcciones**: Normaliza y formatea direcciones en mayúsculas, aplica abreviaturas y separa complementos.
- **Conversión de coordenadas**: Obtiene latitud y longitud de cada dirección usando la API de OpenCage Geocode.
- **Mejora de coordenadas**: Rellena coordenadas faltantes basándose en áreas o barrios.
- **Generación de mapas interactivos**: Crea mapas HTML con marcadores individuales y clusters.

---

## Requisitos

- Python 3.7+

### Usando pip:
```bash
pip install pandas folium opencage tkinter
```

### Usando conda (recomendado si usas Anaconda o Miniconda):
```bash
conda install -c conda-forge pandas folium opencage geocoder tk
```

- `pandas`: manipulación de datos.
- `folium`: visualización de mapas.
- `opencage-geocoder`: reverse geocoding.
- `tkinter`: selección de archivos vía GUI.

## Estructura de Directorios

```
├── original/                # Carpeta para el archivo de entrada (solo un Excel)
├── estandarizado/           # Resultados de la estandarización de direcciones
├── coordenadas/             # Salida con coordenadas obtenidas y mejoradas
├── mapas/                   # Mapas HTML generados
│   └── filtrados/           # Mapas con coordenadas filtradas
├── llave/                   # Archivo `llave.txt` con la API key de OpenCage
└── main.py                  # Script principal
```


## Uso

El script crea automáticamente la estructura de carpetas y permite seleccionar el archivo de direcciones en tiempo de ejecución; **no es necesario** configurar previamente un entorno virtual ni copiar manualmente el archivo de entrada.

1. **Ejecutar el script**
   ```bash
   python main.py
   ```
   - Si la carpeta `original/` está vacía, se abrirá un diálogo para elegir el archivo Excel con las direcciones.
   - El entorno (carpetas `original/`, `estandarizado/`, `coordenadas/`, `mapas/`, etc.) se genera automáticamente.
   - Verás un menú con 4 opciones:
     1. Estandarización de direcciones.
     2. Conversión de coordenadas.
     3. Mejora de coordenadas (requiere haber corrido la opción de conversión primero).
     4. Generación de mapas.

3. **Salida**
   - Archivos Excel en `estandarizado/` y `coordenadas/`.
   - Mapas HTML en `mapas/` y `mapas/filtrados/`.

## Documentación

Puedes consultar la documentación completa del proyecto en el siguiente enlace:

🔗 [Documentación del módulo `main.py`](https://felipe1727.github.io/Georeferenciaci-n-rea-Metropolitana/main.html)
