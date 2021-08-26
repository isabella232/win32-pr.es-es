---
title: La type_free_xmit función
description: Los códigos auxiliares llaman a la función xmit libre \_ de tipo para liberar memoria asociada a los datos \_ transmitidos.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c192e30ec4f18d70d6e694e6097cb77ee7a2338230868730dc37c1c3207010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016585"
---
# <a name="the-type_free_xmit-function"></a>Función \_ \_ xmit libre de tipos

Los códigos auxiliares llaman a **la \_ función \_ xmit** libre de tipo para liberar memoria asociada a los datos transmitidos. Una vez [que el tipo de la función \_ \_ xmit](the-type-from-xmit-function.md) convierte los datos transmitidos a su tipo presentado, la memoria ya no es necesaria. La función se define como:

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

El parámetro es un puntero a la memoria que contiene el tipo transmitido.

En este ejemplo, la memoria contiene una matriz que está en una sola estructura. La función DOUBLE LINK TYPE free xmit usa la función proporcionada por el usuario \_ \_ \_ \_ midl \_ user free para liberar \_ la memoria:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




