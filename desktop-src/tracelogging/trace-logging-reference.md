---
title: Referencia de TraceLogging
description: En los temas siguientes se proporciona información sobre la API de TraceLogging nativa. TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421336"
---
# <a name="tracelogging-reference"></a><span data-ttu-id="14931-103">Referencia de TraceLogging</span><span class="sxs-lookup"><span data-stu-id="14931-103">TraceLogging Reference</span></span>

<span data-ttu-id="14931-104">En los temas siguientes se proporciona información sobre la API de TraceLogging nativa.</span><span class="sxs-lookup"><span data-stu-id="14931-104">The following topics provide information about the native TraceLogging API.</span></span>

<span data-ttu-id="14931-105">TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.</span><span class="sxs-lookup"><span data-stu-id="14931-105">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="14931-106">TraceLogging permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.</span><span class="sxs-lookup"><span data-stu-id="14931-106">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span>

<span data-ttu-id="14931-107"><span class="underline">Para desarrolladores de WinRT</span></span><span class="sxs-lookup"><span data-stu-id="14931-107"><span class="underline">For WinRT developers</span></span></span>

-   <span data-ttu-id="14931-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) se ha ampliado en Windows 10 para que registre los eventos de seguimiento de eventos para Windows (ETW) autodescriptivos sin necesidad de un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="14931-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span>
-   <span data-ttu-id="14931-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) se ha ampliado en Windows 10 para proporcionar métodos de inicio y detención de actividad que proporcionan control sobre el formato y el contenido de los eventos de inicio y detención.</span><span class="sxs-lookup"><span data-stu-id="14931-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="14931-110">Además, las actividades se pueden anidar.</span><span class="sxs-lookup"><span data-stu-id="14931-110">Additionally, activities can be nested.</span></span>

<span data-ttu-id="14931-111"><span class="underline">Para desarrolladores de código administrado (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="14931-111"><span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span>

-   <span data-ttu-id="14931-112">La clase [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) incluida con versiones anteriores de la .NET Framework ya admite la escritura de eventos ETW sin necesidad de un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="14931-112">The [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="14931-113">Sin embargo, los desarrolladores debían usar EventSource como clase base y agregar atributos y métodos a la clase derivada que se han convertido en un manifiesto ETW automáticamente.</span><span class="sxs-lookup"><span data-stu-id="14931-113">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="14931-114">Ahora, los desarrolladores no tienen que derivar de EventSource y, en su lugar, pueden usar EventSource directamente para registrar eventos autodescriptivos que no requieren un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="14931-114">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span>

<span data-ttu-id="14931-115"><span class="underline">Para desarrolladores de C/C++</span></span><span class="sxs-lookup"><span data-stu-id="14931-115"><span class="underline">For C/C++ developers</span></span></span>

-   <span data-ttu-id="14931-116">TraceLoggingProvider. h es la API recomendada para desarrolladores de C/C++ en modo de usuario o kernel.</span><span class="sxs-lookup"><span data-stu-id="14931-116">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="14931-117">Esta API no es muy adecuada para su uso en escenarios dinámicos (con scripts) como JavaScript.</span><span class="sxs-lookup"><span data-stu-id="14931-117">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="14931-118">En los vínculos siguientes se describe la API de C/C++.</span><span class="sxs-lookup"><span data-stu-id="14931-118">The following links describe the C/C++ API.</span></span>

<!-- -->

-   [<span data-ttu-id="14931-119">Clases</span><span class="sxs-lookup"><span data-stu-id="14931-119">Classes</span></span>](trace-logging-classes.md)
-   [<span data-ttu-id="14931-120">Funciones</span><span class="sxs-lookup"><span data-stu-id="14931-120">Functions</span></span>](trace-logging-functions.md)
-   [<span data-ttu-id="14931-121">Macros</span><span class="sxs-lookup"><span data-stu-id="14931-121">Macros</span></span>](trace-logging-macros.md)

<span data-ttu-id="14931-122">Tenga en cuenta que el valor de WINVER afectará a la forma en que se comporta TraceLoggingProvider. h.</span><span class="sxs-lookup"><span data-stu-id="14931-122">Note that the value of WINVER will impact the way TraceLoggingProvider.h behaves.</span></span>

-   <span data-ttu-id="14931-123">Si no se establece WINVER antes de incluir <Windows. h>, <Windows. h> establecerá WINVER en un valor predeterminado que se corresponda con la versión del SDK.</span><span class="sxs-lookup"><span data-stu-id="14931-123">If WINVER is not set before including <windows.h>, then <windows.h> will set WINVER to a default value corresponding to the SDK version.</span></span>
-   <span data-ttu-id="14931-124">Si usa TraceLoggingProvider. h con WINVER establecido en 0x0602 (Windows 8) o superior, el programa no se ejecutará en Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="14931-124">Using TraceLoggingProvider.h with WINVER set to 0x0602 (Windows 8) or higher, the program will not run on Windows Vista or Windows 7.</span></span>
-   <span data-ttu-id="14931-125">Si usa TraceLoggingProvider. h con WINVER establecido en 0x0600 (Windows Vista) o 0x0601 (Windows 7), el programa se configurará para ofrecer compatibilidad y funcionará en las versiones especificadas de Windows.</span><span class="sxs-lookup"><span data-stu-id="14931-125">Using TraceLoggingProvider.h with WINVER set to 0x0600 (Windows Vista) or 0x0601 (Windows 7), the program will be configured for compatibility and will work on the specified versions of Windows.</span></span>

 

 