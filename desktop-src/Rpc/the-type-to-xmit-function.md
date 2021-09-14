---
title: La type_to_xmit función
description: Los códigos auxiliares llaman al tipo a la función xmit para convertir el tipo que presenta la \_ aplicación en el tipo \_ transmitido.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6a6b250d661fc19b0ee8fb68d21f171960e512
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171297"
---
# <a name="the-type_to_xmit-function"></a>El tipo \_ para \_ xmit (Función)

Los códigos auxiliares llaman al tipo a la función **\_ \_ xmit** para convertir el tipo que presenta la aplicación en el tipo transmitido. La función se define como:

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

El primer parámetro es un puntero a los datos de la aplicación. La función establece el segundo parámetro para que apunte a los datos transmitidos. La función debe asignar memoria para el tipo transmitido.

En el ejemplo siguiente, el cliente llama al procedimiento remoto que tiene un **\[ parámetro in y out \]** de tipo DOUBLE LINK \_ \_ TYPE. El código auxiliar de cliente llama al tipo a la función **\_ \_ xmit,** aquí denominada DOUBLE LINK TYPE a xmit, para convertir los datos de la lista vinculada doble \_ en una \_ \_ \_ matriz de tamaño.

La función determina el número de elementos de la lista, asigna una matriz lo suficientemente grande como para contener esos elementos y, a continuación, copia los elementos de lista en la matriz. Antes de que la función vuelva, el segundo parámetro, *ppArray*, se establece para que apunte a la estructura de datos recién asignada.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray)
{
    short cCount = 0;
    DOUBLE_LINK_TYPE * pHead = pList;  // save pointer to start 
    DOUBLE_XMIT_TYPE * pArray;
 
    /* count the number of elements to allocate memory */
    for (; pList != NULL; pList = pList->pNext)
        cCount++;
 
    /* allocate the memory for the array */
    pArray = (DOUBLE_XMIT_TYPE *) MIDL_user_allocate 
         (sizeof(DOUBLE_XMIT_TYPE) + (cCount * sizeof(short)));
    pArray->sSize = cCount;
 
    /* copy the linked list contents into the array */
    cCount = 0;
    for (i = 0, pList = pHead; pList != NULL; pList = pList->pNext)
        pArray->asNumber[cCount++] = pList->sNumber;
 
    /* return the address of the pointer to the array */
    *ppArray = pArray;
}
```



 

 




