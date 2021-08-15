---
title: Funcionamiento de la indexación de tuplas
description: Los índices de tupla se usan para optimizar las búsquedas que tienen 0 o más cadenas de búsqueda medial y 0 o 1 cadenas de búsqueda final. También se pueden usar para optimizar las búsquedas de una cadena de búsqueda inicial si no hay ningún índice normal disponible sobre ese atributo.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indexación de tupla
- Búsqueda Active Directory Active Directory , optimización
- Active Directory, optimización de búsqueda Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9d15bad8de15e4f559123d2d3cb3b6b9ec6446328e6ed4c4c52cf18355d634
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188038"
---
# <a name="how-tuple-indexing-works"></a>Funcionamiento de la indexación de tuplas

Los índices de tupla se usan para optimizar las búsquedas que tienen 0 o más [cadenas de](search-string-types.md) búsqueda medial y 0 o 1 cadenas de búsqueda final. También se pueden usar para optimizar las búsquedas de una cadena de búsqueda inicial si no hay ningún índice normal disponible sobre ese atributo.

Puede activar la indexación de tupla para un atributo estableciendo el bit 5, que corresponde al valor 32, en el [**atributo searchFlags.**](/windows/desktop/ADSchema/a-searchflags) Este atributo se establece en el objeto de esquema que representa el atributo que necesita el índice de tupla. El impacto en el rendimiento de activar la indexación de tupla es que cualquier valor de cadena establecido para ese atributo se expandirá en un gran número de fragmentos en el índice de tupla. Cuando un atributo se expande, consume una mayor cantidad de espacio en disco en el archivo de árbol de información de directorio y también se actualiza más lentamente.

Los índices de tupla están diseñados para acelerar las búsquedas con el formato `*string*` . La aceleración puede ser considerable porque esta forma de búsqueda no se puede optimizar de ninguna otra manera y, en su forma no optimizada, obliga al servidor de Active Directory a recorrer todos los objetos del ámbito de la búsqueda para realizar la consulta. Por lo tanto, una búsqueda base solo buscaría un objeto, que usaría menos recursos, una búsqueda de elementos secundarios inmediato buscaría solo los elementos secundarios de un objeto (que podría usar menos recursos o más recursos según el tamaño del contenedor) y una búsqueda de subárbol recorrerá todo el subárbol bajo el objeto base, lo que normalmente requeriría muchos recursos y sería muy lento debido al tamaño del subárbol.

Los índices de tupla funcionan al dividir una cadena en *tuplas.* Por ejemplo, la cadena "Active Directory" se dividiría en las tuplas siguientes:

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> El directorio se detendrá en 32767 caracteres al expandir una cadena para la indexación de tupla.

 

Un índice de tupla contendrá una entrada para cada una de estas tuplas. Por lo tanto, si un usuario busca , el servidor de Active Directory buscará todas las coincidencias de "cto" en el índice y, en este caso, buscará un puntero al registro que tenía un atributo (indizado por tupla) con un valor `*cto*` de "Directory".

Si la cadena de búsqueda medial ( en el ejemplo anterior) es lo suficientemente específica, la búsqueda será bastante eficaz porque reduce considerablemente el número de objetos que el servidor Active Directory debe inspeccionar para realizar la `*cto*` consulta.

 

 