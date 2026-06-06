# Analizador Léxico y Sintáctico para un Subconjunto de Python

Este proyecto consiste en el desarrollo de una aplicación web interactiva que simula las fases iniciales de un compilador (Analizador Léxico y Analizador Sintáctico) diseñadas específicamente para un subconjunto representativo del lenguaje de programación Python. Desarrollado como proyecto práctico fundamental para el curso de Compiladores.

## Características del Sistema

### 1. Analizador Léxico (Lexer)
* **Máquina Discriminadora Determinista:** Escanea el código fuente carácter por carácter implementando el principio de *Maximal Munch*.
* **Mecanismo de Indentación Nativo:** Incorpora un sistema híbrido con pila para el rastreo de espacios al inicio de cada línea, inyectando de forma precisa los tokens virtuales `INDENT` y `DEDENT` característicos de Python.
* **Clasificación de Tokens:** Identifica Palabras Reservadas (Keywords), Identificadores, Literales (Enteros y Flotantes), Operadores (Aritméticos, de Asignación, Comparación y Bit a Bit) y Delimitadores.
* **Tabla de Símbolos:** Construcción dinámica de la tabla estructurada con los identificadores detectados y sus líneas de aparición.

### 2. Analizador Sintáctico (Parser)
* **Algoritmo Predictivo Descendente LL(1):** Procesa la corriente de tokens utilizando una gramática libre de contexto debidamente factorizada y libre de ambigüedades.
* **Árbol Sintáctico Interactivo:** Renderiza de forma jerárquica y visual la estructura del código analizado (AST) utilizando la librería **D3.js**, permitiendo hacer zoom y colapsar nodos.

### 3. Control de Errores Unificado
* El sistema discrimina y reporta de forma exacta el tipo de error (**LÉXICO** o **SINTÁCTICO**), indicando detalladamente el mensaje y el número de línea exacto donde se produjo la inconsistencia.

---

## Stack Tecnológico

* **Interfaz de Usuario:** Bootstrap 5.3 (Tema Oscuro estilo IDE)
* **Editor de Código:** CodeMirror 6 (Soporte integrado para numeración de líneas y resaltado de sintaxis)
* **Gráficos del Árbol:** D3.js v7 (Layout jerárquico interactivo)
* **Lógica del Compilador:** JavaScript ES6+ puro (Procesamiento directo en el cliente/navegador)

---

## Estructura del Proyecto

* `index.html`: Archivo principal unificado que contiene la estructura semántica de la interfaz web, las hojas de estilo personalizadas y los módulos JavaScript encargados de la tokenización, parsing y manipulación del DOM.

---

_Desarrollado con fines exclusivamente académicos para la simulación interactiva de las fases de la teoría de compiladores._
