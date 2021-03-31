---
description: En una base de datos relacional, las filas devueltas por una consulta de búsqueda deben cumplir todas las condiciones llamadas por la consulta. Por el contrario, una consulta de búsqueda de Windows puede devolver documentos que cumplan las condiciones de búsqueda a distintos grados.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Descripción de los valores de relevancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907741"
---
# <a name="understanding-relevance-values"></a>Descripción de los valores de relevancia

En una base de datos relacional, las filas devueltas por una consulta de búsqueda deben cumplir todas las condiciones llamadas por la consulta. Por el contrario, una consulta de búsqueda de Windows puede devolver documentos que cumplan las condiciones de búsqueda a distintos grados.

Por ejemplo, una búsqueda del término "programa" en una base de datos relacional genera registros que contienen la ortografía específica de la palabra. El hecho de que un registro contenga una o 100 instancias de la palabra no afecte a los resultados. En cambio, Windows Search devuelve un valor de relevancia asociado a los documentos coincidentes. La relevancia de los documentos que tienen "Program" en el título es mayor que los que contienen la palabra solo en el último párrafo. De forma similar, los documentos que contienen variaciones del término de búsqueda, por ejemplo, "programas" y "programación" también coinciden con y son devueltos por la consulta.

Las consultas de Windows Search devuelven valores de relevancia de enteros en la columna denominada "Rank".

Asimismo:

-   Los valores de rango devueltos por la consulta son enteros comprendidos entre 0 y 1000.
-   Los valores de clasificación más altos indican documentos que coinciden mejor con las condiciones de búsqueda.
-   Los valores de rango solo se aplican a la consulta actual, por lo que no se pueden comparar los resultados entre las consultas.
-   Los valores de rango son relativos a los demás documentos que coinciden con la consulta. Por lo tanto, el valor de clasificación de un documento determinado depende de otros documentos que también coinciden con la consulta.
-   Los valores de rango de los elementos que coinciden con un predicado puramente relacional son 1000.

Puede manipular los valores de rango devueltos mediante el uso de pesos de columna en los predicados de la cláusula [Contains](-search-sql-contains.md) y [FREETEXT](-search-sql-freetext.md) , y la cláusula Rank by.

 

 



