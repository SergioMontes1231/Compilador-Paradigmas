Proyecto: Analizador Léxico y Sintáctico con Interfaz Gráfica

Descripción

Este proyecto consiste en la implementación de un analizador léxico y sintáctico desarrollado en Python. El sistema permite analizar código fuente escrito en un lenguaje determinado (adaptado posteriormente para Java), generar los tokens correspondientes, construir un Árbol de Sintaxis Abstracta (AST) y visualizar los resultados mediante una interfaz gráfica desarrollada con Tkinter.

El programa permite cargar archivos de código fuente, analizarlos y mostrar tanto los tokens detectados como la estructura del AST generada.

El proyecto se diseñó de forma modular, separando las diferentes fases del compilador en carpetas independientes para facilitar el trabajo colaborativo y la organización del código.

---

Estructura del Proyecto

La estructura del repositorio está organizada de la siguiente manera:

compiler_project/
│
├── main.py
│
├── compiler/
│   ├── lexer/
│   │   ├── token_type.py
│   │   ├── token.py
│   │   └── lexical_analyzer.py
│   │
│   ├── parser/
│   │   ├── syntax_error.py
│   │   └── syntax_analyzer.py
│   │
│   └── ast/
│       ├── base_nodes.py
│       ├── expressions.py
│       └── statements.py
│
├── gui/
│   ├── app.py
│   ├── file_loader.py
│   └── ast_visualizer.py
│
├── utils/
│   └── ast_printer.py
│
└── examples/
    └── ejemplo1.txt

---

Descripción de los Componentes

main.py

Es el punto de entrada del programa.
Se encarga de iniciar la aplicación y ejecutar la interfaz gráfica.

---

Carpeta "compiler"

Contiene los componentes principales del compilador.

lexer

Implementa el analizador léxico, encargado de convertir el código fuente en una secuencia de tokens.

Archivos:

- token_type.py
  Define los diferentes tipos de tokens mediante una enumeración.

- token.py
  Define la estructura de un token (tipo, valor, línea y columna).

- lexical_analyzer.py
  Implementa el analizador léxico que utiliza expresiones regulares para reconocer tokens.

---

parser

Implementa el analizador sintáctico, encargado de interpretar la secuencia de tokens y construir el AST.

Archivos:

- syntax_error.py
  Define una excepción personalizada para errores de sintaxis.

- syntax_analyzer.py
  Implementa el parser que analiza los tokens y construye el árbol sintáctico.

---

ast

Define los nodos del Árbol de Sintaxis Abstracta (AST).

Archivos:

- base_nodes.py
  Contiene las clases base para los nodos del AST.

- expressions.py
  Define los nodos relacionados con expresiones (operaciones, literales, identificadores, llamadas a función).

- statements.py
  Define los nodos relacionados con sentencias (asignaciones, condicionales, bucles, etc.).

---

Carpeta "gui"

Contiene la implementación de la interfaz gráfica usando Tkinter.

Archivos:

- app.py
  Define la ventana principal de la aplicación.

- file_loader.py
  Permite seleccionar y cargar archivos de código fuente desde el sistema.

- ast_visualizer.py
  Permite mostrar la estructura del AST generado.

---

Carpeta "utils"

Contiene funciones auxiliares utilizadas por el sistema.

Archivo:

- ast_printer.py
  Permite imprimir o recorrer el AST de forma legible.

---

Carpeta "examples"

Contiene archivos de ejemplo para probar el funcionamiento del analizador.

---

Funcionamiento del Sistema

El flujo general del programa es el siguiente:

Archivo de código fuente
        ↓
Analizador Léxico (Lexer)
        ↓
Lista de Tokens
        ↓
Analizador Sintáctico (Parser)
        ↓
Construcción del AST
        ↓
Visualización en la interfaz gráfica

---

Interfaz Gráfica

La aplicación incluye una interfaz gráfica desarrollada con Tkinter que permite:

- Cargar archivos de código fuente.
- Mostrar el código cargado.
- Ejecutar el análisis léxico.
- Visualizar los tokens generados.
- Mostrar el Árbol de Sintaxis Abstracta (AST).

Esto facilita
