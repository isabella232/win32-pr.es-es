---
description: El predicado FREETEXT forma parte de la cláusula WHERE y permite buscar palabras y frases en columnas de texto.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Predicado FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808941"
---
# <a name="freetext-predicate"></a>Predicado FREETEXT

El predicado FREETEXT forma parte de la cláusula [Where](-search-sql-where.md) y permite buscar palabras y frases en columnas de texto. Use el predicado FREETEXT para buscar documentos que contengan combinaciones de las palabras de búsqueda que se distribuyen a lo largo del contenido o de las columnas especificadas. Para obtener el valor de rango, incluya System. Search. Rank, que es una clasificación de relevancia, como una columna en la instrucción SELECT.

El predicado FREETEXT tiene la siguiente sintaxis:


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



La referencia de columna fulltext es opcional. Con él, puede especificar una sola columna o un alias de [agrupación de columnas](-search-sql-with-as.md) en el que se prueba el predicado FREETEXT. Cuando la columna fulltext se especifica como "ALL" o " \* ", se busca en todas las propiedades de texto indizadas. Aunque no es necesario que la columna sea una propiedad de texto, los resultados podrían no tener sentido si la columna es algún otro tipo de datos. El nombre de la columna puede ser un [identificador](-search-sql-identifiers.md)normal o delimitado, y debe separarlo de la condición mediante una coma. Si no se proporciona ninguna condición de texto completo, se usa la columna de contenido, que es el cuerpo del documento.

Puede especificar una configuración regional de búsqueda para identificar el separador de palabras y las formas con inflexión adecuadas para la consulta de búsqueda. Los valores de configuración regional válidos son un identificador de código de idioma (LCID) estándar de Windows. Por ejemplo, 1033 es el LCID para Estados Unidos-English. Coloque el LCID como el último elemento dentro de los paréntesis de la cláusula FREETEXT. Para obtener información importante acerca de la búsqueda y los lenguajes, consulte [uso de búsquedas localizadas](-search-sql-usinglocsearches.md).

> [!Note]  
> La configuración regional de búsqueda predeterminada es la configuración regional predeterminada del sistema.

 

Debe incluir la parte de la condición FREETEXT entre comillas simples y debe estar formada por uno o varios términos de búsqueda. El predicado FREETEXT no admite operaciones lógicas. Para buscar una frase como si fuera una sola palabra, incluya la frase entre comillas dobles.

Cuando se usa el predicado FREETEXT, los resultados de la consulta de búsqueda devuelven documentos que contienen todos los términos de búsqueda. No es necesario que los términos aparezcan en ningún orden concreto. Los documentos que contienen más de los términos de búsqueda tienen valores de columna de rango más altos.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se buscan documentos que contengan "equipo", "software", "hardware" o combinaciones de esas palabras:


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> No se puede usar la coincidencia de palabra única y la coincidencia de frases en el mismo predicado FREETEXT.

 

Al realizar consultas con contrataciones, debe usar el carácter de escape de la comilla en la contracción cuando use FREETEXT, pero no cuando use Contains.

Por ejemplo, se produce un error en la siguiente sintaxis:


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



La sintaxis correcta incluye dos comillas simples, no una comilla doble.

La siguiente sintaxis se realiza correctamente:


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Predicado CONTAINS](-search-sql-contains.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



