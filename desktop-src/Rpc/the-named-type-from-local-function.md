---
title: La named_type_from_local función
description: Los códigos auxiliares llaman al tipo \_ con nombre desde la función \_ \_ local.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c294398913a3bf6fe8b88eed5c42ceec84abf6b23ed994c85ff0fae8f21f2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127625"
---
# <a name="the-named_type_from_local-function"></a>Tipo con \_ nombre de la función \_ \_ local

Los códigos auxiliares llaman al tipo \_ con nombre desde la función \_ \_ local. Convierte el tipo que la aplicación usa en el tipo que los códigos auxiliares transmiten a través de la red. La función se define como:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

El primer parámetro es un puntero a los datos de la aplicación. El segundo parámetro es un puntero a un puntero. La función lo señala a los datos transmitidos. La función debe asignar memoria para el tipo transmitido.

 

 




