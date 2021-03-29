---
title: Solo atributos de búsqueda
description: A veces, realiza una búsqueda para determinar qué tipo de datos están disponibles para un objeto.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Atributos de búsqueda solo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993843"
---
# <a name="search-attributes-only"></a>Solo atributos de búsqueda

A veces, realiza una búsqueda para determinar qué tipo de datos están disponibles para un objeto. En este caso, solo le interesan los atributos y no los valores del objeto. Para ello, establezca la opción "solo atributos de búsqueda". Al especificar esta opción, se devuelven los nombres de atributo sin sus valores. Sin embargo, el conjunto de resultados incluye solo los atributos que tienen valores asignados. Por ejemplo, considere un objeto con los siguientes atributos:

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

Cuando se establece la opción solo atributos de búsqueda, el conjunto de resultados incluye:

``` syntax
First Name
Last Name
Phone Number
```

Para obtener más información sobre cómo usar la opción solo atributos de búsqueda con una interfaz de búsqueda específica, vea:

-   [Devolver solo nombres de atributo con IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)
-   [Buscar con Objetos de datos ActiveX](searching-with-activex-data-objects-ado.md)
-   [Buscar con OLE DB](searching-with-ole-db.md)

 

 




