---
description: Evento de traza de administración de memoria para una operación libre del montón.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: Evento ETW_HEAP_EVENT_FREE (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: fd30eccb5848917d752441df79881078dc14d36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907879"
---
# <a name="etw_heap_event_free-event"></a><span data-ttu-id="40cdb-103">\_ \_ Evento libre de evento de montón ETW \_</span><span class="sxs-lookup"><span data-stu-id="40cdb-103">ETW\_HEAP\_EVENT\_FREE event</span></span>

<span data-ttu-id="40cdb-104">El **evento \_ \_ \_ gratuito del montón ETW** es un evento de seguimiento de administración de memoria para una operación libre del montón.</span><span class="sxs-lookup"><span data-stu-id="40cdb-104">The **ETW\_HEAP\_EVENT\_FREE** event is a memory management tracing event for a heap free operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a><span data-ttu-id="40cdb-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40cdb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40cdb-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="40cdb-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="40cdb-107">Identificador del montón en el que se asignó la memoria.</span><span class="sxs-lookup"><span data-stu-id="40cdb-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="40cdb-108">Este es el montón que controla una aplicación pasada a la función [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) cuando se asignó la memoria.</span><span class="sxs-lookup"><span data-stu-id="40cdb-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="40cdb-109">*Dirección*</span><span class="sxs-lookup"><span data-stu-id="40cdb-109">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="40cdb-110">Dirección de la memoria que se liberó.</span><span class="sxs-lookup"><span data-stu-id="40cdb-110">The address of the memory that was freed.</span></span>

</dd> <dt>

<span data-ttu-id="40cdb-111">*Origen*</span><span class="sxs-lookup"><span data-stu-id="40cdb-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="40cdb-112">El origen de la memoria que el asignador utilizó para la asignación del montón.</span><span class="sxs-lookup"><span data-stu-id="40cdb-112">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="40cdb-113">En la tabla siguiente se enumeran los posibles valores para el parámetro *source* tal y como se define en el archivo de encabezado *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="40cdb-113">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="40cdb-114">Value</span><span class="sxs-lookup"><span data-stu-id="40cdb-114">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="40cdb-115">Significado</span><span class="sxs-lookup"><span data-stu-id="40cdb-115">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="40cdb-116"><dt>**Memoria \_ de DESDE \_**</dt> la <dt>primera</dt> de la</span><span class="sxs-lookup"><span data-stu-id="40cdb-116"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="40cdb-117">Memoria de la lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="40cdb-117">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="40cdb-118"><dt>**Memoria \_ de DESDE \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="40cdb-118"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="40cdb-119">Memoria del montón de fragmentación baja.</span><span class="sxs-lookup"><span data-stu-id="40cdb-119">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="40cdb-120"><dt>**Memoria \_ de DESDE \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="40cdb-120"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="40cdb-121">Memoria de la ruta de acceso del código principal.</span><span class="sxs-lookup"><span data-stu-id="40cdb-121">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="40cdb-122"><dt> **Memoria \_ de \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="40cdb-122"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="40cdb-123">Memoria de c lentamente.</span><span class="sxs-lookup"><span data-stu-id="40cdb-123">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="40cdb-124"><dt>**Memoria \_ de DESDE \_ 5 no válidos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="40cdb-124"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="40cdb-125">Memoria no válida.</span><span class="sxs-lookup"><span data-stu-id="40cdb-125">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="40cdb-126"><dt>**Memoria \_ de DEL \_ \_ montón de segmentos**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="40cdb-126"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="40cdb-127">Este valor se reserva para uso futuro y nunca se devolverá.</span><span class="sxs-lookup"><span data-stu-id="40cdb-127">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40cdb-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40cdb-128">Remarks</span></span>

<span data-ttu-id="40cdb-129">El **evento \_ \_ \_ gratuito del montón ETW** se registra en todas las operaciones libres del montón.</span><span class="sxs-lookup"><span data-stu-id="40cdb-129">The **ETW\_HEAP\_EVENT\_FREE** event is logged on all heap free operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="40cdb-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40cdb-130">Requirements</span></span>



| <span data-ttu-id="40cdb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="40cdb-131">Requirement</span></span> | <span data-ttu-id="40cdb-132">Value</span><span class="sxs-lookup"><span data-stu-id="40cdb-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40cdb-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40cdb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="40cdb-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="40cdb-134">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="40cdb-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40cdb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="40cdb-136">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="40cdb-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="40cdb-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40cdb-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="40cdb-138"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="40cdb-138"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40cdb-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="40cdb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40cdb-140">Eventos de seguimiento de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="40cdb-140">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
