---
description: Microsoft Windows Search, basado en los estándares SQL-92 y SQL-99, mejora las búsquedas basadas en documentos de texto completo en aplicaciones de administración de documentos o administración de conocimientos.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: SQL Extensiones en Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c300b0960e97cba14237bd355e33ae7e42788b1925525e60462d15a5d014e6f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462464"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>SQL Extensiones en Microsoft Windows Search

Microsoft Windows Search, basado en los estándares SQL-92 y SQL-99, mejora las búsquedas basadas en documentos de texto completo en aplicaciones de administración de documentos o administración de conocimientos. Windows Entre las mejoras de búsqueda se incluyen las siguientes:

## <a name="128-character-identifier-names"></a>Nombres de identificador de 128 caracteres

Aunque SQL-92 y SQL-99 restringen la columna y otros identificadores a 18 caracteres, Windows Search admite nombres de columna de 128 caracteres. Para obtener más información, consulte [Identificadores](-search-sql-identifiers.md).

## <a name="grouping-results-by-columns"></a>Agrupar los resultados por columnas

Las consultas pueden especificar cómo agrupar los resultados. Puede especificar los intervalos por los que se va a agrupar y puede especificar más de una columna para la agrupación. Por ejemplo, puede agrupar los resultados en un intervalo de tamaños de archivo (tamaño < 100, 100 <= tamaño < 1000; 1000 <= tamaño) y puede anidar agrupaciones. Para obtener más información, [vea GROUP ON ... Sobre... Instrucción](-search-sql-group-on-over.md).

## <a name="diacritic-insensitive-searching"></a>Diacritic-Insensitive búsqueda

Además de buscar que no distingue mayúsculas de minúsculas, Windows Search admite búsquedas que no son sensibles a los signos diacríticos (acentos). Para obtener más información, vea [Confidencialidad diacrítica en búsquedas](-search-sql-accentinsensitivitysearches.md).

## <a name="column-weighting"></a>Ponderación de columnas

Las consultas que buscan más de una columna pueden especificar la importancia de cada columna. Los [predicados CONTAINS](-search-sql-contains.md) [y FREETEXT](-search-sql-freetext.md) admiten la ponderación de columnas.

## <a name="null-predicate"></a>Predicado NULL

Aunque la indexación de contenido de texto completo no tiene ningún conjunto definido de columnas, las consultas pueden requerir que los miembros del conjunto de resultados tengan o no columnas especificadas. No es posible diferenciar entre un documento que tiene una propiedad especificada con el valor establecido en **NULL** y un documento que no tiene la propiedad en absoluto.

## <a name="rank-modification"></a>Modificación de la clasificación

Puede manipular la clasificación de resultados de búsqueda mediante [ponderaciones](-search-sql-understandingrelevancevalues.md) en propiedades y en grupos de propiedades con alias. La coerción de rangos admite la manipulación directa de la clasificación por relevancia en función de los criterios que especifique.

 

 



