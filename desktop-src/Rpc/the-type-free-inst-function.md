---
title: La type_free_inst función
description: Los códigos auxiliares llaman a la función inst sin \_ tipo para liberar memoria asociada al tipo \_ presentado.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc71c8d3557c62eec39fe9a90855ef3ed057d29c21ec60a82ddc7fe04207f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923714"
---
# <a name="the-type_free_inst-function"></a>El tipo \_ free \_ inst (Función)

Los códigos auxiliares llaman a **la \_ función \_ inst** sin tipo para liberar memoria asociada al tipo presentado. La función se define como:

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

El parámetro apunta a la instancia de tipo presentada. Este objeto no debe liberarse. Para obtener una explicación sobre cuándo llamar a la función, vea [Transmisión \_ como atributo](the-transmit-as-attribute.md).

En el ejemplo siguiente, la lista vinculada doble se libera recorriendo la lista hasta su final y, a continuación, haciendo una copia de seguridad y liberando cada elemento de la lista.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_free_inst(
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    while (pList->pNext != NULL)  // go to end of the list
        pList = pList->pNext;

    pList = pList->pPrevious;
    while (pList != NULL) 
    {  
        // back through the list
        midl_user_free(pList->pNext);
        pList = pList->pPrevious;
    }
} 
```



 

 




