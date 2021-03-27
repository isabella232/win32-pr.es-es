---
description: Esta clase es la clase primaria para los eventos de proceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Process_V2 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: c055dc1f78da13c0dfa29bea948a8f0c94363ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002703"
---
# <a name="process_v2-class"></a><span data-ttu-id="1d815-104">Process \_ V2 (clase)</span><span class="sxs-lookup"><span data-stu-id="1d815-104">Process\_V2 class</span></span>

<span data-ttu-id="1d815-105">Esta clase es la clase primaria para los eventos de proceso.</span><span class="sxs-lookup"><span data-stu-id="1d815-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="1d815-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="1d815-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d815-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d815-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1d815-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d815-108">Members</span></span>

<span data-ttu-id="1d815-109">La clase **Process** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="1d815-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d815-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d815-110">Remarks</span></span>

<span data-ttu-id="1d815-111">Para habilitar los eventos de procesamiento en una sesión de registro del kernel de NT, especifique la marca de  proceso de marca de seguimiento de eventos en el miembro EnableFlags [](/windows/win32/api/evntrace/nf-evntrace-starttracea) de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función StartTrace. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1d815-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="1d815-112">También puede especificar la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="1d815-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="1d815-113">**\_ \_ \_ contadores del proceso de marca de seguimiento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="1d815-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="1d815-114">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de proceso llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ProcessGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="1d815-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="1d815-115">Utilice los siguientes tipos de eventos para identificar el evento de proceso real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="1d815-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="1d815-116">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="1d815-116">Event type</span></span>                                                      | <span data-ttu-id="1d815-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d815-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d815-118">**Evento \_ de Tipo de seguimiento \_ \_ End**(el valor de tipo de evento es 2)</span><span class="sxs-lookup"><span data-stu-id="1d815-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="1d815-119">Evento de finalización de proceso.</span><span class="sxs-lookup"><span data-stu-id="1d815-119">End process event.</span></span> <span data-ttu-id="1d815-120">La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d815-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="1d815-121">**Evento \_ de Tipo de seguimiento \_ \_ Start**(el valor del tipo de evento es 1)</span><span class="sxs-lookup"><span data-stu-id="1d815-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="1d815-122">Evento de inicio del proceso.</span><span class="sxs-lookup"><span data-stu-id="1d815-122">Start process event.</span></span> <span data-ttu-id="1d815-123">La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d815-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="1d815-124">Valor del tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="1d815-124">Event type value, 3</span></span>                                             | <span data-ttu-id="1d815-125">Iniciar el evento del proceso de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="1d815-125">Start data collection process event.</span></span> <span data-ttu-id="1d815-126">Enumera los procesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="1d815-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="1d815-127">La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d815-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="1d815-128">Valor del tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="1d815-128">Event type value, 4</span></span>                                             | <span data-ttu-id="1d815-129">Evento finalizar proceso de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="1d815-129">End data collection process event.</span></span> <span data-ttu-id="1d815-130">Enumera los procesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="1d815-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="1d815-131">La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d815-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="1d815-132">Valor del tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="1d815-132">Event type value, 32</span></span>                                            | <span data-ttu-id="1d815-133">Evento de contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1d815-133">Performance counters event.</span></span> <span data-ttu-id="1d815-134">La clase de MOF [**Process \_ V2 \_ TypeGroup2**](process-v2-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d815-134">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                                                          |
| <span data-ttu-id="1d815-135">Valor del tipo de evento, 33</span><span class="sxs-lookup"><span data-stu-id="1d815-135">Event type value, 33</span></span>                                            | <span data-ttu-id="1d815-136">Detención de los contadores de rendimiento en el inicio de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1d815-136">Rundown of the performance counters at the start of the session.</span></span> <span data-ttu-id="1d815-137">La clase de MOF [**Process \_ V2 \_ TypeGroup2**](process-v2-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d815-137">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                     |
| <span data-ttu-id="1d815-138">Valor del tipo de evento, 39</span><span class="sxs-lookup"><span data-stu-id="1d815-138">Event type value, 39</span></span>                                            | <span data-ttu-id="1d815-139">Evento de proceso inactivo.</span><span class="sxs-lookup"><span data-stu-id="1d815-139">Defunct process event.</span></span> <span data-ttu-id="1d815-140">La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d815-140">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |



 

<span data-ttu-id="1d815-141">Los eventos de inicio de procesos y subprocesos pueden registrarse en el contexto del proceso o subproceso primario.</span><span class="sxs-lookup"><span data-stu-id="1d815-141">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="1d815-142">Como resultado, es posible que los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se está creando.</span><span class="sxs-lookup"><span data-stu-id="1d815-142">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="1d815-143">Este es el motivo por el que estos eventos contienen los identificadores de proceso y de subproceso en los datos de evento (además de los del encabezado de evento).</span><span class="sxs-lookup"><span data-stu-id="1d815-143">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d815-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d815-144">Requirements</span></span>



| <span data-ttu-id="1d815-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d815-145">Requirement</span></span> | <span data-ttu-id="1d815-146">Value</span><span class="sxs-lookup"><span data-stu-id="1d815-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="1d815-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d815-147">Minimum supported client</span></span><br/> | <span data-ttu-id="1d815-148">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="1d815-148">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="1d815-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d815-149">Minimum supported server</span></span><br/> | <span data-ttu-id="1d815-150">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="1d815-150">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d815-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d815-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d815-152">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="1d815-152">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="1d815-153">**Proceso**</span><span class="sxs-lookup"><span data-stu-id="1d815-153">**Process**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="1d815-154">**Procesar \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="1d815-154">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="1d815-155">**Procesar \_ v0**</span><span class="sxs-lookup"><span data-stu-id="1d815-155">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="1d815-156">**Proceso \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1d815-156">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 
