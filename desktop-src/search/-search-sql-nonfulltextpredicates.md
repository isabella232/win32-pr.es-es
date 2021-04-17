---
description: El lenguaje de consulta de Microsoft Windows Search admite seis predicados de búsqueda que no son de texto completo. Los predicados descritos en esta sección se enumeran en la tabla siguiente.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Predicados que no son de texto completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705482"
---
# <a name="non-full-text-predicates"></a>Predicados que no son de texto completo

El lenguaje de consulta de Microsoft Windows Search admite seis predicados de búsqueda que no son de texto completo. Los predicados descritos en esta sección se enumeran en la tabla siguiente.



| Predicado de texto no completo                                                    | Descripción                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ALL bit a bit y SOME](all-bitwise.md)                            | Es un conjunto de palabras clave que se van a probar los bits de un tipo entero.                                                                                                               |
| [DATEADD (función)](-search-sql-dateadd.md)                                | Realiza cálculos de fecha y hora para las propiedades coincidentes que tienen tipos de fecha. Utilice la función DATEADD para obtener fechas y horas en un período de tiempo especificado antes de la presente.     |
| [LIKE (predicado)](-search-sql-like.md)                                     | Compara los valores de columna utilizando la coincidencia de patrones simple con caracteres comodín.                                                                                                          |
| [Comparación de valores literales](-search-sql-literalvaluecomparison.md)         | Compara los valores de columna con cadena, fecha, marca de tiempo, numérico y otros valores literales. Este predicado admite desigualdades como mayor que (' > ') y menor que (' < '). |
| [Comparaciones de varios valores (matriz)](-search-sql-multivaluedcomparisons.md) | Compara las columnas de varios valores con una matriz de literales de varios valores.                                                                                                                   |
| [Predicado NULL](-search-sql-null.md)                                     | Detecta los valores de columna que no están definidos para el documento.                                                                                                                              |



 

> [!IMPORTANT]
> Las consultas de búsqueda que usan el predicado **null** pueden requerir que búsqueda de Windows Examine todo el catálogo, lo que puede ralentizar el rendimiento de la consulta.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



