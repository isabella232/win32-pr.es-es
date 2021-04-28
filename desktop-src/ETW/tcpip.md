---
description: 'Clase TcpIp: esta clase es la clase primaria para los eventos TCP/IP. La sintaxis siguiente se simplifica a partir del código MOF.'
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
ms.openlocfilehash: abcd805b417451adf2122e7baf3310be101a35ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105733"
---
# <a name="tcpip-class"></a><span data-ttu-id="446c4-104">TcpIp (clase)</span><span class="sxs-lookup"><span data-stu-id="446c4-104">TcpIp class</span></span>

<span data-ttu-id="446c4-105">Esta clase es la clase primaria para los eventos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="446c4-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="446c4-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="446c4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="446c4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="446c4-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="446c4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="446c4-108">Members</span></span>

<span data-ttu-id="446c4-109">La **clase TcpIp** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="446c4-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="446c4-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="446c4-110">Remarks</span></span>

<span data-ttu-id="446c4-111">Para habilitar eventos TCP/IP en una sesión de registro del kernel de NT, especifique la marca **\_ \_ \_ \_ TCPIP EVENT TRACE FLAG NETWORK** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="446c4-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="446c4-112">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos TCP/IP llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**TcpIpGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.*</span><span class="sxs-lookup"><span data-stu-id="446c4-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="446c4-113">Use los siguientes tipos de eventos para identificar el evento de red real (TCP/IP) al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="446c4-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="446c4-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="446c4-114">Event type</span></span>                                                            | <span data-ttu-id="446c4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="446c4-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="446c4-116">**EVENT \_ TRACE \_ TYPE \_ ACCEPT**(el valor del tipo de evento es 15)</span><span class="sxs-lookup"><span data-stu-id="446c4-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="446c4-117">Acepte el evento para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="446c4-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="446c4-118">La [**clase MOF \_ TcpIp TypeGroup2**](tcpip-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="446c4-119">**EVENT \_ TRACE \_ TYPE \_ CONNECT**(el valor del tipo de evento es 12)</span><span class="sxs-lookup"><span data-stu-id="446c4-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="446c4-120">Evento de conexión para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="446c4-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="446c4-121">La [**clase MOF \_ TcpIp TypeGroup2**](tcpip-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="446c4-122">**EVENT \_ TRACE \_ TYPE \_ DISCONNECT**(el valor del tipo de evento es 13)</span><span class="sxs-lookup"><span data-stu-id="446c4-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="446c4-123">Evento de desconexión para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="446c4-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="446c4-124">La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="446c4-125">**EVENT \_ TRACE \_ TYPE \_ RECEIVE**(el valor del tipo de evento es 11)</span><span class="sxs-lookup"><span data-stu-id="446c4-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="446c4-126">Evento de recepción para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="446c4-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="446c4-127">La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="446c4-128">**EVENTO \_ TRACE \_ TYPE \_ RECONNECT**(el valor del tipo de evento es 16)</span><span class="sxs-lookup"><span data-stu-id="446c4-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="446c4-129">Evento de reconexión para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="446c4-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="446c4-130">(Error en un intento de conexión y se realiza otro intento). La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="446c4-131">**EVENTO \_ TRACE \_ TYPE \_ RETRANSMIT**(el valor del tipo de evento es 14)</span><span class="sxs-lookup"><span data-stu-id="446c4-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="446c4-132">Evento de retransmisión para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="446c4-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="446c4-133">La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="446c4-134">**EVENTO \_ TRACE \_ TYPE \_ SEND**(el valor del tipo de evento es 10)</span><span class="sxs-lookup"><span data-stu-id="446c4-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="446c4-135">Enviar evento para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="446c4-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="446c4-136">La [**clase MOF TcpIp \_ SendIPV4**](tcpip-sendipv4.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="446c4-137">Valor del tipo de evento, 17</span><span class="sxs-lookup"><span data-stu-id="446c4-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="446c4-138">Evento de error.</span><span class="sxs-lookup"><span data-stu-id="446c4-138">Fail event.</span></span> <span data-ttu-id="446c4-139">La [**clase MOF TcpIp \_ Fail**](tcpip-fail.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="446c4-140">Valor del tipo de evento, 18</span><span class="sxs-lookup"><span data-stu-id="446c4-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="446c4-141">Evento de copia TCP para el protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="446c4-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="446c4-142">La [**clase MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="446c4-143">Valor del tipo de evento, 26</span><span class="sxs-lookup"><span data-stu-id="446c4-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="446c4-144">Enviar evento para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="446c4-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="446c4-145">La [**clase MOF TcpIp \_ SendIPV6**](tcpip-sendipv6.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="446c4-146">Valor de tipo de evento, 27</span><span class="sxs-lookup"><span data-stu-id="446c4-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="446c4-147">Evento de recepción para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="446c4-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="446c4-148">La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="446c4-149">Valor de tipo de evento, 28</span><span class="sxs-lookup"><span data-stu-id="446c4-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="446c4-150">Evento de conexión para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="446c4-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="446c4-151">La [**clase MOF \_ TcpIp TypeGroup4**](tcpip-typegroup4.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="446c4-152">Valor de tipo de evento, 29</span><span class="sxs-lookup"><span data-stu-id="446c4-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="446c4-153">Evento de desconexión para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="446c4-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="446c4-154">La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="446c4-155">Valor de tipo de evento, 30</span><span class="sxs-lookup"><span data-stu-id="446c4-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="446c4-156">Evento de retransmisión para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="446c4-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="446c4-157">La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="446c4-158">Valor de tipo de evento, 31</span><span class="sxs-lookup"><span data-stu-id="446c4-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="446c4-159">Acepte el evento para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="446c4-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="446c4-160">La [**clase MOF \_ TcpIp TypeGroup4**](tcpip-typegroup4.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="446c4-161">Valor de tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="446c4-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="446c4-162">Evento de reconexión para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="446c4-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="446c4-163">(Error en un intento de conexión y se realiza otro intento). La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="446c4-164">Valor de tipo de evento, 34</span><span class="sxs-lookup"><span data-stu-id="446c4-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="446c4-165">Evento de copia TCP para el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="446c4-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="446c4-166">La [**clase MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="446c4-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="446c4-167">Puede realizar un seguimiento de los eventos de red a un proceso de origen y destino mediante la **propiedad ProcessId.**</span><span class="sxs-lookup"><span data-stu-id="446c4-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="446c4-168">Dado que algunos eventos de red se registran mediante subprocesos independientes, es posible que no pueda usar los miembros **ProcessId** y **ThreadId** de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar el proceso o subproceso que originó las actividades de red.</span><span class="sxs-lookup"><span data-stu-id="446c4-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="446c4-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="446c4-169">Requirements</span></span>



| <span data-ttu-id="446c4-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="446c4-170">Requirement</span></span> | <span data-ttu-id="446c4-171">Valor</span><span class="sxs-lookup"><span data-stu-id="446c4-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="446c4-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="446c4-172">Minimum supported client</span></span><br/> | <span data-ttu-id="446c4-173">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="446c4-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="446c4-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="446c4-174">Minimum supported server</span></span><br/> | <span data-ttu-id="446c4-175">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="446c4-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="446c4-176">Consulte también</span><span class="sxs-lookup"><span data-stu-id="446c4-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="446c4-177">**SystemTrace de MSNT \_**</span><span class="sxs-lookup"><span data-stu-id="446c4-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="446c4-178">**Error \_ de TcpIp**</span><span class="sxs-lookup"><span data-stu-id="446c4-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="446c4-179">**TcpIp \_ SendIPV4**</span><span class="sxs-lookup"><span data-stu-id="446c4-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="446c4-180">**TcpIp \_ SendIPV6**</span><span class="sxs-lookup"><span data-stu-id="446c4-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="446c4-181">**TcpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="446c4-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="446c4-182">**TcpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="446c4-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="446c4-183">**TcpIp \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="446c4-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="446c4-184">**TcpIp \_ TypeGroup4**</span><span class="sxs-lookup"><span data-stu-id="446c4-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="446c4-185">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="446c4-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="446c4-186">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="446c4-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
