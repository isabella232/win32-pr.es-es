---
description: Esta clase es la clase primaria para los eventos de subproceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: c4af87462607b675e46b3459a811925fbefe3ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279667"
---
# <a name="thread-class"></a><span data-ttu-id="7e365-104">Thread (clase)</span><span class="sxs-lookup"><span data-stu-id="7e365-104">Thread class</span></span>

<span data-ttu-id="7e365-105">Esta clase es la clase primaria para los eventos de subproceso.</span><span class="sxs-lookup"><span data-stu-id="7e365-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="7e365-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="7e365-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e365-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e365-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="7e365-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e365-108">Members</span></span>

<span data-ttu-id="7e365-109">La clase **Thread** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="7e365-109">The **Thread** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e365-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e365-110">Remarks</span></span>

<span data-ttu-id="7e365-111">Para habilitar eventos de subproceso en una sesión de registro del kernel de NT, especifique la marca de **\_ \_ \_ subproceso de marca de seguimiento de eventos** en el miembro **EnableFlags** de una estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="7e365-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="7e365-112">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de subprocesos llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ThreadGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="7e365-112">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="7e365-113">Utilice los siguientes tipos de eventos para identificar el evento de subproceso real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="7e365-113">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="7e365-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="7e365-114">Event type</span></span>                                                      | <span data-ttu-id="7e365-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e365-115">Description</span></span>                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e365-116">**Evento \_ de Tipo de seguimiento \_ \_ End**(el valor de tipo de evento es 2)</span><span class="sxs-lookup"><span data-stu-id="7e365-116">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="7e365-117">Evento de fin de subproceso.</span><span class="sxs-lookup"><span data-stu-id="7e365-117">End thread event.</span></span> <span data-ttu-id="7e365-118">La clase de MOF [**Thread \_ TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="7e365-118">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="7e365-119">**Evento \_ de Tipo de seguimiento \_ \_ Start**(el valor del tipo de evento es 1)</span><span class="sxs-lookup"><span data-stu-id="7e365-119">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="7e365-120">Evento de subproceso de inicio.</span><span class="sxs-lookup"><span data-stu-id="7e365-120">Start thread event.</span></span> <span data-ttu-id="7e365-121">La clase de MOF [**Thread \_ TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="7e365-121">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="7e365-122">Valor del tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="7e365-122">Event type value, 3</span></span>                                             | <span data-ttu-id="7e365-123">Iniciar evento de subproceso de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="7e365-123">Start data collection thread event.</span></span> <span data-ttu-id="7e365-124">Enumera los subprocesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="7e365-124">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="7e365-125">La clase de MOF [**Thread \_ TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="7e365-125">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="7e365-126">Valor del tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="7e365-126">Event type value, 4</span></span>                                             | <span data-ttu-id="7e365-127">Evento End Data Collection Thread.</span><span class="sxs-lookup"><span data-stu-id="7e365-127">End data collection thread event.</span></span> <span data-ttu-id="7e365-128">Enumera los subprocesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="7e365-128">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="7e365-129">La clase de MOF [**Thread \_ TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="7e365-129">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="7e365-130">Los eventos de inicio de procesos y subprocesos pueden registrarse en el contexto del proceso o subproceso primario.</span><span class="sxs-lookup"><span data-stu-id="7e365-130">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="7e365-131">Como resultado, es posible que los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se está creando.</span><span class="sxs-lookup"><span data-stu-id="7e365-131">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="7e365-132">Este es el motivo por el que estos eventos contienen los identificadores de proceso y de subproceso en los datos de evento (además de los del encabezado de evento).</span><span class="sxs-lookup"><span data-stu-id="7e365-132">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e365-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e365-133">Requirements</span></span>



| <span data-ttu-id="7e365-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e365-134">Requirement</span></span> | <span data-ttu-id="7e365-135">Value</span><span class="sxs-lookup"><span data-stu-id="7e365-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e365-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e365-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7e365-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7e365-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e365-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e365-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7e365-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e365-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e365-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e365-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e365-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="7e365-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="7e365-142">**Subproceso \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="7e365-142">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="7e365-143">**Subproceso \_ v0**</span><span class="sxs-lookup"><span data-stu-id="7e365-143">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="7e365-144">**Subproceso \_ v1**</span><span class="sxs-lookup"><span data-stu-id="7e365-144">**Thread\_V1**</span></span>](thread-v1.md)
</dt> <dt>

[<span data-ttu-id="7e365-145">**Subproceso \_ V2**</span><span class="sxs-lookup"><span data-stu-id="7e365-145">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 
