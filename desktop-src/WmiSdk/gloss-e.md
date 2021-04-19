---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd162feb3936712b396db016de036f78aea35a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707094"
---
# <a name="e-wmi"></a><span data-ttu-id="a4e41-103">E (WMI)</span><span class="sxs-lookup"><span data-stu-id="a4e41-103">E (WMI)</span></span>

<span data-ttu-id="a4e41-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [o](gloss-o.md) [p](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [s](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="a4e41-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a4e41-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**Event (clase)**</span><span class="sxs-lookup"><span data-stu-id="a4e41-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**event class**</span></span>
</dt> <dd>

<span data-ttu-id="a4e41-106">Una clase WMI a la que los *consumidores de eventos* pueden suscribirse mediante una *consulta de evento*.</span><span class="sxs-lookup"><span data-stu-id="a4e41-106">A WMI class that *event consumers* can subscribe to by an *event query*.</span></span> <span data-ttu-id="a4e41-107">La clase informa de un tipo específico de repetición.</span><span class="sxs-lookup"><span data-stu-id="a4e41-107">The class reports a specific type of occurrence.</span></span> <span data-ttu-id="a4e41-108">Por ejemplo, la [**clase \_ ProcessStopTrace de Win32**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) informa de que se ha detenido un proceso específico.</span><span class="sxs-lookup"><span data-stu-id="a4e41-108">For example, the [**Win32\_ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) class reports that a specific process has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="a4e41-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**consumidor de eventos**</span><span class="sxs-lookup"><span data-stu-id="a4e41-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**event consumer**</span></span>
</dt> <dd>

<span data-ttu-id="a4e41-110">Destinatario de las notificaciones que informan de la aparición de un evento.</span><span class="sxs-lookup"><span data-stu-id="a4e41-110">A recipient of notifications that report an occurrence of an event.</span></span> <span data-ttu-id="a4e41-111">Un consumidor de eventos es [*temporal*](gloss-t.md) o [*permanente*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="a4e41-111">An event consumer is either [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4e41-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**proveedor de consumidor de eventos**</span><span class="sxs-lookup"><span data-stu-id="a4e41-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**event consumer provider**</span></span>
</dt> <dd>

<span data-ttu-id="a4e41-113">Proveedor que determina qué consumidor de evento permanente controla un evento determinado.</span><span class="sxs-lookup"><span data-stu-id="a4e41-113">A provider that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="a4e41-114">Un proveedor de consumidor de eventos se registra con WMI mediante una instancia de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), que contiene una lista de las clases de [*consumidor lógicas*](gloss-l.md) que admite el proveedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="a4e41-114">An event consumer provider is registered with WMI by an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), which contains a list of the [*logical consumer*](gloss-l.md) classes that the event consumer provider supports.</span></span> <span data-ttu-id="a4e41-115">Un proveedor de consumidores de eventos es un servidor COM que asigna [*consumidores físicos*](gloss-p.md) a los *consumidores lógicos*.</span><span class="sxs-lookup"><span data-stu-id="a4e41-115">An event consumer provider is a COM server that maps [*physical consumers*](gloss-p.md) to *logical consumers*.</span></span> <span data-ttu-id="a4e41-116">Un proveedor de consumidores de eventos admite la interfaz [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) y es un componente de la arquitectura de consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="a4e41-116">An event consumer provider supports the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface and is a component of the permanent consumer architecture.</span></span>

</dd> <dt>

<span data-ttu-id="a4e41-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**filtro de eventos**</span><span class="sxs-lookup"><span data-stu-id="a4e41-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**event filter**</span></span>
</dt> <dd>

<span data-ttu-id="a4e41-118">Instancia de la clase del sistema [**\_ \_ EventFilter**](--eventfilter.md) que describe un tipo de evento y las condiciones para entregar una notificación.</span><span class="sxs-lookup"><span data-stu-id="a4e41-118">An instance of the [**\_\_EventFilter**](--eventfilter.md) system class that describes an event type and the conditions for delivering a notification.</span></span> <span data-ttu-id="a4e41-119">Un consumidor utiliza un filtro de eventos para registrarse para recibir notificaciones de un tipo específico de evento.</span><span class="sxs-lookup"><span data-stu-id="a4e41-119">A consumer uses an event filter to register to receive notification of a specific type of event.</span></span>

</dd> <dt>

<span data-ttu-id="a4e41-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**proveedor de eventos**</span><span class="sxs-lookup"><span data-stu-id="a4e41-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**event provider**</span></span>
</dt> <dd>

<span data-ttu-id="a4e41-121">Proveedor WMI que supervisa un origen de eventos y notifica a WMI cuando se producen eventos.</span><span class="sxs-lookup"><span data-stu-id="a4e41-121">A WMI provider that monitors a source of events and notifies WMI when events occur.</span></span> <span data-ttu-id="a4e41-122">Un proveedor de eventos implementa las interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) y [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) y, a veces, [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span><span class="sxs-lookup"><span data-stu-id="a4e41-122">An event provider implements the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interfaces, and sometimes [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span></span>

</dd> <dt>

<span data-ttu-id="a4e41-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**consulta de evento**</span><span class="sxs-lookup"><span data-stu-id="a4e41-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**event query**</span></span>
</dt> <dd>

<span data-ttu-id="a4e41-124">Una instrucción [*lenguaje de consulta de WMI*](gloss-w.md) que los consumidores de eventos utilizan para registrarse y recibir notificaciones de eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="a4e41-124">A [*WMI Query Language*](gloss-w.md) statement that event consumers use to register to receive notification of specific events.</span></span> <span data-ttu-id="a4e41-125">Un proveedor de eventos utiliza una consulta de eventos para registrarse y generar notificaciones de eventos concretos.</span><span class="sxs-lookup"><span data-stu-id="a4e41-125">An event provider uses an event query to register to generate notifications of specific events.</span></span>

</dd> <dt>

<span data-ttu-id="a4e41-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**esquema de extensión**</span><span class="sxs-lookup"><span data-stu-id="a4e41-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**extension schema**</span></span>
</dt> <dd>

<span data-ttu-id="a4e41-127">La tercera capa del [*esquema CIM*](gloss-c.md), que incluye extensiones específicas de la plataforma del esquema CIM como Windows, UNIX y Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a4e41-127">The third layer of the [*CIM schema*](gloss-c.md), which includes platform-specific extensions of the CIM schema such as Windows, UNIX, and Exchange Server.</span></span> <span data-ttu-id="a4e41-128">Vea también modelo [*común*](gloss-c.md) y modelo básico.</span><span class="sxs-lookup"><span data-stu-id="a4e41-128">Also see [*common model*](gloss-c.md) and core model.</span></span>

</dd> <dt>

<span data-ttu-id="a4e41-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**evento extrínseco**</span><span class="sxs-lookup"><span data-stu-id="a4e41-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**extrinsic event**</span></span>
</dt> <dd>

<span data-ttu-id="a4e41-130">Una notificación de eventos de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="a4e41-130">An event notification from a provider.</span></span> <span data-ttu-id="a4e41-131">La mayoría de los proveedores crean una instancia de una clase de eventos definida en los archivos MOF del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a4e41-131">Most providers create an instance of an event class defined in the provider MOF files.</span></span> <span data-ttu-id="a4e41-132">Un evento extrínseco hereda de [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="a4e41-132">An extrinsic event inherits from [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span> <span data-ttu-id="a4e41-133">Por ejemplo, el [proveedor de registro de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) define la clase de eventos [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="a4e41-133">For example, the [Event Log Provider](/previous-versions/windows/desktop/eventlogprov/event-log-provider) defines the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="a4e41-134">Vea también el [*evento intrínseco*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="a4e41-134">Also see [*intrinsic event*](gloss-i.md).</span></span>

</dd> </dl>

 

 
