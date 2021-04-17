---
description: Las condiciones que determinan si un documento se incluye en los resultados devueltos por la consulta se especifican mediante la cláusula WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Cláusula WHERE (búsqueda de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686618"
---
# <a name="where-clause-windows-search"></a>Cláusula WHERE (búsqueda de Windows)

Las condiciones que determinan si un documento se incluye en los resultados devueltos por la consulta se especifican mediante la cláusula WHERE. En el nivel más alto, hay dos partes de la sintaxis de la cláusula WHERE:


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



La parte opcional <\_ alias de grupo> de la cláusula simplifica las consultas complejas asignando un alias a un grupo de una o varias columnas. Esto puede mejorar la legibilidad de las consultas complejas que buscan la misma información en varias columnas especificadas por las direcciones URL. Para obtener más información acerca de los alias de grupo, consulte [con el predicado de alias de grupo](-search-sql-with-as.md).

La <search condition> parte de la cláusula WHERE es uno o más predicados de búsqueda que especifican los criterios de coincidencia de la búsqueda. Los predicados de búsqueda son expresiones que imponen algún hecho sobre algún valor.

El resultado de una condición de búsqueda es un valor booleano, **true** si el documento cumple las condiciones de búsqueda especificadas, o bien **false** si no lo hace. Si el resultado es **true**, se devuelve el documento. Si el resultado es **false**, no se devuelve el documento. A los documentos devueltos en una consulta de búsqueda de Microsoft Windows se les asignan valores de clasificación según el grado de coincidencia de las condiciones de búsqueda. Cada una de las condiciones de búsqueda de consultas puede incluir una cláusula [RANKBY](-search-sql-rankby.md) que admite la modificación de los valores de rango devueltos.

La [función ReuseWhere](-search-sql-reusewhere.md) hace que varias consultas que usan las mismas condiciones de búsqueda sean más eficaces. La cláusula WHERE de una consulta especifica el conjunto de elementos que coinciden en una consulta. Las consultas posteriores pueden compartir el trabajo realizado para la evaluación anterior mediante el uso de la función ReuseWhere en la cláusula WHERE de la nueva consulta.

## <a name="search-predicates"></a>Predicados de búsqueda

Una condición de búsqueda consta de uno o varios predicados o condiciones de búsqueda que describen lo que busca el usuario (por ejemplo, donde System. DateCreated > ' 2006-04-19 '). Los predicados de búsqueda se pueden combinar mediante los operadores lógicos **and**, **or** o **Not**. El operador unario opcional **no** se puede usar solo con **y** y solo para negar el valor lógico de un predicado o una condición de búsqueda. Puede usar paréntesis para agrupar y anidar términos lógicos.

En la tabla siguiente se muestra el orden de prioridad de los operadores lógicos.



| Orden (precedencia) | Operador lógico |
|--------------------|------------------|
| Primero (más alto)    | **NOT**          |
| Segundo             | **AND**          |
| Tercer (el más bajo)     | **OR**           |



 

Los operadores lógicos del mismo tipo son asociativos y no hay ningún orden de cálculo especificado. Por ejemplo, (A **y** b) **y** (C **y** d) se pueden calcular (a **y** d) **y** (B **y** C) sin ningún cambio en el resultado lógico.

> [!IMPORTANT]
>
> Incorrecto: donde **no** contiene (' equipo ')
>
> Correcto: donde contiene (' software ') **y no** contiene (' equipo ')

 

En las consultas complejas, es posible que desee poner más énfasis en las coincidencias en algunas columnas que en otras. Por ejemplo, al buscar documentos que analizan "diseño de software", es más probable que buscar el término de búsqueda en el título del documento sea una buena coincidencia que buscar las palabras individuales en el texto del documento. Para influir en la clasificación de los documentos de esta manera, el lenguaje de consulta de Microsoft Windows Search admite la ponderación de las condiciones de búsqueda. Para obtener más información acerca de la ponderación de las columnas, vea [Contains](-search-sql-contains.md) Predicate y [FREETEXT Predicate](-search-sql-freetext.md).

Hay tres grupos de predicados de búsqueda en Windows Search: búsquedas de texto completo, de texto no completo y de profundidad de carpeta. Los predicados de búsqueda de texto completo suelen coincidir con el significado del contenido, el título y otras columnas, y admiten la coincidencia lingüística (por ejemplo, formas de palabras, frases y búsqueda de proximidad). En cambio, los predicados de búsqueda no de texto completo coinciden con el valor de las columnas especificadas y no incluyen ningún procesamiento lingüístico especial, pero en varios casos ofrecen coincidencia de patrones basada en caracteres. Los predicados de profundidad de carpeta restringen el ámbito de búsqueda a una ruta de acceso especificada.

> [!Note]  
> Si la consulta devuelve un documento porque un predicado que no es de texto completo se evalúa como **true** para ese documento, el valor de rango se calcula como 1000. El uso de la [función de conversión de rangos](-search-sql-rankby.md) puede modificar el valor de clasificación.

 

En las tablas siguientes se describen los predicados de búsqueda de texto completo, no completo y de profundidad de carpeta.



| Predicado de texto completo                  | Descripción                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | Admite búsquedas complejas de términos en columnas de texto de documento (por ejemplo, título, contenido). Puede buscar formas derivadas de los términos de búsqueda, probar la proximidad de los términos y realizar comparaciones lógicas. Los términos de búsqueda pueden incluir caracteres comodín. |
| [FREETEXT](-search-sql-freetext.md) | Busca documentos que coincidan con el significado de la frase de búsqueda. Las palabras relacionadas y las frases similares coincidirán, con la columna de rango calculada en función del grado de coincidencia del documento con la frase de búsqueda. Los términos de búsqueda no pueden incluir caracteres comodín.  |



 



| Predicado de texto no completo                                                    | Descripción                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | Los valores de columna se comparan usando la coincidencia de patrones simple con caracteres comodín.                                                                                                    |
| [Comparación de valores literales](-search-sql-literalvaluecomparison.md)         | Los valores de columna se comparan con cadenas, fechas, marcas de tiempo, números y otros valores literales. Este predicado admite igualdad y desigualdades, como mayor que y menor que. |
| [Comparaciones de varios valores (matriz)](-search-sql-multivaluedcomparisons.md) | Las columnas con varios valores se comparan con una matriz de literales de varios valores.                                                                                                             |
| [NULL](-search-sql-null.md)                                               | Los valores de columna no definidos para el documento se pueden detectar mediante el predicado **null** .                                                                                    |



 



| Profundidad de carpeta                             | Descripción                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [ID](-search-sql-folderdepth.md)     | Realiza un recorrido profundo de la ruta de acceso especificada, incluida la carpeta específica y todas las subcarpetas. |
| [Active](-search-sql-folderdepth.md) | Realiza un recorrido superficial de la ruta de acceso especificada, buscando solo en la carpeta específica.            |



 

## <a name="examples"></a>Ejemplos

Para obtener ejemplos de la cláusula WHERE, vea los temas de predicado individuales vinculados en la tabla anterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[ReuseWhere función)](-search-sql-reusewhere.md)
</dt> <dt>

[Propiedades del conjunto de filas](-search-sql-rowset-properties.md)
</dt> <dt>

[Cláusula FROM](-search-sql-from.md)
</dt> <dt>

[Información general de la sintaxis de búsqueda de SQL](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[CON el predicado de alias de grupo AS](-search-sql-with-as.md)
</dt> <dt>

[Predicados de ámbito y directorio](-search-sql-folderdepth.md)
</dt> <dt>

[RANK BY (cláusula)](-search-sql-rankby.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



