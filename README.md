# Limpieza de Base de Contactos (Python)

Este proyecto muestra un proceso completo y reproducible para limpiar una base de datos de contactos donde toda la información venía 
mezclada en una sola columna.

El objetivo es transformar datos caóticos en un dataset estructurado con columnas claras: name, role, city y email.

## Pipeline de limpieza aplicado
1. Extracción y normalización del correo
- Unificación de variantes de gmail.com
- Extracción del email limpio
- Eliminación del email del texto original

2. Limpieza general del texto
- Eliminación de tabuladores, comas, guiones y caracteres repetidos
- Reemplazo de _ por espacio
- Normalización de espacios
- Separación de palabras pegadas 

3. Tokenización
- Conversión del texto limpio en lista de palabras
- Preparación para clasificación

4. Diccionarios de referencia
- Lista de ciudades encontradas en el archivo
- Lista de roles y palabras clave
- Diccionario para estandarizar variaciones (ej. ProductOwner → Product Owner)

5. Clasificación de tokens
Cada palabra se clasifica automáticamente en: City, Role y Name

6. Construcción de columnas finales
- name desde palabras no clasificadas como rol o ciudad
- role desde palabras clave detectadas
- city desde la coincidencia exacta
- Reconstrucción ordenada del registro

7. Correcciones manuales mínimas en escel 

8. Validación
- Revisión de nulos
- Revisión de consistencia por columnas

Dataset listo para uso

## Archivos principales del repositorio
- notebook.ipynb → Notebook con todo el proceso de limpieza
- contacts_clean.csv → Archivo limpio en formato universal (CSV)
- Excel final con acabados mínimos manuales 

## Tecnologías
- Python 3
- Pandas
- Expresiones regulares (regex)
