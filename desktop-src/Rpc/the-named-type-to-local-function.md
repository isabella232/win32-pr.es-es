---
title: La función named_type_to_local
description: El código auxiliar llama al tipo con nombre \_ \_ a la \_ función local para convertir datos de un tipo transmitido al tipo que presentan en la aplicación.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075721"
---
# <a name="the-named_type_to_local-function"></a>El tipo con nombre \_ \_ a la \_ función local

El código auxiliar llama al tipo **con nombre a la función \_ \_ \_ local** para convertir datos de un tipo transmitido al tipo que presentan en la aplicación. La función se define como:

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

El primer parámetro apunta a los datos transmitidos. La función establece el segundo parámetro para apuntar a los datos presentados.

El **tipo con nombre de la función \_ \_ \_ local** debe administrar la memoria para el tipo presentado. La función debe asignar memoria para toda la estructura de datos que comienza en la dirección indicada por el segundo parámetro, excepto para el propio parámetro (el código auxiliar asigna memoria para el nodo raíz y lo pasa a la función). El valor del segundo parámetro no puede cambiar durante la llamada. La función puede cambiar el contenido en esa dirección.

 

 




