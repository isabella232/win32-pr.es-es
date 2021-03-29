---
title: Montón
description: Un montón realiza un seguimiento de un grupo de asignaciones que se liberan como una unidad.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Servicios Web de montón para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421656"
---
# <a name="heap"></a><span data-ttu-id="44286-106">Montón</span><span class="sxs-lookup"><span data-stu-id="44286-106">Heap</span></span>

<span data-ttu-id="44286-107">Un montón realiza un seguimiento de un grupo de asignaciones que se liberan como una unidad.</span><span class="sxs-lookup"><span data-stu-id="44286-107">A heap tracks a group of allocations that are freed as a unit.</span></span>

<span data-ttu-id="44286-108">Esto le permite evitar patrones complejos de asignación y desasignación de memoria cuando se usa WWSAPI.</span><span class="sxs-lookup"><span data-stu-id="44286-108">This allows you to avoid complex patterns of allocating and deallocating memory when you use the WWSAPI.</span></span>


<span data-ttu-id="44286-109">Hay un montón asociado a cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="44286-109">There is a heap associated with every message.</span></span> <span data-ttu-id="44286-110">A medida que se envía un mensaje, o cuando se recibe un mensaje, se usa el montón del mensaje para cualquier asignación relacionada con ese mensaje concreto.</span><span class="sxs-lookup"><span data-stu-id="44286-110">As a message is being sent, or as a message is being received, the heap of the message is used for any allocations relating to that particular message.</span></span> <span data-ttu-id="44286-111">Una vez que se envía o recibe un mensaje, se restablece el montón (que limpia las asignaciones relacionadas con el mensaje determinado).</span><span class="sxs-lookup"><span data-stu-id="44286-111">After a message is sent or received, the heap is reset (which cleans up any allocations related to the particular message).</span></span>

<span data-ttu-id="44286-112">Los montones también se pueden usar para almacenar datos de mensajes de forma independiente de la duración de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="44286-112">Heaps can also be used to store message data separately from the lifetime of a message.</span></span> <span data-ttu-id="44286-113">Muchas de las especificaciones de permiso de la API del montón que se van a usar al leer los datos proporcionan un control explícito sobre la duración de cualquier lectura de datos.</span><span class="sxs-lookup"><span data-stu-id="44286-113">Many of the API's allow specification of the heap to use when reading data give explicit control over the lifetime of any data read.</span></span>

<span data-ttu-id="44286-114">Se garantiza que las asignaciones de un montón estén alineadas en al menos un límite de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="44286-114">Allocations from a heap are guaranteed to be aligned on at least an 8 byte boundary.</span></span>

<span data-ttu-id="44286-115">Las asignaciones de cero bytes devolverán un puntero no nulo.</span><span class="sxs-lookup"><span data-stu-id="44286-115">Zero byte allocations will return a non-NULL pointer.</span></span>

<span data-ttu-id="44286-116">En Windows 7, si PageHeap está habilitada, se usa un montón devuelto de HeapCreate para administrar la memoria.</span><span class="sxs-lookup"><span data-stu-id="44286-116">In Windows 7, if PageHeap is enabled, a heap returned from HeapCreate is used to manage the memory.</span></span> <span data-ttu-id="44286-117">En este caso, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) se asigna directamente a HeapAlloc y [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) a HeapDestroy.</span><span class="sxs-lookup"><span data-stu-id="44286-117">In this case, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) maps directly to HeapAlloc and [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) maps to HeapDestroy.</span></span>

<span data-ttu-id="44286-118">La siguiente enumeración se usa con el montón:</span><span class="sxs-lookup"><span data-stu-id="44286-118">The following enumeration is used with the heap:</span></span>

-   [<span data-ttu-id="44286-119">**identificador de la \_ propiedad del montón WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44286-119">**WS\_HEAP\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

<span data-ttu-id="44286-120">Las siguientes funciones se usan con el montón:</span><span class="sxs-lookup"><span data-stu-id="44286-120">The following functions are used with the heap:</span></span>

-   [<span data-ttu-id="44286-121">**WsAlloc**</span><span class="sxs-lookup"><span data-stu-id="44286-121">**WsAlloc**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [<span data-ttu-id="44286-122">**WsCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="44286-122">**WsCreateHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [<span data-ttu-id="44286-123">**WsFreeHeap**</span><span class="sxs-lookup"><span data-stu-id="44286-123">**WsFreeHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [<span data-ttu-id="44286-124">**WsGetHeapProperty**</span><span class="sxs-lookup"><span data-stu-id="44286-124">**WsGetHeapProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [<span data-ttu-id="44286-125">**WsResetHeap**</span><span class="sxs-lookup"><span data-stu-id="44286-125">**WsResetHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

<span data-ttu-id="44286-126">El siguiente identificador se usa con el montón:</span><span class="sxs-lookup"><span data-stu-id="44286-126">The following handle is used with the heap:</span></span>

-   [<span data-ttu-id="44286-127">\_montón WS</span><span class="sxs-lookup"><span data-stu-id="44286-127">WS\_HEAP</span></span>](ws-heap.md)

<span data-ttu-id="44286-128">Las siguientes estructuras se usan con el montón:</span><span class="sxs-lookup"><span data-stu-id="44286-128">The following structures are used with the heap:</span></span>

-   [<span data-ttu-id="44286-129">**\_propiedades del montón WS \_**</span><span class="sxs-lookup"><span data-stu-id="44286-129">**WS\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [<span data-ttu-id="44286-130">**\_propiedad del montón WS \_**</span><span class="sxs-lookup"><span data-stu-id="44286-130">**WS\_HEAP\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




