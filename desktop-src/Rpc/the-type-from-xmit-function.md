---
title: La type_from_xmit de trabajo
description: Los códigos auxiliares llaman al tipo de la función xmit para convertir datos de su tipo transmitido al tipo que \_ se presenta a la \_ aplicación.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250503"
---
# <a name="the-type_from_xmit-function"></a>El tipo \_ de \_ la función xmit

Los códigos auxiliares llaman al tipo de la función **\_ \_ xmit** para convertir datos de su tipo transmitido al tipo que se presenta a la aplicación. La función se define como:

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

El primer parámetro es un puntero a los datos transmitidos. La función establece el segundo parámetro para que apunte a los datos presentados.

El **tipo de la función \_ \_ xmit** debe administrar la memoria del tipo presentado. La función debe asignar memoria para toda la estructura de datos que comienza en la dirección indicada por el segundo parámetro, excepto para el propio parámetro (el código auxiliar asigna memoria para el nodo raíz y la pasa a la función). El valor del segundo parámetro no puede cambiar durante la llamada. La función puede cambiar el contenido de esa dirección.

En este ejemplo, la función DOUBLE \_ LINK \_ TYPE de \_ \_ xmit convierte la matriz de tamaño en una lista de vínculos dobles. La función conserva el puntero válido al principio de la lista, libera memoria asociada al resto de la lista y, a continuación, crea una nueva lista que comienza en el mismo puntero. La función usa una función de utilidad, **InsertNewNode**, para anexar un nodo de lista al final de la lista y para asignar los punteros *pNext* y *pPrevious* a los valores adecuados.


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



 

 




