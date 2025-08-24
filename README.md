# 📝 Tutorial: Script para Traducir Archivos VTT

> **¿Qué es este script?** Una herramienta automatizada para traducir archivos de subtítulos VTT del inglés al español usando Google Translate.

## 📋 Requisitos del Sistema

### 1. Python 3.6 o superior
El script está escrito en Python 3

### 2. Conexión a Internet
Necesaria para usar la API de Google Translate

### 3. Dependencias de Python
Se instalarán automáticamente

## 🔧 Instalación

### 1. Instalar dependencias
```bash
pip install googletrans==4.0.0rc1
```

### 2. Verificar la instalación
```bash
python3 --version
```

## 📁 Estructura de Carpetas

El script espera la siguiente estructura de carpetas:

```
📁 proyecto_traduccion/
├── 📄 traducir_vtt.py
├── 📁 entrada/
│   ├── 📄 video1.vtt
│   ├── 📄 video2.vtt
│   └── 📄 video3.vtt
└── 📁 salida/
    └── (aquí se guardarán los archivos traducidos)
```

⚠️ **Importante:** Si las carpetas `entrada` y `salida` no existen, el script las creará automáticamente.

## 🚀 Uso del Script

### Método 1: Ejecución directa
```bash
python3 traducir_vtt.py
```

### Método 2: Ejecución con permisos de ejecución
```bash
chmod +x traducir_vtt.py
./traducir_vtt.py
```

## 📖 Ejemplo Completo de Uso

### 1. Preparar los archivos
Coloca tus archivos VTT en la carpeta `entrada/`

### 2. Ejecutar el script
```bash
python3 traducir_vtt.py
```

### 3. Ver el resultado
Los archivos traducidos aparecerán en la carpeta `salida/`

### Salida esperada en la consola:
```
Encontrados 3 archivos VTT para traducir

Procesando: entrada/video1.vtt
Traduciendo segmento 1/25...
Traduciendo segmento 2/25...
...
Archivo traducido guardado en: salida/video1.vtt
--------------------------------------------------
Procesando: entrada/video2.vtt
...

Proceso completado: 3/3 archivos traducidos exitosamente
```

## 🔍 Funcionalidades del Script

| Característica | Descripción |
|---------------|-------------|
| Traducción automática | Traduce del inglés al español usando Google Translate |
| Preservación de timestamps | Mantiene los tiempos exactos de los subtítulos originales |
| Procesamiento por lotes | Procesa múltiples archivos VTT automáticamente |
| Manejo de errores | Reintenta la traducción en caso de fallos temporales |
| Limpieza de texto | Elimina etiquetas HTML y caracteres problemáticos |

## ⚙️ Configuración Avanzada

### Modificar idiomas de traducción
Para cambiar los idiomas, edita la función `translate_text` en el script:

```python
# Cambiar esta línea en translate_text():
result = translator.translate(clean_text, src='en', dest='es')
```

### Parámetros disponibles:
- `src='en'` - Idioma de origen (inglés)
- `dest='es'` - Idioma de destino (español)

## 🛠️ Solución de Problemas

### Error: "La carpeta 'entrada' no existe"
**Solución:** Crea la carpeta `entrada` y coloca los archivos VTT en ella.
```bash
mkdir entrada
```

### Error: "googletrans module not found"
**Solución:** Instala la dependencia requerida.
```bash
pip install googletrans==4.0.0rc1
```

### Error de conexión de red
**Solución:** Verifica tu conexión a Internet y vuelve a intentar.

### Archivos no se traducen completamente
**Posible causa:** Límites de rate limiting de Google Translate.  
**Solución:** El script tiene pausas automáticas entre traducciones para evitar este problema.

## 📝 Notas Importantes

⚠️
- El script requiere conexión a Internet para funcionar
- Google Translate tiene límites de uso, por lo que se incluyen pausas automáticas
- Los archivos originales no se modifican, solo se crean versiones traducidas
- El script preserva toda la estructura temporal de los subtítulos

## 🎯 Casos de Uso Típicos

- **Traductores profesionales:** Para traducir subtítulos de videos
- **Creadores de contenido:** Para hacer contenido accesible en español
- **Estudiantes:** Para entender contenido en inglés
- **Empresas:** Para localizar contenido multimedia

## ✅ ¡El script está listo para usar!

Solo necesitas colocar tus archivos VTT en la carpeta `entrada` y ejecutar el script. Los archivos traducidos aparecerán automáticamente en la carpeta `salida`.

---

<p align="center">
  Tutorial creado para el script traducir_vtt.py<br>
  <em>Última actualización: Diciembre 2024</em>
</p>
