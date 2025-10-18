# Clasificación de Delitos con Uso de Arma en la Ciudad de Buenos Aires

**Proyecto de Aprendizaje Automático – Clasificación Binaria**

Proyecto de Aprendizaje Automático enfocado en el desarrollo y evaluación de un modelo de **clasificación binaria**
para predecir si en un delito registrado en la Ciudad Autónoma de Buenos Aires (CABA) **se utilizó un arma**. 
El modelo utiliza variables contextuales como tipo de delito, barrio, franja horaria, uso de moto y otras características geográficas y temporales,
y está implementado en Python con las librerías **pandas**, **scikit-learn** y **matplotlib**.

---

## Dataset

**Nombre del archivo:** `delitos_2022.xlsx`

**Instancias:** 140.919 registros (delitos ocurridos en CABA durante el año 2022)

**Características clave (columnas):**

- `uso_arma`: **Variable objetivo**. Categórica binaria (`"SI"` / `"NO"`).
- `tipo` / `subtipo`: Categorías generales y específicas del delito (ej.: `"Robo"`, `"Hurto"`, `"Vialidad"`,`"Homicidios"`, `"Lesiones"`, `"Amenazas"`).
- `barrio`: Barrio de CABA donde ocurrió el delito (48 barrios únicos).
- `comuna`: Número de comuna (1 a 15).
- `franja`: Franja horaria del delito (0 a 23, donde 0 = medianoche–1 AM, ..., 23 = 11 PM–medianoche).
- `dia`: Día de la semana (ej.: `"LUN"`, `"MAR"`, ..., `"DOM"`).
- `mes`: Mes del año en texto (ej.: `"enero"`, `"febrero"`, etc.).
- `uso_moto`: Indicador binario (`"SI"` / `"NO"`) sobre el uso de motocicleta en el delito.
- `latitud` / `longitud`: Coordenadas geográficas del lugar del hecho.
- `anio`, `fecha`, `id-mapa`, `cantidad`: Metadatos del registro.

**Tipos de datos:**
- Categóricos: `uso_arma`, `tipo`, `subtipo`, `barrio`, `dia`, `mes`, `uso_moto`.
- Numéricos: `franja`, `comuna`, `latitud`, `longitud`, `cantidad`.
- Fecha: `fecha`.

---

## Origen del dataset

**Fuente oficial:** [Portal de Datos Abiertos – Ciudad de Buenos Aires](https://data.buenosaires.gob.ar/dataset/delitos)  
**Licencia:** Creative Commons Atribución 4.0 Internacional (CC BY 4.0)  
**Adquisición:** Los datos fueron descargados en formato `.xlsx` en abril de 2025, correspondientes al año completo **2022**.  
**Actualización:** El dataset se publica mensualmente por la Dirección General de Estadística y Censos del Gobierno de la Ciudad.
