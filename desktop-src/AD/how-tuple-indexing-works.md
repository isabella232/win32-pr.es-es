---
title: Cómo funciona la indexación de tuplas
description: Los índices de tupla se usan para optimizar las búsquedas que tienen 0 o más cadenas de búsqueda medial y 0 o 1 cadenas de búsqueda final. También se pueden utilizar para optimizar las búsquedas de una cadena de búsqueda inicial si no hay ningún índice ordinario disponible sobre ese atributo.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indexación de tuplas
- Buscar Active Directory de Active Directory, optimización
- Active Directory, optimización de búsqueda Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789514"
---
# <a name="how-tuple-indexing-works"></a>Cómo funciona la indexación de tuplas

Los índices de tupla se usan para optimizar las búsquedas que tienen 0 o más [cadenas de búsqueda medial](search-string-types.md) y 0 o 1 cadenas de búsqueda final. También se pueden utilizar para optimizar las búsquedas de una cadena de búsqueda inicial si no hay ningún índice ordinario disponible sobre ese atributo.

Puede activar la indexación de tupla para un atributo estableciendo el bit 5, que corresponde al valor 32, en el atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) . Este atributo se establece en el objeto de esquema que representa el atributo que necesita el índice de tupla. El impacto en el rendimiento de la activación de la indización de tupla es que cualquier valor de cadena establecido para ese atributo se expandirá en un gran número de fragmentos en el índice de la tupla. Cuando se expande un atributo, consume una cantidad mayor de espacio en disco en el archivo de árbol de información del directorio y también se actualiza más lentamente.

Los índices de tupla están diseñados para acelerar las búsquedas del formulario `*string*` . La aceleración puede ser considerable porque esta forma de búsqueda no se puede optimizar de otra manera, y en su forma no optimizada, obliga al servidor Active Directory a recorrer todos los objetos del ámbito de la búsqueda para realizar la consulta. Por lo tanto, una búsqueda base simplemente buscaría un objeto, que utilizaría menos recursos, una búsqueda secundaria inmediata buscaría solo los elementos secundarios de un objeto (que podría usar menos recursos o más recursos en función del tamaño del contenedor) y una búsqueda de subárbol recorrerá todo el subárbol bajo el objeto base, que normalmente requeriría una gran cantidad de recursos y ser muy lento debido al tamaño del subárbol.

Los índices de tupla funcionan dividiendo una cadena en *tuplas*. Por ejemplo, la cadena "Active Directory" se dividiría en las siguientes tuplas:

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

 

Un índice de tupla contiene una entrada para cada una de estas tuplas. Por lo tanto, si un usuario busca `*cto*` , el servidor de Active Directory buscará todas las coincidencias de "CTO" en el índice y, en este caso, buscará un puntero de nuevo al registro que tenía un atributo (índice de tupla) con un valor de "Directory".

Si la cadena de búsqueda medial ( `*cto*` en el ejemplo anterior) es lo suficientemente específica, la búsqueda será bastante eficaz porque reduce en gran medida el número de objetos que el servidor de Active Directory debe inspeccionar para realizar la consulta.

 

 