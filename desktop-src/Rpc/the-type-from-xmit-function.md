---
title: La función type_from_xmit
description: El código auxiliar llama al tipo \_ desde la \_ función de transmisión para convertir los datos de su tipo transmitido al tipo que se presenta a la aplicación.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076165"
---
# <a name="the-type_from_xmit-function"></a>El tipo \_ de la \_ función de transmisión

El código auxiliar llama al **tipo desde la función \_ de \_ transmisión** para convertir los datos de su tipo transmitido al tipo que se presenta a la aplicación. La función se define como:

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

El primer parámetro es un puntero a los datos transmitidos. La función establece el segundo parámetro para apuntar a los datos presentados.

El **tipo \_ de la función de \_ transmisión** debe administrar la memoria para el tipo presentado. La función debe asignar memoria para toda la estructura de datos que comienza en la dirección indicada por el segundo parámetro, excepto para el propio parámetro (el código auxiliar asigna memoria para el nodo raíz y lo pasa a la función). El valor del segundo parámetro no puede cambiar durante la llamada. La función puede cambiar el contenido en esa dirección.

En este ejemplo, el \_ tipo de vínculo de la función Double \_ de la \_ \_ transmisión convierte la matriz de tamaño en una lista de doble vínculo. La función conserva el puntero válido al principio de la lista, libera la memoria asociada al resto de la lista y, a continuación, crea una nueva lista que comienza en el mismo puntero. La función usa una función de utilidad, **InsertNewNode**, para anexar un nodo de lista al final de la lista y asignar los punteros *pNext* y *pPrevious* a los valores adecuados.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_from_xmit(
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    DOUBLE_LINK_TYPE *pCurrent;
    int i;
 
    if (pArray->sSize <= 0) 
    {  
        // error checking
        return;
    }
 
    if (pList == NULL) // if invalid, create the list head
        pList = InsertNewNode(pArray->asNumber[0], NULL);             
    else 
    {    
        DOUBLE_LINK_TYPE_free_inst(pList);  // free all other nodes
        pList->sNumber = pArray->asNumber[0];
        pList->pNext = NULL; 
    }
 
    pCurrent = pList; 
    for (i = 1; i < pArray->sSize; i++)  
        pCurrent = InsertNewNode(pArray->asNumber[i], pCurrent);
    
    return;
}
```



 

 




