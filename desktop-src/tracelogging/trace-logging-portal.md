---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20f14980646680e0f6a0418470416801240ca17
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473121"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Propósito

TraceLogging es el nuevo marco Windows 10 de seguimiento de eventos para aplicaciones en modo de usuario y controladores en modo kernel. TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="trace-logging-about.md">Acerca de TraceLogging</a><br /> | TraceLogging es la nueva Windows 10 de eventos para aplicaciones en modo de usuario y controladores en modo kernel. TraceLogging es un formato para autodescriptar el seguimiento de eventos para Windows (ETW). TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.<br /> | 
| <a href="tracelogging-using-tracelogging.md">Uso de TraceLogging</a><br /> | En los temas siguientes se proporciona un inicio rápido de TraceLogging para código nativo y administrado, con ejemplos.<br /> | 
| <a href="trace-logging-reference.md">Referencia del registro de seguimiento</a><br /> | En los temas siguientes se proporciona información sobre la API tracelogging nativa.<br /> TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código. TraceLogging permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.<br /><span class="underline">Para desarrolladores de WinRT</span><br /><ul><li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> se ha ampliado en Windows 10 para registrar el seguimiento de eventos autodescripto para eventos Windows (ETW) sin necesidad de un manifiesto.</li><li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity se</strong></a> ha ampliado en Windows 10 para proporcionar métodos de inicio y de detección de actividad que proporcionan control sobre el formato y el contenido de los eventos Start y Stop. Además, las actividades se pueden anidar.</li></ul><span class="underline">Para desarrolladores de código administrado (Microsoft .NET Framework)</span><br /><ul><li>La <a href="/dotnet/api/system.diagnostics.tracing.eventsource">clase EventSource</a> que se incluye con versiones anteriores del .NET Framework ya admite la escritura de eventos ETW sin necesidad de un manifiesto. Sin embargo, los desarrolladores tenían que usar EventSource como clase base y agregar atributos y métodos a la clase derivada que se convertían automáticamente en un manifiesto ETW. Ahora, los desarrolladores no tienen que derivar de EventSource y, en su lugar, pueden usar EventSource directamente para registrar eventos autodescriptos que no requieren un manifiesto.</li></ul><span class="underline">Para desarrolladores de C/C++</span><br /><ul><li>TraceLoggingProvider.h es la API recomendada para desarrolladores de C/C++ en modo de usuario o kernel. Esta API no es adecuada para su uso en escenarios dinámicos (con script), como Javascript. Los vínculos siguientes describen la API de C/C++.</li></ul> | 




 

## <a name="developer-audience"></a>Audiencia de desarrolladores

TraceLogging está diseñado para su uso por parte de desarrolladores de aplicaciones en modo de usuario y desarrolladores de controladores en modo kernel que desean agregar seguimiento a su código.

