---
description: 'Clase de subproceso: esta clase es la clase primaria para los eventos de subproceso. La sintaxis siguiente se simplifica a partir del código MOF.'
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
ms.openlocfilehash: 121a8d4aa04017011648d80329ee02396582987a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105533"
---
# <a name="thread-class"></a><span data-ttu-id="f76b1-104">Thread (clase)</span><span class="sxs-lookup"><span data-stu-id="f76b1-104">Thread class</span></span>

<span data-ttu-id="f76b1-105">Esta clase es la clase primaria para los eventos de subproceso.</span><span class="sxs-lookup"><span data-stu-id="f76b1-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="f76b1-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="f76b1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f76b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f76b1-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="f76b1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f76b1-108">Members</span></span>

<span data-ttu-id="f76b1-109">La **clase Thread** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="f76b1-109">The **Thread** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f76b1-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f76b1-110">Remarks</span></span>

<span data-ttu-id="f76b1-111">Para habilitar eventos de subproceso en una sesión de registro del kernel de NT, especifique la marca **EVENT \_ TRACE FLAG \_ \_ THREAD** en el **miembro EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="f76b1-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="f76b1-112">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de subproceso llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ThreadGuid**](nt-kernel-logger-constants.md) como *parámetro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="f76b1-112">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="f76b1-113">Use los siguientes tipos de eventos para identificar el evento de subproceso real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="f76b1-113">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="f76b1-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="f76b1-114">Event type</span></span>                                                      | <span data-ttu-id="f76b1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f76b1-115">Description</span></span>                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f76b1-116">**EVENT \_ TRACE \_ TYPE \_ END**(el valor del tipo de evento es 2)</span><span class="sxs-lookup"><span data-stu-id="f76b1-116">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="f76b1-117">Evento de subproceso final.</span><span class="sxs-lookup"><span data-stu-id="f76b1-117">End thread event.</span></span> <span data-ttu-id="f76b1-118">La [**clase \_ MOF Thread TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="f76b1-118">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="f76b1-119">**EVENT \_ TRACE \_ TYPE \_ START**(el valor del tipo de evento es 1)</span><span class="sxs-lookup"><span data-stu-id="f76b1-119">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="f76b1-120">Iniciar evento de subproceso.</span><span class="sxs-lookup"><span data-stu-id="f76b1-120">Start thread event.</span></span> <span data-ttu-id="f76b1-121">La [**clase \_ MOF Thread TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="f76b1-121">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="f76b1-122">Valor de tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="f76b1-122">Event type value, 3</span></span>                                             | <span data-ttu-id="f76b1-123">Iniciar evento de subproceso de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="f76b1-123">Start data collection thread event.</span></span> <span data-ttu-id="f76b1-124">Enumera los subprocesos que se están ejecutando actualmente en el momento en que se inicia la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="f76b1-124">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="f76b1-125">La [**clase \_ MOF Thread TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="f76b1-125">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="f76b1-126">Valor de tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="f76b1-126">Event type value, 4</span></span>                                             | <span data-ttu-id="f76b1-127">Evento de subproceso de recopilación de datos final.</span><span class="sxs-lookup"><span data-stu-id="f76b1-127">End data collection thread event.</span></span> <span data-ttu-id="f76b1-128">Enumera los subprocesos que se están ejecutando actualmente en el momento en que finaliza la sesión del kernel.</span><span class="sxs-lookup"><span data-stu-id="f76b1-128">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="f76b1-129">La [**clase \_ MOF Thread TypeGroup1**](thread-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="f76b1-129">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="f76b1-130">Los eventos de inicio de procesos y subprocesos se pueden registrar en el contexto del proceso o subproceso primario.</span><span class="sxs-lookup"><span data-stu-id="f76b1-130">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="f76b1-131">Como resultado, es posible que los **miembros ProcessId** y **ThreadId** de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) no se correspondan con el proceso y el subproceso que se crean.</span><span class="sxs-lookup"><span data-stu-id="f76b1-131">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="f76b1-132">Este es el motivo por el que estos eventos contienen los identificadores de proceso y subproceso en los datos del evento (además de los del encabezado de evento).</span><span class="sxs-lookup"><span data-stu-id="f76b1-132">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="f76b1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f76b1-133">Requirements</span></span>



| <span data-ttu-id="f76b1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f76b1-134">Requirement</span></span> | <span data-ttu-id="f76b1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f76b1-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f76b1-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f76b1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f76b1-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f76b1-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f76b1-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f76b1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f76b1-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f76b1-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f76b1-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f76b1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f76b1-141">**SystemTrace de MSNT \_**</span><span class="sxs-lookup"><span data-stu-id="f76b1-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="f76b1-142">**Thread \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="f76b1-142">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="f76b1-143">**Subproceso \_ V0**</span><span class="sxs-lookup"><span data-stu-id="f76b1-143">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="f76b1-144">**Subproceso \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f76b1-144">**Thread\_V1**</span></span>](thread-v1.md)
</dt> <dt>

[<span data-ttu-id="f76b1-145">**Subproceso \_ V2**</span><span class="sxs-lookup"><span data-stu-id="f76b1-145">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 
