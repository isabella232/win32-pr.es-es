---
description: Microsoft Windows Search, basado en los estándares SQL-92 y SQL-99, mejora las búsquedas basadas en documentos de texto completo en aplicaciones de administración de documentos o de administración de conocimiento.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: Extensiones SQL en Microsoft Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540678"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>Extensiones SQL en Microsoft Search

Microsoft Windows Search, basado en los estándares SQL-92 y SQL-99, mejora las búsquedas basadas en documentos de texto completo en aplicaciones de administración de documentos o de administración de conocimiento. Entre las mejoras de Windows Search se incluyen las siguientes:

## <a name="128-character-identifier-names"></a>128: nombres de identificador de caracteres

Si bien SQL-92 y SQL-99 restringen la columna y otros identificadores a 18 caracteres, Windows Search admite nombres de columna de 128 caracteres. Para obtener más información, vea [Identificadores](-search-sql-identifiers.md).

## <a name="grouping-results-by-columns"></a>Agrupar resultados por columnas

Las consultas pueden especificar cómo agrupar los resultados. Puede especificar los intervalos por los que desea agrupar y puede especificar más de una columna para la agrupación. Por ejemplo, puede agrupar los resultados en un intervalo de tamaños de archivo (Tamaño < 100, 100 <= tamaño < 1000; 1000 <= tamaño) y puede anidar agrupaciones. Para obtener más información, vea [Agrupar por... MÁS de... Instrucción](-search-sql-group-on-over.md).

## <a name="diacritic-insensitive-searching"></a>Búsqueda de Diacritic-Insensitive

Además de la búsqueda que no distingue entre mayúsculas y minúsculas, la búsqueda de Windows admite búsquedas que no se distinguen por signos diacríticos (marcas de acento). Para obtener más información, vea [sensibilidad diacríticas en las búsquedas](-search-sql-accentinsensitivitysearches.md).

## <a name="column-weighting"></a>Ponderación de columnas

Las consultas que buscan más de una columna pueden especificar la importancia de cada columna. Los predicados [Contains](-search-sql-contains.md) y [FREETEXT](-search-sql-freetext.md) admiten la ponderación de las columnas.

## <a name="null-predicate"></a>Predicado NULL

Aunque la indización de contenido de texto completo no tiene ningún conjunto de columnas definido, las consultas pueden requerir que los miembros del conjunto de resultados o no tengan columnas especificadas. No es posible diferenciar entre un documento que tiene una propiedad especificada con el valor establecido en **null** y un documento que no tiene la propiedad.

## <a name="rank-modification"></a>Modificación de rango

Puede manipular la clasificación de los resultados de la búsqueda mediante [pesos](-search-sql-understandingrelevancevalues.md) en las propiedades y en grupos de propiedades con alias. La coerción de rangos admite la manipulación directa de la clasificación de relevancia en función de los criterios que se especifiquen.

 

 



