---
title: Evitar el polimorfismo
description: Los nuevos tipos de datos incluyen dos tipos polimórficos, INT \_ ptr y Long \_ PTR.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- polimorfismo 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357628"
---
# <a name="avoiding-polymorphism"></a><span data-ttu-id="e2089-104">Evitar el polimorfismo</span><span class="sxs-lookup"><span data-stu-id="e2089-104">Avoiding Polymorphism</span></span>

<span data-ttu-id="e2089-105">Los nuevos tipos de datos incluyen dos tipos polimórficos, **int \_ ptr** y **Long \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="e2089-105">The new data types include two polymorphic types, **INT\_PTR** and **LONG\_PTR**.</span></span> <span data-ttu-id="e2089-106">En Windows de 32 bits, el **int \_ ptr** se asigna a **int** y **Long \_ ptr** se asigna a **Long**.</span><span class="sxs-lookup"><span data-stu-id="e2089-106">On 32-bit Windows, the **INT\_PTR** maps to **int** and the **LONG\_PTR** maps to **long**.</span></span> <span data-ttu-id="e2089-107">En Windows de 64 bits, ambos tipos se asignan al tipo intrínseco **\_ \_ Int64** .</span><span class="sxs-lookup"><span data-stu-id="e2089-107">On 64-bit Windows, both types map to the **\_\_int64** intrinsic type.</span></span> <span data-ttu-id="e2089-108">El compilador MIDL admite estos tipos para llamadas a procedimientos remotos, pero hay una limitación inherente que debe tener en cuenta al usarlos en un entorno distribuido.</span><span class="sxs-lookup"><span data-stu-id="e2089-108">The MIDL compiler supports these types for remote procedure calls, but there is an inherent limitation that you must keep in mind when using them in a distributed environment.</span></span> <span data-ttu-id="e2089-109">Asegúrese de comentar el código según corresponda.</span><span class="sxs-lookup"><span data-stu-id="e2089-109">Be sure to comment your code accordingly.</span></span>

<span data-ttu-id="e2089-110">Independientemente del tamaño de la plataforma, el tamaño de conexión de estos tipos polimórficos es siempre de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e2089-110">Regardless of the platform size, the wire size of these polymorphic types is always 32 bits.</span></span> <span data-ttu-id="e2089-111">Al calcular las referencias de en Windows de 64 bits, el signo de la biblioteca en tiempo de ejecución extiende los valores con signo y asigna cero a los bytes de orden superior para un valor sin signo.</span><span class="sxs-lookup"><span data-stu-id="e2089-111">When unmarshaling on 64-bit Windows, the run-time library sign extends signed values and assigns zero to the high-order bytes for an unsigned value.</span></span> <span data-ttu-id="e2089-112">Al colocar un valor de 64 bits en la conexión, el tiempo de ejecución trunca los bytes de orden superior.</span><span class="sxs-lookup"><span data-stu-id="e2089-112">When putting a 64-bit value on the wire, the run time truncates the high-order bytes.</span></span> <span data-ttu-id="e2089-113">Por lo tanto, solo se pueden usar los valores de 32 bits de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="e2089-113">Thus, only the low-order 32-bit values are usable.</span></span>

<span data-ttu-id="e2089-114">Use los tipos polimórficos solo cuando sea necesario para la migración.</span><span class="sxs-lookup"><span data-stu-id="e2089-114">Use the polymorphic types only when necessary for porting.</span></span> <span data-ttu-id="e2089-115">En el caso de las nuevas interfaces, use los tipos enteros intrínsecos de MIDL **\_ \_ Int32** e **\_ \_ Int64**, o bien use un tipo de puntero o un identificador de contexto, lo que sea más adecuado para el tipo de datos que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="e2089-115">For new interfaces, use the MIDL intrinsic integer types **\_\_int32** and **\_\_int64**, or use a pointer type or context handle, whichever is most appropriate for the kind of data being transferred.</span></span>

<span data-ttu-id="e2089-116">El compilador de 64 bits admite un nuevo **\_ \_ int3264** intrínseco polimórfico.</span><span class="sxs-lookup"><span data-stu-id="e2089-116">The 64-bit compiler supports a new polymorphic intrinsic **\_\_int3264**.</span></span> <span data-ttu-id="e2089-117">De nuevo, este tipo se desarrolló para admitir los esfuerzos de migración, en este caso para admitir los tipos de **uint \_ ptr** de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="e2089-117">Again, this type was developed to support porting efforts, in this case to support the **UINT\_PTR** types transparently.</span></span> <span data-ttu-id="e2089-118">(Otro intrínseco, **\_ \_ long3264**, admitirá el tipo de **ULong \_ ptr** ). No use **\_ \_ int3264** directamente; use el tipo **int \_ ptr** cuando necesite un tipo polimórfico por motivos de portabilidad.</span><span class="sxs-lookup"><span data-stu-id="e2089-118">(Another intrinsic, **\_\_long3264**, will support the **ULONG\_PTR** type.) Do not use **\_\_int3264** directly; use the **INT\_PTR** type when you need a polymorphic type for porting reasons.</span></span>

 

 




