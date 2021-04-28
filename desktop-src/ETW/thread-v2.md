---
description: 'Thread_V2 clase : esta clase es la clase primaria para los eventos de subproceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Thread_V2 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: b00067af61a55e61f70b0c799a1512edf284f11c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105623"
---
# <a name="thread_v2-class"></a><span data-ttu-id="d01bf-104">Clase \_ Thread V2</span><span class="sxs-lookup"><span data-stu-id="d01bf-104">Thread\_V2 class</span></span>

<span data-ttu-id="d01bf-105">Esta clase es la clase primaria para los eventos de subproceso.</span><span class="sxs-lookup"><span data-stu-id="d01bf-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="d01bf-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="d01bf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d01bf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d01bf-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="d01bf-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d01bf-108">Members</span></span>

<span data-ttu-id="d01bf-109">La **clase Thread \_ V2** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="d01bf-109">The **Thread\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d01bf-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d01bf-110">Remarks</span></span>

<span data-ttu-id="d01bf-111">Para habilitar eventos de subproceso en una sesión de registro del kernel de NT, especifique la marca **EVENT \_ TRACE FLAG \_ \_ THREAD** en el **miembro EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="d01bf-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="d01bf-112">También puede especificar las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d01bf-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="d01bf-113">**CSWITCH \_ DE MARCA DE SEGUIMIENTO DE \_ \_ EVENTOS**</span><span class="sxs-lookup"><span data-stu-id="d01bf-113">**EVENT\_TRACE\_FLAG\_CSWITCH**</span></span>
-   <span data-ttu-id="d01bf-114">**DISTRIBUIDOR DE \_ MARCAS DE SEGUIMIENTO DE \_ \_ EVENTOS**</span><span class="sxs-lookup"><span data-stu-id="d01bf-114">**EVENT\_TRACE\_FLAG\_DISPATCHER**</span></span>

<span data-ttu-id="d01bf-115">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de subproceso llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ThreadGuid**](nt-kernel-logger-constants.md) como *parámetro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="d01bf-115">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="d01bf-116">Use los siguientes tipos de eventos para identificar el evento de subproceso real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="d01bf-116">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="d01bf-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="d01bf-117">Event type</span></span>                                                      | <span data-ttu-id="d01bf-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d01bf-118">Description</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d01bf-119">**EVENT \_ TRACE \_ TYPE \_ END**(el valor del tipo de evento es 2)</span><span class="sxs-lookup"><span data-stu-id="d01bf-119">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="d01bf-120">Evento de subproceso final.</span><span class="sxs-lookup"><span data-stu-id="d01bf-120">End thread event.</span></span> <span data-ttu-id="d01bf-121">La [**clase \_ MOF Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d01bf-121">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="d01bf-122">**EVENT \_ TRACE \_ TYPE \_ START**(el valor del tipo de evento es 1)</span><span class="sxs-lookup"><span data-stu-id="d01bf-122">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="d01bf-123">Iniciar evento de subproceso.</span><span class="sxs-lookup"><span data-stu-id="d01bf-123">Start thread event.</span></span> <span data-ttu-id="d01bf-124">La [**clase \_ MOF Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d01bf-124">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="d01bf-125">Valor de tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="d01bf-125">Event type value, 3</span></span>                                             | <span data-ttu-id="d01bf-126">Iniciar evento de subproceso de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="d01bf-126">Start data collection thread event.</span></span> <span data-ttu-id="d01bf-127">Enumera los subprocesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="d01bf-127">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="d01bf-128">La [**clase MOF Thread \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d01bf-128">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="d01bf-129">Valor de tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="d01bf-129">Event type value, 4</span></span>                                             | <span data-ttu-id="d01bf-130">Evento de subproceso de recopilación de datos final.</span><span class="sxs-lookup"><span data-stu-id="d01bf-130">End data collection thread event.</span></span> <span data-ttu-id="d01bf-131">Enumera los subprocesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="d01bf-131">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="d01bf-132">La [**clase MOF Thread \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d01bf-132">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="d01bf-133">Valor del tipo de evento, 36</span><span class="sxs-lookup"><span data-stu-id="d01bf-133">Event type value, 36</span></span>                                            | <span data-ttu-id="d01bf-134">Evento de cambio de contexto.</span><span class="sxs-lookup"><span data-stu-id="d01bf-134">Context switch event.</span></span> <span data-ttu-id="d01bf-135">La [**clase MOF**](cswitch.md) de CSwitch define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d01bf-135">The [**CSwitch**](cswitch.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="d01bf-136">Valor del tipo de evento, 50</span><span class="sxs-lookup"><span data-stu-id="d01bf-136">Event type value, 50</span></span>                                            | <span data-ttu-id="d01bf-137">Evento de subproceso listo.</span><span class="sxs-lookup"><span data-stu-id="d01bf-137">Ready thread event.</span></span> <span data-ttu-id="d01bf-138">La [**clase MOF ReadyThread**](readythread.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d01bf-138">The [**ReadyThread**](readythread.md) MOF class defines the event data for this event.</span></span>                                                                                                                          |



 

<span data-ttu-id="d01bf-139">Los eventos de inicio de procesos y subprocesos se pueden registrar en el contexto del proceso o subproceso primario.</span><span class="sxs-lookup"><span data-stu-id="d01bf-139">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="d01bf-140">Como resultado, es posible que los **miembros ProcessId** y **ThreadId** de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se crean.</span><span class="sxs-lookup"><span data-stu-id="d01bf-140">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="d01bf-141">Este es el motivo por el que estos eventos contienen los identificadores de proceso y subproceso en los datos del evento (además de los del encabezado de evento).</span><span class="sxs-lookup"><span data-stu-id="d01bf-141">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="d01bf-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d01bf-142">Requirements</span></span>



| <span data-ttu-id="d01bf-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01bf-143">Requirement</span></span> | <span data-ttu-id="d01bf-144">Valor</span><span class="sxs-lookup"><span data-stu-id="d01bf-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d01bf-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d01bf-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d01bf-146">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="d01bf-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d01bf-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d01bf-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d01bf-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d01bf-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d01bf-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d01bf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01bf-150">**SystemTrace de MSNT \_**</span><span class="sxs-lookup"><span data-stu-id="d01bf-150">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="d01bf-151">**CSwitch**</span><span class="sxs-lookup"><span data-stu-id="d01bf-151">**CSwitch**</span></span>](cswitch.md)
</dt> <dt>

[<span data-ttu-id="d01bf-152">**Hilo**</span><span class="sxs-lookup"><span data-stu-id="d01bf-152">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="d01bf-153">**Thread \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="d01bf-153">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="d01bf-154">**Subproceso \_ V0**</span><span class="sxs-lookup"><span data-stu-id="d01bf-154">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="d01bf-155">**Subproceso \_ V1**</span><span class="sxs-lookup"><span data-stu-id="d01bf-155">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 
