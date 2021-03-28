---
description: Esta clase es la clase primaria para los eventos de error de página. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984479"
---
# <a name="pagefault_v2-class"></a><span data-ttu-id="d5282-104">\_Clase errores V2</span><span class="sxs-lookup"><span data-stu-id="d5282-104">PageFault\_V2 class</span></span>

<span data-ttu-id="d5282-105">Esta clase es la clase primaria para los eventos de error de página.</span><span class="sxs-lookup"><span data-stu-id="d5282-105">This class is the parent class for page fault events.</span></span>

<span data-ttu-id="d5282-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="d5282-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5282-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5282-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="d5282-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d5282-108">Members</span></span>

<span data-ttu-id="d5282-109">La clase **errores \_ V2** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="d5282-109">The **PageFault\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5282-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5282-110">Remarks</span></span>

<span data-ttu-id="d5282-111">Para habilitar todos los eventos de error de página en una sesión de registro del kernel de NT, especifique la marca **Event \_ Trace \_ Flag \_ Memory \_ \_ faults** en el miembro **EnableFlags** de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="d5282-111">To enable all page fault events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="d5282-112">También puede especificar las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d5282-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="d5282-113">**\_ \_ \_ \_ errores severos de memoria de marca de seguimiento \_ de eventos**</span><span class="sxs-lookup"><span data-stu-id="d5282-113">**EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS**</span></span>
-   <span data-ttu-id="d5282-114">**\_ \_ asignación virtual de marca de seguimiento de \_ eventos \_**</span><span class="sxs-lookup"><span data-stu-id="d5282-114">**EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC**</span></span>

<span data-ttu-id="d5282-115">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para todos los eventos de error de página llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**PageFaultGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="d5282-115">Event trace consumers can implement special processing for all page fault events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PageFaultGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="d5282-116">Utilice los siguientes tipos de eventos para identificar el evento de memoria real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="d5282-116">Use the following event types to identify the actual memory event when consuming events.</span></span>



| <span data-ttu-id="d5282-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="d5282-117">Event type</span></span>                                                     | <span data-ttu-id="d5282-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5282-118">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5282-119">Tipo de seguimiento de evento \_ \_ \_ mm \_ Cow (el valor de tipo de evento es 12)</span><span class="sxs-lookup"><span data-stu-id="d5282-119">EVENT\_TRACE\_TYPE\_MM\_COW(Event type value is 12)</span></span><br/> | <span data-ttu-id="d5282-120">Evento de copia en escritura.</span><span class="sxs-lookup"><span data-stu-id="d5282-120">Copy-on-write event.</span></span> <span data-ttu-id="d5282-121">La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-121">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d5282-122">Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-122">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>     |
| <span data-ttu-id="d5282-123">Tipo de seguimiento de eventos \_ \_ \_ mm \_ DZF (el valor de tipo de evento es 11)</span><span class="sxs-lookup"><span data-stu-id="d5282-123">EVENT\_TRACE\_TYPE\_MM\_DZF(Event type value is 11)</span></span><br/> | <span data-ttu-id="d5282-124">Evento de error de petición cero.</span><span class="sxs-lookup"><span data-stu-id="d5282-124">Demand zero fault event.</span></span> <span data-ttu-id="d5282-125">La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-125">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d5282-126">Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-126">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span> |
| <span data-ttu-id="d5282-127">Tipo de seguimiento de eventos \_ \_ \_ mm \_ GPF (el valor de tipo de evento es 13)</span><span class="sxs-lookup"><span data-stu-id="d5282-127">EVENT\_TRACE\_TYPE\_MM\_GPF(Event type value is 13)</span></span><br/> | <span data-ttu-id="d5282-128">Evento de error de página de protección.</span><span class="sxs-lookup"><span data-stu-id="d5282-128">Guard page fault event.</span></span> <span data-ttu-id="d5282-129">La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-129">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d5282-130">Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-130">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="d5282-131">Tipo de seguimiento de eventos \_ \_ \_ mm \_ HPF (el valor de tipo de evento es 14)</span><span class="sxs-lookup"><span data-stu-id="d5282-131">EVENT\_TRACE\_TYPE\_MM\_HPF(Event type value is 14)</span></span><br/> | <span data-ttu-id="d5282-132">Evento de error de página de hardware.</span><span class="sxs-lookup"><span data-stu-id="d5282-132">Hard page fault event.</span></span> <span data-ttu-id="d5282-133">La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-133">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d5282-134">Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-134">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>   |
| <span data-ttu-id="d5282-135">Tipo de seguimiento de eventos \_ \_ \_ mm \_ TF (el valor de tipo de evento es 10)</span><span class="sxs-lookup"><span data-stu-id="d5282-135">EVENT\_TRACE\_TYPE\_MM\_TF(Event type value is 10)</span></span><br/>  | <span data-ttu-id="d5282-136">Evento de error de transición.</span><span class="sxs-lookup"><span data-stu-id="d5282-136">Transition fault event.</span></span> <span data-ttu-id="d5282-137">La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-137">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d5282-138">Antes de Windows Vista, la clase MOF [**errores \_ TransitionFault**](pagefault-transitionfault.md) define el evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-138">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="d5282-139">Tipo de seguimiento de evento \_ \_ \_ mm \_ AV (el valor de tipo de evento es 15)</span><span class="sxs-lookup"><span data-stu-id="d5282-139">EVENT\_TRACE\_TYPE\_MM\_AV(Event type value is 15)</span></span><br/>  | <span data-ttu-id="d5282-140">Evento de infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="d5282-140">Access violation event.</span></span> <span data-ttu-id="d5282-141">La clase MOF [**errores \_ TypeGroup1**](pagefault-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-141">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                           |
| <span data-ttu-id="d5282-142">Valor del tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="d5282-142">Event type value, 32</span></span>                                           | <span data-ttu-id="d5282-143">Evento de error de página de hardware. La clase MOF [**errores \_ HardFault**](pagefault-hardfault.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-143">Hard page fault event.The [**PageFault\_HardFault**](pagefault-hardfault.md) MOF class defines the event data for this event.</span></span>                                                                                                                               |
| <span data-ttu-id="d5282-144">Valor del tipo de evento, 105</span><span class="sxs-lookup"><span data-stu-id="d5282-144">Event type value, 105</span></span>                                          | <span data-ttu-id="d5282-145">Carga de la imagen en el evento de archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="d5282-145">Image load in page file event.</span></span> <span data-ttu-id="d5282-146">La clase MOF [**errores \_ ImageLoadBacked**](pagefault-imageloadbacked.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-146">The [**PageFault\_ImageLoadBacked**](pagefault-imageloadbacked.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="d5282-147">Valor del tipo de evento, 98</span><span class="sxs-lookup"><span data-stu-id="d5282-147">Event type value, 98</span></span>                                           | <span data-ttu-id="d5282-148">Evento de asignación virtual.</span><span class="sxs-lookup"><span data-stu-id="d5282-148">Virtual allocation event.</span></span> <span data-ttu-id="d5282-149">La clase [**VirtualAlloc**](pagefault-virtualalloc.md) de mof define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-149">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="d5282-150">Valor del tipo de evento, 99</span><span class="sxs-lookup"><span data-stu-id="d5282-150">Event type value, 99</span></span>                                           | <span data-ttu-id="d5282-151">Evento gratuito virtual.</span><span class="sxs-lookup"><span data-stu-id="d5282-151">Virtual free event.</span></span> <span data-ttu-id="d5282-152">La clase [**VirtualAlloc**](pagefault-virtualalloc.md) de mof define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5282-152">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                      |



 

<span data-ttu-id="d5282-153">Puede usar los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar el proceso o subproceso con errores.</span><span class="sxs-lookup"><span data-stu-id="d5282-153">You can use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the faulting process or thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5282-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5282-154">Requirements</span></span>



| <span data-ttu-id="d5282-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5282-155">Requirement</span></span> | <span data-ttu-id="d5282-156">Value</span><span class="sxs-lookup"><span data-stu-id="d5282-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5282-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5282-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d5282-158">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d5282-158">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d5282-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5282-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d5282-160">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5282-160">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
