---
title: La named_type_to_local función
description: Los códigos auxiliares llaman al tipo con nombre a la función local para convertir los datos de un tipo transmitido al \_ tipo que presentan a la \_ \_ aplicación.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fc1d45545c920ef19eb4c230045e62322833d3ef38e765357c29b20a48589c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924065"
---
# <a name="the-named_type_to_local-function"></a>Tipo con \_ nombre \_ de función \_ local

Los códigos auxiliares llaman al tipo con nombre a la función **\_ \_ \_ local** para convertir los datos de un tipo transmitido al tipo que presentan a la aplicación. La función se define como:

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

El primer parámetro apunta a los datos transmitidos. La función establece el segundo parámetro para que apunte a los datos presentados.

El **tipo con nombre de la función \_ \_ \_ local** debe administrar la memoria del tipo presentado. La función debe asignar memoria para toda la estructura de datos que comienza en la dirección indicada por el segundo parámetro, excepto para el propio parámetro (el código auxiliar asigna memoria para el nodo raíz y lo pasa a la función). El valor del segundo parámetro no puede cambiar durante la llamada. La función puede cambiar el contenido en esa dirección.

 

 




