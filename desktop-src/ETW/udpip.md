---
description: Esta clase es la clase primaria para los eventos UDP/IP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: Clase UdpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5116b5f97a4aa7e3bafa9da1c1208ce7ee9d5794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543075"
---
# <a name="udpip-class"></a><span data-ttu-id="e74f6-104">Clase UdpIp</span><span class="sxs-lookup"><span data-stu-id="e74f6-104">UdpIp class</span></span>

<span data-ttu-id="e74f6-105">Esta clase es la clase primaria para los eventos UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="e74f6-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="e74f6-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="e74f6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e74f6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e74f6-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="e74f6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e74f6-108">Members</span></span>

<span data-ttu-id="e74f6-109">La clase **UdpIp** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="e74f6-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="e74f6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e74f6-110">Remarks</span></span>

<span data-ttu-id="e74f6-111">Para habilitar los eventos UDP/IP en una sesión de registro del kernel de NT, especifique la marca de **seguimiento de eventos de \_ \_ \_ red \_ TCPIP** Flag en el miembro **EnableFlags** de una estructura de propiedades de [**\_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="e74f6-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="e74f6-112">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos UDP/IP mediante una llamada a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**UdpIpGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="e74f6-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="e74f6-113">Utilice los siguientes tipos de eventos para identificar el evento de red (UDP/IP) real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="e74f6-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="e74f6-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="e74f6-114">Event type</span></span>                                                         | <span data-ttu-id="e74f6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e74f6-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e74f6-116">**Evento \_ de Tipo de seguimiento \_ \_ Receive**(el valor de tipo de evento es 11)</span><span class="sxs-lookup"><span data-stu-id="e74f6-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="e74f6-117">Evento Receive para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="e74f6-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="e74f6-118">La clase MOF [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e74f6-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="e74f6-119">**Evento \_ de Tipo de seguimiento \_ \_ send**(el valor de tipo de evento es 10)</span><span class="sxs-lookup"><span data-stu-id="e74f6-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="e74f6-120">Enviar evento para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="e74f6-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="e74f6-121">La clase MOF [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e74f6-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="e74f6-122">Valor de tipo de evento, 17</span><span class="sxs-lookup"><span data-stu-id="e74f6-122">Event type value, 17</span></span>                                               | <span data-ttu-id="e74f6-123">Evento Fail.</span><span class="sxs-lookup"><span data-stu-id="e74f6-123">Fail event.</span></span> <span data-ttu-id="e74f6-124">La clase MOF [**\_ FAIL UdpIp**](udpip-fail.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e74f6-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="e74f6-125">Valor del tipo de evento 26</span><span class="sxs-lookup"><span data-stu-id="e74f6-125">Event type value, 26</span></span>                                               | <span data-ttu-id="e74f6-126">Envía el evento para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="e74f6-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="e74f6-127">La clase MOF [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e74f6-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="e74f6-128">Valor del tipo de evento 27</span><span class="sxs-lookup"><span data-stu-id="e74f6-128">Event type value, 27</span></span>                                               | <span data-ttu-id="e74f6-129">Evento Receive para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="e74f6-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="e74f6-130">La clase MOF [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e74f6-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="e74f6-131">Puede realizar un seguimiento de los eventos de red a un proceso de origen y de destino mediante la propiedad **ProcessId** .</span><span class="sxs-lookup"><span data-stu-id="e74f6-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="e74f6-132">Dado que algunos eventos de red están registrados por subprocesos independientes, es posible que no pueda usar los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar el proceso o subproceso que originó las actividades de red.</span><span class="sxs-lookup"><span data-stu-id="e74f6-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="e74f6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e74f6-133">Requirements</span></span>



| <span data-ttu-id="e74f6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e74f6-134">Requirement</span></span> | <span data-ttu-id="e74f6-135">Value</span><span class="sxs-lookup"><span data-stu-id="e74f6-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e74f6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e74f6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e74f6-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e74f6-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e74f6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e74f6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e74f6-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e74f6-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e74f6-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e74f6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e74f6-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="e74f6-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="e74f6-142">**Error de UdpIp \_**</span><span class="sxs-lookup"><span data-stu-id="e74f6-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="e74f6-143">**UdpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="e74f6-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="e74f6-144">**UdpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="e74f6-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="e74f6-145">**UdpIp \_ v0**</span><span class="sxs-lookup"><span data-stu-id="e74f6-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="e74f6-146">**UdpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e74f6-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
