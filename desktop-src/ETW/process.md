---
description: Esta clase es la clase primaria para los eventos de proceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Process (clase)
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
ms.openlocfilehash: b014262044db9e227bec5af2b351d1392c243c23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985855"
---
# <a name="process-class"></a><span data-ttu-id="0c9e4-104">Process (clase)</span><span class="sxs-lookup"><span data-stu-id="0c9e4-104">Process class</span></span>

<span data-ttu-id="0c9e4-105">Esta clase es la clase primaria para los eventos de proceso.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="0c9e4-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c9e4-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="0c9e4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c9e4-108">Members</span></span>

<span data-ttu-id="0c9e4-109">La clase **Process** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c9e4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c9e4-110">Remarks</span></span>

<span data-ttu-id="0c9e4-111">Para habilitar los eventos de procesamiento en una sesión de registro del kernel de NT, especifique la marca de  proceso de marca de seguimiento de eventos en el miembro EnableFlags [](/windows/win32/api/evntrace/nf-evntrace-starttracea) de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función StartTrace. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="0c9e4-112">También puede especificar la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="0c9e4-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="0c9e4-113">**\_ \_ \_ contadores del proceso de marca de seguimiento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="0c9e4-114">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de proceso llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ProcessGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="0c9e4-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="0c9e4-115">Utilice los siguientes tipos de eventos para identificar el evento de proceso real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="0c9e4-116">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="0c9e4-116">Event type</span></span>                                                      | <span data-ttu-id="0c9e4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c9e4-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9e4-118">**Evento \_ de Tipo de seguimiento \_ \_ End**(el valor de tipo de evento es 2)</span><span class="sxs-lookup"><span data-stu-id="0c9e4-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="0c9e4-119">Evento de finalización de proceso.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-119">End process event.</span></span> <span data-ttu-id="0c9e4-120">La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="0c9e4-121">**Evento \_ de Tipo de seguimiento \_ \_ Start**(el valor del tipo de evento es 1)</span><span class="sxs-lookup"><span data-stu-id="0c9e4-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="0c9e4-122">Evento de inicio del proceso.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-122">Start process event.</span></span> <span data-ttu-id="0c9e4-123">La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="0c9e4-124">Valor del tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="0c9e4-124">Event type value, 3</span></span>                                             | <span data-ttu-id="0c9e4-125">Iniciar el evento del proceso de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-125">Start data collection process event.</span></span> <span data-ttu-id="0c9e4-126">Enumera los procesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="0c9e4-127">La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="0c9e4-128">Valor del tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="0c9e4-128">Event type value, 4</span></span>                                             | <span data-ttu-id="0c9e4-129">Evento finalizar proceso de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-129">End data collection process event.</span></span> <span data-ttu-id="0c9e4-130">Enumera los procesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="0c9e4-131">La clase de MOF [**Process \_ TypeGroup1**](process-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="0c9e4-132">Los eventos de inicio de procesos y subprocesos pueden registrarse en el contexto del proceso o subproceso primario.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-132">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="0c9e4-133">Como resultado, es posible que los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se está creando.</span><span class="sxs-lookup"><span data-stu-id="0c9e4-133">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="0c9e4-134">Este es el motivo por el que estos eventos contienen los identificadores de proceso y de subproceso en los datos de evento (además de los del encabezado de evento).</span><span class="sxs-lookup"><span data-stu-id="0c9e4-134">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c9e4-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c9e4-135">Requirements</span></span>



| <span data-ttu-id="0c9e4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c9e4-136">Requirement</span></span> | <span data-ttu-id="0c9e4-137">Value</span><span class="sxs-lookup"><span data-stu-id="0c9e4-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0c9e4-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c9e4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0c9e4-139">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="0c9e4-139">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="0c9e4-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c9e4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0c9e4-141">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="0c9e4-141">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c9e4-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c9e4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c9e4-143">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-143">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="0c9e4-144">**Procesar \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-144">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="0c9e4-145">**Procesar \_ v0**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-145">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="0c9e4-146">**Proceso \_ v1**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-146">**Process\_V1**</span></span>](process-v1.md)
</dt> <dt>

[<span data-ttu-id="0c9e4-147">**Proceso \_ V2**</span><span class="sxs-lookup"><span data-stu-id="0c9e4-147">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 
