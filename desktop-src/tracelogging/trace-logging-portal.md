---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103796384"
---
# <a name="tracelogging"></a><span data-ttu-id="c9f65-103">TraceLogging</span><span class="sxs-lookup"><span data-stu-id="c9f65-103">TraceLogging</span></span>

## <a name="purpose"></a><span data-ttu-id="c9f65-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="c9f65-104">Purpose</span></span>

<span data-ttu-id="c9f65-105">TraceLogging es el nuevo marco de seguimiento de eventos de Windows 10 para aplicaciones en modo de usuario y controladores de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="c9f65-105">TraceLogging is the new Windows 10 event tracing framework for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="c9f65-106">TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.</span><span class="sxs-lookup"><span data-stu-id="c9f65-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c9f65-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c9f65-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9f65-108">Tema</span><span class="sxs-lookup"><span data-stu-id="c9f65-108">Topic</span></span></th>
<th><span data-ttu-id="c9f65-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9f65-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9f65-110"><a href="trace-logging-about.md">Acerca de TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="c9f65-110"><a href="trace-logging-about.md">About TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="c9f65-111">TraceLogging es el nuevo seguimiento de eventos de Windows 10 para aplicaciones en modo de usuario y controladores de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="c9f65-111">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="c9f65-112">TraceLogging es un formato para el seguimiento de eventos autodescriptivo para Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="c9f65-112">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="c9f65-113">TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.</span><span class="sxs-lookup"><span data-stu-id="c9f65-113">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9f65-114"><a href="tracelogging-using-tracelogging.md">Usar TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="c9f65-114"><a href="tracelogging-using-tracelogging.md">Using TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="c9f65-115">En los temas siguientes se proporciona una guía de inicio rápido de TraceLogging para código nativo y administrado, con ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c9f65-115">The following topics provide a TraceLogging quick start for native and managed code, with examples.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9f65-116"><a href="trace-logging-reference.md">Referencia de TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="c9f65-116"><a href="trace-logging-reference.md">TraceLogging Reference</a></span></span><br/></td>
<td><span data-ttu-id="c9f65-117">En los temas siguientes se proporciona información sobre la API de TraceLogging nativa.</span><span class="sxs-lookup"><span data-stu-id="c9f65-117">The following topics provide information about the native TraceLogging API.</span></span><br/> <span data-ttu-id="c9f65-118">TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.</span><span class="sxs-lookup"><span data-stu-id="c9f65-118">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="c9f65-119">TraceLogging permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.</span><span class="sxs-lookup"><span data-stu-id="c9f65-119">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span><br/> <span data-ttu-id="c9f65-120"><span class="underline">Para desarrolladores de WinRT</span></span><span class="sxs-lookup"><span data-stu-id="c9f65-120"><span class="underline">For WinRT developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="c9f65-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> se ha ampliado en Windows 10 para que registre los eventos de seguimiento de eventos para Windows (ETW) autodescriptivos sin necesidad de un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c9f65-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span></li>
<li><span data-ttu-id="c9f65-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> se ha ampliado en Windows 10 para proporcionar métodos de inicio y detención de actividad que proporcionan control sobre el formato y el contenido de los eventos de inicio y detención.</span><span class="sxs-lookup"><span data-stu-id="c9f65-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="c9f65-123">Además, las actividades se pueden anidar.</span><span class="sxs-lookup"><span data-stu-id="c9f65-123">Additionally, activities can be nested.</span></span></li>
</ul><span data-ttu-id="c9f65-124">
<span class="underline">Para desarrolladores de código administrado (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="c9f65-124">
<span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="c9f65-125">La clase <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> incluida con versiones anteriores de la .NET Framework ya admite la escritura de eventos ETW sin necesidad de un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c9f65-125">The <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="c9f65-126">Sin embargo, los desarrolladores debían usar EventSource como clase base y agregar atributos y métodos a la clase derivada que se han convertido en un manifiesto ETW automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c9f65-126">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="c9f65-127">Ahora, los desarrolladores no tienen que derivar de EventSource y, en su lugar, pueden usar EventSource directamente para registrar eventos autodescriptivos que no requieren un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c9f65-127">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span></li>
</ul><span data-ttu-id="c9f65-128">
<span class="underline">Para desarrolladores de C/C++</span></span><span class="sxs-lookup"><span data-stu-id="c9f65-128">
<span class="underline">For C/C++ developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="c9f65-129">TraceLoggingProvider. h es la API recomendada para desarrolladores de C/C++ en modo de usuario o kernel.</span><span class="sxs-lookup"><span data-stu-id="c9f65-129">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="c9f65-130">Esta API no es muy adecuada para su uso en escenarios dinámicos (con scripts) como JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c9f65-130">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="c9f65-131">En los vínculos siguientes se describe la API de C/C++.</span><span class="sxs-lookup"><span data-stu-id="c9f65-131">The following links describe the C/C++ API.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a><span data-ttu-id="c9f65-132">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="c9f65-132">Developer audience</span></span>

<span data-ttu-id="c9f65-133">TraceLogging está diseñado para que lo usen los desarrolladores de aplicaciones en modo de usuario y los desarrolladores de controladores en modo kernel que deseen agregar seguimiento a su código.</span><span class="sxs-lookup"><span data-stu-id="c9f65-133">TraceLogging is designed for use by user-mode application developers and kernel-mode driver developers who want to add tracing to their code.</span></span>

