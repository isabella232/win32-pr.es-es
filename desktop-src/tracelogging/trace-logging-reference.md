---
title: Referencia del registro de seguimiento
description: En los temas siguientes se proporciona información sobre la API tracelogging nativa. TraceLogging se basa en el seguimiento de eventos Windows (ETW) y proporciona una manera simplificada de instrumentar el código.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6563186411ace599f249220b9fd44b9ee4c682fdebd1391b4a3027a87c3482e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349995"
---
# <a name="tracelogging-reference"></a>Referencia del registro de seguimiento

En los temas siguientes se proporciona información sobre la API tracelogging nativa.

TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código. TraceLogging permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.

<span class="underline">Para desarrolladores de WinRT</span>

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) se ha ampliado en Windows 10 para registrar el seguimiento de eventos autodescripto para eventos Windows (ETW) sin necesidad de un manifiesto.
-   [**LoggingActivity se**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) ha ampliado en Windows 10 para proporcionar métodos de inicio y de detección de actividad que proporcionan control sobre el formato y el contenido de los eventos Start y Stop. Además, las actividades se pueden anidar.

<span class="underline">Para desarrolladores de código administrado (Microsoft .NET Framework)</span>

-   La [clase EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) que se incluye con versiones anteriores del .NET Framework ya admite la escritura de eventos ETW sin necesidad de un manifiesto. Sin embargo, los desarrolladores tenían que usar EventSource como clase base y agregar atributos y métodos a la clase derivada que se convertían automáticamente en un manifiesto ETW. Ahora, los desarrolladores no tienen que derivar de EventSource y, en su lugar, pueden usar EventSource directamente para registrar eventos autodescriptos que no requieren un manifiesto.

<span class="underline">Para desarrolladores de C/C++</span>

-   TraceLoggingProvider.h es la API recomendada para desarrolladores de C/C++ en modo de usuario o kernel. Esta API no es adecuada para su uso en escenarios dinámicos (con script), como Javascript. Los vínculos siguientes describen la API de C/C++.

<!-- -->

-   [Clases](trace-logging-classes.md)
-   [Funciones](trace-logging-functions.md)
-   [Macros](trace-logging-macros.md)

Tenga en cuenta que el valor de WINVER afectará a la forma en que se comporta TraceLoggingProvider.h.

-   Si WINVER no se establece antes de incluir <windows.h>, <windows.h> establecerá WINVER en un valor predeterminado correspondiente a la versión del SDK.
-   Con TraceLoggingProvider.h con WINVER establecido en 0x0602 (Windows 8) o posterior, el programa no se ejecutará en Windows Vista o Windows 7.
-   Con TraceLoggingProvider.h con WINVER establecido en 0x0600 (Windows Vista) o 0x0601 (Windows 7), el programa se configurará por compatibilidad y funcionará en las versiones especificadas de Windows.

 

 