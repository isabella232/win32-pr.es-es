---
title: La función type_free_xmit
description: El código auxiliar llama a la \_ función de transmisión libre de tipos \_ para liberar memoria asociada a los datos transmitidos.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33d5cb8079d50923de2161b0384550829a5f22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268853"
---
# <a name="the-type_free_xmit-function"></a><span data-ttu-id="c9beb-104">La \_ función de \_ transmisión libre de tipos</span><span class="sxs-lookup"><span data-stu-id="c9beb-104">The type\_free\_xmit Function</span></span>

<span data-ttu-id="c9beb-105">El código auxiliar llama a la función de **\_ \_ transmisión libre de tipos** para liberar memoria asociada a los datos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="c9beb-105">The stubs call the **type\_free\_xmit** function to free memory associated with the transmitted data.</span></span> <span data-ttu-id="c9beb-106">Después de que el [tipo de la función \_ de \_ transmisión](the-type-from-xmit-function.md) convierta los datos transmitidos a su tipo presentado, la memoria ya no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="c9beb-106">After the [type\_from\_xmit](the-type-from-xmit-function.md) function converts the transmitted data to its presented type, the memory is no longer needed.</span></span> <span data-ttu-id="c9beb-107">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="c9beb-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

<span data-ttu-id="c9beb-108">El parámetro es un puntero a la memoria que contiene el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="c9beb-108">The parameter is a pointer to the memory that contains the transmitted type.</span></span>

<span data-ttu-id="c9beb-109">En este ejemplo, la memoria contiene una matriz que está en una única estructura.</span><span class="sxs-lookup"><span data-stu-id="c9beb-109">In this example, the memory contains an array that is in a single structure.</span></span> <span data-ttu-id="c9beb-110">La transmisión gratuita del tipo de vínculo de doble función \_ \_ \_ \_ usa el usuario de MIDL de la función proporcionada por el usuario \_ \_ para liberar memoria:</span><span class="sxs-lookup"><span data-stu-id="c9beb-110">The function DOUBLE\_LINK\_TYPE\_free\_xmit uses the user-supplied function midl\_user\_free to free the memory:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




