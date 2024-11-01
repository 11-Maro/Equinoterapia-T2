# Conjuntos de Tweets como Árboles Binarios de Búsqueda

## Departamento de TIC
### Computación y Estructuras Discretas II
### Tarea Integradora 2

---

## Índice

- [Descripción del Proyecto](#descripción-del-proyecto)
- [Resultados de Aprendizaje](#resultados-de-aprendizaje)
- [Estructura del Proyecto](#estructura-del-proyecto)
  - [Preparación](#preparación)
  - [Análisis y Diseño](#análisis-y-diseño)
  - [Primera Parte: Filtros](#primera-parte-filtros)
  - [Segunda Parte: Uniones](#segunda-parte-uniones)
  - [Tercera Parte: Ordenando Tweets por Influencia](#tercera-parte-ordenando-tweets-por-influencia)
  - [Cuarta Parte: Poniendo Todo en Marcha](#cuarta-parte-poniendo-todo-en-marcha)
  - [Quinta Parte: Cifrado de la Salida](#quinta-parte-cifrado-de-la-salida)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Autores](#autores)


---

## Descripción del Proyecto

Este proyecto tiene como objetivo representar conjuntos de tweets como **árboles binarios de búsqueda** utilizando **Scala** y aplicando el **paradigma funcional**. Se trabajará con un conjunto de datos de **X** (antes llamado Twitter) para comparar y procesar información producida en redes sociales.

Los tweets se representarán mediante la clase `Tweet`, que incluye los campos `user`, `text` y `retweets`. Se implementarán diferentes Tipos Abstractos de Datos (TADs) y se aplicarán buenas prácticas para crear y trabajar con estructuras inmutables.

## Resultados de Aprendizaje

- **Aplicar el paradigma funcional** en el análisis, diseño, evaluación, selección e implementación de algoritmos para solucionar problemas autocontenidos.
- **Aplicar conceptos fundamentales de la teoría de números** en el análisis de problemas computacionales, incluyendo el análisis de relaciones binarias, especialmente relaciones de equivalencia y de orden.
- **Comunicar ideas principales** sobre estructuras discretas o programación funcional utilizando vocabulario y lenguaje especializado.

## Estructura del Proyecto

### Preparación

- El proyecto se desarrolla utilizando **Desarrollo Guiado por Pruebas (TDD)**.
- Uso de un **repositorio Git** desde el inicio, con al menos **10 commits** distribuidos equitativamente.
- Los equipos están conformados por **2 a 3 integrantes** y deben registrarse en la [hoja de registro](#).

### Análisis y Diseño

- **Exploración del proyecto** y creación de un inventario de clases, traits y objetos.
- **Definición de TADs** para las estructuras de datos utilizadas, incluyendo representación, invariantes y especificación de operaciones.
- **Diagrama de Clases UML** para visualizar la estructura del proyecto.
- **Diseño e implementación de pruebas unitarias**, esenciales para la validación de las funcionalidades.

### Primera Parte: Filtros

Implementación de métodos para filtrar conjuntos de tweets:

- `def filter(p: Tweet => Boolean): TweetSet`
- `def filterAcc(p: Tweet => Boolean, acc: TweetSet): TweetSet`

Estos métodos permiten obtener subconjuntos de tweets que cumplen con un predicado específico.

### Segunda Parte: Uniones

Implementación del método para unir dos conjuntos de tweets:

- `def union(that: TweetSet): TweetSet`

Este método produce un nuevo conjunto que contiene todos los elementos de ambos conjuntos, sin duplicados.

### Tercera Parte: Ordenando Tweets por Influencia

Implementación de funcionalidades para ordenar los tweets según su número de retweets:

- `def mostRetweeted: Tweet`  
  Retorna el tweet más retuiteado del conjunto.
- `def descendingByRetweet: TweetList`  
  Retorna una lista de tweets ordenada de mayor a menor influencia.

### Cuarta Parte: Poniendo Todo en Marcha

Modificaciones en los objetos `GoogleVsApple` y `Main`:

- **Carga de Datos**: Utilización de `TweetReader.allTweets` para cargar un conjunto grande de tweets.
- **Filtrado de Tweets**: Definición de `googleTweets` y `appleTweets` usando las listas de palabras clave.
  - `lazy val googleTweets: TweetSet`
  - `lazy val appleTweets: TweetSet`
- **Análisis de Influencia**: Unión de los conjuntos y ordenamiento por influencia.
  - `lazy val trending: TweetList`
- **Determinación de Tendencias**: Respuesta a la pregunta sobre cuál plataforma genera más interés.
- **Salida de Datos**: Guardar resultados en `output.txt` y compararlos con otros grupos.

### Quinta Parte: Cifrado de la Salida

Implementación de una clase `RSA` para:

- **Cifrar y Decodificar** el contenido de `output.txt` utilizando el algoritmo RSA.
- **Generación de Archivos**: Guardar la salida cifrada en `cifrado.txt`.
- **Integración en el Diagrama de Clases** y pruebas unitarias.

## Tecnologías Utilizadas

- **Scala**: Lenguaje de programación funcional.
- **SBT (Simple Build Tool)**: Herramienta de construcción para Scala.
- **Git y GitHub Classroom**: Control de versiones y colaboración en equipo.
- **Herramientas UML**: Para el diseño del diagrama de clases.
- **Algoritmo RSA**: Para el cifrado y decodificación de archivos.

## Autores

- **[Nombre Integrante 1](#)**
- **[FABIO FELIPE MURILLO RIVAS](A00401131)**
- **[Nombre Integrante 3](#)**


