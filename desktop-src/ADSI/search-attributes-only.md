---
title: Solo atributos de búsqueda
description: A veces se realiza una búsqueda para determinar qué tipo de datos está disponible para un objeto.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- AdsI de solo atributos de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b1775c759975a508f5382ef2a30f290ac4a96b3b92120d4face6b1d0556426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443935"
---
# <a name="search-attributes-only"></a>Solo atributos de búsqueda

A veces se realiza una búsqueda para determinar qué tipo de datos está disponible para un objeto. En este caso, solo le interesan los atributos y no los valores del objeto. Para ello, establezca la opción "solo atributos de búsqueda". Si se especifica esta opción, se devuelven los nombres de atributo sin sus valores. Sin embargo, el conjunto de resultados incluye solo los atributos que tienen valores asignados. Por ejemplo, considere un objeto con los atributos siguientes:

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

Cuando se establece la opción de solo atributos de búsqueda, el conjunto de resultados incluye:

``` syntax
First Name
Last Name
Phone Number
```

Para obtener más información sobre el uso de la opción de solo atributos de búsqueda con una interfaz de búsqueda específica, vea:

-   [Devolver solo nombres de atributo con IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)
-   [Buscar con objetos ActiveX datos](searching-with-activex-data-objects-ado.md)
-   [Búsqueda con OLE DB](searching-with-ole-db.md)

 

 




