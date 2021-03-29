---
title: La función type_free_inst
description: El código auxiliar llama a \_ la \_ función inst Free de tipo para liberar memoria asociada al tipo presentado.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3754106cf8e0cc6e338f91d6c233181aa33038eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903484"
---
# <a name="the-type_free_inst-function"></a><span data-ttu-id="ae56a-104">La \_ función Free \_ inst de tipo</span><span class="sxs-lookup"><span data-stu-id="ae56a-104">The type\_free\_inst Function</span></span>

<span data-ttu-id="ae56a-105">El código auxiliar llama a la función **\_ \_ inst Free de tipo** para liberar memoria asociada al tipo presentado.</span><span class="sxs-lookup"><span data-stu-id="ae56a-105">The stubs call the **type\_free\_inst** function to free memory associated with the presented type.</span></span> <span data-ttu-id="ae56a-106">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="ae56a-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="ae56a-107">El parámetro apunta a la instancia de tipo presentada.</span><span class="sxs-lookup"><span data-stu-id="ae56a-107">The parameter points to the presented type instance.</span></span> <span data-ttu-id="ae56a-108">Este objeto no se debe liberar.</span><span class="sxs-lookup"><span data-stu-id="ae56a-108">This object should not be freed.</span></span> <span data-ttu-id="ae56a-109">Para obtener una explicación sobre cuándo llamar a la función, vea [el \_ atributo transmitir como](the-transmit-as-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="ae56a-109">For a discussion on when to call the function, see [The transmit\_as Attribute](the-transmit-as-attribute.md).</span></span>

<span data-ttu-id="ae56a-110">En el ejemplo siguiente, la lista de vínculos dobles se libera recorriendo la lista hasta su final, haciendo una copia de seguridad y liberando cada elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="ae56a-110">In the following example, the double-linked list is freed by walking the list to its end, then backing up and freeing each element of the list.</span></span>


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



 

 




