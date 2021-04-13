---
title: La función named_type_from_local
description: El código auxiliar llama al \_ tipo con nombre \_ desde la \_ función local.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356884"
---
# <a name="the-named_type_from_local-function"></a><span data-ttu-id="9ed27-104">El tipo con nombre \_ \_ de la \_ función local</span><span class="sxs-lookup"><span data-stu-id="9ed27-104">The named\_type\_from\_local Function</span></span>

<span data-ttu-id="9ed27-105">El código auxiliar llama al \_ tipo con nombre \_ desde la \_ función local.</span><span class="sxs-lookup"><span data-stu-id="9ed27-105">The stubs call the named\_type\_from\_local function.</span></span> <span data-ttu-id="9ed27-106">Convierte el tipo que utiliza la aplicación en el tipo que el código auxiliar transmite a través de la red.</span><span class="sxs-lookup"><span data-stu-id="9ed27-106">It converts the type that the application uses into the type the stubs transmit across the network.</span></span> <span data-ttu-id="9ed27-107">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="9ed27-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

<span data-ttu-id="9ed27-108">El primer parámetro es un puntero a los datos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ed27-108">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="9ed27-109">El segundo parámetro es un puntero a un puntero.</span><span class="sxs-lookup"><span data-stu-id="9ed27-109">The second parameter is a pointer to a pointer.</span></span> <span data-ttu-id="9ed27-110">La función apunta a los datos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="9ed27-110">The function points it to the transmitted data.</span></span> <span data-ttu-id="9ed27-111">La función debe asignar memoria para el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="9ed27-111">The function must allocate memory for the transmitted type.</span></span>

 

 




