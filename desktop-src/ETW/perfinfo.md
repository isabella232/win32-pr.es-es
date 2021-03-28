---
description: Esta clase es la clase primaria para los eventos de contador de rendimiento. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: Clase PerfInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984514"
---
# <a name="perfinfo-class"></a><span data-ttu-id="aa7e2-104">Clase PerfInfo</span><span class="sxs-lookup"><span data-stu-id="aa7e2-104">PerfInfo class</span></span>

<span data-ttu-id="aa7e2-105">Esta clase es la clase primaria para los eventos de contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-105">This class is the parent class for performance counter events.</span></span>

<span data-ttu-id="aa7e2-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa7e2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa7e2-107">Syntax</span></span>

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="aa7e2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa7e2-108">Members</span></span>

<span data-ttu-id="aa7e2-109">La clase **PerfInfo** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-109">The **PerfInfo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa7e2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa7e2-110">Remarks</span></span>

<span data-ttu-id="aa7e2-111">Para habilitar los eventos de llamada a procedimiento diferida (DPC) en una sesión de registro del kernel de NT, especifique la marca de DPC de la **marca de \_ seguimiento \_ \_ de eventos** en el miembro **EnableFlags** de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="aa7e2-111">To enable deferred procedure call (DPC) events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="aa7e2-112">También puede especificar una o varias de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="aa7e2-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="aa7e2-113">**\_interrupción de \_ marca de seguimiento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="aa7e2-113">**EVENT\_TRACE\_FLAG\_INTERRUPT**</span></span>
-   <span data-ttu-id="aa7e2-114">**\_Perfil de \_ marca de seguimiento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="aa7e2-114">**EVENT\_TRACE\_FLAG\_PROFILE**</span></span>
-   <span data-ttu-id="aa7e2-115">**marca de seguimiento de eventos \_ \_ \_ SYSTEMCALL**</span><span class="sxs-lookup"><span data-stu-id="aa7e2-115">**EVENT\_TRACE\_FLAG\_SYSTEMCALL**</span></span>

<span data-ttu-id="aa7e2-116">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de DPC llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**PerfInfoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="aa7e2-116">Event trace consumers can implement special processing for DPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PerfInfoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="aa7e2-117">Utilice los siguientes tipos de eventos para identificar el evento real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-117">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="aa7e2-118">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="aa7e2-118">Event type</span></span>           | <span data-ttu-id="aa7e2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa7e2-119">Description</span></span>                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7e2-120">Valor del tipo de evento, 46</span><span class="sxs-lookup"><span data-stu-id="aa7e2-120">Event type value, 46</span></span> | <span data-ttu-id="aa7e2-121">Evento de perfil muestreado.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-121">Sampled profile event.</span></span> <span data-ttu-id="aa7e2-122">La clase MOF [**SampledProfile**](sampledprofile.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-122">The [**SampledProfile**](sampledprofile.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="aa7e2-123">Valor del tipo de evento, 51</span><span class="sxs-lookup"><span data-stu-id="aa7e2-123">Event type value, 51</span></span> | <span data-ttu-id="aa7e2-124">Evento de entrada de llamada del sistema.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-124">System call enter event.</span></span> <span data-ttu-id="aa7e2-125">La clase MOF [**SysCallEnter**](syscallenter.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-125">The [**SysCallEnter**](syscallenter.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="aa7e2-126">Valor del tipo de evento, 52</span><span class="sxs-lookup"><span data-stu-id="aa7e2-126">Event type value, 52</span></span> | <span data-ttu-id="aa7e2-127">Evento de salida de llamada del sistema.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-127">System call exit event.</span></span> <span data-ttu-id="aa7e2-128">La clase MOF [**SysCallExit**](syscallexit.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-128">The [**SysCallExit**](syscallexit.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="aa7e2-129">Valor del tipo de evento, 66</span><span class="sxs-lookup"><span data-stu-id="aa7e2-129">Event type value, 66</span></span> | <span data-ttu-id="aa7e2-130">Evento de DPC de subproceso.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-130">Threaded DPC event.</span></span> <span data-ttu-id="aa7e2-131">La clase MOF de [**DPC**](dpc.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-131">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                          |
| <span data-ttu-id="aa7e2-132">Valor del tipo de evento, 67</span><span class="sxs-lookup"><span data-stu-id="aa7e2-132">Event type value, 67</span></span> | <span data-ttu-id="aa7e2-133">Evento de la rutina de servicio de interrupción (ISR).</span><span class="sxs-lookup"><span data-stu-id="aa7e2-133">Interrupt service routine (ISR) event.</span></span> <span data-ttu-id="aa7e2-134">La clase MOF de [**ISR**](isr.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-134">The [**ISR**](isr.md) MOF class defines the event data for this event.</span></span>       |
| <span data-ttu-id="aa7e2-135">Valor del tipo de evento, 68</span><span class="sxs-lookup"><span data-stu-id="aa7e2-135">Event type value, 68</span></span> | <span data-ttu-id="aa7e2-136">Evento de DPC.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-136">DPC event.</span></span> <span data-ttu-id="aa7e2-137">La clase MOF de [**DPC**](dpc.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-137">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="aa7e2-138">Valor del tipo de evento, 69</span><span class="sxs-lookup"><span data-stu-id="aa7e2-138">Event type value, 69</span></span> | <span data-ttu-id="aa7e2-139">Evento de temporizador de DPC.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-139">DPC timer event.</span></span> <span data-ttu-id="aa7e2-140">La clase MOF de [**DPC**](dpc.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="aa7e2-140">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="aa7e2-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa7e2-141">Requirements</span></span>



| <span data-ttu-id="aa7e2-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa7e2-142">Requirement</span></span> | <span data-ttu-id="aa7e2-143">Value</span><span class="sxs-lookup"><span data-stu-id="aa7e2-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa7e2-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa7e2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="aa7e2-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aa7e2-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa7e2-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa7e2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="aa7e2-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa7e2-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
