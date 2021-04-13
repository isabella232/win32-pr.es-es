---
title: La función named_type_from_local
description: El código auxiliar llama al \_ tipo con nombre \_ desde la \_ función local.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356884"
---
# <a name="the-named_type_from_local-function"></a>El tipo con nombre \_ \_ de la \_ función local

El código auxiliar llama al \_ tipo con nombre \_ desde la \_ función local. Convierte el tipo que utiliza la aplicación en el tipo que el código auxiliar transmite a través de la red. La función se define como:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

El primer parámetro es un puntero a los datos de la aplicación. El segundo parámetro es un puntero a un puntero. La función apunta a los datos transmitidos. La función debe asignar memoria para el tipo transmitido.

 

 




