---
description: Para seleccionar una NIC de una tabla BLOB de NPP devuelta por Monitor de red, llame a la función GetNPPBlobTable. Esta función devuelve una tabla de BLOBs NPP, que la aplicación puede enumerar a continuación para seleccionar la NIC en la que está interesado.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Selección de una NIC de una tabla BLOB NPP devuelta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08215bb647482ba8544d7eaa033dea7efd9a5ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909802"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a>Selección de una NIC de una tabla BLOB NPP devuelta

Para seleccionar una NIC de una tabla BLOB de NPP devuelta por Monitor de red, llame a la función [**GetNPPBlobTable**](getnppblobtable.md) . Esta función devuelve una tabla de BLOBs NPP, que la aplicación puede enumerar a continuación para seleccionar la NIC en la que está interesado.

Cuando se llama a esta función, puede devolver una tabla BLOB de todas las NIC registradas en el equipo local o un conjunto más pequeño de NIC filtradas. Para filtrar las NIC que se devuelven, puede proporcionar un [*BLOB de filtro*](f.md) cuando se realiza la llamada.



| Para información acerca de                                                       | Vea                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Cómo especificar un filtro que limite las NIC devueltas en una tabla de BLOBs NPP. | [Especificación de un BLOB en filtro](specifying-a-filter-blob.md)                                             |
| Cómo seleccionar una NIC registrada en un equipo local.                         | [Selección de una NIC registrada](selecting-a-registered-nic.md)                                         |
| Cómo seleccionar una NIC de una tabla BLOB de NPP proporcionada                          | [Selección de una NIC de una tabla BLOB de NPP proporcionada](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



