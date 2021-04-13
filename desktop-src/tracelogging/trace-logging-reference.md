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
# <a name="tracelogging-reference"></a>Referencia de TraceLogging

En los temas siguientes se proporciona información sobre la API de TraceLogging nativa.

TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código. TraceLogging permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.

<span class="underline">Para desarrolladores de WinRT</span>

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) se ha ampliado en Windows 10 para que registre los eventos de seguimiento de eventos para Windows (ETW) autodescriptivos sin necesidad de un manifiesto.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) se ha ampliado en Windows 10 para proporcionar métodos de inicio y detención de actividad que proporcionan control sobre el formato y el contenido de los eventos de inicio y detención. Además, las actividades se pueden anidar.

<span class="underline">Para desarrolladores de código administrado (Microsoft .NET Framework)</span>

-   La clase [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) incluida con versiones anteriores de la .NET Framework ya admite la escritura de eventos ETW sin necesidad de un manifiesto. Sin embargo, los desarrolladores debían usar EventSource como clase base y agregar atributos y métodos a la clase derivada que se han convertido en un manifiesto ETW automáticamente. Ahora, los desarrolladores no tienen que derivar de EventSource y, en su lugar, pueden usar EventSource directamente para registrar eventos autodescriptivos que no requieren un manifiesto.

<span class="underline">Para desarrolladores de C/C++</span>

-   TraceLoggingProvider. h es la API recomendada para desarrolladores de C/C++ en modo de usuario o kernel. Esta API no es muy adecuada para su uso en escenarios dinámicos (con scripts) como JavaScript. En los vínculos siguientes se describe la API de C/C++.

<!-- -->

-   [Clases](trace-logging-classes.md)
-   [Funciones](trace-logging-functions.md)
-   [Macros](trace-logging-macros.md)

Tenga en cuenta que el valor de WINVER afectará a la forma en que se comporta TraceLoggingProvider. h.

-   Si no se establece WINVER antes de incluir <Windows. h>, <Windows. h> establecerá WINVER en un valor predeterminado que se corresponda con la versión del SDK.
-   Si usa TraceLoggingProvider. h con WINVER establecido en 0x0602 (Windows 8) o superior, el programa no se ejecutará en Windows Vista o Windows 7.
-   Si usa TraceLoggingProvider. h con WINVER establecido en 0x0600 (Windows Vista) o 0x0601 (Windows 7), el programa se configurará para ofrecer compatibilidad y funcionará en las versiones especificadas de Windows.

 

 