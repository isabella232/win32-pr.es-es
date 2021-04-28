---
description: 'Clase UdpIp: esta clase es la clase primaria para eventos UDP/IP. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: UdpIp (clase)
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
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105393"
---
# <a name="udpip-class"></a><span data-ttu-id="8ba46-104">UdpIp (clase)</span><span class="sxs-lookup"><span data-stu-id="8ba46-104">UdpIp class</span></span>

<span data-ttu-id="8ba46-105">Esta clase es la clase primaria para los eventos UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="8ba46-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="8ba46-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="8ba46-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba46-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ba46-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="8ba46-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8ba46-108">Members</span></span>

<span data-ttu-id="8ba46-109">La **clase UdpIp** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="8ba46-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba46-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ba46-110">Remarks</span></span>

<span data-ttu-id="8ba46-111">Para habilitar eventos UDP/IP en una sesión de registro del kernel de NT, especifique la marca **\_ \_ \_ \_ TCPIP EVENT TRACE FLAG NETWORK** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="8ba46-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="8ba46-112">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos UDP/IP llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**UdpIpGuid**](nt-kernel-logger-constants.md) como *parámetro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="8ba46-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="8ba46-113">Use los siguientes tipos de eventos para identificar el evento de red (UDP/IP) real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="8ba46-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="8ba46-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="8ba46-114">Event type</span></span>                                                         | <span data-ttu-id="8ba46-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ba46-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba46-116">**EVENT \_ TRACE \_ TYPE \_ RECEIVE**(el valor del tipo de evento es 11)</span><span class="sxs-lookup"><span data-stu-id="8ba46-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="8ba46-117">Evento de recepción para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ba46-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="8ba46-118">La [**clase MOF \_ UdpIp TypeGroup1**](udpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ba46-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="8ba46-119">**EVENT \_ TRACE \_ TYPE \_ SEND**(el valor del tipo de evento es 10)</span><span class="sxs-lookup"><span data-stu-id="8ba46-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="8ba46-120">Envío de eventos para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ba46-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="8ba46-121">La [**clase MOF \_ UdpIp TypeGroup1**](udpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ba46-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="8ba46-122">Valor de tipo de evento, 17</span><span class="sxs-lookup"><span data-stu-id="8ba46-122">Event type value, 17</span></span>                                               | <span data-ttu-id="8ba46-123">Evento de error.</span><span class="sxs-lookup"><span data-stu-id="8ba46-123">Fail event.</span></span> <span data-ttu-id="8ba46-124">La [**clase MOF UdpIp \_ Fail**](udpip-fail.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ba46-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="8ba46-125">Valor de tipo de evento, 26</span><span class="sxs-lookup"><span data-stu-id="8ba46-125">Event type value, 26</span></span>                                               | <span data-ttu-id="8ba46-126">Enviar evento para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ba46-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="8ba46-127">La [**clase MOF UdpIp \_ TypeGroup2**](udpip-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ba46-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="8ba46-128">Valor del tipo de evento, 27</span><span class="sxs-lookup"><span data-stu-id="8ba46-128">Event type value, 27</span></span>                                               | <span data-ttu-id="8ba46-129">Evento de recepción para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ba46-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="8ba46-130">La [**clase MOF UdpIp \_ TypeGroup2**](udpip-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ba46-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="8ba46-131">Puede realizar un seguimiento de los eventos de red a un proceso de origen y destino mediante la **propiedad ProcessId.**</span><span class="sxs-lookup"><span data-stu-id="8ba46-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="8ba46-132">Dado que algunos eventos de red se registran mediante subprocesos independientes, es posible que no pueda usar los miembros **ProcessId** y **ThreadId** de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar el proceso o subproceso que originó las actividades de red.</span><span class="sxs-lookup"><span data-stu-id="8ba46-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba46-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba46-133">Requirements</span></span>



| <span data-ttu-id="8ba46-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba46-134">Requirement</span></span> | <span data-ttu-id="8ba46-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8ba46-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ba46-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ba46-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba46-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8ba46-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8ba46-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ba46-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba46-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ba46-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ba46-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8ba46-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba46-141">**SystemTrace de MSNT \_**</span><span class="sxs-lookup"><span data-stu-id="8ba46-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="8ba46-142">**Error \_ de UdpIp**</span><span class="sxs-lookup"><span data-stu-id="8ba46-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="8ba46-143">**UdpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="8ba46-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="8ba46-144">**UdpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="8ba46-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="8ba46-145">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="8ba46-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="8ba46-146">**UdpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="8ba46-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
