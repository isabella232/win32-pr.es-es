---
description: El predicado FREETEXT forma parte de la cláusula WHERE y admite la búsqueda de palabras y frases en columnas de texto.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Predicado FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9fb3d65c1b9dc72ef74c8c6862ccfb778ebbd4149b9e5bf5aca4d36674045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863411"
---
# <a name="freetext-predicate"></a>Predicado FREETEXT

El predicado FREETEXT forma parte de la [cláusula WHERE](-search-sql-where.md) y admite la búsqueda de palabras y frases en columnas de texto. Use el predicado FREETEXT para buscar documentos que contengan combinaciones de las palabras de búsqueda repartidas por el contenido o las columnas especificadas. Para obtener el valor de rango, incluya System.Search.Rank, que es una clasificación de recadencia, como una columna en la instrucción SELECT.

El predicado FREETEXT tiene la sintaxis siguiente:


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



La referencia de columna de texto completo es opcional. Con ella, puede especificar una sola columna o un alias de agrupación de [columnas](-search-sql-with-as.md) con el que se prueba el predicado FREETEXT. Cuando la columna de texto completo se especifica como "ALL" o " ", se busca en todas las \* propiedades de texto indizado. Aunque no es necesario que la columna sea una propiedad de texto, los resultados podrían no tener sentido si la columna es algún otro tipo de datos. El nombre de columna puede ser un identificador normal o [delimitado](-search-sql-identifiers.md)y debe separarlo de la condición mediante una coma. Si no se proporciona ninguna condición de texto completo, se usa la columna Contenido, que es el cuerpo del documento.

Puede especificar una configuración regional de búsqueda para identificar el separador de palabras adecuado y los formularios con convolucional para la consulta de búsqueda. Los valores de configuración regional válidos son Windows de código de idioma estándar (LCID). Por ejemplo, 1033 es el LCID para Estados Unidos-inglés. Coloque el LCID como el último elemento entre paréntesis de la cláusula FREETEXT. Para obtener información importante sobre la búsqueda y los idiomas, vea [Usar búsquedas localizadas.](-search-sql-usinglocsearches.md)

> [!Note]  
> La configuración regional de búsqueda predeterminada es la configuración regional predeterminada del sistema.

 

Debe incluir la parte de la condición de texto libre entre comillas simples y debe constar de uno o varios términos de búsqueda. El predicado FREETEXT no admite operaciones lógicas. Para buscar una frase como si fuera una sola palabra, encierre la frase entre comillas dobles.

Cuando se usa el predicado FREETEXT, los resultados de la consulta de búsqueda devuelven documentos que contienen todos los términos de búsqueda. No es necesario que los términos aparezcan en un orden determinado. Los documentos que contienen más términos de búsqueda tienen valores de columna de mayor rango.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se buscan documentos que contengan "equipo", "software", "hardware" o combinaciones de esas palabras:


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> No puede usar la coincidencia de una sola palabra y la coincidencia de frases en el mismo predicado FREETEXT.

 

Al realizar consultas con contracciones, debe escapar las comillas de la contracción cuando se usa FREETEXT, pero no cuando se usa CONTAINS.

Por ejemplo, se produce un error en la sintaxis siguiente:


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



La sintaxis correcta incluye dos comillas simples, no comillas dobles.

La sintaxis siguiente se realiza correctamente:


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[CONTAINS Predicate](-search-sql-contains.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



