---
description: Evento de seguimiento de administración de memoria para una operación de asignación de montón.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: Evento ETW_HEAP_EVENT_ALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360323"
---
# <a name="etw_heap_event_alloc-event"></a><span data-ttu-id="79882-103">\_Evento de \_ asignación de eventos del montón ETW \_</span><span class="sxs-lookup"><span data-stu-id="79882-103">ETW\_HEAP\_EVENT\_ALLOC event</span></span>

<span data-ttu-id="79882-104">El evento de asignación de **\_ eventos del montón \_ \_ ETW** es un evento de seguimiento de administración de memoria para una operación de asignación en el montón.</span><span class="sxs-lookup"><span data-stu-id="79882-104">The **ETW\_HEAP\_EVENT\_ALLOC** event is a memory management tracing event for a heap allocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a><span data-ttu-id="79882-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79882-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79882-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="79882-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="79882-107">Identificador del montón en el que se asignó la memoria.</span><span class="sxs-lookup"><span data-stu-id="79882-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="79882-108">Este es el montón que controla una aplicación pasada a la función [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) cuando se asignó la memoria.</span><span class="sxs-lookup"><span data-stu-id="79882-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="79882-109">*Tamaño*</span><span class="sxs-lookup"><span data-stu-id="79882-109">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="79882-110">Tamaño en bytes asignado del montón.</span><span class="sxs-lookup"><span data-stu-id="79882-110">The size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="79882-111">*Dirección*</span><span class="sxs-lookup"><span data-stu-id="79882-111">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="79882-112">Dirección de la memoria que se asignó.</span><span class="sxs-lookup"><span data-stu-id="79882-112">The address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="79882-113">*Origen*</span><span class="sxs-lookup"><span data-stu-id="79882-113">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="79882-114">El origen de la memoria que el asignador utilizó para la asignación del montón.</span><span class="sxs-lookup"><span data-stu-id="79882-114">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="79882-115">En la tabla siguiente se enumeran los posibles valores para el parámetro *source* tal y como se define en el archivo de encabezado *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="79882-115">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="79882-116">Value</span><span class="sxs-lookup"><span data-stu-id="79882-116">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="79882-117">Significado</span><span class="sxs-lookup"><span data-stu-id="79882-117">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="79882-118"><dt>**Memoria \_ de DESDE \_**</dt> la <dt>primera</dt> de la</span><span class="sxs-lookup"><span data-stu-id="79882-118"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="79882-119">Memoria de la lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="79882-119">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="79882-120"><dt>**Memoria \_ de DESDE \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="79882-120"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="79882-121">Memoria del montón de fragmentación baja.</span><span class="sxs-lookup"><span data-stu-id="79882-121">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="79882-122"><dt>**Memoria \_ de DESDE \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="79882-122"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="79882-123">Memoria de la ruta de acceso del código principal.</span><span class="sxs-lookup"><span data-stu-id="79882-123">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="79882-124"><dt> **Memoria \_ de \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="79882-124"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="79882-125">Memoria de la ruta de acceso lenta.</span><span class="sxs-lookup"><span data-stu-id="79882-125">Memory from slow path.</span></span><br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="79882-126"><dt>**Memoria \_ de DESDE \_ 5 no válidos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="79882-126"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="79882-127">Memoria no válida.</span><span class="sxs-lookup"><span data-stu-id="79882-127">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="79882-128"><dt>**Memoria \_ de DEL \_ \_ montón de segmentos**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="79882-128"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="79882-129">Este valor se reserva para uso futuro y nunca se devolverá.</span><span class="sxs-lookup"><span data-stu-id="79882-129">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79882-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79882-130">Remarks</span></span>

<span data-ttu-id="79882-131">El evento de **\_ asignación de \_ eventos \_ del montón ETW** se registra en todas las asignaciones del montón.</span><span class="sxs-lookup"><span data-stu-id="79882-131">The **ETW\_HEAP\_EVENT\_ALLOC** event is logged on all heap allocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="79882-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79882-132">Requirements</span></span>



| <span data-ttu-id="79882-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="79882-133">Requirement</span></span> | <span data-ttu-id="79882-134">Value</span><span class="sxs-lookup"><span data-stu-id="79882-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79882-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79882-135">Minimum supported client</span></span><br/> | <span data-ttu-id="79882-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="79882-136">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="79882-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79882-137">Minimum supported server</span></span><br/> | <span data-ttu-id="79882-138">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="79882-138">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="79882-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79882-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="79882-140"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="79882-140"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79882-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="79882-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79882-142">Eventos de seguimiento de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="79882-142">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
