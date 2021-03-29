---
title: La función named_type_to_local
description: El código auxiliar llama al tipo con nombre \_ \_ a la \_ función local para convertir datos de un tipo transmitido al tipo que presentan en la aplicación.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075721"
---
# <a name="the-named_type_to_local-function"></a><span data-ttu-id="2895b-104">El tipo con nombre \_ \_ a la \_ función local</span><span class="sxs-lookup"><span data-stu-id="2895b-104">The named\_type\_to\_local Function</span></span>

<span data-ttu-id="2895b-105">El código auxiliar llama al tipo **con nombre a la función \_ \_ \_ local** para convertir datos de un tipo transmitido al tipo que presentan en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2895b-105">The stubs call the **named\_type\_to\_local** function to convert data from a transmitted type to the type that they present to the application.</span></span> <span data-ttu-id="2895b-106">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="2895b-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

<span data-ttu-id="2895b-107">El primer parámetro apunta a los datos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="2895b-107">The first parameter points to the transmitted data.</span></span> <span data-ttu-id="2895b-108">La función establece el segundo parámetro para apuntar a los datos presentados.</span><span class="sxs-lookup"><span data-stu-id="2895b-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="2895b-109">El **tipo con nombre de la función \_ \_ \_ local** debe administrar la memoria para el tipo presentado.</span><span class="sxs-lookup"><span data-stu-id="2895b-109">The **named\_type\_to\_local** function must manage memory for the presented type.</span></span> <span data-ttu-id="2895b-110">La función debe asignar memoria para toda la estructura de datos que comienza en la dirección indicada por el segundo parámetro, excepto para el propio parámetro (el código auxiliar asigna memoria para el nodo raíz y lo pasa a la función).</span><span class="sxs-lookup"><span data-stu-id="2895b-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="2895b-111">El valor del segundo parámetro no puede cambiar durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="2895b-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="2895b-112">La función puede cambiar el contenido en esa dirección.</span><span class="sxs-lookup"><span data-stu-id="2895b-112">The function can change the contents at that address.</span></span>

 

 




