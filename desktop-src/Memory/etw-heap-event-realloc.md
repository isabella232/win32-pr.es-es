---
description: Evento de traza de administración de memoria para una operación de reasignación de montón.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: Evento ETW_HEAP_EVENT_REALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687448"
---
# <a name="etw_heap_event_realloc-event"></a><span data-ttu-id="599dc-103">Evento \_ de \_ evento REALLOC del montón ETW \_</span><span class="sxs-lookup"><span data-stu-id="599dc-103">ETW\_HEAP\_EVENT\_REALLOC event</span></span>

<span data-ttu-id="599dc-104">El evento de **\_ \_ evento \_ REALLOC del montón ETW** es un evento de seguimiento de administración de memoria para una operación de reasignación del montón.</span><span class="sxs-lookup"><span data-stu-id="599dc-104">The **ETW\_HEAP\_EVENT\_REALLOC** event is a memory management tracing event for a heap reallocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a><span data-ttu-id="599dc-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="599dc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="599dc-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="599dc-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="599dc-107">Identificador del montón en el que se asignó la memoria.</span><span class="sxs-lookup"><span data-stu-id="599dc-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="599dc-108">Este es el montón que controla una aplicación pasada a la función [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) cuando se asignó la memoria.</span><span class="sxs-lookup"><span data-stu-id="599dc-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="599dc-109">*La*</span><span class="sxs-lookup"><span data-stu-id="599dc-109">*NewAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="599dc-110">La nueva dirección de la memoria que se asignó.</span><span class="sxs-lookup"><span data-stu-id="599dc-110">The new address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="599dc-111">*OldAddress*</span><span class="sxs-lookup"><span data-stu-id="599dc-111">*OldAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="599dc-112">Dirección antigua de la memoria que se asignó previamente.</span><span class="sxs-lookup"><span data-stu-id="599dc-112">The old address of the memory that was previously allocated.</span></span>

</dd> <dt>

<span data-ttu-id="599dc-113">*NewSize*</span><span class="sxs-lookup"><span data-stu-id="599dc-113">*NewSize*</span></span> 
</dt> <dd>

<span data-ttu-id="599dc-114">Nuevo tamaño en bytes asignado desde el montón.</span><span class="sxs-lookup"><span data-stu-id="599dc-114">The new size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="599dc-115">*OldSize*</span><span class="sxs-lookup"><span data-stu-id="599dc-115">*OldSize*</span></span> 
</dt> <dd>

<span data-ttu-id="599dc-116">Tamaño anterior en bytes previamente asignado desde el montón.</span><span class="sxs-lookup"><span data-stu-id="599dc-116">The old size in bytes previously allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="599dc-117">*Origen*</span><span class="sxs-lookup"><span data-stu-id="599dc-117">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="599dc-118">El origen de la memoria que el asignador utilizó para la asignación del montón.</span><span class="sxs-lookup"><span data-stu-id="599dc-118">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="599dc-119">En la tabla siguiente se enumeran los posibles valores para el parámetro *source* tal y como se define en el archivo de encabezado *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="599dc-119">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="599dc-120">Value</span><span class="sxs-lookup"><span data-stu-id="599dc-120">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="599dc-121">Significado</span><span class="sxs-lookup"><span data-stu-id="599dc-121">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="599dc-122"><dt>**Memoria \_ de DESDE \_**</dt> la <dt>primera</dt> de la</span><span class="sxs-lookup"><span data-stu-id="599dc-122"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="599dc-123">Memoria de la lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="599dc-123">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="599dc-124"><dt>**Memoria \_ de DESDE \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="599dc-124"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="599dc-125">Memoria del montón de fragmentación baja.</span><span class="sxs-lookup"><span data-stu-id="599dc-125">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="599dc-126"><dt>**Memoria \_ de DESDE \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="599dc-126"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="599dc-127">Memoria de la ruta de acceso del código principal.</span><span class="sxs-lookup"><span data-stu-id="599dc-127">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="599dc-128"><dt> **Memoria \_ de \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="599dc-128"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="599dc-129">Memoria de c lentamente.</span><span class="sxs-lookup"><span data-stu-id="599dc-129">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="599dc-130"><dt>**Memoria \_ de DESDE \_ 5 no válidos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="599dc-130"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="599dc-131">Memoria no válida.</span><span class="sxs-lookup"><span data-stu-id="599dc-131">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="599dc-132"><dt>**Memoria \_ de DEL \_ \_ montón de segmentos**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="599dc-132"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="599dc-133">Este valor se reserva para uso futuro y nunca se devolverá.</span><span class="sxs-lookup"><span data-stu-id="599dc-133">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

<span data-ttu-id="599dc-134">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="599dc-134">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="599dc-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="599dc-135">Remarks</span></span>

<span data-ttu-id="599dc-136">El evento de **\_ \_ evento \_ REALLOC del montón ETW** se registra en todas las reasignaciones del montón.</span><span class="sxs-lookup"><span data-stu-id="599dc-136">The **ETW\_HEAP\_EVENT\_REALLOC** event is logged on all heap reallocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="599dc-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="599dc-137">Requirements</span></span>



| <span data-ttu-id="599dc-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="599dc-138">Requirement</span></span> | <span data-ttu-id="599dc-139">Value</span><span class="sxs-lookup"><span data-stu-id="599dc-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="599dc-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="599dc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="599dc-141">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="599dc-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="599dc-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="599dc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="599dc-143">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="599dc-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="599dc-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="599dc-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="599dc-145"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="599dc-145"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="599dc-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="599dc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599dc-147">Eventos de seguimiento de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="599dc-147">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
