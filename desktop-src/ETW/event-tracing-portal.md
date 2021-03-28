---
description: Esta documentación es para las aplicaciones de modo de usuario que desean usar ETW. Para obtener información acerca de la instrumentación de controladores de dispositivos que se ejecutan en el modo kernel, consulte seguimiento de software WPP y agregar seguimiento de eventos a controladores de Kernel-Mode en el kit de controladores de Windows (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361464"
---
# <a name="event-tracing"></a><span data-ttu-id="48cfb-104">Seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="48cfb-104">Event Tracing</span></span>

## <a name="purpose"></a><span data-ttu-id="48cfb-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="48cfb-105">Purpose</span></span>

<span data-ttu-id="48cfb-106">Seguimiento de eventos para Windows (ETW) proporciona a los programadores de aplicaciones la capacidad de iniciar y detener sesiones de seguimiento de eventos, instrumentar una aplicación para proporcionar eventos de seguimiento y consumir eventos de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="48cfb-106">Event Tracing for Windows (ETW) provides application programmers the ability to start and stop event tracing sessions, instrument an application to provide trace events, and consume trace events.</span></span> <span data-ttu-id="48cfb-107">Los eventos de seguimiento contienen un encabezado de evento y datos definidos por el proveedor que describen el estado actual de una aplicación u operación.</span><span class="sxs-lookup"><span data-stu-id="48cfb-107">Trace events contain an event header and provider-defined data that describes the current state of an application or operation.</span></span> <span data-ttu-id="48cfb-108">Puede usar los eventos para depurar una aplicación y realizar análisis de rendimiento y capacidad.</span><span class="sxs-lookup"><span data-stu-id="48cfb-108">You can use the events to debug an application and perform capacity and performance analysis.</span></span>

<span data-ttu-id="48cfb-109">Esta documentación es para las aplicaciones de modo de usuario que desean usar ETW.</span><span class="sxs-lookup"><span data-stu-id="48cfb-109">This documentation is for user-mode applications that want to use ETW.</span></span> <span data-ttu-id="48cfb-110">Para obtener información acerca de la instrumentación de controladores de dispositivos que se ejecutan en el modo kernel, consulte [seguimiento de software WPP](/windows-hardware/drivers/devtest/wpp-software-tracing) y [Agregar seguimiento de eventos a controladores de Kernel-Mode](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="48cfb-110">For information about instrumenting device drivers that run in kernel mode, see [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Adding Event Tracing to Kernel-Mode Drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="48cfb-111">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="48cfb-111">Where applicable</span></span>

<span data-ttu-id="48cfb-112">Use ETW cuando desee instrumentar la aplicación, registrar eventos de usuario o de kernel en un archivo de registro y consumir eventos de un archivo de registro o en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="48cfb-112">Use ETW when you want to instrument your application, log user or kernel events to a log file, and consume events from a log file or in real time.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="48cfb-113">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="48cfb-113">Developer audience</span></span>

<span data-ttu-id="48cfb-114">ETW está diseñado para desarrolladores de C y C++ que escriben aplicaciones en modo usuario.</span><span class="sxs-lookup"><span data-stu-id="48cfb-114">ETW is designed for C and C++ developers who write user-mode applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="48cfb-115">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="48cfb-115">Run-time requirements</span></span>

<span data-ttu-id="48cfb-116">ETW se incluye en Microsoft Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="48cfb-116">ETW is included in Microsoft Windows 2000 and later.</span></span> <span data-ttu-id="48cfb-117">Para obtener información acerca de los sistemas operativos necesarios para usar una función determinada, consulte la sección de requisitos de la documentación de la función.</span><span class="sxs-lookup"><span data-stu-id="48cfb-117">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="48cfb-118">Procesar seguimientos de ETW en código .NET</span><span class="sxs-lookup"><span data-stu-id="48cfb-118">Process ETW traces in .NET code</span></span>

<span data-ttu-id="48cfb-119">Puede usar la [API TraceProcessing de .net](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analizar seguimientos de ETW para las aplicaciones y otros componentes de software.</span><span class="sxs-lookup"><span data-stu-id="48cfb-119">You can use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="48cfb-120">Esta API se usa internamente en Microsoft para analizar los datos de ETW generados por Windows Engineering System y también se usa para potenciar varias tablas en el [analizador de rendimiento de Windows](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="48cfb-120">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="48cfb-121">Esta API está disponible como un paquete NuGet.</span><span class="sxs-lookup"><span data-stu-id="48cfb-121">This API is available as a NuGet package.</span></span>

<span data-ttu-id="48cfb-122">Para obtener más información, consulte [este artículo](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="48cfb-122">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="48cfb-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="48cfb-123">In this section</span></span>



| <span data-ttu-id="48cfb-124">Tema</span><span class="sxs-lookup"><span data-stu-id="48cfb-124">Topic</span></span>                                                                     | <span data-ttu-id="48cfb-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="48cfb-125">Description</span></span>                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="48cfb-126">Novedades del seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="48cfb-126">What's New in Event Tracing</span></span>](what-s-new-in-event-tracing.md)<br/> | <span data-ttu-id="48cfb-127">Nuevas características que se agregaron al seguimiento de eventos en cada versión.</span><span class="sxs-lookup"><span data-stu-id="48cfb-127">New features that were added to Event Tracing in each release.</span></span><br/>          |
| [<span data-ttu-id="48cfb-128">Acerca del seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="48cfb-128">About Event Tracing</span></span>](about-event-tracing.md)<br/>                 | <span data-ttu-id="48cfb-129">Información general sobre el seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="48cfb-129">General information about Event Tracing.</span></span><br/>                                |
| [<span data-ttu-id="48cfb-130">Usar el seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="48cfb-130">Using Event Tracing</span></span>](using-event-tracing.md)<br/>                 | <span data-ttu-id="48cfb-131">Temas relacionados con tareas que describen cómo usar la API ETW.</span><span class="sxs-lookup"><span data-stu-id="48cfb-131">Task-related topics that describe how to use the ETW API.</span></span><br/>               |
| [<span data-ttu-id="48cfb-132">Referencia de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="48cfb-132">Event Tracing Reference</span></span>](event-tracing-reference.md)<br/>         | <span data-ttu-id="48cfb-133">Descripciones detalladas de las funciones ETW y otros elementos de programación.</span><span class="sxs-lookup"><span data-stu-id="48cfb-133">Detailed descriptions of ETW functions and other programming elements.</span></span> <br/> |



 

 

 
