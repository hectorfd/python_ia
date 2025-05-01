# Tipos de Machine Learning

Cada uno de estos Aprendizajes se asemejan en como aprenden los humanos

## 1. Aprendizaje Supervisado

Requiere de un conjunto de datos con características y la etiqueta correcta.

Ejem:

- Predicción de precio de casas

    - Que característica afectan el precio de una casa?

        - ... numero de baños, ... numero de cuartos

        - que tamaño(m²) tiene la alberca?

        - seguro hay mas características importantes

##### Datos
Cada casa(una fila con caracteristicas) cuenta con su etiqueta(respuesta). en este caso, es el precio

| Baños | Cuartos | Tamaño (m²) | ¿Tiene alberca? | Precio     |
|-------|---------|-------------|------------------|------------|
| 2     | 3       | 400         | No               | \$50,000   |
| 3     | 4       | 500         | Sí               | \$65,000   |
| 3     | 5       | 500         | Sí               | \$80,000   |
| 1     | 2       | 250         | No               | \$34,000   |
`El aprnedizaje supervisado puede utilizarse para Regresión y Clasificación`
##### Modelos
__Regresión__ -> puede predecir un dato numérico continuo
__Clasificación__ -> Predecir la categoría correcta

### 🔥 **Ejemplos:

#### 1. **Predicción de Precios de Viviendas** (Regresión)

- **Objetivo**: Predecir el precio de una casa.
    
- **Features**:
    
    - Metros cuadrados, número de baños, ubicación, antigüedad, etc.
        
- **Algoritmos**: Regresión lineal, Random Forest, XGBoost.
    

#### 2. **Detección de Spam en Emails** (Clasificación)

- **Objetivo**: Clasificar emails como "spam" o "no spam".
    
- **Features**:
    
    - Frecuencia de palabras ("oferta", "ganador"), estructura del correo.
        
- **Algoritmos**: Naive Bayes, SVM, Redes Neuronales.
    
#### 3. **Diagnóstico Médico** (Clasificación)

- **Objetivo**: Predecir si un paciente tiene diabetes (Sí/No).
    
- **Features**:
    
    - Niveles de glucosa, IMC, edad, presión arterial.
        
- **Algoritmos**: Regresión logística, Árboles de decisión.
    
#### 4. **Recomendación de Productos** (Clasificación/Regresión)

- **Objetivo**: Predecir si un usuario comprará un producto (ej: Netflix, Amazon).
    
- **Features**:
    
    - Historial de compras, búsquedas, demografía.
        
- **Algoritmos**: Sistemas de filtrado colaborativo, Matrix Factorization.
    

#### 5. **Predicción de Fallos en Máquinas** (Clasificación)

- **Objetivo**: Predecir si una máquina fallará en los próximos 7 días.
    
- **Features**:
    
    - Vibración, temperatura, horas de uso.
        
- **Algoritmos**: Random Forest, Gradient Boosting.
    

#### 6. **Análisis de Sentimiento** (Clasificación)

- **Objetivo**: Clasificar reseñas como "positivas", "negativas" o "neutrales".
    
- **Features**:
    
    - Palabras usadas, puntuación, contexto.
        
- **Algoritmos**: NLP con BERT, LSTM, SVM.
    

#### 7. **Predicción de Ventas** (Regresión)

- **Objetivo**: Predecir ventas mensuales de un producto.
    
- **Features**:
    
    - Publicidad, temporada, precios históricos.
        
- **Algoritmos**: ARIMA, Prophet, Redes Neuronales.
    

#### 8. **Reconocimiento de Dígitos Escritos** (Clasificación)

- **Objetivo**: Identificar dígitos (0-9) en imágenes.
    
- **Features**:
    
    - Pixeles de la imagen normalizados.
        
- **Algoritmos**: CNN (Redes Neuronales Convolucionales).

## 2. Aprendizaje no Supervisado

  Se requiere de datos sin etiquetas, El modelo busca patrones y relaciones
Segmentación de clientes
- podemos crear clusters o grupos de clientes, con los datos que tenemos?
##### Datos
podemos crear grupos de los datos que tenemos para hacer algo diferente con cada grupo
Con este resultado se puede hacer campañas para cada tipo de grupo la idea es convencerlos de comprar

#### **Grupos (Clusters) Propuestos**:

| **Cluster**                    | **Comportamiento**          | **Estrategia**              | **Técnica de Marketing**             |
| ------------------------------ | --------------------------- | --------------------------- | ------------------------------------ |
| **1. Compradores Leales**      | Visitan mucho, gastan mucho | Retener y fidelizar         | Programas VIP, descuentos exclusivos |
| **2. Compradores Ocasionales** | Visitan poco, gastan mucho  | Incrementar frecuencia      | Cupones por visita recurrente        |
| **3. Exploradores**            | Visitan mucho, gastan poco  | Convertirlos en compradores | Muestras gratis, novedades           |
| **4. Inactivos**               | Visitan poco, gastan poco   | Reactivación                | Ofertas agresivas, recordatorios     |

### 🔥 **Ejemplos :
#### 📌 **1. Segmentación de Clientes**

**Para qué sirve**: Agrupar clientes por comportamiento (compras, frecuencia de visita) y crear campañas personalizadas.

#### 📌 **2. Detección de Anomalías**

**Para qué sirve**: Identificar fraudes en transacciones o fallos en equipos industriales (patrones raros).

#### 📌 **3. Organización de Documentos**

**Para qué sirve**: Clasificar textos automáticamente (ej: emails, reseñas) por temas sin etiquetas previas.
## 3. Aprendizaje por Refuerzo

Un agente aprende en un ambiente por medio de acciones y retroalimentación

Jugar Ajedrez -> el agente realiza una acción y cambia el estado del ambiente. se premia o reprende al modelo con un puntaje numérico
EL modelo busca tomar acciones que le den mas puntos

`Cada accion cambia el ambiente dando retroalimentación constante` -> el robot puede mover algo del ambiente.
En ajedrez, cambia el estado del tablero. Con cada acción se debe re-evaluar.

### 🔥 **Ejemplos :

#### 📌 **Ejemplo 1: Ajedrez (como mencionaste)**

|**Componente**|**Descripción**|
|---|---|
|**Ambiente**|Tablero de ajedrez.|
|**Acción**|Mover una pieza (ej: "Peón a E4").|
|**Retroalimentación**|+1 por capturar una pieza, +10 por jaque mate, -1 por perder una pieza.|
|**Objetivo**|Maximizar puntos ganando partidas.|

---

#### 📌 **Ejemplo 2: Robot en Almacén**

|**Componente**|**Descripción**|
|---|---|
|**Ambiente**|Almacén con paquetes dispersos.|
|**Acción**|Mover brazos robóticos para levantar/transportar paquetes.|
|**Retroalimentación**|+5 por colocar un paquete correctamente, -2 por golpear algo, -10 por caída.|
|**Objetivo**|Optimizar tiempo y minimizar errores en la logística.|

---

#### 📌 **Ejemplo 3: Videojuegos (ej: Super Mario)**

|**Componente**|**Descripción**|
|---|---|
|**Ambiente**|Nivel del juego con enemigos y plataformas.|
|**Acción**|Saltar, correr, agacharse.|
|**Retroalimentación**|+100 por llegar al final, -1 por cada segundo, -50 por morir.|
|**Objetivo**|Completar el nivel con la máxima puntuación.|

---

### 🔍 **Patrón Común (Resumen)**

1. **Ambiente**: Mundo donde actúa el agente (físico o digital).
    
2. **Acción**: Movimiento o decisión que cambia el ambiente.
    
3. **Recompensa**: Puntaje numérico que guía el aprendizaje.
    
4. **Meta**: Maximizar recompensas acumuladas.
    

**¿Para qué sirve?** Desde autos autónomos hasta publicidad personalizada.