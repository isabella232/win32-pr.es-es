---
description: Una sesión de seguimiento de eventos privados es una sesión de seguimiento de eventos de modo usuario que se ejecuta en el mismo proceso que sus proveedores de seguimiento de eventos&\# 8212; la sesión privada y los proveedores que habilita deben estar todos en el mismo proceso.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configurar e iniciar una sesión de registrador privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497711"
---
# <a name="configuring-and-starting-a-private-logger-session"></a><span data-ttu-id="9e8f7-103">Configurar e iniciar una sesión de registrador privado</span><span class="sxs-lookup"><span data-stu-id="9e8f7-103">Configuring and Starting a Private Logger Session</span></span>

<span data-ttu-id="9e8f7-104">Una sesión de seguimiento de eventos privados es una sesión de seguimiento de eventos de modo usuario que se ejecuta en el mismo proceso que sus proveedores de seguimiento de eventos: la sesión privada y los proveedores que habilita deben estar todos en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-104">A private event tracing session is a user-mode event tracing session that runs in the same process as its event trace providers—the private session and the providers that it enables must all be in the same process.</span></span> <span data-ttu-id="9e8f7-105">La ventaja de utilizar una sesión privada es que la sesión privada no cuenta con el máximo de 64 sesiones de seguimiento de eventos que se ejecutan simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-105">The benefit of using a private session is that the private session does not count against the maximum of 64 event tracing sessions executing simultaneously.</span></span>

<span data-ttu-id="9e8f7-106">Configurar e iniciar una sesión privada es similar a iniciar una sesión de seguimiento de eventos normal.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-106">Configuring and starting a private session is similar to starting a normal event trace session.</span></span> <span data-ttu-id="9e8f7-107">La diferencia es que el miembro **Wnode. GUID** de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) debe contener el **GUID** del proveedor, no la sesión, y el proveedor debe haber registrado ya el GUID.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-107">The difference is that **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure must contain the **GUID** of the provider, not the session, and the provider must have already registered the GUID.</span></span> <span data-ttu-id="9e8f7-108">Tenga en cuenta que si también establece el \_ seguimiento \_ de eventos privado \_ en \_ modo de registro de procedimientos, puede usar un **GUID** diferente para la sesión y el proveedor.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-108">Note that if you also set the EVENT\_TRACE\_PRIVATE\_IN\_PROC logging mode, you can use a different **GUID** for the session and provider.</span></span> <span data-ttu-id="9e8f7-109">Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos normal, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="9e8f7-109">For details on starting a normal event trace session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="9e8f7-110">Tenga en cuenta que no puede iniciar, detener o vaciar una sesión de seguimiento privada desde DllMain; debe hacerlo en las rutinas de inicialización y finalización de la DLL.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-110">Note that you cannot start, stop, or flush a private trace session from DllMain; you should do so in the initialization and finalization routines of the DLL.</span></span>

<span data-ttu-id="9e8f7-111">De Windows 8.1 a Windows 10, la versión 1607, los filtros de carga de eventos, ámbito y recorrido de pila se pueden usar en la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y en las estructuras de [**\_ \_ descriptor de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) y [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) para filtrar determinadas condiciones en una sesión del registrador.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-111">From Windows 8.1 to Windows 10, version 1607, event payload, scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="9e8f7-112">Para obtener más información sobre los filtros de carga de eventos, vea las funciones [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)y [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , así como las estructuras de [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **habilitar \_ \_ parámetros de seguimiento**, **\_ \_ descriptor de filtro de eventos** y filtro de carga.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-112">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="9e8f7-113">A partir de Windows 10, versión 1703, los usuarios con pocos privilegios ahora pueden iniciar una sesión de registrador privada en los procesos que han iniciado.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-113">Starting with Windows 10, version 1703, low privilege users can now start a private logger session in processes they started.</span></span> <span data-ttu-id="9e8f7-114">Ya no es necesario registrar el proveedor antes de habilitar o iniciar la sesión privada, lo que significa que el proveedor está "habilitado previamente" similar al de los proveedores de sesiones no privados.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-114">The provider no longer needs to be registered prior to enabling or starting the private session, meaning the provider is "pre-enabled" similar to how non-private session providers are.</span></span> <span data-ttu-id="9e8f7-115">Hay un límite de 8 registradores privados del sistema para un proceso individual.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-115">There is a limit of 8 system wide private loggers to an individual process.</span></span> <span data-ttu-id="9e8f7-116">Para mejorar el rendimiento en escenarios de proceso cruzado, se recomienda usar el filtrado para las API de sesión (incluidas [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)y [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) al iniciar un registrador de sistema privado.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-116">For increased performance in cross process scenarios, it's recommended to use filtering for session APIs (including [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) when starting a system wide private logger.</span></span> <span data-ttu-id="9e8f7-117">Tenga en cuenta que los mismos filtros se deben pasar a todas las API de sesión.</span><span class="sxs-lookup"><span data-stu-id="9e8f7-117">Note that the same filters should be passed to all session APIs.</span></span> <span data-ttu-id="9e8f7-118">Para obtener más información acerca de los filtros, consulte [**propiedades de seguimiento de eventos \_ \_ \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span><span class="sxs-lookup"><span data-stu-id="9e8f7-118">For more information about filters, see [**EVENT\_TRACE\_PROPERTIES\_V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span></span>

<span data-ttu-id="9e8f7-119">Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="9e8f7-119">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="9e8f7-120">Para obtener información detallada sobre cómo iniciar una sesión del registrador del kernel de NT, vea [configurar e iniciar la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="9e8f7-120">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="9e8f7-121">Para obtener más información sobre cómo iniciar una sesión del registrador global, vea [configurar e iniciar una sesión del registrador global](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="9e8f7-121">For details on starting a Global Logger session, see [Configuring and Starting a Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="9e8f7-122">Para obtener más información sobre cómo iniciar una sesión del registrador automático, vea [configurar e iniciar una sesión de registrador automático](configuring-and-starting-an-autologger-session.md).</span><span class="sxs-lookup"><span data-stu-id="9e8f7-122">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e8f7-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e8f7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e8f7-124">Configurar e iniciar una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="9e8f7-124">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="9e8f7-125">Configurar e iniciar una sesión de registrador automático</span><span class="sxs-lookup"><span data-stu-id="9e8f7-125">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="9e8f7-126">Configurar e iniciar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="9e8f7-126">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="9e8f7-127">Configuración e inicio de la sesión del registrador del kernel de NT</span><span class="sxs-lookup"><span data-stu-id="9e8f7-127">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="9e8f7-128">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="9e8f7-128">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="9e8f7-129">**HABILITAR \_ parámetros de seguimiento \_**</span><span class="sxs-lookup"><span data-stu-id="9e8f7-129">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="9e8f7-130">**\_propiedades de seguimiento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="9e8f7-130">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="9e8f7-131">**Propiedades de seguimiento de eventos \_ \_ \_ V2**</span><span class="sxs-lookup"><span data-stu-id="9e8f7-131">**EVENT\_TRACE\_PROPERTIES\_V2**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[<span data-ttu-id="9e8f7-132">**descriptor de filtro de eventos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e8f7-132">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="9e8f7-133">**\_predicado de filtro de carga \_**</span><span class="sxs-lookup"><span data-stu-id="9e8f7-133">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="9e8f7-134">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="9e8f7-134">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="9e8f7-135">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="9e8f7-135">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="9e8f7-136">Actualizar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="9e8f7-136">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
