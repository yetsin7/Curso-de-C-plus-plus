# Curso de C++ — De cero a PRO

Guía completa de C++ desde los fundamentos hasta la programación moderna, con
enfoque en rendimiento, control de recursos y pensamiento técnico profundo.

Repositorio oficial: https://github.com/yetsin7/curso-de-cpp

---

## Para estudiantes de Nicaragua (y de toda Latinoamérica)

Hola. Si tú eres de Nicaragua, de Centroamérica o de cualquier país de habla
hispana, este libro fue pensado para ti. Aquí no necesitas pagar un curso caro
ni registrarte en ninguna plataforma: solo descargar el repositorio y empezar
a estudiar a tu ritmo, incluso sin conexión permanente a internet.

Este material está escrito en español claro y directo, con ejemplos prácticos
que puedes compilar y modificar. La idea es que cualquier persona con ganas de
aprender pueda llegar a dominar C++ de forma seria, sin atajos pero también
sin barreras.

## ¿Por qué existe este libro?

En Nicaragua y en muchos países de la región, el acceso a formación técnica
de calidad sigue siendo difícil: cursos costosos, libros caros, requisitos de
internet permanente o suscripciones mensuales. Este proyecto nace para
cambiar un poco esa realidad.

La misión es sencilla pero importante:

- Que **más nicaragüenses** puedan aprender a programar de forma profesional.
- Que el conocimiento de C++ esté disponible **gratis**, en español, para
  cualquier estudiante o autodidacta.
- Que no haga falta pagar, registrarse, ni depender de internet constante.
- Que cualquier persona, desde una computadora modesta, pueda formarse y
  competir con desarrolladores de cualquier parte del mundo.

Si este libro te ayuda, compártelo con otros estudiantes. Mientras más
nicaragüenses aprendan a programar, más fuerte será nuestra comunidad
técnica.

---

## ¿Para quién es este libro?

- Programadores con conocimientos básicos de cualquier lenguaje (Python, Java, etc.)
- Desarrolladores que ya saben C y quieren dar el salto a C++
- Estudiantes que quieren aprender C++ con ejemplos prácticos y compilables
- Autodidactas que estudian sin un profesor cerca y necesitan material claro

No se requiere experiencia previa en C++, pero sí ayuda conocer variables,
condicionales y bucles en cualquier lenguaje.

## Qué aprenderás

Este libro te ayudará a entender:

- cómo C++ extiende a C con abstracciones más potentes;
- cómo trabajar con objetos, memoria y recursos;
- cómo escribir software rápido sin perder claridad;
- cómo pensar el costo real de cada decisión técnica.

---

## Relación con software y hardware

C++ se usa mucho cuando importa el rendimiento porque te permite trabajar muy
cerca de la máquina, pero con herramientas más ricas que C. Eso significa que
muchos ejemplos te ayudarán a conectar:

- instrucciones del código;
- uso de CPU y memoria;
- costo de copias y referencias;
- vida útil de objetos y recursos.

## Cómo compilar los ejemplos

Todos los archivos `.cpp` se compilan con **g++** usando el estándar C++17:

```bash
# Compilación básica
g++ -std=c++17 -o programa archivo.cpp

# Con mensajes de advertencia (recomendado)
g++ -std=c++17 -Wall -Wextra -o programa archivo.cpp

# Capítulo 13 (usa SQLite3, requiere la librería instalada)
g++ -std=c++17 -o explorar 01_explorar_bd.cpp -lsqlite3
```

### Requisitos

- **g++** versión 7 o superior (incluido en GCC / MinGW en Windows)
- **SQLite3** (solo para el capítulo 13): `sudo apt install libsqlite3-dev` en Linux,
  o descargar las amalgamation headers en Windows.

---

## Estudiar sin internet (offline)

Una vez que clonas el repositorio, todo el contenido queda guardado en tu
computadora. Puedes estudiar sin conexión, en tu casa, en la universidad o
donde tengas acceso a una computadora.

```bash
git clone https://github.com/yetsin7/curso-de-cpp.git
cd curso-de-cpp
```

Cada capítulo tiene su propia carpeta con su `README.md` y archivos `.cpp`
listos para compilar y experimentar.

---

## Tabla de contenidos

| # | Capítulo | Temas principales |
|---|----------|-------------------|
| 01 | [Introducción](01-introduccion/README.md) | Hola mundo, cin/cout, namespaces, diferencias con C |
| 02 | [Variables y tipos](02-variables-y-tipos/README.md) | Tipos primitivos, auto, string, bool, nullptr, const, constexpr |
| 03 | [Operadores y expresiones](03-operadores-y-expresiones/README.md) | Aritméticos, lógicos, comparación, ternario, new/delete |
| 04 | [Control de flujo](04-control-de-flujo/README.md) | if/else, switch, while, for, range-for, break/continue |
| 05 | [Funciones](05-funciones/README.md) | Sobrecarga, referencias, parámetros por defecto, inline, lambdas |
| 06 | [POO — Clases](06-poo-clases/README.md) | Clases, objetos, constructores, destructores, encapsulación |
| 07 | [Herencia y polimorfismo](07-herencia-y-polimorfismo/README.md) | Herencia, virtual, override, final, clases abstractas |
| 08 | [Plantillas (Templates)](08-plantillas-templates/README.md) | Function templates, class templates, especialización |
| 09 | [STL — Contenedores](09-stl-contenedores/README.md) | vector, map, set, iteradores, algoritmos de `<algorithm>` |
| 10 | [Manejo de errores](10-manejo-de-errores/README.md) | try/catch/throw, std::exception, excepciones personalizadas |
| 11 | [Archivos e I/O](11-archivos-e-io/README.md) | ifstream, ofstream, fstream, stringstream |
| 12 | [C++11 Moderno](12-c++11-moderno/README.md) | auto, lambdas, smart pointers, move semantics, nullptr |
| 13 | [Proyecto Biblia](13-proyecto-biblia/README.md) | SQLite3 en C++, consultas reales a la BD de la Biblia |

---

## Base de datos de la Biblia

A partir del **capítulo 11**, algunos ejemplos usan la base de datos SQLite de la Biblia
Reina-Valera 1960, ubicada en:

```
../../datos/biblia_rv60.sqlite3
```

Esta ruta es relativa a cada subcarpeta de capítulo. Ver
[datos/README.md](datos/README.md) para detalles de uso y estructura de la BD.

---

## Estructura del proyecto

```
Curso de C++/
├── README.md                  ← Este archivo
├── datos/
│   └── README.md              ← Info sobre la BD de la Biblia
├── 01-introduccion/
├── 02-variables-y-tipos/
├── 03-operadores-y-expresiones/
├── 04-control-de-flujo/
├── 05-funciones/
├── 06-poo-clases/
├── 07-herencia-y-polimorfismo/
├── 08-plantillas-templates/
├── 09-stl-contenedores/
├── 10-manejo-de-errores/
├── 11-archivos-e-io/
├── 12-c++11-moderno/
└── 13-proyecto-biblia/
```

---

## Cómo apoyar este proyecto

Este libro es **100% gratuito**, **sin registro** y se puede usar **sin
internet** una vez clonado. La mejor manera de apoyarlo es ayudando a que
llegue a más estudiantes:

- Dale una estrella al repositorio en GitHub. Eso lo hace visible para más
  personas que están buscando aprender.
- Comparte el enlace con amigos, compañeros de clase, profesores o cualquier
  persona en Nicaragua o en Latinoamérica que quiera aprender a programar.
- Abre un issue si encuentras un error, una explicación poco clara o un
  ejemplo que no compile.
- Envía un pull request si quieres mejorar un capítulo, corregir un texto o
  proponer un nuevo ejemplo. Toda contribución cuenta.

Repositorio: https://github.com/yetsin7/curso-de-cpp

Mientras más nicaragüenses aprendamos a programar, más oportunidades vamos
a abrir para nuestra generación y para las que vienen. Gracias por estudiar,
compartir y contribuir.
