---
description: 'Process_V2 clase : esta clase es la clase primaria para los eventos de proceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Process_V2 clase
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
ms.openlocfilehash: 77d700e7847d0ad19a019985a4e19343ce8f383d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106303"
---
# <a name="process_v2-class"></a><span data-ttu-id="84ecc-104">Clase Process \_ V2</span><span class="sxs-lookup"><span data-stu-id="84ecc-104">Process\_V2 class</span></span>

<span data-ttu-id="84ecc-105">Esta clase es la clase primaria para los eventos de proceso.</span><span class="sxs-lookup"><span data-stu-id="84ecc-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="84ecc-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="84ecc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="84ecc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84ecc-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="84ecc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="84ecc-108">Members</span></span>

<span data-ttu-id="84ecc-109">La **clase Process** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="84ecc-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="84ecc-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84ecc-110">Remarks</span></span>

<span data-ttu-id="84ecc-111">Para habilitar los eventos de proceso en una sesión de registro del kernel de NT, especifique la marca **EVENT \_ TRACE FLAG \_ \_ PROCESS** en el **miembro EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="84ecc-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="84ecc-112">También puede especificar la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="84ecc-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="84ecc-113">**CONTADORES \_ DE PROCESO DE MARCA DE SEGUIMIENTO DE \_ \_ \_ EVENTOS**</span><span class="sxs-lookup"><span data-stu-id="84ecc-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="84ecc-114">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de proceso llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ProcessGuid**](nt-kernel-logger-constants.md) como *parámetro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="84ecc-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="84ecc-115">Use los siguientes tipos de eventos para identificar el evento de proceso real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="84ecc-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="84ecc-116">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="84ecc-116">Event type</span></span>                                                      | <span data-ttu-id="84ecc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="84ecc-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84ecc-118">**EVENT \_ TRACE \_ TYPE \_ END**(el valor del tipo de evento es 2)</span><span class="sxs-lookup"><span data-stu-id="84ecc-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="84ecc-119">Evento de proceso final.</span><span class="sxs-lookup"><span data-stu-id="84ecc-119">End process event.</span></span> <span data-ttu-id="84ecc-120">La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="84ecc-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="84ecc-121">**EVENT \_ TRACE \_ TYPE \_ START**(el valor del tipo de evento es 1)</span><span class="sxs-lookup"><span data-stu-id="84ecc-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="84ecc-122">Evento de inicio del proceso.</span><span class="sxs-lookup"><span data-stu-id="84ecc-122">Start process event.</span></span> <span data-ttu-id="84ecc-123">La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="84ecc-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="84ecc-124">Valor de tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="84ecc-124">Event type value, 3</span></span>                                             | <span data-ttu-id="84ecc-125">Evento de inicio del proceso de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="84ecc-125">Start data collection process event.</span></span> <span data-ttu-id="84ecc-126">Enumera los procesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="84ecc-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="84ecc-127">La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="84ecc-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="84ecc-128">Valor de tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="84ecc-128">Event type value, 4</span></span>                                             | <span data-ttu-id="84ecc-129">Evento de proceso de recopilación de datos final.</span><span class="sxs-lookup"><span data-stu-id="84ecc-129">End data collection process event.</span></span> <span data-ttu-id="84ecc-130">Enumera los procesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="84ecc-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="84ecc-131">La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="84ecc-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="84ecc-132">Valor del tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="84ecc-132">Event type value, 32</span></span>                                            | <span data-ttu-id="84ecc-133">Evento de contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="84ecc-133">Performance counters event.</span></span> <span data-ttu-id="84ecc-134">La [**clase \_ MOF Process V2 \_ TypeGroup2**](process-v2-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="84ecc-134">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                                                          |
| <span data-ttu-id="84ecc-135">Valor del tipo de evento, 33</span><span class="sxs-lookup"><span data-stu-id="84ecc-135">Event type value, 33</span></span>                                            | <span data-ttu-id="84ecc-136">Resumen de los contadores de rendimiento al principio de la sesión.</span><span class="sxs-lookup"><span data-stu-id="84ecc-136">Rundown of the performance counters at the start of the session.</span></span> <span data-ttu-id="84ecc-137">La [**clase \_ MOF Process V2 \_ TypeGroup2**](process-v2-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="84ecc-137">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                     |
| <span data-ttu-id="84ecc-138">Valor del tipo de evento, 39</span><span class="sxs-lookup"><span data-stu-id="84ecc-138">Event type value, 39</span></span>                                            | <span data-ttu-id="84ecc-139">Evento de proceso en desa desarrollo.</span><span class="sxs-lookup"><span data-stu-id="84ecc-139">Defunct process event.</span></span> <span data-ttu-id="84ecc-140">La [**clase \_ MOF Process TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="84ecc-140">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |



 

<span data-ttu-id="84ecc-141">Los eventos de inicio de procesos y subprocesos se pueden registrar en el contexto del proceso o subproceso primario.</span><span class="sxs-lookup"><span data-stu-id="84ecc-141">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="84ecc-142">Como resultado, es posible que los **miembros ProcessId** y **ThreadId** de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se crean.</span><span class="sxs-lookup"><span data-stu-id="84ecc-142">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="84ecc-143">Este es el motivo por el que estos eventos contienen los identificadores de proceso y subproceso en los datos del evento (además de los del encabezado de evento).</span><span class="sxs-lookup"><span data-stu-id="84ecc-143">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="84ecc-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84ecc-144">Requirements</span></span>



| <span data-ttu-id="84ecc-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="84ecc-145">Requirement</span></span> | <span data-ttu-id="84ecc-146">Valor</span><span class="sxs-lookup"><span data-stu-id="84ecc-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="84ecc-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84ecc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="84ecc-148">Aplicaciones de escritorio de Windows Vista \[ \| para aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="84ecc-148">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="84ecc-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84ecc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="84ecc-150">Aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="84ecc-150">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84ecc-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84ecc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84ecc-152">**SystemTrace de MSNT \_**</span><span class="sxs-lookup"><span data-stu-id="84ecc-152">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="84ecc-153">**Proceso**</span><span class="sxs-lookup"><span data-stu-id="84ecc-153">**Process**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="84ecc-154">**Process \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="84ecc-154">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="84ecc-155">**Proceso \_ V0**</span><span class="sxs-lookup"><span data-stu-id="84ecc-155">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="84ecc-156">**Proceso \_ V1**</span><span class="sxs-lookup"><span data-stu-id="84ecc-156">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 
