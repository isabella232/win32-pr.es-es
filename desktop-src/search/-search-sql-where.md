---
description: La cláusula WHERE especifica las condiciones que determinan si un documento se incluye en los resultados devueltos por la consulta.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Cláusula WHERE (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e711219ff8eea81e8c4f8fd8145baccc35f49389d412f0e4ac088aa06666643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462407"
---
# <a name="where-clause-windows-search"></a>Cláusula WHERE (Windows Search)

La cláusula WHERE especifica las condiciones que determinan si un documento se incluye en los resultados devueltos por la consulta. En el nivel más alto, hay dos partes en la sintaxis de la cláusula WHERE:


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



El alias <grupo> parte de la cláusula simplifica las consultas complejas asignando un alias a un grupo de una o \_ varias columnas. Esto puede mejorar la legibilidad de las consultas complejas que buscan la misma información en varias columnas especificadas por las direcciones URL. Para obtener más información sobre los alias de grupo, [vea WITH -- AS Group Alias Predicate](-search-sql-with-as.md).

La parte de la cláusula WHERE es uno o varios predicados de búsqueda que especifican criterios <search condition> de coincidencia para la búsqueda. Los predicados de búsqueda son expresiones que declaran algún hecho sobre algún valor.

El resultado de una condición de búsqueda es un valor booleano, ya sea **TRUE** si el documento cumple las condiciones de búsqueda especificadas o **FALSE** si no lo hace. Si el resultado es **TRUE,** se devuelve el documento. Si el resultado es **FALSE,** no se devuelve el documento. A los documentos devueltos en una consulta de Microsoft Windows Search se les asignan valores de rango según el grado de coincidencia de las condiciones de búsqueda. Cada una de las condiciones de búsqueda de consultas puede incluir [una cláusula RANKBY](-search-sql-rankby.md) que admite la modificación de los valores de rango devueltos.

La [función ReuseWhere](-search-sql-reusewhere.md) hace que varias consultas que usan algunas de las mismas condiciones de búsqueda sea más eficaz. La cláusula WHERE de una consulta especifica el conjunto de elementos que coinciden en una consulta. Las consultas posteriores pueden compartir el trabajo realizado para la evaluación anterior mediante la función ReuseWhere de la nueva cláusula WHERE de consulta.

## <a name="search-predicates"></a>Predicados de búsqueda

Una condición de búsqueda consta de uno o varios predicados o condiciones de búsqueda que describen lo que el usuario busca (por ejemplo, WHERE System.DateCreated >'2006-04-19'). Los predicados de búsqueda se pueden combinar mediante los operadores lógicos **AND**, **OR** o **NOT**. El operador unario **opcional NOT** solo se puede usar con **AND** y solo para negar el valor lógico de un predicado o condición de búsqueda. Puede usar paréntesis para agrupar y anidar términos lógicos.

En la tabla siguiente se muestra el orden de prioridad de los operadores lógicos.



| Orden (prioridad) | Operador lógico |
|--------------------|------------------|
| Primero (más alto)    | **NOT**          |
| Segundo             | **AND**          |
| Tercero (más bajo)     | **OR**           |



 

Los operadores lógicos del mismo tipo son asociativos y no hay ningún orden de cálculo especificado. Por ejemplo, (A **AND** B) **AND** (C **AND** D) se puede calcular (A **AND** D) **AND** (B **Y** C) sin ningún cambio en el resultado lógico.

> [!IMPORTANT]
>
> Incorrecto: WHERE **NOT** CONTAINS ('equipo')
>
> Correcto: WHERE CONTAINS ('software') **Y NOT** CONTAINS ('equipo')

 

En consultas complejas, es posible que quiera hacer más énfasis en las coincidencias en algunas columnas que en otras. Por ejemplo, al buscar documentos que analicen el "diseño de software", es más probable que buscar el término de búsqueda en el título del documento sea una buena coincidencia que buscar las palabras individuales en el texto del documento. Para influir en la clasificación de documentos de esta manera, el lenguaje de consulta de Microsoft Windows Search admite la ponderación de las condiciones de búsqueda. Para obtener más información sobre la ponderación de columnas, vea [CONTAINS Predicate](-search-sql-contains.md) y [FREETEXT Predicate](-search-sql-freetext.md).

Hay tres grupos de predicados de búsqueda en Windows Search: búsquedas de texto completo, texto no completo y profundidad de carpeta. Los predicados de búsqueda de texto completo suelen coincidir con el significado del contenido, el título y otras columnas, y admiten la coincidencia lingüística (por ejemplo, formularios de palabras alternativos, frases y búsqueda de proximidad). En cambio, los predicados de búsqueda que no son de texto completo coinciden con el valor de las columnas especificadas y no incluyen ningún procesamiento lingüístico especial, pero en varios casos ofrecen coincidencia de patrones basados en caracteres. Los predicados de profundidad de carpeta restringen el ámbito de búsqueda a una ruta de acceso especificada.

> [!Note]  
> Si la consulta devuelve un documento porque un predicado de texto no completo se evalúa como **TRUE** para ese documento, el valor de rango se calcula como 1000. El uso [de la función rank coercion](-search-sql-rankby.md) puede modificar el valor de rango.

 

En las tablas siguientes se describen los predicados de búsqueda de profundidad de texto completo, texto no completo y carpeta.



| Predicado de texto completo                  | Descripción                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | Admite búsquedas complejas de términos en columnas de texto del documento (por ejemplo, título o contenido). Puede buscar formas detalladas de los términos de búsqueda, probar la proximidad de los términos y realizar comparaciones lógicas. Los términos de búsqueda pueden incluir caracteres comodín. |
| [FREETEXT](-search-sql-freetext.md) | Busca documentos que coincidan con el significado de la frase de búsqueda. Las palabras relacionadas y frases similares coincidirán, con la columna rank calculada en función de la coincidencia del documento con la frase de búsqueda. Los términos de búsqueda no pueden incluir caracteres comodín.  |



 



| Predicado de texto no completo                                                    | Descripción                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | Los valores de columna se comparan mediante la coincidencia de patrones simples con caracteres comodín.                                                                                                    |
| [Comparación de valores literales](-search-sql-literalvaluecomparison.md)         | Los valores de columna se comparan con valores de cadena, fecha, marca de tiempo, numéricos y otros valores literales. Este predicado admite igualdad y desigualdades, como mayor que y menor que. |
| [Comparaciones multivalor (ARRAY)](-search-sql-multivaluedcomparisons.md) | Las columnas multivalor se comparan con una matriz de literales de varios valores.                                                                                                             |
| [NULL](-search-sql-null.md)                                               | Los valores de columna que no están definidos para el documento se pueden detectar mediante el predicado **NULL.**                                                                                    |



 



| Profundidad de la carpeta                             | Descripción                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Alcance](-search-sql-folderdepth.md)     | Realiza un recorrido profundo de la ruta de acceso especificada, incluida la carpeta específica y todas las subcarpetas. |
| [Directorio](-search-sql-folderdepth.md) | Realiza un recorrido superficial de la ruta de acceso especificada, buscando solo la carpeta específica.            |



 

## <a name="examples"></a>Ejemplos

Para obtener ejemplos de la cláusula WHERE, vea los temas de predicado individuales vinculados en la tabla anterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Función ReuseWhere](-search-sql-reusewhere.md)
</dt> <dt>

[Propiedades del conjunto de filas](-search-sql-rowset-properties.md)
</dt> <dt>

[FROM (Cláusula)](-search-sql-from.md)
</dt> <dt>

[Información general de la sintaxis de SQL búsqueda](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[WITH : predicado de alias de grupo de AS](-search-sql-with-as.md)
</dt> <dt>

[Predicados SCOPE y DIRECTORY](-search-sql-folderdepth.md)
</dt> <dt>

[Cláusula RANK BY](-search-sql-rankby.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



