---
description: Esta clase es la clase primaria para los eventos TCP/IP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: TcpIp (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6488ece2fd8df0670455ceea25560835c352b83e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984774"
---
# <a name="tcpip-class"></a><span data-ttu-id="8ac59-104">TcpIp (clase)</span><span class="sxs-lookup"><span data-stu-id="8ac59-104">TcpIp class</span></span>

<span data-ttu-id="8ac59-105">Esta clase es la clase primaria para los eventos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8ac59-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="8ac59-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="8ac59-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ac59-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ac59-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="8ac59-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8ac59-108">Members</span></span>

<span data-ttu-id="8ac59-109">La clase **TCPIP** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="8ac59-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ac59-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ac59-110">Remarks</span></span>

<span data-ttu-id="8ac59-111">Para habilitar los eventos TCP/IP en una sesión de registro del kernel de NT, especifique la marca de **seguimiento de eventos de \_ \_ \_ red \_ TCPIP** Flag en el miembro **EnableFlags** de una estructura de propiedades de [**\_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="8ac59-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="8ac59-112">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos TCP/IP mediante una llamada a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**TcpIpGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="8ac59-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="8ac59-113">Utilice los siguientes tipos de eventos para identificar el evento de red (TCP/IP) real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="8ac59-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="8ac59-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="8ac59-114">Event type</span></span>                                                            | <span data-ttu-id="8ac59-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ac59-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac59-116">**Evento \_ de Tipo de seguimiento \_ \_ Accept**(el valor de tipo de evento es 15)</span><span class="sxs-lookup"><span data-stu-id="8ac59-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="8ac59-117">Evento Accept para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ac59-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="8ac59-118">La clase MOF [**\_ TypeGroup2 de TCPIP**](tcpip-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="8ac59-119">**Evento \_ de Tipo de seguimiento \_ \_ Connect**(el valor de tipo de evento es 12)</span><span class="sxs-lookup"><span data-stu-id="8ac59-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="8ac59-120">Evento de conexión para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ac59-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="8ac59-121">La clase MOF [**\_ TypeGroup2 de TCPIP**](tcpip-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="8ac59-122">**Evento \_ de Tipo de seguimiento \_ \_ Disconnect**(el valor del tipo de evento es 13)</span><span class="sxs-lookup"><span data-stu-id="8ac59-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="8ac59-123">Evento de desconexión del protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ac59-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="8ac59-124">La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="8ac59-125">**Evento \_ de Tipo de seguimiento \_ \_ Receive**(el valor de tipo de evento es 11)</span><span class="sxs-lookup"><span data-stu-id="8ac59-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="8ac59-126">Evento Receive para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ac59-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="8ac59-127">La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="8ac59-128">**Evento \_ de Tipo de seguimiento \_ \_ reconnect**(el valor de tipo de evento es 16)</span><span class="sxs-lookup"><span data-stu-id="8ac59-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="8ac59-129">Evento de reconexión para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ac59-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="8ac59-130">(Se produjo un error en un intento de conexión y se realiza otro intento). La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="8ac59-131">**Evento \_ de Tipo de seguimiento \_ \_ retransmitir**(el valor del tipo de evento es 14)</span><span class="sxs-lookup"><span data-stu-id="8ac59-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="8ac59-132">Evento de retransmisión para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ac59-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="8ac59-133">La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="8ac59-134">**Evento \_ de Tipo de seguimiento \_ \_ send**(el valor de tipo de evento es 10)</span><span class="sxs-lookup"><span data-stu-id="8ac59-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="8ac59-135">Enviar evento para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ac59-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="8ac59-136">La clase MOF [**\_ SendIPV4 de TCPIP**](tcpip-sendipv4.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="8ac59-137">Valor de tipo de evento, 17</span><span class="sxs-lookup"><span data-stu-id="8ac59-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="8ac59-138">Evento Fail.</span><span class="sxs-lookup"><span data-stu-id="8ac59-138">Fail event.</span></span> <span data-ttu-id="8ac59-139">La clase de [**TCPIP \_ FAIL**](tcpip-fail.md) mof define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="8ac59-140">Valor de tipo de evento, 18</span><span class="sxs-lookup"><span data-stu-id="8ac59-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="8ac59-141">Evento de copia TCP para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="8ac59-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="8ac59-142">La clase MOF [**\_ TypeGroup1 de TCPIP**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="8ac59-143">Valor del tipo de evento 26</span><span class="sxs-lookup"><span data-stu-id="8ac59-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="8ac59-144">Envía el evento para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ac59-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="8ac59-145">La clase MOF [**\_ SendIPV6 de TCPIP**](tcpip-sendipv6.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="8ac59-146">Valor del tipo de evento 27</span><span class="sxs-lookup"><span data-stu-id="8ac59-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="8ac59-147">Evento Receive para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ac59-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="8ac59-148">La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="8ac59-149">Valor del tipo de evento 28</span><span class="sxs-lookup"><span data-stu-id="8ac59-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="8ac59-150">Evento de conexión para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ac59-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="8ac59-151">La clase MOF [**\_ TypeGroup4 de TCPIP**](tcpip-typegroup4.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="8ac59-152">Valor de tipo de evento, 29</span><span class="sxs-lookup"><span data-stu-id="8ac59-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="8ac59-153">Evento de desconexión para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ac59-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="8ac59-154">La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="8ac59-155">Valor de tipo de evento, 30</span><span class="sxs-lookup"><span data-stu-id="8ac59-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="8ac59-156">Evento de retransmisión para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ac59-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="8ac59-157">La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="8ac59-158">Valor de tipo de evento, 31</span><span class="sxs-lookup"><span data-stu-id="8ac59-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="8ac59-159">Evento Accept para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ac59-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="8ac59-160">La clase MOF [**\_ TypeGroup4 de TCPIP**](tcpip-typegroup4.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="8ac59-161">Valor del tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="8ac59-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="8ac59-162">Evento de reconexión para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ac59-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="8ac59-163">(Se produjo un error en un intento de conexión y se realiza otro intento). La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="8ac59-164">Valor del tipo de evento, 34</span><span class="sxs-lookup"><span data-stu-id="8ac59-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="8ac59-165">Evento de copia TCP para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ac59-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="8ac59-166">La clase MOF [**\_ TypeGroup3 de TCPIP**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="8ac59-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="8ac59-167">Puede realizar un seguimiento de los eventos de red a un proceso de origen y de destino mediante la propiedad **ProcessId** .</span><span class="sxs-lookup"><span data-stu-id="8ac59-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="8ac59-168">Dado que algunos eventos de red están registrados por subprocesos independientes, es posible que no pueda usar los miembros **ProcessId** y **ThreadId** del [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar el proceso o subproceso que originó las actividades de red.</span><span class="sxs-lookup"><span data-stu-id="8ac59-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ac59-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ac59-169">Requirements</span></span>



| <span data-ttu-id="8ac59-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ac59-170">Requirement</span></span> | <span data-ttu-id="8ac59-171">Value</span><span class="sxs-lookup"><span data-stu-id="8ac59-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ac59-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ac59-172">Minimum supported client</span></span><br/> | <span data-ttu-id="8ac59-173">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8ac59-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8ac59-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ac59-174">Minimum supported server</span></span><br/> | <span data-ttu-id="8ac59-175">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ac59-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ac59-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ac59-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac59-177">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="8ac59-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="8ac59-178">**Error de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="8ac59-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="8ac59-179">**SendIPV4 de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="8ac59-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="8ac59-180">**SendIPV6 de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="8ac59-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="8ac59-181">**TypeGroup1 de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="8ac59-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="8ac59-182">**TypeGroup2 de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="8ac59-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="8ac59-183">**TypeGroup3 de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="8ac59-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="8ac59-184">**TypeGroup4 de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="8ac59-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="8ac59-185">**V0 de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="8ac59-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="8ac59-186">**TcpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="8ac59-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
