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
# <a name="the-type_from_xmit-function"></a><span data-ttu-id="1ea47-104">El tipo \_ de la \_ función de transmisión</span><span class="sxs-lookup"><span data-stu-id="1ea47-104">The type\_from\_xmit Function</span></span>

<span data-ttu-id="1ea47-105">El código auxiliar llama al **tipo desde la función \_ de \_ transmisión** para convertir los datos de su tipo transmitido al tipo que se presenta a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1ea47-105">The stubs call the **type\_from\_xmit** function to convert data from its transmitted type to the type that is presented to the application.</span></span> <span data-ttu-id="1ea47-106">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="1ea47-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

<span data-ttu-id="1ea47-107">El primer parámetro es un puntero a los datos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="1ea47-107">The first parameter is a pointer to the transmitted data.</span></span> <span data-ttu-id="1ea47-108">La función establece el segundo parámetro para apuntar a los datos presentados.</span><span class="sxs-lookup"><span data-stu-id="1ea47-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="1ea47-109">El **tipo \_ de la función de \_ transmisión** debe administrar la memoria para el tipo presentado.</span><span class="sxs-lookup"><span data-stu-id="1ea47-109">The **type\_from\_xmit** function must manage memory for the presented type.</span></span> <span data-ttu-id="1ea47-110">La función debe asignar memoria para toda la estructura de datos que comienza en la dirección indicada por el segundo parámetro, excepto para el propio parámetro (el código auxiliar asigna memoria para el nodo raíz y lo pasa a la función).</span><span class="sxs-lookup"><span data-stu-id="1ea47-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="1ea47-111">El valor del segundo parámetro no puede cambiar durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="1ea47-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="1ea47-112">La función puede cambiar el contenido en esa dirección.</span><span class="sxs-lookup"><span data-stu-id="1ea47-112">The function can change the contents at that address.</span></span>

<span data-ttu-id="1ea47-113">En este ejemplo, el \_ tipo de vínculo de la función Double \_ de la \_ \_ transmisión convierte la matriz de tamaño en una lista de doble vínculo.</span><span class="sxs-lookup"><span data-stu-id="1ea47-113">In this example, the function DOUBLE\_LINK\_TYPE\_from\_xmit converts the sized array to a double-linked list.</span></span> <span data-ttu-id="1ea47-114">La función conserva el puntero válido al principio de la lista, libera la memoria asociada al resto de la lista y, a continuación, crea una nueva lista que comienza en el mismo puntero.</span><span class="sxs-lookup"><span data-stu-id="1ea47-114">The function retains the valid pointer to the beginning of the list, frees memory associated with the rest of the list, then creates a new list that starts at the same pointer.</span></span> <span data-ttu-id="1ea47-115">La función usa una función de utilidad, **InsertNewNode**, para anexar un nodo de lista al final de la lista y asignar los punteros *pNext* y *pPrevious* a los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="1ea47-115">The function uses a utility function, **InsertNewNode**, to append a list node to the end of the list and to assign the *pNext* and *pPrevious* pointers to appropriate values.</span></span>


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



 

 




