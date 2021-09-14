---
title: La type_free_inst función
description: Los códigos auxiliares llaman a la \_ función inst de \_ tipo free para liberar memoria asociada al tipo presentado.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3754106cf8e0cc6e338f91d6c233181aa33038eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161031"
---
# <a name="the-type_free_inst-function"></a>El tipo \_ free \_ inst (Función)

Los códigos auxiliares llaman a **la \_ función \_ inst de** tipo free para liberar memoria asociada al tipo presentado. La función se define como:

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

El parámetro apunta a la instancia de tipo presentada. Este objeto no debe liberarse. Para obtener una explicación sobre cuándo llamar a la función, vea [Transmitir \_ como atributo](the-transmit-as-attribute.md).

En el ejemplo siguiente, la lista de doble vinculación se libera recorriendo la lista hasta su final y, a continuación, haciendo una copia de seguridad y liberando cada elemento de la lista.


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



 

 




