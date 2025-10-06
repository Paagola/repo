# Ejercicios de Lenguajes de Marcas

Este repositorio contiene la resolución de los ejercicios sobre **lenguajes de marcas**.  Cada enunciado se presenta como una sección con su respuesta en texto y, cuando corresponde, se incluye un enlace a la solución en formato XML junto con su definición de tipo de documento (DTD) dentro del directorio [`src`](./src).

Para dar una mejor explicación de los ejercicios y una mejora visual al `Readme.md` me he apoyado de la IA, pero estos ejercicios los he hecho completamente yo.


---

## Ejercicio 1

**Enunciado**

> Lee el siguiente listado y marca cuáles son características propias de los lenguajes de marcas:
>
> 1. Están basados en etiquetas o marcas.
> 2. Se utilizan únicamente para programar algoritmos matemáticos.
> 3. Son legibles tanto por personas como por máquinas.
> 4. Permiten estructurar la información.
> 5. Solo sirven para diseñar páginas web.

**Respuesta**

Un lenguaje de marcas se caracteriza por emplear etiquetas para estructurar contenido de manera que sea comprensible tanto por seres humanos como por ordenadores.  Las opciones correctas son:

- **Están basados en etiquetas o marcas.**
- **Son legibles tanto por personas como por máquinas.**
- **Permiten estructurar la información.**


---

## Ejercicio 2

**Enunciado**

> Explica dos ventajas principales de usar XML frente a un formato propietario (como un archivo .docx o .xlsx) para intercambiar datos entre dos aplicaciones de software diferentes.

**Respuesta**

1. **Interoperabilidad universal:** XML es texto plano, por lo que cualquier programa puede leerlo o generarlo sin necesidad de licencias o software específico.  Al ser legible tanto por personas como por máquinas, facilita el análisis y la depuración.
2. **Estructura clara y extensible:** permite definir etiquetas propias para describir la información con precisión.  De esta forma, los sistemas que intercambian datos pueden acordar un esquema común y validar que los documentos cumplan esa estructura.

---

## Ejercicio 3

**Enunciado**

> Clasifica los siguientes lenguajes de marcas según el tipo: HTML, SVG, LaTeX, XML, MathML, Markdown.

**Respuesta**

| Tipo                        | Lenguajes                                                       |
|-----------------------------|-----------------------------------------------------------------|
| **Lenguajes de presentación** | HTML, MathML, Markdown                                          |
| **Lenguajes de datos**        | XML                                                            |
| **Lenguajes especializados**   | SVG, MathML, LaTeX                                             |

---

## Ejercicio 4

**Enunciado**

> Relaciona cada lenguaje de marcas con su ámbito de aplicación:
>
> 1. HTML
> 2. SVG
> 3. MathML
> 4. GML
> 5. RSS
>
> a) Descripción de datos geográficos
> b) Creación de fórmulas matemáticas
> c) Publicación de contenidos sindicados (noticias, blogs)
> d) Representación de páginas web
> e) Imágenes vectoriales escalables

**Respuesta**

| Lenguaje | Ámbito de aplicación                                      |
|----------|-----------------------------------------------------------|
| **HTML** | d) Representación de páginas web                          |
| **SVG**  | e) Imágenes vectoriales escalables                        |
| **MathML** | b) Creación de fórmulas matemáticas                     |
| **GML**  | c) Publicación de contenidos sindicados (noticias, blogs) |
| **RSS**  | a) Descripción de datos geográficos                       |

---

## Ejercicio 5

**Enunciado**

> Una empresa necesita intercambiar facturas electrónicas entre un sistema de gestión y una aplicación de contabilidad. ¿Por qué XML es adecuado para este caso y no un lenguaje de presentación como HTML?

**Respuesta**

XML está diseñado para intercambiar información estructurada entre plataformas.  Al describir los datos de forma independiente de su presentación, permite que ambos sistemas interpreten el contenido de manera fiable y valida su estructura mediante DTD o XSD.  HTML, por el contrario, se centra en cómo se presenta la información y no ofrece garantías de estructura ni validación, por lo que no es idóneo para el intercambio automatizado de datos.

---

## Ejercicio 6

**Enunciado**

> Di si las siguientes afirmaciones son verdaderas (V) o falsas (F):
>
> a) XML tiene etiquetas predefinidas como `<body>` o `<table>`.
>
> b) XML permite crear etiquetas definidas por el usuario.
>
> c) XML distingue entre mayúsculas y minúsculas en sus etiquetas.
>
> d) Un documento XML debe tener siempre una única etiqueta raíz.

**Respuesta**

| Afirmación | Valor | Comentario                                            |
|------------|------|------------------------------------------------------|
| a) XML tiene etiquetas predefinidas como `<body>` o `<table>`. | **F**  | 
| b) XML permite crear etiquetas definidas por el usuario.         | **V**  |
| c) XML distingue entre mayúsculas y minúsculas en sus etiquetas. | **V**  | 
| d) Un documento XML debe tener siempre una única etiqueta raíz.    | **V**  | 

---

## Ejercicio 7

**Enunciado**

> Corrige el siguiente documento XML para que sea bien formado:
>
> ```xml
> <libros>
>     <libro id=1
>         <titulo>El Quijote</titulo>
>         <autor>Cervantes</autor>
>     </libro>
>     <libro id=”2”>
>         <titulo>Cien años de soledad</titulo>
>         <autor>García Márquez</autor>
>     </libro>
> </libros>
> ```

**Respuesta**

El documento debe tener atributos con valores entrecomillados, cierre de etiquetas correcto y una declaración opcional de tipo de documento.  La solución completa está en
 [`src/ejercicio7`](./src/ejercicio7) y [`ejercicio7.dtd`](./src/ejercicio7/ejercicio7.dtd) define su estructura.

---

## Ejercicio 8

**Enunciado**

> Indica cuál de los siguientes documentos XML está bien formado y cuál no, justificando:
>
> **Documento A**
>
> ```xml
> <persona>
>   <nombre>Ana</nombre>
>   <edad>25</edad>
> </persona>
> ```
>
> **Documento B**
>
> ```xml
>  <persona>
>    <nombre>Ana</Nombre>
>    <Edad>25</Edad>
>  </persona>
> ```
>

**Respuesta**

El Documento A respeta las reglas básicas de XML (elemento raíz único, etiquetas correctamente anidadas y atributos con valores entrecomillados).  El Documento B no es válido porque cierra una etiqueta con mayúsculas (`</Nombre>`) mientras que la apertura utiliza minúsculas (`<nombre>`).  XML diferencia entre mayúsculas y minúsculas, por lo que las etiquetas de apertura y cierre deben coincidir exactamente.

---

## Ejercicio 9

**Enunciado**

> Crea un documento XML que combine información de un catálogo de libros con metadatos Dublin Core, utilizando espacios de nombres.

**Respuesta**

Se ha creado un documento XML denominado **`ejercicio9.xml`** que declara el espacio de nombres Dublin Core (`xmlns:dc="http://purl.org/dc/elements/1.1/"`) y utiliza los elementos `dc:title`, `dc:creator`, `dc:publisher` y `dc:date` para describir cada libro:

- [`ejercicio9.xml`](./src/ejercicio9/ejercicio9.xml) — contiene el catálogo de libros con metadatos.
- [`ejercicio9.dtd`](./src/ejercicio9/ejercicio9.dtd) — describe la estructura del documento y define las etiquetas con prefijo `dc`.

---

## Ejercicio 10

**Enunciado**

> Diseña un documento XML que represente una agenda de contactos con al menos 2 contactos.  Debe:
>
>  • Estar bien formado.
> 
>  • Incluir atributos en algún elemento.
> 
>  • Usar un espacio de nombres para los datos de dirección.

**Respuesta**

La agenda se ha modelado como un elemento raíz `agenda` con un prefijo de espacio de nombres `g`.  Cada teléfono (`g:telefono`) incluye un atributo `id` y contiene varias entradas de contacto (`g:contacto1`, `g:contacto2`, etc.) con sus respectivos números (`g:tlf`).  Para revisar el código y su definición de tipo de documento visita:

- [`agenda.xml`](./src/ejercicio10/agenda.xml)
- [`agenda.dtd`](./src/ejercicio10/agenda.dtd)

---

## Ejercicio 11

**Enunciado**

> Elabora y puebla con datos un documento XML bien formado basándote en los siguientes supuestos.  El nombre del archivo generado deberá llamarse **banco.xml**.
>
>  a. El banco tiene sucursales, cada una de ellas identificadas por un código.
> 
>  b. Cada sucursal tiene asignadas una serie de cuentas corrientes, que igualmente se identifican mediante un código.
> 
>  c. La cuenta tiene asignados uno o varios clientes.

**Respuesta**

Se ha creado el archivo **`banco.xml`** que refleja la jerarquía indicada: el elemento raíz `banco` contiene varias `sucursal` con atributo `codigo`.  Cada `sucursal` agrupa varias `cuenta`, y cada `cuenta` contiene uno o más elementos `cliente` con atributos `id` y subelementos `nombre` y `dni` para identificar a los titulares.

**Ejercicio:** [`src/ejercicio11`](./src/ejercicio11):

- [`banco.xml`](./src/ejercicio11/banco.xml)
- [`banco.dtd`](./src/ejercicio11/banco.dtd)

---
