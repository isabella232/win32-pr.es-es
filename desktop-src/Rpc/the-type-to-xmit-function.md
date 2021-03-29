---
title: La función type_to_xmit
description: El código auxiliar llama a \_ la \_ función de transmisión para convertir el tipo presentado por la aplicación en el tipo transmitido.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6a6b250d661fc19b0ee8fb68d21f171960e512
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994446"
---
# <a name="the-type_to_xmit-function"></a><span data-ttu-id="472c9-104">Tipo \_ para la \_ función de transmisión</span><span class="sxs-lookup"><span data-stu-id="472c9-104">The type\_to\_xmit Function</span></span>

<span data-ttu-id="472c9-105">El código auxiliar llama a la función de **\_ \_ transmisión** para convertir el tipo presentado por la aplicación en el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="472c9-105">The stubs call the **type\_to\_xmit** function to convert the type that is presented by the application into the transmitted type.</span></span> <span data-ttu-id="472c9-106">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="472c9-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

<span data-ttu-id="472c9-107">El primer parámetro es un puntero a los datos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="472c9-107">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="472c9-108">La función establece el segundo parámetro para que señale a los datos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="472c9-108">The second parameter is set by the function to point to the transmitted data.</span></span> <span data-ttu-id="472c9-109">La función debe asignar memoria para el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="472c9-109">The function must allocate memory for the transmitted type.</span></span>

<span data-ttu-id="472c9-110">En el ejemplo siguiente, el cliente llama al procedimiento remoto que tiene un parámetro **\[ in, \] out** de tipo de \_ vínculo doble \_ .</span><span class="sxs-lookup"><span data-stu-id="472c9-110">In the following example, the client calls the remote procedure that has an **\[in, out\]** parameter of type DOUBLE\_LINK\_TYPE.</span></span> <span data-ttu-id="472c9-111">El código auxiliar del cliente llama al tipo para la función de **\_ \_ transmisión** , aquí denominado \_ tipo de vínculo doble para la \_ \_ \_ transmisión, para convertir los datos de la lista de vínculos dobles en una matriz de tamaño.</span><span class="sxs-lookup"><span data-stu-id="472c9-111">The client stub calls the **type\_to\_xmit** function, here named DOUBLE\_LINK\_TYPE\_to\_xmit, to convert double-linked list data into a sized array.</span></span>

<span data-ttu-id="472c9-112">La función determina el número de elementos de la lista, asigna una matriz lo suficientemente grande como para contener esos elementos y, a continuación, copia los elementos de la lista en la matriz.</span><span class="sxs-lookup"><span data-stu-id="472c9-112">The function determines the number of elements in the list, allocates an array large enough to hold those elements, then copies the list elements into the array.</span></span> <span data-ttu-id="472c9-113">Antes de que la función devuelva, el segundo parámetro, *ppArray*, se establece de forma que apunte a la estructura de datos recién asignada.</span><span class="sxs-lookup"><span data-stu-id="472c9-113">Before the function returns, the second parameter, *ppArray*, is set to point to the newly allocated data structure.</span></span>


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



 

 




